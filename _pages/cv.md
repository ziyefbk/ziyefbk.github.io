---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **浙江大学** 控制科学与工程学院 · 竺可桢学院工程教育高级班 | 2023.9 -- 至今
  * 自动化（控制）专业 · GPA: 3.91/4.0 · 大三
  * 导师：赵永望 教授（CCF 杰出会员，工信部重大专项首席科学家）
  * 联合导师：袁胜浩 老师（浙江大学区块链与数据安全全国重点实验室）

Research Experience
======
* **使用 Rocq 实现 Linux eBPF 虚拟机指令集形式化语义构建** | 2025.05 -- 至今
  * 在 Rocq (Coq) 中实现 Linux 内核 eBPF 虚拟机指令集的形式化语义
  * 通过官方测试及自动化验证工具验证与原实现语义一致性
  * CCF-A 类编程语言领域顶会论文在投

* **Linux 内核安全关键模块组件研究** | 2025.01 -- 至今
  * 发现 Linux 内核中的潜在缺陷和漏洞，设计并实现修复方案
  * 向上游提交 4 个 patch，相关修复已合入最新版 Linux 内核主线
  * 为 Linux 社区提供开源贡献

* **基于 Rust 的论文复现与性能优化** | 2025.02 -- 2025.05
  * 研究并复现 CCF-A 类程序分析领域顶级会议 ISSTA'25 与 TOPLAS'15
  * 将数值抽象域的 C++ 实现迁移至 Rust，通过 SIMD 并行化与零成本抽象等进行性能优化
  * 开源三个 Rust 库：[Tnum](https://github.com/OpenSourceVerif/Tnum-for-Rust)、[Wrapped Interval](https://github.com/OpenSourceVerif/Wrapped-Interval-for-Rust)、[Reduced Product](https://github.com/OpenSourceVerif/Reduced-Product-for-Rust)，用于 eBPF 静态分析
  * 经基准测试对比，Rust 实现较原 C++ 版本提速约 40%
  * 发现原代码中存在的区间分析 bug，已与原作者沟通确认

## Linux 内核开源贡献
======
* **[bpf: Add bitwise tracking for BPF_END](https://github.com/kernel-patches/bpf/commit/9d21199842247ab05c675fb9b6c6ca393a5c0024)** | upstream kernel
  * 为 BPF_END（字节序转换）指令实现了 bitwise tracking（tnum 分析），增强 BPF verifier 在处理网络协议代码时的验证能力
  * 合入 Linux 内核主线 [Linux 6.14](https://cdn.kernel.org/pub/linux/kernel/v6.14/)

* **[bpf: Add range tracking for BPF_DIV and BPF_MOD](https://github.com/kernel-patches/bpf/commit/44fdd581d27366092e162b42f025d75d5a16c851)** | upstream kernel
  * 为 BPF_DIV 和 BPF_MOD 指令实现了区间分析，减少 BPF verifier 对安全代码的误判
  * 合入 Linux 内核主线 [Linux 6.14](https://cdn.kernel.org/pub/linux/kernel/v6.14/)

* **[bpf: Reject negative offsets for ALU ops](https://github.com/kernel-patches/bpf/commit/55c0ced59fe17dee34e9dfd5f7be63cbab207758)** | upstream kernel
  * 修复了 BPF verifier 中 ALU 指令偏移量检查的缺陷，拒绝负数偏移以防止越界访问

* **[bpf: Reset register ID for BPF_END value tracking](https://github.com/kernel-patches/bpf/commit/a3125bc01884431d30d731461634c8295b6f0529)** | upstream kernel
  * 修复了 BPF_END 操作后寄存器 scalar ID 未正确重置导致 verifier 边界推导错误的问题

* **[bpf: Fix out-of-bounds read in bpf_patch_call_args()](https://lore.kernel.org/bpf/03aec17f262c5c9f1d8b2d1747b2c795a93db7a9.camel@gmail.com/)** | upstream kernel
  * 修复了 bpf_patch_call_args() 函数中的越界读取问题，提升内核安全性

Projects
======
* **计算机视觉与深度神经网络研究** | 2025.04 -- 2025.08
  * Image Classification：从零实现 kNN、SVM、Softmax 分类器及全连接网络，CIFAR-10 达 92% 准确率
  * CNN：实现 BatchNorm、Dropout、卷积模块及 ResNet-18，在 CIFAR-10 上达到 92% 准确率
  * Advanced Vision：实现 Transformer 图像描述生成、DDPM 扩散模型、CLIP 对比图文匹配及 DINO 自监督学习

* **深度学习模型压缩与高效部署研究** | 2025.08 -- 2026.01
  * Pruning：实现 CNN 权重迭代剪枝，削减 80% 参数量的同时 Top-1 准确率下降不超过 2%
  * Quantization：将 ResNet 模型从 FP32 量化至 INT8，设计混合精度量化策略，推理速度提升约 3.1 倍
  * NAS：基于 DARTS 算法实现神经网络架构自动搜索，在 CIFAR-10 上搜索得到参数量仅 0.5M 的轻量化网络
  * LLM Compression & Deployment：对 LLaMA-2-7B 进行 4-bit GPTQ 量化，笔记本本地部署速度达 15 tokens/s

* **嵌入式开发与深度学习：魔杖动作识别与机械狗动作指令控制系统** | 2025.04 -- 2025.12
  * 基于 MPU6050 构建六轴 IMU 传感器数据采集系统，完成时序数据清洗、分割与滑窗特征提取
  * 设计 1-D CNN 特征提取和分类模型，在自采多类别动作数据集上达 97.3% 识别准确率
  * 优化模型参数量并部署至上位 PC 机完成动作识别，驱动电机完成机器狗指定动作指令

Skills
======
* **编程语言：** Python (PyTorch), C/C++, Rust, MATLAB
* **开发技能：** 熟练使用 Linux 系统进行开发；了解 Linux 内核开发流程；熟悉使用 Git 进行版本管理
* **专业基础：** 线性代数、矩阵论、概率论与数理统计、数据结构及算法、运筹学、凸优化、机器学习与深度学习

## 获奖情况
======
* **iGEM 2025 国际遗传工程机器大赛** 银奖
* **浙江大学二、三等奖学金**

## 服务与领导力
======
* 担任硬件设计与开发负责人，参与 2025 iGEM 国际遗传工程机器大赛
