# YC Directory

Browse Y Combinator startups with fast search and filters. Built with **Next.js (App Router)**, **TypeScript**, **Tailwind CSS**, and **Sanity** CMS.

- Instant search across name, tags, batch, and description
- Filter by categories / batches
- SEO-friendly pages with ISR/SSG
- Content managed in Sanity (easy to add/edit startups)


---

## Tech Stack

- **Next.js 14** (App Router, Server Components)
- **TypeScript**
- **Tailwind CSS**
- **Sanity CMS** (GROQ queries)
- **ESLint / Prettier**

---

## Quickstart

### 1) Clone & install

```bash
git clone https://github.com/jeena-krishna/YC-Directory.git
cd YC-Directory
npm install
# or: pnpm install / yarn install

2) Environment variables

Create a .env.local in the project root:

# Public values used by the frontend
NEXT_PUBLIC_SANITY_PROJECT_ID=your_project_id
NEXT_PUBLIC_SANITY_DATASET=production
NEXT_PUBLIC_SANITY_API_VERSION=2023-10-01

# Optional (only if you run server actions that need a token)
SANITY_API_READ_TOKEN=your_sanity_token


You can find the Sanity project ID and dataset in your Sanity project settings.

3) Run the dev server
npm run dev
# open http://localhost:3000

4) Build & start (production)
npm run build
npm start


Scripts
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start",
    "lint": "next lint",
    "sanity": "sanity start"
  }
}

npm run dev — local development
npm run build — production build
npm start — run production server
npm run sanity — run Sanity Studio (if Studio is inside this repo)


Sanity Content Model (example)

Startup document typically includes:
name (string)
slug (slug generated from name)
batch (string, e.g., S22, W23)
tags (array of strings)
website (url)
logo (image)
description (text)
Create/edit content in Sanity Studio and query via GROQ in your Next.js app


Notes for Deployment

Add the same environment variables on your hosting platform (Vercel/Netlify).
If Sanity Studio is in this repo, you can deploy it separately (Sanity Managed / Vercel) or keep it local.


