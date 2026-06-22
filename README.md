# CD Case

CD Case is a standalone browser app for building a personal album crate out of share links. Paste an album link, generate a visual CD-style case, flip it open for playback links and QR codes, pin favorites into a Top 3 shelf, and print clean QR pucks for real-world sharing.

## What it does

- Adds albums from Spotify and other music-service links.
- Resolves cross-platform listening links through song.link when available.
- Falls back to Spotify oEmbed for Spotify links if the broader resolver is unavailable.
- Generates scannable QR codes for Spotify or universal song.link pages.
- Saves the collection locally in the browser.
- Lets users edit titles and artists directly on each case.
- Supports Top 3 pinning, case flipping, print sheets, import, and export.
- Optionally connects to Spotify with PKCE OAuth to import saved albums.

## Why it is useful

CD Case turns a music library into something tactile and browsable. It is part mixtape wall, part record shelf, part tiny print shop: good for sharing favorite albums, making visual collections, or turning listening links into physical cards and stickers.

## Privacy and security

The app is client-side HTML/CSS/JavaScript. It does not include a server component.

- Album data is stored in the user's own browser storage.
- Spotify login is optional.
- No Spotify Client ID, access token, refresh token, account data, email, or personal file path is embedded in this file.
- If a user connects Spotify, their OAuth data is created at runtime in their own browser.
- Backup exports include album data and Top 3 pins, but exclude Spotify auth data and Client IDs.
- QR generation happens locally using the bundled page script and the QRCode library loaded from CDN.

## External services

CD Case uses these external resources at runtime:

- Google Fonts for typography.
- cdnjs for the QRCode library.
- song.link API to resolve cross-service music links.
- Spotify oEmbed for fallback Spotify metadata.
- Spotify Accounts and Web API only when the user chooses to connect Spotify.

## Deployment

This is a single-file static app. It can be hosted on GitHub Pages as `cd-case.html`.

For Spotify import, the page must be served from a redirect URI registered in the user's Spotify Developer Dashboard. The app explains this setup in its Spotify section.
