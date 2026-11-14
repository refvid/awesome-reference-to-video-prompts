---
name: reference-to-video-prompts
description: Write prompts for reference-to-video AI models (Kling, Seedance, Wan, Vidu) that keep the same person, pet or product in every shot. Use when someone wants a consistent-character or product video from reference photos, or asks for a multi-shot video prompt.
---

# Reference-to-video prompts

A reference-to-video model takes 1–10 photos per subject and a prompt. The photos carry who or what it is; the prompt carries what happens.

## How to write one

1. Ask what the subject is (person, pet, product, thing) and how many subjects; give each a slot `[1]`, `[2]`, matching the order of the photo sets.
2. Never re-describe the subject's looks in words — write `[1]` and let the photos decide. Describe clothes or setting only when they should change.
3. Write 2–3 shots, one line each: setting, one action, camera (wide, close-up, tracking, from behind, slow push-in). Write them as `Shot 1: …`.
4. Products: one product per photo set, plain-background photos, a shot that shows it in use and a final hero shot.
5. Say the length (5–10 s) and ratio (9:16 for Shorts/Reels/TikTok, 16:9 for YouTube, 1:1 for feeds); add sound only if the model supports it.

## Examples

Every tested prompt is in [`prompts.json`](../../prompts.json) (71 entries: subjects, shots, model, seconds, ratio, photo tips). Pick the closest one, keep its structure, change the setting and action. For instance:

- Road Trip (person): `Shot 1: A vintage convertible drives along a sunny coastal road; [1] at the wheel and [2] in the passenger seat laugh, hair blowing in the wind. Wide tracking s…`
- Birthday Greeting (person): `Medium close-up of [1] in a cosy living room holding a small cake with lit candles toward the camera, then smiling and saying warmly: "Happy birthday! I hope th…`
- Cinematic Drive (product): `Shot 1: Low tracking shot alongside [1] as it drives along a winding coastal road at golden hour, the sea and cliffs behind, sunlight flaring off the paint.…`

To generate without setting up a model, each entry's `url` opens it as a template on [RefVid](https://refvid.com).
