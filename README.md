# Instagram API Schema Diff Dataset

This repository contains version-to-version diffs of Instagram Android internal API schemas.

The diffs are generated from the file:

ig4a-instagram-schema_client_persist_ids.json

extracted from different Instagram Android application versions.

The version order is determined using the official values from `AndroidManifest.xml`:

- android:versionCode
- android:versionName

This ensures accurate chronological comparison between releases.

## Dataset Structure

Each entry represents the differences between two consecutive application versions.

Example structure:

version_diffs/
  index.json
  batch_0001_0100/
    0001__30122962_to_30155555/
      diff.json

Each `diff.json` contains:
- added operations
- removed operations
- changed operations
- updated `client_doc_id` values

## Purpose

This dataset is intended for:

- Security research
- Bug bounty research
- Monitoring changes in Instagram internal APIs
- Historical tracking of API evolution

## Notes

- The repository only contains generated diff data.
- No proprietary application binaries are included.
- All data is derived from publicly available application releases.

## Disclaimer

This repository is provided for **security research and educational purposes only**.

Instagram and Meta are trademarks of Meta Platforms, Inc.  
This project is not affiliated with or endorsed by Meta.