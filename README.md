<div align="center">
  <h1>BITS Video Prompt Generator</h1>
  <p><strong>One-shot Google Flow ad kits for affiliate products.</strong></p>
  <p>One product photo in. One copy-ready master prompt + three clean ingredient images out.</p>
  <p>
    <img src="https://img.shields.io/badge/Google%20Flow-4285F4?style=flat&logo=google&logoColor=white" alt="Google Flow" />
    <img src="https://img.shields.io/badge/Veo-000000?style=flat&logo=google&logoColor=white" alt="Veo" />
    <img src="https://img.shields.io/badge/ChatGPT-10A37F?style=flat&logo=openai&logoColor=white" alt="ChatGPT" />
    <img src="https://img.shields.io/badge/Indonesian-FF0000?style=flat&logo=googletranslate&logoColor=white" alt="Indonesian" />
    <img src="https://img.shields.io/badge/9%3A16-111827?style=flat" alt="9:16 vertical" />
    <img src="https://img.shields.io/badge/10s-111827?style=flat" alt="10 seconds" />
    <img src="https://img.shields.io/badge/license-Proprietary-1F2937?style=flat" alt="Proprietary" />
  </p>
</div>

---

## ✨ What is this?

**BITS Video Prompt Generator** is a collection of production-ready meta-prompts for **Google Flow**. It replaces the usual storyboard → keyframe → editing pipeline with one structured reply:

- **One master prompt** — ready to copy and paste into Flow.
- **Three ingredient images** — clean references, ready to upload.
- **Zero storyboards** — no shot list, no phase gates, no approval step.

Give ChatGPT a product photo — plus a model photo if you choose the **Dengan Model** workflow — and it returns everything Flow needs: a locked product, a locked human reference, a master frame, a real-world interaction frame, and a six-beat timeline.

Flow settings stay manual. The kit deliberately does not prescribe model names, duration presets, or upload steps. You configure Flow; the prompt handles the creative and visual locks.

> **Built for Indonesian affiliate ads.** Natural Indonesian voice-over, local environment and styling, no CTA, no music, no platform logos — one video can run on both TikTok and Shopee.

---

## 🎯 Two Workflows

| | **Dengan Model** | **Tanpa Model** |
|---|---|---|
| **Input** | 1 product photo + 1 model photo | 1 product photo only |
| **Human reference** | Full model: face, hair, skin tone, body proportions, wardrobe | No face, head, or torso; maximum one right hand and forearm, optional |
| **Best for** | Fashion, beauty, accessories, lifestyle demos | Packaged goods, tools, home, electronics, products that do not need a person |
| **Guide** | [`Dengan Model/README.md`](Dengan%20Model/README.md) | [`Tanpa Model/README.md`](Tanpa%20Model/README.md) |
| **Prompt** | [`Dengan Model/PROMPT.md`](Dengan%20Model/PROMPT.md) | [`Tanpa Model/PROMPT.md`](Tanpa%20Model/PROMPT.md) |

Both workflows use the same output contract: **one master prompt + three images**, nothing else.

---

## 📦 What You Get

| Output | Role |
|---|---|
| `flow-1-product.png` | **Product authority.** Clean packshot on a plain background. Locks silhouette, color, material, finish, logo, and label. |
| `flow-2-hero.png` | **Master frame.** Product — and model, if selected — in a realistic environment. Locks scale, composition, lighting, grade, and the opening product state. |
| `flow-3-lifestyle.png` | **Interaction frame.** Generated from `flow-2-hero.png`, never from the original photo. Locks hand interaction, scale, and real-world use. |
| **Master prompt** | One copy-safe fenced code block: product lock, human lock, style, overlays, six-beat timeline, cinematic notes, and negative rules. |

> **Three images. One prompt. No storyboard.** The response is intentionally limited so nothing breaks when copied into Flow.

---

## 🖼️ Ingredient Pipeline

```text
product photo  (+ model photo)
        │
        ▼
flow-1-product.png        product authority
        │
        ▼
flow-2-hero.png           master frame: scale, light, environment
        │
        ▼
flow-3-lifestyle.png      interaction, hand, real-world use
        │
        ▼
Google Flow Ingredients + master prompt
        │
        ▼
10 seconds · 9:16 · 6 beats
```

