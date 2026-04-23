---
title: "Linux Kernel Security Research"
excerpt: "Discovered potential defects and vulnerabilities in the Linux kernel BPF subsystem, designed and implemented fixes. Submitted 5 patches upstream; fixes merged into the latest Linux kernel mainline."
collection: portfolio
---

## Linux 内核安全研究

发现 Linux 内核 BPF 子系统中的潜在缺陷与安全漏洞，设计并实现修复方案。

### 主要工作

- 分析 Linux 内核安全关键模块组件
- 发现潜在缺陷和安全漏洞
- 设计并实现修复方案
- 向上游提交 5 个 patch，已合并至最新版 Linux 内核主线

### 提交记录

- **[bpf: Add bitwise tracking for BPF_END](https://github.com/kernel-patches/bpf/commit/9d21199842247ab05c675fb9b6c6ca393a5c0024)** — 为 BPF_END（字节序转换）指令实现 bitwise tracking（tnum 分析），增强 verifier 在网络协议代码处理中的验证能力
- **[bpf: Add range tracking for BPF_DIV and BPF_MOD](https://github.com/kernel-patches/bpf/commit/44fdd581d27366092e162b42f025d75d5a16c851)** — 为 BPF_DIV 和 BPF_MOD 指令实现区间分析，减少 verifier 对安全代码的误判
- **[bpf: Reject negative offsets for ALU ops](https://github.com/kernel-patches/bpf/commit/55c0ced59fe17dee34e9dfd5f7be63cbab207758)** — 修复 verifier 中 ALU 指令偏移量检查缺陷，拒绝负数偏移以防止越界访问
- **[bpf: Reset register ID for BPF_END value tracking](https://github.com/kernel-patches/bpf/commit/a3125bc01884431d30d731461634c8295b6f0529)** — 修复 BPF_END 操作后寄存器 scalar ID 未正确重置导致边界推导错误的问题
- **[bpf: Fix out-of-bounds read in bpf_patch_call_args()](https://lore.kernel.org/bpf/03aec17f262c5c9f1d8b2d1747b2c795a93db7a9.camel@gmail.com/)** — 修复 bpf_patch_call_args() 函数中的越界读取问题
