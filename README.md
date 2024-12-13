
# MRI Brain Tumor Segmentation using YOLOv7

![MRI Brain Tumor Segmentation](images/result1.png)

## Overview

This project aims to segment brain tumors in MRI images using YOLOv7, a state-of-the-art object detection algorithm. The segmentation of tumors in MRI scans plays a crucial role in early diagnosis and treatment planning for patients with brain tumors. By leveraging deep learning techniques, this project automates the process of tumor detection, enabling efficient and accurate identification of tumor regions in MRI scans.

## Key Features

- **YOLOv7 Object Detection**: Utilizes the YOLOv7 architecture for fast and accurate detection of brain tumors in MRI images.
- **Custom Dataset Training**: Trained the YOLOv7 model on a custom MRI dataset comprising annotated brain tumor images.
- **Tumor Segmentation**: After inferencing the model, it accurately segments tumor regions in MRI scans, providing valuable insights for medical diagnosis and treatment.
- **Efficient and Scalable**: The YOLOv7 model offers high efficiency and scalability, making it suitable for real-time tumor detection applications.

## Usage

### Installation

1. Clone the repository:
   git clone https://github.com/rahimnadan/mri_brain_tumor_segmentation.git

### Training

1. Prepare the custom MRI dataset with annotated tumor regions.
2. Modify the YOLOv7 configuration file (`yolov7.yaml`) according to your dataset specifications.
3. Train the YOLOv7 model using the following command:
python train.py --img 640 --batch 16 --epochs 50 --data custom_data.yaml --weights yolov7.pt --cache

### Inference

1. After training, run inference on MRI images to detect and segment brain tumors:
python detect.py --source /path/to/mri/images --weights runs/train/exp/weights/best.pt --img-size 640 --save-txt --save-conf

## Results

![MRI Tumor Segmentation Result](images/result2.png)

## Acknowledgments

Special thanks to the contributors of the YOLOv7 implementation and the creators of the custom MRI dataset used in this project.

