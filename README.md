Backend :
1. FastAPI - Web framework for building API endpoints (GET/POST)
2. CORSMiddleware - Handles Cross-Origin Resource Sharing for frontend-backend communication
3. whisper - OpenAI's speech recognition for audio-to-text conversion
4. os - Handles file system operations (create dirs, file paths)(stores temp audio files)
5. re - Regular expressions for pattern matching in speech analysis
6. AudioSegment (pydub) - Audio file conversion/processing (WAV conversion) - When you upload a YouTube video: Backend downloads the audio track (not video) - > pydub converts it to WAV format because WAV is uncompressed = better for speech analysis Whisper model works best with WAV/PCM audio
7. YouTubeTranscriptApi - Fetches YouTube video transcripts
8. SequenceMatcher (difflib) - Compares spoken vs expected text similarity
9. datetime - Timestamps progress tracking entries

Key Functions:
- Whisper transcribes audio
- Regex detects stutter patterns
- pydub converts audio formats
- YouTube API gets practice material
- SequenceMatcher calculates accuracy

Frontend:
Here's a concise explanation of each part of your React frontend code:

1. ReactMic - Audio recording component that captures user speech
2. fetchTranscript - Gets YouTube transcript from backend API
3. fetchNextLine - Retrieves the next practice phrase from backend
4. fetchProgress - Fetches user's progress history with memoization
5. Recording Controls - startRecording/stopRecording manage audio capture
6. onStop Handler - Processes recorded audio and sends to backend for analysis
7. Specific Advice - Component that displays personalized stutter feedback
8. ProgressDisplay - Shows user's improvement timeline with accuracy metrics
9. UI Sections - Organized components for input, current phrase, results, and recording
10.Analysis Display - Shows accuracy percentage, disfluency rate, and colored feedback text
11.Error Handling - Catches and displays API errors to users

Key Flow: User records speech → Audio sent to backend → Returns analysis → Displays visual feedback + tracks progress.

Cure to stuttering:
Slow and controlled speech – Speaking at a slower pace reduces pressure.
Breathing exercises – Proper breath control can improve fluency.
Pausing and phrasing – Breaking speech into smaller chunks helps with smoother speech.
