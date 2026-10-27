# Ostlery · Question film, the reference (approved by the founder, 2026-10-26)

Style inspired by Spotify's video "Now you can talk to Spotify" (2026,
https://www.youtube.com/shorts/Qf-iBP8X7pI): an independent style study,
not affiliated with or endorsed by Spotify, and none of its assets.
Ostlery is a fictional company made for omnigami's examples (`ostlery.example`).

**TL;DR.** The whole frame is Ostlery's input box. A traveller asks for a lake cabin, asks which one is best,
taps Book it and asks how to get in. Each request fills the frame flush left; sent, it folds up into a headline
band and Ostlery's real answer rises under it, so every answer shows the question it answers. It ends on the
composer typing "Plan a stay in a sentence." and the approved mark/wordmark lockup.

9:16 only; 1080 × 1920; 30 fps; 132 BPM; 66 beats = 16½ bars = 30.0 s.
Every screen is a capture of Ostlery's working app (`assets/screens/`); the photographs (`assets/stays/`) and the
mark (`assets/mark.svg`) are Ostlery's own.

## The device (and why it travels)

- **Request = the input box, full frame.** Flush left on a 64 px margin, Figtree 880, tracking −0.035 em, leading
  0.98 (descenders clear the line below), the send button (r 90) in the corner where every composer keeps it.
- **Fold.** Sent, the field folds up into a band (rounded foot, r 56) and the request's own words travel into the
  headline as one FLIP: every word from the same start, each from its full-field place and size to its band place and
  size, all at one scale on every frame; line breaks change only because words travel. The words slide across first
  (with the size, expoInOut [.87,0,.13,1] over 0.385 s from the fold) and rise only as the band comes up (the rise
  waits 0.3 s, then lands with the band over 0.48 s), so no word passes through another (the founder, 2026-10-26).
  The real answer rises from below into the space the band leaves, staggered.
- **Reopen.** The next request comes down from the top as a new band, its foot leading, over the answer, which
  falls back and darkens; the new words rise into their lines, weight filling in during the rise.
- **A real control opens into a request.** Book it (the app's `.pill.dark`) dips on the beat (0.08 s), then its rect
  grows to the frame (expoInOut, 0.5 s), green from its first frame, keeping its radius until past 90 % of the frame,
  its label centred on its capitals and scaling with it to the centred request.

Any product that answers a request (search, an assistant, a form, a report) can do this with its own composer,
its own answer screens and its own buttons.

## As built (beats at 132 BPM)

| Time (s) | Beat | Point | Move (reference moment it takes its grammar from) |
|---|---|---|---|
| 0.12–2.81 | 0–6 | The product: a new trip; say the trip. | The New trip page rises, all but the composer fades, the composer glides to centre, "Tell Ostlery the trip." typed (ref 0.0–3.3). |
| 3.18–4.02 | 7–8.8 | "Tell Ostlery the trip." | The composer opens into the whole frame; its four typed words drop to their own lines first, then slide home as they grow (one FLIP, one scale, none crossing another) into the poster, Ostlery turning ember; the send button travels to the corner (ref 3.4–4.5, letters lift out of the input). |
| 4.66–5.95 | 10.25–13 | "A weekend lake cabin, with our dog, on a budget" | The send button swells into the ember field (cosine in log space, ≤1.3× a frame); the request rises word by word inside the swelling disc from 0.2 s into it, weight 360→880 during the rise (ref 5.25–6.2). |
| 7.84 / 7.94–9.4 | 17.25 | Six stays that fit. | Press on the beat; fold into the ember band; the search card rises and the six photos pull up from below, 0.06 s apart, left to right and row by row (ref 7.45 push; 7.6–8.4). |
| 10.68–11.5 | 23.5 | "Which one's best?" | A new ink band drops from the top over the answer (ref 10.15 whip, entrance at speed). |
| 12.27 / 12.37–13.4 | 27 | Heron Point is the best fit, Book it. | Fold into the ink band; the real answer panel rises, its carousel sliding in from the right with the reply and actions as one response (ref 12.35 card slide). |
| 15.00 / 15.08–15.58 | 33 | "Book it" | Book it dips on the beat; its rect grows into the green field, its label centred and growing into the request (one shape, one move); nothing under it moves. |
| 16.82–17.37 | 37 | Booking → Booked → Done. | Fold into the green band from the press (band settled by 17.2 s); the cabin and the booking card are already under it, rising 40 px from 16.9 s, three frames apart; spinner → Booked at 18.18 (one label at a time); at 18.64 Done and the trip card arrive and the page reflows, the photo making room (ref 16.85 cascade). |
| 20.45–21.3 | 45 | "How do we get in?" | A new linen band drops over the answer; the lines enter from opposing sides (ref 19.85). |
| 22.27 / 22.37–23.4 | 49 | The living room; Getting in. | Fold into the linen band; the cabin's living room turns in from edge-on, its angle eased so it settles flat (ref 22.45) and the trip page's Drive / Getting in rows rise. |
| 25.00–25.72 | 55 | Back to the composer. | The band closes down into the composer at the centre; its question fades as it shrinks, the answer falls back and away; the composer arrives empty, no placeholder, only its idle send button. |
| 25.68–27.27 | 56.5–60 | "Plan a stay in a sentence." | Typed into the real composer (a capture per key); press on 27.17. |
| 27.27–30.0 | 60–66 | Ostlery. | The composer turns edge-on, the mark turns in and glides to the approved lockup; the word fades in only once it is wholly inside the frame, in full ink, set at the brand's tracking (−0.0174 em). |

Curves: `EXPO_OUT [.16,1,.3,1]` for arrivals, `EXPO_IO [.87,0,.13,1]` for moves from rest (opening, fold, Book it),
`EXPO_IN [.7,0,.84,0]` for departures, `MOVE [.45,0,.15,1]` for the composer's glide and the close, `DRAW [.6,0,.3,1]`
for fades (`../style.md`).

## Sound

The skill's song (`../music/song.mp3`, 132 BPM) with its stems, `--bpm 132 --land 27.27` (its last hit on the 27.27 s
bar line, with the mark's turn); kit effects on the cues (ticks on keys, taps on presses, soft swishes on the visible
onset of each big move, one pop on Booked), 6 dB under the song.

## Checks

`render.mjs --size 9:16 --check` (determinism, 82 frames in two orders, plus 14 film checks: the lockup geometry,
every request and headline inside its margins and band, every word inside the frame on every fold frame, no word
passing through another in the folds, the hook and Book it, the leading (descenders clear the line below by 12.7 px at
the closest), the first request starting inside the opening disc) and `--stress` (defaults, long and short words) pass.
