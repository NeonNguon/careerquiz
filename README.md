# Creative Career Quiz — RMIT Vietnam (Digital Media)

A BuzzFeed-style reflection quiz for final-year Bachelor of Design (Digital Media)
students. Eight questions suggest which creative career archetype fits how a student
likes to work. It is a **starting point for thinking, not an assessment** — there are
no right answers.

Six archetypes: Studio Designer, Agency Creative, Interactive Designer, Production
Creative, Motion/Animation & 3D Artist, and Freelancer.

## Privacy

The quiz collects **nothing**. No cookies, no `localStorage`, no network requests,
no analytics. All logic runs in the browser and answers never leave the page. The
whole thing is one static HTML file that works offline.

## Test locally

Just **double-click `index.html`** — it opens in any browser and runs fully offline.
No build step, no server, no dependencies.

Worth checking before you publish:
- Resize the window down to **320px** wide (mobile) and up to **~900px** — the layout
  should stay readable at both.
- Tab through with the **keyboard only**: every option and button is reachable and
  shows a visible focus ring; Enter/Space activate them.
- Use **Back** mid-quiz — it returns to the previous question and removes that answer's
  points, so re-answering scores correctly.

## Publish on GitHub Pages

1. Create a GitHub repository and add `index.html` (and this `README.md`) to it.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select branch **`main`** and folder **`/ (root)`**, then **Save**.
5. Wait ~1 minute. Your quiz will be live at:
   `https://USERNAME.github.io/REPO/`

Replace `USERNAME` with your GitHub username and `REPO` with the repository name.

## Embed in RMIT Canvas

Add this snippet to a Canvas page (edit the page → HTML editor), replacing
`USERNAME` and `REPO`:

```html
<iframe src="https://USERNAME.github.io/REPO/" width="100%" height="700" style="border:1px solid #e3e5e9;border-radius:12px;"></iframe>
```

If Canvas strips the `<iframe>`, ask your Canvas admin to allow the
`USERNAME.github.io` domain, or use Canvas's **External URL** / Redirect tool to
link out to the quiz instead.

## Editing content

Everything lives in `index.html`. The quiz content is in two JavaScript objects near
the top of the `<script>` block:

- `QUESTIONS` — the eight questions, their options, and point weights.
- `RESULTS` — the archetype descriptions, roles, where-to-look, and honest first-step
  notes.

Scoring is a weighted tally: each answer adds points to one or more archetypes; the
highest total wins. Ties break in the priority order `ST > AG > IN > PR > PM > FR`.
The second-highest archetype is shown as the "see also" suggestion. Freelancer has an
intentionally low ceiling — it only wins on consistently independence-oriented answers.
