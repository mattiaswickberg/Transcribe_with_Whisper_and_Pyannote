# Transcribe_with_Whisper_and_Pyannote
Based on the work of https://github.com/Majdoddin, I rewrote the code to suit the needs of myself and my colleagues.
This version iterates over a directory ("Data") and creates transcriptions of each file in that directory, with both a simple Whisper-transcription and a version divided by speaker (using Pyannote for diarization), and writes the result to a text file per original file in the Data directory. 

Note that the default language in this file is Swedish. 


## Notes: 

The pure whisper-transcription still seems to do better that the version with division by speaker, which is why I decided to do both versions by default. 

In Swedish, some odd things are happening, especially in the transcription with Pyannote. There seems to be a common-ish hallucination about subtitles ("Undertexter från...", and one about  patreon ("Tack till mina supporters på Patreon"). In addition to this I have gotten an unicode error that appears inconsistently, but only when using the tiny model (haven't tried small or base). 

