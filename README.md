# getheddle.github.io

Source for the org-level landing page. Content is served by GitHub
Pages at **<https://getheddle.dev/>**. The backing GitHub Pages URL is
**<https://getheddle.github.io/>**.

This repository exists to give the `getheddle` family a single
**front door** — a one-page overview that introduces
[`heddle`](https://github.com/getheddle/heddle),
[`heddle-sdk`](https://github.com/getheddle/heddle-sdk),
[`warp-design`](https://github.com/getheddle/warp-design), and
[`heddle-workspace`](https://github.com/getheddle/heddle-workspace), shows
what is moving across the family, explains
the design philosophy, and points readers at the right documentation
site for what they need next.

Per-project deep documentation lives elsewhere:

- heddle docs: <https://getheddle.dev/heddle/>
- SDK docs: <https://getheddle.dev/heddle-sdk/>
- warp-design (vision + ADRs): repo-rendered markdown

## What's here

```text
CNAME           GitHub Pages custom domain: getheddle.dev.
index.html      Single-page landing.
style.css       Light/dark mode, no framework, no network fonts.
README.md       This file.
```

## URL setup

GitHub Pages serves the site with `getheddle.dev` as the custom domain.
The root `CNAME` file is intentional and must remain present because
Pages uses it to bind the custom domain to this repository.

DNS should point the apex to GitHub Pages and `www` to the Pages host:

```text
getheddle.dev      A/AAAA  GitHub Pages apex records
www.getheddle.dev  CNAME   getheddle.github.io
```

Do not add a competing Cloudflare redirect rule for `getheddle.dev` unless
the Pages custom domain is removed first.

## Editing the site

Plain HTML + CSS — no build step, no Jekyll, no Hugo. Open
`index.html` in a browser to preview locally. Edit, commit, push;
GitHub Pages republishes within a minute.

If the page grows beyond a single landing screen, migrate to a static
site generator (Jekyll is the path of least resistance with GH Pages)
or fold into the heddle MkDocs site as a separate top-level section.

## License

Site source: MPL 2.0 (matching the rest of the family).
