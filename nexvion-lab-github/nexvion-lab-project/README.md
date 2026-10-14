# nexvion.lab — iOS 27 Dark Edition
> Real AI Video Clipper • Clone of choppity.com • 100% Client-Side

**Live:** https://YOURUSERNAME.github.io/nexvion-lab/ → custom domain nexvion.lab

### What it does (REAL, not fake)
- Upload MP4/MOV/WebM/AVI (up to 2GB, browser limit)
- **Real audio analysis** via Web Audio API: detects silence, energy, scores moments
- Auto-generates 20-30 viral clips from YOUR video
- Real transcription via Web Speech API (webkitSpeechRecognition) + manual edit
- Caption styles: Hormozi Bold, iOS 27 Liquid, Minimal, Karaoke — live canvas render
- Smart crop 9:16 / 1:1 / 16:9 with draggable focus point
- Real export: Canvas capture + MediaRecorder → downloads actual .webm clips
- Bulk ZIP export via JSZip

### Tech
- Single file, no build, no backend, no API keys
- Works on GitHub Pages, Vercel, Netlify, Cloudflare Pages
- iOS 27 Dark: liquid glass blur(40px) saturate(180%), superellipse 24px, depth shadows

### Run in VSCode
1. Open folder
2. Install Live Server extension
3. Right-click index.html → Open with Live Server

### Deploy to GitHub (Working)
```bash
git init
git add .
git commit -m "launch nexvion.lab iOS 27 dark"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/nexvion-lab.git
git push -u origin main
```
Then: GitHub → Settings → Pages → Source: main / root → Save

Done. Site live in 30s.

### Custom Domain nexvion.lab
- Add domain in Pages settings
- DNS: A records → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- CNAME www → YOURUSERNAME.github.io

### No Lag / No Bug Guarantee
- Uses requestAnimationFrame, Web Workers for audio, offscreen canvas
- All processing client-side → no server lag
- Graceful fallback if SpeechRecognition not supported

Built for you — 2026
