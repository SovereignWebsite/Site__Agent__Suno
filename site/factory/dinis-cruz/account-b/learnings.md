# suno.b: learnings

- Suno's official MCP (api.suno.com/mcp) needs no API key: a claude.ai custom connector signed in to suno.com. The developer API is a gated beta.
- Costs, measured on this account: one generation (two takes) is 10 song credits; publishing, listing, reading and the listening tool cost nothing; a full-quality download is 1 download credit (15 a month), so downloads are the scarce part.
- Suno's embed (suno.com/embed/<id>) can be framed by another site; the song page cannot; the MP3 is refused (403). Covers come from cdn1 or cdn2.suno.ai.
- The two takes of a generation share one creation time and one prompt: that is how 30 clips became 2 songs x 15 versions x 2 takes. The honest difference between takes is what Suno made of the prompt, and length.
- Suno reinterprets instruments: Parada asked for cavaquinho and flute and got horns and an accordion-like reed. Next time: variety 0 and high style influence.
- The listening tool (audio-listen) gives bpm, key, lead instruments, sections and stop times as JSON: the source for each song page's timings.
- Test the buttons people press, not a neighbouring one: my "all five" claim on the A/B switch was wrong because I had tested only Compare (round 2).
- Check a decision record myself (operates link, signature, the event itself): one record cited a message id that did not exist; decisions.b corrected it.
- Lyrics can name private people: Strangers in the Loop's are not published.

- See handover.md for the fado and Brazilian-groove lessons (25 Nov): reference mode keeps tempo and feel; strong style names drop the Portuguese guitar; instruments drift, so check every take.
- Blocks (26 Nov): an instrumental can miss its style even when the lyric version hits it (the doo-wop instrumental came back as a modern ballad and a jazz ballad). Check style_match on every take; under 3, make it again with style influence 0.9, variety 0, concrete markers (12/8 triplet piano, I-vi-IV-V) and the wrong styles as negatives.
- Suno's connection has no delete: public or private only; trashing is in the app. Playlists only append, so reordering means emptying and refilling; a trashed song is refused on add, which is how trashed takes are found.
- Blocks (26 Nov, block 4): ask the listening tool whether the whole lyric is sung (complete_song); a short take can cut off the last line.
- Blocks (26 Nov, block 5): when an instrumental prompt keeps missing (Chicago blues came back as smooth jazz, lounge and soul twice), make the instrumental from the sung take instead: simple mode, the sung take as reference, "make an instrumental version ... let the harmonica play the vocal melody". It hit 5 of 5 at the first go. Try that before a third prompt.
- Cite Dinis's words by memo id (dinis.<time>.b), not by an estimated time, and name the id in the commit (Source: ...). From maestro.b, 26 Nov.
- Blocks (26 Nov, block 6): an instrument named in the lyric can enter the arrangement: Ten Credits Gone sings about a harmonica, and both Afrobeat takes brought one in, pushing the horns back. Keep instrument names out of the lyric when they clash with the style.
- Dinis's taste and the listening tool's scores can disagree: he liked the blues take scored 0 of 5 and trashed the one scored 5, and trashed all of block 7's picks (27 Nov). Scores pick a default; his likes and trashes decide.
- Blocks (27 Nov, block 10): long lyrics lose their last line (eight sung takes in a row). Ending on a short shout ([Outro] Hey!) kept both forró takes complete; the fado song without one was cut off again. End every sung lyric on a short shouted or one-word outro.
