# SMS

Static Student Management System website.

## Deploy to Cloudflare Pages

Use Cloudflare Pages static deployment (not Workers deploy).

Build settings:
- Build command: (leave empty)
- Build output directory: `.`

Wrangler CLI command (manual deploy):
- `npx wrangler pages deploy .`

This project includes `wrangler.toml` with:
- `pages_build_output_dir = "."`

Notes:
- `index.html` is the main homepage file.

