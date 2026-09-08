# Y2K Task Galaxy

An offline-first planner that can be hosted on GitHub Pages and installed as a progressive web app.

## Run locally

Open `index.html` in a browser for the basic planner. Service workers require a secure origin, so use a local server to test offline installation:

```text
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a GitHub repository.
2. Upload `index.html`, `manifest.json`, `sw.js`, and `icon.svg`.
3. Open **Settings > Pages**.
4. Select **Deploy from a branch**, choose the default branch and root folder, then save.
5. Open the generated HTTPS URL and install the app from the browser menu.

## Data and safety

Planner records and theme preferences are stored in the browser's local storage. They are not uploaded or synchronized between devices. Do not store passwords, payment data, or other sensitive information in tasks or notes.

The app has no server credentials or user authentication. Add a backend with authentication and server-side validation before introducing shared accounts or cloud sync.
