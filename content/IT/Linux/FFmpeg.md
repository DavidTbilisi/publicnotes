---
tags:
  - it/cli
  - media
  - enabler
  - free
---




```bash
ffmpeg -list_devices true -f dshow -i dummy
# list devices 
```


| Part                        | What it does                                                         |
| --------------------------- | -------------------------------------------------------------------- |
| `-f gdigrab`                | Screen capture input (Windows only)                                  |
| `-framerate 30`             | Frames per second (you can increase to 60)                           |
| `-i desktop`                | Capture the full screen                                              |
| `-f dshow`                  | DirectShow input for audio                                           |
| `audio="Microphone (Camo)"` | Your mic                                                             |
| `-vcodec libx264`           | Video codec                                                          |
| `-preset ultrafast`         | Less CPU, bigger file (change to `medium` or `slow` for compression) |
| `-pix_fmt yuv420p`          | Ensures compatibility for players                                    |



```bash
ffmpeg -f dshow -i audio="Microphone (2- Samson Q2U Microphone)" -t 00:00:10 test-audio.wav 
# Test audio - Record 10 seconds and stop
```

```powershell
Get-Process |
  Where-Object { $_.MainWindowTitle } |
  Select-Object Id, ProcessName, MainWindowTitle
# Get window titles to record only certain window
```

