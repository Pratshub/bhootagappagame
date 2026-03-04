# 💀 Bhootagappa — by JustUtter Horror

> *Solve the dark riddles. Spot the horror creatures. Survive the night.*

A horror game built as a single-file PWA. Open `public/index.html` in any browser and play — no internet required after first load.

---

## 🎮 Gameplay

Each of the **3 horror settings** has two phases back to back:

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
- Base riddle points + time bonus + streak multiplier − hint penalty
- Creature points + time remaining bonus
- Wrong riddle answers: **−50 pts**
- Hunt miss-clicks: **−15 pts**

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
bhootagappagame/
├── public/
│   ├── index.html       ← The entire game (open this to play)
│   ├── manifest.json    ← PWA install config
│   ├── sw.js            ← Offline service worker
│   └── icons/
│       ├── icon.svg
│       ├── icon-192.png
│       └── icon-512.png
├── ARCHITECTURE.md      ← Code explanation & diagrams
├── ARCHITECTURE.svg     ← Visual architecture diagram
└── README.md
```

---

## 🏗 Architecture

See [ARCHITECTURE.md](ARCHITECTURE.md) for a full explanation of the code structure, game loop, scoring system, and data layer.

![Architecture Diagram](ARCHITECTURE.svg)

---

## 🌐 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 80+ | ✅ Full |
| Firefox 75+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 80+ | ✅ Full |
| Samsung Internet | ✅ Full |

---

## 📱 Installing as an App

The game installs as a PWA on any device:

| Platform | How |
|----------|-----|
| Android (Chrome) | Tap ⋮ → *Add to Home Screen* |
| iOS (Safari) | Tap Share → *Add to Home Screen* |
| Desktop (Chrome/Edge) | Click ⊕ in the address bar |

---

*JustUtter Horror · Built with pure HTML, CSS, and vanilla JavaScript. No frameworks. No build tools. Just horror.*
