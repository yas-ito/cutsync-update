# CutSync — User Guide

CutSync is a panel (UXP plugin) for Adobe Premiere Pro 25.6 or later (macOS / Windows).
It snaps the **start and end** of your captions (text / graphics clips) to the **cut points** of your video or audio.

## Open the panel

**Window → UXP Plugins → yas-tools | CutSync.**
The first time, "Choose your language" appears — click **English** (you can change it later in Settings).

## Use it

1. Open a sequence that is already cut, with your captions placed on it.
2. **Reference track** — the track with your cuts. Choose Video or Audio and a number (default: Video 1).
3. **Track to fix** — leave it on **Auto** (it finds every track that has text clips), or pick a track.
4. **Max offset** — leave it on **Auto** (it measures the actual drift and shows the value in the LOG), or set 3–5 for tight cuts, up to about 10 for loose cuts.
5. Click **Snap to cuts**. There is no confirmation dialog; the result appears right below the button.

- Neighboring captions are never deleted: where snapping would cover a short caption, that edge is left in place (the LOG shows how many).
- Undo everything with a single **Ctrl+Z / Cmd+Z**, or click **Restore original timing** to go back to before your first run.
- Cuts and transcripts are never touched; only caption starts and ends move.

## Settings

Panel colors, language (Auto / 日本語 / English) and **Reset to defaults**. Settings are saved on your computer.

## Troubleshooting

- **"No offsets found within N frames"** — check the track type and numbers. If the LOG says "Auto → 0 frames", set the max offset to 8–10.
- **"... track number is out of range"** — the number points to a track that does not exist in the sequence.
- **Snapped somewhere unexpected** — try a smaller max offset (3–5) and make sure the caption track contains only captions.
- **The panel is not in Window → UXP Plugins** — restart Premiere Pro completely.

## Updates

- From the Adobe Creative Cloud Marketplace: updates arrive through the Creative Cloud desktop app.
- From other stores: when a new version is released, the panel shows a notice; download it from where you purchased CutSync.

[Privacy Policy](PRIVACY.md) · [License Terms](TERMS.md) · Contact: iyasunori0802@gmail.com
