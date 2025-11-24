# Workbench Plugin Registry

minimal registry for discovering and installing Workbench plugins.
Workbench Repo : https://github.com/TateMat99/Workbench

## Endpoint
`https://tatemat99.github.io/Workbench-registry/registry/v1/index.json`

## Overview
- The registry is a single JSON document.
- It declares a registry version and a list of plugins.
- All downloadable assets **must** be served over HTTPS.

## Top-Level Schema
```json
{
  "registry_version": "1",
  "plugins": [ /* array of Plugin objects */ ]
}
```

## Plugin Object
```json
{
  "id": "color_picker",
  "name": "Color Picker",
  "version": "1.2.3",
  "author": "Optional Author",
  "summary": "Short, one-line description.",
  "wheel_url": "https://host/path/plugin-1.2.3-py3-none-any.whl",
  "icon_url": "https://host/path/icon.ico",
  "background_allowed": false
}
```

### Field Definitions
- **id** (string): Unique identifier, `a–z`, `0–9`, and `- , _`.
- **name** (string): Display name.
- **version** (string): Semantic Version.
- **author** (string, optional): Author.
- **summary** (string): Single sentence description.
- **wheel_url** (string, HTTPS): Direct link to a `.whl` file.
- **icon_url** (string, HTTPS, optional): PNG, SVG or ICO icon.
- **background_allowed** (boolean):  
  - `true` — plugin may operate in the background (e.g., watchers, schedulers).  
  - `false` — plugin runs **only** when explicitly invoked by the user.
