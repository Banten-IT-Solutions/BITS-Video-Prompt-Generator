<div align="center">
  <h1>BITS Video Prompt Generator</h1>
  <p><strong>One-shot Google Flow ad kits for affiliate products.</strong></p>
  <p>One product photo (plus optional model reference) in. One copy-ready master prompt + three clean ingredient images out.</p>
  <p>
    <img src="https://img.shields.io/badge/Google%20Flow-4285F4?style=flat&logo=google&logoColor=white" alt="Google Flow" />
    <img src="https://img.shields.io/badge/Veo-000000?style=flat&logo=google&logoColor=white" alt="Veo" />
    <img src="https://img.shields.io/badge/ChatGPT-10A37F?style=flat&logo=openai&logoColor=white" alt="ChatGPT" />
    <img src="https://img.shields.io/badge/Indonesian-FF0000?style=flat&logo=googletranslate&logoColor=white" alt="Indonesian" />
    <img src="https://img.shields.io/badge/9%3A16-111827?style=flat" alt="9:16 vertical" />
    <img src="https://img.shields.io/badge/10s-111827?style=flat" alt="10 seconds" />
  </p>
</div>

---

## ✨ What is this?

**BITS Video Prompt Generator** is a collection of production-ready meta-prompts for **Google Flow**. It replaces the usual storyboard → keyframe → editing pipeline with one structured reply:

- **One master prompt** — ready to copy and paste into Flow.
- **Three ingredient images** — clean references, ready to upload.
- **Zero storyboards** — no shot list, no phase gates, no approval step.

Give ChatGPT a product photo — plus a model photo for **Dengan Model** — and it returns a product-locked master prompt, three ingredient images, and a fixed six-beat timeline whose actions, overlays, and visual treatment adapt to the product evidence and selected workflow.

Flow settings stay manual. The kit deliberately does not prescribe model names, duration presets, or upload steps. You configure Flow; the prompt handles the creative and visual locks.

> **Built for Indonesian affiliate ads.** Natural Indonesian voice-over and locally relevant product context; environment/styling follow product category and reference, without stereotypes. No CTA, music, or platform logos.

---

## 🎯 Two Workflows

| | **Dengan Model** | **Tanpa Model** |
|---|---|---|
| **Input** | 1 product photo + 1 model photo | 1 product photo only |
| **Human reference** | Adult model only where relevant/safe; identity follows reference; product-only shots allowed. Muslimah product lines retain hijab rule. | No face/head/torso; optional single right hand only when useful |
| **Best for** | Products where adult model adds relevant context and can be represented safely | Products suited to neutral packshots; optional hand only when it adds useful scale/use context |
| **Guide** | [`Dengan Model/README.md`](Dengan%20Model/README.md) | [`Tanpa Model/README.md`](Tanpa%20Model/README.md) |
| **Prompt** | [`Dengan Model/PROMPT.md`](Dengan%20Model/PROMPT.md) | [`Tanpa Model/PROMPT.md`](Tanpa%20Model/PROMPT.md) |

Both workflows return **one master prompt + three images**. With Model may add a concise conditional note for unconfirmed model usage rights or material input ambiguity; this narrowly scoped exception does not change core output format.

---

## 📦 What You Get

For model workflow, use photos only when you have rights/consent for commercial publication. Requirements can vary by jurisdiction and platform; this repository is not legal advice.

| Output | Role |
|---|---|
| `flow-1-product.png` | **Product authority.** Clean packshot on a plain background. Locks silhouette, color, material, finish, logo, and label. |
| `flow-2-hero.png` | **Master frame.** Product-led, with model only if relevant and safe. Locks scale, composition, lighting, grade, and verified opening state. |
| `flow-3-lifestyle.png` | **Context frame.** Generated from `flow-2-hero.png`, never independently. Shows a product-appropriate interaction or product-only composition; hand/model use is optional when it adds no value or cannot be shown safely. |
| **Master prompt** | One copy-safe fenced code block: product lock, optional human lock, product-adaptive style/overlays/actions, fixed 10s six-beat timeline, cinematic notes, and negative rules. |

> **Three images. One prompt. No storyboard.** The response stays compact for copying; optional evidence-supported overlays/accents and conditional safety/rights notes remain controlled by the workflow prompt.

---

## 🧪 Golden Sample — Reply Shape

ChatGPT's reply must match this shape exactly. Anything beyond it is drift:

```text
FLOW KIT — Sereal Kacang Hijau x model wanita dewasa berhijab

[one fenced code block: the master prompt, starting at
"Create a single 10-second, 9:16 vertical product advertisement..."
and ending at the final "NEGATIVE:" line — nothing else inside]

flow-1-product.png
flow-2-hero.png
flow-3-lifestyle.png
```

