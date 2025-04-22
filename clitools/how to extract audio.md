START
Basic
Front: 
How to extract audio from a file and convert it to a WAV with 1 channel and 16 kHz sampling rate?
Back: 
```sh
ffmpeg -i file.m4a -ac 1 -ar 16000 output.wav
```
Here:
- `-ac 1` — one audio channel;
- `-ar 16000` — 16 kHz sampling rate.
<!--ID: 1745238713598-->
END
