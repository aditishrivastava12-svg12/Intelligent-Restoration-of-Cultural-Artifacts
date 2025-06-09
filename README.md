# Intelligent-Restoration-of-Cultural-Artifacts
This project demonstrates the restoration of damaged artworks using a deep learning-based image-to-image translation approach. Leveraging Convolutional Neural Networks (CNNs), the system learns from paired examples of damaged and undamaged art to predict visually restored versions of degraded images.



## 📁 Dataset Overview

The dataset is organized as follows:


AI_for_Art_Restoration_2/
├── paired_dataset_art/
│   ├── damaged/        # Damaged artworks (e.g., cracks, stains)
│   └── undamaged/      # Ground truth (clean) images
├── unpaired_dataset_art/
│   ├── damaged/        # Extra damaged images (no direct pair)
│   └── undamaged/      # Extra clean images

* Total Files: 533
* Image Formats: .jpg, .png, .webp

---

## ⚙ Technologies Used

* *Python 3*
* *Google Colab* (development environment)
* *TensorFlow / Keras* – Deep Learning framework
* *NumPy* – Array and numerical operations
* *PIL* – Image processing
* *Matplotlib* – Visualization
* *Scikit-learn* – Data splitting
* *TQDM* – Progress bar for loops
* *Google Drive* – Dataset storage

## 🧠 Model Architecture

A simple *Autoencoder CNN* is used, consisting of:

* *Encoder*: Multiple Conv2D + MaxPooling2D layers
* *Decoder*: UpSampling2D + Conv2D layers
* *Loss Function*: Mean Squared Error (MSE)
* *Optimizer*: Adam (learning rate = 1e-4)
* *Metric*: Mean Absolute Error (MAE)


## 🛠 Project Workflow

1. *Mount Google Drive* to access dataset
2. *Match paired images* based on filename pattern
3. *Preprocess* images (resize to 256×256, normalize)
4. *Split* into training and validation sets
5. *Build & train* the CNN restoration model
6. *Visualize results* (loss plots and image comparisons)

---

## 📊 Sample Outputs

* *Training vs Validation Loss Graph*
* *Side-by-Side Comparison*:

  * Damaged Input
  * Model Output (Restored)
  * Ground Truth (Undamaged)

## 🚀 How to Run

1. Open the [Colab Notebook](https://colab.research.google.com/)
2. Mount your Google Drive
3. Upload the dataset to MyDrive
4. Run cells to:

   * Match images
   * Train the model
   * Visualize outputs

---

## 🔮 Future Scope

* Introduce *GANs* for sharper and more realistic restorations
* Handle *unpaired datasets* using *CycleGAN*
* Add a *Streamlit UI* for easy image upload and download

---

## 🙌 Acknowledgments

Special thanks to the contributors of public datasets and the creators of educational resources on deep learning and image restoration.
