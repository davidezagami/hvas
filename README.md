# H.V.A.S.
<img alt="HVAS" height="40px" src="https://i.imgur.com/u2obU99.png" />

## Table of Contents
- [Hora Video Analytic System](#Hora-Video-Analytic-System)
	- [Model list](#Model-list)
	- [Using the platform interface](#Using-the-platform-interface)
	    - [Creating a project](#Creating-a-project)
	    - [Drag and drop your files](#Drag-and-drop-your-files)
	- [Using the Rest API](#Using-the-Rest-API)

## Hora Video Analytic System

The app lives at [app.horavision.ai](https://app.horavision.ai).

Available models are as follows. The list follows the parent-child relationships for each network (a parent is usually a detection model, and its children are usually classifiers). Click on parent links to get more info about its entire "package".

### Model list

- [**Common Objects Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-common-objects-detection.md#common-objects-detection-model)

- [**Face Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-face-person-recognition.md#face-recognition-models)
  - Gender Detection
  - Age Estimation
  - Emotion Recognition
  - Head Orientation Estimation
  - Gaze Estimation
  - Face Recognition
  - Facial Landmarks Detection
  - More Facial Landmarks Detection
  - Face Mask Usage

- [**Person Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-face-person-recognition.md#person-recognition-models)
  - Person Clothing Recognition
  - Pose Estimation
  - Person Recognition

- [**Vehicle Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-vehicle-and-plate-detection.md#vehicle-recognition-models)
  - Vehicle Color Recognition
  - Vehicle Make Recognition

- [**Registration Plates Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-vehicle-and-plate-detection.md#registration-plates-recognition-models)
  - Registration Plate Recognition

- [**Road Recognition**](https://github.com/davidezagami/hvas/blob/main/hvas-road-recognition.md#road-recognition-maskrcnn-model)

- [**Car Damage Recognition**](https://github.com/davidezagami/hvas/blob/main/hvas-car-damage-recognition.md#car-damage-recognition-maskrcnn-model)

- [**Logo Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-logo-detection.md#logo-detection-model)

- [**Text Detection**](https://github.com/davidezagami/hvas/blob/main/hvas-text-recognition.md#text-recognition-models)
  - Text Recognition

- [**Image tagging**](https://github.com/davidezagami/hvas/blob/main/hvas-image-tagging.md#image-tagging-models)
  - NSFW Classification
  - Topic Extraction

- [**Video Colorization**](https://github.com/davidezagami/hvas/blob/main/hvas-video-colorization.md#video-colorization-model)

### Using the platform interface

#### Creating a project

Create a new project.

![](https://i.imgur.com/nzhyJEO.png)


Give your project a name and a description.

![](https://i.imgur.com/gnSG2xQ.png)

Select what kind of input you are going to use. Our models are optimized for each kind, so it matters if your video comes from a moving phone or from a security camera. For this example, we'll select **Handsfree**.

![](https://i.imgur.com/LsQo1md.png)

Select what model you want to use. Let's try **Logo Detection**.

![](https://i.imgur.com/cO4tf3q.png)

Check that all details are ok then hit Submit.

![](https://i.imgur.com/cMG0cHU.png)

#### Drag and drop your files

Drop a Video or an Image file to start the analysis, you can upload multiple files.

![](https://i.imgur.com/4Jniqdk.png)

You'll see your media being processed.

![](https://i.imgur.com/8723Cch.png)

When results are ready, you'll see a rendering of the analyzed image or video. For more details and statistics, hit **View**.

![](https://i.imgur.com/VszUX7k.png)


### Using the Rest API

![](https://i.imgur.com/Zb5h2n7.png)

Grab your `PROJECT_ID` and `PROJECT_API_KEY`, then start a new analysis with:

```bash=
curl --location --request POST 'https://app.horavision.ai/api/project/PROJECT_ID/analyses' \
    --header 'Authorization: Bearer PROJECT_API_KEY' \
    --form 'type="image"' \
    --form 'file=@"/path/to/file.jpg"'
```

Response:

```json
{
    "user_id": 15,
    "project_id": 126,
    "type": "image",
    "file_name": "file.jpg",
    "file_url": null,
    "skip_render": false,
    "uuid": "ANALYSIS_ID",
    "updated_at": "2022-01-20T10:47:46.406171Z",
    "created_at": "2022-01-20T10:47:43.718091Z",
    "id": 375140,
    "filemime": "image\\/jpeg",
    "filesize": 1523348,
    "frames": 1,
    "framerate": 1,
    "cost": 1,
    "execution_time_in_seconds": 2.688,
    "state": "READY",
    "video_duration": 0,
    ...
}
```

Grab the `ANALYSIS_ID` from the `uuid` field then get the results of the analysis with:

```bash=
curl -X GET -G "https://app.horavision.ai/api/projects/PROJECT_ID/analyses/ANALYSIS_ID/collect" \
    -H "Authorization: Bearer PROJECT_API_KEY"
```

Response:

```json
{
    "fps": "1",
    "frames": 1,
    "created_at": "2022-01-20 11:47:43",
    "updated_at": "2022-01-20 11:48:25",
    "output": [
        {
            "ts": "2022-01-20T10:47:54.237486+00:00",
            "FBM0RO": {
                "face-detection": {
                    "bounding_box": {
                        "x": 3533,
                        "y": 1706,
                        "w": 97,
                        "h": 139,
                        "class": "face",
                        "conf": 0.8661545991897583
                    }
                }
            },
            "F22LUM": {
                "face-detection": {
                    "bounding_box": {
                        "x": 2728,
                        "y": 1255,
                        "w": 79,
                        "h": 120,
                        "class": "face",
                        "conf": 0.9443729758262634
                    }
                }
            }
        }
    ]
}
```

Find more details and code snippets in various languages at https://app.horavision.ai/documentation
