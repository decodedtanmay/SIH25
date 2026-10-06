# FRA-Mitra — AI decision support for Forest Rights Act claims

Team XCalibre's web app for **Smart India Hackathon 2025, problem statement PS25108**. It digitizes Forest Rights Act (FRA) claim documents with AI and helps officials review claims and match claimants to government schemes. The team cleared Pillai College of Engineering's internal SIH round with it.

> Hackathon prototype, built in September 2025. Not production software.

## What it does

- **AI document extraction.** Upload a scanned FRA claim (PDF, JPEG, PNG). Gemini (`gemini-2.0-flash-lite`) reads it and returns structured fields: claimant, spouse, parent, village, gram panchayat, tehsil, district, state, ST / other-forest-dweller status, family members, land area, tribal group, and claim type (IFR, CFR, habitat rights). Single and bulk upload are supported.
- **Claims workflow.** Claims move through `DRAFT → PENDING → UNDER_REVIEW → APPROVED / REJECTED / PROCESSED`, with priority levels and duplicate-claim detection.
- **Scheme recommendations.** For a given claim, Gemini suggests relevant Centrally Sponsored Schemes across livelihood, education, health, housing, agriculture/forest livelihood and social security, with eligibility notes.
- **Map and dashboard.** A Leaflet map of claim locations, plus dashboard stats and charts (Recharts, D3).
- **Accounts.** Email/password sign-up and sign-in (bcrypt) with roles: admin, reviewer, user.
- **Bilingual landing page** (English and Hindi).

## Stack

| Layer | Tech |
|---|---|
| App | Next.js 15 (App Router, Turbopack), React 19, TypeScript, Tailwind CSS 4 |
| Data | PostgreSQL + Prisma ORM |
| AI | Google Gemini via `@google/generative-ai` |
| Maps & charts | Leaflet / React-Leaflet, D3, Recharts, react-countup |

## API routes

`/api/auth/signup`, `/api/auth/signin`, `/api/claims`, `/api/claims/[id]`, `/api/documents`, `/api/documents/upload`, `/api/process-document`, `/api/process-documents-bulk`, `/api/scheme-recommendations`, `/api/dashboard/stats`

## Run locally

```bash
npm install
# .env: DATABASE_URL=postgresql://... and GOOGLE_API_KEY=...
npm run db:generate && npm run db:migrate && npm run db:seed
npm run dev          # http://localhost:3001
```

See `DATABASE_SETUP.md` for database details.

## Team

Team XCalibre, Pillai College of Engineering. Most of the app was committed by **Arnav Deka** (upstream: [Arnavcloud0412/SIH25](https://github.com/Arnavcloud0412/SIH25)). **Tanmay Gawade** built landing-page layout and the animated stats counters. Gayatri Vinod and Sanyam Maharana also contributed.

A companion repo with the Flask / OCR / PostGIS architecture plan is [fra-webgis-dss](https://github.com/decodedtanmay/fra-webgis-dss).
