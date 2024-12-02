# Neural Network for Image Segmentation with U-Net

This project implements an image segmentation model using a U-Net architecture in TensorFlow/Keras. It is designed to process images and their corresponding segmentation masks for tasks such as semantic segmentation in autonomous driving scenarios.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Features](#features)
3. [Dataset](#dataset)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Model Architecture](#model-architecture)
7. [Results](#results)
8. [Contributing](#contributing)
9. [License](#license)

---

## Introduction <a name="introduction"></a>
The U-Net model is a convolutional neural network used for biomedical and general image segmentation. It was adapted for this project to segment images from a dataset with corresponding masks.

---

## Features <a name="features"></a>
- **Preprocessing pipeline**: Automatic resizing and normalization of input images and masks.
- **Custom U-Net model**: Configurable depth, number of filters, and dropout.
- **Visualization tools**: Display the original image, ground truth mask, and predicted mask.
- **Training pipeline**: Easy-to-use training with model performance visualization.

---

## Dataset <a name="dataset"></a>
The dataset used contains:
- Images: RGB images representing a scene.
- Masks: Segmentation masks where each pixel corresponds to a class label.

### Dataset Directory Structure

Place the dataset inside the `data/` folder. Update the `path` variable in the script if the dataset is located elsewhere.

---

## Installation <a name="installation"></a>
### Requirements
- Python 3.7+
- TensorFlow 2.0+
- NumPy
- Matplotlib
- ImageIO

### Steps
1. Clone this repository:
    ```bash
    git clone https://github.com/your-repository.git
    cd your-repository
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

---

## Usage <a name="usage"></a>
1. Preprocess the data and train the model:
    ```bash
    python train.py
    ```

2. Visualize predictions:
    Modify the `show_predictions` function to set `num` to the desired number of predictions to display.

---

## Model Architecture <a name="model-architecture"></a>
The U-Net architecture consists of:
1. **Contracting Path**: Extracts features using convolutional layers with pooling.
2. **Bottleneck**: Combines high-level features with context.
3. **Expanding Path**: Recovers spatial information using transposed convolutions and skip connections.


---

## Results <a name="results"></a>
### Training Accuracy
- Accuracy plot during training:  
  ![Training Accuracy](./results/accuracy_plot.png)

### Sample Output
| Input Image | True Mask | Predicted Mask |
|-------------|-----------|----------------|
| ![Image](./results/sample_image.png) | ![Mask](./results/sample_mask.png) | ![Prediction](./results/sample_prediction.png) |

---

## Contributing <a name="contributing"></a>
Contributions are welcome! Please fork the repository and create a pull request for your feature additions or bug fixes.

---

## License <a name="license"></a>
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

