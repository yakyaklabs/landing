# YakYak Design System

> Warm parchment canvas, terracotta accent, Noto typography, approachable human tone.

---

## 1. Visual Identity

YakYak's visual identity is warm, editorial, and approachable — a literary salon reimagined for language learning. The parchment-toned canvas (`#f5f4ed`) evokes paper rather than a digital surface. The terracotta accent anchors the brand with earthy warmth. The three monkeys (see/hear/speak) serve as the core visual motif. Chunky Duolingo-style shadows keep the tone playful rather than serious.

**Key characteristics:**
- Warm parchment canvas (`#f5f4ed`) — never pure white
- Terracotta brand accent (`#c96442`) — earthy, un-tech
- Noto Serif for headings, Noto Sans for body and UI
- Three monkeys motif (see, hear, speak)
- Chunky bottom shadows on interactive elements (Duolingo-inspired)
- Sticky nav, blur backdrop

---

## 2. Colour Palette

All values are hex. Every neutral carries a warm yellow-brown undertone — no cool blue-grays.

### Surface and background

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#f5f4ed` | Page canvas (warm parchment) |
| `--surface` | `#faf9f5` | Cards, elevated containers |
| `--surface-warm` | `#e8e6dc` | Button backgrounds, interactive surfaces |

### Foreground and text

| Token | Value | Usage |
|---|---|---|
| `--fg` | `#141413` | Primary text (warm near-black) |
| `--fg-2` | `#3d3d3a` | Dark links, emphasised secondary text |
| `--muted` | `#5e5d59` | Secondary body text (olive-gray) |
| `--meta` | `#87867f` | Tertiary text, footnotes, metadata |

### Accent and semantic

| Token | Value | Usage |
|---|---|---|
| `--accent` | `#c96442` | Primary CTA, key brand moments |
| `--accent-on` | `#faf9f5` | Text on terracotta backgrounds |
| `--accent-hover` | `#a34e32` | Hover state for accent |
| `--accent-active` | `#8a3f28` | Active/pressed state |
| `--danger` | `#b53333` | Error states (warm red) |

### Borders

| Token | Value | Usage |
|---|---|---|
| `--border` | `#f0eee6` | Standard light-theme border |
| `--border-soft` | `#e8e6dc` | Section dividers, emphasised borders |

---

## 3. Typography

### Font families

| Token | Font | Weight loaded | Usage |
|---|---|---|---|
| `--font-display` | Noto Serif | 400, 500, 600, 700 | All headings |
| `--font-body` | Noto Sans | 400, 700 | Body text, UI, buttons, forms |
| `--font-mono` | Noto Sans Mono | 400 | Code |
| Chinese TC | Noto Sans TC | 400 | Traditional Chinese characters |
| Chinese SC | Noto Sans SC | 400 | Simplified Chinese characters |

### Weight defaults

- Headings: **500** (`--font-weight-display: 500`)
- Body: **400** (`--font-weight-body: 400`)

### Type scale

| Token | Size | Usage |
|---|---|---|
| `--text-xs` | 10px | *(unused — reserved)* |
| `--text-sm` | 14px | Labels, metadata, footnotes, captions |
| `--text-base` | 16px | Body text, buttons, nav links |
| `--text-lg` | 20px | Lead paragraphs, feature descriptions |
| `--text-xl` | 25px | *(unused — reserved)* |
| `--text-2xl` | 32px | h3, card titles |
| `--text-3xl` | 52px | h2, section titles |
| `--text-4xl` | 64px | h1, hero headline |

### Line heights

- Headings: `1.10–1.20` (tight)
- Body: `1.60` (relaxed, book-like)

### Principles

- Serif for authority (headings), sans for utility (body/UI)
- Single weight (500) for all headings — consistent voice
- Relaxed body leading (`1.60`) for literary reading feel
- Chinese characters use Noto Sans TC/SC at 400 weight, 44px in hero cards

---

## 4. Spacing

Base unit: **8px**.

| Token | Value |
|---|---|
| `--space-1` | 4px |
| `--space-2` | 8px |
| `--space-3` | 12px |
| `--space-4` | 16px |
| `--space-5` | 20px |
| `--space-6` | 24px |
| `--space-8` | 32px |
| `--space-12` | 48px |

Section vertical spacing: `96px` on desktop, `60px` on tablet, `48px` on phone.

Container max-width: `1200px`, centred. Gutter: `24px` desktop, `16px` tablet, `12px` phone.

---

## 5. Border radius

| Token | Value | Usage |
|---|---|---|
| `--radius-sm` | 8px | Standard buttons, cards |
| `--radius-md` | 12px | Primary buttons, inputs, nav |
| `--radius-lg` | 16px | Featured containers, hero visuals |

No sharp corners — softness is core to the identity.

---

## 6. Elevation and shadows

