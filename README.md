# 🎨 The Visual Thinking Toolkit

> **A curated index and prompt-engineering suite of 275+ visual thinking artifacts used by designers, concept artists, animators, game developers, and filmmakers to explore, define, sequence, construct, validate, and communicate visual ideas.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-4285F4?style=for-the-badge&logo=google-chrome)](https://rachidd31.github.io/visual-thinking-tools/)
[![License: MIT](https://img.shields.io/badge/License-MIT-amber.svg?style=for-the-badge)](LICENSE)
[![Design System](https://img.shields.io/badge/UI-Material%203%20Design-34A853?style=for-the-badge&logo=material-design)](https://m3.material.io/)
[![Schema Validation](https://img.shields.io/badge/Schema-JSON%20Schema%202020--12-EA4335?style=for-the-badge&logo=json)](schema.json)

---

## 🧭 Overview

In creative production—whether designing an indie game, storyboarding a feature film, building an enterprise design system, or art-directing a brand campaign—ideas must be crystallized into **tangible visual artifacts** before execution.

The **Visual Thinking Toolkit** establishes an authoritative taxonomy and interactive catalog of the visual models, diagrams, and production documents across 14 creative disciplines and 11 workflow stages.

Every artifact in the catalog is paired with:
* **Production Specifications**: Required Inputs, Deliverable Outputs, Spatial Structure, and Real-World Examples.
* **AI Visual Prompts**: Ready-to-use prompt templates for **Midjourney**, **Flux**, and **DALL·E 3**.
* **AI Concept & LLM Prompts**: Structured brainstorming and specification prompts for **Claude 3.7**, **GPT-4o**, and **Gemini**.

---

## ✨ Features

* 🔍 **Instant Search & Real-Time Filtering**: Search across artifact names, definitions, stages, and outputs.
* 🌓 **Material 3 Design System**: Native light and dark themes with smooth transitions and elevation tokens.
* 🏷️ **14 Creative Disciplines**: Concept Art, Character Design, Storyboarding, UI/UX, Game Design, Infoviz, Motion Design, Brand Architecture, Animation, Environment, Audio, and Music.
* ⏱️ **11 Production Workflow Stages**: Research $\to$ Ideation $\to$ Exploration $\to$ Selection $\to$ Definition $\to$ Structure $\to$ Narrative $\to$ Construction $\to$ Execution $\to$ Validation $\to$ Communication.
* 🤖 **Dynamic AI Prompt Generator**: Automatically generates calibrated visual generation prompts and LLM design briefs from any card definition.
* 💾 **Local Persistence**: Save your favorite artifacts and bookmarks directly in your browser (`localStorage`).
* ➕ **In-Browser Card Editor & JSON Importer**: Edit cards inline or paste custom JSON tool definitions with live schema validation against [`schema.json`](schema.json).
* ⚡ **Zero-Backend Architecture**: 100% client-side vanilla JavaScript/HTML/CSS. No build steps, no node_modules, no dependencies.

---

## 📁 Repository Structure

```
visual-thinking-tools/
├── index.html                       # Standalone single-page web application (GitHub Pages entrypoint)
├── tools.html                       # Master SPA source
├── schema.json                      # Formal JSON Schema (Draft 2020-12) validating tool data models
├── categories.txt                   # Complete 275-artifact taxonomy across 14 categories & 11 stages
├── genData.txt                      # AI dataset generator prompt & contract
├── README.md                        # Project documentation
├── LICENSE                          # MIT License
├── .gitignore                       # Git ignore definitions
│
└── components/                      # Modular HTML UI components
    ├── hero.html                    # Top hero banner component
    ├── left-sidebar.html            # Navigation sidebar with search, theme toggle, views & filters
    ├── card.html                    # Interactive tool card template with hover-expanded metadata
    ├── card-details.html            # Deep-dive popup modal with specs, media & AI prompt generators
    ├── card-edit.html               # In-browser card editing modal
    ├── add-json-modal.html          # JSON import/validation modal for adding new tools
    └── footer.html                  # App footer component
```

---

## 📊 Taxonomy & Covered Disciplines

| Category | Key Artifacts | Typical Workflow Stages |
| :--- | :--- | :--- |
| **Research** | Moodboard, Precedent Study, Reference Sheet, Trend Report, Cultural Context Map | Research, Exploration |
| **Drawing** | Thumbnail Sketch Sheet, Gesture Study, Perspective Grid, Orthographic Turnaround | Ideation, Exploration, Construction |
| **Character** | Character Design Sheet, 360° Turnaround, Model Sheet, Rig Range-of-Motion Sheet | Definition, Construction, Structure |
| **Environment** | Mood Key, Establishing Shot Painting, Greybox Blockout, Top-Down Level Map | Exploration, Definition, Construction |
| **Story** | Beat Sheet, Story Spine, Script Breakdown, Shot List, Storyboard Panel Sequence | Narrative, Structure, Construction |
| **Animation** | Exposure Sheet (X-Sheet), Timing Chart, Key Pose Layout, Walk Cycle Sheet | Structure, Construction, Execution |
| **Motion** | Style Frame, Kinetic Typography, Transition Study, Compositing Layer Stack | Ideation, Definition, Execution |
| **UI/UX** | Information Architecture, Wireframe, User Journey Map, Component Library | Research, Structure, Execution |
| **Brand** | Logo Construction Grid, Typography System Sheet, Brand Architecture Diagram | Definition, Structure, Validation |
| **Games** | Game Design Document (GDD), Level Blockout, Skill Tree, UI/HUD Wireframe | Definition, Structure, Validation |
| **Infoviz** | Sankey Diagram, Gantt Chart, Heat Map, Process Swimlane Diagram | Structure, Execution, Communication |
| **Handoff** | Design Spec (Redlines), Asset Manifest, Pipeline Diagram, QA Bug Template | Communication, Structure, Validation |
| **Sound & Music** | Sound Palette, Foley Cue Sheet, Temp Track Playlist, Leitmotif Chart | Exploration, Definition, Construction |

---

## 🛠️ Data Model & Schema

Each tool object adheres strictly to [`schema.json`](schema.json):

```json
{
  "n": "Thumbnail Sketch Sheet",
  "c": "drawing",
  "s": "Ideation",
  "e": "✏️",
  "p": "Rapid, low-fidelity conceptual drawings exploring volumetric massing, silhouette, and fundamental compositional structure.",
  "i": "Core design brief requirements, bounding envelope constraints, and functional component footprints.",
  "o": "Single canvas containing 20-50 small, energetic structural studies exploring diverse formal directions.",
  "st": "Monochrome loose sketches arranged in a dense contact sheet layout focusing entirely on contour and negative space.",
  "ex": "Executing 40 thumbnail sketches in 60 minutes to discover an aggressive form factor for a sci-fi tactical transport craft.",
  "img": "https://images.unsplash.com/photo-1581291518655-9523c932edcf?w=640&h=400&fit=crop"
}
```

---

## 🚀 Deployment & Running Locally

### 1. GitHub Pages (1-Click Hosting)
1. Push this repository to GitHub.
2. In **Settings** $\to$ **Pages**, set **Source** to `Deploy from a branch` (`main` / `/ (root)`).
3. Your toolkit is instantly live at `https://<username>.github.io/<repo-name>/`.

### 2. Local Preview
Because this app is 100% static:
* **VS Code**: Right-click `index.html` $\to$ **Open with Live Server**.
* **Python**: `python -m http.server 8000` (open `http://localhost:8000`).
* **Node.js**: `npx serve .`

---

## 📜 License

Distributed under the [MIT License](LICENSE). Open-source for designers, engineers, and creators worldwide.
