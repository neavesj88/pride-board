# Pride Board

A simple **lacrosse coaching whiteboard** that runs in any web browser — on a phone, tablet, or
computer. Drag players around a to‑scale field, draw run/pass arrows, set up plays, and save or
share them as a picture or PDF. It works **offline**, needs **no account**, and is just a single
file.

It's built around the **Lacrosse Australia Unified Field Markings** (full‑field, 100 m × 60 m).

---

## 📱 Put it on your phone (the easy way)

The board works best when you open it from a **web link** (a web address). When it's opened from a
link, your phone can add it to your home screen as a proper app, with the club crest as the icon.

> Ask whoever set it up for the link (it will look something like
> `https://neavesj88.github.io/pride-board`). If no one has hosted it yet, see
> **"Putting it online"** at the bottom — it's a one‑time, 2‑minute job.

### On an Android phone (Chrome)
1. Open the link in **Chrome**.
2. Tap the **⋮** menu (three dots, top‑right).
3. Tap **Add to Home screen** (it may say **Install app**).
4. Tap **Add / Install**.
5. The maroon crest icon appears on your home screen — tap it to open the board full‑screen.

### On an iPhone or iPad (Safari)
1. Open the link in **Safari** (this part only works in Safari, not Chrome, on iPhone).
2. Tap the **Share** button (the square with an arrow pointing up).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add** (top‑right).
5. The crest icon appears on your home screen — tap it to open the board full‑screen.

Once it's on your home screen it runs like a normal app and **works without internet**.

---

## 💾 "I just have the file" (no link yet)

You can also use the single file directly, though you won't get the nice app icon this way:

- **Android:** Download `index.html` from this page (tap the file, then the **download** icon).
  Open your **Files**/**Downloads** app, tap `index.html`, and choose **Chrome** to open it.
- **iPhone/iPad:** Downloading and opening a web file locally is fiddly on iOS and won't install as
  an app. Using a **link** (above) is strongly recommended on iPhone.

For the real app experience on both phones, use a link — see **"Putting it online"** below.

---

## 🥍 What you can do

- **Move players** — drag any disc. Long‑press a player to remove it.
- **Add players** — tap **Add**, pick a role, then tap the field to drop it. Roles are shown by
  shape: plain disc = attack, disc with an inner ring = midfield, **gold pole** = long‑pole
  (defence / long‑stick midfield), rounded square with a dashed ring = goalie. Plus ball and cone.
- **Set starting line‑up** — drops a full face‑off formation for both teams in one tap.
- **Draw** — solid **Run** arrows, dashed **Pass** arrows, free‑hand **pen**, and a **flag** to
  highlight a player.
- **Two teams by colour** — defaults to maroon and blue; change either from **Teams**.
- **Save & share** — **Screenshot (PNG)** with the camera button, or **Save as PDF** with a play
  name. Save one play to come back to later.
- **Make it yours** — portrait or landscape, light or dark mode, a background colour, and a
  player‑size slider (discs start small; drag to enlarge).
- **Gentle rule reminders** — a soft warning if a team has too many long poles, or too many
  players over the halfway line (offside).

Everything stays **on your device**. Nothing is uploaded.

---

## 🌐 Putting it online (one‑time setup, for the organiser)

To get a shareable link, host the single `index.html` anywhere that serves web pages. The simplest
free option is **GitHub Pages**:

1. In this GitHub repository, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set the branch to **`main`** and the folder to **`/ (root)`**, then **Save**.
4. Wait ~1 minute, refresh, and GitHub shows your link
   (e.g. `https://neavesj88.github.io/pride-board`). Share that with your coaches.

Any other static host works too (Netlify, Cloudflare Pages, etc.) — just upload `index.html`.

---

## 🛠️ For the curious (how it's built)

It's one self‑contained `index.html` (~250 KB): the logo, app icons, and settings are all built
into the file as text, so there's nothing to install and no server to run. The field is drawn on a
`<canvas>`; players are little on‑screen elements you can drag; arrows are vector graphics. The
code inside `index.html` is commented in plain English if you'd like to look.

Default team colours: maroon `#4E121A` and blue `#2E5FA8`, with a gold `#E2B33C` accent.
