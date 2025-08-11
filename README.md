Welcome to Nambili Samuel's Badge Repository! These badges represent collections awarded to Nambili Samuel by various entities and institutions as recognition of his work.  Howver, there is no single badge published by Nambili. Please take a moment to read the README file and the license for this repository


# Recognition Badges Grid for GitHub Page

This file contains **two** ready-to-copy options for displaying recognition badges in a clean, consistent grid with 6 cards per row and equal-sized frames.

* **Option A — GitHub Pages (recommended)**: Uses embedded CSS + HTML. Works in a GitHub Pages site (`.html` or `.md` in a Jekyll site) where style tags are allowed.
* **Option B — README / Plain Markdown fallback**: Uses a pure-Markdown / HTML table-friendly approach that works in `README.md` (no external CSS required). It's less flexible visually but safe for GitHub repo pages.

---

## Option A — GitHub Pages (CSS Grid, responsive, polished)

> Paste into a `.md` file that will be rendered on GitHub Pages (or into an HTML include). This uses a small `<style>` block to keep everything equal-sized and responsive. 6 cards per row on wide screens, fewer on small screens.

```html
<style>
.badges-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr); /* 6 columns */
  gap: 1rem;
  align-items: start;
}

.badge-card {
  background: #ffffff;
  border: 1px solid rgba(15,23,42,0.06);
  border-radius: 10px;
  box-shadow: 0 6px 18px rgba(2,6,23,0.04);
  padding: 12px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  min-height: 180px; /* ensures equal card heights */
  box-sizing: border-box;
}

.badge-image {
  width: 96px;
  height: 96px;
  object-fit: contain;
  margin-bottom: 10px;
}

.badge-meta {
  font-size: 12px;
  color: #334155;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.badge-title {
  font-weight: 700;
  font-size: 13px;
  color: #0f172a;
}

.badge-org {
  font-size: 12px;
  color: #475569;
}

.badge-date {
  font-size: 11px;
  color: #6b7280;
}

.badge-cta {
  margin-top: 8px;
  font-size: 12px;
}

/* Responsiveness */
@media (max-width: 1400px) { .badges-grid { grid-template-columns: repeat(4, 1fr); } }
@media (max-width: 900px)  { .badges-grid { grid-template-columns: repeat(3, 1fr); } }
@media (max-width: 700px)  { .badges-grid { grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 420px)  { .badges-grid { grid-template-columns: repeat(1, 1fr); } }
</style>

<div class="badges-grid">

  <!-- Repeat this block for each badge -->
  <div class="badge-card">
    <img class="badge-image" src="https://placehold.co/96x96/EEE/000?text=Badge" alt="Badge: Example Certified" />
    <div class="badge-meta">
      <div class="badge-title">Example Certified — Level 1</div>
      <div class="badge-org">Issued by: Acme Institute</div>
      <div class="badge-date">Issued: 2024-08-01</div>
      <div class="badge-cta"><a href="#" rel="noopener">View credential</a></div>
    </div>
  </div>
  <!-- /badge block -->

  <!-- Add as many badge blocks as you need -->

</div>
```

**How to use**

* Replace the `src` image URL with your badge image link (SVG/PNG). Keep image sizes roughly square for best fit.
* Use the same `min-height` in `.badge-card` if you want taller or shorter cards.
* Change `grid-template-columns` if you want fewer than 6 columns on the largest view.

---

## Option B — README-friendly (pure Markdown / HTML table fallback)

GitHub `README.md` sanitizes many style tags — so here is a simple table approach that keeps frames visually consistent. It fakes a grid with a table: 6 badges per row. Each cell holds an image and metadata underneath.

> Note: Table cells will auto-size in GitHub; to keep visuals consistent, host badge images with identical dimensions (e.g., 200x200) or use square SVG badges.

```markdown
| ![Badge1](https://placehold.co/150x150/EEE/000?text=1)<br>**Example Certified**<br>Acme Institute<br>2024-08-01 | ![Badge2](https://placehold.co/150x150/EEE/000?text=2)<br>**Data Wizard**<br>Data Academy<br>2023-12-12 | ![Badge3](https://placehold.co/150x150/EEE/000?text=3)<br>**Open Source Hero**<br>OSS Foundation<br>2022-05-05 | ![Badge4](https://placehold.co/150x150/EEE/000?text=4)<br>**Cloud Pro**<br>CloudOrg<br>2024-01-20 | ![Badge5](https://placehold.co/150x150/EEE/000?text=5)<br>**Security Ace**<br>SecureNow<br>2021-09-09 | ![Badge6](https://placehold.co/150x150/EEE/000?text=6)<br>**UX Star**<br>Design Guild<br>2020-11-11 |
|---|---|---|---|---|---|

<!-- Add more rows as needed -->
```

This keeps each badge cell with the same image size so visually everything lines up.

---

## Recommended badge metadata fields

When you add a new badge, keep metadata consistent in this order to enable automatic parsing later (if you add scripts):

* `title` (e.g. "Data Wizard — Level 2")
* `issuer` (organization name)
* `issued_date` (ISO format: `YYYY-MM-DD`)
* `credential_url` (link to verify)
* `image` (SVG/PNG, ideally square)

---

## Optional: JSON data block for automation

You can place a JSON block in your repo (e.g. `badges.json`) and loop through it in a Jekyll include to render cards automatically. Example schema:

```json
[
  {
    "title": "Example Certified — Level 1",
    "issuer": "Acme Institute",
    "issued_date": "2024-08-01",
    "credential_url": "https://example.org/cred/123",
    "image": "https://example.org/badges/badge1.svg"
  }
]
```

---

## Quick tips

* Use SVG for sharpness at any size.
* Host images on your repo (`/assets/badges/`) or a CDN for reliability.
* Keep all badge images square and same pixel dimensions for the best uniform look in fallback mode.
* Use `rel="noopener"` on external links for security.

---

If you want, I can:

* Generate a ready-to-fill `badges.json` or Jekyll include file that renders the grid automatically.
* Convert your existing badge list into the exact card HTML (you can paste it here).

Which would you like next?
