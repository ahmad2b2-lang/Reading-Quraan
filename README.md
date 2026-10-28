# ورد القرآن — Reading Quraan

A minimal, mobile-friendly webapp for reading the Quran one session at a time.

- Sign up with any username (Arabic or English) and a PIN of 4+ digits, entered on an on-screen keypad (no email needed).
- On opening the app, choose how many pages to read this session (default 1).
- Pages follow the Madinah mushaf (604 pages), starting from page 1.
- Progress is saved after every page, so you resume where you stopped.
- A session ends when its pages are done; start a new one from the main page.
- Installable to the phone home screen (button at the top of the main page).

**Status:** the complete mushaf (all 604 pages, 6236 ayat) is included. After page 604 the reader
finishes a khatma, the session ends with a short congratulation, and reading restarts at Al-Fatihah.

## Files
- `index.html` — the whole app (Supabase login + reader)
- `pages/<n>.json` — text of each mushaf page
- `fonts/hafs.18.woff2` — KFGQPC Uthmanic Hafs font
- `manifest.webmanifest`, `sw.js`, `icons/` — installable home-screen app, works offline once opened

## Backend
Supabase (shared project, separate objects): table `quran_readers`,
function `quran_complete_page(p_page)`, edge function `quran-signup`.

## Sources
Quran text, page layout and font: King Fahd Glorious Quran Printing Complex
(KFGQPC), Uthmanic Hafs v18 — https://qurancomplex.gov.sa/ — used unmodified.
