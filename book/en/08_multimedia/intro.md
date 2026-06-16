# Multimedia in HTML

Multimedia elements allow you to integrate images, audio, and video directly into your HTML pages. HTML5 provides native tags without needing external plugins.

## What is multimedia?

Multimedia refers to:
- 🖼️ **Images** — PNG, JPG, SVG, WebP
- 🔊 **Audio** — MP3, OGG, WAV
- 🎥 **Video** — MP4, WebM, OGG
- 📺 **Embedded content** — iframes, maps

## Images with `<img>`

The most basic tag:

```html
<img src="image.jpg" alt="Description">
```

**Important attributes:**
- `src` — Image path (required)
- `alt` — Alternative text (required for accessibility)
- `width` / `height` — Dimensions
- `loading="lazy"` — Lazy loading

### Responsive images

To adapt images to different screens:

```html
<img 
  src="image.jpg" 
  srcset="
    image-small.jpg 600w,
    image-medium.jpg 1000w,
    image-large.jpg 1600w"
  sizes="(max-width: 600px) 100vw, 
         (max-width: 1000px) 75vw, 
         90vw"
  alt="Description">
```

- `srcset` — List of images by width
- `sizes` — Which image to use per viewport
- Browser automatically chooses

### `<picture>` element for full control

```html
<picture>
  <source media="(min-width: 1200px)" srcset="image-large.jpg">
  <source media="(min-width: 600px)" srcset="image-medium.jpg">
  <img src="image-small.jpg" alt="Description">
</picture>
```

Use: different images per device or format.

## Audio with `<audio>`

Native audio playback:

```html
<audio controls>
  <source src="song.mp3" type="audio/mpeg">
  <source src="song.ogg" type="audio/ogg">
  Your browser doesn't support HTML5 audio.
</audio>
```

**Attributes:**
- `controls` — Shows playback controls
- `autoplay` — Plays automatically
- `loop` — Continuous repeat
- `muted` — Muted by default
- `preload="auto|metadata|none"` — How to load

**Formats:**
- MP3 — Compatible with all
- OGG — Open source alternative
- WAV — High quality

## Video with `<video>`

Native video playback:

```html
<video controls width="640" height="360">
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Your browser doesn't support HTML5 video.
</video>
```

**Attributes:**
- `controls` — Playback controls
- `poster="image.jpg"` — Preview image
- `autoplay` — Plays automatically
- `loop` — Repeat
- `muted` — Muted
- `preload` — How to load

**Formats:**
- MP4 — Best compatibility
- WebM — Better compression
- OGG — Open source alternative

## Subtitles and text tracks

```html
<video controls>
  <source src="video.mp4">
  <track kind="subtitles" src="subtitles-en.vtt" srclang="en" label="English">
  <track kind="subtitles" src="subtitles-es.vtt" srclang="es" label="Español">
  <track kind="captions" src="captions.vtt" srclang="en">
</video>
```

**Track types:**
- `subtitles` — Dialogue translation
- `captions` — Full transcript (including sounds)
- `descriptions` — Description for visually impaired

## iframes for external content

```html
<iframe 
  src="https://www.youtube.com/embed/VIDEO_ID" 
  width="560" 
  height="315" 
  frameborder="0" 
  allowfullscreen>
</iframe>
```

**Security attributes:**
- `sandbox` — Security restrictions
- `allow` — Specific permissions

**Secure example:**
```html
<iframe 
  src="https://www.youtube.com/embed/VIDEO_ID"
  sandbox="allow-playback allow-same-origin"
  title="YouTube Video">
</iframe>
```

## Multimedia best practices

### ✅ Make multimedia accessible
```html
<img src="chart.png" alt="Q1 2026 sales chart">
<audio controls>
  <source src="podcast.mp3">
  <p>Your browser doesn't support audio.</p>
</audio>
```

### ✅ Use multiple formats
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
</video>
```

### ✅ Optimize images
- Use responsive `srcset` tool
- Compress without losing quality
- Consider WebP as modern alternative

### ✅ Lazy loading
```html
<img src="image.jpg" loading="lazy" alt="...">
```

### ❌ Avoid
- Audio/video auto-playing without permission
- Images without `alt` attribute
- Multimedia without text alternatives

---

In upcoming topics you'll learn:
1. Responsive images in detail
2. Multimedia optimization
3. JavaScript integration
4. Accessibility in multimedia
