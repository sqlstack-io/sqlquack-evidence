# SQLQuack evidence

Recorded database answers that back SQLQuack's syntax and translation checks.

- `syntax/<dialect>/` holds the SQL that was run (`cases/`) and whether the database accepted it (`receipts/`, with re-runs in `repeats/`).
- `convert/<dialect>/` holds translation cases (`cases/`) and the rows the source database returned (`results/`, named by case hash), with later re-recordings in `repeats/`.
- `referee/<dialect>/` holds type and signature checks (`cases/`, `results/`, `functions/`).

Files are only ever added or appended to. SQLQuack pins one commit of this repository in its `evidence.toml`, with the SHA-256 of its files, and its make targets fetch and verify that commit. No credentials, account names or raw query logs are stored here.
