# CUTROOM

**A transcript-bound video editor.** Record from your camera, get a live transcript, and cut the footage by deleting words. Every line of text is welded to its slice of video — delete the line, lose the slice.

One HTML file. Runs entirely in the browser: `MediaRecorder` for capture, the Web Speech API for the live transcript, and canvas + WebAudio to re-render only the kept ranges into a trimmed WebM on export. Nothing is uploaded anywhere.

## How it works

1. **Record.** The transcript builds as you speak; each phrase is time-stamped to the recording.
2. **Edit the text.** Delete a phrase to cut it. Restore it to put it back. Double-click to fix a transcription — timing stays bound, only the words change.
3. **Play.** Playback skips the cuts so you hear the edit as you go.
4. **Export.** A new WebM containing only what survived.

## Why

Text is the fastest editing surface there is, and most talking-head footage is already text in disguise. Descript proved the model; this is the minimum viable version of it with no account, no upload, no install.

## Caveats

Browser speech recognition quality varies by browser and language (best in Chromium-based browsers). Export re-encodes through canvas, so expect it to take roughly real time.
