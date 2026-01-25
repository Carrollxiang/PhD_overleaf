# 第四章 原子内态操控与里德堡激发 (Internal State Manipulation and Rydberg Excitation)

## 4.1 原子态制备与初始化 (State Preparation)
*   **4.1.1 极化态制备 ($|F=2, m_F=2\rangle$)**
    *   $\sigma^+$ 偏振光抽运机制：$D2$ 线 $F=2 \to F'=2$ 的暗态制备 ($|F=2, m_F=2\rangle$) [参考: 2013 PhD [1], [2]]。
    *   再泵浦光 (Repumper) 的作用：防止原子落入 $F=1$ 态。
    *   偏置磁场 (Bias Field) 的配置与量子化轴定义。
    *   光路配置：与 MOT 冷却光同轴或独立光路设计。
*   **4.1.2 钟态制备 ($|F=2, m_F=0\rangle$)**
    *   技术背景：传统单光子 $\pi$ 偏振泵浦的局限性。
    *   **方法一：微波转移法** (Microwave Transfer)：先制备到 $|2,2\rangle$，经由 $|1,1\rangle$ 两次 $\pi$ 脉冲转移至 $|2,0\rangle$ [参考: 593]。
    *   **方法二：拉曼-回泵循环法** (Raman-Depumper Cycle)：结合 795nm Depumper 与 780nm 拉曼光的循环光抽运机制。
*   **4.1.3 偏振与磁场优化流程**
    *   **粗调 (Ensemble Optimization)**：利用偶极阱中的原子系综，监测 795nm Depump 诱导的原子数损耗，粗略优化偏振消光比和磁场方向 [参考: 555]。
    *   **精调 (Single Atom Optimization)**：单原子 Depumping 速率测量与极致优化。
    *   **态制备保真度**：通过吹除法 (Blow-away) 测量制备效率。

## 4.2 基态相干操控 (Ground State Coherence Control)
*   **4.2.1 全局微波操控**
    *   微波天线设计与 $|F=1\rangle \leftrightarrow |F=2\rangle$ 磁偶极跃迁原理。
    *   **拉比振荡 (Rabi Flopping)**：测量 $\pi$ 脉冲时间，确定由于微波功率和失谐导致的广义拉比频率 [参考: 2013 PhD [4], [5]]。
    *   **Ramsey 干涉**：测量基态 $T_2^*$ 相干时间，评估磁场噪声 [参考: 2015 PhD [6]]。
*   **4.2.2 远失谐拉曼光系统 (Raman Laser System)**
*   *   **原理**：基于 $D1$ 线远失谐 ($\Delta \gg \Gamma$) 的双光子过程，实现高速（$\mu s$级）比特翻转。
    *   **技术路线选型**：
        *   *路线 A (弃用)*：光纤 EOM 直接强度调制 (IM)。局限：低功率、高损耗、温漂严重。
        *   *路线 B (采用)*：自由空间相位调制 (PM) + 体光栅 (VBG/Chirped Bragg Grating)。优势：高功率耐受、无源温控稳定、相位-强度调制转换效率高 [参考: 580, 585]。
    *   **光路构建**：6.8 GHz 边带产生与光学锁相。
*   **4.2.3 拉曼光束的校准与对齐 (Calibration & Alignment)**
    *   **空间重合 (粗调)**：
        *   辅助光法：混入微弱 780nm Repump 光，利用单原子成像时的荧光计数（无回泵则暗）定位光束中心。
    *   **精密校准 (Fine Tuning)**：
        *   **差分光频移法 (Differential Light Shift)**：利用强拉曼光（无调制）对 $|1,0\rangle \leftrightarrow |2,0\rangle$ 产生的 MHz 级频移。
        *   **原位成像**：扫描微波频率测绘光频移分布，反推拉曼光在阵列平面的强度分布 [参考: 574]。
        *   **功率稳定性监测**：利用微波 Ramsey 序列对光强噪声的敏感性进行评估。
    *   **参数优化**：EOM 调制深度优化与单光子失谐匹配（匹配 VBG 衍射效率曲线）。
    *   

    *   
## 4.3 里德堡态的双光子激发 (Two-photon Rydberg Excitation)
*   **4.3.1 激发方案与激光系统**
    *   能级选择：$5S_{1/2} \xrightarrow{780nm} 5P_{3/2} \xrightarrow{480nm} nS/nD$ (中间态失谐 $\Delta$)。
    *   有效拉比频率 $\Omega_{\text{eff}}$ 与双光子失谐 $\delta$ 的理论推导（绝热消除中间态）[参考: 2016 PhD [9]]。
    *   **频率锁定系统**：
        *   780 nm：基于 MOT 同源光的移频锁定。
        *   480 nm：超稳腔 (ULE) 锁定与参考泡稳频 [参考: 566]。
*   **4.3.2 480 nm 激光的频率寻找流程 (Frequency Search Protocol)**
    *   **步骤 1：MOT 耗散谱 (Coarse)**。常开 480nm 光照射 MOT，利用高功率 780nm 和梯度磁场环境下的原子高激发率，观测 MOT 荧光数下降 [参考: 393]。
    *   **步骤 2：阱中耗散谱 (Intermediate)**。在静态光镊中，长脉冲 (ms级) 照射。利用光镊光引起的基态展宽 (Broadening, ~20 MHz)，在大范围内寻找里德堡共振峰。
    *   **步骤 3：自由空间拉比谱 (Fine)**。逐步降低阱深直至完全关闭（自由空间），缩短脉冲时间，扫描出傅里叶极限线宽的拉比谱。
*   **4.3.3 光束校准与对齐**
    *   **CCD 辅助对齐**：利用高灵敏相机直接监视 480nm/780nm 光斑位置 [参考: 604]。
    *   **偏振校准**：针对 780nm (激发)、480nm 和拉曼光分别进行波片角度扫描优化。

## 4.4 相干激发实验结果 (Experimental Results)
*   **4.4.1 双光子拉比振荡 (Rabi Oscillation)**
    *   直接驱动 $|g\rangle \leftrightarrow |r\rangle$。
    *   分析退相干机制：中间态散射、激光相位噪声、多普勒频移 [参考: 2018 PhD [13]]。
*   **4.4.2 受激拉曼绝热通过 (STIRAP)**
    *   **原理**：Counter-intuitive 脉冲序列（先开480nm，后开780nm），利用暗态实现高保真度转移 [参考: 2018 PhD [14]]。
    *   **参数优化**：扫描脉冲延迟 ($\Delta t$) 和脉冲宽度，寻找最高转移效率平台 [参考: 2018 PhD [15]]。
    *   对比直接拉比激发与 STIRAP 的鲁棒性。