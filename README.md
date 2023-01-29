# Transcribe_with_Whisper_and_Pyannote
Based on the work of https://github.com/Majdoddin, I rewrote the code to suit the needs of myself and my colleagues.
This version iterates over a directory ("Data") and creates transcriptions of each file in that directory, with both a simple Whisper-transcription and a version divided by speaker (using Pyannote for diarization), and writes the result to a text file per original file in the Data directory. 

Note that the default language in this file is Swedish. 
