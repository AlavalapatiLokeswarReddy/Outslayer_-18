Duality AI – Offroad Semantic Scene Segmentation
Team ZeroDay

Transformer-based semantic segmentation for complex off-road environments using a DINOv2 Vision Transformer backbone.

📌 Project Overview

This project focuses on semantic scene segmentation in challenging off-road environments.
We leverage a self-supervised pretrained DINOv2 Vision Transformer (ViT-S/14) as a frozen backbone and train a custom convolutional decoder for accurate pixel-wise classification.

The system classifies each pixel into 10 semantic terrain/object classes, enabling robust perception for autonomous off-road navigation.

🚀 Key Features

✅ Transformer-based global feature extraction

✅ ConvNeXt-style segmentation head

✅ Combined CrossEntropy + Dice Loss

✅ IoU, Dice, Pixel Accuracy evaluation

✅ Training curve visualization

✅ Modular PyTorch training script

📊 Final Performance
Metric	Value
Best Epoch	29
Final Validation IoU	0.4952
Validation Dice Score	0.65
mAP@50	0.65
Validation Pixel Accuracy	0.80
🗂 Dataset Structure
Offroad_Segmentation_Training_Dataset/
├── train/
│   ├── Color_Images/
│   ├── Segmentation/
├── val/
│   ├── Color_Images/
│   ├── Segmentation/

10 semantic classes

Custom raw pixel-to-class mapping

🧠 Model Architecture
Backbone

DINOv2 ViT-S/14

Patch size: 14

Self-supervised pretrained

Frozen during training

Decoder

ConvNeXt-style convolutional head

GELU activation

Final 1×1 convolution for 10-class output

🏋️ Training Configuration

Optimizer: SGD (momentum = 0.9)

Learning Rate: 1e-4

Batch Size: 2

Epochs: 30

Loss Function:

Total Loss = CrossEntropy + 0.5 × Dice Loss
📦 Installation
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
pip install -r requirements.txt

Required libraries:

torch

torchvision

numpy

matplotlib

tqdm

opencv-python

pillow

▶️ Training

Update dataset paths inside train.py, then run:

python train.py

Outputs:

Trained model: segmentation_head.pth

Training curves: train_stats/

Evaluation metrics: evaluation_metrics.txt

🧪 Evaluation

Metrics computed:

IoU (Intersection over Union)

Dice Score

Pixel Accuracy

mAP@50

🔮 Future Improvements

Backbone fine-tuning

Multi-scale decoder

Class-weighted loss

Real-time optimization for deployment

👥 Team ZeroDay

A. Lokeswar Reddy (Team Leader)

K. Arun Kumar Reddy

C. Koushik Reddy

C. H. Shanmuka Padmanabha Reddy

📜 Declaration

This project is original work completed by Team ZeroDay.
Test images were not used during training or validation.