Generate in order: **1 → 2 → 3**. Image 2 is the master frame. Image 3 is generated from Image 2 so the product, lighting, and environment stay consistent.

---

## 🚀 Quick Start

### Requirements

| Requirement | Notes |
|---|---|
| **ChatGPT with image generation** | Produces the master prompt and the three images. |
| **Google Flow account** | Generates the final video. |
| **1 product photo** | Complete product, one variant, no marketplace UI. |
| **1 model photo** | **Dengan Model only.** One person, clear face, simple wardrobe. |
| **No build step** | Everything is Markdown. Clone or download and go. |

### Steps

1. **Clone the repository** (optional — you can also download the files).

   ```bash
   git clone https://github.com/Banten-IT-Solutions/BITS-Video-Prompt-Generator.git
   cd BITS-Video-Prompt-Generator
   ```

2. **Choose a workflow**: `Dengan Model` or `Tanpa Model`.

3. **Open a new ChatGPT chat** and upload the required photos.
   - `Dengan Model`: product first, then model.
   - `Tanpa Model`: product only.

4. **Paste the entire `PROMPT.md`** and send it.

5. **Download the three images in order** — `flow-1-product.png`, `flow-2-hero.png`, `flow-3-lifestyle.png`.

6. **Upload the three images to Flow Ingredients**, paste the master prompt, configure Flow, and generate 3–4 variations.

> **Do not upload the original product photo to Flow.** The three ingredients already carry the product identity. Uploading the raw photo again can pull the result back toward the original framing.

---

## 🧩 What the Prompt Locks

| Section | What it controls |
|---|---|
| `PRODUCT LOCK` | Concrete shape, proportions, colors, materials, finish, logo placement, and visible label text. One product unit only. |
| `MODEL LOCK` / `HAND LOCK` | Face, skin, hair, wardrobe — or, for product-only ads, one hand with consistent skin tone, nails, and sleeve. |
| `INGREDIENT ROLES` | Image 2 is the master frame; Image 3 must match it exactly. |
| `REFERENCE USE` | References are not frames. They cannot be displayed, animated, panned, zoomed, or frozen. |
| `STYLE` | Concrete lighting, lens, depth of field, color grade, and material realism. |
| `ON-SCREEN GRAPHICS` | Exactly three text overlays and two graphic accents. Never covering the logo. |
| `TIMELINE` | Six beats, first frame already showing the product, closing hold at the end. |
| `CINEMATIC NOTES` | Camera, photographic effect, and transition for each beat. Simple moves and hard cuts only. |
| `NEGATIVE` | No faces or people where banned, no duplicate product, no floating product, no plastic skin, no HDR, no wide-angle distortion, and no visual effects soup. |

---

## 🎬 Video Blueprint

| # | Beat | Window | Job |
|---|---|---|---|
| 1 | **Hook** | 0.0–1.5s | Product visible from frame one, headline overlay |
| 2 | **Feature** | 1.5–3.0s | One clear product detail, feature label, red arrow |
| 3 | **Demo** | 3.0–4.5s | One simple action; hard cut to the second product state if applicable |
| 4 | **Benefit** | 4.5–6.5s | Product in use, benefit card, yellow sparkle |
| 5 | **Value** | 6.5–8.0s | Hero detail or product beauty shot |
| 6 | **Closing** | 8.0–10.0s | Steady hold, no on-screen text, no new action |

**Format:** 10 seconds · 9:16 vertical · 1080×1920 · 24fps · six beats · hard cuts under 0.2s.

**Audio:** Indonesian voice-over, 26–32 words total, starts at 0.2s. No music, no jingle, no captions, no subtitles.

**Text:** exactly three overlays and two graphic accents. No CTA, no prices, no ratings, no platform logos.

> ⚙️ **Flow note:** available duration depends on the selected Flow model and plan. The prompt is written for 10 seconds; if your Flow model only supports 8 seconds with ingredients, generate the closest duration and cut the last beat in Flow.

---

## 🧠 Drift Control

Long prompts are not the problem. Drift comes from repetition, conflicting values, and overloading beats.

