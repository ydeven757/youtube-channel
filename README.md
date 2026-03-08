# YouTube Channel Automation

n8n workflows for YouTube Shorts automation.

## Files
- `youtube_shorts_automation_workflow.json` — v1 starter pipeline (script + VO + scene jobs)
- `youtube_shorts_automation_workflow_v2.json` — v2 extended pipeline (includes Execute Command/ffmpeg node)
- `youtube_shorts_automation_workflow_v2_1_cloudsafe.json` — cloud-safe v2.1 (no Execute Command; uses Render API HTTP node)
- `youtube_shorts_automation_workflow_v3_blotato.json` — v3 (OpenRouter + Render API + Blotato publish to YouTube; uses env vars)
- `youtube_shorts_automation_workflow_v3_noenv_easysetup.json` — v3 no-env edition (edit keys once in first node)

## Import
In n8n: **Workflows → Import from file** and select the JSON.

## Required env vars (v2/v2.1/v3)
- `OPENROUTER_API_KEY`
- `REPLICATE_API_TOKEN`
- `ELEVENLABS_API_KEY`
- `ELEVENLABS_VOICE_ID`
- `TELEGRAM_CHAT_ID`
- `YOUTUBE_UPLOAD_WEBHOOK_URL` (used by v2/v2.1 uploader placeholder)
- `RENDER_API_URL` (required for v2.1/v3 render step)
- `BLOTATO_API_KEY` (required for v3)
- `BLOTATO_ACCOUNT_ID` (required for v3)

## Notes
- Workflows now use **OpenRouter** for script generation (`openai/gpt-4o-mini` by default).
- No Blotato dependency in v2; rendering is done with `ffmpeg`.
- `v3_noenv_easysetup` is easiest to start, but keys are stored inside the workflow node. Use env/credentials for production security.
