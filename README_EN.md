# Road Damage Detection using YOLOv5

Limited research has been conducted on the effectiveness of the advanced Road Damage Dataset (RDD) 2022, which encompasses road damage data from six nations: Japan, Norway, the United States, the Czech Republic, and China. RDD 2022 includes four common types of road damage: vertical cracks, horizontal cracks, alligator cracks, and potholes. This project presents a deep neural network model for road damage detection in photographic representations of road surfaces.

## Model Architecture and Enhancements

The model is built upon the YOLOv5 object detection framework and has been tailored to road damage detection. It incorporates several techniques to enhance accuracy and generalization performance:

- Efficient Channel Attention (ECA-Net): This module helps in capturing and emphasizing relevant features.
- Label Smoothing: Introducing label smoothing techniques to improve model robustness.
- K-means++ Algorithm: Utilizing K-means++ for improved anchor box initialization.
- Focal Loss: Employing Focal loss to address class imbalance and improve training.
- Additional Prediction Layer: Adding an extra prediction layer for refined results.

The model achieved a significant improvement of 1.9% in mean average precision (mAP) and 1.29% in F1-Score compared to YOLOv5s, with a minor increase of 1.1 million parameters. Additionally, the model showcases a 0.11% improvement in mAP and 0.05% in F1-Score compared to YOLOv8s, while utilizing 3 million fewer parameters and 12 Gigabytes fewer GFLOPs.

## Installation and Usage

1. Clone the repository:
   ```bash
   $ git clone https://github.com/YourUsername/YourRepository.git
   $ cd YourRepository
## Install required dependencies:
$ pip install -r requirements.txt
## Training:
$ python train.py --data xyz.yaml --cfg configs/yolov5/yolov5s.yaml
## Inference:
$ python detect.py --source 0  # webcam
                  img.jpg    # image
                  vid.mp4    # video
                  path/      # directory
                  path/*.jpg  # glob
## Acknowledgements

Special acknowledgment to YOLOAir for inspiring and supporting this project's development.

---
