# Jam Looper

A multitrack loop station that runs in your browser. Record from your mic, overdub, mute and solo tracks, switch between scenes, and export the mix as a WAV. It's one HTML file with no build step and no dependencies.

**[▶ Try it live](https://trymoto.github.io/jam-looper/)**

![Jam Looper screenshot](docs/screenshot.png)

## Features

- **Multitrack recording and overdubbing** from any audio input, with per-track volume, pan, mute and solo
- **Loop sections**: drag on the timeline to loop and record into just a few bars
- **Scenes**: save different clip arrangements and queue the switch to land on the next loop
- **Chords & form**: lay out a chord chart over the bars, with a key picker and preset forms
- **Metronome, count-in and tap tempo**
- **Latency calibration** so overdubs line up
- **Undo / redo**
- **Export the mix** as a stereo `.wav`
- **Projects** saved in your browser (IndexedDB). Nothing gets uploaded anywhere.
- Light and dark Gruvbox themes. Works on phones and can be added to your home screen.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `Space` | Play / stop |
| `1`–`9`, `0` | Record on track 1–10 |
| `Shift` + number | Mute track |
| `Alt` + number | Solo track |
| `←` / `→` | Previous / next bar (`Shift`: by beat) |
| `Home` | Go to start |
| `↑` / `↓` | BPM ±1 (`Shift`: ±5) |
| `[` / `]` | Set loop start / end here |
| `L` | Toggle loop section (`Shift+L` clears it) |
| `,` / `.` | Previous / next scene |
| `R` | Toggle performance mode |
| `I` | Toggle performance input |
| `M` | Metronome |
| `C` | Count-in |
| `T` | Tap tempo |
| `B` | Rec starts at top of loop / next bar |
| `N` | New track |
| `K` | Show / hide chords |
| `E` | Export mix |
| `Ctrl/⌘+Z`, `Ctrl/⌘+Shift+Z` or `Ctrl/⌘+Y` | Undo / redo |
| `Esc` | Cancel a pending recording |

## Running locally

Open `index.html` in a browser. Mic access needs a secure context, so if your browser won't allow it from a `file://` URL, serve the folder instead:

```sh
npx serve .
# or
python -m http.server
```

Then open http://localhost:3000 (or :8000).

Use headphones while overdubbing so the speakers don't bleed into the mic.

## Browser support

This works in any recent version of Chrome, Edge, Firefox or Safari. It needs the Web Audio API, `getUserMedia` and IndexedDB.

## Contributing

Issues and pull requests are welcome. The whole app lives in `index.html`: the styles, markup and script are all inline.

## License

[MIT](LICENSE)
