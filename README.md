# Task 6: Constructing and Evaluating Synthetic Media

> ⚠️ **SYNTHETIC MEDIA DISCLOSURE**: Every audio/video file in this repository is AI-generated. No real person's voice or likeness was used without consent. The narration script is derived from a real LLM-generated analysis I produced and verified in Task 5.

## Project description
This repo takes the "coach advisory" narrative I generated and fact-checked in Task 5 (Syracuse Women's Lacrosse dataset) and converts it into synthetic audio and video using free, accessible AI tools, to explore what current synthetic-media generation can and can't do convincingly — and whether it can fool a detector built to catch it.

## Source material
- `script.txt` — narration script, condensed from the Task 5 "coach question" answer (Q7 in `Prompt_and_Response.pdf`, [Task 5 repo](https://github.com/AmulyaWalimbe/Task-04-05---Ground-Truth-to-LLM-Judgment))

## Artifacts
| File | Tool(s) | Notes |
|---|---|---|
| `artifact1_coach_narrative_AI_VOICE_elevenlabs.mp3` | ElevenLabs (free tier) | Voice: Roger — Laid-Back, Casual, Resonant. Model: Eleven Multilingual v2 |
| `artifact2_coach_narrative_AI_VIDEO_did_lovo.mp4` | LOVO (audio) + D-ID (video/avatar) | Audio: Jenny (Female, US English), default settings. Video: D-ID avatar "Amber," sentiment set to Professional |

## How to reproduce
1. Read `script.txt`
2. Paste into ElevenLabs (free tier) using a stock voice → export mp3
3. For the video: paste the same script into LOVO to generate a second audio track → upload that audio into D-ID, select a stock avatar, generate the lip-synced video
4. Label all outputs clearly as AI-generated in the filename, per the convention above

## What I learned
The most surprising finding was that a purpose-built voice deepfake detector (deepfakedetection.io) scored the ElevenLabs audio 95% "Likely Authentic" — fully synthetic speech, misclassified as a real human recording, with a confident explanation to back it up. That gap between how convincing generation has become and how reliable free detection tools actually are was the biggest takeaway from this task. On the construction side, voice quality varied far more across tools than video quality did: ElevenLabs was consistently the most natural-sounding artifact, while the video's technical mechanics (lip-sync accuracy, blinking) held up well, but was let down by the flatter LOVO voice track, a slight voice/avatar personality mismatch, and avatar body motion that read as more mechanical than human. I also learned, somewhat frustratingly, that several tools marketed as "free" (TTSMaker, Murf.ai) gate the actual file download behind a paid upgrade — a hygiene issue worth knowing about before committing time to a tool.

## Files in this repo
- `script.txt` — narration script
- `artifact1_coach_narrative_AI_VOICE_elevenlabs.mp3` — synthetic audio, ElevenLabs
- `artifact2_coach_narrative_AI_VIDEO_did_lovo.mp4` — synthetic video, D-ID avatar driven by LOVO audio
- `process log.pdf` — tools, versions, settings, iteration notes, time spent
- `evaluation.pdf` — critical evaluation of each artifact + detection/provenance check
- `screenshots/` — tool settings screenshots and detection report screenshots
- `README.md` — this file
