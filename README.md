# SplitExec-Video-Splitter-For-Discord-And-Other-Platforms
SplitExec -> Video Splitter For Discord And Other Platforms -> App's purpose is to help you update easier.

What does SplitExec do?

A lightweight Windows desktop app that splits any video file into multi-volume
7-Zip archives sized to fit under upload caps. Drag a video into the window,
pick a part size, and SplitExec produces `Movie.7z.001`, `Movie.7z.002`, …
ready to upload to Discord, e-mail, or any service that limits file size.

Drop a 2 GB video and 450 MB part size → you get 5 parts, each just under
Discord Nitro's 500 MB cap. You can even limit it to 25 MB for free users.

To watch it back: download every part into the same folder, open `.7z.001`
with 7-Zip, click Extract. 7-Zip reads all parts automatically and restores
the original video.

Why split-archives (not just compression):

Video files are already compressed (H.264, HEVC, etc.) — re-compressing them
takes hours and barely shrinks anything. SplitExec uses 7-Zip in "store" mode
(`-mx=0`): no recompression, the split is essentially instant disk I/O.
Multi-volume archives are a 7-Zip native feature, so any 7-Zip install on
the receiving end opens them with no extra tooling.

Presets (and Custom):

- **450 MB** — Discord Nitro (500 MB upload cap, 50 MB headroom)
- **300 MB** — most webmail / cloud share links
- **100 MB** — older platforms
- **50 MB** — chat apps with tight caps
- **Custom** — type any MB value; the Custom button lights up automatically

The drop zone accepts: MP4 · MKV · AVI · MOV · WMV · FLV · WebM · M4V · TS.

Setup screen:

Comes with its own dark-themed installer (`SplitExec_Setup.exe`). One click:
copies to `C:\Program Files\SplitExec\`, makes a desktop shortcut, registers
in Programs & Features. Uninstall removes everything cleanly — including the
install folder itself (no leftovers).

Requirements: Windows 10/11 · 7-Zip ([7-zip.org](https://www.7-zip.org/), free)

Install: Download `SplitExec_Setup.exe` from **Releases**, run it, click Install → Launch.

For help & requests: hero999help@outlook.com

<img width="872" height="682" alt="image" src="https://github.com/user-attachments/assets/325a139e-3f2d-40b9-8bd3-49e84728b890" />

Developer's Note

I built this because Discord's 25 MB upload cap (and even the 500 MB Nitro
cap) keeps stopping me from sharing videos with friends. Existing tools
either re-encode the video (slow, quality loss) or hand you a 5 GB file split
into uselessly small pieces. SplitExec is the smallest possible tool for the
job: drag, pick a size, drop the parts into a chat. The whole thing is
Python + Tkinter + a `subprocess.Popen` call to 7-Zip — no encoding, no
quality loss, no cloud accounts. Same philosophy as the rest of my apps: I
don't believe AI-built tools should be paywalled, so this one is free too.

However, if you want, I would welcome a free coffee :D.
https://buymeacoffee.com/hero999
