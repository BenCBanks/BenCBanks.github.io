---
layout: post
title: Post Component Demo
type: Essay
description: A reference post showing every available formatting component — pull quotes, stat grids, highlight boxes, and code blocks.
tags: [meta]
---

This post exists as a reference. Each section below shows one component you can drop into any future post. The source file lives at `_posts/2026-04-06-component-demo.md`.

---

## Pull quote

Use a pull quote to call out a key sentence. Wrap any paragraph in a `<div class="pullquote">` tag.

**HTML to paste:**

```html
<div class="pullquote">
  <p>Your standout sentence goes here. Keep it short — one or two lines.</p>
</div>
```

**What it looks like:**

<div class="pullquote">
  <p>The interesting question is never whether something will change — it is how long that change takes to matter.</p>
</div>

---

## Stat grid

Use a stat grid to highlight 2–4 numbers side by side. Each number gets a `.stat-cell` inside the `.stat-row` wrapper. Add or remove cells freely — the grid adjusts automatically.

**HTML to paste:**

```html
<div class="stat-row">
  <div class="stat-cell">
    <div class="stat-num">84%</div>
    <div class="stat-label">Single-family zoned</div>
  </div>
  <div class="stat-cell">
    <div class="stat-num">111</div>
    <div class="stat-label">Candidate parcels</div>
  </div>
  <div class="stat-cell">
    <div class="stat-num">3</div>
    <div class="stat-label">Target deals</div>
  </div>
</div>
```

**What it looks like:**

<div class="stat-row">
  <div class="stat-cell">
    <div class="stat-num">84%</div>
    <div class="stat-label">Single-family zoned</div>
  </div>
  <div class="stat-cell">
    <div class="stat-num">111</div>
    <div class="stat-label">Candidate parcels</div>
  </div>
  <div class="stat-cell">
    <div class="stat-num">3</div>
    <div class="stat-label">Target deals</div>
  </div>
</div>

---

## Highlight box

Use a highlight box for a key fact, quote, or regulatory clause you want to stand apart from the body text. Bold the important part if needed.

**HTML to paste:**

```html
<div class="highlight-box">
  <p><strong>Key fact:</strong> Your important sentence or clause goes here. Keep it to two or three lines.</p>
</div>
```

**What it looks like:**

<div class="highlight-box">
  <p><strong>Table 4-1, footnote 1:</strong> Lot standards do not apply to individual sublots but do apply to the parcel on which the sublot is located.</p>
</div>

---

## Code block

Use triple backticks for any code or data. Add the language name after the opening backticks for syntax highlighting.

**Markdown to paste:**

````
```python
# Filter to candidate parcels
candidates = parcels[
    (parcels["zone_class"].str.startswith("N1")) &
    (parcels["sqft"] >= parcels["zone_min_sqft"] * 2.3)
]
```
````

**What it looks like:**

```python
# Filter to candidate parcels
candidates = parcels[
    (parcels["zone_class"].str.startswith("N1")) &
    (parcels["sqft"] >= parcels["zone_min_sqft"] * 2.3)
]
```

---

## Combining them

In a real post you would mix these with normal Markdown paragraphs. The components are just HTML snippets — paste them anywhere in your `.md` file and write regular text above and below them. Everything else (headers, bold, lists, links) is standard Markdown.
