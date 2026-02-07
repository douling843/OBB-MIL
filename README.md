# OBB-MIL <img src="linux-original.svg" width="5%">  <img src="python-original.svg" width="5%">  <img src="pytorch-icon.svg" width="5%">  <img src="github.svg" width="5%">


![image text](https://github.com/douling843/OBB-MIL/blob/main/fig-1.png)  

⚡   This repository includes the official implementation of the paper:  

👋  **OBB-MIL: Oriented Ship Detection Based on Multiple Instance Learning and SAM-Driven Noise Annotation Recalibration in SAR Images**

👨‍💻   **Code:** [GitHub](https://github.com/douling843/OBB-MIL/edit/main)

## Installation  <img src="images/Installation.svg" width="4%">


- <span> Step 1. Create a conda environment and activate it.


`conda create --name OBB-MIL python=3.8 -y`  
`conda activate OBB-MIL`

- <span> Step 2. Install PyTorch following official instructions, e.g.
 
`Step 2. Install PyTorch following official instructions, e.g.`

- <span> Install
- <span> Step 0. Install MMCV and MMDetection using MIM.
`pip install -U openmim`    
`mim install mmcv-full`  
`mim install mmdet\<3.0.0`  

- <span> Install MMRotate.
`git clone https://github.com/open-mmlab/mmrotate.git`
`cd mmrotate`
`pip install -v -e .`


## Train <img src="images/train.svg" width="4%">
` CUDA_VISIBLE_DEVICES=1 python tools/train.py configs/rotated_faster_rcnn/rotated_faster_rcnn_r50_fpn_3x_ssdd_le90_03_5_mask2obb.py --work-dir='work_dir/ssdd/rotated_faster_rcnn_r50_fpn_3x_ssdd_le90_03_5_mask2obb' ` 

## Test   <img src="images/inf.svg" width="4%">
`CUDA_VISIBLE_DEVICES=1 python ./tools/test.py configs/rotated_faster_rcnn/rotated_faster_rcnn_r50_fpn_3x_ssdd_le90_03_5_mask2obb_MIL.py work_dir/ssdd/rotated_faster_rcnn_r50_fpn_3x_ssdd_le90__03_5_mask2obb_MIL/epoch_36.pth --show-dir work_dirs/vis/ssdd/rotated_faster_rcnn_r50_fpn_3x_ssdd_le90__03_5_mask2obb_MIL
`


## Acknowledgement  📫

This repository is based on [mmdetection](https://github.com/open-mmlab/mmdetection) 🤝  and [MMRotate](https://github.com/open-mmlab/mmrotate) 👯.

This repository is based on [mmdetection](https://github.com/open-mmlab/mmdetection) 🤝  and [OA-MIL](https://github.com/cxliu0/OA-MIL) 👯.

