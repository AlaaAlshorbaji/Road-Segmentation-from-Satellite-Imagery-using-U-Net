
# 🛰️ Road Segmentation from Satellite Imagery using U-Net

This project implements a U-Net-based deep learning model for segmenting roads from satellite images. Road segmentation is a key task in remote sensing, urban planning, and autonomous driving.

U-Net is a popular convolutional neural network architecture used for semantic segmentation tasks, particularly with limited training data.

## 🎯 Objective

* Segment roads from high-resolution satellite images
* Train a U-Net model to learn pixel-level classification (road vs. background)
* Visualize segmentation results and evaluate performance

## 🗺️ Dataset

The dataset consists of satellite images and their corresponding road masks. Each mask represents road pixels as white and background as black.

* Images are typically of size 256×256 or 512×512
* Preprocessed into:

  * `images/` – input RGB satellite images
  * `masks/` – binary mask images

> Note: The dataset used is assumed to be manually provided and loaded from local directories (`image_dir`, `mask_dir`).

---

## 🗂️ File Structure & Code Explanation

The project is implemented in the following notebook:

```
📄 Road_Segmentation_from_Satellite_Imagery_using_U_Net.ipynb
```

It contains the following sections:

### 1. 📚 Importing Libraries

* `os`, `cv2`, `numpy`, `matplotlib`, `tensorflow`, `sklearn`, etc.

### 2. 📥 Loading Images & Masks

* Loads and resizes input images and corresponding binary masks.
* Normalizes input images to `[0, 1]`.

### 3. 🔀 Train/Test Split

* Splits the dataset into training and validation sets using `train_test_split`.

### 4. 🧠 U-Net Model Architecture

* Defines a full U-Net model using Keras Functional API.
* Includes encoder, bottleneck, and decoder layers.

### 5. 🏋️ Model Training

* Compiles the model using `binary_crossentropy` loss and `Adam` optimizer.
* Trains using `.fit()` and monitors accuracy and loss.

### 6. 📈 Evaluation & Visualization

* Plots training and validation curves.
* Displays sample predictions next to original images and ground truth masks.

---

## ⚙️ Installation & Usage

### 📋 Prerequisites

Make sure the following packages are installed:

```bash
pip install tensorflow matplotlib numpy opencv-python scikit-learn
```

### ▶️ Running the Notebook

1. Place the dataset in folders like:

   * `images/`
   * `masks/`

2. Open the notebook in Jupyter or Colab:

```bash
jupyter notebook Road_Segmentation_from_Satellite_Imagery_using_U_Net.ipynb
```

3. Run all cells sequentially to:

   * Load data
   * Train U-Net
   * Visualize predictions

---

## 👨‍💻 Author

**Alaa Shorbaji**
Artificial Intelligence Instructor
Deep Learning & Satellite Vision Applications

---

## 📜 License

This project is licensed under the **MIT License**.

You are free to:

* ✅ Use and share the code for educational or commercial purposes
* ✅ Modify and redistribute with appropriate credit

You must:

* ❗ Attribute the original author properly
* ❗ Include this license notice in any substantial portions of the project

> **Disclaimer:** The model architecture is based on the standard U-Net design. The dataset is assumed to be provided by the user.
