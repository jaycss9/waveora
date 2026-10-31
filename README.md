# Waveora - 4K Export Fixed for Vercel

This build uses FFmpeg.wasm MT (multi-thread) when deployed on Vercel with COOP/COEP headers.

- GitHub Pages: single-thread, slow, may OOM on 4K
- Vercel (this): multi-thread, 4x faster, true 4K works

## Deploy
1. Push this folder to GitHub
2. Import to Vercel (vercel.com/new)
3. Deploy - done. No env vars needed.

Exports will be true 2160x3840 H.264 + AAC.
