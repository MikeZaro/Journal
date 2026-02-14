# AI Memory Journal

Production-ready MVP built with:
- Next.js 15 App Router + TypeScript
- Tailwind + shadcn-style UI
- Supabase Auth + Postgres + pgvector
- OpenAI API (`text-embedding-3-small`, `gpt-4o-mini` by default)
- Vercel-ready deployment

## Local setup

1. Install dependencies:
```bash
npm install
```

2. Create `.env.local` from `.env.example` and fill values.

3. In Supabase SQL Editor, run `supabase/schema.sql`.

4. Start dev server:
```bash
npm run dev
```

5. Open `http://localhost:3000`.

## Environment variables

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`
- `OPENAI_API_KEY`
- `OPENAI_CHAT_MODEL` (optional, default `gpt-4o-mini`)
- `OPENAI_EMBEDDING_MODEL` (optional, default `text-embedding-3-small`)

## Feature summary

- Email/password + magic-link auth (Supabase Auth)
- Journal dashboard with month view + full entry list
- New entry modal with date + text content
- Full-screen chat against lifetime memory
- Retrieval on each message:
  - Top 8 vector-similar entries
  - 5 most recent entries
- Auto-embedding on each saved entry
- RLS for user-owned data isolation
- Mobile-first responsive UI (desktop sidebar + mobile bottom nav)
