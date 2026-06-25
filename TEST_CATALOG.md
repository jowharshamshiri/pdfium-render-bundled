# Rust Test Catalog

**Total Tests:** 59

**Numbered Tests:** 59

**Unnumbered Tests:** 0

**Numbered Tests Missing Descriptions:** 0

**Numbering Mismatches:** 0

All numbered test numbers are unique.

This catalog lists all tests in the Rust codebase.

| Test # | Function Name | Description | File |
|--------|---------------|-------------|------|
| test0001 | `test0001_readme_example` | TEST0001: Readme example | src/lib.rs:203 |
| test0002 | `test0002_dynamic_bindings` | TEST0002: Dynamic bindings | src/lib.rs:247 |
| test0003 | `test0003_static_bindings` | TEST0003: Static bindings | src/lib.rs:278 |
| test0004 | `test0004_reader_lifetime` | TEST0004: Reader lifetime | src/lib.rs:286 |
| test0005 | `test0005_is_true` | TEST0005: Is true | src/bindings.rs:9716 |
| test0006 | `test0006_unaligned_bgr_to_rgba` | Tests of color conversion functions. | src/utils.rs:490 |
| test0007 | `test0007_aligned_bgr_to_rgba` | TEST0007: Aligned bgr to rgba | src/utils.rs:503 |
| test0008 | `test0008_bgra_to_rgba` | TEST0008: Bgra to rgba | src/utils.rs:563 |
| test0009 | `test0009_rgb_to_bgra` | TEST0009: Rgb to bgra | src/utils.rs:576 |
| test0010 | `test0010_rgba_to_bgra` | TEST0010: Rgba to bgra | src/utils.rs:589 |
| test0011 | `test0011_aligned_grayscale_to_unaligned` | TEST0011: Aligned grayscale to unaligned | src/utils.rs:602 |
| test0012 | `test0012_date_time_to_pdf_date_string` | Tests of date time conversion functions. | src/utils.rs:613 |
| test0013 | `test0013_valid_utf16le_from_emoji` | TEST0013: Valid utf16le from emoji | src/utils.rs:637 |
| test0014 | `test0014_rect_is_inside` | TEST0014: Rect is inside | src/pdf/rect.rs:292 |
| test0015 | `test0015_rect_does_overlap` | TEST0015: Rect does overlap | src/pdf/rect.rs:311 |
| test0016 | `test0016_transform_rect` | TEST0016: Transform rect | src/pdf/rect.rs:324 |
| test0017 | `test0017_coordinate_space_order_guard` | TEST0017: Coordinate space order guard | src/pdf/rect.rs:347 |
| test0018 | `test0018_quadpoints_extents` | TEST0018: Quadpoints extents | src/pdf/quad_points.rs:354 |
| test0019 | `test0019_quadpoints_to_rect` | TEST0019: Quadpoints to rect | src/pdf/quad_points.rs:368 |
| test0020 | `test0020_points_ordering` | TEST0020: Points ordering | src/pdf/points.rs:204 |
| test0021 | `test0021_from_hex` | TEST0021: From hex | src/pdf/color.rs:381 |
| test0022 | `test0022_to_hex` | TEST0022: To hex | src/pdf/color.rs:398 |
| test0023 | `test0023_matrix_apply_to_points` | TEST0023: Matrix apply to points | src/pdf/matrix.rs:351 |
| test0024 | `test0024_link_rect` | TEST0024: Link rect | src/pdf/link.rs:120 |
| test0025 | `test0025_from_bytes` | TEST0025: From bytes | src/pdf/bitmap.rs:400 |
| test0026 | `test0026_point_transform` | TEST0026: Point transform | src/pdf/path/segment.rs:126 |
| test0027 | `test0027_point_transform_during_iteration` | TEST0027: Point transform during iteration | src/pdf/path/segment.rs:180 |
| test0028 | `test0028_page_rendering_reusing_bitmap` | TEST0028: Page rendering reusing bitmap | src/pdf/document/page.rs:1069 |
| test0029 | `test0029_rendered_image_dimension` | TEST0029: Rendered image dimension | src/pdf/document/page.rs:1100 |
| test0030 | `test0030_bookmarks` | TEST0030: Bookmarks | src/pdf/document/bookmark.rs:304 |
| test0031 | `test0031_page_size` | TEST0031: Page size | src/pdf/document/pages.rs:671 |
| test0032 | `test0032_page_sizes` | TEST0032: Page sizes | src/pdf/document/pages.rs:690 |
| test0033 | `test0033_apply_matrix` | TEST0033: Apply matrix | src/pdf/document/page/object.rs:1270 |
| test0034 | `test0034_reset_matrix_to_identity` | TEST0034: Reset matrix to identity | src/pdf/document/page/object.rs:1309 |
| test0035 | `test0035_transform_captured_in_content_regeneration` | TEST0035: Transform captured in content regeneration | src/pdf/document/page/object.rs:1350 |
| test0036 | `test0036_overlapping_chars_results` | TEST0036: Overlapping chars results | src/pdf/document/page/text.rs:429 |
| test0037 | `test0037_text_chars_results_equality` | TEST0037: Text chars results equality | src/pdf/document/page/text.rs:509 |
| test0038 | `test0038_cache_instantiation` | TEST0038: Cache instantiation | src/pdf/document/page/index_cache.rs:300 |
| test0039 | `test0039_get_and_set_index_for_page` | TEST0039: Get and set index for page | src/pdf/document/page/index_cache.rs:336 |
| test0040 | `test0040_get_invalid_page` | TEST0040: Get invalid page | src/pdf/document/page/index_cache.rs:530 |
| test0041 | `test0041_insert_pages_at_index` | TEST0041: Insert pages at index | src/pdf/document/page/index_cache.rs:572 |
| test0042 | `test0042_delete_pages_at_index` | TEST0042: Delete pages at index | src/pdf/document/page/index_cache.rs:739 |
| test0043 | `test0043_pathological_delete_all_pages` | TEST0043: Pathological delete all pages | src/pdf/document/page/index_cache.rs:890 |
| test0044 | `test0044_paragraph_construction` | TEST0044: Paragraph construction | src/pdf/document/page/paragraph.rs:870 |
| test0045 | `test0045_get_annotation_flags` | TEST0045: Get annotation flags | src/pdf/document/page/annotation/private.rs:597 |
| test0046 | `test0046_set_annotation_flags` | TEST0046: Set annotation flags | src/pdf/document/page/annotation/private.rs:633 |
| test0047 | `test0047_update_one_annotation_flag` | TEST0047: Update one annotation flag | src/pdf/document/page/annotation/private.rs:674 |
| test0048 | `test0048_get_form_field_flags` | TEST0048: Get form field flags | src/pdf/document/page/field/private.rs:534 |
| test0049 | `test0049_set_form_field_flags` | TEST0049: Set form field flags | src/pdf/document/page/field/private.rs:572 |
| test0050 | `test0050_update_one_form_field_flag` | TEST0050: Update one form field flag | src/pdf/document/page/field/private.rs:615 |
| test0051 | `test0051_object_get_translation` | TEST0051: Object get translation | src/pdf/document/page/object/private.rs:510 |
| test0052 | `test0052_object_get_scale` | TEST0052: Object get scale | src/pdf/document/page/object/private.rs:545 |
| test0053 | `test0053_object_get_rotation` | TEST0053: Object get rotation | src/pdf/document/page/object/private.rs:580 |
| test0054 | `test0054_object_get_skew` | TEST0054: Object get skew | src/pdf/document/page/object/private.rs:615 |
| test0055 | `test0055_page_image_object_retains_format` | TEST0055: Page image object retains format | src/pdf/document/page/object/image.rs:1006 |
| test0056 | `test0056_image_scaling_keeps_aspect_ratio` | TEST0056: Image scaling keeps aspect ratio | src/pdf/document/page/object/image.rs:1084 |
| test0057 | `test0057_group_bounds` | TEST0057: Group bounds | src/pdf/document/page/object/group.rs:1004 |
| test0058 | `test0058_group_text` | TEST0058: Group text | src/pdf/document/page/object/group.rs:1040 |
| test0059 | `test0059_group_apply` | TEST0059: Group apply | src/pdf/document/page/object/group.rs:1071 |
---

*Generated from Rust source tree*
*Total tests: 59*
*Total numbered tests: 59*
*Total unnumbered tests: 0*
*Total numbered tests missing descriptions: 0*
*Total numbering mismatches: 0*
