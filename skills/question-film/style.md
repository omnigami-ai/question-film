# Question film: style

A tall app film in the grammar of Spotify's video "Now you can talk to Spotify" (2026): an independent style study,
not affiliated with or endorsed by Spotify, and none of its assets. Grammar only: never its footage, words, logo,
colours, music or app. Every screen, word, colour and face is the user's. Every number here is read from
`reference/index.html`.

**What we take from it:** the request as the poster (huge, heavy, flush-left type filling a flat colour field);
type that grows in weight as it arrives; the app's own control growing into the next scene; answers that rise in at
speed and settle on a long tail; lines entering from opposing sides; a picture turning in from edge-on; extreme
ease-in-out on moves from rest. **What we don't:** its story, its app, its palette, its typeface, its music and its
characters. Ours is built on one device that travels to any product that answers requests: the question folds up
into a headline band and stays on screen above the real answer, so every answer frame shows what was asked.

## Format

| | |
|---|---|
| Frame | 1080 × 1920, 30 fps (900 frames), no motion blur. Tall only (`--size 9:16`). |
| Length | 30.0 s = 66 beats = 16½ bars: the opening 0–4.6, four requests and answers 4.66–25.0, the close 25.0–30.0. |
| Grid | 132 BPM: a beat 0.4545 s, a bar 1.818 s. Every press and every band lands on a beat (`b(n)`). The song's last hit lands at 27.27 s (beat 60), as the composer turns away for the mark. |
| Sound | The skill's song (`music/`) with the kit's effects 6 dB under it: ticks on keys (gain 0.32), taps on presses (0.55–0.6), soft swishes on the first visible frame of each big move (0.2–0.26), one pop on the done state (0.36). |
| Look | Flat fields in four of the brand's colours; heavy flush-left type; the product's real screens as panels with one soft contact shadow; the brand's mark and wordmark at the end. No gradients, no blur, no texture. |

## Colours by role (the reference's tokens, `C`)

| Role | Token | Ostlery | Where |
|---|---|---|---|
| Ground | `paper` | #F7F4EE linen | the page, the hook's field, every answer's ground, the lockup |
| Quiet fill | `sand` | #EFEAE1 | request 4's field; the composer's idle send button |
| The input | `card` | #FFFFFF | the composer (the field the close lands in) |
| Ink | `ink` | #17191F | request 2's field; every dark word; the opening's ground behind the rising page |
| Placeholder | `soft` | #80858E | the idle send button's arrow |
| Hairline | `line` | #E3DDD2 | the composer's 1 css px edge |
| Light pressed | `rule` | #D6CFC2 | a light send button at its press |
| Brand colour | `ember` | #C2482B | request 1's field; the hook's key word; request 4's key word; the send button on light and ink fields; the mark |
| Brand pressed | `ember2` | #A93B20 | the brand-colour send button at its press |
| Success | `ok` | #2E7A57 | the field the answer's button opens into (Book it) |

| Request | Field | Words | Key word | Send button (press) |
|---|---|---|---|---|
| Hook | paper | ink | ember | ember, white arrow |
| 1 | ember | paper | — | paper, ember arrow (rule) |
| 2 | ink | paper | — | ember, white arrow (ember2) |
| 3 (the button) | ok | paper | — | paper, ok arrow (rule) |
| 4 | sand | ink | ember | ember, white arrow (ember2) |

Four fields, each a colour the brand already uses for that meaning: its colour for the first ask, its ink for the
follow-up, its success colour for the action's result, its quiet fill for the last, practical question.

## Type

