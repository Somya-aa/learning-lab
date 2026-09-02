# HTML Multimedia

HTML provides elements for adding multimedia content such as audio, video, and subtitles to webpages. The main elements used for multimedia are `<audio>`, `<video>`, `<source>`, and `<track>`.

---

## Audio

The `<audio>` element is used to embed sound or music into a webpage.

### Basic Syntax

```html
<audio controls>
    <source src="audio/song.mp3" type="audio/mpeg">
</audio>
```

The `controls` attribute displays native browser playback controls such as play, pause, seek, and volume.

---

### Audio Attributes

| Attribute | Purpose |
| :--- | :--- |
| `controls` | Displays native audio playback controls |
| `autoplay` | Starts playing the audio automatically upon page load |
| `muted` | Sets audio output to silent by default |
| `loop` | Automatically restarts the audio from the beginning when finished |
| `preload` | Suggests to the browser how to load the audio file (`none`, `metadata`, `auto`) |

```html
<audio controls loop>
    <source src="audio/music.mp3" type="audio/mpeg">
</audio>
```

> **Note:** Browsers frequently restrict `autoplay` behavior unless paired with `muted` to prevent unexpected playback.

---

## Video

The `<video>` element is used to embed movie clips and video streams.

### Basic Syntax

```html
<video controls width="640">
    <source src="video/movie.mp4" type="video/mp4">
</video>
```

---

### Video Attributes

| Attribute | Purpose |
| :--- | :--- |
| `controls` | Displays native playback controls |
| `autoplay` | Starts the video automatically upon page load |
| `muted` | Mutes audio output by default |
| `loop` | Replays the video continuously |
| `width` / `height` | Sets the display dimensions of the video player in pixels |
| `poster` | Displays an image placeholder before playback begins |
| `preload` | Informs the browser about media preloading strategy |

```html
<video controls width="640" poster="images/thumbnail.jpg">
    <source src="video/lesson.mp4" type="video/mp4">
</video>
```

---

## Multiple Formats & Fallback with `<source>`

Different browsers support different audio and video codecs. The `<source>` element lets you declare multiple formats so the browser can select the first compatible option it supports.

### Video with Multiple Sources

```html
<video controls width="640">
    <source src="video/lesson.mp4" type="video/mp4">
    <source src="video/lesson.webm" type="video/webm">
    <p>Your browser does not support the HTML5 video element.</p>
</video>
```

### Audio with Multiple Sources

```html
<audio controls>
    <source src="audio/music.mp3" type="audio/mpeg">
    <source src="audio/music.ogg" type="audio/ogg">
    <p>Your browser does not support the HTML5 audio element.</p>
</audio>
```

---

## Subtitles and Captions with `<track>`

The `<track>` element specifies timed text tracks (subtitles, captions, descriptions) using standard WebVTT (`.vtt`) files.

```html
<video controls width="640">
    <source src="video/lesson.mp4" type="video/mp4">
    <track src="captions/en.vtt" kind="subtitles" srclang="en" label="English" default>
</video>
```

### Track Attributes

| Attribute | Purpose |
| :--- | :--- |
| `kind` | Defines track category (`subtitles`, `captions`, `descriptions`, `chapters`) |
| `src` | URL/path of the `.vtt` timed text file |
| `srclang` | Language code of the text track (e.g., `en`, `es`) |
| `label` | User-readable title displayed in the caption menu |
| `default` | Marks the track to be activated automatically |

---

## Embedding External Videos (`<iframe>`)

Third-party video hosts (such as YouTube, Vimeo, or external media services) provide embedded players using `<iframe>`:

```html
<iframe
    width="560"
    height="315"
    src="https://www.example.com"
    title="Embedded content"
    allowfullscreen>
</iframe>
```

---

## Multimedia File Formats

### Common Audio Formats

| Format | Common Use Cases |
| :--- | :--- |
| **MP3** | Broadest cross-platform browser support |
| **WAV** | High-quality, uncompressed audio |
| **OGG** | Open-source container format |
| **AAC** | Highly efficient compressed audio format |

### Common Video Formats

| Format | Common Use Cases |
| :--- | :--- |
| **MP4** | Universal standard supported across nearly all browsers and devices |
| **WebM** | Lightweight, open format designed specifically for the web |
| **OGG** | Open-source alternative video format |

---

## Recommended Project File Structure

