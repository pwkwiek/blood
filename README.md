# Color Me Synthetic
Generating Peripheral Blood Cells with Conditional GANs

When biomedical data is scarce, deep models still want more.

---

## What This Is

This project tackles **biomedical data scarcity** by generating synthetic microscopic images of peripheral blood cells using **conditional GANs (cGANs)**.

Using the **BloodMNIST** dataset (8 blood cell classes), we analyze how **cell morphology and RGB color distribution** contribute to classification — and how synthetic data can be generated without breaking biological plausibility.

---

## What It Does

- Analyzes **color distributions** using histograms and **k-means clustering**
- Identifies **dominant color components** (spoiler: blue barely matters)
- Uses **UMAP** and distance matrices to study class similarity
- Trains and compares multiple **conditional GAN architectures**
- Generates synthetic blood cell images for data augmentation
- Evaluates classification performance on generated data

---

## Key Findings

- Six dominant colors capture most chromatic information
- The **blue channel contributes minimally** and can be excluded from the loss
- High inter-class similarity limits perfect synthesis
- A **Mixture-of-Experts cGAN** with residual blocks and LeakyReLU performs best
- Synthetic data achieves **classification accuracy up to 0.97**

---

## Model Highlights

- Conditional GANs (baseline + variants)
- **Mixture-of-Experts cGAN**
- Residual blocks
- LeakyReLU activations
- Class-conditional image generation

---

## Why It Matters

- Medical datasets are small, imbalanced, and expensive
- Synthetic data can **boost training** when real samples are limited
- Color and morphology matter — but not equally
- Helps understand **what models actually learn** from biomedical images

---

## Notes

- Some misclassifications persist due to **high biological similarity**
- Designed for **analysis and insight**, not photorealistic perfection
- Best used as a **data augmentation and exploratory tool**

---

## Dataset

- BloodMNIST (MedMNIST collection)
