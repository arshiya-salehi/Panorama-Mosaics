# Panorama Mosaics

This project implements **image stitching and panorama creation** using computer vision techniques.  
It takes a series of overlapping images and combines them into a single seamless panorama.

## 📸 Project Overview
- Input: Multiple overlapping images (e.g., IMG_1341.JPG, IMG_1342.JPG, …).
- Process: Detects and matches key feature points across images, estimates transformations, and warps images.
- Output: A stitched mosaic / panorama image.

The workflow is implemented in the Jupyter notebook **`3_panorama.ipynb`** and uses helper scripts like **`selectpoints.py`** for selecting corresponding points.

## 🛠️ Tools & Libraries
- **Python 3**
- **NumPy** – numerical computations
- **OpenCV / Image processing utilities** – feature detection, warping, and blending
- **Matplotlib** – visualization
- **Pickle** – for saving and loading image correspondences
- **Jupyter Notebook** – interactive development

## 🧩 Algorithms & Techniques
- **Feature Detection & Matching**  
  Extract keypoints across overlapping images and compute correspondences.
  
- **Homography Estimation**  
  Compute the perspective transformation (homography) between images using matched points.
  
- **Image Warping & Alignment**  
  Warp images into a common reference frame using the estimated homography.
  
- **Mosaic Blending**  
  Merge multiple warped images together to produce a smooth panorama.

## 📂 File Structure

Panorama-Mosaics-main/
│── 3_panorama.ipynb # Main notebook for panorama stitching
│── selectpoints.py # Helper script for selecting feature correspondences
│── *.pckl # Pre-saved correspondence files
│── *.JPG # Input images for stitching
│── base.jpg / left.jpg / right.jpg # Example panorama inputs
│── README.md # Project description



## 🚀 How to Run
1. Clone or download the repository.  
2. Install dependencies:
   ```bash
   pip install numpy matplotlib opencv-python


