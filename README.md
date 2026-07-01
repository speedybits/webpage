# speedybits · Projects

A single-page portfolio summarizing the projects I've worked on — robotics & embedded
systems, AI & voice assistants, games, and web apps.

**Live site:** https://speedybits.github.io/webpage/

## Views

- **Grid** — the default card grid, filterable by search box and category chips.
- **Timeline** — a chronological spine (newest first) grouped by year, with sticky
  year-jump pills that highlight as you scroll. Toggle between them top-right of the
  controls bar. Each project's date span comes from the `dates` map in `index.html`
  (`name: [started, last-active]`, sourced from GitHub `created_at` / `pushed_at`).

## Editing

Everything is in `index.html`. To add, remove, or reword a project, edit the
`projects` array near the bottom of the file. Each entry looks like:

```js
{ name: "project-name", desc: "One-line description.", lang: "Python",
  stars: 0, category: "Robotics", url: "https://github.com/speedybits/project-name" }
```

- Omit `url` (or leave it empty) to mark a project **private** — the card shows a
  "Private" badge and is not clickable.
- `category` values automatically become filter chips at the top of the page.

No build step, no dependencies — it's plain HTML/CSS/JS served straight by GitHub Pages.
