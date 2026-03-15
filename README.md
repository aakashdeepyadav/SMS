# SMS

Student Management System static website.

## Overview

This project is a static multi-page website built with HTML and CSS.

Main entry page:

- `index.html`

Includes:

- Course pages
- Attendance and timetable pages
- Assignment and inquiry forms (front-end only)
- Image assets
- Syllabus PDFs in the `Syllabus` folder

## Project Structure

Key files and folders:

- `index.html` - main homepage
- `sms.css` - shared homepage/navigation styles
- `assignment.css`, `asgn.css`, `inquiry.css`, `login.css` - page-specific styles
- `Syllabus/` - PDF files linked from the syllabus page
- `wrangler.toml` - Cloudflare deployment configuration

## Run Locally

Because this is a static site, you can open `index.html` directly in a browser.

For better local testing, use a simple static server (optional).

## Deploy to Cloudflare Pages (Recommended)

Use Cloudflare Pages static deployment.

Cloudflare Pages build settings:

- Build command: leave empty
- Build output directory: `.`
- Deploy command: `npx wrangler pages deploy .`
- Version command: leave empty
- Root directory: `/`
- Production branch: `main`
- Build watch paths include: `*`

Manual deploy command:

```bash
npx wrangler pages deploy .
```

Important:

- `npx wrangler deploy` is Worker deploy mode and can fail for static sites if Pages is intended.
- For this project, prefer `npx wrangler pages deploy .`.

## CI/CD Note

Use Pages deploy mode in CI/CD:

- `npx wrangler pages deploy .`

Do not use `npx wrangler deploy` for this project.

## Post-Deploy Verification

After deployment, verify these URLs on your live domain:

1. `/`
2. `/slide1.jpg`
3. `/Syllabus/CSE111slbs.pdf`

If all three open correctly, pages, photos, and PDFs are published properly.
