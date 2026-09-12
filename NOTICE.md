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
