# Nursery Rhyme Audio Files

This directory contains pre-recorded audio files for nursery rhymes. When available, these sung versions will play instead of text-to-speech.

## File Naming Convention

Files should match the `audioFile` property in `src/components/NurseryRhymes.tsx`:

```
twinkle-star.mp3
humpty-dumpty.mp3
baa-baa-black-sheep.mp3
itsy-bitsy-spider.mp3
old-macdonald.mp3
jack-and-jill.mp3
row-row-boat.mp3
wheels-on-bus.mp3
...etc
```

## Required Format

- **Format**: MP3 or OGG (MP3 recommended for better browser support)
- **Quality**: 128kbps or higher
- **Duration**: 30 seconds to 2 minutes per rhyme
- **Size**: Aim for 1-2 MB per file

## Where to Find Free Recordings

### 1. Freesound.org
- Search for "nursery rhyme" or specific titles
- Filter by CC0 or CC-BY licenses
- https://freesound.org/

### 2. Internet Archive
- Public domain recordings
- Search: "nursery rhymes children songs"
- https://archive.org/

### 3. Wikimedia Commons
- Category: Children's songs
- https://commons.wikimedia.org/

### 4. YouTube Audio Library
- Royalty-free music
- https://studio.youtube.com/channel/UC.../music

### 5. Record Your Own!
- Use your phone or microphone
- Sing the rhymes yourself
- Convert to MP3 using Audacity (free)

## How It Works

1. Component checks if audio file exists
2. If yes: Plays recorded singing
3. If no: Falls back to browser text-to-speech
4. Both work offline (PWA)

## Adding a New Audio File

1. Download/record your audio file
2. Name it according to the convention above
3. Place it in this directory
4. Make sure the filename matches `audioFile` in NurseryRhymes.tsx
5. Test locally: `npm run dev`
6. Rebuild and redeploy

## File Size Considerations

- GitHub Pages limit: 1 GB total
- Current estimate: ~30 rhymes × 1.5 MB = ~45 MB
- Plenty of room! ✅

## License Compliance

Make sure any audio you add is:
- ✅ Public domain
- ✅ CC0 (no attribution required)
- ✅ CC-BY (requires attribution - add to credits)
- ✅ Your own recording
- ❌ NOT copyrighted commercial recordings

## Testing

After adding files:

```bash
# Test locally
npm run dev

# Check the rhyme plays audio
# Look for: "🎤 Sung Version Available" badge

# Check browser console
# Should see: [NurseryRhymes] Using audio: /audio/rhymes/...
```

## Deployment

Files are automatically included in the build when you run:

```bash
npm run build
```

The `public/` directory is copied to `dist/` during build.

---

**Need help?** Check the main README or open an issue!
