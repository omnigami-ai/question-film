---
name: question-film
description: Make a 30-second tall (9:16) film of a product that answers requests, in code, in the grammar of Spotify's "Now you can talk to Spotify" ad (an independent style study) - the user's questions fill the screen in the product's own input-field style, each one folds up into a headline band as the product's real answer rises under it, the next question drops down over the answer, a real button in an answer opens into the next request, and the film closes into the product's own input with its line typed in and the mark and wordmark lockup. Renders a tall MP4 with music. Use when the user asks for a question film, a vertical or tall app ad, a Reel/TikTok/Shorts ad for an assistant, search, chat or booking product, or a Spotify-style "talk to it" film of their product.
---

# Question film

A 30-second tall film for a product you ask things of. The whole frame is the product's input field. The user's
question fills it, big and flush left, with the field's send button in its corner. Sent, the question folds up into a
headline band at the top and the product's real answer rises under it, so every answer is shown with the question it
answers. The next question drops down over the answer as a new band. A real button in an answer ("Book it") grows into
the next request. The last band closes back into the product's own input, its line is typed in, and the film ends on
the lockup. Flat colour fields, one heavy sans, real screens. 30 fps on a 132 BPM grid, tall (1080 × 1920) only.

You work by **adapting a finished film**. `reference/` is the complete film for Ostlery (a fictional stay-booking
assistant made for omnigami's examples; its story is in `reference/STORY.md`). Keep its machinery: the easing, the
timeline, the type rules, the fold, the reopen, the button opening, the close and the film's own checks. Its nouns
become the user's: the input, the questions, the answers, the button, the colours, the fonts, the line, the mark and
the wordmark. Every setting you change is labelled ADAPT in `reference/index.html`; everything labelled KEEP stays.

Read `style.md` before you plan and `critique.md` before you judge anything.

## What it needs

- **The product itself**, running: its app, a demo or its source you can serve. Every screen in the film is a capture
  of the real product with sample data, never a screen drawn for the film.
- **Its input field**: the field the user types a request into, with its own send button (a composer, a search box
  with a go button, a prompt box). The film opens on the page that holds it and closes back into it.
- **Three answers it really gives**, each a part of a real screen: a first answer to a long request (a result list, a
  search with its matches), a second that picks or explains (one result with the product's reply), and a third that
  follows **a real button in the second answer** (a confirmation, a booked or sent state). A fourth answer, to a short
  practical question, ends the story (directions, a detail, a next step).
- **The words**: the hook typed into the input (the product's own prompt, about four words, its name in it), three
  requests a real user would type, the button's own label, and the product's line (three to six words).
- **Its brand**: the mark as an SVG, the wordmark (its face, weight and tracking, or an outlined SVG), the interface
  face (files with their licences), the brand colour, the ink, the ground, a quiet fill and a success colour.

Read the site and the app before asking; then ask once, in one message, for what they can't answer. If the user wants
no questions or an unattended run, decide from what you can reach and say what you decided.

## Set up

Check Node 20+, ffmpeg and a Chrome-family browser (`scripts/chrome.mjs` finds it; `CHROME_PATH` overrides). Explain
anything missing and stop. Work in `question-film/` in the current directory; set `SKILL_DIR` to this file's folder
first:

```bash
SKILL_DIR=/path/to/question-film   # the folder this SKILL.md is in
mkdir question-film && cd question-film
cp -R "$SKILL_DIR/reference" reference && cp -R "$SKILL_DIR/reference" film && cp -R "$SKILL_DIR/scripts" scripts && cp -R "$SKILL_DIR/music" music
rm -rf reference/out film/out film/STORY.md
npm init -y >/dev/null && npm i -D puppeteer-core
node scripts/render.mjs reference --size 9:16 --times key --sheet --out out/reference
```

The film is tall only: pass `--size 9:16` to every `render.mjs` command (it defaults to 16:9). `reference/` stays
untouched, to compare against. You edit `film/`: its `index.html` and its `assets/` (the product's captures in
`assets/screens/`, its photographs or media in `assets/stays/` if its answers show any, its mark, its fonts beside
their licences; delete the reference's once yours load). Your `STORY.md` and `PRODUCT.md` go at the top of
`question-film/`. Look at `out/reference/9x16-sheet.png` now: that is the bar.

## 1. Read the product

1. `node scripts/capture.mjs <url> capture` and read every screenshot and `capture/brand.json`. Then open the product
   itself and use it: type a request into its input, follow the answer, press the button the answer offers. A local
   app: serve it (`python3 -m http.server`) and use its address.
2. Write `PRODUCT.md`: what it does in one sentence, its voice, its fonts and licences, its line, its input field (fill,
   corner radius, hairline, placeholder, send button: colour, shape, icon, its idle and ready states), the answers you
   found and the button in the second one, and its colours by role (the film's tokens, `C`):
   - `paper` the app's ground, `card` the input's fill, `ink` its text, `soft` its placeholder grey, `line` the input's
     hairline;
   - `ember` the brand colour and `ember2` that colour pressed (the names are the reference's; keep the role names);
   - `sand` a quiet fill the app uses (an idle button, a muted panel), `rule` a light pressed shade;
   - `ok` its success colour (the field the button opens into: the button's result).
   Each with where you found it, and the date.

## 2. The story and the words

The story is four requests and their answers, in the order someone really uses the product:

| Request | Field | What it is |
|---|---|---|
| The hook (`HOOK_TEXT`, `HOOK.text`) | the ground, ink type, the name in the brand colour | the product's own prompt, typed into its input: "Tell Ostlery the trip." |
| 1 (`q1`) | the brand colour, ground-coloured type | the long first request, the way a user would type it: "A weekend lake cabin, with our dog, on a budget" |
| 2 (`q2`) | ink, ground-coloured type | a short follow-up that asks it to choose or explain: "Which one's best?" |
| 3 (`Q3_TEXT`) | the success colour | the real button in answer 2, by its own label: "Book it" |
| 4 (`q4`) | the quiet fill, ink type, one word in the brand colour | a short practical question: "How do we get *in?*" |
| The line (`LINE_TEXT`) | typed into the real input at the end | the product's line: "Plan a stay in a sentence." |

- **Requests are the user's words, in the user's voice**: plain, specific, the way someone types to the product. The
  answers are the product's real screens with its sample data; the film never sets a result, price or name from the
  sample data as a statement.
- **Lengths** (the film's checks fail beyond them): request 1 six to ten words (up to 64 characters), set in up to five
  lines; requests 2 and 4 two to four words (up to 32 characters), in two or three lines; the button's label one or
  two short words; the hook about four words (up to about 26 characters, typed at 0.045 s a letter before the box
  opens at 3.18 s); the line up to about 26 characters (typed at 0.04 s a letter, done before the press at 27.17 s).
  Each request also folds into a headline of at most two lines at 85–120 px.
- **Break the lines by hand** with ` / ` ("A weekend / lake cabin, / with our / dog, on a / budget"), so each line is a
  phrase and the fold keeps reading order: a word may only travel to its own line or a line above, never past a word
  that stays. The film's check ("no word passes through another") fails a break that makes words cross in the fold;
  re-break the request, never the check.
- One word of request 4 may be marked `*like this*` to set in the brand colour (the reference marks "in?"). The hook's
  key word (the product's name) is marked the same way in `HOOK.text`.

Write `STORY.md` in the shape of `reference/STORY.md`: the TL;DR, what each beat says, the beat sheet with your input,
answers, button and fields, and every word with its source. Show the user the requests, the answers you'll capture and
the button in a few lines and ask for one review, unless they asked for an unattended run. Never take silence as
approval.

## 3. Capture the real screens

Write a plan for `scripts/screens.mjs` (the format is at the top of the script) at a 390 × 844 phone viewport, and run
it into `film/assets/screens/` (`node scripts/screens.mjs plan.json film/assets/screens`). The film draws captures by
name from `screens.json`, so keep the reference's names:

| Name | What | Steps |
|---|---|---|
| `home` | the page that holds the input, whole viewport, scale 3 | `capture` with `full` |
| `composer` | the empty input, scale 4 | `capture` `around` the input |
| `ask-01` … `ask-NN` | the hook typed a letter at a time | `type` into the input with `capture: "ask"`, `around` the input |
| `line-01` … `line-NN` | the line typed the same way | `type` with `capture: "line"` |
| `search` | answer 1's lead panel (the reference: the search card) | `capture` `around` it after sending request 1 |
| `a2` | answer 2: the chosen result, the reply and its buttons, as one panel | `capture` `around` the response |
| `a3` | answer 3: the state the button leads to (Booked, its card) | press the button, then `capture` |
| `trip-info` | answer 4's panel (the reference: the trip page's Drive and Getting in rows) | `capture` `around` it |

Record the input's rect (`rects`) so `COMP`, `TXT` and `SEND` match it: `COMP` is the input's box in CSS px (x, y, w,
h, its radius), `TXT` its text's left inset, size and first baseline, `SEND` the send button's centre and radius
inside it. Before capturing, check its labels sit centred: `node scripts/centring.mjs plan.json`, and report what it
lists. Answers that show photographs (the reference's six stays, the cabin and its room) use the product's own images
in `assets/stays/` (`STAYS`, `FOCUS`); an answer without photographs rises as captured panels only.

## 4. Adapt `film/index.html`

- **Tokens and faces** (`C`, `SANS`, `SERIF`): the brand's colours by role (step 1). `SANS` is the interface face, set
  at 880 for every request and headline: a variable face with a heavy end (the reference's Figtree runs 300–900);
  a face without one: its heaviest weight, and say so. `SERIF` is the wordmark's face. Load both in `prepare()`.
- **The mark and icons** (`MARK`, `ICON_UP`, `ICON_CHECK`): the SVG's path data copied exactly (scaled into the 100-unit
  box if its viewBox differs); the app's own send and check icons, copied exactly.
- **The requests** (`HOOK`, `REQ`, `defaults()`, `fields`, `Q3_TEXT`): the words from step 2; each request's field,
  type, accent and send-button colours (`bg`, `ink`, `acc`, `btn`, `arrow`, `dark` for its press); `bh`, each band's
  height (the first, two lines, 440; the rest 330).
- **The answers** (`answer1` … `answer4`, `A1` … `A4`, `A2_ROWS`, `A2_PILL`, `A3`, `PILL`): the product's captures, at
  2.6–2.7× their CSS size (a 390 px phone page at the frame's width is 2.77×), centred under the band. Keep how they
  arrive (KEEP): every part rises from below into the space the band leaves, staggered (photos 0.06 s apart, left to
  right and row by row; a response's rows 0.045 s apart), on `EXPO_OUT`, never a fade or a slide from the side
  (answer 2's carousel slides in from the right inside its panel, because the product's carousel scrolls that way).
  Measure the button in the `a2` capture into `A2_PILL` (its CSS rect) and redraw it the app's way in `drawPill`, so it
  can be pressed and grown.
- **Answer 3's state change** (`bookPill`, `T.booked`, `T.done`): the product's own in-progress state, then its done
  state, one label at a time, then the captured done panel. If the product shows no progress state, cut that step and
  rise the done panel on `T.booked`.
- **The lockup** (`LOCK`, `endLock`, `sceneEnd`, `prepare`'s `MW`): keep the proportions (the wordmark's size
  124:98.6 of the mark's drawn height, the gap 26:98.6, the baseline on the mark's foot, the mark a touch above the
  middle: the film checks them). The word, its face and weight are the brand's; **its tracking is the brand's own**
  (the reference sets Ostlery's −0.0174 em, as its other films do: a wordmark set looser than the brand sets it was
  sent back). An outlined wordmark: draw its path instead of `fillText`.
- **KEEP:** the easing curves, `T` (change a time only with its neighbours, `style.md`), `MARGIN`, `TRACK`, `LEAD`,
  `WT`, the layout and its breaks, `foldK`, `flipWord`, `riseWord`, the fold, the reopen, the button opening, the iris,
  the close, the cues and `selfChecks`.

### The rules the founder set for the fold (all KEEP; the film's checks hold the first four)

1. **The words slide across first and rise only as the band comes up.** `foldK`: across (with the size) from the press
   over 70% of the move; the rise waits 0.3 s, until the band has come up close under the words, then lands with it.
2. **One shared scale.** Every word of a request on one progress, one curve, one start: no per-word or per-line stagger
   in the fold, so all words are the same size on every frame.
3. **No word passes through another**, in any fold, in the hook's row-to-column move or in the button's opening.
4. **Enough leading that descenders clear** the line below (`LEAD = 0.98`; the check measures the ink).
5. **Answers rise from below, staggered**, into the space the band leaves; never cross-fade.
6. **The first request rises inside the swelling send-button disc**, so the opening disc pulls the words in (they start
   0.2 s into the iris).
7. **The composer close shows no placeholder**: the closing band becomes the empty input with only its idle send
   button; the line is then typed into it.
8. **The wordmark's tracking is the brand's.**

## 5. Check, critique, revise

1. `node scripts/render.mjs film --size 9:16 --check`: frames match when rendered twice in different orders, and the
   film's own checks pass (it prints each failure with its numbers, and the count when all pass): the lockup's
   proportions and padding, every request and headline inside its margins and band, every word inside the frame on
   every fold frame, no word passing through another, the leading, and the first request starting inside the opening
   disc. Fix every failure in the film, never in the check; if you replace a step, change its check to match.
2. `node scripts/render.mjs film --size 9:16 --stress` (the words at their longest and shortest), `--times key --sheet
   --out out/round<N>`, `--phone`, and `--review` (strips around every cut and key time). Lay your sheet beside the
   reference's (`node scripts/compare.mjs reference film out/round<N>/compare.png`) and look at the images.
3. Score every still and strip on `critique.md`. Get a fresh judgement if your agent can start a sub-agent without this
   session's memory: give it only `critique.md`, `style.md` and the round's images beside the reference's; merge what it
   finds. Otherwise reread `critique.md` and score from the images alone, as a stranger would.
4. Fix, and keep notes in `out/round<N>/NOTES.md`. Stop when every line scores 8 or more; after three rounds, show the
   user what remains.

## 6. Render

```bash
node scripts/render.mjs film --size 9:16 --video --sound --audio music/song.mp3 --stems music/song-stems --bpm 132 --land 27.27 --poster 29 --out out
```

This writes `out/9x16.mp4` (30 fps, no motion blur, as the reference), its poster on the lockup, and the soundtrack:
the skill's song (`music/song.mp3`, 132 BPM, the film's grid) from its first downbeat, its last hit landing on
`--land` (`T.endTurn`, 27.27 s: the composer turns away and the mark turns in), where its drums stop and the rest
closes and fades (from its stems), with the kit's quiet effects on the film's cues under it (ticks on keys, taps on
presses, soft swishes on the big moves, one pop on the done state). If you move `T.endTurn`, move `--land` to match.
`--music` instead of `--audio … --land …` gives the synthesised score; the user's own song works with
`--audio their-song.wav --land 27.27` (without `--bpm 132`). Run it in the foreground and wait for it. Then
`node scripts/motion.mjs out/9x16.mp4 <from> <to>` over each fold (press to press + 1.8 s), each reopen, the button
opening and the close; `critique.md` lists the flags the machinery raises by design.

## 7. Deliver

Run `node scripts/preview.mjs film` and give the address it prints: it plays the film and edits the requests (a saved
edit needs a new render to reach the MP4). Write `README.md` (the files, how to preview, how to change a request, how
to render), `out/CAPTION.md` (a post under 280 characters in the product's words, with its URL) and `out/REVIEW.md` (the
scores, round by round). Hand over the MP4, the poster, the caption, the check results and the one change that would
most improve the film.

## Hard rules

- **Only the user's product.** Its real input, its real answers captured from the running product, its real button,
  its mark exactly, its words, its colours, its fonts with licences. No screen drawn for the film; sample data stays
  inside the screens.
- **Nothing from the inspiring film:** none of its footage, frames, words, logo, colours, music or app. Its grammar only.
- `seek(t, values)` paints from its arguments only: no clocks, unseeded randomness, timers or network; CPU-backed
  canvases (`willReadFrequently: true`), `ctx.reset()` every frame. Every file the film loads lives inside `film/`.

## Files

- `reference/`: the Ostlery film (`index.html`), its story (`STORY.md`), its captures (`assets/screens/`, from
  Ostlery's working app), its stays' photographs (`assets/stays/`), its mark (`assets/mark.svg`), its fonts (Figtree
  and Newsreader, SIL Open Font License, `assets/fonts/`) and `kit.js`. To watch it with its song:
  `node scripts/render.mjs reference --size 9:16 --video --sound --audio music/song.mp3 --stems music/song-stems --bpm 132
  --land 27.27 --out out/reference`. Ostlery is a fictional company made for omnigami's examples.
- `style.md`: the grammar, with numbers. `critique.md`: the review, every rule with how to check it.
- `music/`: the skill's song and its stems.
- `scripts/`: `render.mjs` (stills, strips, the quick test, checks, MP4s), `compare.mjs`, `motion.mjs`, `screens.mjs`
  (the product's real screens), `capture.mjs` (brand from a URL), `centring.mjs`, `preview.mjs`, `music.mjs`,
  `song.mjs`, `sfx.mjs` and `chrome.mjs`.

Style inspired by Spotify's video ["Now you can talk to Spotify"](https://www.youtube.com/shorts/Qf-iBP8X7pI) (2026):
an independent style study, not affiliated with or endorsed by Spotify, and none of its assets.

This skill is omnigami's (https://omnigami.ai), © 2026 Auberon LLC. Use what it makes for anything,
commercial work included, and change the skill for your own use; don't redistribute or
sell the skill. Full terms: https://github.com/omnigami-ai/skills/blob/main/LICENSE.md
