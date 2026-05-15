# getheddle.github.io

Source for the org-level landing page that lives at
[**getheddle.dev**](https://getheddle.dev) (and as a fallback at
`https://getheddle.github.io/`).

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
CNAME           Custom domain mapping (getheddle.dev).
README.md       This file.
```

## DNS

The `CNAME` file declares `getheddle.dev` as the custom domain. GitHub
Pages will serve the site at that domain once the apex / `www` DNS
records point to GitHub:

```
@        A       185.199.108.153
@        A       185.199.109.153
@        A       185.199.110.153
@        A       185.199.111.153
www      CNAME   getheddle.github.io.
```

If DNS is not yet configured, the site is reachable at
`https://getheddle.github.io/` until it is.

## Editing the site

Plain HTML + CSS — no build step, no Jekyll, no Hugo. Open
`index.html` in a browser to preview locally. Edit, commit, push;
GitHub Pages republishes within a minute.

If the page grows beyond a single landing screen, migrate to a static
site generator (Jekyll is the path of least resistance with GH Pages)
or fold into the heddle MkDocs site as a separate top-level section.

## License

Site source: MPL 2.0 (matching the rest of the family).
