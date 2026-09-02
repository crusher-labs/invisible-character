# Invisible Character

One-click copy of invisible Unicode characters (Hangul filler, zero-width space, braille blank and more) for blank usernames, empty messages and invisible text, with a generator and a paste-to-test checker.

Live: <https://crusher-labs.github.io/invisible-character/>

## Privacy

This tool runs entirely in your browser. There is no server. No data is uploaded, no telemetry, no analytics.

## Framework / hosting

- Static HTML / CSS / JS deployed via GitHub Pages from this repo's `main` branch.
- UI chrome is the published `crusher-ui-kit` static contract; the pinned version and its SRI hashes are managed fleet-wide by `tools-hub/scripts/bump-kit.mjs`.

## Development

- Open `index.html` directly in a browser. No build, no dependencies.
- Or serve the parent workspace via the hub's preview server: `cd ../../tools-hub && npm run preview` then visit `http://127.0.0.1:8723/utility-tools/invisible-character/`.

## License

MIT.
