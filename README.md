# ورد القرآن — Reading Quraan

A minimal, mobile-friendly webapp for reading the Quran one session at a time.

- Sign up with a username and password (no email needed).
- On opening the app, choose how many pages to read this session (default 1).
- Pages follow the Madinah mushaf (604 pages), starting from page 1.
- Progress is saved after every page, so you resume where you stopped.
- A session ends when its pages are done; start a new one from the main page.

**Status:** pages 1–20 are included while the app is being fine-tuned.
To add more, generate `pages/<n>.json` files and raise `AVAILABLE_PAGES` in `index.html`.

## Files
- `index.html` — the whole app (Supabase login + reader)
- `pages/<n>.json` — text of each mushaf page
- `fonts/hafs.18.woff2` — KFGQPC Uthmanic Hafs font

## Backend
Supabase (shared project, separate objects): table `quran_readers`,
function `quran_complete_page(p_page)`, edge function `quran-signup`.

## Sources
Quran text, page layout and font: King Fahd Glorious Quran Printing Complex
(KFGQPC), Uthmanic Hafs v18 — https://qurancomplex.gov.sa/ — used unmodified.
