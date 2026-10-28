# 🖼️ Classical & Computational Image Processing Algorithms

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg?logo=python&logoColor=white)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/Vision-OpenCV%20%7C%20Scikit--Image-5C3EE8.svg?logo=opencv&logoColor=white)](https://opencv.org/)
[![NumPy](https://img.shields.io/badge/Array-NumPy-013243.svg?logo=numpy&logoColor=white)](https://numpy.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Academic](https://img.shields.io/badge/Hacettepe%20University-BBM413-990000.svg)](https://cs.hacettepe.edu.tr/)

**Fundamental implementations of computational photography and image processing algorithms: Glass-plate RGB channel alignment, Reinhard statistical color transfer in $L\alpha\beta$ space, Laplacian/Gaussian multiresolution pyramid blending, and Normalized Cross-Correlation (NCC) template matching.**

</div>

---

## 📌 Laboratory Modules Overview

This repository contains algorithmic implementations and technical laboratory reports for classical computer vision and computational photography:

### 1. Assignment 1: Multi-Channel Glass Plate Color Alignment (Prokudin-Gorskii Restoration)
- **Glass Plate Separation:** Automated partitioning of single-channel glass negative plates into R, G, and B channel exposures.
- **Border & Artifact Removal:** Crop border luminance heuristics to remove scanning artifacts.
- **Sub-Pixel Channel Alignment:** Cross-correlation and Sum of Squared Differences (SSD) optimization across image pyramids to re-align chromatic layers into high-fidelity color photographs.

### 2. Assignment 2: Statistical Color Transfer in $L\alpha\beta$ Space (Reinhard Algorithm)
- **Decorrelated Color Space:** Conversion from RGB to Ruderman $L\alpha\beta$ color space to decouple luminance from color channels.
- **Distribution Matching:** Scaling and shifting mean and standard deviations of source pixel channels to match target color palettes:
  $$L^* = \frac{\sigma_{target}^L}{\sigma_{source}^L}(L - \mu_{source}^L) + \mu_{target}^L$$
- **Region-Based Semantic Transfer:** K-means clustering for localized color transfer across semantic regions.

### 3. Assignment 3: Multiresolution Image Blending via Gaussian & Laplacian Pyramids
- **Gaussian Pyramid:** Iterative low-pass filtering and downsampling.
- **Laplacian Pyramid:** Band-pass decomposition capturing edge details across spatial frequencies.
- **Seamless Masking:** Multi-scale spatial blending avoiding seam discontinuities and ghosting artifacts (e.g. "Oraple" blending).

### 4. Assignment 4: Template Matching & Classification via Normalized Cross-Correlation (NCC)
- **Pattern Matching:** Sliding-window normalized cross-correlation:
  $$\gamma(x, y) = \frac{\sum_{x', y'} (T(x', y') - \bar{T})(I(x+x', y+y') - \bar{I}_{x, y})}{\sqrt{\sum_{x', y'} (T(x', y') - \bar{T})^2 \sum_{x', y'} (I(x+x', y+y') - \bar{I}_{x, y})^2}}$$
- **Invariant Object Classification:** Robust detection under linear illumination shifts.

---

## 📂 Repository Structure

```ascii
Image_Processing_Assignments/
├── ass1/                        # Prokudin-Gorskii RGB Glass Plate Alignment
├── ass2/                        # Reinhard Color Transfer in L*a*b* Space
├── ass3/                        # Multiresolution Laplacian Pyramid Blending
├── ass4/                        # NCC Template Matching & Image Classification
└── README.md                    # Laboratory documentation
```

---

<div align="center">
Developed by <a href="https://github.com/huseyin-yigit-ulker">Hüseyin Yiğit Ülker</a>
</div>
