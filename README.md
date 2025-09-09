# Workbench – Plugin Registry

Static registry used by the **Workbench** app to list and install plugins.

## Registry URL (paste this into Workbench)
`https://TateMat99.github.io/workbench-registry/registry/v1/index.json`

## Schema (v1)
Top-level:
- `registry_version`: string (e.g., "1")
- `plugins`: array of plugin objects

Plugin object:
- `id`: stable machine id, lowercase `a-z0-9-`
- `name`: display name
- `version`: SemVer
- `core_api`: compatibility specifier (e.g., ">=1.0,<2.0")
- `summary`: short description
- `wheel_url`: HTTPS URL to a `.whl` (GitHub Release asset)
- `sha256`: hex SHA-256 of the wheel
- `icon_url`: optional HTTPS URL (png/svg)
- `homepage`: repo
- `changelog`: releases page
- `author`: optional
- `license`: optional (e.g., MIT)
- `run_mode`: "tool" (acts only when invoked by the user) | "worker" (may operate continuously or asynchronously)

