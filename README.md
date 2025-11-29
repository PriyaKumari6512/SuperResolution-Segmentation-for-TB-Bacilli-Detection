# 🧬 TB Bacilli Detection Using Super-Resolution & Segmentation

This repository presents a complete deep-learning pipeline for detecting **Mycobacterium tuberculosis (TB bacilli)** from light microscopy smear images.  
The approach combines **Super-Resolution (EDSR)** and **Segmentation-based detection**, enabling more accurate identification of bacilli in low-resolution medical images.

This project is restructured, documented, and maintained by **Priya Kumari**, IIT Mandi (M.Tech CSE), inspired by publicly available research concepts on super-resolution and segmentation.

---

## 🔬 1. Motivation

Manual TB bacilli detection under a microscope is challenging because:

- Microscopy images are **low resolution**
- Bacilli are often **small & unclear**
- High noise & blur reduce accuracy

To improve visibility & detection, this project uses:

✔ **Deep Super-Resolution** (enhances image quality)  
✔ **Segmentation Model** (high-precision bacilli detection)  
✔ **PyTorch-based automated pipeline**

---

## 🧠 2. Methodology

### 🔷 **Step 1 — Super-Resolution (EDSR Fine-Tuning)**
- EDSR (Enhanced Deep Super Resolution Network)
- Domain-specific fine-tuning for microscopy images
- Pretrained SR model included: `edsr_ft_best.pth`

### 🔷 **Step 2 — Data Preparation**
- LR–HR image pair generation  
- Tensor conversion  
- Patch extraction  
- Custom dataset class in `dataset.py`

### 🔷 **Step 3 — Bacilli Segmentation**
- Pixel-level segmentation of bacilli regions  
- Detection masks generation  
- Full training + inference scripts included

### 🔷 **Step 4 — End-to-End Pipeline**
Scripts included:
- `fine_tune_EDSR_model.py`
- `train.py`
- `infer.py`
- `dataset.py`
- `losses.py`
- `model_esrgan.py`

---

## 📁 3. Project Structure

```
📦 TB-Bacilli-Detection-SR-Seg
 ┣ 📜 Main.py
 ┣ 📜 train.py
 ┣ 📜 run_inference.py
 ┣ 📜 dataset.py
 ┣ 📜 losses.py
 ┣ 📜 model_esrgan.py
 ┣ 📜 fine_tune_EDSR_model.py
 ┣ 📜 data_preparation_LR_HR_pair.py
 ┣ 📜 convert_dataset_to_tensor.py
 ┣ 📜 edsr_ft_best.pth
 ┗ 📜 README.md
```

---

## ⚙️ 4. Installation

### Install dependencies
```bash
pip install -r requirements.txt
```

Or manually install major libraries:
```bash
pip install torch torchvision numpy matplotlib opencv-python scikit-image tqdm
```

---

## 🚀 5. Usage

### ▶ A. Generate LR–HR Pairs
```bash
python data_preparation_LR_HR_pair.py
```

### ▶ B. Fine-Tune EDSR
```bash
python fine_tune_EDSR_model.py
```

### ▶ C. Train Segmentation Model
```bash
python train.py
```

### ▶ D. Run Inference
```bash
python run_inference.py --input test_image.png
```

---

## 📊 6. Results

### ✔ Super-Resolution Output
- Improved clarity  
- Sharper structures  
- Enhanced visibility of bacilli  

### ✔ Segmentation Output
- Pixel-level detection  
- Clear marking of bacilli regions  
- Reduced false positives  

*(Add sample output images here)*

---

## 🏗 7. Future Improvements

- YOLOv8-based TB bacilli segmentation  
- Model deployment using **FastAPI / Streamlit**  
- Mobile-friendly inference pipeline  
- Semi-supervised SR for limited datasets  

---

## 👤 8. Author

**Priya Kumari**  
M.Tech — Computer Science & Engineering  
Indian Institute of Technology **(IIT) Mandi**  
- GitHub: [github.com/PriyaKumari6512](https://github.com/PriyaKumari6512)  
- LinkedIn: [linkedin.com/in/priya-kumari-keshri-136107234](https://linkedin.com/in/priya-kumari-keshri-136107234)

---

## 📝 9. Notes

- This repo is inspired by open-source research work.
- Code is **restructured, renamed, documented, and organized** by Priya Kumari.
- Project structure & scripts are optimized for clarity and reproducibility.

---

## 🔖 License

This project is intended for research and educational use only.

---

### ⭐ If you want a **GitHub banner image**, project badge, or a more research-style README—just tell me.  

