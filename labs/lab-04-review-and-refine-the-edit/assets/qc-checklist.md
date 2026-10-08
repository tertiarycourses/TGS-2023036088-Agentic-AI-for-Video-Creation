# Technical QC checklist — vertical Short (9:16, 60 s)

| # | Parameter | Target | Measured / observed | PASS / FAIL | Evidence |
|---|---|---|---|---|---|
| 1 | Resolution | 1080x1920 | | | export settings |
| 2 | Aspect ratio | 9:16 | | | |
| 3 | Frame rate | constant 24/25/30 fps | | | |
| 4 | Duration | 55-60 s; end card ≥ 3 s | | | |
| 5 | Loudness | about -14 LUFS integrated | | | meter reading |
| 6 | True peak | ≤ -1 dBTP | | | |
| 7 | Dialogue clarity | every word clear over music | | | |
| 8 | A/V and lip-sync | no visible offset | | | |
| 9 | Captions | 100% accurate; ≤ 2 lines; inside safe zone | | | |
| 10 | Continuity | characters, props, light, direction match | | | |
| 11 | Artefacts | none on faces, hands, text | | | |
| 12 | Compliance basics | disclaimer on end card; no personal data | | | |

Optional measurement (trainer demo):

    ffprobe -v error -select_streams v:0 -show_entries stream=width,height,r_frame_rate:format=duration -of default=nw=1 EP01_v2.mp4
    ffmpeg -i EP01_v2.mp4 -af loudnorm=print_format=summary -f null -
