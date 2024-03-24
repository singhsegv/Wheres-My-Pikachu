# Pikachu Dataset

This directory contain Pikachus. Lots and lots of pikachus from different internet sources, youtube videos, etc, in a lot of different backgrounds. To train a neural network to find pikachus, you need to give it a lot of pikachus with labelled bounding boxes or segmented pixels.

Most of the frameworks (Ultralytics YOLO, Detectron2, etc) will require moving the dataset in their own sub-directory for ease of use. So, the sole purpose of this directory is to provide a way to explore the complete dataset while each of the implementation sub-directory will have instructions about how to get data for its own training purposes.

There are two folders, `detection` and `segmentation` each with a `training.dvc` and `validation.dvc` file to download the respective images and labels. Further sections will desribe how to fetch the images and labels to your local environment and use the provided `jupyter notebook` to visualize them.

For now, both the detection and segmentation labels are in `YOLO format` since that was the first library I started digging into, I might add scripts to transform the labels into other formats in the future.

## Sample Images

### Bounding Boxes

<div style="text-align:center">
<img src="./figures/detection_bbox_sample.png" alt="Dataset samples with bounding boxes" width="800"/>
</div>

### Segmented Pixel (Closed Polygons)

<div style="text-align:center">
<img src="./figures/segmentation_labels.png" alt="Dataset samples with segmented pixels" width="800"/>
</div>

## How to get the data

The data is stored on my dagshub repo [here](https://dagshub.com/iamrajdeep1008/Wheres-My-Pikachu) and is maintained using [dvc](https://dvc.org/) for ease of use and to keep the repository's size small. To fetch the data, first do a `pip install dvc dvc-s3` and then from the `./dataset/detection` or `./dataset/segmentation` directory of the project, run this command:

```
dvc pull
```

After that you can refer to `eda.ipynb` notebook from the respective directory which will let you through the process of loading images and using the bounding box labels for exploratory data analysis purposes.

## Data Statistics

This dataset contain approximately **208 images** (segmentation one has a little less than 208) with corresponding labels in YOLO data format (refer to [this](https://albumentations.ai/docs/getting_started/bounding_boxes_augmentation/#yolo) to know more about this format if this is new to you). The images were labelled using [LabelStudio](https://labelstud.io/) and pictures can have more than 1 label since there are a few images with a lot of pikachus in them.

They are split into 2 folders, `training` and `validation`, each containing `images` and `labels` folders. A 80:20 split is done for **Training** and **Validation**.

## Additional comments about the Data

- Most of the bounding boxes look a lot bigger than pikachu's body. This is due to the fact that pikachus have a long tail attached to them and we definitely don't want our models to recognize tailless pikachus.
- In a lot of images, when a pikachu is using `Thunderbolt` or `Irontail` attack, the body or the tail looks very bright.
- Since this dataset is small, I'll strongly suggest using image augmentation while working.

## Disclaimer

I do not own any of the images included in this collection. All images are the property of their respective owners. The collection and labeling of these images have been done for personal use only, without any intention of copyright infringement or commercial benefit.
