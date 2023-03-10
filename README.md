
## Introduction

### [ARS-DETR: Aspect Ratio Sensitive Oriented Object Detection with Transformer](https://arxiv.org/abs/2303.04989)

## Abstract

Existing oriented object detection methods commonly use metric AP50 to measure the performance of the model. We argue that AP50 is inherently unsuitable for oriented object detection due to its large tolerance in angle deviation. Therefore, we advocate using high-precision metric, e.g. AP75, to measure the performance of models. In this paper, we propose an Aspect Ratio Sensitive Oriented Object Detector with Transformer, termed ARS-DETR, which exhibits a competitive performance in high-precision oriented object detection. Specifically, a new angle classification method, calling Aspect Ratio aware Circle Smooth Label (AR-CSL), is proposed to smooth the angle label in a more reasonable way and discard the hyperparameter that introduced by previous work (e.g. CSL). Then, a rotated deformable attention module is designed to rotate the sampling points with the corresponding angles and eliminate the misalignment between region features and sampling points. Moreover, a dynamic weight coefficient according to the aspect ratio is adopted to calculate the angle loss. Comprehensive experiments on several challenging datasets show that our method achieves competitive performance on the high-precision oriented object detection task. Source code will be made publicly available.

## Results and models

DOTA1.0

|         Backbone         | AP50  | AP75  | Angle | lr schd | Aug  | Batch Size |                           Configs                            |                           Download                           |
| :----------------------: | :---: | ----- | :---: | :-----: | :--: | :--------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| ResNet50 (1024,1024,200) | 63.42 | 26.92 | le90  |   3x    |  -   |     2      | [deformable_detr_r50_dota](configs/ars_detr/deformable_detr_r50_dota.py) | [model](https://1drv.ms/u/s!AsmpWJamS0mRf7JkW3wV_2dGhBk?e=t3VkgJ) \|[model(baidu(rdsp))](https://pan.baidu.com/s/12xNB5xYj2v-FYwdAOl-dTw) \|[log](https://1drv.ms/u/s!AsmpWJamS0mRgQVckn69UzQpHx-S?e=sXyO36)
| ResNet50 (1024,1024,200) | 72.08 | 43.22 | le90  |   3x    |  -   |     2      |     [csl_detr_r50_dota](configs/ars_detr/csl_detr_r50_dota.py)      | [model](https://1drv.ms/u/s!AsmpWJamS0mRgQBmD3NwjSz4yMq9?e=adE1lc)\|[model(baidu(hd8m))](https://pan.baidu.com/s/1ljeiRR8-GYcSDNyhvR5YIA) \|[log](https://1drv.ms/u/s!AsmpWJamS0mRgQRpe8OXons1_Bmp?e=fJZ1Ji) |
| ResNet50 (1024,1024,200) | 72.66 | 45.64 | le90  |   3x    |  -   |     2      |   [arcsl_detr_r50_dota](configs/ars_detr/arcsl_detr_r50_dota.py)    | [model](https://1drv.ms/u/s!AsmpWJamS0mRgQHpsBm_BV8QIpZv?e=geZKEx)\|[model(baidu(0afe))](https://pan.baidu.com/s/1Rv3XauFi3_ypbAtT6GC06A) \|[log](https://1drv.ms/u/s!AsmpWJamS0mRgQaC1y0yiDRr6OIG?e=kOWiaw) |
| ResNet50 (1024,1024,200) | 73.42 | 48.41 | le90  |   3x    |  -   |     2      | [dn_arw_arm_arcsl_rdetr_r50_dota](configs/ars_detr/dn_arw_arm_arcsl_rdetr_r50_dota.py) | [model](https://1drv.ms/u/s!AsmpWJamS0mRgQLIqpXPR5jzLNxo?e=EgP5Gp)\|[model(baidu(hlkv))](https://pan.baidu.com/s/1TClQJVDx5KFxMzAkKT8WNw) \|[log](https://1drv.ms/u/s!AsmpWJamS0mRgQfZYSar_PNTwm_0?e=MPzbFz) |




## Installation

Please refer to the official guide of [MMRotate 0.x](https://github.com/open-mmlab/mmrotate) or [install.md](docs/en/install.md) for installation guide.

## Get Started

Please see [get_started.md](docs/en/get_started.md) for the basic usage of MMRotate.

## Data Preparation

Please refer to [data_preparation.md](tools/data/README.md) to prepare the data.

## Acknowledgement

MMRotate is an open source project that is contributed by researchers and engineers from various colleges and companies. We appreciate all the contributors who implement their methods or add new features, as well as users who give valuable feedbacks. We wish that the toolbox and benchmark could serve the growing research community by providing a flexible toolkit to reimplement existing methods and develop their own new methods.

## Citation
```
@article{zeng2023ars-detr,
  title={ARS-DETR: Aspect Ratio Sensitive Oriented Object Detection with Transformer},
  author={Zeng, Ying and Yang, Xue, Li, Qingyun and Chen, Yushi and Yan, Junchi},
  journal={arXiv preprint arXiv:2303.04989},
  year={2023}
}
```
