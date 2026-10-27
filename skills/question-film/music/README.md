# Music

`song.mp3` is this skill's song: an instrumental in bright, polished electro-pop at 132 BPM, made for this skill by omnigami with AI. `song-stems/` holds its stems (`drums.m4a`, `rest.m4a`), split from it with Demucs.
`node scripts/render.mjs film --size 9:16 --video --sound --audio music/song.mp3 --stems music/song-stems --bpm 132 --land 27.27` fits it to the film (`--bpm 132` is the song's tempo, which the fitter would otherwise misread; drop it for another song; `--land 27.27` is the film's `T.endTurn`, where the composer turns away for the mark: move it with that): the full groove from the first frame, and at the turn the drums land one hit and stop while the rest closes and fades under the lockup. The song is over two minutes long; `--from <seconds>` starts at another section.
Usage terms: see the skill's licence.
