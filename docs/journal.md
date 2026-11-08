
## 2026-11-08 — yt-dlp (lecture de liens TikTok)
- Installé : paquet PyPI `yt-dlp` 2026.10.26 (pip), dans le conteneur de session cloud. ffmpeg était déjà présent.
- Droits : lit les pages TikTok données ; écrit uniquement dans le dossier temporaire de session. Aucun identifiant ni cookie fourni.
- Retrait : `pip uninstall yt-dlp` (le conteneur est éphémère).
