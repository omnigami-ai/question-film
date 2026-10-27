# Question film: critique

You judge twice: the key stills and strips, then the rendered MP4. Judge as a stranger seeing it in a feed, sound off
first. Never loosen a check to get a pass; fix the film.

**Look at:** your key sheet beside the reference's (`node scripts/compare.mjs reference film out/compare.png`); the
review strips (`node scripts/render.mjs film --size 9:16 --review`: every other frame around every cut and key time);
12-frame strips (`--strip <t>`) at each moment named below; `node scripts/render.mjs film --size 9:16 --check` (the
film's own checks); `node scripts/motion.mjs out/9x16.mp4 <from> <to>` over each move; the MP4 twice, once for the
picture, once for the sound. Times below are the reference's; find the same moment in your film.

## The film's own checks (`render.mjs film --size 9:16 --check`)

All must pass. Each is one of the founder's rules, measured:

| Check | The rule |
|---|---|
| approved lockup: 124:98.6 type, 26:98.6 gap, baseline on mark foot | The lockup is set as the brand's other films set it: a bold wordmark, a tight gap, on the mark's foot. |
| lockup padded inside the tall frame | The mark and the word stay 70 px or more from the frame's sides. |
| request N: settled words inside the margins, above the send button | Every request sits inside the 64 px margins and clears the send button by a quarter of its size. |
| request N: headline fits its band | Every headline fits its band in two lines or fewer, inside the margins, with the same words as its request. |
| folds: every word inside the frame on every frame | No word is cut by the frame's edge while it travels. |
| no word passes through another (folds, the hook, Book it) | Words never print over each other in a fold, in the hook's row-to-column move or in the button's opening (the founder, 2026-10-26). Fails name the fold, the time and the two words: re-break the request by hand (` / `) so no word must cross another to reach its line. |
| leading: descenders clear the line below | In every request, the hook and every headline, no line's ink (a g, y, p) reaches the capitals of the line below (the founder, 2026-10-26, at 0:06: "g and d" touched). |
| first request starts inside the swelling disc, after it opens | Request 1's words begin rising inside the opening disc, so the disc pulls them in (the founder, 0:06). |

## Each still and strip: 1–10 (8 or more on every line)

1. **It reads as the reference.** The request is the poster: heavy, flush left, filling the measure, on one flat field;
   the answer is the product's real screen under the question's band. A gradient, a texture, a second accent colour,
   a busy frame or type that doesn't fill the frame fails.
2. **Every screen is the product's.** Each answer, the input and the button are captures of the running product with
   its sample data, never a screen drawn for the film, never two of its pieces joined into one it doesn't have.
3. **The question stays.** On every answer frame its question is legible in the band above it, at 85–120 px.
4. **Words placed with care.** Flush left on the margin, broken into phrases, the key word in the brand colour, no
   widow, no word cut by the frame; labels in buttons centred on their capitals.
5. **Fields read as the brand's.** Four flat fields, each a colour the brand uses for that meaning (its colour, its ink,
   its success colour, its quiet fill); the send button stands out on each, and its press is visible.
6. **The lockup** as the brand's other films set it: bold, baseline-aligned, a tight gap, the wordmark at the brand's
   own tracking, in full ink.

## The film: 1–10 (nothing ships under 8)

1. **Story:** a stranger can say, from the MP4, what the product does (they ask, it answers, it acts on a press) and
   its name; every answer is read beside the question it answers.
2. **One connected move per change.** The input opens into the hook; the send button swells into the first request;
   each request folds into its band as its answer rises; each new request drops in over the old answer; the button
   grows into its request; the band closes back into the input. Nothing changes by a cut or a cross-fade between
   fields.
3. **Ease in from rest.** Moves from rest on `EXPO_IO` (a slow start, a snap through the middle, a long settle);
   arrivals on `EXPO_OUT`; departures on `EXPO_IN`. The first frames of each fold, the box opening and the button's
   growth barely move (strip at 3.18, 7.94, 15.08, 25.0).
4. **Breathing room.** Each request held long enough to read (request 1 about 2 s settled, the short ones about
   1 s); each answer held about 2.6 s from its fold; the line read before the press; the lockup held about 1.7 s.
5. **Truth.** Requests are what a real user types; the answers are the product's; nothing from the sample data is set
   as a statement; the mark and icons are exact.
6. **Finish.** No one-frame pops; nothing parked then creeping on; the iris in log space; the song's last hit on the
   composer's turn into the mark; the effects quiet under the song.

## The founder's review of this film (hunt for each in yours)

