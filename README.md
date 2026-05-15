# getheddle.github.io

Source for the org-level landing page. Content is served by GitHub
Pages at **<https://getheddle.github.io/>**. The public-facing URL
**<https://getheddle.dev>** is configured outside this repo (as a
Cloudflare-side 301 redirect to the `.github.io` URL).

This repository exists to give the `getheddle` family a single
**front door** — a one-page overview that introduces
[`heddle`](https://github.com/getheddle/heddle),
[`heddle-sdk`](https://github.com/getheddle/heddle-sdk),
and [`warp-design`](https://github.com/getheddle/warp-design), explains
the design philosophy, and points readers at the right documentation
site for what they need next.

Per-project deep documentation lives elsewhere:

- heddle docs: <https://getheddle.github.io/heddle/>
- SDK docs: <https://getheddle.github.io/heddle-sdk/>
- warp-design (vision + ADRs): repo-rendered markdown

## What's here

```text
index.html      Single-page landing.
style.css       Light/dark mode, no framework, no network fonts.
README.md       This file.
```

## URL setup

GitHub Pages serves directly at <https://getheddle.github.io/> — no
custom-domain CNAME configured on the repo. The shorter brand URL
<https://getheddle.dev> is owned in Cloudflare and redirects to the
`.github.io` URL via a Cloudflare Page Rule (or equivalent). The
`CNAME` file is intentionally absent so that GitHub Pages doesn't
issue its own reverse redirect (`.github.io` → custom domain) and
fight the Cloudflare-side redirect.

## Editing the site

Plain HTML + CSS — no build step, no Jekyll, no Hugo. Open
`index.html` in a browser to preview locally. Edit, commit, push;
GitHub Pages republishes within a minute.

If the page grows beyond a single landing screen, migrate to a static
site generator (Jekyll is the path of least resistance with GH Pages)
or fold into the heddle MkDocs site as a separate top-level section.

## License

Site source: MPL 2.0 (matching the rest of the family).
