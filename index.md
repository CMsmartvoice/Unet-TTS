---
layout: default
---

## Unet-TTS: Improving Unseen Speaker and Style Transfer in One-shot Voice Cloning
Email: rayn.li@cloudminds.com

Our proposed algorithm has powerful speaker and style transfer capabilities, especially excellent imitation of out-of-domain emotions.

- No fine-tuning required, just a few seconds of target audio
- Synthesize arbitrary text
- Embedding pause, stess, and other speaking styles in speech

[Code](https://github.com/CMsmartvoice/One-Shot-Voice-Cloning)

[Colab notebook](https://colab.research.google.com/drive/1sEDvKTJCY7uosb7TvTqwyUdwNPiv3pBW?usp=sharing)

[Paper link](https://arxiv.org/abs/2109.11115)

## Abstract
One-shot voice cloning aims to transform speaker voice and speaking style in speech synthesized from a text-to-speech (TTS) system, where only a shot recording from the target speech can be used. Out-of-domain transfer is still a challenging task, and one important aspect that impacts the accuracy and similarity of synthetic speech is the conditional representations carrying speaker or style cues extracted from the limited references. In this paper, we present a novel one-shot voice cloning algorithm called Unet-TTS that has good generalization ability for unseen speakers and styles. Based on a skip-connected U-net structure, the new model can efficiently discover speaker-level and utterance-level spectral feature details from the reference audio, enabling accurate inference of complex acoustic characteristics as well as imitation of speaking styles into the synthetic speech. According to both subjective and objective evaluations of similarity, the new model outperforms both speaker embedding and unsupervised style modeling (GST) approaches on an unseen emotional corpus.

![](./pics/structure.png)

## Demo (One-shot Unseen Emotion Transfer)

**Model Description:**  
**Unet-TTS** - Our proposed model  
**GST** - Tacotron with unsupervised style modeling of GST  
**SpkEmbed** - Tacotron with speaker embedding  

These reference emotion speech to be transferred are unseen in the training process.

## 1. Same Text as Reference

#### Neutral
- ????????????????????????????????? <audio src="res/test/parallel/neutral01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/neutral01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/neutral01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/neutral01_spk.wav" controls preload></audio> |

- ??????????????????????????????????????? <audio src="res/test/parallel/neutral02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/neutral02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/neutral02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/neutral02_spk.wav" controls preload></audio> |

#### Angry
- ??????????????????????????????????????? <audio src="res/test/parallel/angry01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/angry01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/angry01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/angry01_spk.wav" controls preload></audio> |

- ?????????????????????????????????????????? <audio src="res/test/parallel/angry02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/angry02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/angry02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/angry02_spk.wav" controls preload></audio> |

#### Surprise
- ?????????????????????????????????????????? <audio src="res/test/parallel/surprise01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/surprise01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/surprise01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/surprise01_spk.wav" controls preload></audio> |

- ?????????????????????????????????????????? <audio src="res/test/parallel/surprise02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/surprise02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/surprise02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/surprise02_spk.wav" controls preload></audio> |

#### Happy
- ??????????????????????????????????????? <audio src="res/test/parallel/happy01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/happy01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/happy01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/happy01_spk.wav" controls preload></audio> |

- ????????????????????????????????? <audio src="res/test/parallel/happy02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/happy02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/happy02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/happy02_spk.wav" controls preload></audio> |

#### Sad
- ?????????????????????????????????????????? <audio src="res/test/parallel/sad01_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/sad01_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/sad01_gst.wav" controls preload></audio> | <audio src="res/test/parallel/sad01_spk.wav" controls preload></audio> |

- ?????????????????????????????????????????? <audio src="res/test/parallel/sad02_gt.wav" controls preload></audio>

|    Unet-TTS      |      GST     |    SpkEmbed    |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/parallel/sad02_unet.wav" controls preload></audio>  | <audio src="res/test/parallel/sad02_gst.wav" controls preload></audio> | <audio src="res/test/parallel/sad02_spk.wav" controls preload></audio> |


## 2. Arbitrary Text (AT)
**(The text of the reference is the same as above)**

#### Neutral
- AT1: ???????????????????????????????????????
- AT2: ???????????????????????????????????????

|    Reference     |   Unet-TTS   |       GST      |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/non-parallel/neutral01_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/neutral01_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/neutral01_gst.wav" controls preload></audio> |
| <audio src="res/test/non-parallel/neutral02_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/neutral02_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/neutral02_gst.wav" controls preload></audio> |

#### Angry
- AT1: ?????????????????????????????????????????????????????????
- AT2: ??????????????????????????????

|    Reference     |   Unet-TTS   |       GST      |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/non-parallel/angry01_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/angry01_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/angry01_gst.wav" controls preload></audio> |
| <audio src="res/test/non-parallel/angry02_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/angry02_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/angry02_gst.wav" controls preload></audio> |

#### Surprise
- AT1: ?????????????????????????????????
- AT2: ?????????????????????????????????

|    Reference     |   Unet-TTS   |       GST      |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/non-parallel/surprise01_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/surprise01_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/surprise01_gst.wav" controls preload></audio> |
| <audio src="res/test/non-parallel/surprise02_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/surprise02_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/surprise02_gst.wav" controls preload></audio> |

#### Happy
- AT1: ?????????????????????????????????
- AT2: ???????????????????????????

|    Reference     |   Unet-TTS   |       GST      |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/non-parallel/happy01_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/happy01_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/happy01_gst.wav" controls preload></audio> |
| <audio src="res/test/non-parallel/happy02_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/happy02_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/happy02_gst.wav" controls preload></audio> |

#### Sad
- AT1: ??????????????????????????????
- AT2: ???????????????????????????????????????

|    Reference     |   Unet-TTS   |       GST      |
|:---------------: |:------------:|:--------------:|
| <audio src="res/test/non-parallel/sad01_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/sad01_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/sad01_gst.wav" controls preload></audio> |
| <audio src="res/test/non-parallel/sad02_gt.wav" controls preload></audio>  | <audio src="res/test/non-parallel/sad02_unet.wav" controls preload></audio> | <audio src="res/test/non-parallel/sad02_gst.wav" controls preload></audio> |

## 3. Other
- Ref1: ?????????????????????????????????
- Ref2: ???????????????????????????????????????
- Ref3: ??????????????????????????????????????????????????????????????????????????????????????????????????????
- Ref4: ????????????????????????????????????????????????????????????

- AT: ?????????????????????????????????????????????????????????

|    Description   |   Reference  |    Unet-TTS    |
|:---------------: |:------------:|:--------------:|
| Pause style | <audio src="res/other/pause_gt.wav" controls preload></audio>  | <audio src="res/other/pause_unet.wav" controls preload></audio>  |
| Stress style | <audio src="res/other/stress_gt.wav" controls preload></audio>  | <audio src="res/other/stress_unet.wav" controls preload></audio>  |
| PC Recording | <audio src="res/other/mini_gt.wav" controls preload></audio>  | <audio src="res/other/mini_unet.wav" controls preload></audio>  |
| Phone recording | <audio src="res/other/qsy_gt.wav" controls preload></audio>  | <audio src="res/other/qsy_unet.wav" controls preload></audio>  |
