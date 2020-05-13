[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/fast-visual-object-tracking-with-rotated/visual-object-tracking-on-vot2019)](https://paperswithcode.com/sota/visual-object-tracking-on-vot2019?p=fast-visual-object-tracking-with-rotated)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/fast-visual-object-tracking-with-rotated/visual-object-tracking-on-vot201718)](https://paperswithcode.com/sota/visual-object-tracking-on-vot201718?p=fast-visual-object-tracking-with-rotated)
[![PWC](https://img.shields.io/endpoint.svg?url=https://paperswithcode.com/badge/fast-visual-object-tracking-with-rotated/visual-object-tracking-on-vot2016)](https://paperswithcode.com/sota/visual-object-tracking-on-vot2016?p=fast-visual-object-tracking-with-rotated)
# SiamMask_E
In this project, we demonstrate a novel algorithm that uses ellipse ﬁtting to estimate the bounding box rotation angle and size with the segmentation(mask) on the target for online and real-time visual object tracking. Our method, SiamMask E, improves the bounding box ﬁtting procedure of the state-of-the-art object tracking algorithm SiamMask and still retains a fast-tracking frame rate (80 fps) on a system equipped with GPU (GeForce GTX 1080 Ti or higher). We tested our approach on the visual object tracking datasets (VOT2016, VOT2018, and VOT2019) that were labeled with rotated bounding boxes. By comparing with the original SiamMask, we achieved an improved Accuracy of 65.2% and 30.9% EAO on VOT2019, which is 5.6% and 2.6% higher than the original SiamMask.
 
This repository is the add-on package for [PySOT](https://github.com/STVIR/pysot) project.

## Paper

[Fast Visual Object Tracking with Rotated Bounding Boxes](https://arxiv.org/abs/1907.03892)

## News
Aug. 14, 2019: posted results on datasets: VOT2016, VOT2018, VOT2019.

Aug. 12, 2019: accepted as a workshop paper in ICCV2019 The Visual Object Tracking Challenge Workshop VOT2019.

## Merge file to pysot
```bash
cd siammask_e
bash install.sh [/path/to/pysot]
```

## Webcam demo
```bash
python tools/demo.py \
    --config experiments/siammaske_r50_l3/config.yaml \
    --snapshot experiments/siammaske_r50_l3/model.pth \
    # --video demo/bag.avi # (in case you don't have webcam)
```

## Model
Please use the same model as SiamMask, refer to [PySOT Model Zoo](https://github.com/STVIR/pysot/)

## Short-term Tracking on VOT2016, 2018, 2019
<div align="center">
  <img src="images/table.png" width="800px" />
</div>

## Sample outputs
<div align="center">
  <img src="images/outputs.png" width="800px" />
</div>

## Reference
```
@article{chen2019fast,
title={Fast Visual Object Tracking with Rotated Bounding Boxes},
author={Chen, Bao Xin and Tsotsos, John K},
journal={arXiv preprint arXiv:1907.03892},
year={2019}
}

@article{wang2018fast,
title={Fast Online Object Tracking and Segmentation: A Unifying Approach},
author={Wang, Qiang and Zhang, Li and Bertinetto, Luca and Hu, Weiming and Torr, Philip HS},
journal={arXiv preprint arXiv:1812.05050},
year={2018}
}

@article{li2018siamrpn++,
title={SiamRPN++: Evolution of Siamese Visual Tracking with Very Deep Networks},
author={Li, Bo and Wu, Wei and Wang, Qiang and Zhang, Fangyi and Xing, Junliang and Yan, Junjie},
journal={arXiv preprint arXiv:1812.11703},
year={2018}
}
```
