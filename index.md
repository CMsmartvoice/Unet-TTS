---
layout: default
---

## Unet-TTS: Improving Unseen Speaker and Style Transfer in One-shot Voice Cloning
Email: rayn.li@cloudminds.com

## Abstract
One-shot voice cloning aims to transform speaker voice and speaking style in speech synthesized from a text-to-speech (TTS) system, where only a shot recording from the target speech can be used. Out-of-domain transfer is still a challenging task, and one important aspect that impacts the accuracy and similarity of synthetic speech is the conditional representations carrying speaker or style cues extracted from the limited references. In this paper, we present a novel one-shot voice cloning algorithm called Unet-TTS that has good generalization ability for unseen speakers and styles. Based on a skip-connected U-net structure, the new model can efficiently discover speaker-level and utterance-level spectral feature details from the reference audio, enabling accurate inference of complex acoustic characteristics as well as imitation of speaking styles into the synthetic speech. According to both subjective and objective evaluations of similarity, the new model outperforms both speaker embedding and unsupervised style modeling (GST) approaches on an unseen emotional corpus.

## Demo

**Unet-TTS** - Our proposed model
**GST** - Tacotron with unsupervised style modeling of GST
**SpkEmbed** - Tacotron with speaker embedding

### 1. Same Text as Reference

#### Neutral
- 七十六万八千四百四十四
<audio src="res/test/parallel/neutral01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/neutral01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/neutral01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/neutral01_spk.wav" controls preload></audio> |

- 希望以后找个老师好好学一下
<audio src="res/test/parallel/neutral02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/neutral02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/neutral02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/neutral02_spk.wav" controls preload></audio> |

### 2. Arbitrary Text