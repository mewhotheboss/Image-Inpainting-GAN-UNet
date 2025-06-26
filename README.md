# Image Inpainting using GAN and U-Net with Web Deployment

## 📌 Project Overview

We developed an **image inpainting system** that fills large missing areas in high-resolution images. The project uses a **hybrid deep learning model**, where **U-Net acts as the generator** to restore structure and **GAN acts as the discriminator** to create realistic textures.
We also built a **web application** that allows users to upload damaged images and get inpainted results in real-time. This tool helps in tasks like **restoring old photos** or **repairing broken images**.

---

## 🛠️ Development Environment

* Platform: **Google Colab**
* Language: **Python**
* Framework: **PyTorch**
* Web Deployment: **Flask** + **Ngrok**
* Data storage and checkpoints: **Google Drive**

---

## 📂 Dataset

We used the **CelebA-HQ (256×256 resolution)** dataset, downloaded using **KaggleHub** in Google Colab.
The dataset contains high-quality human face images suitable for training image inpainting models.

---

## 🧠 Model Architecture

* **Generator**: U-Net based architecture to reconstruct missing regions.
* **Discriminator**: CNN-based model with **Spectral Normalization** to help generate realistic textures.
* Loss Functions used:

  * **Adversarial Loss (BCELoss)**
  * **Pixel-wise L1 Loss**
  * **Gradient Penalty** for GAN stability.

---

## 🚀 Training Details

* **Environment**: Google Colab with GPU support.
* **Custom Dataset Loader**: Applies **random square masks** on images to simulate missing areas during training.
* **Training Strategy**:

  * Generator learns to fill gaps.
  * Discriminator learns to differentiate between real and generated images.
  * Both models trained together using **GAN training loop**.
* **Output Checkpoints** and **Generated Results** saved in Google Drive.

---

## 🌐 Web Application Deployment

We integrated the trained model into a **Flask-based web application**.
Using **Ngrok**, we exposed the app to the internet from Google Colab, allowing users to:

* Upload broken images.
* Get real-time inpainted results.

---

## 📈 Performance Comparison

We compared our model's performance with existing inpainting techniques to check **visual quality** and **realism** on different image types.

---

## 🎯 Applications

* Damaged image repair.