Header format follows the workflow: `Tanpa Model` ends at the product name — no `x [model descriptor]`. Checklist: exactly one header line, exactly one code block, exactly three images in order. Optional overlays/accents are omitted when unsupported. With Model may append only conditional model-rights or material-ambiguity notes. No manifest, tables, Flow settings, or other commentary.

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
| **ChatGPT with image generation** | Produces the master prompt and the three images. Exact image ratio/resolution depends on generator; final video target remains 9:16, 1080×1920. |
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
| `MODEL LOCK` / `HAND LOCK` | Preserve reference identity/presentation when model appears; product-only or optional single-hand shots when more relevant. |
| `INGREDIENT ROLES` | Image 2 is the master frame; Image 3 must match it exactly. |
| `REFERENCE USE` | References are not frames. They cannot be displayed, animated, panned, zoomed, or frozen. |
| `STYLE` | Product-appropriate Indonesian context, concrete lighting/lens/grade, and realism matched across ingredient images. |
| `ON-SCREEN GRAPHICS` | Zero to three evidence-supported text overlays and zero to two useful accents. Omit anything redundant, unsupported, unreadable, or obstructive. |
| `TIMELINE` | Six beats across exactly 10 seconds; adapt actions to product evidence. Opening shows product; model appears only if relevant/safe; closing holds at end. |
| `CINEMATIC NOTES` | Camera, photographic effect, and transition for each beat. Simple moves and hard cuts only. |
| `NEGATIVE` | No faces or people where banned, no duplicate product, no floating product, no plastic skin, no HDR, no wide-angle distortion, and no visual effects soup. |

---

## 🎬 Video Blueprint

| # | Beat | Window | Job |
|---|---|---|---|
| 1 | **Hook** | 0.0–1.5s | Product visible from frame one; optional product-specific headline |
| 2 | **Feature** | 1.5–3.0s | One visible product detail; optional verified label/accent |
| 3 | **Demo** | 3.0–4.5s | One safe action only if product supports it; otherwise product presentation; verified state changes use hard match cut |
| 4 | **Benefit** | 4.5–6.5s | Evidence-supported use/result or neutral presentation; optional overlay/accent |
| 5 | **Value** | 6.5–8.0s | Hero detail or product beauty shot |
| 6 | **Closing** | 8.0–10.0s | Steady hold, no on-screen text, no new action |

**Format:** exactly 10 seconds · 9:16 vertical · 1080×1920 · six timed beats · hard cuts. If ingredient generation cannot output exact 9:16/1080×1920, use closest portrait source and crop safely; final video remains 9:16/1080×1920. Frame rate follows the Flow setting.

**Audio:** Indonesian voice-over, starts at 0.2s; 24–30 words is a pacing guide, not a quota. Keep lines natural and evidence-based. No music, jingle, captions, or subtitles.

**Text:** zero to three optional product-specific overlays and zero to two useful accents. Claims require visible evidence or explicit user-provided product information; staged demos do not prove performance. Omit unsupported or obstructive text. No CTA, prices, ratings, or platform logos.

> ⚙️ **Flow note:** prompt output always targets 10 seconds. Verify that the selected Flow model/plan supports this duration with ingredients. Do not simply cut the closing beat; if Flow cannot produce 10 seconds, use supported edit controls to retime all six beats while preserving opening, closing, and message. If that is unavailable, the workflow cannot meet this spec in that Flow mode.

---

## 🧠 Drift Control

Long prompts are not the problem. Drift comes from repetition, conflicting values, and overloading beats.

| Principle | Implementation |
|---|---|
| **One value per attribute** | Each attribute is stated once, in the section that owns it. No duplicate lighting, lens, or wardrobe instructions. |
| **One idea per beat** | Each beat has one dominant action. Extra actions are cut, not compressed. |
| **No circular references** | `STYLE` names source, direction, temperature, and shadow quality. Ingredient image descriptions reuse those values without introducing alternatives. |
| **Master frame first** | Image 2 locks scale, environment, lighting, and opening state before Image 3 is generated. |
| **Hard cuts only** | No dissolve, whip pan, zoom blur, morph, or mechanism animation. |
| **Product-specific copy** | Overlay claims, demonstrations, and benefits must fit the uploaded product and visible evidence; examples are not default claims. |
| **Concrete language** | Light source, surface, material, lens, and action. No “beautiful,” “stunning,” or “high quality.” |

The master prompt uses only as much detail as needed for accurate product/model locks, safety, and product-specific direction. The former 950–1200-word range is guidance only, never a quota.

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
- Ingredient images may use the generator's closest supported portrait size. Keep the final video exactly 9:16 at 1080×1920; crop or reframe safely without cutting off product or model.
- If a hand keeps failing, switch that beat to a **product-only shot**.
- Preserve the product's original label. Never invent certifications, badges, or claims.

---

## 🤝 Contributing

Contributions are welcome. Keep the contract intact:

- **One master prompt + three images.** No storyboards, keyframes, shot lists, or timing tables. Preserve exactly 10 seconds, 9:16, 1080×1920, and six beats; adapt actions and optional graphics to product evidence.
- **No Flow settings in the prompt output.** The user configures Flow manually.
- **No CTA, music, captions, or platform logos.**
- **Test both workflows** before opening a pull request.
- **Do not rewrite `References/`** unless the change is explicitly about the legacy docs.

Open an issue for bugs, drift patterns, or product categories that need better handling.

---

## 📄 License

Released under the [MIT License](LICENSE). Copyright © 2026 **Banten IT Solutions**.

---

<div align="center">
  <strong>BITS Video Prompt Generator</strong> — built with ❤️ by <a href="https://bits.co.id"><strong>Banten IT Solutions</strong></a>
</div>
