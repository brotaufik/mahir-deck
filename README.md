# AI Nation 2030 · MAHIR

NICTSeD 2026 CyberSAFE® Challenge Trophy, Grand Final deck.
SMK St Bernadette's Convent, Perak Darul Ridzuan · AEB2064

Live: https://brotaufik.github.io/mahir-deck/
Portal: https://brotaufik.github.io/mahir-portal/

## The framework

**MAHIR** is the plain-language name we propose for the *Trust via Responsible Governance*
pillar of the National AI Action Plan 2026-2030, which today is four enablers called E11 to E14.

| | Rule | Already in the plan as |
|---|---|---|
| **M** | Manage AI Responsibly | E13 National AI Classification |
| **A** | Accountability | E14 AI-Aware Stewardship |
| **H** | Human in Command | E11 Holistic and Sectoral AI Governance |
| **I** | Integrity | E12 AI Trust Function |
| **R** | Respecting Human Dignity | The Vision, an AI Nation for the Rakyat |

*Mahir* is the Malay word for skilled.

## Driving the deck

30 slides, 9 acts. Slides 22 to 30 are a hidden evidence bank for Q&A.

- **Tap anywhere** on the stage to go forward. The left edge strip goes back, the right edge goes forward.
- Tapping a card, a chart bar or a timeline stop opens its detail instead of advancing.
- Arrows, space, PageUp/PageDown and a presenter clicker all work.
- `H` home · `/` search · `S` side panel · `N` notes · `T` timer · `Q` evidence bank · `D` dark or light · `F` fullscreen · `Esc` close

`?hub=1` shows a PORTAL button. Inside the portal iframe the deck hides its own side panel,
so only the portal's panel is visible.

## Notes for whoever edits this next

- **Everything is one file.** `index.html`, no build step, no backend, works offline.
- **Motion is CSS and SVG, never video.** Slides 1 and 3 had MP4 and WebM backdrops. On the
  presenter's own machine they decoded to a still poster, so they were rebuilt as CSS animation:
  nothing to decode, no autoplay policy to fight, and vector sharp on any projector.
  `media/` still holds the retired video files as source material. Nothing references them.
- **`#frame` must keep `flex:0 0 auto`.** `#stage` is a flex container, so without it the 1600x900
  design canvas gets shrunk to the stage width and then scaled again, and every slide reflows
  differently on every screen.
- **Never `display:none` the side panel.** `#app` is a two-column grid; removing `#sb` moves
  `#main` into the 0-width first column and the stage collapses. Hide it with `visibility:hidden;width:0`.
- **The search index is generated.** Edit slide text, then run `rebuild_index.py` or search will
  return stale wording.
- The old `maruah-deck` URL is a hash-preserving redirect stub. Do not push a deck over it.
