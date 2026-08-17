# CHAPTER 20 — NANDU · FINAL

This is the final implementation of the requested Chapter 20 birthday journey.

## 1. Run it

1. Extract the ZIP completely.
2. Open the `chapter-20` folder.
3. Double-click `index.html` for a quick visual preview.
4. For microphone candle blowing, use a local server because browser microphone permission is normally restricted on `file://` pages.
5. If Python is installed, open a terminal inside the `chapter-20` folder and run:

```text
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Allow microphone access when the browser asks.

## 2. Add your audio

Put your files in `assets/audio/` with these exact names:

- `nandu-laugh.mp3` — Chapter 6 laugh
- `my-voice-note.mp3` — Chapter 7 voice note
- `birthday-recording.mp3` — Chapter 20 birthday-song page, if you later decide to use one there
- `happy-birthday.mp3` — the birthday song that plays while the 20 candles are being blown
- `background.mp3` — optional site background music

The paths are already configured in `config.js`.

## 3. Add photos

The final build deliberately leaves personal-photo placeholders instead of inventing images.

### Chapter 3
Replace `YOUR FIRST MEETUP PHOTO` in `script.js` with an `<img>` pointing to your image.

### Chapter 9
Replace the two boxes labelled:

- `PHOTO WITH HER PARENTS`
- `PHOTO WITH HER SISTER`

with your actual images.

### Chapter 11
There are two separate childhood-photo boxes. Replace:

- `CHILDHOOD PHOTO 01`
- `CHILDHOOD PHOTO 02`

with your actual images.

### Chapter 12
The photo room is generated from `CONFIG.memories` in `config.js`. Put images in `assets/images/` and set each memory's `image` field to its relative path, for example:

```text
assets/images/memory-01.jpg
```

Two TikTok placeholders are also provided. Put your two TikTok videos in `assets/tiktoks/` and replace the corresponding placeholder elements in Chapter 12 with `<video controls>` elements using those paths.

### Chapter 14
Replace `BOUQUET PHOTO` with your bouquet image.

### Final chapter
Replace `BABY PHOTO · THE DAY YOU WERE BORN` with the childhood/baby photo you want to use.

## 4. Edit the final letter

The easiest place to edit the letter is `config.js`, inside `finalMessage`.

You can write as much as you want. The full-screen letter reader also contains an editable area so the displayed letter can be adjusted while testing.

## 5. Test the important interactions

- Welcome: the `No Not needed from you` button moves instead of accepting a click.
- Chapter 5: click the blocking button six times; the text grows, sad emojis escalate, and the button shrinks away.
- Chapter 6: add `nandu-laugh.mp3`, then press `accept the risk`.
- Chapter 7: add `my-voice-note.mp3`, then press `Tell me what you what to say`.
- Chapter 13: click each glowing hidden cover.
- Chapter 14: spin the wheel five times. Each result appears as a three-second popup; after the fifth spin the site moves on automatically.
- Chapter 19: start the countdown. Each of the 20 memories is highlighted for four seconds.
- Chapter 20: press `Make a wish and blow the candle`, allow microphone access, or use tap/swipe fallback. The birthday song loops until all candles are out. Then cut the cake with the knife to continue.
- Letter: press `Disclose the letter`; the ribbon opens and the letter rises into a full-screen reading view.

## 6. Final deployment

After all photos/audio/text are added and tested on desktop and mobile, upload the complete `chapter-20` folder to any static-hosting service that accepts HTML/CSS/JS files. The entry point is `index.html`.

Do not rename `style.css`, `script.js`, or `config.js` unless you also update their references.
