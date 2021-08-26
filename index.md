---
layout: default
---

---
## Abstract
A novel one-shot voice-imitating TTS is proposed, which is able to synthesize audio with similar voice-style as reference voice. Also, the reference audio is  unseen during training.
- One-Shot Voice-Style-Transfer TTS
- Not relying on Speaker Embeding
- In addition to Pitch and Tone, the voice styles imitated include: Speed, Rhythm, Emotion

By **Rayn.li**@cloudminds
- - -

## Method
OneShot-TTS + WaveRNN
- - -
## Demo

#### *Reference*
<audio src="res/ref/qsy_src.wav" controls preload></audio>

#### *Synthesized*
|    |RTVC+GST  |OneShot-TTS|
|----| ---- | ---- |
|same text as reference|<audio src="res/rtvc/qsy_1.wav" controls preload></audio>|<audio src="res/adain/qsy_1.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/qsy_2.wav" controls preload></audio>|<audio src="res/adain/qsy_2.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/qsy_3.wav" controls preload></audio>|<audio src="res/adain/qsy_3.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/qsy_4.wav" controls preload></audio>|<audio src="res/adain/qsy_4.wav" controls preload></audio>|
- - -

#### *Reference*
<audio src="res/ref/mini_src.wav" controls preload></audio>

#### *Synthesized*
|    |RTVC+GST  |OneShot-TTS|
|----| ---- | ---- |
|same text as reference|<audio src="res/rtvc/mini_1.wav" controls preload></audio>|<audio src="res/adain/mini_1.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/mini_2.wav" controls preload></audio>|<audio src="res/adain/mini_2.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/mini_3.wav" controls preload></audio>|<audio src="res/adain/mini_3.wav" controls preload></audio>|
|arbitrary  text|<audio src="res/rtvc/mini_4.wav" controls preload></audio>|<audio src="res/adain/mini_4.wav" controls preload></audio>|