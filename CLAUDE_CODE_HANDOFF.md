# Task: push and deploy the FDA calendar dashboard site

Paste this whole prompt into a Claude Code session that has push access to
`github.com/srikaryallala/fda-calendar-dashboard` (e.g. your local `claude` CLI,
already `gh auth login`'d as srikaryallala).

---

I have an empty GitHub repo at `https://github.com/srikaryallala/fda-calendar-dashboard`
(public). I have two files locally: `index.html` and `README.md` (attached / in this
folder) that make up a static site — no build step, no dependencies to install.

Please:

1. Initialize a git repo in the folder containing these two files (or clone the empty
   remote and copy them in), commit them on `main`, and push to
   `https://github.com/srikaryallala/fda-calendar-dashboard.git`.
2. Enable GitHub Pages on the repo via the `gh` CLI or GitHub API: source = deploy from
   branch `main`, folder `/ (root)`. (Equivalent: `gh api -X POST repos/srikaryallala/fda-calendar-dashboard/pages -f "source[branch]=main" -f "source[path]=/"` — if that returns a 409 because Pages is already configured, use PUT instead of POST.)
3. Poll `gh api repos/srikaryallala/fda-calendar-dashboard/pages` (or the web UI) until
   the build status is `built`, then report back the live URL (should be
   `https://srikaryallala.github.io/fda-calendar-dashboard/`).
4. Open/fetch the live URL and confirm the page loads and shows FDA decision rows (it
   pulls data live from a public Supabase project — no further setup needed there, the
   page is fully self-contained).

Report back the final live URL and confirm the page renders data correctly.

---

The two files to push are attached to this message in Claude.ai / Cowork (or already in
this folder if you downloaded them there): `index.html`, `README.md`.
