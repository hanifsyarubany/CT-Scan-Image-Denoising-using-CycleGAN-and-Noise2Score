# Adversarial and Score-Based CT Denoising: CycleGAN vs Noise2Score

This repository provides the code, configuration files, and reproducible experiments for the article  
**“Adversarial and Score-Based CT Denoising: CycleGAN vs Noise2Score.”**

It implements and compares two complementary paradigms under a unified CT denoising framework:

- **CycleGAN-based Residual Translator** — an *adversarial*, *unpaired* image translation model.  
- **Noise2Score (N2S)** — a *score-matching*, *self-supervised* denoising model.

The repository enables **fair benchmarking** and **reproducible evaluation** across both paradigms.  
It includes training and testing scripts, dataset preparation utilities, and result analysis modules (PSNR, SSIM).  
The implementation focuses on clarity, minimal dependencies, and ease of extending to new datasets or model architectures.

📝 You can read the full article here:  
👉 [Arxiv](https://arxiv.org/pdf/2511.04083)

## 🚀 Learning Framework

### CycleGAN-based Residual Learning Framework
<p align="left">
  <img src="assets/img_losses.jpg" alt="CycleGAN" width="700"/>
</p>

### Noise2Score Learning Framework
<p align="left">
  <img src="assets/img_n2s_flow.jpg" alt="N2S" width="700"/>
</p>

---

## 🔍 Evaluation

### Qualitative Evaluation
<p align="left">
  <img src="assets/img_qualitative.png" alt="qualitative" width="800"/>
</p>

### Training Loss Curves in CycleGAN
<div align="left">
<table>
  <tr>
    <td align="center" width="50%">
      <img src="assets/img_adv_loss.png" alt="Adversarial Loss" width="340"/>
      <br>
      <em>Adversarial Loss</em>
    </td>
    <td align="center" width="50%">
      <img src="assets/img_cycle_iden.png" alt="Cycle + Identity Loss" width="360"/>
      <br>
      <em>Cycle + Identity Loss</em>
    </td>
  </tr>
</table>
</div>

### Training Loss Curves in Noise2Score
<p align="left">
  <img src="assets/img_n2s_loss.png" alt="n2s_loss" width="500"/>
</p>

---

## ⚙️ Reproducing the Environment
```bash
pip install typing_extensions
pip install torch
pip install numpy
pip3 install Cython
pip install scipy
pip install torch
pip install torchvision
```

---
## 📚 Citation
If you use this work, please consider citing the following foundational papers:
```bibtex
@article{Li2020UnpairedLDCT,
  author  = {Zeheng Li and Shiwei Zhou and Junzhou Huang and Lifeng Yu and Mingwu Jin},
  title   = {Investigation of Low-Dose CT Image Denoising Using Unpaired Deep Learning Methods},
  journal = {IEEE Transactions on Radiation and Plasma Medical Sciences},
  year    = {2020},
  volume  = {5},
  number  = {2},
  pages   = {224--234},
  doi     = {10.1109/TRPMS.2020.3007583},
  url     = {https://pmc.ncbi.nlm.nih.gov/articles/PMC7978404/}
}

@article{Tan2022SKFCycleGAN,
  author  = {Chaoqun Tan and Mingming Yang and Zhisheng You and Hu Chen and Yi Zhang},
  title   = {A Selective Kernel-Based Cycle-Consistent Generative Adversarial Network for Unpaired Low-Dose CT Denoising},
  journal = {Precision Clinical Medicine},
  year    = {2022},
  volume  = {5},
  number  = {2},
  pages   = {pbac011},
  doi     = {10.1093/pcmedi/pbac011},
  url     = {https://pmc.ncbi.nlm.nih.gov/articles/PMC9172657/}
}

@inproceedings{Kim2021Noise2Score,
  author    = {Kwanyoung Kim and Jong Chul Ye},
  title     = {Noise2Score: Tweedie's Approach to Self-Supervised Image Denoising without Clean Images},
  booktitle = {Advances in Neural Information Processing Systems (NeurIPS)},
  year      = {2021},
  url       = {https://papers.neurips.cc/paper/2021/file/077b83af57538aa183971a2fe0971ec1-Paper.pdf}
}

@article{Zhao2025Review,
  author  = {Feixiang Zhao and Mingzhe Liu and Mingrong Xiang and Dongfen Li and Xin Jiang and Xiance Jin and Cai Lin and Ruili Wang},
  title   = {Unsupervised and Self-Supervised Learning in Low-Dose Computed Tomography Denoising: Insights from Training Strategies},
  journal = {Journal of Imaging Informatics in Medicine},
  year    = {2025},
  volume  = {38},
  number  = {2},
  pages   = {902--930},
  doi     = {10.1007/s10278-024-01213-8},
  note    = {Epub 2024 Sep 4},
  url     = {https://pmc.ncbi.nlm.nih.gov/articles/PMC11950483/}
}

@inproceedings{Zhu2017CycleGAN,
  author    = {Jun{-}Yan Zhu and Taesung Park and Phillip Isola and Alexei A. Efros},
  title     = {Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks},
  booktitle = {Proceedings of the IEEE International Conference on Computer Vision (ICCV)},
  year      = {2017},
  pages     = {2223--2232},
  doi       = {10.1109/ICCV.2017.244},
  url       = {https://openaccess.thecvf.com/content_ICCV_2017/papers/Zhu_Unpaired_Image-To-Image_Translation_ICCV_2017_paper.pdf}
}

@inproceedings{Lim2020ARDAE,
  author    = {Jae Hyun Lim and Aaron Courville and Christopher Pal and Chin-Wei Huang},
  title     = {{AR-DAE}: Towards Unbiased Neural Entropy Gradient Estimation},
  booktitle = {Proceedings of the 37th International Conference on Machine Learning (ICML)},
  pages     = {6061--6071},
  year      = {2020},
  publisher = {PMLR},
  volume    = {119},
  series    = {Proceedings of Machine Learning Research},
  url       = {https://proceedings.mlr.press/v119/lim20a.html}
}

@inproceedings{Ronneberger2015UNet,
  author    = {Olaf Ronneberger and Philipp Fischer and Thomas Brox},
  title     = {U-Net: Convolutional Networks for Biomedical Image Segmentation},
  booktitle = {Medical Image Computing and Computer-Assisted Intervention (MICCAI)},
  volume    = {9351},
  pages     = {234--241},
  year      = {2015},
  doi       = {10.1007/978-3-319-24574-4\_28},
  url       = {https://arxiv.org/abs/1505.04597}
}

@inproceedings{Oktay2018AttentionUNet,
  author    = {Ozan Oktay and Jo Schlemper and Loic Le Folgoc and Matthew Lee and Mattias Heinrich and Kensaku Mori and Steven McDonagh and Nils Y. Hammerla and Bernhard Kainz and Ben Glocker and Daniel Rueckert},
  title     = {Attention U-Net: Learning Where to Look for the Pancreas},
  booktitle = {Medical Image Computing and Computer-Assisted Intervention (MICCAI)},
  year      = {2018},
  url       = {https://arxiv.org/abs/1804.03999}
}

@article{Gurrola2021ResidualDenseUNet,
  author    = {Javier Gurrola-Ramos and Oscar Dalmau and Teresa E. Alarc{\'o}n},
  title     = {A Residual Dense U-Net Neural Network for Image Denoising},
  journal   = {IEEE Access},
  volume    = {9},
  pages     = {31742--31754},
  year      = {2021},
  doi       = {10.1109/ACCESS.2021.3061062},
  url       = {https://ieeexplore.ieee.org/document/9431444}
}

@article{Chen2017REDCNN,
  author  = {Hu Chen and Yi Zhang and Mannudeep K. Kalra and Feng Lin and Yang Chen and Peixi Liao and Jiliu Zhou and Ge Wang},
  title   = {Low-Dose CT With a Residual Encoder-Decoder Convolutional Neural Network},
  journal = {IEEE Transactions on Medical Imaging},
  year    = {2017},
  volume  = {36},
  number  = {12},
  pages   = {2524--2535},
  month   = dec,
  doi     = {10.1109/TMI.2017.2715284},
  url     = {https://pmc.ncbi.nlm.nih.gov/articles/PMC5727581/}
}
@inproceedings{Isola2017Pix2PixPatchGAN,
  author    = {Phillip Isola and Jun{-}Yan Zhu and Tinghui Zhou and Alexei A. Efros},
  title     = {Image-to-Image Translation with Conditional Adversarial Networks},
  booktitle = {Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  pages     = {5967--5976},
  year      = {2017},
  doi       = {10.1109/CVPR.2017.632},
  url       = {https://arxiv.org/pdf/1611.07004}
}
```
