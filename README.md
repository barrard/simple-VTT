# Simple Chrome VTT Dictation Pad

Small single-page HTML app for browser-based dictation in Chrome using the native Web Speech API.

## Requirements

- `npm`
- Chrome or another Chromium-based browser with microphone access enabled

## Run With `live-server`

Install `live-server` globally with npm:

```bash
npm install -g live-server
```

Start the app from this folder:

```bash
live-server
```

That will serve `index.html` locally and usually open it in your browser.

## Alternative: Run Without Installing Globally

You can also run it with `npx`:

```bash
npx live-server
```

## Features

- Native Chrome speech recognition via `SpeechRecognition` / `webkitSpeechRecognition`
- Start / stop dictation controls
- Copy transcript to clipboard
- Clear transcript
- Live interim dictation preview with visible caret
- Spoken formatting commands converted into text structure
- Phrase-level confidence display when Chrome exposes confidence values
- Low-confidence phrase highlighting
- Manual correction tools for uncertain phrases
- LLM-friendly formatting helpers for structured prompting

## Supported Voice Commands

- `new line`
- `new paragraph`
- `new bullet`
- `period`
- `comma`
- `question mark`
- `exclamation point`
- `colon`
- `semicolon`
- `open quote`
- `close quote`
- `open parenthesis`
- `close parenthesis`
- `open bracket`
- `close bracket`
- `open brace`
- `close brace`
- `dash`
- `em dash`
- `arrow`
- `ellipsis`
- `delete last sentence`
- `delete last paragraph`
- `scratch that`
- `speaker note`
- `end note`
- `instruction`
- `context`
- `example`
- `important`
- `new section`
- `code block`
- `end code block`

## Notes

- Confidence is typically phrase-level, not word-level.
- Browser support is best in Chrome / Chromium.
- You may need to allow microphone permission the first time you start dictation.
