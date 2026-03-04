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


---

*Built with pure HTML, CSS, and vanilla JavaScript. No frameworks. No build tools. Just horror. — JustUtter Horror*
