# Detectron2 Windows 安裝與測試紀錄 (Detectron2 Windows Installation & Test Log)
How to install Detectron2 on Windows <br>
如何在Windows安裝Detectron2

## 📌 專案簡介 (Project Description)

本專案紀錄了 Facebook AI Research 所開源的物件偵測框架 [Detectron2](https://github.com/facebookresearch/detectron2) 在 Windows 10 平台下的完整安裝與測試過程，並提供 Conda 環境設定檔、pip 安裝流程、測試程式碼與推論成果，供有需求的使用者參考與重現。

This repository documents the complete installation and testing process of [Detectron2](https://github.com/facebookresearch/detectron2), a powerful object detection framework by Facebook AI Research, on a Windows 10 environment. It includes Conda environment setup, pip installation logs, test scripts, and inference results for future reuse and reference.

---

## 💻 系統環境 (System Environment)

| 項目 | 規格 |
|------|------|
| 作業系統 OS | Windows 10 / 11 |
| Python 版本 | 3.8|
| CUDA Toolkit | 11.0 |
| PyTorch | 2.4.1 (CPU 版本 or GPU if available) |
| OpenCV | 4.11 |
| 安裝工具 | Conda + pip |

---

## 🔧 安裝與設定目的 (Purpose)

- 測試在 Windows 環境下安裝 Detectron2 
- 提供他人參考與學習之用

To:
- Verify the feasibility of installing Detectron2 on Windows
- Serve as a reference for others interested in Detectron2 setup

---

## 🧩 Step-by-Step 安裝教學 (Step-by-Step Installation Guide)

本節說明如何在 Windows 上從零開始安裝 Detectron2 並執行推論範例。

This section explains how to install Detectron2 from scratch on Windows and run a sample inference.

---

### 🔧 Step 1：建立 Conda 環境 (Create Conda Environment)

```bash 
conda create -n detectron_env python=3.8 -y #建立虛擬環境 python版本為3.8
conda activate detectron_env #啟用虛擬環境

---

### 📦 Step 2：安裝 PyTorch + CUDA（GPU）

```bash 
conda install pytorch torchvision torchaudio cudatoolkit=11.0 -c pytorch #下載需要的版本

---

### 📁 Step 3：Clone Detectron2 原始碼

```bash 
git clone https://github.com/facebookresearch/detectron2.git
cd detectron2

---

###  📌 Step 4：安裝相關依賴套件

```bash 
pip install -e .
pip install opencv-python
