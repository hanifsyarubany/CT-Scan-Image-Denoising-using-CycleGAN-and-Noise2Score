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
