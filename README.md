# 📌 Bit Plane Slicing of a Color Image

## 🔷 Overview

This project demonstrates **Bit Plane Slicing** on a color image (RGB).
The objective is to extract and display individual bit planes from each color channel and analyze their contribution to the overall image intensity.

A color image consists of three channels:

* Red (R)
* Green (G)
* Blue (B)

Each channel contains 8 bits per pixel, resulting in a total of:

[
3 \times 8 = 24 \text{ bit planes}
]

---

## 🎯 Objectives

* Read a color image
* Extract individual RGB channels
* Perform bitwise operations to obtain bit planes (0–7)
* Display and analyze each bit plane
* Optionally reconstruct the image using selected bit planes

---

## 🧠 Concept

Each pixel in an 8-bit channel has values ranging from 0 to 255.

Example:

```
150 → 10010110 (Binary)
```

Each binary digit represents a bit plane:

* Bit 0 → Least Significant Bit (LSB)
* Bit 7 → Most Significant Bit (MSB)

Mathematically:

[
BitPlane_k = (Pixel >> k) & 1
]

Where:

* `>> k` shifts the pixel value by k positions
* `& 1` extracts the last bit

---

## 🔹 Process

1. Load the color image.
2. Separate the image into Red, Green, and Blue channels.
3. Extract bit planes (0–7) from each channel.
4. Display all 24 bit planes.
5. Analyze the visual contribution of each plane.
6. Optionally reconstruct the image using selected higher bit planes.

---

## 📊 Observations

### 🔹 Lower Bit Planes (0–2)

* Contain minor intensity variations
* Mostly noise
* Minimal visual contribution

### 🔹 Middle Bit Planes (3–5)

* Moderate structure visibility
* Partial image information

### 🔹 Higher Bit Planes (6–7)

* Major structural information
* Significant contribution to brightness and color
* Image structure clearly visible

Higher bit planes contribute more because:

[
2^7 = 128 \quad (High weight)
]
[
2^0 = 1 \quad (Low weight)
]

---

## 🔧 Applications

* Image compression
* Digital watermarking
* Image enhancement
* Noise analysis
* Steganography

---

## ✅ Conclusion

Bit plane slicing helps in understanding how different bits contribute to image intensity.
Higher-order bit planes carry the most important structural information, while lower-order bit planes mainly contain fine details and noise.

This technique is widely used in image processing applications such as compression and data hiding.

---
AUTHOR
ADHITYAN R
BTECH AI&DS
