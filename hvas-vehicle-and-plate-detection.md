
# H.V.A.S.
<img alt="HVAS" height="40px" src="https://i.imgur.com/u2obU99.png" />

## Hora Video Analytic System

Try all the models at [app.horavision.ai](https://app.horavision.ai) by making a free account. See [here](https://github.com/davidezagami/hvas) for how to use the platform or the API.

Vehicle and registration plate recognition models in Python using neural network architectures including Yolo and EfficientNet, as well as various features such as vehicle color and make.

### Vehicle Recognition models

- **Vehicle Detection**
  - Vehicle Color Recognition
  - Vehicle Make Recognition

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP @ [IoU=0.50:0.95] (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Vehicle Detection | Yolo v5 | 200.8   | 187.4 | 96.3 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AVG Top-1 (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Vehicle Color Recognition | EfficientNet | 8.33 |	32.15  | 95.3 |
| Vehicle Make Recognition | EfficientNet | 17.51 |	53.55  | 93.5 |

#### Demo:

Vehicle detection:

| 1 | 2 |
| -------- | -------- |
| ![](https://i.imgur.com/a8zrpow.gif)     |   ![](https://i.imgur.com/dVUzq2V.gif)     |


| Heatmap | Flowmap |
| -------- | -------- |
| ![](https://i.imgur.com/FrAFLfW.jpg)     | ![](https://i.imgur.com/PfVkOJ3.jpg)     |


Color and Make Recognition:

<img alt="HVAS" width="500px" src="https://i.imgur.com/3IvLTjy.jpg" />


### Registration Plates Recognition models

- **Registration Plates Detection**
  - Registration Plate Recognition

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP @ [IoU=0.50:0.95] (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Registration Plates Detection | Yolo v5 | 11.3   | 13.57 | 98.1 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | Accuracy |
| ------------------- | ------ | ------ | ----- | ---- |
| Registration Plate Recognition | ResNeXt-101 | 12.4 |	39.8  | 93.89 |

#### Demo:
<img alt="HVAS" width="500px" src="https://i.imgur.com/U8ppWgi.jpg" />
