# Question film · omnigami

Your users’ questions fill the screen, then fold up over your product’s real answers.

A 30-second tall film for products you ask things of. Each question fills the screen in your own input’s style, big and flush left. Sent, it folds up into a headline band as your product’s real answer rises under it, so every answer shows the question it answers. A real button in an answer grows into the next request, and the last band closes back into your own input, where your line is typed before your logo. Style inspired by Spotify’s video; an independent style study, not affiliated with or endorsed by Spotify.

Watch it play live, and change its words, at [omnigami.ai/skills/question-film](https://omnigami.ai/skills/question-film).

## Install

In Claude Code:

```
/plugin marketplace add omnigami-ai/skills
/plugin install omnigami-question-film@omnigami
```

With the skills CLI, for Claude Code and other agents that read SKILL.md:

```bash
npx skills add omnigami-ai/question-film
```

Or copy `skills/question-film/` into your agent's skills folder (for Claude Code, `~/.claude/skills/question-film/`). Then ask:

```
Make a question film for https://your-product.com
```

## What it runs

The skill works on your computer. It runs the Node scripts in `skills/question-film/scripts/`: they open your product's pages in a local headless browser to capture its real screens, then render the film with that browser and ffmpeg, writing MP4s and an editable HTML film to your project. It sends nothing to omnigami or anyone else, and uses no network beyond loading your own product's pages and the fonts and assets in this folder.

## You need

- Claude Code with Opus 5.5
- Node 20 or later
- ffmpeg
- Chrome, Chromium, Edge or Brave

None beyond your Claude plan’s usage. Node, ffmpeg and the browser are free.

## Licence

Free to use. Use the films and anything else the skill makes for anything, commercial work included. Don't redistribute the skill. See [LICENSE.md](LICENSE.md). The bundled fonts keep their own licence (SIL Open Font License, beside them in `reference/assets/fonts/`).

## Credits

Style inspired by Spotify’s video “Now you can talk to Spotify” (2026) (https://www.youtube.com/shorts/Qf-iBP8X7pI); Spotify didn’t make or endorse this skill. Its example shows Ostlery, a fictional company made for omnigami’s examples, with sample data.

omnigami is not affiliated with Anthropic. More skills at [omnigami.ai](https://omnigami.ai).
