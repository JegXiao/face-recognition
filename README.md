# 人脸识别 | Face Detection

> 打开摄像头，用 OpenCV Haar 级联分类器实时检测画面中的正面人脸并标注绿框，按 `q` 退出。
> Opens your webcam and detects frontal faces in real time with OpenCV's Haar cascade classifier, drawing green boxes; press `q` to quit.

## 功能特性 | Features

- 摄像头实时检测（设备索引 0），逐帧标注 `Face` 绿框。
  Real-time detection on camera index 0, annotating each frame with a green `Face` box.
- 检测参数可调：`scaleFactor=1.1`、`minNeighbors=5`（在源码 `detectMultiScale` 处修改灵敏度）。
  Tunable parameters: `scaleFactor=1.1`, `minNeighbors=5` (edit `detectMultiScale` in the source to change sensitivity).
- Haar 模型文件（`haarcascade_frontalface_default.xml`）随 OpenCV 包自带，**无需额外下载**。
  The Haar model file ships with the OpenCV package — **no extra download needed**.

## 快速开始 | Quick Start

```bash
pip install -r requirements.txt
python 人脸识别.py
```

## 依赖 | Dependencies

- `opencv-python`（唯一第三方依赖）
  `opencv-python` (the only third-party dependency)
- 一个可用的摄像头 | A working webcam

## 说明 | Notes

- 这是人脸**检测**（框出人脸位置），不是人脸**识别**（辨认是谁）。
  This is face **detection** (locating faces), not face **recognition** (identifying who).
- 画面为本地窗口，**没有任何网络请求**，图像不会离开你的电脑。
  The preview is a local window with **no network requests** — frames never leave your machine.
