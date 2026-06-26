# Security Pass

Checked files:

- `cd-case.html`
- `knoll-color-analyzer.html`
- `cd-case-writeup.md`
- `knoll-writeup.md`

## Result

No embedded personal information was found in the GitHub-ready files.

Specifically, the scan did not find:

- Personal email addresses.
- Phone numbers.
- Usernames intended for publishing.
- Local Windows paths from the working machine.
- API keys.
- Hard-coded OAuth Client IDs or client secrets.
- Access tokens or refresh tokens.
- GitHub, OpenAI, AWS, Google, Slack, or GitLab token patterns.
- Private keys.

## Notes

CD Case no longer includes Spotify OAuth, Spotify account import, Client ID input, or token exchange code. Visitors do not need Spotify Developer access.

CD Case backup exports include album data and Top 3 pins only.

Do not upload browser-exported backup JSON files unless the saved album list is intentionally public.

Story share links encode the selected story data in the URL hash. They can include album titles, artists, cover image URLs, and listen links, but not account tokens or browser storage.

The social story feature does not connect to Instagram, Facebook, TikTok, or Spotify APIs and does not require developer keys.

Knoll does not upload images. It processes images locally in the browser and generates local exports from the currently loaded image.
