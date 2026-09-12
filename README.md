# Cali for Typlog

A Typlog v3 theme based on the current cali.so design. See [NOTICE.md](NOTICE.md)
and [LICENSE](LICENSE) for attribution.

## Install

This repository places all required theme files at its root. Version 0.4.0 uses
three self-contained templates: home.j2, list.j2, and item.j2.

Typlog PRO users can open Settings → Themes & Design → Change and enter
`wangyr45/cali-typlog@0.4.0` in the theme picker. The Git tag must match the version in
theme.json. See the [official installation guide](https://typlog.com/changelog/use-own-theme).

Keep a copy of the previous theme and injected styles. Use a real Typlog preview
to check native search, subscriptions, comments, audio, and protected content
before activation. Local fixture tests cannot prove service behavior.

## Content

- The home page shows the ten most recent articles and episodes.
- The circular color portrait uses the site logo.
- Home navigation cards always use the first three primary links. Legacy
  `nav_cards` overrides are ignored.
- Same-site Moments links show up to three public photo thumbnails, with no
  credentials. Failed requests retain a working album link and placeholder.
- Writing lists group posts by year, with pixel year markers and compact dates.
- The dock contains Home, Archive, the configured About entry, and secondary links.
- Secondary links keep their order and new-tab settings. Long rows can scroll.
  Zhihu, Xiaohongshu, X/Twitter, Bilibili, YouTube, Telegram, GitHub, Weibo, and
  Instagram use built-in platform icons.
- The footer credits [Cali Castle](https://github.com/CaliCastle/cali.so).
- Public article thumbnails use the cover set in the post editor. Protected
  article covers are not emitted by the theme.
- Optional PRO settings use the `_config/cali-typlog` JSON asset.

See [the content guide](CONTENT.zh-CN.md) and [example settings](config.example.json).
The theme does not include account credentials, subscriber data, or article bodies.

## Files

The Jinja files include their CSS and JavaScript. No Node server or separate asset
host is required. Content and access control remain managed by Typlog.

The editable source is maintained separately from this installation repository.
To update the installed theme, publish the new templates and a matching version tag.
