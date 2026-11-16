# Danica Green Portfolio: Design System (PD2)

Design system for the portfolio in the `PD2` folder. The colours, fonts and base components are reused from First Portfolio. Everything new  is listed under [Changes in PD2](#changes-in-pd2).

## Site structure

| File | Page | Contents |
| --- | --- | --- |
| `index.html` | Resume | Highlights, featured project link, other technologies, education, volunteer, school activities |
| `yatzy.html` | Yatzy Game | Overview, screenshots, technologies, architecture, REST API, game flow, game design system, challenges |
| `styles.css` | Both | One shared stylesheet |
| `images/` | Yatzy | Game screenshots |

Both pages share the same header, navigation bar and footer. The current page's links are in-page anchors, and the link to the other page is coloured orange (`.site-nav__page`).

## 1. Colours

All colours are CSS custom properties defined on `:root` in `styles.css`.

| Token | Hex | Usage |
| --- | --- | --- |
| `--primary` | `#0B6B4B` | Navigation bar, links, section headings, card left border |
| `--primary-dark` | `#12332A` | Header and footer background, code blocks, nav hover |
| `--accent` | `#F2A541` | Heading underline, badges, tagline, focus outline |
| `--bg` | `#F7FAF8` | Page background |
| `--surface` | `#FFFFFF` | Cards and tables |
| `--text` | `#2B2F2E` | Body text |
| `--muted` | `#5F6B66` | Dates, intro text |
| `--border` | `#D5E3DC` | Card, table and chip borders |
| `--surface-tint` | `#EEF5F1` | Table headers, tag chips, inline code |

## 2. Typography

| Role | Font | Token |
| --- | --- | --- |
| Headings | Inter, Arial, sans-serif | `--font-heading` |
| Body text | Inter, Arial, sans-serif | `--font-body` |
| Dates and notes | Inter, Arial, sans-serif | `--font-dates-notes` |
| Code  | System monospace stack (`ui-monospace`, Consolas, Menlo) | `--font-code` |

Inter weights loaded: 400, 600, 700.

## 3. Components

| Component | Class | Notes |
| --- | --- | --- |
| Card | `.card` | White box, 5 px green left border, 12 px radius |
| Badge | `.badge` | Orange pill, used for status labels such as "In progress" |
| Navigation | `.site-nav` | Green bar, collapses to a column under 700 px |
| Flex grid | `.grid` | Wrapping cards, each at least 280 px wide |
| Stack | `.stack` | Cards in a single column |

## Changes in PD2

### New design tokens
- `--surface-tint` colour and `--font-code` font stack (see above).

### New components

| Component | Class | Purpose |
| --- | --- | --- |
| Featured card | `.card--featured` | Card with an orange left border, used for the Yatzy project |
| Green badge | `.badge--green` | Second badge colour so two badges can sit together |
| Tag chips | `.tags` / `.tag` | Short technology labels |
| Table | `.table` in `.table-wrap` | Technologies and API reference; scrolls sideways on small screens |
| Code | `code`, `pre` | Inline code and dark code blocks |
| Numbered steps | `.steps` | Game turn sequence (a real sequence, so numbering is meaningful) |
| Colour swatches | `.swatches` / `.swatch` | Shows the Yatzy game palette |
| Figure / gallery | `.figure`, `.figure--narrow`, `.gallery` | Captioned screenshots; images keep natural size and never stretch |
| Section intro | `.section-intro` | Short paragraph under a heading, limited to 70 characters wide |
| Skip link | `.skip-link` | Hidden until focused, jumps past navigation |
| Page link | `.site-nav__page` | Orange nav link that goes to the other page instead of a section |
| Back link | `.back-link` | "Back to resume" link at the end of the Yatzy page |

### Accessibility
- Visible `:focus-visible` outline on links.
- Sections use `aria-labelledby`, and the nav has `aria-label`.
- Nav links jump straight to their section (no smooth scrolling), with `scroll-margin-top` so headings are not flush with the window edge.


## 4. Yatzy game design system

The Yatzy game keeps its own palette and fonts (Lagoon, Bone, Pip Red, Brass; Bricolage Grotesque and Atkinson Hyperlegible). It is documented in the Yatzy README and summarized in the portfolio's Yatzy section. Its colours are not mixed into the portfolio tokens above, except as swatches that show the game palette.