---
layout: default
---

## Unet-TTS: Improving Unseen Speaker and Style Transfer in One-shot Voice Cloning
Email: rayn.li@cloudminds.com

## Abstract
One-shot voice cloning aims to transform speaker voice and speaking style in speech synthesized from a text-to-speech (TTS) system, where only a shot recording from the target speech can be used. Out-of-domain transfer is still a challenging task, and one important aspect that impacts the accuracy and similarity of synthetic speech is the conditional representations carrying speaker or style cues extracted from the limited references. In this paper, we present a novel one-shot voice cloning algorithm called Unet-TTS that has good generalization ability for unseen speakers and styles. Based on a skip-connected U-net structure, the new model can efficiently discover speaker-level and utterance-level spectral feature details from the reference audio, enabling accurate inference of complex acoustic characteristics as well as imitation of speaking styles into the synthetic speech. According to both subjective and objective evaluations of similarity, the new model outperforms both speaker embedding and unsupervised style modeling approach (GST) on an unseen emotional corpus. 




## Note
We tentatively show arbitrary text speech synthesized using our colleague's voice as a reference. We will update soon with more samples of the emotional transfer studied in the paper.

## Demo

- arbitrary text 1: 达闼科技是一家云端智能机器人运营商，达闼科技正为各行业客户提供专业的机器人运营服务
- arbitrary text 2: 十年生死两茫茫，不思量自难忘
- arbitrary text 3: 本音频由一句话风格迁移语音合成系统合成

#### *Reference-1*
请问台湾居民能否使用旅游签证乘坐国内航班

<audio src="res/colleague/ref/qsy_src.wav" controls preload></audio>

|    DEMO-1        | GST-Tacotron | Unet-TTS |
|:---------------: |:------------------:|:--------------:|
| same text as ref | <audio src="res/colleague/rtvc/qsy_1.wav" controls preload></audio> | <audio src="res/colleague/adain/qsy_1.wav" controls preload></audio> |
| arbitrary text 1   | <audio src="res/colleague/rtvc/qsy_2.wav" controls preload></audio> | <audio src="res/colleague/adain/qsy_2.wav" controls preload></audio> |
| arbitrary text 2  | <audio src="res/colleague/rtvc/qsy_3.wav" controls preload></audio> | <audio src="res/colleague/adain/qsy_3.wav" controls preload></audio> |
| arbitrary text 3  | <audio src="res/colleague/rtvc/qsy_4.wav" controls preload></audio> | <audio src="res/colleague/adain/qsy_4.wav" controls preload></audio> |



#### *Reference-2*
产业园这是一个第一期的这个，第一期的这个，建筑面积应该是两百四十三亩

<audio src="res/colleague/ref/mini_src.wav" controls preload></audio>

|    DEMO-2        | GST-Tacotron | Unet-TTS |
|:---------------: |:------------------:|:--------------:|
| same text as ref | <audio src="res/colleague/rtvc/mini_1.wav" controls preload></audio> | <audio src="res/colleague/adain/mini_1.wav" controls preload></audio> |
| arbitrary text 1  | <audio src="res/colleague/rtvc/mini_2.wav" controls preload></audio> | <audio src="res/colleague/adain/mini_2.wav" controls preload></audio> |
| arbitrary text 2  | <audio src="res/colleague/rtvc/mini_3.wav" controls preload></audio> | <audio src="res/colleague/adain/mini_3.wav" controls preload></audio> |
| arbitrary text 3  | <audio src="res/colleague/rtvc/mini_4.wav" controls preload></audio> | <audio src="res/colleague/adain/mini_4.wav" controls preload></audio> |
