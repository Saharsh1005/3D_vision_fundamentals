# Foundations of 3D Vision with Emphasis on NeRF

This repository accompanies the independent study project conducted by **Saharsh Barve** under **CS597-DWH, Spring 2024 at UIUC**, advised by **Prof. Derek Hoiem** and **Yuqun Wu**. The focus of the project is on exploring state-of-the-art methods in 3D scene representation, particularly **Neural Radiance Fields (NeRF)** and complementary techniques to refine its geometric outputs.

## 📚 Project Summary

The primary goal of this study was to analyze and improve 3D geometry reconstruction from image data using deep learning models like NeRF, and evaluate methods to enhance the geometric fidelity of such models. Key contributions include:

- Reproducing and experimenting with the **TinyNeRF** implementation on the Lego dataset.
- Applying **MonoPatchNeRF** to the Tanks & Temples (TnT) dataset for high-quality surface and normal reconstruction.
- Integrating **MonoPatchNeRF with NKSR** for enhanced mesh reconstruction, and critically evaluating its sensitivity to noise.

## 🧠 Techniques Covered

- **Structure from Motion (SfM)** and **Multi-View Stereo (MVS)**: Classical methods for sparse and dense 3D reconstruction from multiple images.
- **NeRF (Neural Radiance Fields)**: Deep learning-based method for novel view synthesis and volumetric rendering.
- **MonoPatchNeRF**: A monocular-patch-based method to improve NeRF by incorporating depth and surface normals.
- **NKSR (Neural Kernel Surface Reconstruction)**: Method for converting point clouds into mesh representations using kernel-based learning.

## 🧪 Experiments

| Model            | Dataset          | Highlights                                                                 |
|------------------|------------------|---------------------------------------------------------------------------|
| TinyNeRF         | Lego (100x100)   | Lightweight implementation to understand NeRF pipeline and rendering      |
| MonoPatchNeRF    | Tanks & Temples  | Barn scene reconstruction using monocular cues and patch-based sampling   |
| MonoPatchNeRF + NKSR | Tanks & Temples  | Evaluated geometric fidelity and limitations due to noise sensitivity     |

## 📈 Results & Observations

- TinyNeRF effectively demonstrated the fundamentals of view synthesis.
- MonoPatchNeRF improved geometry reconstruction with structural loss functions (NCC, SSIM).
- NKSR, while promising, showed sensitivity to noisy inputs and required careful preprocessing of point clouds.
- The study suggests future work involving NeRF-generated novel views fed into MVS pipelines for further accuracy.

## 🛠️ Tools & Libraries

- PyTorch (NeRF implementations)
- COLMAP (Structure from Motion)
- CUDA for GPU acceleration
- NKSR (sparse convolutional mesh reconstruction)

## 📎 References

This work builds on literature from leading conferences like ECCV, CVPR, and includes:
- NeRF (Mildenhall et al.)
- MonoPatchNeRF (Yuqun Wu et al.)
- NKSR (Huang et al.)
- COLMAP, TinyNeRF, Tanks & Temples dataset, and more.

Refer to `report.pdf` in this repo for the full write-up and detailed citations.

## 🙏 Acknowledgements

Special thanks to **Prof. Derek Hoiem**, **Prof. Shenlong Wang**, **Chuhang Zou**, and **Yuqun Wu** for their insightful discussions and guidance throughout this independent study.

---

> _“Exploring 3D vision through a blend of classical geometry and modern neural rendering.”_
