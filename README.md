# Mamba-Shield
A High-Throughput Network Intrusion Detection System based on State Space Models (Mamba).
# Mamba-Shield: 高效网络入侵检测系统

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?logo=PyTorch&logoColor=white)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Mamba-Shield 是一个基于状态空间模型（Selective State Space Models, Mamba）的轻量级、高吞吐量网络入侵检测系统（NIDS）。本项目旨在将前沿的序列建模架构应用于网络安全防御，解决传统 Transformer 模型在处理长周期网络流量时计算复杂度过高的问题。

## 📌 项目背景与核心优势

在真实的网络攻防对抗中，高级持续性威胁（APT）往往跨越较长的时间维度。传统的深度学习检测模型在处理超长网络数据包序列时面临显存瓶颈。

本项目引入 Mamba 架构，具备以下核心优势：
* 线性复杂度计算：相比于自注意力机制的 $O(N^2)$ 复杂度，Mamba 实现了 $O(N)$ 的时间复杂度，能够极速处理海量日志。
* 长序列上下文感知： 能够有效捕捉被恶意拉长请求间隔的隐蔽扫描和低频攻击。
* 工程友好： 基于 PyTorch 构建，支持主流开源网络安全数据集的快速接入与评估。

## 🚀 开发路线图 (Roadmap)

本项目正处于活跃开发阶段，后续将逐步完善以下功能：

- [ ] Phase 1: 基础框架搭建
  - [x] 初始化 GitHub 仓库。
  - [ ] 整合 Time-Series-Library (TSLib) 作为底层训练框架。
- [ ] Phase 2: 数据流水线构建
  - [ ] 编写针对常见网络流量数据集（如 CIC-IDS-2017）的预处理清洗脚本。
  - [ ] 实现兼容 PyTorch 的自定义 `DataLoader`。
- [ ] Phase 3: 核心模型重写
  - [ ] 定制 1D-Mamba 块，适配网络流量的离散特征提取。
  - [ ] 开发异常分类模块（支持二分类与多分类）。
- [ ] Phase 4: 性能评估与对比
  - [ ] 完善评估指标（Accuracy, Precision, Recall, F1-Score）。
  - [ ] 开源与 Baseline 模型的可视化对比结果。

## 🛠️ 快速开始 (即将推出)

环境依赖与运行指南将在 Phase 1 与 Phase 2 完成后同步更新，敬请期待。
