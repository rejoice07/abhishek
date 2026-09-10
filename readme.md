# Abhishek Dave | Personal Portfolio Website

A modern, futuristic personal portfolio for **Abhishek Dave** — IT Developer, AI Enthusiast, Web Developer, and Game Developer. Built as a single self-contained HTML file with an animated 3D-style web-network background, dark crimson/black theme, and full responsive layout.

**Brand statement:** *Building ideas. Forging technology.*

---

## 🚀 Quick Start

This is a **single self-contained HTML file** — no build step, no dependencies, no installation required.

### Option 1 — Open directly
Double-click `abhishek-dave-portfolio.html` and it opens in your default browser.

### Option 2 — Local server (recommended for testing forms/animations)
```bash
# Python
python3 -m http.server 8000

# Node
npx serve .
```
Then visit `http://localhost:8000/abhishek-dave-portfolio.html`.

### Option 3 — Deploy for free
Drag-and-drop deploy, no config needed:
- **Netlify** → [app.netlify.com/drop](https://app.netlify.com/drop) — drag the HTML file in
- **Vercel** → `vercel deploy`
- **GitHub Pages** → push to a repo, rename file to `index.html`, enable Pages in repo settings
- **Cloudflare Pages** → connect repo or drag-and-drop

---

## ⚠️ Before You Publish — Required Edits

The content rules for this site say **never fabricate information**. So a few placeholders are intentionally left in the file for you to fill in with real links. Find-and-replace these across the file:

| Placeholder | Where it appears | Replace with |
|---|---|---|
| `[ADD GITHUB LINK]` | Projects section, Contact section, Footer | Your real GitHub profile/repo URL |
| `[ADD LINKEDIN LINK]` | Contact section, Footer | Your real LinkedIn profile URL |
| `[ADD EMAIL]` | Contact section (`mailto:`), Footer | Your real email address |
| `[ADD PROJECT DEMO]` | Car Showroom project card | Live demo URL, if available |

**Quick way to replace them (Mac/Linux terminal):**
```bash
sed -i '' 's|\[ADD GITHUB LINK\]|https://github.com/yourusername|g' abhishek-dave-portfolio.html
sed -i '' 's|\[ADD LINKEDIN LINK\]|https://linkedin.com/in/yourusername|g' abhishek-dave-portfolio.html
sed -i '' 's|\[ADD EMAIL\]|you@example.com|g' abhishek-dave-portfolio.html
```
*(On Linux, drop the `''` after `-i`.)*

Already wired up and does **not** need editing: the **EduTrack AI** project's live demo button, which points to `https://riishilmmehta.github.io/edutrack-ai/`.

---

## 📄 Making the Contact Form Actually Send Emails

Right now the form validates input (name, email format, required message) but doesn't send anywhere — it just shows a confirmation message in the UI. To make it functional, pick one:

- **[Formspree](https://formspree.io)** — add `action="https://formspree.io/f/yourFormId"` and `method="POST"` to the `<form>` tag
- **[EmailJS](https://www.emailjs.com)** — add their JS SDK and call `emailjs.send()` inside the existing submit handler
- **Netlify Forms** (if hosting on Netlify) — just add `data-netlify="true"` and a hidden `form-name` input to the `<form>` tag

---

## 🗂 File Structure

```
abhishek-dave-portfolio.html   ← everything (HTML + CSS + JS in one file)
README.md                       ← this file
```

Because it's a single file, there's nothing to "build" — every style, animation, and script lives inline.

---

## 🎨 Design System

| Element | Value |
|---|---|
| Background | `#08080b` (void black) |
| Surface | `#131318` / `#1a1a21` (charcoal) |
| Accent | `#ff3b52` (ember red) / `#d81e3f` (crimson) |
| Text | `#f2f1ee` (bone) / `#8f8f9a` (ash, secondary) |
| Headings font | Sora (700–800 weight) |
| Body font | Inter |
| Monospace accents | JetBrains Mono (tags, kickers, code-like labels) |

The animated background is a **Canvas 2D particle network** — glowing red nodes connected by threads, with fake depth (parallax based on a `z` value per node) and mouse-interactive "web-shooter" style connecting lines. It respects `prefers-reduced-motion` and automatically scales particle count to screen size for performance.

---

## 📱 Sections Included

1. Hero (animated intro + CTAs)
2. About (bio + trait pills + 4 focus cards)
3. Education (timeline card — ITM SLS Baroda University)
4. Skills (6 categorized skill groups)
5. Projects (7 full project cards: NovaForge, Auronix, EduTrack AI, Smart Curriculum & Attendance, Car Showroom, AI/CV Project, Game Dev)
6. Achievements (4 achievement cards)
7. Leadership (NovaForge team lead spotlight)
8. Builder Mindset (Idea → Research → Design → Development → Testing → Presentation flow)
9. Technology Interests (6-cell grid)
10. Currently Exploring (learning tag cloud)
11. Developer Journey (Student → ... → Future Developer timeline)
12. What's Next (future goals list)
13. Contact (validated form + direct links)
14. Footer

---

## ✅ Technical Notes

- **No build tools, no npm, no bundler** — works by just opening the file
- **Fully responsive**: desktop, tablet, and mobile all have dedicated layouts (not just a shrunk desktop view)
- **Accessible**: semantic HTML, visible focus states, `prefers-reduced-motion` support, form field error messaging
- **SEO-ready**: meta description, Open Graph tags, semantic headings, inline favicon (no external file needed)
- **No fabricated content**: no fake stats, testimonials, job history, or invented awards — only what was explicitly provided, with `[ADD ...]` placeholders where real data is still needed

---

## 🔧 Optional: Migrating to React + Vite + Tailwind + Framer Motion

The original spec's preferred stack was React + Vite + Tailwind + Framer Motion + Lucide React, with this structure:

```
src/
├── components/
├── sections/
├── assets/
├── data/
├── App.jsx
└── main.jsx
```

This delivery is the plain HTML/CSS/JS version for instant, zero-setup use. If you'd like the componentized React version instead (recommended once you're ready to add routing, a CMS, or more advanced interactivity), that can be built as a follow-up — just ask.

---

*Built with passion and code. © 2026 Abhishek Dave.*
