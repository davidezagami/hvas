# H.V.A.S.
<img alt="HVAS" height="40px" src="https://i.imgur.com/u2obU99.png" />

## Hora Video Analytic System

Try all the models at [app.horavision.ai](https://app.horavision.ai) by making a free account. See [here](https://github.com/davidezagami/hvas) for how to use the platform or the API.

Face and person recognition models in Python using neural network architectures including Yolo and EfficientNet, as well as various features such as gender, age, head and body pose, gaze estimation, landmarks, mask usage and clothing. These models can detect more faces quicker than Google Cloud, Amazon Rekognition, and Azure Vision.

### Face Recognition models

- **Face Detection**
  - Gender Detection
  - Emotion Recognition
  - Age Estimation
  - Head Orientation Estimation
  - Gaze Estimation
  - Facial Landmarks Detection
  - More Facial Landmarks Detection
  - Face Mask Usage
  - Face Recognition

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP @ [IoU=0.50:0.95] (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Face Detection | Yolo v5 | 29.4   | 20.0 | 98.7 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AVG Top-1 (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Gender Detection | EfficientNet | 3.76 |	14.14  | 98.3 |
| Emotion Recognition | EfficientNet | 4.22 |	19.33  | 72.3 |
| Face Mask Usage | EfficientNet | 2.85 |	8.41  | 99.4 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | MAE / MNE |
| ------------------- | ------ | ------ | ----- | ---- |
| Age Estimation | MobileNet | 0.76 | 4.14  | 5.5 |
| Head Orientation Estimation | SimpleCNN |  	0.210    | 3.82   | 7.1 |
| Gaze Estimation | SimpleCNN | 	0.268    | 3.77  | 6.2 |
| Facial Landmarks Detection | SimpleCNN | 0.056     | 1.76   | 0.11 |
| More Facial Landmarks Detection | SimpleCNN | 0.142     | 4.25   | 0.56 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | LFW |
| ------------------- | ------ | ------ | ----- | ---- |
| Face Recognition | MobileNet V2 | 5.88  | 11.07  | 0.9832 |

#### Demo:
![](https://i.imgur.com/zXjWbGd.gif)

### Person Recognition models

- **Person Detection**
  - Person Clothing Recognition
  - Pose Estimation
  - Person Recognition

#### Performance

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP @ [IoU=0.50:0.95] (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Person Detection | EfficientDet | 22.4   | 16.4 | 98.1 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AVG Top-1 (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Person Clothing Recognition | EfficientNet | 13.66 |	51.64  | 90.5 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | AP (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Pose Estimation | MobileNet V2 | 50.25  | 23.16   | 79.0 |

| Model  | Arch | Complexity (GFLOPs) | Size (Mp) | mAP (%) |
| ------------------- | ------ | ------ | ----- | ---- |
| Person Recognition | MobileNet V2 | 4.01  | 5.10  | 96.2 |

#### Demo:
![](https://i.imgur.com/eTHYmQ4.gif)

### Comparison with Google Cloud, AWS Rekognition, and Azure Vision

#### Google Cloud
Face count: 51
![](https://i.imgur.com/iYYHyz8.png)

#### AWS Rekognition
Face count: 92
![](https://i.imgur.com/sS6v3qL.jpg)

#### Azure Vision
Face count: 103
![](https://i.imgur.com/L9Upskh.jpg)

#### HoraVision
Face count: 176
![](https://i.imgur.com/hyUE5pH.jpg)
