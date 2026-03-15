# SMS

Student Management System static website.

## Deployment Status

This project is deployed as a static site on Cloudflare Pages.

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

## Run Locally

Because this is a static site, you can open `index.html` directly in a browser.

For better local testing, use a simple static server (optional).

## Cloudflare Pages Configuration

This project uses Cloudflare Pages Git-based static deployment.

Use these settings in Cloudflare Pages:

- Build command: empty
- Build output directory: `.`
- Root directory: `/`
- Production branch: `main`

For this static setup:

- Do not use `wrangler deploy`
- Do not require `CLOUDFLARE_API_TOKEN` in build variables

## Post-Deploy Verification

After deployment, verify these URLs on your live domain:

1. `/`
2. `/slide1.jpg`
3. `/Syllabus/CSE111slbs.pdf`

If all three open correctly, pages, photos, and PDFs are published properly.
