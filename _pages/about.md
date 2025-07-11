---
permalink: /
title: "Hello, I'm Xinghao Chen"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<!-- 1. Header Banner -->


<p align="center">
  <a href="https://github.com/cxhcxh2233"><img src="https://img.shields.io/badge/GitHub-cxhcxh2233-blue?style=for-the-badge&logo=github" alt="GitHub"></a>
  <a href="mailto:cxhcxh2233@gmail.com"><img src="https://img.shields.io/badge/Email-cxhcxh2233@gmail.com-red?style=for-the-badge&logo=gmail" alt="Email"></a>
</p>

I'm an aspiring researcher and engineer in my final year at **Beihang University**, driven by a mission to demystify the complex interplay between algorithms and the silicon they run on. My academic journey is centered around a core question: **How can we build more efficient, powerful, and perceptive hardware for the age of AI?** This question has led me to dive deep into the worlds of **FPGA/ASIC design, computer vision, and wireless sensing**.

---

### 🛠️ Technical Skillset

<p align="center">
  <b>Languages:</b><br>
  <img src="https://img.shields.io/badge/Verilog-A8B1B6?style=for-the-badge&logo=verilog&logoColor=white" alt="Verilog"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++"/>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=black" alt="C"/>
  <img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="Shell Script"/>
  <img src="https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white" alt="LaTeX"/>
  <br>
  <b>Frameworks & Libraries:</b><br>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn"/>
  <img src="https://img.shields.io/badge/MATLAB-0076A8?style=for-the-badge&logo=mathworks&logoColor=white" alt="MATLAB"/>
  <br>
  <b>Hardware & EDA Tools:</b><br>
  <img src="https://img.shields.io/badge/Vivado-D22A0F?style=for-the-badge&logo=xilinx&logoColor=white" alt="Vivado"/>
  <img src="https://img.shields.io/badge/KiCad-314193?style=for-the-badge&logo=kicad&logoColor=white" alt="KiCad"/>
  <img src="https://img.shields.io/badge/CST-003366?style=for-the-badge" alt="CST Studio"/>
  <img src="https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white" alt="STM32"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git"/>
</p>

---

### ✨ Featured Research & Projects

<details open markdown="1">
<summary><strong>🔎 Project 1: Rethinking Millimeter-Wave Object Detection (First Author, under review)</strong></summary>
<br>


<!-- Text-Image Layout: Image on the right -->

**The Challenge:** Standard object detectors fail in millimeter-wave security screening due to noisy backgrounds and faint, tiny targets. A fundamentally different approach was needed.

**My Approach:** I architected a multi-stage, "divide and conquer" detection pipeline. First, I used a Segmentation foundation model (SAM) to **surgically remove background clutter**. Then, I re-engineered the YOLOv8 architecture with custom **"Windmill Convolutions"** and a **"Monte Carlo Attention"** mechanism, forcing the network to focus on preserving the subtle features of minuscule targets.

**The Impact:** This novel framework boosted the core detection accuracy (**mAP50-95) by 6.84%** while simultaneously making the model leaner and faster, slashing **parameters by 45.85%**. This work was recognized with a university research award and is currently under review at *IEEE GRSL*.

<br clear="all" />
</details>


<details open markdown="1">
<summary><strong>📡 Project 2: Sensing Human Activity with Wi-Fi Signals (First Author, IEEE ICSECE 2025)</strong></summary>
<br>


<!-- Text-Image Layout: Image on the right -->


**The Challenge:** Can we perceive human actions without cameras or wearables, using only the ambient Wi-Fi signals that already surround us? The difficulty lies in extracting meaningful patterns from these abstract, noisy signals.

**My Approach:** My core insight was to reframe the problem. Instead of analyzing the raw signal directly, I used Short-Time Fourier Transform (STFT) to convert the Wi-Fi Channel State Information (CSI) into **3D spectrograms**—essentially turning the signal into an "image" that reveals the micro-Doppler shifts caused by human movement. I then built a hybrid **CNN-BiLSTM network**. The CNN acts as a feature "eye," extracting spatial patterns from each spectrogram frame, while the BiLSTM models the sequence, understanding the grammar of motion over time.

**The Impact:** This method achieved **71.50% accuracy** on the public OPERAnet dataset, with F1 scores **exceeding 0.9** for dynamic activities like walking. It validates a powerful, privacy-preserving approach to human activity recognition.

<br clear="all" />
</details>


<details open markdown="1">
<summary><strong>⚡ Project 3: Adaptive Image Denoising on an FPGA (First Author, IEEE AUTEEE 2024)</strong></summary>
<br>


<!-- Text-Image Layout: Image on the right -->


**The Challenge:** Traditional image filters make a trade-off: remove noise but blur important details. I wanted to create a filter "smart" enough to know the difference.

**My Approach:** I designed and implemented, entirely in **Verilog**, a real-time denoising system with a two-level adaptive engine. The algorithm analyzes the local complexity of the image on-the-fly, applying strong smoothing to flat areas while delicately preserving edges and textures. The entire process was optimized for **parallel pipeline execution** on a PYNQ-Z2 FPGA.

**The Impact:** The hardware-accelerated system demonstrably outperformed static filters, achieving a superior **Structural Similarity (SSIM) index of 0.3804**. It runs in real-time using minimal resources (just **5.28% of LUTs**), proving its practicality for real-world applications.

<br clear="all" />
</details>

---

### 👨‍💻 More About Me

When I step away from the workbench, I enjoy the discipline and expression of playing the piano, the patience and perspective of photography, and the endurance of long-distance running. Exploring new places and cultures during my travels constantly reframes my thinking and fuels my creativity.

**I am actively seeking PhD opportunities for Fall 2026 and am eager to connect with faculty and research groups who share my passion. For a detailed list of all my work, please see my [full Curriculum Vitae](./cv.md).**
