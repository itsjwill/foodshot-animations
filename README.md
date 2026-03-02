# FoodShot Animations — 48 Hero Section Concepts

<div align="center">

![Next.js](https://img.shields.io/badge/Next.js-14-black?style=for-the-badge)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-11-purple?style=for-the-badge)
![Components](https://img.shields.io/badge/Concepts-48-orange?style=for-the-badge)

**[Live Demo](https://nextjs-animated-components.vercel.app/demos/foodshot)**

</div>

48 distinct homepage hero section concepts for [FoodShot AI](https://foodshot.ai) — an AI food photography enhancement platform. Every concept sells the same product from a completely different visual angle. Real restaurant photos, no stock imagery.

---

## Preview

Each concept is a full-screen, self-contained hero section showcasing before/after food photography transformations through a unique interaction pattern:

| # | Concept | Interaction |
|---|---------|-------------|
| 1 | **Tasting Menu** | Editorial gallery with scroll-driven reveals |
| 2 | **The Proof** | Side-by-side before/after comparison |
| 3 | **The Slider** | Drag slider to reveal transformation |
| 4 | **The Process** | Scroll-driven assembly line pipeline |
| 5 | **The Pitch** | Homepage hero with revenue stats |
| 6 | **The Wall** | Portal grid with hover expansion |
| 7 | **The Spotlight** | Cinematic carousel with spotlight lighting |
| 8 | **Split Screen** | Full-screen split before vs after |
| 9 | **The Lens** | Magic magnifying glass reveal |
| 10 | **The Menu** | Restaurant menu card layout |
| 11 | **The Stack** | Swipeable card deck |
| 12 | **The Reveal** | Text masking with photo fill |
| 13 | **The Tilt** | 3D perspective card with mouse tracking |
| 14 | **The Filmstrip** | Cinema reel horizontal scroll |
| 15 | **The Counter** | Revenue impact with animated numbers |
| 16 | **The Morph** | Circle reveal transition |
| 17 | **The Orbit** | 3D orbital carousel |
| 18 | **The Curtain** | Theatrical curtain pull reveal |
| 19 | **The Flip** | Playing card flip animation |
| 20 | **The Accordion** | Expandable panel layout |
| 21 | **The Spotlight Beam** | Directional light beam sweep |
| 22 | **The Mosaic** | Tile-by-tile assembly animation |
| 23 | **The Scramble** | Pixel dissolve resolve effect |
| 24 | **The Gravity** | Physics-based falling elements |
| 25 | **The Wipe** | Horizontal scroll wipe transition |
| 26 | **The Mirror** | Reflected typography with photo reveal |
| 27 | **The Pulse** | Heartbeat grid with staggered animation |
| 28 | **The Marquee** | Infinite ticker tape scroll |
| 29 | **The Zoom** | Infinite zoom into nested frames |
| 30 | **The Polaroid** | Scattered instant photos that organize on scroll |
| 31 | **The Glitch** | VHS/digital glitch with RGB channel splits |
| 32 | **The Parallax** | Multi-layer depth parallax scrolling |
| 33 | **The Ripple** | Click-to-reveal expanding circle |
| 34 | **The Typewriter** | Terminal CLI aesthetic with typed stats |
| 35 | **The Cube** | Draggable 3D cube with photos on each face |
| 36 | **The Noir** | Black & white film noir with selective color on hover |
| 37 | **The Neon** | Neon sign glow — click to illuminate |
| 38 | **The Shatter** | Glass shattering into triangular shards |
| 39 | **The Slots** | Slot machine with spinning reels and jackpot |
| 40 | **The Constellation** | Star map with connected photo nodes |
| 41 | **The Split** | Giant words torn in half revealing photos |
| 42 | **The Liquid** | Organic blob morphing between shapes |
| 43 | **The Scratch** | Lottery scratch card — drag to reveal |
| 44 | **The TV** | Retro CRT television with channel switching |
| 45 | **The Vending** | Vending machine — click to dispense items |
| 46 | **The X-Ray** | Draggable scanner beam reveals enhanced photo |
| 47 | **The Roulette** | Game show prize wheel with confetti |
| 48 | **The Vinyl** | Record player turntable with groove animation |

---

## Run Locally

```bash
git clone https://github.com/itsjwill/foodshot-animations.git
cd foodshot-animations
npm install
npm run dev
```

Open [http://localhost:3000/demos/foodshot](http://localhost:3000/demos/foodshot) to see all 48 concepts.

---

## Tech Stack

| Library | Purpose |
|---------|---------|
| **Next.js 14** | App Router with dynamic imports (`ssr: false`) |
| **Framer Motion 11** | Animations, gestures, spring physics, layout |
| **next/image** | Optimized image loading with `fill` + `object-cover` |
| **Tailwind CSS** | Styling |
| **TypeScript** | Full type safety |

---

## Architecture

```
src/
├── app/demos/foodshot/
│   └── page.tsx                    # Main showcase — 48 lazy-loaded sections
├── components/foodshot/
│   ├── photo-data.ts               # Shared data (6 restaurants x before/after)
│   ├── before-after-theater.tsx     # Concept 1: Tasting Menu
│   ├── glow-up-machine.tsx          # Concept 2: The Proof
│   ├── hero-dish.tsx                # Concept 3: The Slider
│   │   ... (45 more component files)
│   ├── roulette-wheel.tsx           # Concept 47: The Roulette
│   └── vinyl-record.tsx             # Concept 48: The Vinyl
└── public/foodshot/
    ├── before-1.jpg ... before-6.jpg
    └── after-1.jpg  ... after-6.jpg
```

**Each component is fully self-contained.** Every `.tsx` file:
- Imports shared photo data from `photo-data.ts`
- Uses `next/image` for optimized loading
- Contains all animation logic inline (no external state)
- Renders a full-screen section with its own unique interaction

**The showcase page** (`page.tsx`) lazy-loads all 48 components with `next/dynamic` and `ssr: false` so the initial bundle stays small. Each section has a loading spinner while it hydrates.

---

## Photo Data

All concepts share the same 6 restaurant before/after photo pairs defined in `photo-data.ts`:

| Restaurant | Before | After |
|------------|--------|-------|
| Culinary Dropout | `before-1.jpg` | `after-1.jpg` |
| Tokyo Hana | `before-2.jpg` | `after-2.jpg` |
| El Jefe Restaurant | `before-3.jpg` | `after-3.jpg` |
| CAPO PIZZA | `before-4.jpg` | `after-4.jpg` |
| Mega Burgers | `before-5.jpg` | `after-5.jpg` |
| Roost | `before-6.jpg` | `after-6.jpg` |

To use your own photos, replace the files in `public/foodshot/` and update the restaurant names in `photo-data.ts`.

---

## Animation Techniques Used

Across the 48 concepts, these techniques appear:

- **Framer Motion** — `motion`, `AnimatePresence`, `useScroll`, `useTransform`, `useSpring`, `useMotionValue`, `animate()`
- **CSS clip-path** — Circle reveals, polygon shards, inset wipes
- **CSS filters** — Grayscale, brightness, saturate, sepia, hue-rotate chains
- **3D transforms** — `perspective`, `rotateX/Y/Z`, `translateZ`, `backfaceVisibility`
- **Spring physics** — Bouncy interactions, slot machine reels, confetti particles
- **SVG filters** — `feColorMatrix` for RGB channel separation (glitch effect)
- **CSS gradients** — `conic-gradient` for vinyl grooves, radial for spotlights
- **Pointer events** — Drag-to-scratch, drag-to-scan, drag-to-rotate
- **Scroll-linked** — `useScroll` + `useTransform` for parallax and scroll-driven animations
- **Procedural generation** — `useMemo` for deterministic star fields, shard patterns, confetti

---

## License

MIT
