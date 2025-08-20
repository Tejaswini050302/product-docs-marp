---
marp: true
theme: product-docs
title: "Product Documentation Presentation"
description: "Maintainable docs in version control; export to HTML/PDF/PPTX with Marp CLI"
paginate: true
math: katex
headingDivider: 2
---

<!-- _class: lead -->
# Product Documentation with Marp
### A maintainable, multi-format workflow
**Author:** Technical Writer · **Email:** 24f2004718@ds.study.iitm.ac.in

---

## Why Marp for Product Docs?

- **Version-control friendly:** Just Markdown in Git.
- **Repeatable builds:** Render to **HTML / PDF / PPTX** via CI.
- **Single source of truth:** Reuse diagrams, snippets, and equations.
- **Custom styling:** Apply a **company theme** via CSS.
- **Math support:** Powered by KaTeX for algorithm docs.

> Tip: Keep one slide deck per feature / release, and tag versions.


---

## Conventions & Structure

- Each top-level `##` heading becomes a new slide (via `headingDivider: 2`).
- Use **speaker notes** with `<!-- {{{ note }}} -->` and `<!-- {{{ /note }}} -->` blocks (Marp / Marpit notes).
- Keep code in fenced blocks with language hints for highlighting.
- Link to the **Raw GitHub URL** to embed this deck elsewhere.
- **Email for feedback:** 24f2004718@ds.study.iitm.ac.in

---

## Algorithmic Complexity (Math demo)

Inline math like \(T(n) = O(n \log n)\).

Block math:

$$
T(n) = 
\begin{cases}
1, & n \le 1 \\
2\,T(n/2) + n, & n > 1
\end{cases}
\quad\Rightarrow\quad T(n) = O(n \log n)
$$

---

<!-- Custom slide-level styling via directives -->
<!-- style: "background: linear-gradient(135deg, #0ea5e9 0%, #64748b 100%); color: white; padding: 40px;" -->

## Slide with Custom Styling

- This slide uses a **Marp `style` directive** for a gradient background.
- Text color overridden to **white** for contrast.
- Try also: `class: box small` to use theme classes.

---

<!-- Background image with overlay style -->
![bg opacity:0.15](https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=1400&q=80)

## Architecture Overview (Background Image)

- The background image is applied with `![bg]` syntax.
- Add `opacity` to improve text readability.
- Combine with theme classes or `style` to polish the look.

---

## Export & Automation

**Local export** (requires Node.js):  
```bash
npm i -g @marp-team/marp-cli
marp slides.md --allow-local-files --theme-set themes/product-docs.css --html  -o dist/slides.html
marp slides.md --allow-local-files --theme-set themes/product-docs.css --pdf   -o dist/slides.pdf
marp slides.md --allow-local-files --theme-set themes/product-docs.css --pptx  -o dist/slides.pptx
```

**CI export**: See `.github/workflows/marp.yml` to auto-build on every push.

---

## GitHub Raw URL

Use the template:

`https://raw.githubusercontent.com/USERNAME/REPOSITORY/main/slides.md`

Replace `USERNAME` and `REPOSITORY` with your GitHub account and repo name.

Examples:
- `https://raw.githubusercontent.com/acme-inc/product-docs/main/slides.md`
- `https://raw.githubusercontent.com/yourname/marp-decks/main/slides.md`

---

## Contact & Next Steps

- Feedback and content requests: **24f2004718@ds.study.iitm.ac.in**
- Add more slides for API changes, release notes, and runbooks.
- Keep assets in `assets/` and reference with relative paths.

<footer>© 2025 Your Company — Product Docs</footer>
