# Tasks PWA

A small browser-based task list demonstrating local storage, offline caching, notifications, and an installable web app manifest.

## Run locally

No build step or npm dependencies are required. From the repository root:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://localhost:8000`. Serve the app over HTTP on localhost or HTTPS; opening `index.html` directly does not provide the service-worker environment.

## How it works

- `index.html` contains the interface and task logic.
- Tasks are saved in browser `localStorage`.
- `service-worker.js` caches app resources for offline access after an initial load.
- `manifest.json` defines standalone installation and icons.
- Notifications require browser permission and platform support.

## Limitations

There is no backend or cross-device synchronization. Clearing browser storage removes saved tasks. The manifest uses an absolute `/index.html` start URL; adjust it when hosting under a subdirectory such as a GitHub Pages project path. This is a compact learning demo.