| Time (reference) | Note | The check |
|---|---|---|
| 3.18–4.0, the hook | "Hook lockup is too tame: use the space and squeeze the characters in" (2026-10-25). | The hook's widest word fills the 952 px measure, heavy (880) and tight (−0.035 em); its block fills most of the frame's height. |
| 4.66–5.9 and every request | "Transitions need amplified motion … the variable font growth should happen in the transition … much more fluid and connected, less rigid" (2026-10-25). | The weight grows during the rise (360 → 880 over the same 0.62 s), never after the words land; each change is one move on the measured curves. |
| 0:06 (4.86–5.6) | The leading was too tight ("g" and "d" touched), and the request should rise inside the swelling send-button disc (2026-10-26). | The leading check passes; on a strip at 4.66–5.3 the words are clipped to the disc and rise as it opens. |
| 0:08 (7.94–8.8), every fold | The fold "feels too disjointed" (2026-10-26). | The words slide across first and rise only as the band comes up close under them, landing together with it (strip at 7.94: the words on their own lines for the first 0.3 s, the band arriving under them). |
| 0:09 (8.3–9.2) | "Let's not use the arched masks for the images" (2026-10-25); then: the photos should pull up from below, staggered, not sweep in from the left (2026-10-26). | Photographs in the product's own corner radius; they rise from below the frame, 0.06 s apart, left to right and row by row. |
| 0:23 (22.75–23.6) | "Make the rotating picture land more smoothly" (2026-10-26). | The turn is eased in its angle, so it settles flat: `motion.mjs` 22.2–23.6 shows the change falling off smoothly, no snap on its last frames. |
| 0:26 (25.0–25.7) | Remove the placeholder text in the input during the close: "there isn't enough time to read it" (2026-10-26). | The closing band becomes the empty input with only its idle send button; the line is typed into it. |
| 0:28, the lockup | The wordmark faded in grey (its fade never reached full strength), and its letters were "a bit too spaced out … match other videos" (2026-10-26). | The wordmark ends in full ink, at the brand's tracking (Ostlery's −0.0174 em, as its Device and Statement films set it). |
| The end lockup | "Thicker" type, "aligned on the baseline" (2026-10-25). | The lockup check passes. |
| Every fold | Approved: "almost perfect" (2026-10-26), then "good to go". | Your film keeps all of the above. |

## Found in review before the founder saw it (hunt for each)

- **Words falling into a staircase at different sizes** in a fold: every word on one progress, one scale.
- **Words passing through each other for 5–8 frames** when every word moved on one curve: across first, then up
  (`foldK`), and the check.
- **The opening's words stepping diagonally** from the input into the hook: they drop to their lines first, then slide
  home as they grow.
- **A black pill covering the reply** when the button was pressed: the button's own rect grows, in the success colour
  from its first frame, and nothing under it moves.
- **A frame with the top half empty** as a band lifted: the answer is in place under the band before it uncovers it
  (answer 3 rises from 16.9 s, under the band).
- **An answer cross-fading in**: answers rise from below, staggered.

## What `motion.mjs` flags by design

The approved reference raises these flags itself (`node scripts/motion.mjs out/9x16.mp4 <from> <to>`); at the same
moments in your film they aren't faults. Check each on a strip all the same; flag anything else.

- **A jump at 1.53 s** (0.90 → 2.67): the page fading as the input starts its glide.
- **A jump at 3.63 s** (5.21 → 15.15): the box opening snapping through the middle of `EXPO_IO`.
- **A stop at 7.93 s, a jump at 8.00 s; a stop at 22.33–22.37 s, a jump at 22.43 s; a jump at 12.43 s:** the press
  (a small dip and return), the held frame, then the fold leaving rest on `EXPO_IO`.
- **A jump at 15.30 s** (4.69 → 11.17): the button's rect growing through the middle of its move.
- **A jump at 16.90 s; stops at 17.90–17.97 and 18.43–18.50 s; a jump at 18.57 s:** the band lifting from the press,
  the in-progress state holding (only its spinner turns), then the reflow.
- **Stops at 25.63–25.70 s:** the input settles, empty, before the typing starts.
- **A stop and a halt at 27.50 s:** the input turned edge-on, the mark starting its turn in from edge-on.

`--stress` also lists notes for the reviewer that are the film's design, not faults: at 5.11 s the hook's words under
request 1's (the disc covering the hook), and at 20.76 s request 4's lines "cut by the edge" (they enter from the
sides).

## General finish rules

- Every press has a press state: the button sinks and shades (a light button darkens, a dark one lightens), then comes
  back, on the beat.
- No one-frame pops at hand-offs: shrink, cover or fade anything that would vanish or appear in a frame.
- Shapes change in one move (a button into a field, a band into the input), never through a chain of shapes.
- Nothing parked: no move that stops, then creeps on.
- Labels in pills and buttons centre on their capitals (`kit.centreText`; `scripts/centring.mjs` on the product).
