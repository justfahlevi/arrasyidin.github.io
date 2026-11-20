# Ar Rasyidin Academy — website

Live build of the Figma file "Ar Rasyidin - Web Design" (Design Revision page), with the approved motion spec.

## Run it on localhost

You need Node.js 18 or newer (check with `node -v`; install from https://nodejs.org if missing).

```bash
cd ar-rasyidin-site
npm install
npm run dev
```

Your browser opens at http://localhost:5173. Stop it with Ctrl + C.

## Pages

| Route | Page |
| --- | --- |
| `/` | Home |
| `/about` | About |
| `/episodes` | Episodes (filters, sort, See More) |
| `/quick-answers` | Open video / Quick answers (player, answer list) |
| `/guests` | Guests (Load More) |
| `/collaboration` | Collaboration (form with Sending → Sent) |
| `/contact` | Contact (form with Sending → Sent) |

## Things to fill in

- **External links:** `src/links.js` — every `#TODO-…` (Instagram, Facebook, X, TikTok, LinkedIn, WhatsApp channel, Orius Digital, legal pages, per-guest YouTube episodes).
- **Hero video:** the Home hero is a video in Figma. Save it as `public/video/hero.mp4` and it plays automatically; until then the poster image shows.
- **Co-host roles:** still "[role]" in `src/pages/Home.jsx` and `src/pages/About.jsx`.
- **Forms:** they show the Sending/Sent states but don't send email yet — connect them to a form service (Formspree, Resend, etc.) in `src/components/Form.jsx`.

## Motion

Tokens live in `src/motion.js` (same values as the Figma spec): quick 160 ms, medium 320 ms, slow 560 ms, press spring 400/30/1, 60 ms stagger, 24 px rise (16 px on mobile).

## Deploy

`npm run build` creates `dist/`. Push the folder to GitHub and import it on Vercel or Netlify (framework: Vite).
