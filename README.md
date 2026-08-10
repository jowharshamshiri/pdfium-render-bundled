# pdfium-render-bundled

A fork of [**`pdfium-render`** by Alastair Carey](https://github.com/ajrcarey/pdfium-render)
that links a statically built [PDFium](https://pdfium.googlesource.com/) instead
of loading a shared library at runtime.

**Upstream comes first.** The Rust bindings, the API, the documentation and
essentially all of the engineering in this crate are Alastair Carey's work.
This fork changes how the library is *linked* and almost nothing about how it is
*used*. If you are choosing a PDF crate, use
[`pdfium-render`](https://crates.io/crates/pdfium-render). If you have a
question about the API, upstream's documentation answers it, because the API is
theirs and unchanged. Bug reports about rendering, text extraction or the
binding layer belong upstream; only linking and packaging issues belong here.

## What is different, and why

`pdfium-render` binds to PDFium dynamically: your program finds `pdfium.dll`,
`libpdfium.so` or `libpdfium.dylib` at runtime, usually beside the executable.
That is a good default — it keeps the crate small, lets a user swap the PDFium
build, and avoids imposing a C++ toolchain on everyone who compiles it.

It is a poor fit for a program distributed as a single self-contained
executable. A loose shared library has to be shipped, installed next to the
binary, code-signed and notarised on macOS, and kept in step with the executable
that loads it — and when any of that goes wrong, the failure arrives at runtime,
in front of a user, as a missing-library error rather than as a build failure in
front of a developer.

This fork:

- links a **static** PDFium at build time, so there is one file to ship, sign
  and install, and a missing or mismatched PDFium is a compile error;
- resolves the library and headers through `pkg-config`, so the PDFium build is
  chosen by configuration rather than compiled in;
- keeps upstream's public API, so switching between the two is a dependency
  change rather than a rewrite.

That is the whole of the difference. It is a packaging decision, not an
improvement — upstream's dynamic linking is the better default for most people,
and this fork exists for the case where it is not.

## Using it

```toml
[dependencies.pdfium-render-bundled]
git = "https://github.com/jowharshamshiri/pdfium-render-bundled"
tag = "v1.469.4233"
```

The build needs a static PDFium discoverable through `pkg-config` — a
`pdfium.pc` naming the include path and the library. Any static build will do;
[`pdfium-bundle`](https://github.com/jowharshamshiri/pdfium_bundle) is one that
produces exactly that layout.

```bash
PKG_CONFIG_PATH=/path/to/pdfium/dist cargo build
```

PDFium is C++, so a C++ standard library is linked too; `pdfium.pc` records
which one the build expects.

For everything else — rendering pages to bitmaps, extracting text, editing and
creating documents — see
[upstream's documentation](https://docs.rs/pdfium-render/). The API here is
theirs.

## Keeping up with upstream

Upstream moves, and this fork should follow it rather than diverge. The changes
carried here are deliberately narrow — the linking strategy, the build script,
and the dependency metadata — so that merging a new upstream release stays a
small operation. If you find yourself wanting a feature, ask upstream for it
first; a fork that accumulates features is a fork that stops being mergeable.

## Licensing

This crate is a modified version of `pdfium-render`, which is copyright Alastair
Carey and dual-licensed **MIT OR Apache-2.0**. Those terms carry over to this
fork unchanged, and the modifications described above are noted here as
Apache-2.0 §4(b) requires. See `LICENSE.md`.

Note that linking PDFium brings its own obligations. PDFium is BSD 3-Clause and
its tree incorporates third-party libraries — FreeType, libjpeg-turbo,
libopenjpeg, libpng, zlib, Skia, Abseil and others — each under its own terms,
several with attribution requirements of their own. `LICENSE.md` explains this;
the authoritative list for any particular binary is the `LICENSE` file and
`third_party/` directory of the PDFium checkout it was built from.

This is a pointer, not legal advice.
