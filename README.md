# Hypocaust

### 项目名称

hypocaust，一个 RISC-V Type-1 hypervisor。

### 项目描述

虚拟化是一个在复杂计算系统和体系结构中被广泛应用的技术。今天我们所认为的大部分系统都是在数据中心强大的服务器上的虚拟机中相互隔离运行的大量应用程序。这些应用的虚拟化特性十分灵活，可以抽象出特定的硬件模式，因此许多软件可以直接运行在许多系统中。虚拟化技术的研究来源于对计算机系统性能和效率的不断追求，它可以解决传统物理系统存在的资源浪费、管理复杂、难以扩展等问题。

本课题将围绕 RISC-V Type-1 hypervisor 进行 ，目标是基于 RISC-V H 扩展设计并实现一款高性能稳定运行的 Type-1 hypervisor。当前国内外学术界和工业界对于 RISC -V Type-1 hypervisor 的研究较少，因此该课题研究有助于促进推动 RISC -V 开源和创新的软硬件生态系统的建立；同时，对于 RISC-V Type-1 hypervisor 的研究有助于为操作系统提供更好的隔离环境。相比于其他移植了 RISC -V 架构的 hypervisor 来说，本课题要求参赛队使用 Rust 语言进行构建，具有内存安全、抽象性强等特性，更便于维护与调试。同时，本课题希望参赛队对于 hypervisor 的性能进行调优，目标是同现有的 type-1 hypervisor 相比在某方面或者某几方面的性能表现更为优秀。

### 所属赛道

2025全国大学生操作系统比赛的“OS功能设计”赛道

### 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求

### 项目导师

齐呈祥

- Email: kuangjux@outlook.com
- Github: KuangjuX

### 难度

中等--高等

### 特征

- 熟悉操作系统/虚拟化/计算机组成原理等基本知识

- 熟悉 Rust 编程语言

- 熟悉 RISC-V 指令集架构

### 参考实现

- [GitHub - KuangjuX/hypocaust-2: hypocaust-2, a type-1 hypervisor with H extension run on RISC-V machine](https://github.com/KuangjuX/hypocaust-2)

### License

- MIT license

## 预期目标

### 注意：下面的内容是建议内容，不要求必须全部完成。选择本项目的同学也可与导师联系，提出自己的新想法，如导师认可，可加入预期目标

**注：建议在参考实现上进行开发，并通过 PR 合并入主线**

### 第一题

实现 hypervisor 的多核、多 guest 扩展，包括以下功能：

- 添加必要的代码，使得 hypervisor 支持多核运行

- 设计一种虚拟 CPU 和物理 CPU 映射方案，使得 hypervisor 可同时支持多个 guest 运行

- 设计一种调度算法，使得 hypervisor 可以支持不同 guest 之间的切换

### 第二题

支持 RISC-V AIA(Advanced Interrupt Architecture)，包括以下功能：

- 根据 RISC-V AIA 标准，为 hypervisor 软件添加 AIA 支持，并可以将其在 QEMU 上验证通过

- 目前市面上仍然没有支持 RISC-V Hypervisor Extension 的芯片，可选择修改支持 RISC-V Hypervisor Extension 的软核(例如：Rocket Chip) 并为其支持 AIA 并搭建 SOC，并将 hypervisor 运行在自己搭建的 SOC 上。

### 第三题

支持 RISC-V IOMMU 草案，包括以下功能：

- 根据 RISC-V IOMMU 草案，为 hypervisor 添加 IOMMU 软件支持，并可以将其在 QEMU 上验证通过

- 目前市面上仍没有支持 RISC-V IOMMU 的芯片，可选择修改支持 RISC-V Hypervisor Extension 的软核(例如：Rocket Chip) 并为其支持 IOMMU 并搭建 SOC，并将 hypervisor 运行在自己搭建的 SOC 上。

### 第四题

支持 RISC-V 嵌套虚拟化，包括以下功能：

- 设计一种方案，可以实现在 RISC-V 平台上进行嵌套虚拟化（例如：在 hypervisor 上运行多个 Guest Linux，这些 Guest Linux 可以通过嵌套虚拟化技术使用 KVM 再进行虚拟化）
