# @sequential/app-tool-editor

Tool and plugin development environment with parameter definition, schema generation, and import management.

## Installation

```bash
npm install @sequential/app-tool-editor
```

## Features

- Integrated with Sequential Desktop environment
- Hot reload support for development
- Real-time collaboration via Zellous SDK
- Persistent state management

## Usage

This package is typically used as a desktop application. Load it in Sequential Desktop via the app registry.

```javascript
import manifest from './app-tool-editor/manifest.json';
// App automatically registers in desktop environment
```

## Manifest

Apps must export a `manifest.json` file:

```json
{{
  "id": "app-tool-editor",
  "name": "App Name",
  "version": "1.0.0",
  "icon": "📱",
  "entry": "dist/index.html",
  "capabilities": ["sequential-os"],
  "window": {{
    "defaultWidth": 800,
    "defaultHeight": 600,
    "resizable": true
  }}
}}
```

## Architecture

- **Frontend**: Single-page application in `dist/index.html`
- **State**: Persisted to localStorage with automatic restore
- **Communication**: WebSocket and HTTP APIs with Sequential Desktop
- **Components**: Built with vanilla JS or imported from @sequential/desktop-ui-components

## Related Packages

- [@sequential/desktop-shell](../desktop-shell) - Window manager and desktop UI
- [@sequential/desktop-ui-components](../desktop-ui-components) - Shared UI components
- [@sequential/zellous-client-sdk](../zellous-client-sdk) - Collaboration SDK

## License

MIT
