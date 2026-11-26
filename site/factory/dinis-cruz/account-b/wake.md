# suno.b: the four-hourly wake

Dinis, 25 Nov 2026 in suno.b's session: "can you now do this workflow where every 4 hours you woke up and you create a new song and you publish it?" Credits: no working limit ("the point here is to use all the credits"); stop and tell Dinis if fewer than 100 song credits are left. Downloads and visuals credits: never at a wake ("let's not use those video credits for now").

At each wake, in this order:
1. `git pull` both repositories (Site__Agent__Suno, the agent; Site__Platform__Suno, the work); read this area's now.md and experiments.md (Site__Agent__Suno site/factory/dinis-cruz/account-b/).
2. Suno: account-usage (credits); library-list liked=true (Dinis's likes on this account). Mark each liked take in site/data/songs.json ("liked": true on the take); a liked take is shown first and starts in the board's Liked column.
3. Check every take in songs.json still exists (audio-retrieve); if Dinis deleted one on Suno, remove it from the data and say so.
4. Make the next song: a request Dinis left first, else the next line of docs/experiments.md. One generation (two takes), custom mode, the series rules at the top of experiments.md. Publish both takes (audio-settings public).
5. Ask Suno's listening tool about both takes (lead, groove, melody continuity, mix, sections); record the brief, the exact prompt, the result and each take's analysis in songs.json; set "best" to the better take.
6. In Site__Platform__Suno: site/data/budget.json and docs/spend.md. In this area (Site__Agent__Suno): agent.json (updated), now.md, and mark the experiment done in experiments.md; commit and push both.
7. In Site__Platform__Suno, regenerate: python3 tools/pages.py; run build, share-check, quality, html-validate, axe and signers; commit (signed, trailers) and push to dev.
8. Refresh the two Suno playlists (newest 10 and newest 20, best take per version, newest first, archived left out): remove all, add in order.
9. Report to Dinis in the session: the song, both takes' links, what worked and what did not, credits left.
