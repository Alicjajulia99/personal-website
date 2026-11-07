# Personal Website — Learning Roadmap

The goal is twofold: **ship a personal website** (about me, projects, contact) and **learn React and the tools around it by building it myself**.

## How we work together

- **You write the code, Claude coaches.** For each step: Claude explains the concept, you try it, Claude reviews and suggests improvements. Ask for hints before asking for full solutions.
- **Small steps, frequent commits.** Every finished step = one git commit with a clear message. Later we switch to branches + pull requests to practice a real team workflow.
- **Tick the boxes** in this file as you go, and commit the change. This file is your progress log.
- **Stuck for more than ~20 minutes?** Ask. Being stuck is part of learning; being stuck for hours is not.

## The stack (and why)

| Piece | Choice | Why |
|---|---|---|
| Build tool | [Vite](https://vite.dev) | Fast, simple, the standard way to start a React app today |
| UI | React + **TypeScript** | TypeScript catches mistakes early and makes Storybook/components much nicer. (Plain JavaScript is fine too if you prefer to start simpler.) |
| Routing | React Router | Separate pages: Home, About, Projects, Contact |
| Styling | CSS Modules → design tokens later | Learn real CSS first; tokens come from Figma in Phase 4 |
| Hosting | GitHub Pages | Free, lives next to your code, auto-deploys on every push |
| Backend | Node + Express (Phase 3) | Same language as the frontend, so less to learn at once |
| Components | Storybook (Phase 5) | Build and document components in isolation |

Everything lives on your **personal** GitHub account (`Alicjajulia99`).

---

## Phase 0 — Setup (Git, GitHub, first app)

- [ ] Create the project with Vite (`npm create vite@latest`) and run it locally
- [ ] Understand the folder structure: `index.html`, `src/main.tsx`, `src/App.tsx`, `package.json`
- [ ] `git init`, make a `.gitignore`, first commit
- [ ] Create a repo on GitHub and push to it
- [ ] Learn the daily loop: `git status` → `git add` → `git commit` → `git push`

**Concepts:** what npm is, what a dev server does, what Git tracks vs. what GitHub hosts.

## Phase 1 — React fundamentals by building the site

- [ ] Rough sketch of the pages on paper (5 minutes, not Figma yet)
- [ ] **Components & JSX** — build `Header`, `Footer`, `Hero`
- [ ] **Props** — make a reusable `ProjectCard` that takes a title, description, link, image
- [ ] **Lists & keys** — keep projects in a `projects.ts` data file and render them with `.map()`
- [ ] **State** (`useState`) — a light/dark theme toggle, or filtering projects by tag
- [ ] **Routing** — pages for Home, About, Projects, Contact with React Router
- [ ] **Styling** — CSS Modules, flexbox and grid, make it work on mobile
- [ ] **Effects** (`useEffect`) — e.g. remember the theme choice in `localStorage`

**Concepts:** one-way data flow, why components re-render, "lifting state up".

## Phase 2 — Deploy it

- [ ] Deploy to GitHub Pages with a GitHub Actions workflow
- [ ] Every push to `main` updates the live site automatically
- [ ] Start using branches + pull requests for new features

**Concepts:** build vs. dev, what `npm run build` produces, CI/CD basics.

## Phase 3 — Backend

Something real for a personal site to need:

- [ ] Small Express server with one route (`GET /api/health`)
- [ ] `GET /api/projects` — serve projects from the backend instead of a local file
- [ ] Fetch it from React (loading and error states!)
- [ ] `POST /api/contact` — a working contact form (validate input, send yourself an email)
- [ ] Environment variables and secrets (never commit them)
- [ ] Deploy the backend (e.g. Render or Railway) and connect the frontend to it

**Concepts:** HTTP and REST, JSON, CORS, client vs. server, async/await.

## Phase 4 — Figma & design

- [ ] Learn Figma basics: frames, auto layout, components, variants
- [ ] Define a small design system: colors, typography, spacing
- [ ] Redesign the site in Figma
- [ ] Turn the design system into CSS variables (design tokens) in code
- [ ] Rebuild the UI to match the design

**Concepts:** design tokens, consistency, designing *with* components.

## Phase 5 — Storybook & a component library

- [ ] Add Storybook to the project
- [ ] Write stories for `Button`, `ProjectCard`, `Header`, … (all variants and states)
- [ ] Accessibility checks with the a11y addon
- [ ] Component tests with Vitest + Testing Library
- [ ] Publish Storybook alongside the site

**Concepts:** building components in isolation, API design for props, testing.

## Phase 6 — Polish (ongoing)

- [ ] Accessibility pass (keyboard navigation, contrast, alt text)
- [ ] SEO and social preview images
- [ ] Performance (Lighthouse score)
- [ ] Optional: custom domain

---

## Progress log

Write a line here whenever you finish something or learn something that clicked.

- 2026-11-07 — Made the plan.
