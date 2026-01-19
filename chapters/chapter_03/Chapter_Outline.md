# 第三章 实验装置与控制系统 (Experimental Setup and Control)

## 3.1 真空系统设计 (Vacuum System)
*   **3.1.1 双腔差分系统架构**
    *   上层：2D MOT 源腔 (Source Chamber) 设计与压力梯度控制 [6-8]
    *   中间连接：差分管/孔 (Differential Pumping Tube) 的流阻计算 [9, 10]
    *   下层：3D MOT 科学腔 (Science Chamber) 与超高真空维持 [11, 12]
*   **3.1.2 原子源与输运**
    *   Rb 分配器 (Dispenser) 与 2D MOT 磁场构型 [13]
    *   推原子光 (Push Beam) 的光路设计与原子通量优化 [14]

## 3.2 激光与光学系统 (Optical Systems)
*   **3.2.1 冷却与俘获光源 (780 nm)**
    *   外腔半导体激光器 (ECDL) 与锥形放大器 (TA) 架构 [15]
    *   频率锁定稳频系统 (SAS/PDH) [16, 17]
*   **3.2.2 D1 线成像与冷却光源 (795 nm)**
    *   $\Lambda$-enhanced gray molasses 的光路配置 (EOM 产生边带) [18]
    *   成像光与冷却光的时序复用设计
*   **3.2.3 偶极阱光源**
    *   高功率陷阱光 (如 1064 nm 或 850 nm) 的光束质量控制 [19, 20]

## 3.3 光镊阵列生成与控制 (Tweezer Array Generation)
*   **3.3.1 静态阵列生成 (SLM)**
    *   空间光调制器 (SLM) 的光路映射与傅里叶平面配置 [21]
    *   高数值孔径 (NA) 物镜系统的像差校正与焦点表征 [22, 23]
    *   基于 GS 算法的加权全息图生成与均匀性反馈 [24]
*   **3.3.2 动态阵列生成 (AOD)**
    *   双轴声光偏转器 (2D AOD) 系统搭建 [25]
    *   射频驱动系统 (RF Drivers) 与频率-位置校准 [26]

## 3.4 实验时序与控制 (Sequence & Control)
*   **3.4.1 时序控制系统 (FPGA/DDS)**
*   **3.4.2 典型实验时序**
    *   MOT 加载 $\to$ PGC $\to$ 光镊装载 $\to$ 成像 $\to$ 重排 $\to$ 实验操作 $\to$ 读出 [27, 28]

## 3.5 单原子成像与探测 (Imaging & Detection)
*   **3.5.1 成像光路设计**
    *   EMCCD 相机配置与感兴趣区域 (ROI) 设置 [29]
    *   背景噪声抑制与滤光片选择 [30]
*   **3.5.2 D1 线成像机制**
    *   利用 795 nm 灰莫拉斯光实现“原位冷却成像” (In-trap cooling & imaging)
    *   直方图分析与保真度计算 [29]

## 3.6 原子重排与移动系统 (Atom Assembly)
*   **3.6.1 移动光镊算法**
    *   从 2D AOD 频率映射到空间坐标的查找表 (LUT) [31]
    *   最短路径规划与防碰撞算法 (Collision-free algorithms) [32]
*   **3.6.2 移动与静态光镊的切换与对齐**
    *   AOD 与 SLM 坐标系的配准 (Registration)
    *   原子在该过程中的交接 (Handover) 效率优化 [26]
