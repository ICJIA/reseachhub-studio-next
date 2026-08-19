# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased] - 2026-08-19

### Added

- Dataset "Data file" dropzones (create and post forms) now accept Excel files (`.xlsx`, `.xls`) in addition to CSV. Files continue to be uploaded to the API as-is, with no client-side parsing or conversion.
- `CHANGELOG.md` and a README note documenting the accepted dataset file formats.
- `.nvmrc` pinning Node 14.17.3 to match the Netlify build environment.

### Changed

- Dropzone helper message for dataset files updated from "Drop a CSV file here to upload" to "Drop a data file (CSV or Excel) here to upload".

### Fixed

- Netlify deploys failed during `npm install`: the abandoned `fibers` package (a build-speed optimization for Dart Sass) no longer compiles on current build images (Node 14's bundled node-gyp 5 is incompatible with Python 3.11+). Removed `fibers`; sass-loader automatically falls back to async Dart Sass, so no configuration changes were needed.

### Removed

- `brotli-webpack-plugin` and its native `iltorb` dependency: iltorb's prebuilt binaries are no longer downloadable and it fails to compile on current build images, which would have crashed the build step. Brotli precompression is unnecessary on Netlify, which compresses at the CDN edge; gzip (zopfli) precompression of assets remains in place.

## [1.1.6] - 2022-03-17

### Added

- Initial commit (`3b0df4b`): ICJIA Research Hub Studio at v1.1.6 — a Vue 2 / Vuetify internal app for managing Research Hub contents (apps, articles, and datasets) against the Research Hub API, including dropzone-based file uploads (images, PDF, markdown, JSON, and CSV data files), content preview via `researchhub-lib`, and publish/status management.
