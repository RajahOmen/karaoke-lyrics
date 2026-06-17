Lyrics for songs in FFXIV, unofficially hand-timed for synced playback. Lyrics are fetched/consumed by the [Karaoke plugin](https://github.com/RajahOmen/Karaoke) and defined in the [karaoke-lyrics] github repository (https://github.com/RajahOmen/karaoke-lyrics).

Lyrics are stored as .lrc files, with some custom tags to configure playback in-game. Custom tags are the following:
- `[ids:{id1;id2;...}]` - Semicolon-separated list of BGM ids that the lyric file should be loaded for. Must be the first tag, on the first line.
- `[idoffsets:{id1:float1;id2:float2;...}]` - Semicolon-separated key-value pairs of lyric offsets (in seconds) to apply to specific BGM ids.
- `[loop:{int}]` - The zero-indexed line number for the first line after the song loops in-game. 

Subdirectories are used to group lyrics by category. 
- `official`: Lyrics from official SE sources, such as FanFest or physical releases. Takes default priority if other lyrics exist.
- `unofficial`: Lyrics from unofficial community sources, typically before official lyrics are known. Can be inaccurate.

Any lyrics in directories defined above will be overwritten when the plugin is loaded, or the user reloads lyrics manually.