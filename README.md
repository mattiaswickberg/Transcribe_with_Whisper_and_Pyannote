# Whisper_trials

I've been looking into using Whisper för automatic transcription of audio files, and these are my scipts and reflections. 

## Whisper and Pyannote
Based on the work of https://github.com/Majdoddin, I rewrote the code to suit the needs of myself and my colleagues.
This version iterates over a directory ("Data") and creates transcriptions of each file in that directory, with both a simple Whisper-transcription and a version divided by speaker (using Pyannote for diarization), and writes the result to a text file per original file in the Data directory. 

Note that the default language in this file is Swedish. 


### Notes: 

The pure whisper-transcription still seems to do better that the version with division by speaker. 

In Swedish, some odd things are happening, especially in the transcription with Pyannote. There seems to be a common-ish hallucination about subtitles ("Undertexter från...", and one about  patreon ("Tack till mina supporters på Patreon"). In addition to this I have gotten an unicode error that appears inconsistently, but only when using the tiny model (haven't tried small or base). 

When trying to run this on GPU, I run into CUDA memory error. Trying to fix. 

## WhisperX
Testing Max Bains WhisperX (https://github.com/m-bain/whisperX![bild](https://user-images.githubusercontent.com/21317603/216549140-275f4f7b-408c-4d0b-b204-8d35d8a24377.png)) with KBLabs wav2vec2 model (https://huggingface.co/KBLab/wav2vec2-large-voxrex-swedish). 

A slightly modified version of WhisperX seems to be the best alternative so far. Modified verison available at https://github.com/mattiaswickberg/whisperX, and notebook to run is available in this repository (iterates through directory and creates transcription files or subtitles). 




