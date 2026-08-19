# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased] - 2026-08-19

### Added

- Dataset "Data file" dropzones (create and post forms) now accept Excel files (`.xlsx`, `.xls`) in addition to CSV. Files continue to be uploaded to the API as-is, with no client-side parsing or conversion.
- `CHANGELOG.md` and a README note documenting the accepted dataset file formats.

### Changed

- Dropzone helper message for dataset files updated from "Drop a CSV file here to upload" to "Drop a data file (CSV or Excel) here to upload".

## [1.1.6] - 2022-03-17

### Added

- Initial commit (`3b0df4b`): ICJIA Research Hub Studio at v1.1.6 — a Vue 2 / Vuetify internal app for managing Research Hub contents (apps, articles, and datasets) against the Research Hub API, including dropzone-based file uploads (images, PDF, markdown, JSON, and CSV data files), content preview via `researchhub-lib`, and publish/status management.
