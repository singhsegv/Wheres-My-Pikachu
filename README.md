# Pikachu Detection Squad 🕵️‍♂️⚡

<img src="thumbnail.png" alt="Where's My Pikachu?" width="800"/>

## Overview

Welcome to the ultimate showdown of Computer Vision vs. Pikachu! As I zigzag through the electrifying path of Computer Vision, I've decided to tackle the most shocking challenge first - detecting Pikachu in the wild (and in pictures, because let's be honest, the wild is hard to come by).

## Mission Statement

To develop and refine computer vision models capable of spotting the electrifying presence of Pikachu. Why Pikachu, you ask? Because if you can detect an electric-type Pokémon adept at camouflaging itself in various environments (and occasionally in Ash Ketchum's arms), what can't you detect?

Since there are a lot of mature frameworks available for computer vision tasks by great teams such as Ultralytics, Meta, Google, etc, this repository acts as a central place to learn how to work with these with a common goal of training them to work with my custom dataset.

## Current Progress

- [x] **Phase 1**: Learning how to not electrocute myself while plugging in my GPU.
- [x] **Phase 2**: Collecting a dataset of Pikachu images and labelling them.
- [ ] **Phase 3**: Training models to detect Pikachus.
- [ ] **Final Phase**: World domination (or at least, winning a local Pokémon Go contest).

## Implementations

| Framework                                                          |         Task          | Architecture |
| ------------------------------------------------------------------ | :-------------------: | :----------: |
| [Ultralytics YOLOv8](./ultralytics_yolov8/segmentation/) (WIP)     |   Object Detection    |     YOLO     |
| [Ultralytics YOLOv8](./ultralytics_yolov8/segmentation/) (WIP)     | Semantic Segmentation |     YOLO     |
| [Tensorflow Object Detection API](./tf_od_api/segmentation/) (WIP) |   Object Detection    | Faster RCNN  |
| [Tensorflow Object Detection API](./tf_od_api/segmentation/) (WIP) | Semantic Segmentation |  Mask RCNN   |
| Meta Detectron2 (WIP)                                              |         Lorem         |    Ipsum     |
| Meta SAM (WIP)                                                     |         Lorem         |    Ipsum     |

## Todo

- [ ] Add the code for ultralytics YOLO experiments
- [ ] Compare different model sizes of YOLO
- [ ] Add the code for tensorflow object detection API experiments
- [ ] Explore Meta's Segment Anything Model (SAM)
- [ ] Explore Meta's Detectron2
- [ ] Multi class examples (Where's My Pikachu and Ash?)

## How You Can Help

- **Contribute Pikachu Images:** Got a Pikachu photo? Is it high quality, low quality, or just right for training a neural network? Head over to the dataset folder to read the process that I followed for labeling images. You can help increase the pikachus in the dataset.
- **Code Contributions:** If you're skilled in the art of computer vision or just want to learn alongside me, your pull requests are more than welcome.
- **Suggestions:** Are there some frameworks/tools that you use at your workplace? Create an issue about the tools you'd like me to train on custom data.

## Disclaimer

This project is for educational purposes and a personal challenge on my journey to deepen my computer vision knowledge. It's also a testament to my love for Pokémon. Please use it responsibly and don't try to catch actual Pikachu with it. They don't like it.
