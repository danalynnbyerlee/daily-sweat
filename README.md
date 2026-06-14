# Daily Sweat 💪

A simple daily strength checklist that lives on your phone's home screen.

Tap to check off exercises as you do them. See your week at a glance. Edit your own targets inline. That's it — no accounts, no apps to install, no data collection. Just one HTML file.

**[→ See it live](https://danalynnbyerlee.github.io/daily-sweat/)**
<p align="center">
  <img src="screenshot-main.png" width="30%" />
  <img src="screenshot-dropdown.png" width="30%" />
  <img src="screenshot-week.png" width="30%" />
</p>
---

## Why I built this

I wanted a daily workout checklist that:
- Worked on my phone like an app (home screen icon, fullscreen)
- Let me edit reps inline as I got stronger
- Showed me my week so I could see if I was actually being consistent
- Looked nice enough that I'd actually open it

None of the fitness apps I tried did all of these without an account or a subscription. So I built it as one HTML file. You can do the same with your own exercises in about 15 minutes.

---

## Make your own

### 1. Fork this repo

Click **Fork** in the top right of this page. That gives you your own copy.

### 2. Edit the exercises

In your fork, open `index.html` and find the `EXERCISES = [` block (around line 400). Each exercise is one entry that looks like this:

~~~js
{ id:'goblet', group:'quad', name:'Goblet Squat', target:'3 × 12',
  body:'Hold one dumbbell vertically at your chest...',
  tip:'<strong>Start weight:</strong> 15–20 lbs.' },
~~~

The fields:

- **id** — any unique short name (no spaces)
- **group** — one of: `tricep`, `bicep`, `quad`, `glute`, `core`
- **name** — what shows on the card
- **target** — your reps/sets (you can also edit this later from the phone, no code needed)
- **body** — the how-to text
- **tip** — the highlighted tip box (optional — delete the whole `tip:` line if you don't want one)

To **add** an exercise: copy any existing entry and change the fields.
To **remove** one: delete the whole `{ ... },` block.

### 3. Turn on GitHub Pages

- Go to your fork's **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main**, folder: **/ (root)**
- Save

Your live URL appears at the top of the Pages settings about a minute later. It'll look like `https://<yourusername>.github.io/daily-sweat/`.

### 4. Add to your phone

- **Android (Chrome):** Open the URL → ⋮ menu → "Add to Home screen"
- **iPhone (Safari):** Open the URL → Share → "Add to Home Screen"

Open it from the home screen icon (not a fresh browser tab) so your check-offs persist.

---

## Customizing further

- **Reps/sets:** Tap any target pill on your phone to edit inline — no code editing needed.
- **Muscle group colors:** Edit the `--tricep`, `--bicep` etc. CSS variables at the top of `index.html`.
- **Background gradient:** Change `--bg-start`, `--bg-mid`, `--bg-end` (same place).
- **Icons:** Each muscle group uses a Lucide icon (`dumbbell`, `zap`, `footprints`, `activity`, `flame`). Browse all icons at [lucide.dev](https://lucide.dev) and swap the name in the `GROUP_ICON` block.

---

## How this actually works (no engineer required)

Quick demystification, because I had to learn it myself:

- The HTML file lives on GitHub's servers. When you visit the URL, GitHub sends a copy of the file to your phone.
- Your phone's browser runs the JavaScript inside the file. When you tap a checkbox, the JS writes to your browser's **localStorage** — a small private storage area your browser keeps for each website.
- That's why your data persists when you close the page: it's tucked into your browser's locker, not gone.
- It's also why your data is **device-specific**. Your phone's history doesn't show up on your laptop, because they're different browsers with different lockers.
- Nothing about your check-offs is sent anywhere. Not to GitHub, not to me, not to a database. There's no backend.

**The trade-offs:**

- ✅ Free, fast, no accounts, no privacy policy needed
- ✅ Works offline once the page is loaded
- ❌ Doesn't sync across devices
- ❌ Clearing your browser data wipes your history
- ❌ New phone = fresh start (no export feature yet)

For a daily checklist you only use on your phone, the trade-offs are fine. If you ever want true sync, you'd need to add a backend (Firebase, a Google Sheet, etc.) — bigger project.
---

## Built with

- One HTML file (no build step, no framework)
- [Lucide icons](https://lucide.dev) for the muscle group icons
- [Inter](https://rsms.me/inter/) for the font
- Browser localStorage for tracking (your data lives on your device, nowhere else)

Built with Claude as a thinking partner. I'm not an engineer, if I can do this, you can too.
