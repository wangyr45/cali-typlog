# Cali for Typlog

A Typlog v3 theme port of the current [cali.so](https://cali.so/) design, based on
upstream revision `a35dcf2` (September 2026). This replaces the earlier 2024-style
port. See [NOTICE.md](NOTICE.md) and [LICENSE](LICENSE) for attribution.

The layout uses a 600 px column, dotted side rules, a 240 px halftone portrait,
three illustrated navigation cells, numbered section labels, the 10 most recent article
rows, and a fixed glass dock. The reading page uses the same column, a paper
cover frame, metadata rules, and an optional table of contents.

The dock contains Home, Archive, Projects, the configured About link, and all secondary
links from Typlog. Secondary links keep their order and new-tab setting. The row
scrolls when space is limited; the preferences menu also lists all links by name.
The first three primary links always control the home navigation cards. Older
`nav_cards` settings are ignored. Known social domains use built-in platform icons, including official WeChat
account links on `mp.weixin.qq.com`.
Public article thumbnails use Typlog's cover field, set with Edit Cover in the
post editor. No article body is requested to find an image. Protected covers are
excluded from public theme markup.

The default profile uses the site's own name, summary, logo, and navigation.
The runtime settings asset `_config/cali-typlog` can override introduction text,
portrait, article count and heading, projects, collections, and article
cover/TOC visibility. This uses Typlog's documented `query.config` PRO feature.
Partial settings inherit defaults; explicit empty lists remove optional sections.
Non-PRO sites retain normal content editing and use build-time defaults for the
extra fields. There is no custom Typlog admin form in this repository.

See [CONTENT.zh-CN.md](CONTENT.zh-CN.md) for the exact editing workflow and
[config.example.json](config.example.json) for a configuration asset example.
Do not put account secrets or private image URLs in public display configuration.

## Build and preview

```sh
python3 build.py
python3 -m venv .venv
.venv/bin/pip install -r requirements-dev.txt
.venv/bin/python preview.py
.venv/bin/python -m unittest discover -s tests
node --test tests/*.test.cjs
python3 -m http.server 8765 --bind 127.0.0.1 --directory preview
```

The build produces three templates with inline CSS/JavaScript, five bundled images, and
`dist/cali-typlog-0.8.0.zip`. No Node runtime or separate image account is required. Typlog serves the bundled
images through its theme static URL. Keep the assets directory in the release. Edit source files under `src/` and run the build; do not edit the
generated root templates. The `/settings-demo/` preview exercises runtime settings without rebuilding.
The `/components/` preview demonstrates optional
collections with clearly named samples. The home page does not claim these
samples as the site's owner's collection.

## Home identity

The site title uses 28 px type on desktop and 24 px on mobile. The opening motto
uses a restrained spectrum gradient. A native subscription button follows the
introduction when Typlog subscriptions are enabled. On mobile, the 150 px portrait
sits above the text. No continuous canvas animation runs.

Archive and tag primary links use the original small polaroid stacks. They load
up to three public article covers from the linked list page. No article bodies
are fetched. Public Moments previews retain the same behavior. Empty or failed
requests preserve the original working link and paper placeholder.

## Projects

The dock opens `/#projects`, a dedicated view within the home template. It follows
Cali's compact project rows and mobile layout. The view includes Shigu, DockPic,
and portus; the portus row states its regional availability. CSS fragment routing
works without JavaScript and requires no new Typlog Page. The view shares the
home page's canonical URL and cannot be indexed as a separate `/projects` page.
A small script updates the title, current navigation, focus, and menu state.

The `projects` array and `projects_intro` support the same runtime configuration
as other optional collections. Empty projects remove the view and its shortcuts.
Icons use public URLs with monogram fallbacks. The default Shigu icon comes from
the official Chrome store; DockPic and portus use the owner-supplied bundled images.

## Footer and images

The hero uses an independent bundled portrait. The dock always uses the native
site logo, even when the hero portrait changes. Dock tooltips are positioned from
each button, outside the scrolling container. Content landmarks keep focus without
a page-sized outline; interactive controls retain visible keyboard focus.

The Contact column retains native social links and icons, adds tree connectors,
and shows small destination preview cards. It does not request social profile data.
The old Index column is replaced by support and backup WeChat QR cards. Image links
work without scripting; a native dialog adds enlargement, Escape dismissal, and
focus restoration. The design credit appears before Powered by Typlog.

The five owner-provided images have EXIF and text metadata removed. Pixel data and
color profiles are preserved. QR images are never redrawn, cropped, or recolored.
Use `portrait`, `support_qr`, and `wechat_qr` to change public images; empty QR values
hide their cards. The dock logo remains independent of these settings.

## Typlog contract

This targets the legacy interface used by Ueno 0.8.0: `home.j2`, `list.j2`,
`item.j2`, and the `style`, `script`, and `body` blocks. It is not a v4 theme.
The official `render_subject_content(site, page)` macro controls protected
content. Native search, theme switching, subscriptions, comments, and audio
remain Typlog responsibilities. Offline fixtures cannot prove service behavior.

See [INSTALL.zh-CN.md](INSTALL.zh-CN.md) for installation paths. The zip is a file
distribution, not a verified one-click upload format. Nothing is published or
activated by the build.

## Deliberate adaptation boundaries

- The hero uses the uploaded portrait as a square, feathered halftone. The dock
  keeps its circular color avatar. Canvas or CORS failures retain the grayscale
  image; image failures retain the site initial.
- Fonts use the operating system stack. No third-party font or tracking request
  is added. Different fonts and introduction length affect exact text wrapping.
- Book and record shelves support click and arrow-key selection. Original React
  spring physics, shader easter eggs, photo service, remote project database, and AMA
  checkout are not part of this Typlog port.
- Navigation follows Typlog settings. Album cards load up to three public
  thumbnails from the linked same-site Moments page, without credentials.
  No invented photo or article totals,
  career entries, or original-author collection data are displayed.

## Failure states

- Failed theme images reveal a monogram, paper thumbnail, or text cover. A failed
  article cover is hidden. Article text and navigation remain available.
- Collections start as static lists with working links. JavaScript enables the
  shelf controls only after initialization succeeds. Arrow keys keep selection
  in the shelf without scrolling the page.
- The TOC handles duplicate anchors and updates after visible article content
  changes. Unrelated player updates do not reset its links or keyboard focus.
- Optional controls follow Typlog feature flags. Local preview search filters the
  fixture titles. Local email subscription is explicitly disabled; the production
  theme uses Typlog's native subscription handler.
- Test routes include `/empty/`, `/image-failure/`, `/long-content/`, `/diagram/`,
  `/no-script/`, `/navigation-demo/`, and `/navigation-overflow/`. The
  `/album-demo/` and `/archive-demo/` cover photo cards, platform icons, and year
  groups. The `/cover-demo/` routes compare uploaded, replaced, and removed sample covers.
  These fixtures are excluded from the distribution.

Native search, email delivery, protected-content authentication, and audio
playback still require a Typlog service preview before production activation.


## Version 0.8.0

Secondary links precede About, and a fixed podcast card opens in a new tab.
Contact links show platform-specific hover cards. The optional `contact_cards`
setting provides owner-maintained profiles; no service counters are invented.
The compact support area stays beside Contact on mobile.

The music and book shelves include the owner's selected artwork, perspective
layout, drag and keyboard selection, and reduced-motion support. Dark mode uses
a separate halftone portrait. Appearance offers Light, System, and Dark, with
per-tab persistence and native Typlog theme integration. Duplicate links have
been removed from preferences.
