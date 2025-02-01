# 🌍 GRESIDAN: Graphically RESIDual Attentive Network For Tackling Aerial Image Occlusion

## 🚀 Repository Updates
- ✅ Upload baseline inference code files
- ✅ Upload datasets and weights
- ✅ Upload testing and training instructions
- ⬜ Update training code
- ⬜ Create live demo with full inference

---

## 🛠 Installation Setup

### 📌 Object Detection
```bash
cd .../<parent directory>
pip install timm
pip install .
```

### 📌 Occlusion Detection
```bash
conda create -n <envname> python=3.8 -y
conda activate <envname>
pip install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu122
pip install ninja yacs cython matplotlib tqdm
pip install opencv-python
pip install scikit-image
git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
python setup.py build_ext install
cd .../<parent directory>
conda install cudatoolkit=10.1 -c pytorch
conda install -c conda-forge cudnn
pip install numpy==1.26.3
python3 setup.py build develop
pip install portalocker
pip install pillow==9.5.0
CUDA_VISIBLE_DEVICES=0
pip install -U pycocotools
```

### 📌 Occlusion Removal
Follow the instructions here ➡️ [Generative Inpainting GitHub](https://github.com/JiahuiYu/generative_inpainting)

---

## 📂 Datasets & Weights

- 📁 **SAIOD Object Detection Dataset** ➡️ [Download Here](https://drive.google.com/file/d/16HsspfaDDFCXNPKkWUtZzReYs7n-3yo-/view?usp=sharing)
- 📁 **COCO2017 Dataset** ➡️ [Download Here](https://drive.google.com/drive/folders/1_IflcPKwWf3efhkzJ1sel7quEwFZvs2y?usp=sharing)
- 📁 **Trained Occlusion Detection Model File** ➡️ [Download Here](https://drive.google.com/file/d/1u8H-J2mExx-2o7JT43sjedPUWcSXFFDY/view?usp=sharing)

---

## 🎯 Running Inference

### 🔍 Occlusion Detection Inference
```bash
!python3 demo/demo.py --config-file configs/fcos/fcos_imprv_R_101_FPN.yaml --input 'images' --output 'images_output' --opts MODEL.WEIGHTS BCNet/models/output_pth2.pth
```

### 🔍 Occlusion Removal
Follow the instructions here ➡️ [Generative Inpainting GitHub](https://github.com/JiahuiYu/generative_inpainting)

---

🎯 **Contribute & Star ⭐ the repository if you find it helpful!** 🚀
