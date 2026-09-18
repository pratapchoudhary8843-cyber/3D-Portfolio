# Pratap Choudhary | Data Analyst · AI & ML — Portfolio

An interactive, single-page portfolio website featuring a 3D animated brain-shaped neural network background built with Three.js, along with a fully functional project showcase, resume viewer, and PDF resume generator.

## 🔗 Live Preview
Open `index.html` directly in any modern browser — no build step or server required.

## ✨ Features

### Visual / Experience
- **3D Neural Network Brain** — A WebGL brain-shaped particle system (Three.js) with glowing neurons, curved connection filaments, and ambient starfield dust. Rotates on hover and pulses on click.
- **4 Color Themes** — Midnight, Aurora, Nebula, Solar (press `T` or use the nav toggle).
- **Custom Cursor Glow**, animated typewriter intro, scroll-reveal sections, and a scroll progress bar.
- **Performance Mode** — Toggle (`P`) to reduce particle count for lower-end devices.
- **Ambient Audio** toggle (low hum via Web Audio API).

### Navigation & Usability
- Command Palette (`Ctrl/Cmd + K`) with searchable actions (go to section, download resume, toggle theme, etc.)
- Keyboard shortcuts panel (`?`) — includes `G H/P/R/C` section jumps, `D` for download, arrow-key project navigation.
- Section dot navigation, mobile drawer menu, "back to top" button, live clock, session timer, and live neuron/connection HUD stats.

### Projects Section
- Searchable + filterable project grid (All / AI-ML / Computer Vision / Web / Python).
- Click any card to open a detailed modal (tech stack, overview, features, skills) with **Prev/Next** navigation and a **Copy Link** action.
- **Random Project** shuffle button.
- Skill tags in the Resume section deep-link back into the filtered project search.

### Resume
- Animated skill bars, categorized tech stack tags, certifications, education, and experience timeline.
- **One-click PDF Resume Generator** using `jsPDF` — dynamically builds a formatted, multi-section PDF (objective, experience, education, projects, certifications, skills, soft skills, hobbies) and triggers a download.

### Contact
- Simple contact form that opens the user's mail client with a pre-filled subject/body via `mailto:`.

## 🛠️ Tech Stack
| Category | Technologies |
|---|---|
| Structure/Styling | HTML5, CSS3 (custom properties, responsive grid/flexbox) |
| Interactivity | Vanilla JavaScript (ES Modules) |
| 3D Graphics | [Three.js](https://threejs.org/) (r160, via import map) |
| PDF Generation | [jsPDF](https://github.com/parallax/jsPDF) (via CDN) |
| Fonts | Google Fonts — Inter, JetBrains Mono |

## 📁 File Structure
This is a **single self-contained HTML file** — all CSS and JavaScript are inlined, with only two external script dependencies loaded via CDN:
```
index.html          # Entire site: markup, styles, and logic
```

## ⚙️ External Dependencies (CDN)
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script type="importmap">
  { "imports": { "three": "https://unpkg.com/three@0.160.0/build/three.module.js" } }
</script>
```
An internet connection is required on first load to fetch these plus Google Fonts.

## ⌨️ Keyboard Shortcuts
| Key | Action |
|---|---|
| `Ctrl/Cmd + K` | Open command palette |
| `?` | Show shortcuts panel |
| `T` | Cycle theme |
| `P` | Toggle performance mode |
| `D` | Download resume PDF |
| `G` then `H/P/R/C` | Jump to Home / Projects / Resume / Contact |
| `←` / `→` | Navigate projects (inside modal) |
| `Esc` | Close any open dialog |

## 📇 Contact Info Embedded in Site
- **Email:** pratapchoudhary8843@gmail.com
- **Phone:** 8237462052
- **Location:** Nalasopara East, Maharashtra/Mumbai
- **LinkedIn:** [pratap-choudhary-131382373](https://linkedin.com/in/pratap-choudhary-131382373)

## 📝 Notes for Customization
- Update personal details, projects, and skills in the HTML `data-*` attributes (project cards) and the `ResumeData` object in the script (used for PDF generation).
- Adjust the `CONFIG` object in the Three.js section to change neuron count, brain radius, or connection density for performance tuning.
- Colors/themes are controlled via CSS custom properties under `:root` and `[data-theme="..."]` selectors.

## 📄 License
Personal portfolio — feel free to fork the structure for your own portfolio, but please replace personal content (name, contact info, resume data, project descriptions) with your own.
