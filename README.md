# Viktorie Láchová · Portfolio

My CV and data portfolio as a small static website: no build step, no framework.

| Page | What it shows |
|---|---|
| [`index.html`](index.html) | **CV**: roles, highlights, strengths, stack, education. Every role links to its projects. |
| [`projects.html`](projects.html) | **Data projects**: a 14-axis skill web. Click a skill to see the projects that prove it, browse the timeline since 2018, open any project for what I did, the result and the impact. |
| [`how-i-work.html`](how-i-work.html) | **How I work**: six habits, each backed by a real story, plus how I lead and what I am working on. |

## Files

- `projects.js`: all project data (one entry per project, oldest first). Edit this to add or update a project.
- `site.css`: shared colours, type and navigation for all pages.
- `.nojekyll`: serve the files as they are on GitHub Pages.

## Run locally

```bash
python -m http.server 8768
```

Then open http://localhost:8768.

## Adding a project

Add an object to `projects` in `projects.js`:

```js
{
  id: "my-project", title: "My project", org: "Company", kind: "job", // job | freelance | project | creative
  start: "2026-01", end: "2026-06", role: "Data Engineer",
  summary: "One or two sentences.",
  did: ["What I did"], result: "", impact: "",
  stack: ["dbt"], axes: ["pipe", "sem"], // keys of the skill web
  numbers: [{ v: "98.5%", l: "label" }],
}
```

Skill levels on the web are a self-assessment on a 0 to 5 scale, backed by the projects listed under each skill.
