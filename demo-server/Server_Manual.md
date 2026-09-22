# Demo Server

This local server gives reviewers one browser entry point for manual testing.

Voice Module supports:

- text-based web calling
- microphone speech recognition when the browser supports it
- browser speech playback
- audio recording save to `test_reports/voice_assistant/recordings/`
- transcript history

## Run

```powershell
python .\src\server.py --host 127.0.0.1 --port 8088
```

Then open:

- `http://127.0.0.1:8088/`
- `http://127.0.0.1:8088/voice_assistant`
- `http://127.0.0.1:8088/knowledge_system`
- `http://127.0.0.1:8088/regional_bots`
- `http://127.0.0.1:8088/realtime_analytics`
