# 🥛 DairyTrack

Apni bhains ke doodh ki bikri ka hisab-kitab rakhne ke liye ek chhota sa **PWA (Progressive Web App)** — koi server nahi, koi login nahi, koi kharcha nahi. Saara data phone ke browser me hi rehta hai.

## Kya-kya hota hai isme

- **Roz ki entry — Subah / Shaam alag-alag.** Har grahak sirf usi time ki list me dikhta hai jis time wo doodh leta hai (Sirf Subah / Sirf Shaam / Dono).
- **Har grahak ka apna rate.** Aam rate ₹80/L hai, lekin jisne bargain kiya uska ₹79 ya ₹78 — rate har grahak ke saath uski date ke hisaab se save hota hai, taaki rate badalne par purane mahine ka hisab na bigde.
- **Mahine ka hisab ek tap me** — kul litre × usi grahak ka rate + pichla baaki − jama = kul dena hai.
- **WhatsApp parchi** — date-wise poori parchi (subah/shaam alag) seedha grahak ke WhatsApp par.
- **Grahak chhod jaye to "Band"** — delete nahi hota; purana hisab aur baaki hamesha safe, kabhi bhi phir chalu kar sakte ho.
- **Backup / Restore** — poora hisab ek JSON file ya text ke roop me; phone badlo to wapas la sakte ho.
- **Offline chalta hai** — ek baar install ho jaye to internet ki zaroorat nahi.

## Chalana kaise hai

Ye ek static site hai. Kisi bhi free HTTPS hosting par folder daal do:

- **GitHub Pages:** repo ke `Settings → Pages → Branch: main / root` — live URL mil jayega.
- Ya Netlify / Cloudflare Pages par folder drag-and-drop.

Phone ke Chrome me link kholo → **📲 Install Karo** button (ya Chrome menu → "App install karo") → home screen par icon aa jayega.

> ⚠ Note: sirf file kholne (file://) par install aur offline kaam nahi karega — HTTPS wala link chahiye. Service worker `http://localhost` par bhi chalta hai, to laptop par test karna ho to: `python -m http.server 8000` aur browser me `localhost:8000` kholo.

## Tech

- Ek hi `index.html` me poora app (HTML + CSS + vanilla JS) — koi framework nahi, koi build step nahi.
- Data: browser `localStorage` (key `doodhHisabV3`). Koi data kahi upload nahi hota.
- `manifest.json` + `service-worker.js` = installable PWA, offline-first.

## Aage ka plan (roadmap)

- [ ] Bakri (goat) ke doodh ka alag module — paas wali dairy se aata hai
- [ ] Play Store par TWA (PWABuilder) se — bina code dobara likhe
- [ ] Mahine ki PDF report

## License

Personal use ke liye banaya gaya hai.
