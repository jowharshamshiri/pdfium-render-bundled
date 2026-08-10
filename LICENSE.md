# Licence

## Attribution

This crate is a **modified version of `pdfium-render`**, copyright
**Alastair Carey** and contributors — <https://github.com/ajrcarey/pdfium-render>.

The Rust bindings, the public API and the great majority of the code here are
their work. The modifications carried by this fork are limited to how PDFium is
linked and located:

- PDFium is linked **statically at build time** rather than loaded as a shared
  library at runtime;
- the library and headers are discovered through `pkg-config`;
- the build script and dependency metadata changed accordingly.

This notice records those changes, as section 4(b) of the Apache License, 2.0
requires of a modified work.

## Terms

Licensed under either of

* Apache License, Version 2.0 (<http://www.apache.org/licenses/LICENSE-2.0>)
* MIT License (<http://opensource.org/licenses/MIT>)

at your option — the same dual licence upstream offers, carried over unchanged.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 licence, shall be
dual licensed as above, without any additional terms or conditions.

## PDFium

A binary built from this crate contains PDFium, which is **not** covered by the
licence above.

PDFium is copyright The PDFium Authors and is licensed under the BSD 3-Clause
licence. Redistributing a binary that contains it requires reproducing that
copyright notice, the licence conditions and the disclaimer in your
documentation or other materials.

PDFium is also not a single-licence work. Its source tree incorporates
third-party libraries — among them FreeType, libjpeg-turbo, libopenjpeg, libpng,
zlib, Skia and Abseil — each under its own licence, several of which carry their
own attribution requirements. A statically linked binary contains all of them.

This crate does not vendor PDFium, so the authoritative list of what went into
any particular binary is the `LICENSE` file and `third_party/` directory of the
PDFium checkout it was linked against. Generate any product notice file from
that checkout rather than from this document.

This summary is a pointer, not legal advice.
