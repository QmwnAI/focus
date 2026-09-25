# Focus

A browser-based focus workspace built around a distraction-light timer, Pomodoro sessions, visual scenes, and optional music playback.

The project currently lives in a single `index.html` file, so it can be hosted as a simple static site without a backend.

## Features

### Focus timer
- Preset sessions: 25, 45, 60, and 90 minutes
- Custom focus duration
- Start, pause, reset, and complete-session controls
- Circular progress display
- Focus/fullscreen mode
- Session statistics

### Pomodoro
- Optional Pomodoro mode
- Configurable short breaks
- Configurable long breaks
- Four-session cycle tracking

### Visual scenes
Choose between:
- Night
- Sunset
- Forest
- Aurora

### Music
Focus currently supports:
- **YouTube** videos and playlists
- **Spotify** through Spotify's Web API / Web Playback SDK
- **Apple Music** through the embedded Apple Music player

> SomaFM was previously tested as an integrated radio source, but has been removed because its stream servers returned HTTP 403 responses when requested from the hosted Focus site.

### Local preferences
Where appropriate, settings such as volume and service configuration are stored in the browser using `localStorage`.

## Running Focus

Because Focus is a static web app, the simplest option is to open `index.html` in a browser.

For features that depend on web origins or OAuth, such as Spotify, run or host the page through HTTP/HTTPS rather than relying on a `file://` URL.

The repository can also be deployed directly with GitHub Pages.

## Spotify setup

Spotify integration requires a Spotify Developer application.

1. Open the Spotify Developer Dashboard.
2. Create an app.
3. Add the exact Redirect URI displayed inside Focus.
4. Enable the Web API and Web Playback SDK.
5. Paste the app's Client ID into Focus and connect your account.

Spotify playback requires Spotify Premium.

Focus uses the authorization-code flow with PKCE; a client secret should not be placed in this front-end repository.

## YouTube

Paste a YouTube video or playlist URL into the YouTube section. Focus uses the YouTube iframe player for playback.

## Apple Music

Apple Music is presented through its embedded web player. Playback and account capabilities are governed by Apple's player and the user's Apple Music access.

## Project structure

```text
focus/
├── index.html
└── README.md
```

At present, the HTML, CSS, and JavaScript are intentionally contained in one file.

## Privacy

Focus is primarily client-side. Browser preferences and supported service configuration may be stored locally in the user's browser.

Third-party music services are subject to their own authentication, privacy, and playback policies.

## Development

The current application is functional, but the interface is still evolving. Planned work includes refining individual tools and giving components such as the Brain Dump Trainer a more distinctive visual identity rather than forcing every part of Focus to share the same design language.

## License

No license has been specified yet.
