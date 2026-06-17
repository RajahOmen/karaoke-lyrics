100% hand-timed lyrics for songs in FFXIV. Fetched/consumed by the [Karaoke plugin](https://github.com/RajahOmen/Karaoke).

Lyrics are stored as .lrc files, with some custom tags to configure playback in-game. Custom tags are the following:
- [loop:{int}] - The zero-indexed line number for the first line after the song loops in-game. 
- [ids:{id1;id2;...}] - Semicolon-separated list of BGM ids that the lyric file should be loaded for.
- [idoffsets:{id1:float1;id2:float2;...}] Semicolon-separated kvp of second offsets to apply to lyric times for specific BGM ids.

Subdirectories are used to group lyrics by category. 
- official: Lyrics from official SE sources, such as FanFest or physical releases.
- unofficial: Lyrics from unofficial community sources, typically before official lyrics are known. Can be inaccurate.