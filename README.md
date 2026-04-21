# 🎨 Conditional GAN for Sketch-to-Face Generation

## 🚀 Overview

This project implements a **Conditional Generative Adversarial Network (cGAN)** that converts **facial sketches into realistic human face images**. The model learns a mapping from a sketch domain to a photo-realistic domain, enabling applications in digital art, forensics, and creative design.

---

## 🧠 Motivation

Generating realistic faces from sketches is a challenging task due to:

* Missing texture and color information in sketches
* Ambiguity in facial details
* Need for identity preservation

This project addresses these challenges using **conditional GANs with perceptual and reconstruction losses**.

---

## 🏗️ Model Architecture

### 🔹 Generator

* Encoder-Decoder (U-Net style)
* Skip connections for preserving structure
* Takes:

  * Sketch image
  * Condition input (optional attributes)

### 🔹 Discriminator

* CNN-based binary classifier
* Distinguishes:

  * Real face images
  * Generated images

---

## ⚙️ Training Objective

The model is trained using a combination of:

* **Adversarial Loss** → realism
* **L1 Loss** → structure preservation
* **Perceptual Loss (VGG)** → high-level features

### Final Loss:

## Training Objective

The total loss function:

<p align="center">
L = L<sub>GAN</sub> + λ₁ L<sub>L1</sub> + λ₂ L<sub>perceptual</sub>
</p>

## 📊 Dataset

* Based on CelebA
* Preprocessing:

  * Convert images → sketches (edge detection / synthetic sketching)
  * Resize to 64×64 or 128×128
  * Normalize to [-1, 1]

---

## 🧪 Results

### ✏️ Input → Output

* Sketch → Realistic Face
* Preserves:

  * Facial structure
  * Key features (eyes, nose, mouth)

### ✅ Achievements:

* Sharp facial details
* Consistent identity
* Reduced blurriness with perceptual loss

---

## 📁 Project Structure

```
Sketch2Face-GAN/
│
├── dataset.py           # Data loading
├── model.py             # Generator + Discriminator
├── train.py             # Training loop
├── utils.py             # Helper functions
├── checkpoints/         # Saved models
├── samples/             # Generated images
└── notebook.ipynb       # Kaggle/Colab notebook
```

---

## ⚡ Installation

```bash
git clone https://github.com/your-username/Sketch2Face-GAN.git
cd Sketch2Face-GAN
pip install -r requirements.txt
```

---

## ▶️ Usage

### Train model

```bash
python train.py
```

### Resume training

```bash
python train.py --resume
```

---

## 🖼️ Sample Outputs

| Sketch | Generated Face |
| ------ | -------------- |
| ✏️     | 🙂             |

<img width="254" height="345" alt="image" src="https://github.com/user-attachments/assets/44cd6e13-d1a4-48ca-a363-113fe52dde6b" />


---

## 🔥 Applications

* 🕵️ Forensic sketch reconstruction
* 🎮 Game character design
* 🎨 Digital art generation
* 🧑‍🎨 Face editing tools

---

## 📈 Future Work

* Higher resolution (128×128, 256×256)
* Attention-based GAN
* Multi-attribute control
* Diffusion model comparison

---

## 👨‍💻 Author

**Your Name**

* GitHub: [https://github.com/your-username](https://github.com/Ataullah128)
* LinkedIn:www.linkedin.com/in/ata-ullah-648756230



---

## ⭐ Contributing

Feel free to fork the repo and submit pull requests!

---

## 📜 License

This project is open-source under the MIT License.

---


