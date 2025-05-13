# Img_compression-using-KMeans
# 📷 Image Compression using KMeans Clustering

This project demonstrates image compression using **KMeans clustering**, a popular unsupervised machine learning technique. The goal is to reduce the number of colors in an image by clustering similar colors together, resulting in a smaller file size with minimal visual loss.

---

## 🔍 Overview

The original image is compressed using KMeans with:
- **16 clusters**
- **32 clusters**
- **64 clusters**

For each cluster count, we:
- Compress the image
- Display the result
- Calculate the original and compressed size (in KB)
- Compute the compression ratio

---

## ✨ Features

- 📊 KMeans clustering on RGB pixel data
- 🎨 Visual comparison between original and compressed images
- 📦 Compression ratio and file size calculation
- 📁 Clean, modular code for easy experimentation

---

## 🧪 How It Works

1. **Load an image** and normalize pixel values.
2. **Flatten** the image into an (N, 3) array where N = total number of pixels.
3. **Apply KMeans clustering** to group pixel colors.
4. **Replace each pixel** with its cluster center value.
5. **Reshape and scale** the image back to RGB format.
6. **Calculate sizes**:
   - Original size in bits: `num_pixels × 3 × 8`
   - Compressed size in bits: `k × 3 × 32 (cluster centers)` + `num_pixels × log2(k) (labels)`
7. **Convert to KB** and compute compression ratio.

