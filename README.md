# YouTube Channel Automation

n8n workflows for YouTube Shorts automation.

## Files
- `youtube_shorts_automation_workflow.json` — v1 starter pipeline (script + VO + scene jobs)
- `youtube_shorts_automation_workflow_v2.json` — v2 extended pipeline (polling, render, approval, upload placeholder)

## Import
In n8n: **Workflows → Import from file** and select the JSON.

## Required env vars (v2)
- `OPENAI_API_KEY`
- `REPLICATE_API_TOKEN`
- `ELEVENLABS_API_KEY`
- `ELEVENLABS_VOICE_ID`
- `TELEGRAM_CHAT_ID`
- `YOUTUBE_UPLOAD_WEBHOOK_URL` (your uploader endpoint)
