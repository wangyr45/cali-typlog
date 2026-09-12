# Cali for Typlog

A Typlog v3 theme based on the current cali.so design. See [NOTICE.md](NOTICE.md)
and [LICENSE](LICENSE) for attribution.

Version 0.7.0 includes verified desktop and mobile previews, project artwork,
per-button dock tooltips, and QR image dialogs. Publishing does not activate the
theme in Typlog. Native service behavior still requires a Typlog preview.

## Install

This repository places all required theme files at its root. Version 0.7.0 uses
three self-contained templates: home.j2, list.j2, and item.j2.

Typlog PRO users can open Settings → Themes & Design → Change and enter
`wangyr45/cali-typlog@0.7.0` in the theme picker. The Git tag must match the version in
theme.json. See the [official installation guide](https://typlog.com/changelog/use-own-theme).

Keep a copy of the previous theme and injected styles. Use a real Typlog preview
to check native search, subscriptions, comments, audio, and protected content
before activation. Local fixture tests cannot prove service behavior.

## Content

- The home page shows the ten most recent articles and episodes.
- The hero uses the supplied portrait as a feathered halftone image, with a
  grayscale image fallback. The dock independently follows the Typlog site logo
  and keeps its circular color appearance.
- The larger site title, soft spectrum motto, and native subscription link
  provide a clearer home introduction.
- Home navigation cards always use the first three primary links. Legacy
  `nav_cards` overrides are ignored.
- Same-site Moments links show up to three public photo thumbnails, with no
  credentials. Failed requests retain a working album link and placeholder.
- Writing lists group posts by year, with pixel year markers and compact dates.
- The dock contains Home, Archive, Projects, the configured About entry, and secondary links.
- Secondary links keep their order and new-tab settings. Long rows can scroll.
  Zhihu, Xiaohongshu, X/Twitter, Bilibili, YouTube, Telegram, GitHub, Weibo, and
  Instagram use built-in platform icons. Official WeChat account links on
  `mp.weixin.qq.com` use the WeChat icon.
- Archive and tag links use small polaroid stacks with up to three public article
  covers. Empty collections and failed requests retain their links and placeholders.
- The Projects dock entry opens `/#projects`, with compact rows for Shigu, DockPic,
  and portus. It requires no additional Typlog Page and works without JavaScript.
  The portus row states that the mainland China store is not supported.
- `projects` and `projects_intro` can be edited through the runtime JSON asset.
  DockPic and portus include their supplied artwork in the theme assets. The view
  shares the home canonical URL. Route focus does not draw a frame around the view.
- The Contact footer preserves native social icons and adds destination previews.
- Support and backup WeChat account QR images replace the footer index. They open
  in an accessible enlargement dialog, with direct image links as a fallback.
- The footer credits [Cali Castle](https://github.com/CaliCastle/cali.so) before
  Powered by Typlog.
- Dock tooltips align with their own buttons, including scrollable secondary links.
- Public article thumbnails use the cover set in the post editor. Protected
  article covers are not emitted by the theme.
- Optional PRO settings use the `_config/cali-typlog` JSON asset.

See [the content guide](CONTENT.zh-CN.md) and [example settings](config.example.json).
The theme does not include account credentials, subscriber data, or article bodies.

## Files

The Jinja files include their CSS and JavaScript. Keep the complete `assets/`
directory when installing. Typlog serves these images through its theme static
URL. No Node server or separate asset host is required. Content and access control
remain managed by Typlog. Supplied artwork has location and text metadata removed;
its pixel data is unchanged.

The editable source is maintained separately from this installation repository.
To update the installed theme, publish the new templates and a matching version tag.
