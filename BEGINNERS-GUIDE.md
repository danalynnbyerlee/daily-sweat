# Daily Sweat — Your Own Version

A cheat sheet

## What is GitHub and why do you need it?

GitHub is basically Google Drive for code. You put your HTML file there, and GitHub gives you a free public URL where the app actually runs in a browser. That URL is what lets you save a shortcut to your phone home screen like a real app.

You need it because: **a file on your computer can't be a shortcut on your phone. A file on GitHub can.**

---

## You can't permanently break anything

Read this first — it's the reason you can relax and experiment.

Every time you save a change, GitHub keeps the old version forever. If an edit wrecks your app, you can roll back: in your repo, click **"Commits"** (the little clock/history icon near the top of the file list), find the last version that worked, and restore it.

So experiment freely. There's always an undo.

---

## Part 1: Get your own copy (15 min, one time)

**1. Make a GitHub account**
Go to github.com → Sign up. Use any email. Pick a username you don't hate seeing in a URL (it'll show up like `yourusername.github.io`).

**2. Copy my project to your account**
Go to: https://github.com/danalynnbyerlee/daily-sweat
Click the **"Fork"** button (top right). This makes your own independent copy — your changes won't touch mine, and mine won't touch yours. Name it whatever; `daily-sweat` is fine.

**3. Turn on the website (GitHub Pages)**
In your new forked repo:
- Click **Settings** (top menu)
- Click **Pages** (left sidebar)
- Under "Source," pick **main** branch, **/ (root)** folder
- Click Save
- Wait 1–2 min

Your URL will be: `https://yourusername.github.io/daily-sweat/`

**4. Add to phone home screen**
- Open that URL in Chrome on your Android
- Tap the three-dot menu → **Add to Home screen**
- Done. You have an "app" now.

---

## Part 2: Customize your exercises with AI

**1. Open the file you'll edit**
- In your repo, click `index.html`
- Click the **pencil icon** (top right of the file view) to edit
- Select all the code, copy it

**2. Open Gemini, ChatGPT, or Claude.ai**
Paste the code in. Then prompt like this:

> *"This is an HTML fitness tracker. I want to swap out the current exercises and put in my own. Here's what I want: [list your exercises with sets x reps and muscle group, e.g. Pull-Ups, 3x8, Back]. Give me back the complete updated HTML file with my exercises in place of the originals. Keep the same structure and format for each exercise (the id, group, name, target, body, and tip fields). Don't change anything else."*

**3. Replace the code**
- Copy the new code the AI gives you
- **Check it's complete first** — it should start with `<!DOCTYPE html>` and end with `</html>`. If it cuts off partway, the AI ran out of room. Just say *"the file got cut off, give me the full thing again"* or *"continue from where you stopped."*
- Go back to GitHub, paste it in (replacing everything)
- Scroll down. When GitHub asks where to save, pick **"Commit directly to main"** (more on that below)
- Click **Commit changes**
- Wait 1–2 min, refresh your phone shortcut

---

## A few things that'll confuse you (they confused me)

**"Commit to main" vs. "Create a new branch"**
Always pick **"Commit directly to main."** Branches are a tool for teams working on the same code at once — you're one person on one file, so you'll never need them.

**You don't need code to change reps**
Tap any target pill (like "3 × 12") right on your phone and edit it. Code editing is only for *adding/removing* exercises or changing the look.

**If you don't see your change after editing**
Give it a full 1–2 minutes, then refresh. If it's still showing the old version, close the app fully and reopen it — your phone sometimes holds onto a cached copy for a bit.

---

## Where does your check-off data go?

When you tap a box, it saves to *your phone's browser storage* — not to GitHub, not anywhere online. Nobody but you can see it. That's why:

- Your history sticks around when you close the app ✅
- It does **not** sync to your laptop (a different device = different storage)
- **Always open it from the home screen icon.** If you open the link inside another app (tapping it in a text or Instagram), it can use separate storage and look empty. Your data isn't gone — you're just looking through the wrong window.

**If your weekly history suddenly resets after an edit:** the AI probably renamed the hidden `id` labels on each exercise. Tell it: *"keep the existing id for each exercise the same so my history doesn't reset,"* and re-do the edit.

---

## Want to redesign the look?

Don't just tell the AI "make it prettier" — you'll get generic, samey defaults. Instead:

1. Screenshot 3–4 apps whose style you love
2. Paste them to the AI and say: *"Build me a design system first — name the colors, fonts, spacing, and corner styles — then restyle my app to match. Don't generate anything until the system is defined."*
3. Lock the style you want, **then** let it touch the code

Giving it real references and making it define the system *before* writing code is the difference between "looks like every AI app" and "looks like the thing in your head."

---

## Tips for working with the AI

- **Always say "give me the complete file back"** — otherwise it gives you snippets you won't know where to put.
- **Change one thing at a time.** Easier to spot what broke.
- **If something breaks:** paste the broken code back in and say *"this isn't working, here's what I see [describe], fix it and give me the complete file."*
- **Brainstorm exercises first:** before coding, just ask *"I want to build a strength plan focused on [your goals]. Suggest exercises grouped by muscle, with sets x reps."* Get the list you want, then plug it in.
