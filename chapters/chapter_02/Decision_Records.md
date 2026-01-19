# 编辑决策记录 (Editorial Decision Records - EDR)

## 术语与符号约定 (Terminology & Notation)

### EDR-001: 核心术语中文化对应表
*   **状态**: [已采纳]
*   **内容**:
    *   Optical Tweezers -> **光镊** (用于指代阵列生成工具)
    *   Optical Dipole Trap -> **偶极阱** (用于讨论物理势阱原理时)
    *   Rearrangement / Sorting -> **原子重排** (统一使用此术语，强调从无序到有序)
    *   Single Atom Detection -> **单原子成像** 或 **单原子分辨探测**
    *   Acousto-Optic Deflector -> **声光偏转器** (AOD)
    *   Spatial Light Modulator -> **空间光调制器** (SLM)

### EDR-002: 物理符号规范
*   **状态**: [已采纳]
*   **内容**:
    *   拉比频率: 使用 $\Omega$ (不使用 $\omega_R$)。
    *   失谐量: $\Delta = \omega_{laser} - \omega_{atom}$ (蓝失谐为正，红失谐为负)。
    *   主量子数: $n$ (里德堡态); 有效主量子数: $n^*$。
    *   超精细能级: $F$, 磁量子数 $m_F$。

## 内容取舍决策 (Content Scope Decisions)

### EDR-003: 激光冷却理论深度
*   **问题**: 激光冷却是否需要推导 Fokker-Planck 方程？
*   **决策**: **否**。
*   **理由**: 论文侧重于系统搭建与工程实现。理论部分仅需涵盖多普勒冷却极限温度公式及 PGC 的定性半经典图像 (Sisyphus cooling)，无需深入量子统计力学推导。

### EDR-004: SLM 全息算法描述
*   **问题**: 是否介绍 SLM 的硬件液晶物理原理？
*   **决策**: **否**，仅介绍 GS 算法。
*   **理由**: 重点在于如何生成光镊阵列。硬件细节属商业产品说明，重点应放在相位恢复算法 (Gerchberg-Saxton Algorithm) 的迭代逻辑及对阵列均匀性的影响上。[参考: 2016 PhD@Rydberg... Ch.3]

### EDR-005: 场电离 (Field Ionization) 模型选择
*   **问题**: 场电离涉及复杂的量子隧穿，理论描述到什么深度？
*   **决策**: 采用 **半经典鞍点模型 (Classical Saddle Point Model)**。
*   **理由**: 实验中的探测主要依赖电离阈值 ($E \propto 1/16n^{*4}$) 进行态分辨。半经典模型足以解释不同 $n$ 态在不同电压下出峰的现象，且物理图像直观。[参考: 2013 PhD@Measurement... Appx B]
