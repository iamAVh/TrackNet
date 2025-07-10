# 🎾 TrackNet - Tennis Ball Tracking from Broadcast Videos

This is a deep learning-based project to track tennis balls from broadcast match videos using the **TrackNet** architecture. The model takes in consecutive frames and outputs a heatmap showing the ball's position, even in cases where it’s blurry, fast-moving, or partially occluded.

## 📌 Features

- Tracks small and fast tennis balls in real-time
- Learns motion and trajectory from multiple video frames
- Outputs Gaussian heatmaps for ball localization

## 🧠 Model Architecture

TrackNet is based on a CNN encoder-decoder structure. It takes 3 consecutive frames as input (merged into 9 channels) and predicts a heatmap indicating the ball's location in the center frame.

## 📁 Dataset

The dataset includes:
- 10 broadcast match videos
- 19,835 labeled frames
- Labels include: `Frame Name`, `Visibility`, `X`, `Y`, and `Trajectory Pattern`

Dataset: [Google Drive Link](https://drive.google.com/drive/folders/11r0RUaQHX7I3ANkaYG4jOxXK1OYo01Ut)

## 🚀 Getting Started

# Install dependencies
pip install -r requirements.txt

# Generate ground truth images and labels
python gt_gen.py

# Train the model
python main.py

