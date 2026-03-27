# RATE — Music Player

A browser-based music player inspired by [AOTY](https://www.albumoftheyear.org/), built for listeners who want to rate and explore their music collection at the track level.

---

## Features

### Playback & Formats

Supports MP3, FLAC and WAV (tested). AAC/M4A and OGG should work but are untested. Runs entirely in the browser, only tested in Chrome and Chromium-based browsers. Firefox may work.

### Ratings

Rate every track from 1-100, just like AOTY but without the album rating threshold. 

### Shuffle Modes

Four mathematically distinct shuffle algorithms:

| Mode | Description |
|------|-------------|
| **FY (Fisher-Yates)** | Pre-generates a complete random sequence. Every track plays exactly once before repeating. No weighting. |
| **ST (Stochastic)** | Weighted random sampling using a log-scale rating distribution. Higher rated tracks are more likely to be picked. Unrated tracks default to 75. |
| **EN (Entropy)** | Like Stochastic, but actively penalises recently played artists, genres and albums to maximise variety. |
| **FC (Focus)** | Like Stochastic, but steered toward a chosen artist, genre or album. Other tracks blend in when the focused pool runs low. |

### Library Management

- Inline editing of track title, artist, album and genre
- Sort by rating, title, artist, album, genre or recently added
- Group by album, artist or genre with collapsible groups, collapse state persists across sessions
- Repeat mode per group (album/artist/genre)
- Search across title, artist, album and genre simultaneously
- Multi-select tracks for bulk actions (set cover art, fetch art, delete)
- Auto-fetch album art and genre tags via MusicBrainz
- Drag and drop import
- Session restore, resumes last played track, playback position and volume on reload

### Stats

Rating distribution, top artists and albums by average rating, total playtime, rated vs unrated count and more, all computed from your local library.

### Other

- Light mode (white + lime green) and dark mode (black + gold)
- Audio visualizer + animated progress bar
- Keyboard shortcuts: `Space` (play/pause), `←` (previous), `→` (next)
- All data stored locally in your browser (IndexedDB), nothing is sent to a server

---

## Storage & Performance

Should work comfortably up to ~2,000 tracks, possibly more. Provided as-is, use at your own risk. See LICENSE.

---

## License

MIT, see [LICENSE](LICENSE)
