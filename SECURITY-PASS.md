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

CD Case includes optional Spotify OAuth code. That code can store a user's Spotify Client ID and OAuth tokens in that user's browser storage after they connect Spotify, but the committed HTML file does not contain any actual Spotify credentials.

CD Case backup exports were hardened during this pass. They now include album data and Top 3 pins, but exclude Spotify auth data and Client IDs.

Do not upload browser-exported backup JSON files unless the saved album list is intentionally public.

Knoll does not upload images. It processes images locally in the browser and generates local exports from the currently loaded image.
