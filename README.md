<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/YOLOv11-00FFFF?style=flat&logo=yolo&logoColor=black"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white"/>
</p>

<h1 align="center">🗑️ Smart City Waste Classifier</h1>

<p align="center">
  A computer vision system for automated waste detection and classification,
  built as part of a Smart City internship at Harmony Technology.
  Benchmarks CNN, VGG19, and YOLOv11 architectures on real urban waste data.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-active-brightgreen?style=flat"/>
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat"/>
  <img src="https://img.shields.io/badge/internship-Harmony%20Technology-purple?style=flat"/>
</p>

---

## 📌 Overview

Urban waste management is a critical challenge for smart cities. Manual sorting is slow, expensive, and error-prone. This project develops a **deep learning-based waste detection and classification module** that can be integrated into a smart city web interface for real-time waste identification.

Three architectures were benchmarked to find the best trade-off between accuracy and inference speed:
- **Custom CNN** — lightweight baseline trained from scratch
- **VGG19** — transfer learning from ImageNet weights
- **YOLOv11** — state-of-the-art object detection for real-time inference

---

## ✨ Features

- **Multi-model benchmarking** — CNN vs VGG19 vs YOLOv11 comparison
- **Transfer learning** — VGG19 fine-tuned on waste classification categories
- **Object detection** — YOLOv11 for real-time bounding box prediction
- **Color mask generation** — segmentation preprocessing pipeline
- **COCO format support** — dataset compatible with standard detection frameworks
- **Web integration ready** — model exported for deployment in a web interface

---

## 🗂 Project structure
```
smart-city-waste-classifier/
│
├── cocoset+CNN.ipynb          # CNN training on COCO-format dataset
├── trashnet+CNN.ipynb         # CNN training on TrashNet dataset
├── VGG19+trashnet.ipynb       # VGG19 transfer learning on TrashNet
├── yolov11+trashnet.ipynb     # YOLOv11 fine-tuning on TrashNet
├── gen_color_masks.ipynb      # Color mask generation for segmentation
├── color_to_label_num.ipynb   # Label mapping and preprocessing
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 🧠 Models compared

| Model | Type | Dataset | Notes |
|-------|------|---------|-------|
| Custom CNN | Classification | TrashNet + COCO | Lightweight baseline |
| VGG19 | Transfer learning | TrashNet | ImageNet pretrained |
| YOLOv11 | Object detection | TrashNet | Real-time inference |

---

## 📊 Datasets

### TrashNet
- 6 categories: glass, paper, cardboard, plastic, metal, trash
- Used for classification models (CNN, VGG19)
- Download: [garythung/trashnet](https://github.com/garythung/trashnet)

### COCO
- Real-world urban waste images in COCO annotation format


> Datasets are not included in this repo.

---

## 🚀 Getting started

### Prerequisites
- Python 3.9+
- Jupyter Notebook or VS Code with Jupyter extension


### Run the notebooks in order
```
1. color_to_label_num.ipynb     ← label preprocessing
2. gen_color_masks.ipynb        ← mask generation
3. cocoset+CNN.ipynb            ← CNN on COCO data
4. trashnet+CNN.ipynb           ← CNN on TrashNet
5. VGG19+trashnet.ipynb         ← VGG19 transfer learning
6. yolov11+trashnet.ipynb       ← YOLOv11 detection
```

---

## ⚙️ How it works
```
Raw waste images
      │
      ▼
Preprocessing (color masks + label mapping)
      │
      ├──▶ CNN (from scratch) ──────────────▶ Classification
      │
      ├──▶ VGG19 (transfer learning) ───────▶ Classification
      │
      └──▶ YOLOv11 (fine-tuned) ────────────▶ Detection + Bounding boxes
                                                      │
                                                      ▼
                                              Web interface integration
```

---

## 🛠 Tech stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.9 |
| Deep learning | TensorFlow, Keras |
| Object detection | YOLOv11 (Ultralytics) |
| Computer vision | OpenCV |
| Data processing | NumPy, Pandas |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |


## 📄 License

This project is licensed under the MIT License.

---

## 👩‍💻 Author

**Hajar Benbassou**  
Final-year AI & Data Science Engineering student at ENSAM Rabat

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/hajar-benbassou)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/hajar-125)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:benbassou.hajar@gmail.com)
