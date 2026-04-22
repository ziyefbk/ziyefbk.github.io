---
title: "Rust Abstract Domain Libraries"
excerpt: "Reproduced ISSTA'25 & TOPLAS'15 papers; migrated C++ numerical abstract domains to Rust with ~40% speedup via SIMD vectorization and zero-cost abstractions."
collection: portfolio
---

## Rust 抽象域库

复现 ISSTA'25 和 TOPLAS'15 论文，将 C++ 数值抽象域迁移至 Rust。

### 主要工作

- 研究并复现 CCF-A 类程序分析领域顶级会议论文
- 将数值抽象域的 C++ 实现迁移至 Rust
- 通过 SIMD 向量化与零成本抽象实现约 40% 性能提升
- 发现原代码中存在的区间分析 bug，已与原作者沟通确认

### 开源项目

- [Tnum](https://github.com/OpenSourceVerif/Tnum-for-Rust)
- [Wrapped Interval](https://github.com/OpenSourceVerif/Wrapped-Interval-for-Rust)
- [Reduced Product](https://github.com/OpenSourceVerif/Reduced-Product-for-Rust)

所有项目发布于 [OpenSourceVerif](https://github.com/OpenSourceVerif) 组织，用于 eBPF 静态分析。
