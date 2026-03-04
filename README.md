# 💀 Bhootagappa — by JustUtter Horror

> *Solve the dark riddles. Spot the horror creatures. Survive the night. By JustUtter Horror.*

A fully offline-capable horror game built as a single-file PWA (Progressive Web App). No framework, no build step, no dependencies — just open `public/index.html` and play.

---

## 🎮 Gameplay

Each of the **3 horror settings** has two phases:

| Phase | Description |
|-------|-------------|
| 📜 **Riddle Phase** | Answer 5 creepy multiple-choice riddles. Speed = more points. Streak bonuses stack. |
| 👁 **Creature Hunt** | Spot & click hidden horror creatures in the scene before the timer runs out. Miss-clicks cost points. |

### Settings
- **Thornwood Manor** — Haunted mansion with cursed mirrors, sealed rooms, and ancestral portraits
- **Ravenscroft Asylum** — Abandoned asylum with restraint chairs, padded cells, and missing patients
- **The Darkwood** — Cursed forest with a Witch's Yew, shadow stalkers, and an unmarked path

### Creatures
Ghost · Vampire · Skull · Spider · Bat · Shadow Figure · Watching Eye · Doll · Witch · Werewolf

### Scoring
- Base riddle points + time bonus + streak multiplier - hint penalty
- Creature points + time remaining bonus
- Wrong riddle answers: **-50 pts**
- Hunt miss-clicks: **-15 pts**

---

## 🏆 Achievements (13 total)

| Achievement | Condition | Rarity |
|-------------|-----------|--------|
| 🩸 First Blood | Solve your first riddle | Common |
| 👁 First Hunt | Spot your first creature | Common |
| ⚡ Speedrunner | Answer correctly in under 4s | Common |
| 🕯 Unaided | Solve 5 riddles without hints | Common |
| 🔮 Sharp Mind | No wrong answers in a riddle round | Rare |
| 💀 Perfect Hunt | Find all creatures in a hunt | Rare |
| 🗡 On a Roll | 3 correct riddles in a row | Rare |
| 🌑 Survived the Night | Complete all 6 rounds | Rare |
| 🌑 In the Dark | Full game with no hints | Rare |
| 🔪 Top Scorer | Score over 3,000 pts | Rare |
| 🐺 Creature Master | Find all creatures in all hunts | Legendary |
| ⚰ Iron Mind | Perfect riddle accuracy | Legendary |
| 👑 Legend of the Dark | Score over 6,000 pts | Legendary |

---

## 📦 Project Structure

```
bhootagappa/
├── public/                 # Everything served to the browser
│   ├── index.html          # The entire game (single file)
│   ├── manifest.json       # PWA manifest
│   ├── sw.js               # Service worker (offline support)
│   └── icons/
│       ├── icon.svg        # Vector app icon
│       ├── icon-192.png    # PWA icon (192×192) — generate from SVG
│       └── icon-512.png    # PWA icon (512×512) — generate from SVG
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages auto-deploy on push to main
├── netlify.toml            # Netlify deploy config (alternative)
├── .gitignore
└── README.md
```

---

## 🚀 Deploy to GitHub Pages (Recommended)

### Step 1 — Create the repo

```bash
# Create a new repo on GitHub first, then:
git init
git add .
git commit -m "🩸 Initial commit — Bhootagappa by JustUtter Horror"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bhootagappa.git
git push -u origin main
```

### Step 2 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **GitHub Actions**
4. The workflow in `.github/workflows/deploy.yml` runs automatically on every push to `main`

### Step 3 — Done!

Your game will be live at:
```
https://YOUR_USERNAME.github.io/bhootagappa/
```

> **Note:** First deploy takes ~2 minutes. Check the **Actions** tab for progress.

---

## ⚡ Deploy to Netlify (Alternative — even faster)

### Option A — Drag & Drop (instant, no account needed)
1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag the entire **`public/`** folder onto the page
3. Get a live URL instantly (e.g. `https://random-name.netlify.app`)

### Option B — Git-connected (auto-deploys on push)
1. Push your repo to GitHub
2. Log in to [netlify.com](https://netlify.com)
3. Click **Add new site** → **Import an existing project**
4. Connect GitHub → select your repo
5. Build settings are auto-detected from `netlify.toml`:
   - **Publish directory:** `public`
   - No build command needed
6. Click **Deploy site**

### Custom Domain (either platform)
Both GitHub Pages and Netlify support custom domains for free — add your domain in the platform's domain settings, then point your DNS records as instructed.

---

## 📱 Installing as an App (PWA)

The game is a fully installable PWA:

| Platform | How to Install |
|----------|----------------|
| **Android (Chrome)** | Tap ⋮ → *Add to Home Screen* |
| **iOS (Safari)** | Tap Share → *Add to Home Screen* |
| **Desktop (Chrome/Edge)** | Click the install icon (⊕) in the address bar |

An install banner also appears automatically the first time you visit.

---

## 🔧 Generating PNG Icons

The `public/icons/` folder includes `icon.svg`. To generate the required PNG sizes:

**Online (no install):**
- Go to [squoosh.app](https://squoosh.app) or [svgtopng.com](https://svgtopng.com)
- Upload `icon.svg`, resize to 192×192 → save as `icon-192.png`
- Repeat at 512×512 → save as `icon-512.png`

**Command line (if you have `rsvg-convert` or `inkscape`):**
```bash
# Using rsvg-convert
rsvg-convert -w 192 -h 192 public/icons/icon.svg -o public/icons/icon-192.png
rsvg-convert -w 512 -h 512 public/icons/icon.svg -o public/icons/icon-512.png

# Using Inkscape
inkscape public/icons/icon.svg -w 192 -h 192 -o public/icons/icon-192.png
inkscape public/icons/icon.svg -w 512 -h 512 -o public/icons/icon-512.png
```

> The game works perfectly without PNG icons — the SVG icon covers modern browsers. PNGs are only needed for full iOS home screen support.

---

## 🛠 Customising the Game

All game content lives in `public/index.html`. The data is easy to find and edit:

| What | Where in the file |
|------|-------------------|
| Riddles & answers | `const SETTING_DATA` → `riddles` array |
| Creatures & positions | `const SETTING_DATA` → `hunt.creatures` array |
| Points values | `pts` property on each riddle/creature |
| Timer durations | `startTimer(40)` (riddles) / `startTimer(55)` (hunts) |
| Setting names/colours | `const SETTINGS` array |
| Achievements | `const ACHIEVEMENTS` array |

---

## 🌐 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 80+ | ✅ Full (including PWA install) |
| Firefox 75+ | ✅ Full |
| Safari 14+ | ✅ Full (PWA via Add to Home Screen) |
| Edge 80+ | ✅ Full (including PWA install) |
| Samsung Internet | ✅ Full |

---

## 📄 License

MIT — do whatever you want with it. Attribution appreciated but not required.

---

*Built with pure HTML, CSS, and vanilla JavaScript. No frameworks. No build tools. Just horror. — JustUtter Horror*
