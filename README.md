# Gist

Offline lecture transcription and study notes for Android. Record a lecture, get a live
transcript on your phone, then turn it into notes. Built around the Galaxy Z Fold4, and works on
other 64-bit Android 12+ phones, such as the Pixel 9 Pro.

## What it does

- **Live transcription, fully offline.** Whisper runs on the phone. Nothing is uploaded.
- **Word-by-word highlighting** while you play a lecture back, with tap-to-jump on any line.
- **Notes** written by an AI: overview, notes by time, key terms and review questions.
  Use a small model on your own home server (over Tailscale), or switch on Full offline mode to
  write them on the phone.
- **Speaker detection** (optional): see when someone else speaks.
- **Word checking** (optional): an offline AI fixes mis-heard words, like "cash" for "cache".
- **Bookmarks**, playback speed, search across transcripts and notes, and bulk actions
  (press and hold lectures to share, delete or save many at once).
- **Fold layout** (Samsung Zfold4 tested on): side-by-side panes when unfolded.

## First launch

1. Allow the microphone and notifications.
2. Tap **Download** on the card to fetch the speech model (about 400 MB, Wi-Fi only).
   After that, transcription works offline.
3. Optional extras are in **Settings**. Each one asks "Download prerequisites?" before it
   downloads anything:
   - Speaker model, about 26 MB
   - Offline AI, about 1.6 GB (for Full offline mode and word checking)

## AI notes on your own server

Follow `SERVER-SETUP.md` to run Ollama in a Proxmox container with Tailscale, then enter the
server's address in **Settings** and tap **Test connection**. Only transcript text is sent,
never audio.

## Privacy

Audio and transcripts stay on the phone. The only thing that can leave it is transcript text sent
to a server you choose, and not even that in Full offline mode.

## Status

Personal project, built step by step and not yet widely tested. Expect rough edges, and
please report build errors or odd behaviour.
