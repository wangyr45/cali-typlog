# Source and attribution

This port targets the current design of [cali.so](https://cali.so/), using
Cali Castle's `upstream/dev` revision `a35dcf2` (September 2026).
The original source is licensed under MIT. The full copyright and license text
is preserved in `LICENSE` and included in the distribution.

`src/reference.css` retains the original section labels, compact article rows,
print stacks, polaroid frames, navigation cards, and dock styles. Typlog templates,
and platform integration are implemented for this port.
`src/collections.css` and `src/collections.js` adapt the MIT-licensed
`components/vinyl-shelf.tsx`, `components/bookshelf.tsx`, and shelf styles from
the original `dev` branch. The transform geometry, gesture handling, wood
material, and transition curves are ported to dependency-free JavaScript.

The original author's biography, contact details, portrait, book covers, music
artwork, and account integrations are not copied into the theme. The default
introduction is adapted from the public page
https://wangyurui.com/me. It is editable through the runtime configuration asset or `config.json`.

The preview references the site's public logo on its existing Typlog image host.
Article bodies and optional collection samples are explicitly local fixtures.
The port does not include Sanity, Clerk, analytics, billing, subscriber exports,
API credentials, or private content.

Platform icons, including WeChat, are from Simple Icons (CC0 1.0), revision
`b054428646591252023b9599defb56f6e0b32f10`:
https://github.com/simple-icons/simple-icons
https://creativecommons.org/publicdomain/zero/1.0/
Brand names and marks remain the property of their respective owners.
The original design source is https://github.com/CaliCastle/cali.so.

The halftone portrait enhancement follows the original MIT-licensed portrait
rendering approach. It processes the site's own public image in the visitor's
browser, with an ordinary image fallback.

The compact project rows in `src/theme.css` are adapted from the same upstream
MIT source. Project names and store links were supplied by the site owner. The
Shigu icon references its public Chrome Web Store image. The hero portrait,
DockPic icon, portus icon, support QR and backup WeChat QR were supplied by the
site owner for publication in this theme. EXIF and text metadata were removed;
pixel data and color profiles were preserved. Product marks remain the
property of their owners. No original-author project catalog is included.

## Owner-selected books and records

The owner selected the following public catalog pages. Their cover images are
bundled for these collection displays, with attribution and outbound catalog
links. Artwork remains the property of its respective rights holders and is not
covered by the theme source code MIT license. No audio or book text is included.

- [After Hours](https://music.apple.com/cn/album/after-hours/1499378108) — record-1499378108.jpg
- [Ah Yeah](https://music.apple.com/cn/album/ah-yeah/982223883) — record-982223883.jpg
- [Full Moon - EP](https://music.apple.com/cn/album/full-moon-ep/1305881083) — record-1305881083.jpg
- [HEART MAID](https://music.apple.com/cn/album/heart-maid/1848070290) — record-1848070290.jpg
- [Starboy](https://music.apple.com/cn/album/starboy/1440871397) — record-1440871397.jpg
- [WE](https://music.apple.com/cn/album/we/1463174475) — record-1463174475.jpg
- [Street](https://music.apple.com/cn/album/street/1118367147) — record-1118367147.jpg
- [范特西](https://music.apple.com/cn/album/%E8%8C%83%E7%89%B9%E8%A5%BF/535739206) — record-535739206.jpg
- [Inner Child](https://music.apple.com/cn/album/inner-child/1444166430) — record-1444166430.jpg
- [我肯定在几百年前就说过爱你](https://music.apple.com/cn/album/%E6%88%91%E8%82%AF%E5%AE%9A%E5%9C%A8%E5%B9%BE%E7%99%BE%E5%B9%B4%E5%89%8D%E5%B0%B1%E8%AA%AA%E9%81%8E%E6%84%9B%E4%BD%A0/1546062804) — record-1546062804.jpg
- [新的心跳](https://music.apple.com/cn/album/%E6%96%B0%E7%9A%84%E5%BF%83%E8%B7%B3/1053567923) — record-1053567923.jpg
- [Wild Thing](https://book.douban.com/subject/37071291/) — book-37071291.jpg
- [清代地方政府](https://book.douban.com/subject/35713871/) — book-35713871.jpg
- [互联网思想十讲](https://book.douban.com/subject/26253507/) — book-26253507.jpg
- [资治通鉴](https://book.douban.com/subject/6790302/) — book-6790302.jpg
- [中国的奋斗](https://book.douban.com/subject/36526876/) — book-36526876.jpg
- [醉古堂剑扫](https://book.douban.com/subject/1105448/) — book-1105448.jpg
- [孙犁全集（1-11卷）](https://book.douban.com/subject/1084028/) — book-1084028.jpg

The owner supplied `hero-portrait-dark.png` for the dark-mode portrait.
The packaged PNG has no EXIF or text metadata. Image pixels are unchanged. Separate
light/dark tone mapping follows the original halftone portrait component.
