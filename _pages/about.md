---
permalink: /
title: "About Me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

## About Me

我是**曹天赐**，浙江大学控制科学与工程学院自动化专业大三学生，竺可桢学院工程教育高级班成员。

我对 MLsys、形式化验证和大语言模型充满热情，目前的研究方向包括：

- 在 [Rocq (Coq)](https://github.com/coq/rocq) 中为 Linux 内核 eBPF 构建形式化语义，支撑后续安全验证研究
- Linux 内核安全关键模块组件研究，发现潜在缺陷并设计实现修复方案
- 机器学习模型压缩：剪枝、量化、NAS 及 LLM 部署优化

## Education

- **浙江大学** — 控制科学与工程学院 · 竺可桢学院工程教育高级班
  - 自动化（控制）专业 · GPA: 3.91/4.0
  - 导师：赵永望 教授（CCF 杰出会员，工信部重大项目负责人）
  - 联合导师：袁胜浩 老师（浙江大学区块链与数据安全全国重点实验室）

## Research Experience

**eBPF 形式语义构建** | 2025.05 — 至今

- 在 Rocq 中实现 Linux eBPF 虚拟机指令集的形式化语义
- 通过官方测试及自动化验证工具验证与原实现语义一致性
- CCF-A 类编程语言领域顶会论文在投

**Linux 内核安全研究** | 2025.01 — 至今

- 发现 Linux 内核中的潜在缺陷与安全漏洞，设计并实现修复方案
- 向上游提交 4 个 patch，已合并至最新版 Linux 内核主线

**Rust 抽象域库开发** | 2025.02 — 2025.05

- 复现 ISSTA'25 和 TOPLAS'15 论文，将 C++ 数值抽象域迁移至 Rust
- 通过 SIMD 向量化与零成本抽象实现约 40% 性能提升
- 开源三个 Rust 库：[Tnum](https://github.com/OpenSourceVerif/Tnum-for-Rust)、[Wrapped Interval](https://github.com/OpenSourceVerif/Wrapped-Interval-for-Rust)、[Reduced Product](https://github.com/OpenSourceVerif/Reduced-Product-for-Rust)，用于 eBPF 静态分析，发布于 [OpenSourceVerif](https://github.com/OpenSourceVerif) 组织

## Projects

- **计算机视觉与深度神经网络**：从零实现 kNN、SVM、ResNet-18 等，CIFAR-10 达 92% 准确率
- **模型压缩与高效部署**：CNN 剪枝（80% 参数）、FP32→INT8 量化（3.1x 加速）、DARTS NAS、LLaMA-2-7B 4-bit GPTQ 本地部署
- **嵌入式与深度学习**：魔杖运动识别与机器狗控制，IMU 数据采集 + 1-D CNN 分类器达 97.3% 准确率

## Contact

- Email: [ziyectc@gmail.com](mailto:ziyectc@gmail.com)
- GitHub: [ziyefbk](https://github.com/ziyefbk)
