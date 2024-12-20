# Efficient Fine-Tuning of Vision Transformers with LoRA for Image Classification

## Overview

This project explores efficient fine-tuning of Vision Transformers (ViTs) for ultrasound image classification using Low-Rank Adaptations (LoRA), AdaLoRA, Skip-ViT, Post-Training Quantization (PTQ), and Quantization-Aware Training (QAT). We targeted resource-constrained environments to reduce computational overhead while preserving high accuracy.

## Project Structure

```
├── Code-LoRA
│   ├── ABHIK - Adalora.ipynb
│   ├── ABHIK - DeiT_LoRA.ipynb
│   ├── ABHIK - LoRA_Initial.ipynb
│   ├── ABHIK - Skip_ViT.ipynb
│   └── ABHIK - ViT_OldvNew_Implementation_ViT_Pretrained.ipynb
├── Quantization-Code
│   └── PTQ_Notebook.ipynb
│   └── QAT_Notebook.ipynb
└── .gitignore
└── LICENSE
└── README.md

```


## Key Features

### Model Fine-Tuning Techniques:

- LoRA: Introduces low-rank matrices into model layers to reduce trainable parameters.

- AdaLoRA: Dynamically reallocates resources using singular value decomposition (SVD).

- Skip-ViT: Reduces computation by skipping less informative tokens.

### Quantization Approaches:

- PTQ: Post-training quantization to int8 reduces memory usage.

- QAT: Quantization-aware training for improved accuracy in quantized models.


## How to run project

1. Clone the repository:

```bash
git clone https://github.com/your-repo/efficient-vit-finetuning.git
```
2. For LoRA, run the Jupyter notebooks in the `Code-LoRA` directory.
3. For quantization, run the Jupyter notebooks in the `Quantization-Code` directory.

## Results

![metrics](https://github.com/user-attachments/assets/fc01725e-929e-4b99-a124-d62c2632eb6a)
<p style="text-align: center;"><em>Figure 1: Performance comparison of the best models, from each instance of fine-tuning (using LoRA, AdaLoRA, SkipViT) on the Ultrasound Dataset, compared with a baseline of ResNet-18 Architecture
</em></p>

<img width="1342" alt="all_attentionheads_vit" src="https://github.com/user-attachments/assets/89434ad1-1e0f-499c-a1a0-6200978a35f1" />
<p style="text-align: center;"><em>Figure 2: Performance metrics while fine-tuning all attention heads of ViT with LoRA, across multiple ranks 
</em></p>


<img width="1321" alt="all_encoder_layers_vit" src="https://github.com/user-attachments/assets/c2f381ed-0c87-4e7e-ba68-236c38a7eb7f" />

<p style="text-align: center;"><em>Figure 3: Performance metrics while fine-tuning all encoder layers of ViT with LoRA, across multiple ranks
</em></p>

<img width="1324" alt="deit_all_attentionheads" src="https://github.com/user-attachments/assets/62ed5be7-4c53-42bb-b146-c13c073677f1" />

<p style="text-align: center;"><em>Figure 3: Performance metrics while fine-tuning all encoder layers of DeiT with LoRA, across multiple ranks
</em></p>


![correct_preds](https://github.com/user-attachments/assets/670c9f43-b256-431d-ba2f-9cb0d3852c5b)
<p style="text-align: center;"><em>Figure 4: Model Predictions
</em></p>
