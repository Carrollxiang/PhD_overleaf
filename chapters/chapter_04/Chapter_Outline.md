# 第四章 原子内态操控与里德堡激发 (Internal State Manipulation and Rydberg Excitation)

## 4.1 基态初始化：光抽运 (Optical Pumping)
*   **4.1.1 原理与光路**
    *   $\sigma^+$ 偏振光抽运机制：$D2$ 线 $F=2 \to F'=2$ 的暗态制备 ($|F=2, m_F=2\rangle$) [参考: 2013 PhD [1], [2]]。
    *   再泵浦光 (Repumper) 的作用：防止原子落入 $F=1$ 态。
    *   偏置磁场 (Bias Field) 的配置与量子化轴定义。
*   **4.1.2 偏振与磁场校准**
    *   **校准方法**：利用微波或拉曼光谱测量 Depumping 速率，优化波片角度和补偿线圈电流，使原子在该态的寿命最长（Depumping time maximization）[参考: 2019 PhD [3]]。
    *   **态制备保真度**：通过吹除法 (Blow-away) 测量制备效率。

## 4.2 基态相干操控：微波与拉曼跃迁 (Ground State Coherence)
*   **4.2.1 微波操控 (Global Operations)**
    *   微波天线设计与 $|F=1\rangle \leftrightarrow |F=2\rangle$ 磁偶极跃迁原理。
    *   **拉比振荡 (Rabi Flopping)**：测量 $\pi$ 脉冲时间，确定由于微波功率和失谐导致的广义拉比频率 [参考: 2013 PhD [4], [5]]。
    *   **Ramsey 干涉**：测量基态 $T_2^*$ 相干时间，评估磁场噪声 [参考: 2015 PhD [6]]。
*   **4.2.2 远失谐受激拉曼跃迁 (Local/Fast Operations)**
    *   **原理**：基于 $D1$ 线远失谐 ($\Delta \gg \Gamma$) 的双光子过程，实现高速（$\mu s$级）比特翻转。
    *   **光路系统**：两束拉曼光的频率差锁定（相位锁相环 OPLL 或 注入锁定）[参考: 2013 PhD [7]]。
    *   **光束校准**：
        *   *位置校准*：利用 AC Stark Shift 对原子共振频率的移动来定位光束中心 [参考: 2019 PhD [8]]。
        *   *强度平衡*：优化两束光强比以最大化拉比频率。

## 4.3 里德堡态的双光子激发 (Two-photon Rydberg Excitation)
*   **4.3.1 激发方案概述**
    *   能级选择：$5S_{1/2} \xrightarrow{780nm} 5P_{3/2} \xrightarrow{480nm} nS/nD$ (中间态失谐 $\Delta$)。
    *   有效拉比频率 $\Omega_{\text{eff}}$ 与双光子失谐 $\delta$ 的理论推导（绝热消除中间态）[参考: 2016 PhD [9]]。
*   **4.3.2 激光系统与频率锁定**
    *   780nm 与 480nm 激光器架构（ECDL/TA/SHG）。
    *   **频率校准**：利用 EIT (电磁诱导透明) 信号或 Autler-Townes 分裂在参考泡中锁定频率零点。
    *   **频率稳定**：超稳腔 (ULE Cavity) 锁定方案 [参考: 2018 PhD [10]]。

## 4.4 激发光束的精密校准 (Beam Calibration & Alignment)
*   **4.4.1 空间重合与指向校准**
    *   **粗调**：使用 CCD 相机监测原子荧光损失。
    *   **精调**：利用光致电离 (Photo-ionization) 或 AC Stark Shift 扫描光束位置，寻找原子损失/频移的最大值 [参考: 2013 PhD [11], [12]]。
*   **4.4.2 偏振校准**
    *   利用选择定则（Selection Rules）激发特定 $m_j$ 态，扫描波片角度优化跃迁强度。

## 4.5 相干激发实验结果 (Experimental Results)
*   **4.5.1 双光子拉比振荡 (Rabi Oscillation)**
    *   直接驱动 $|g\rangle \leftrightarrow |r\rangle$。
    *   分析退相干机制：中间态散射、激光相位噪声、多普勒频移 [参考: 2018 PhD [13]]。
*   **4.5.2 受激拉曼绝热通过 (STIRAP)**
    *   **原理**：Counter-intuitive 脉冲序列（先开480nm，后开780nm），利用暗态实现高保真度转移 [参考: 2018 PhD [14]]。
    *   **参数优化**：扫描脉冲延迟 ($\Delta t$) 和脉冲宽度，寻找最高转移效率平台 [参考: 2018 PhD [15]]。
    *   对比直接拉比激发与 STIRAP 的鲁棒性。