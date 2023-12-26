# Ultralytics (CPU) Object Detection

[Ultralytics](https://ultralytics.com)'s [YOLO CLI](https://docs.ultralytics.com/quickstart/#use-ultralytics-with-cli) allows convenient execution of object detection on images and videos.

## ⚙️ Usage

First, open the project in [GitHub Codespaces](https://codespaces.new/?template_repository=bystefankuehnel/ultralytics). Then, follow the steps below.

> **Note**: GitHub Codespaces are free for a limited time (180 hours). When not in use, an active Codespace should be stopped or deleted.

### Steps

#### 1. Downloading a Video

Use `yt-dlp` to retrieve a video from YouTube or a supported source. In the example, a video named `cars.mp4` is downloaded:

```sh
yt-dlp -o cars.mp4 https://youtu.be/CftLBPI1Ga4
```

> **Note**:  Alternatively, a local video can be uploaded via Drag & Drop.

#### 2. Running YOLO Object Detection

Use `yolo` to perform object detection on the video `cars.mp4`:

```sh
yolo predict model=yolov8n-seg.pt source='cars.mp4'
```

> **Note**: The _annotated_ video file is located in the `/runs/predict/predict{n}/` folder.

**Options**:

- `model`: Specifies the YOLO model for object detection. For a list of available models, see [here](https://github.com/ultralytics/ultralytics#models).
- `source``: Specifies the video source, which can be an image or video file.

## 👷‍ Error Found?

Thank you for your message! Please fill out a [bug report](../../issues/new?assignees=&labels=&template=bug_report.md&title=).

## License

This project is licensed under the [European Union Public License 1.2](https://choosealicense.com/licenses/eupl-1.2/).