```text
website/
├── index.html
├── audio/
│   └── music.mp3
├── video/
│   └── lesson.mp4
├── images/
│   └── thumbnail.jpg
└── captions/
    └── en.vtt
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML Multimedia</title>
</head>
<body>

    <h1>HTML Multimedia</h1>

    <h2>Audio</h2>
    <audio controls>
        <source src="audio/music.mp3" type="audio/mpeg">
        <source src="audio/music.ogg" type="audio/ogg">
        <p>Your browser does not support the audio element.</p>
    </audio>

    <h2>Video</h2>
    <video controls width="640" poster="images/thumbnail.jpg">
        <source src="video/lesson.mp4" type="video/mp4">
        <source src="video/lesson.webm" type="video/webm">

        <track
            src="captions/en.vtt"
            kind="subtitles"
            srclang="en"
            label="English"
            default
        >

        <p>Your browser does not support the video element.</p>
    </video>

</body>
</html>
```

---

## Multimedia Accessibility

- **Video:**
  - Always provide captions or subtitles (`.vtt`) for spoken dialogues.
  - Set meaningful `title` attributes on `<iframe>` tags.
  - Provide interactive controls (`controls`).
  - Do not autoplay unmuted audio tracks.
- **Audio:**
  - Always provide playback controls.
  - Offer transcripts or text equivalents for podcasts and voice recordings.
  - Never surprise users with unprompted background music.

---

## Best Practices

- [x] Always include the `controls` attribute unless custom JavaScript controls are implemented.
- [x] Avoid unexpected `autoplay` audio to protect user experience.
- [x] Pair `autoplay` with `muted` when automated playback is necessary.
- [x] Provide multiple `<source>` formats for broader codec compatibility.
- [x] Attach subtitles or captions (`<track>`) to spoken audio/video content.
- [x] Optimize file compressions and bitrates to ensure fast load times.
- [x] Add informative fallback text inside `<video>` and `<audio>` tags.
- [x] Always supply a `poster` image to avoid empty black screens before video playback.

---

## Common Mistakes to Avoid

### 1. Omitting the `controls` Attribute

```html
<!-- Incorrect (user cannot play or stop media) -->
<audio src="audio/music.mp3"></audio>

<!-- Correct -->
<audio controls>
    <source src="audio/music.mp3" type="audio/mpeg">
</audio>
```

### 2. Broken Relative Paths

```html
<!-- Incorrect if lesson.mp4 is located in a subfolder -->
<video controls src="lesson.mp4"></video>

<!-- Correct -->
<video controls>
    <source src="video/lesson.mp4" type="video/mp4">
</video>
```

### 3. Missing Captions on Spoken Media

```html
<!-- Better accessibility practice -->
<video controls width="640">
    <source src="video/lesson.mp4" type="video/mp4">
    <track src="captions/en.vtt" kind="subtitles" srclang="en" label="English">
</video>
```

---

## Common Multimedia Elements & Attributes Reference

| Element / Attribute | Description |
| :--- | :--- |
| `<audio>` | Embeds sound or music |
| `<video>` | Embeds video content |
| `<source>` | Defines an alternate media file resource |
| `<track>` | Attaches timed text tracks (subtitles, captions) |
| `controls` | Displays native playback controls |
| `autoplay` | Automatically initiates playback |
| `muted` | Silences media by default |
| `loop` | Restarts playback continuously upon completion |
| `poster` | Image shown before video starts |
| `preload` | Hint for how the browser preloads media files |

---

## What I Learned

- Embedding audio files with `<audio>` and video streams with `<video>`.
- Providing format fallbacks using `<source>` tags.
- Adding accessible subtitles and captions via `<track>` and WebVTT (`.vtt`).
- Configuring playback attributes (`controls`, `muted`, `autoplay`, `loop`, `poster`).
- Organizing multimedia assets across dedicated subdirectories.
- Embedding external players securely with `<iframe>`.
- Accessibility considerations for audio and video assets on the web.

---

## Summary

HTML native multimedia elements make embedding audio and video seamless:

```html
<audio controls>
    <source src="audio/music.mp3" type="audio/mpeg">
</audio>

<video controls width="640" poster="images/thumbnail.jpg">
    <source src="video/lesson.mp4" type="video/mp4">
</video>
```

Combining playback controls, fallbacks, captions, and responsive dimensions delivers an accessible, robust media experience across all web platforms.

---

## Navigation

⬅️ Previous: [HTML Swmantic Elements](08-HTML-Semantic-Elements.md)

➡️ Next: [HTML Attribute](10-HTML-Attribute.md)