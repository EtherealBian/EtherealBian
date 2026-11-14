# Xiangyu Bian

南京理工大学 · 通信工程 ｜ 东南大学 · 保研-网络安全

[个人主页 / Personal website](https://etherealbian-home.unitedlabel4.chatgpt.site/) · [Email](mailto:EtheralBian@njust.edu.cn)

我主要做 FPGA 数字系统、信号处理和量子计算硬件相关工程。

## 实习经历

**太一量生（上海）量子科技有限公司 · 控制算法工程师**

2026.10–至今

- **CXP 采集与显示**。在 ZCU216 上实现两版 CXP 采集与显示系统，分别对接滨松 C15550-22UP 相机和星测电子 PCIe-1005 CXP 模拟卡。设计 CXP 至 AXI-Stream 转换和 FIFO 背压缓冲，搭建 SGDMA 写入 PL DDR、CDMA 搬运至 PS DDR 的两级通路，并实现 AXI DMA 直写 PS DDR 的备选路径。在 PetaLinux 下通过 UDP 回显图像。
- **HLS 原子检测**。设计 4-bank 行分片 DATAFLOW 流水线，通过三副本行缓存和冲突仲裁解决多读口冲突，实现窗口提取与乘加流水化。用二分法预计算判决边界，将实时浮点比较替换为整数判决。在 300 MHz 下，单帧延迟为 0.268 ms。
- **HLS 原子重排**。将行列扫描的确定性分通道策略实现为 HLS 流水线，依次执行分类、清空通道、批量停靠和缺失补偿。重排受 AOD 双轴各 16 音调上限约束，按波控接口输出每条 5 拍、每拍 512 bit 的 AXI-Stream 指令。
- **AOD 多音调控制**。在 ZCU216 上实现 X/Y 双轴多音调 RF 波形合成。每轴支持 16 音调，通过四路并行 CORDIC 生成连续 I/Q 样本，经多音调求和、包络整形后打包送入 RF-DAC，支持频率配置、扫频与包络控制。
- **链路联调与平台迁移**。参与 Spark 集群与 VCU118 之间的 100G RDMA 通信联调，以及两块 ZCU216 之间的 4 × 12.5G 板间通信联调。参与向 VCU118 迁移，主机通过 PCIe 与 FPGA 交互。

实习期间准备拟投 DAC 2027 的论文。[完整个人主页](https://etherealbian-home.unitedlabel4.chatgpt.site/#experience)

## 工程项目

| 项目 | 内容 |
| --- | --- |
| [eLinex Vision Stream](https://github.com/EtherealBian/elinx-vision-stream) | OV5640 视频采集、FPGA 图像处理与 HDMI / UDP 输出 |
| [Vitis HLS Kernel Optimization](https://github.com/EtherealBian/vitis-hls-kernel-optimization) | 基于 AMD Vitis Libraries 优化 HMAC-SHA256、LZ4 和 Cholesky，附决赛 Zynq 频谱仪 |
| [FPGA Lissajous Controller](https://github.com/EtherealBian/fpga-lissajous-controller) | I/Q 跟踪、CORDIC 与 DDS 波形合成 |
| [N60 Ultrasonic Phased Array](https://github.com/EtherealBian/n60-ultrasonic-phased-array) | 60 路超声相控阵、Python 波束参数计算和 FPGA PWM |

更多项目、实习经历和竞赛记录见[个人主页](https://etherealbian-home.unitedlabel4.chatgpt.site/)。
