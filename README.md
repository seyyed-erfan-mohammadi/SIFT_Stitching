# 🔍 SIFT Panorama Stitching with Blending Modes
<div align="center">
  <img width="595" height="641" alt="Screenshot 2025-07-20 at 21 10 44" src="https://github.com/user-attachments/assets/65356065-b0c1-483c-98ef-4b53303d178a" />
</div>



## 🧠 Overview
This project investigates the performance of the **SIFT (Scale-Invariant Feature Transform)** algorithm for stitching panoramic images. It evaluates how well SIFT performs under various conditions such as image rotation, scaling, cropping, and intensity variation. The goal is to simulate real-world challenges in image alignment and to enhance visual output using different image blending strategies.

Panorama stitching is often used in computer vision for applications such as virtual tours, wide-angle photography, and autonomous vision systems. This repository serves as an experimental platform to understand the behavior of SIFT-based stitching across common distortions and variations in image data.

---

## 💡 Objective
The primary aim is to test the robustness of SIFT against:
- **Geometric transformations**, such as rotations (45°, 90°, 135°, 180°) and scaling,
- **Photometric changes**, such as increased intensity and brightness shifts,
- **Structural modifications**, such as cropping resulting in different image sizes.

These tests simulate how an algorithm might behave when dealing with overlapping image pairs captured under imperfect or dynamic conditions.

Additionally, this project evaluates different **blending modes** to improve the appearance of stitched images. Stitching without blending can result in visible seams, misalignments, or abrupt changes in brightness. To overcome this, blending techniques such as linear blending and constant blending correction are incorporated.

---

## 🖼️ Experimental Scenarios
The repository contains several predefined tests that apply SIFT stitching to different image pairs:

- **Normal image pairs** are tested to establish a baseline for performance and appearance. These serve as references for comparison with altered images.
- **Cropped images**, where one image in the pair has missing sections or reduced dimensions, evaluate SIFT’s tolerance for image size mismatch.
- **Rotated images** simulate camera orientation differences. Here, the right image is rotated at various angles before stitching.
- **Scaled images** test the algorithm's scale invariance by resizing one of the image pairs before alignment.
- **Intensity-modified images** simulate lighting variation by artificially increasing the brightness and contrast of one image in the pair.

In each scenario, results are examined with and without blending to highlight how different blending strategies affect the final panorama quality.

## 📊 Results Interpretation
The stitched images demonstrate that SIFT is highly robust to transformations such as rotation and scaling. Even under 135° or 180° rotations, the algorithm successfully identifies keypoints and aligns images with high accuracy. However, intensity variations and cropping present more of a challenge. This is where blending plays a critical role in producing visually acceptable results.

Blending helps eliminate harsh seams, aligns exposure levels, and produces a more cohesive panorama. Among the three modes tested, linear blending with constant correction provides the most seamless output.