| Words | Face (Ostlery) | Size | Setting |
|---|---|---|---|
| Every request and headline | Figtree 880 (the interface face) | fitted to the 952 px measure, at most `max` | tracking −0.035 em, leading 0.98, flush left at x 64, the first line's capitals from y 134 |
| The hook | Figtree 880 | up to 420 (Ostlery: 286 px, "Ostlery" filling the measure, four lines) | its key word in the brand colour |
| Request 1 | Figtree 880 | up to 400 (192.8 px, five lines) | as broken by hand (` / `) |
| Request 2 | Figtree 880 | up to 400 (336.9 px, three lines) | |
| The button's request | Figtree 880 | up to 400 (311.5 px, one line) | its capitals centred on the frame's middle line |
| Request 4 | Figtree 880 | up to 330 (281.1 px, three lines) | its key word in the brand colour |
| A headline (the band) | Figtree 880 | up to 120, two lines at most, rebroken for width (85.1 px for request 1; 117.5–120 for the rest) | centred in the band at `bh` / 2 + 8 |
| A rising request word | Figtree 360 → 880 | its line's size | rises one em from below its baseline, clipped to its line's slot |
| The composer's text | Figtree 400 (the app's) | 18 css px × 2.77 | the captures; the opening's words travel from here into the hook |
| The answer's button | Figtree 600 (the app's) | 15 css px × 2.62 | white, centred on its capitals |
| The wordmark | Newsreader 600 (the brand's) | 124:98.6 of the mark's drawn height (201 px for a 160 px mark) | the brand's own tracking (−0.0174 em), ink |

Sizes are set by the widest line: a layout breaks into more lines only when that buys 15% more size, never below
40 px, and always above the send button with a quarter of the size to spare. Every label in a button is centred on its
capitals (`kit.centreText`), never on its em box.

## Sizes

- **The send button, full frame:** a disc of radius 90 with its centre 154 px in from the right and bottom edges
  (926, 1766); the app's arrow at 1.1× the radius, stroke 0.11× the radius.
- **The band:** the full width, its foot rounded r 56, its top beyond the frame; `bh` 440 for a two-line headline, 330
  for one; a soft shadow (rgba(23,25,31,0.17), blur 36, y 13) while it settles.
- **The answers:** the product's captures at 2.6–2.7× their CSS size (a 390 px phone page at the frame's width is
  2.77×), on panels of the ground with a radius of 16–20 css px × the scale and one contact shadow (rgba(23,25,31,0.28),
  blur 60, y 22). Photographs fill the margins (952 px wide) at radius 32, or a 3 × 2 grid with 18 px gutters.
- **The composer:** the capture at 2.77× (969 × 727 px), centred; its corner 28 css px.
- **The lockup:** the mark 160 px tall; the wordmark's size 1.258× that, the gap 0.264× (42 px); the wordmark's
  baseline on the mark's foot; the whole centred across the frame, the mark's top 0.58 of its height above the middle.

## The timeline (s, `T`; beats in brackets)

| Time | Event | Ease |
|---|---|---|
| 0.12 | The product's page (the `home` capture) rises from below as a sheet over the ink, 0.62 s; its top corners (r 56) square off in the second half | out5; `DRAW` |
| 1.36 [3] | All but the input fades into the ground (0.44 s); from 1.40 the input glides to the frame's centre (0.62 s) | `DRAW`; `MOVE` |
| 1.82 [4] | The hook is typed into the real input, a capture per key, 0.045 s a letter, a steady caret; the send button lights (0.16 s) | |
| 3.18 [7] | The input opens into the whole frame (white to the ground, its hairline fading), 0.655 s; the typed words drop to their own lines first (0.46 s), then slide home as they grow from 0.2 s (0.46 s), weight 400 → 880, the key word turning to the brand colour; the send button travels to the corner (0.84 s) | `EXPO_IO` |
| 4.66 [10.25] | The send button swells into request 1's field: its radius 90 → 2080 in log space on a cosine (0.62 s, at most 1.3× a frame); its arrow fades in the first 45%; the words rise inside the disc from 4.86, 0.055 s apart, 0.62 s each; the new send button grows in at 5.24 (0.5 s) | cosine in log space; `EXPO_OUT` |
| 7.84 [17.25] | The press: the send sinks to 0.9 and shades in 0.07 s, returns over 0.24 s | out3; settle |
| 7.94 | The fold: the band's foot lifts from below the frame to `bh` (`EXPO_IO`, 0.61 s from 8.11); the words slide across with their size (0.385 s from 7.94), then rise from 8.24 (0.48 s), landing with the band; the send button rides the band's foot and is gone by 42% of the lift | `EXPO_IO` |
| 8.06 → | The answer rises from below into the space the band leaves: its lead panel 620 px up (0.72 s from 8.30); the six photographs from below the frame, 0.06 s apart, left to right and row by row (0.7 s each from 8.36) | `EXPO_OUT` |
| 10.68 [23.5] | The reopen: request 2's band drops from the top, its rounded foot leading, to the frame's foot (0.78 s; the radius squares off in the last 40%); the answer under it shrinks to 0.94 about (540, 1190), sinks 60 px and darkens 24%; the words rise from 10.84, 0.06 s apart; the send button grows in at 11.36 | `EXPO_OUT` |
| 12.27 [27] | Press; 12.37 fold into the ink band; answer 2's panel rises 760 px (0.76 s from 12.73), its carousel slides in 520 px from the right inside it (0.8 s from 12.79), its rows rise 46 px, 0.045 s apart, from 12.85 | `EXPO_IO`; `EXPO_OUT` |
| 15.00 [33] | The answer's button dips (to 0.9, 0.08 s, a lighter ink); 15.08 its own rect grows to the frame (0.5 s), in the success colour from its first frame, keeping its round ends until past 90% of the frame; its label, centred on its capitals, scales with it into request 3 (600 → 880, white → the ground's colour); the answer behind darkens 22%; nothing under it moves; the send button grows in at 15.52 | out3; `EXPO_IO` |
| 16.82 [37] | Press, and the fold starts on it: the band lifts on its own 0.38 s curve, its foot never above the travelling words, settled by 17.2; the answer is already under it: the photo rises 40 px from 16.90 (0.45 s), the result card three frames later | `EXPO_IO`; `EXPO_OUT` |
| 18.18 [40] | The product's in-progress state turns done: the pill widens and turns from ink to the success colour (0.34 s); "Booking" leaves upward (0.16 s), "Booked" rises in from 18.28 (0.4 s): one label at a time; the captured done state from 18.63 | `MOVE`; `EXPO_IN`; `EXPO_OUT` |
| 18.52 | The reflow: the card grows to its full height and the photo shrinks to make room (0.44 s); "Done" and the trip card rise 34 px from 18.70, 0.08 s apart | `MOVE`; out5 |
| 20.45 [45] | Reopen into request 4: the band drops; its lines enter from opposing sides (even lines from 0.32 of the frame left, odd from 0.75 right), 0.04 s apart, 0.6 s, weight 380 → 880 | `EXPO_OUT` |
| 22.27 [49] | Press; 22.37 fold; the room photograph lifts 300 px (0.86 s from 22.71) as it turns in from edge-on, its angle (88.7° → 0) eased so it settles flat (0.82 s from 22.75); the trip panel rises 560 px (0.76 s from 22.85) | `EXPO_OUT` |
| 25.00 [55] | The close: the band closes down into the input at the centre (0.72 s), its colour turning to the input's white by 60%, its hairline from 40%; its question fades and lifts 30 px; the input's idle send button arrives from 30%, no placeholder; the answer falls away (1500 px, 0.58 s) | `EXPO_IO`; `EXPO_IN` |
| 25.68 [56.5] | The line is typed into the real input, 0.04 s a letter | |
| 27.17 | The send press | out3; settle |
| 27.27 [60] | The song's last hit: the input turns edge-on about the frame's centre (0.17 s, darkening 12%) | ease-in (p^2.2) |
| 27.44 | The mark turns in from edge-on at 300 px and glides into the lockup (0.84 s, its size in log space); the wordmark grows from 0.7 to 1× and fades in only once it is wholly inside the frame | `MOVE` |
| 28.28–30.0 | The lockup holds | |

