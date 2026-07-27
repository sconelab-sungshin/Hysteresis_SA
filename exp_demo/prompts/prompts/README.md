# Image Generation Prompt Files

This folder contains JSON-format prompts used to generate visual stimuli for the Hysteresis_SA project.

## Files

### `face_image_prompt.json`

This file contains JSON prompts used to generate facial expression transition stimuli.

The prompts are organized by expression version:

- `happy_version`: prompt used to generate happy-expression images from a neutral reference face.
- `angry_version`: prompt used to generate angry-expression images from a neutral reference face.

The generated facial expression stimuli are intended to form a continuous transition sequence from happy expression to neutral expression to angry expression.

Each face stimulus set consists of 41 frames:

- `frame_001` to `frame_020`: happy-expression frames
- `frame_021`: neutral-expression frame
- `frame_022` to `frame_041`: angry-expression frames

The frame order is designed so that the sequence can be presented in either direction during the jsPsych demo:

- `happy_to_angry`: `frame_001` → `frame_041`
- `angry_to_happy`: `frame_041` → `frame_001`

---

### `scene_image_prompt.json`

This file contains JSON prompts used to generate scene category transition stimuli.

The prompts are organized by scene version:

- `living_room_version`: prompt used to generate living-room endpoint or living-room-dominant transition images.
- `bedroom_version`: prompt used to generate bedroom endpoint or bedroom-dominant transition images.

The generated scene stimuli are intended to form a continuous transition sequence between indoor scene categories while preserving category-irrelevant visual features, such as:

- camera angle
- viewpoint
- room layout
- lighting
- wall and floor appearance
- overall visual style

These prompts are included for documentation and reproducibility of the stimulus generation process.

## Notes

The JSON files are not directly used by the jsPsych experiment code.  
They are documentation files that record how the AI-generated stimuli were produced.
