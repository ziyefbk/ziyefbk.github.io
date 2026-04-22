---
title: "Model Compression & Efficient Deployment"
excerpt: "CNN pruning (80% params), FP32→INT8 quantization (3.1x speedup), DARTS NAS (0.5M params), LLaMA-2-7B 4-bit GPTQ local deployment at 15 tokens/s."
collection: portfolio
---

## 深度学习模型压缩与高效部署

### Pruning（剪枝）

- 实现 CNN 权重迭代剪枝
- 削减 80% 参数量的同时 Top-1 准确率下降不超过 2%

### Quantization（量化）

- 将 ResNet 模型从 FP32 量化至 INT8
- 设计混合精度量化策略，推理速度提升约 3.1 倍

### NAS（神经架构搜索）

- 基于 DARTS 算法实现神经网络架构自动搜索
- 在 CIFAR-10 上搜索得到参数量仅 0.5M 的轻量化网络

### LLM Compression & Deployment

- 对 LLaMA-2-7B 进行 4-bit GPTQ 量化
- 笔记本本地部署速度达 15 tokens/s
