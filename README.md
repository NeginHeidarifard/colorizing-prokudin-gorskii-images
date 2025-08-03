#  Colorizing the Prokudin-Gorskii Collection using Image Alignment Techniques

**Author**: Negin Heidarifard  
**Course**: M2 Artificial Intelligence, Université Paris-Saclay  
**Project**: Computer Vision – Assignment  

---

## Project Overview

This project focuses on reconstructing color photographs from early 20th-century grayscale glass plate negatives captured by **Sergei Mikhailovich Prokudin-Gorskii**. Each image contains three vertically stacked grayscale channels taken with Red, Green, and Blue filters. Our goal is to extract and align these layers to produce high-quality color images.

This assignment offers a practical exercise in classical computer vision, image alignment, and real-world signal reconstruction.

---

##  Objectives

- Extract R, G, and B channels from the scanned plates  
- Align color channels using various computer vision techniques  
- Improve visual quality using cropping and contrast enhancement  
- Evaluate performance based on alignment accuracy and visual fidelity

---

## 🔧 Techniques Implemented

###  1. Naive Channel Splitting
- Splits the image vertically into three channels (B, G, R)
- Produces highly misaligned color images without further processing

###  2. Sum of Squared Differences (SSD)
- Uses brute-force search to find the best displacement
- Measures pixel-wise similarity across small shift ranges

###  3. Canny Edge Alignment
- Improves robustness using edge-based similarity instead of raw pixel values
- Reduces sensitivity to lighting and texture differences

###  4. Image Pyramid Alignment
- Applies recursive downsampling and alignment at multiple resolutions
- Speeds up search and handles large misalignments

###  5. Contour-Based Matching
- Aligns edges using Canny and Sobel filters
- Suitable for high-resolution images with structural features

---

##  Results and Enhancements

- **Post-processing**:  
  - Cropping black borders  
  - Histogram Equalization in YCrCb space for contrast improvement  

- **Performance**:  
  - Achieved visually accurate color alignment  
  - Verified with qualitative assessment of facial features and textures

---

##  Repository Structure

```bash
ProkudinGorskii-Colorization/
├── assignment_computer_vision_Negin_HEIDARIFARD.ipynb  # Main code notebook
├── assignment_computer_vision_Negin_HEIDARIFARD.pdf    # Exported report
├── Data/                                               # Input images
├── Outputs/                                            # Aligned results
├── LICENSE                                             # License (MIT)
└── README.md                                           # This documentation


Python (NumPy, SciPy, OpenCV)

Matplotlib, MoviePy

Jupyter Notebook

 Sample Input & Output
Input: emir.tiff – Prokudin-Gorskii glass plate

Output: RGB image after alignment and enhancement

Refer to the notebook for visual results and step-by-step illustrations.

 License
This project is licensed under the MIT License.

 Dataset Access
Due to storage limitations, the input dataset is not publicly uploaded.
 To access the dataset for academic reproduction, please contact the author via GitHub or email.

 Author
Negin Heidarifard
MSc in Artificial Intelligence
Université Paris-Saclay
GitHub: github.com/NeginHeidarifard

📚 References
MIT CSAIL – Eulerian Video Magnification

Prokudin-Gorskii Digital Archive – Library of Congress

A. Efros, CMU/UC Berkeley Computer Vision Course Materials

 This project demonstrates strong applied skills in classical computer vision, signal alignment, and photographic restoration — with relevance to both AI research and real-world visual computing tasks.


