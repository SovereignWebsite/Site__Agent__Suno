# suno.b: the four-hourly wake

Dinis, 25 Nov 2026 in suno.b's session: "can you now do this workflow where every 4 hours you woke up and you create a new song and you publish it?" Credits: no working limit ("the point here is to use all the credits"); stop and tell Dinis if fewer than 100 song credits are left. Downloads and visuals credits: never at a wake ("let's not use those video credits for now").

Dinis, 26 Nov 2026 in the new session: "write a lyric, kind of a funny one and witty lyric about the work that has happened since or in the last 24 hours. Pick multiple examples and then write a song about it and pick styles ... I should be surprised for what you pick, and let's do different styles ... for each style, always do one with the lyrics and one instrumental. So basically, do 4 songs per block of 4 hours." So each wake is a block of four generations (40 song credits): two styles, never used before (styles.md), each once with lyrics and once instrumental. At 240 credits a day the month's credits last about 9 days; Dinis: "Don't worry about the budget".

At each wake, in this order:
1. `git pull` both repositories (Site__Agent__Suno, the agent; Site__Platform__Suno, the work); read this area's now.md and experiments.md (Site__Agent__Suno site/factory/dinis-cruz/account-b/).
2. Suno: account-usage (credits); library-list liked=true (Dinis's likes on this account). Mark each liked take in site/data/songs.json ("liked": true on the take); a liked take is shown first and starts in the board's Liked column.
3. Check every take in songs.json still exists (audio-retrieve); if Dinis deleted one on Suno, remove it from the data and say so.
4. Make the block: a request Dinis left first. Else pick two styles not yet in styles.md (surprising, far apart). Write a witty lyric about the last 24 hours of work (git log of both repositories, now.md, the sessions): several concrete events, no private person named, no invented facts. For each style: one generation in custom mode with the lyric, one instrumental (custom mode, the same style). Publish the takes (audio-settings public); if publishing is refused, say so on the song and to Dinis. Add the styles to styles.md. (The fado-guitar queue, experiments.md, is paused while Dinis wants this.)
5. Ask Suno's listening tool about both takes (lead, groove, melody continuity, mix, sections); record the brief, the exact prompt, the result and each take's analysis in songs.json; set "best" to the better take.
6. In Site__Platform__Suno: site/data/budget.json and docs/spend.md. In this area (Site__Agent__Suno): agent.json (updated), now.md, and mark the experiment done in experiments.md; commit and push both.
7. In Site__Platform__Suno, regenerate: python3 tools/pages.py; run build, share-check, quality, html-validate, axe and signers; commit (signed, trailers) and push to dev.
8. Refresh the two Suno playlists (newest 10 and newest 20, best take per version, newest first, archived left out): remove all, add in order.
9. Report to Dinis in the session: the song, both takes' links, what worked and what did not, credits left.
