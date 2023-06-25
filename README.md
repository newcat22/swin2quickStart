# 训练测试指南

## 一 运行使用

前置条件：CUDA==11.1

### 1.1 环境安装

创建conda虚拟环境

conda create -n your_env_name python=3.10.11

安装依赖
pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113


pip install -r requirements.txt

模型，测试数据已经包含在项目中，无需下载。

### 1.2 运行测试

python main_test_swin2sr.py --task compressed_sr --scale 4 --training_patch_size 48 --model_path model_zoo/swin2sr/Swin2SR_CompressedSR_X4_48.pth --folder_lq ./inputs --save_img_only

结果在results目录下

## 二 模型训练

训练代码位于 KAIR。 遵循与 Jingyun Liang 的 SwinIR 相同的训练设置。详细训练细节见论文。

[GitHub - cszn/KAIR: Image Restoration Toolbox (PyTorch). Training and testing codes for DPIR, USRNet, DnCNN, FFDNet, SRMD, DPSR, BSRGAN, SwinIR](https://github.com/cszn/KAIR/)
