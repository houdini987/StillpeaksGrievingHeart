# Canon Authority

## Live Canon Rule

The authoritative source document for current Stillpeak canon is:

`Stillpeaks_Grieving_Heart_MASTER_Packets_1-5_v7_REFORMATTED.docx`

Version numbers in filenames such as `v7` are treated as authoritative live version markers.

## Git Source Rule

This repository is the durable source layer for exported canon.

- Markdown files under `canon/` are the repo-native canon source.
- Image files under `assets/images/` are the canonical visual assets for repo publishing.
- Exported `.docx` and `.pdf` files under `exports/` are derived artifacts, not the source of truth.

## Image Handling Rule

Embedded images from Word should be converted into standalone asset files whenever possible.
Until then, packet files may preserve image placement using explicit placeholders or future asset paths.
