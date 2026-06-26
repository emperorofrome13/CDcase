# CD Case

CD Case is a standalone browser app for building a personal collection of CD-style album cases out of share links. Paste an album link, generate a visual CD-style case, flip it open for playback links and QR codes, pin favorites into a Top 3 shelf, and print clean QR pucks for real-world sharing.

## What it does

- Adds albums from Spotify and other music-service links.
- Resolves cross-platform listening links through song.link when available.
- Falls back to Spotify oEmbed for Spotify links if the broader resolver is unavailable.
- Generates scannable QR codes for Spotify or universal song.link pages.
- Saves the collection locally in the browser.
- Lets users edit titles and artists directly on each case.
- Supports Top 3 pinning, case flipping, print sheets, import, and export.
- Creates 9:16 social story/share cards for Instagram, Facebook, TikTok, Snapchat, Bluesky, Reddit, Discord, and Pinterest.
- Exports exact 1080x1920 story PNGs and short animated WebM stories.
- Copies share links that reconstruct the story from URL hash data.
- Requires no Spotify Developer app, Client ID, login, or account access.

## Why it is useful

CD Case turns a music library into something tactile and browsable. It is part mixtape wall, part record shelf, part tiny print shop: good for sharing favorite albums, making visual collections, or turning listening links into physical cards and stickers.

The story maker turns saved CD cases into postable social assets. It does not auto-post to social platforms; it generates a downloadable/shareable story image or animation that users can post manually.

## Privacy and security

The app is client-side HTML/CSS/JavaScript. It does not include a server component.

- Album data is stored in the user's own browser storage.
- No Spotify Client ID, access token, refresh token, account data, email, or personal file path is embedded in this file.
- Backup exports include album data and Top 3 pins only.
- Story share links encode selected album titles, artists, cover URLs, and listen links in the URL hash.
- Social story creation uses browser APIs only; it does not use social-platform or Spotify login APIs.
- QR generation happens locally using the bundled page script and the QRCode library loaded from CDN.

## External services

CD Case uses these external resources at runtime:

- Google Fonts for typography.
- cdnjs for the QRCode library.
- song.link API to resolve cross-service music links.
- Spotify oEmbed for fallback Spotify metadata.
- Browser Web Share API when available.

## Deployment

This is a single-file static app. It can be hosted on GitHub Pages as `index.html`.

No developer account setup is required. Visitors paste album links directly into the app.