| Token | Value | Usage |
|---|---|---|
| `--elev-flat` | `none` | Default state |
| `--elev-ring` | `0 0 0 1px var(--border)` | Border-like halo for interactive cards |
| `--elev-raised` | `rgba(0,0,0,0.05) 0px 4px 24px` | Whisper-soft elevation |
| `--elev-chunky` | `0 4px 0 0 var(--border-soft)` | Duolingo-style chunky shadow |
| `--elev-chunky-accent` | `0 4px 0 0 color-mix(...)` | Chunky shadow in accent colour |

The chunky bottom shadows on buttons and interactive elements are the signature YakYak flourish — they create a playful, tactile press-down effect on click (`translateY(3px)` + shadow reduction).

---

## 7. Components

### Buttons

**Primary CTA:**
- Background: `--accent` (#c96442)
- Text: `--accent-on` (#faf9f5)
- Radius: `--radius-md` (12px)
- Weight: 700
- Shadow: `--elev-chunky-accent`
- Hover: `translateY(3px)`, shadow shrinks
- Active: `translateY(4px)`, shadow removed

### Cards

**Feature card:**
- Background: `--surface` (#faf9f5)
- Border: `1px solid --border`
- Radius: `--radius-lg` (16px)
- Padding: 40px
- Shadow: none (flat) on default
- Hover: accent border, raised shadow, `translateY(-4px)`

**Character card (hero):**
- Background: `--bg` (#f5f4ed)
- Border: `1px solid --border`
- Radius: `--radius-md` (12px)
- Padding: 20px
- Shadow: `--elev-ring`
- Float animation infinite

### Navigation

- Sticky top nav with frosted background (`rgba(245,244,237,0.95)` + `backdrop-filter: blur`)
- Logo: left, CTA button: right
- Links hidden on mobile (< 768px)

### Forms

- Input radius: 12px
- Focus ring: `3px rgba(201,100,66,0.2)`
- Font: `--font-body`
- Submit button: same style as primary CTA
- Mobile: form stacks vertically

### Stealth banner

- Background: `#8b8c7a` (olive)
- Sticky at top, pulsing dot indicator
- Font: 14px

---

## 8. Component manifest

| Component | Selector | Key classes |
|---|---|---|
| Button primary | `button, .btn.btn-primary` | `.btn`, `.btn-primary` |
| Feature card | `.feature-card` | — |
| Character card | `.char-card` | `.char-card-1` through `.char-card-4` |
| Character unit | `.char-unit` | `.char-symbol`, `.char-pinyin` |
| Hero | `.hero` | `.hero-content`, `.hero-visual`, `.hero-visual-content` |
| Navigation | `header nav` | `.logo-link`, `.links` |
| Waitlist form | `#waitlist-form-main` | `.waitlist-inline`, `.btn-notify` |
| Stealth banner | `.stealth-banner` | `.stealth-dot` |
| Footer | `footer` | `.footer-content`, `.footer-bottom` |

---

## 9. Responsive breakpoints

| Name | Width | Key changes |
|---|---|---|
| Phone | < 480px | Stacked layout, reduced padding, 28px heading |
| Tablet | < 768px | Single column hero, hidden nav links, 60px section padding |
| Desktop | < 1024px | Hero collapses to single column (if not already) |
| Wide | 1200px+ | Full layout, max container width |

---

## 10. Motion and animation

| Animation | Duration | Element |
|---|---|---|
| Hero card float | 5–6s ease-in-out | `.char-card-*` |
| Bell ring | 2s ease-in-out infinite | `.bell-animate` |
| Star pop | 2s ease-in-out infinite | Hero star gif |
| Hover lift | 0.3s | `.feature-card` |
| Button press | 0.15s | `.btn-primary` |
| Page load (construction) | 0.6s ease | `.uc-heading`, `.uc-desc` |

---

## 11. Core layout patterns

### Section alternation
Light sections (`--surface` to `--bg` gradient) alternating with dark sections (`--fg` background, white text) creates chapter-like reading rhythm.

### Hero layout
Two-column grid (1fr 1fr) on desktop. Left column: headline + lead + CTA. Right column: floating character cards in a relative container. On tablet/phone: single column, hero visual below text.

### Features grid
Auto-fit grid with minimum 320px columns, `48px` gap. Cards hover to accent border with lift.

### Footer grid
Auto-fit grid with minimum 250px columns. Dark background (`--fg`), warm silver text (`#b0aea5`). Four columns: About, Products, Help, Social.

---

## 12. Content guidelines

- **Voice**: Warm, encouraging, straightforward. Good for a secondary school student to understand.
- **Tone**: Approachable and human — not cold or techy.
- **Dashes**: Do NOT use m-dashes (—). Use single dash or rephrase.
- **Quotes**: Single quotation marks for quotes, double for quotes within quotes.
- **Oxford commas**: Do NOT use.
- **Placeholders**: Short honest placeholders (—, grey block, labelled stub) instead of invented metrics ("10× faster").
- **Avoid**: Lorem ipsum, generic emoji icon rows, left-border accent cards, purple gradients, warm beige page washes not justified by brand.