Change a time only with its neighbours: presses stay on beats with the fold 0.1 s after; each answer holds about
2.6 s or more from its fold to the next move (Ostlery's: 2.74, 2.63, 3.63 and 2.63 s), so it is read; the line's typing
ends at least 0.4 s before its press; the lockup lands on the song's last hit.

## Easing (`KEEP`)

Measured from the inspiring film (entrances arrive at speed and settle on a long tail; exits accelerate into the next
shot; a move out of a hold starts slowly and snaps through its middle):

- `EXPO_IO` = cubic-bezier(0.87, 0, 0.13, 1): every move from rest to rest (the box opening, the fold, the band's lift,
  the button growing into a field, the close).
- `EXPO_OUT` = cubic-bezier(0.16, 1, 0.3, 1): every arrival from off frame or from nothing (answers rising, bands
  dropping in, words rising, lines entering from the sides, the room turning in).
- `EXPO_IN` = cubic-bezier(0.7, 0, 0.84, 0): departures (the answer falling away, a label leaving).
- `MOVE` = cubic-bezier(0.45, 0, 0.15, 1): the input's glide, the reflow, the mark's glide to the lockup.
- `DRAW` = cubic-bezier(0.6, 0, 0.3, 1): fades.
- The iris: (1 − cos πp) / 2 in log space. Zooms run in log space, never linear in scale.
- The fold's words: two progresses on `EXPO_IO`, across (and size) first, the rise 0.3 s later (`foldK`).

## Another product

| Piece | Ostlery | How it's found for any product |
|---|---|---|
| The input | its composer with the send button inside | the product's own field with its own send or go button, captured |
| The hook | "Tell Ostlery the trip." | its own prompt or placeholder idea, about four words, its name as the key word |
| Request 1 | a weekend lake cabin, with the dog, on a budget | the long first ask a real user types |
| Answer 1 | the search card and six stays | its first real answer: results, matches, a draft |
| Request 2 | "Which one's best?" | a short follow-up: choose, explain, compare |
| Answer 2 | Heron Point, the reply and Book it | the chosen result with the product's reply and its action buttons |
| The button | Book it (`.pill.dark`) | a real button in answer 2 (Approve, Send, Pay, Add, Book) |
| Answer 3 | Booking → Booked → Done | the state the button leads to, in-progress then done |
| Request 4 | "How do we get in?" | a short practical question |
| Answer 4 | the room and Getting in | its real answer: a detail page, directions, the next step |
| The line | "Plan a stay in a sentence." | its own line, typed into its own input |
| The lockup | the arches and "ostlery" in Newsreader 600 | its mark (SVG) and wordmark, at the brand's tracking |
