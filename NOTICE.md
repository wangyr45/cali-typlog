# Source and attribution

This port targets the current design of [cali.so](https://cali.so/), using
Cali Castle's `upstream/dev` revision `a35dcf2` (September 2026).
The original source is licensed under MIT. The full copyright and license text
is preserved in `LICENSE` and included in the distribution.

`src/reference.css` retains the original section labels, compact article rows,
print stacks, polaroid frames, navigation cards, and dock styles. Typlog templates,
collection controls, and platform integration are implemented for this port.

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
Shigu icon references its public Chrome Web Store image. DockPic and portus use
text initials until the owner supplies public icons. Product marks remain the
property of their owners. No original-author project catalog is included.
