# -
有关于溺水测试
@@ -0,0 +1,59 @@
# 基于蓝牙4.0的人体上肢运动姿态采集及识别系统研究

为了能够实现运动人员体育运动过程中的动作识别及有效评价，就全面研究了现代化的人 体上肢运动姿态识别方面相关知识，提出了基于蓝牙4.0的人体上肢运动姿态收集及识别系统，全 面收集了运动人员在运动过程中经常使用的运动信息。所设计的系统主要包括信息收集、传输、

动作识别及信号去噪声等部分，最后对系统进行了测试，通过测试结果表示，相互结合传统时域特 征及过零点特征、上四分及下四分的位点特点，能够分离屈肘侧平举和曲臂弯曲静止，以此有效提 高上肢运动姿态识别的效率。

##### 运动姿态收集和识别系统

运动姿态收集和识别系统主要包括多个模块构成，比如姿态检测单元、数据收集单元、数据处理单 元、通信模块等，此系统已经是以现代加速度传感器 及惯性测量技术为基础，实现人体运动姿态信息收 集和计算，从而得出输出结果。利用运动姿态检测系统实现人体运动姿态数据的收集之后处理，并且 将其到计算机中传输，从而实现之后的处理和姿态运动；

##### 数据收集

数据收集模块属于人体运动姿态识别系统中的 最底层，是得到人体运动信息的主要途径，此模块通 过集成收集装置中加速度传感器得到人体运动过程 中的加速度信号，并且将数据对终端进行传输，所得 到加速度数据质量和识别系统性能具有密切的联 系。目前，并没有标准数据收集平台，并且标准的数 据集也较少，所以就要设计能够满足自身需求的收 集装置[9]。图4为数据收集平台和硬件结构。

在实现数据收集器设计的过程中，一般会将加 速度传感器、数据存储等模块都在收集器中集成，之 后利用某种数据传输方式使收集器存储数据能够到 计算机设备和其他设备中进行传输及处理。利用传 输技术实现有线及无线传输的划分。

##### 特征的收集

在收集原始加速度信号值或者利用预处理加
速度信号值，虽然其能够在人体姿态识别系统中使 用，但是原始的加速度辛哈之中的人体运动物理意 义比较狭隘，识别率较低。在人体运动姿态识别系 统中，一般都是会对原始加速度信号值实现特征选
择和提取，并。目前，特征提取和选择并没有统一标 准，不同系统识别行为及分类方法不同，所以使用的 信号特征也不同，不同特征对于分类器识别效率的 影响也会不同。一般通信信号的分析方式主要包括
频域分析、时域分析、时频分析；

##### 加速度传感器

可以佩戴的设备传感器的体积要小，并且成本 和功耗要低，要求具有较高的灵敏度，所以可以使用微电子机械系统传感器，其能够保证数据传输过程 中没有迟延，并且还能够连接磁力计，适应于穿戴设 备产品中开发使用，并且其具有较高的灵敏度。综合考虑低成本、低功耗及频段开放等3方面的因素，选择数据传输的方式。

通过蓝牙4.0方式实现数据传输， 从而能够保证可穿戴设备在静态丁作时候能够长时 间使用，并且此芯片的价格比价便宜，便于量产和研
究，蓝牙4.0也具有开放性的频段，所以能够实现主机及从机的数据传输。

##### 姿态收集系统

姿态核心处理部分主要包括CC2451处理器作 为核心创建下位机，主要包括从机与主机，从机中具 有加速度收集芯片的集成。系统实现数据包的发送 主要包括：

1) 将主机和从机打开，保证主机和从机相互拦 截；

2)  上位机下法收集指令对主机进行发送，主机 接收到指令之后对从机发送，以此收集数据。图6 为主机的运行逻辑。

3）从机中的MPU加速度传感器收集运动过程 中的三轴加速度信息和陀螺仪信息，从而得到人体 上肢运动过程中的运动信息，并且从机对蓝牙传送 实施数据。

##### 上肢运动姿态的数据收集

在上肢运动，上肢在竖直轴、水平轴和纵轴3个 方向都会具有加速度，利用SMP软件编程将加速度 值转换成为角度信息，这个时候就能够收集上肢空 间中俯仰角、横滚角和航偏角的信息。在人体运动 的时候因为运动频率和幅度都会出现不同的变化， 所以这3个方向具有一定的差别，从而就要实现人 体建模，图8为人体的模型。

在进行数据收集的过程中，要在上臂相同位置 中佩戴收集仪器，之后将收集的数据根据相同的模 式实现数据处理，为了能够有效提高收集数据精准 性，要想避免数据在收集过程中收集上肢触碰的物 体，从而产生较大的加速度；

##### 系统的调试

在创建系统硬件和软件之后，就要设计调试方 案测试系统整体的功能，本文研究系统主要包括硬 件及软件的代码，其在调试过程中具有多种方法，并 且也能够使用多种工具。通过系统局部及整体调 试，发现系统中存在的漏洞并且完善。

在调试硬件过程中，首先创建具有VGA显示器 及SDRAM工程，使其能够成为显示器缓存，之后在 显示器中显示，表示能够将图像显示出来。在调试 图像收集、存储和显示之后，表示硬件系统中的各个 模块都能够正常的工作。

在本文系统中，软件的调试主要是利用编程实 现验证，其主要目的就是查看数据是否能够正常的 读取，从而保证后续的处理精准度。对图片进行水 平扫描，输出灰度256色，设置最大的高度及宽度都 为112,输出的类型为C语言，将图像信息文件实现编程测试，对数据正确性进行测试。由于图像处理过程中具有多种算法，所以就要使用大量测试样本 实现对比分析算法，通过对比验证之后，在Nios平台 中实现。在完成每部操作处理之后，对函数进行调 用，以此在显示屏中显示处理的结果，从而对实时处 理结果进行查看；在调试硬件及软件之后创建系统整体输入。

##### 系统的测试

 通过系统调试之后，系统摄像头能够实时的实
现目标图像的收集，并且在显示器中显示收集的图 像|17]。在运行之后，系统模块运行正常，没有其他异 常现象，表示系统设计正确。
