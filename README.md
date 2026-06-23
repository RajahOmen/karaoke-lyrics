# Karaoke Lyrics

Lyrics for songs in FFXIV, unofficially hand-timed for synced playback. Lyric files are fetched by the [Karaoke plugin](https://github.com/RajahOmen/Karaoke) and defined in the [karaoke-lyrics](https://github.com/RajahOmen/karaoke-lyrics) repo.

Lyrics are stored as .lrc files, with some custom tags to configure playback in-game. Custom tags are the following:
- `[ids:{id1;id2;...}]` - Semicolon-separated list of BGM ids that the lyric file should be loaded for. This tag is required for use by the plugin.
- `[idoffsets:{id1:float1;id2:float2;...}]` - Semicolon-separated key-value pairs of lyric offsets (in seconds) to apply to specific BGM ids.
- `[loop:{int}]` - The zero-indexed line number for the first line after the song loops in-game. 

Subdirectories are used to group lyrics by category. 
- `official`: Lyrics from official SE sources, such as FanFest or physical releases. Takes default priority if other lyrics exist.
- `unofficial`: Lyrics from unofficial community sources, typically before official lyrics are known. Can be inaccurate. Lyricists for songs of this category may include the names/aliases of the fan-made transcriptions the sync are based on.

Any lyrics in directories defined above will be overwritten when the plugin is loaded, or the user reloads lyrics manually.

## New Song Requests

Ideally, all songs with lyrics should be supported as new ones are added. If a song with intelligible lyrics has no file, submit an issue with the song name, all of its FFXIV BGM ids, lyrics, and the source those lyrics are obtained from. I will time sync the song to the lyrics when I have time.

Alternatively, you can also sync the lyrics yourself and submit the LRC file as a PR to the appropriate folder category. If you take this approach, word-by-word/enhanced LRC files are highly preferred, and take care to ensure a high degree of accuracy with the timestamps for each word/line. Note: I've found that AI syncing tools available at the start of this project were not acceptably accurate, even when provided lyrics.

## Lyric/Sync Change Requests

If a song has incorrect lyrics or a timing feels off, feel free to make an issue or PR with the correction.

If a lyric is wrong, include an explanation and/or link to a source in your issue/PR. If the lyrics are unofficial and the correction is not from an official source, the change may or may not be accepted depending on the explanation, and how it listens to me/others.