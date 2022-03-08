# H.V.A.S.
<img alt="HVAS" height="40px" src="https://i.imgur.com/u2obU99.png" />

## Hora Video Analytic System

Try all the models at [app.horavision.ai](https://app.horavision.ai) by making a free account. See [here](https://github.com/davidezagami/hvas) for how to use the platform or the API.

Text detection and recognition models, based on [PixelLink](https://arxiv.org/abs/1801.01315) architecture.

### Text Recognition models

- **Text Detection**
  - Text Recognition

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP @ [IoU=0.50:0.95] (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Text Detection | PixelLink | 33.9   | 39.22 | 96.7 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | Accuracy |
| ------------------- | ------ | ------ | ----- | ---- |
| Text Recognition | ResNeXt-101 + LSTM | 98.3 |	178.8  | 91.79 |

#### Demo:

![](https://i.imgur.com/GcYldV3.jpg)

