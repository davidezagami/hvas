# H.V.A.S.
<img alt="HVAS" height="40px" src="https://i.imgur.com/u2obU99.png" />

## Hora Video Analytic System

Try all the models at [app.horavision.ai](https://app.horavision.ai) by making a free account. See [here](https://github.com/davidezagami/hvas) for how to use the platform or the API.

The **Topic Extraction** model performs Image captioning by leveraging *Attention* mechanisms and a 9000+ words dictionary with Beam Search, which in the end produce a short description of the scene within the image or video.

The **NSFW Classification** model distinguishes between safe and unsafe images (or even video frames). In case of unsafe images, it specifies whether the content involves nudity, violence, or revealing clothing.

### Image tagging models

- **Image tagging**
  - Topic Extraction
  - NSFW Classification

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | METEOR |
| ------------------- | ------ | ------ | ----- | ---- |
| Topic Extraction | [Custom LSTM](https://arxiv.org/abs/1502.03044) | - |	-  | 35.6 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AVG Top-1 (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| NSFW Classification | EfficientNet | 6.38 |	28.07  | 92.3 |

#### Demo:

Topic Extraction:

| ![](https://i.imgur.com/2wMX6RF.gif) | ![](https://i.imgur.com/aZCvEvb.gif) |
| -------- | -------- |

NSFW Classification:

| ![](https://i.imgur.com/GbbzlYG.jpg) | ![](https://i.imgur.com/AkfYzof.jpg) |
| -------- | -------- |
| ![](https://i.imgur.com/fskKCjR.jpg) | ![](https://i.imgur.com/d2q4LLq.jpg) |

