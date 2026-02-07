# Custom Face Detection Model
This project focuses on building and training a custom face detection model from scratch using deep learning, instead of relying on pre-trained face detectors such as Haar Cascades, MTCNN, or RetinaFace.

The goal is to understand the end-to-end pipeline of object detection, including:
- Data preprocessing
- Bounding box scaling and normalization
- Model design
- Training limitations
- Evaluation through visualization

### Dataset
- 100 Face images in portrait orientation with clearly visible frontal face.
- Manually annotated bounding boxes.
- Images resized to a fixed resolution.
- Bounding boxes scaled and normalized during preprocessing.

### Model Architecture

MobileNetV2 is used as a convolutional feature extractor without pre-trained classification layers.

Global Average Pooling is applied to reduce spatial dimensions.

A fully connected output layer with sigmoid activation predicts normalized bounding box coordinates.

### Tech Stack
- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- MobileNetV2

### Results

- The model is able to localize approximate face regions in images and webcam frames.

- Bounding boxes generally capture the face but tend to be larger than the actual facial region.