| Principle | Implementation |
|---|---|
| **One value per attribute** | Each attribute is stated once, in the section that owns it. No duplicate lighting, lens, or wardrobe instructions. |
| **One idea per beat** | Each beat has one dominant action. Extra actions are cut, not compressed. |
| **No circular references** | The prompt never says “same lighting as Image 2.” It names the source, direction, temperature, and shadow quality. |
| **Master frame first** | Image 2 locks scale, environment, lighting, and opening state before Image 3 is generated. |
| **Hard cuts only** | No dissolve, whip pan, zoom blur, morph, or mechanism animation. |
| **Concrete language** | Light source, surface, material, lens, and action. No “beautiful,” “stunning,” or “high quality.” |

The master prompt targets **950–1150 words** — a density guide, not a quota. Every sentence must add one visual fact.

---

## 📁 Repository Structure

```text
BITS-Video-Prompt-Generator/
├── Dengan Model/
│   ├── PROMPT.md                      # meta-prompt: product + model → Flow kit
│   ├── README.md                      # workflow guide (Bahasa Indonesia)
│   └── References/
│       ├── IMAGE-STORYBOARD-GENERATOR.MD
│       └── VIDEO-GENERATOR.MD
├── Tanpa Model/
│   ├── PROMPT.md                      # meta-prompt: product only → Flow kit
│   ├── README.md                      # workflow guide (Bahasa Indonesia)
│   └── References/
│       ├── IMAGE-STORYBOARD-GENERATOR.MD
│       └── VIDEO-GENERATOR.MD
└── README.md
```

`References/` contains the legacy storyboard and video generators. They are kept for reference only and are **not** part of the one-shot Flow pipeline.

---

## 📚 Documentation

| Document | Purpose |
|---|---|
| [`Dengan Model/README.md`](Dengan%20Model/README.md) | Step-by-step guide for the product + model workflow, including troubleshooting. |
| [`Dengan Model/PROMPT.md`](Dengan%20Model/PROMPT.md) | The meta-prompt to paste into ChatGPT for the product + model kit. |
| [`Tanpa Model/README.md`](Tanpa%20Model/README.md) | Step-by-step guide for the product-only workflow, including optional hand handling. |
| [`Tanpa Model/PROMPT.md`](Tanpa%20Model/PROMPT.md) | The meta-prompt to paste into ChatGPT for the product-only kit. |
| [`Dengan Model/References/`](Dengan%20Model/References/) | Archived storyboard and video generators for the model workflow. |
| [`Tanpa Model/References/`](Tanpa%20Model/References/) | Archived storyboard and video generators for the product-only workflow. |

**New here?** Open the README for your chosen workflow first. It explains what to upload, what comes back, and how to recover when a result drifts. Then paste `PROMPT.md` into ChatGPT.

---

## ⚠️ Good to Know

AI video is probabilistic. The kit improves consistency, but it does not guarantee a perfect first generation.

| Product type | Success chance | Notes |
|---|---|---|
| Simple shape, matte, no logo | High | Best fit for one-shot generation |
| Clear logo, texture, simple hand action | Medium | Expect 2–4 variations |
| Reflective, transparent, apparel, food, skincare | Low–medium | May need several attempts |
| Many variants or tiny logos | Low | Pick one variant; avoid extreme logo close-ups |

- Generate **3–4 variations** and pick the most consistent one.
- If one image fails, **regenerate that image only** in the same chat.
- If a hand keeps failing, switch that beat to a **product-only shot**.
- Preserve the product's original label. Never invent certifications, badges, or claims.

---

## 🤝 Contributing

Contributions are welcome. Keep the contract intact:

- **One master prompt + three images.** No storyboards, keyframes, shot lists, or timing tables.
- **No Flow settings in the prompt output.** The user configures Flow manually.
- **No CTA, music, captions, or platform logos.**
- **Test both workflows** before opening a pull request.
- **Do not rewrite `References/`** unless the change is explicitly about the legacy docs.

Open an issue for bugs, drift patterns, or product categories that need better handling.

---

## 📄 License

All rights reserved by **Banten IT Solutions**. Published for reference and use with the BITS Video Prompt Generator workflows. For commercial licensing, white-label deployment, or collaboration, contact [bits.co.id](https://bits.co.id).

---

<div align="center">
  <strong>BITS Video Prompt Generator</strong> — built with ❤️ by <a href="https://bits.co.id"><strong>Banten IT Solutions</strong></a>
</div>
