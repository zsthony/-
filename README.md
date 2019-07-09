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

@@ -0,0 +1,69 @@
# 传感器人体运动行为特征识别研究进展

##### 人体运动行为特征识别

用于运 动数据采集的传感器和相应方法，简述了运动数据预处理的一般手段;介绍了运动数据特征提取的过程，重点描述了常见运动行为特征识别方法的研究现状，并简述其应用现状。

人体运动行为直观的表现是四肢及躯干有目的的移动，并可通过人体位移、肢体速度和加速度、关节受 力、表面肌电等可被监测的运动参数进行表征。

加速度传感器、压力传感器以及表面肌电装置是三种最常 用的获取人体运动数据的传感器。

原始的运动数据通常存在噪点，并且数据持续的 时间较长，数据量巨大。因此，常需要对原始的运动数 据进行预处理，具体方法包括对运动数据进行滤波和数据分割等。

##### 运动数据的获取

基于加速度传感器、压力传感器以及表面肌电的三
种运动数据获取方法，可分别采集到人体的运动学参 数、动力学参数和生理参数，这些参数是人体运动行为 不同形式的表现。表面肌电信号强度一般较微弱，通常 需要使用专业设备进行采集，因此多在实验室环境下进
行;而压力传感器一般用于采集足底压力和关节力，使 用过程中容易受到磨损，影响数据的准确获取;而加速 度传感器相比前两种传感器具有体积小、易于应用的特 点，同时加速度数据也较为直观，因此运动行为特征识别系统中大多包含有加速度传感器模块。

基于加速度传感器加速度传感器是进行人体运动 行为特征识别研究中使用最普遍的一种惯性传感器。 随着MEMS技术的不断进步，在目前的研究中常采用 多轴加速度传感器来对人体运动的加速度数据进行采 集。通过将传感器安装或佩戴在人体的胸前、腰部、 腕部、踝关节等位置，可以对相应部位的加速度、角 速度变化情况进行测量。另外，还可通过内置有加速度 传感器的智能手机、智能手表等设备来对人体运动的加速度数据进行采集

基于压力传感器人体行走时的步态是运动行为特 征识别较为关注的方面之一，步态参数包括步长、步频、摆动时间、支撑时间等。

在对步态的研究中，会利用压力传感器来对步行时的足底压力数据进行采集。通 过在鞋垫内安装多个单点式压力传感器，可以实现对足 底压力数据的实时采集；

##### 滤波与数据分割是运动行为特征识别研究中常用的两种数据预处理方法

在获取运动数据的过程中，传感器容易受到外界噪声的干扰，而通过滤波处理可以有 效地改善这一问题。另外，由于运动数据会随人体的各 种运动行为而持续产生，采集到的运动数据长度往往会 很长。而为了识别某个时刻或一段时间内的运动行为，通常会根据特定的数据分割规则来将运动数据划分为 若干长度有限的数据片段，之后再进行识别。

数据分割在传感器采集到大量运动数据后，往往 只有部分运动数据是感兴趣或需要识别的。而通过数据分割可以将有效的运动数据分离出来，排除无关的数 据，这有助于降低运动行为识别过程的运算量。同时， 将运动数据按照采集的时间顺序进行分割，可在一定程 度上保留数据的时间信息。

##### 分割数据

一种较容易实现的数据分
割方法是，采用固定长度数据窗口，并按照一定重叠率 在运动数据序列上滑动来对数据进行分割。对于加 速度数据，采样频率为50 Hz，窗口宽度为10 s时，运动 行为识别的效果要好于其他数据分割方式。在实际研 究中也可按照研究需求通过手工操作的方式对数据进 行分割。而一种较为合理的方法是采用长度可变的窗口进行数据分割，首先估算出识别不同运动行为所需 的最小数据量，再以此作为数据分割的窗口长度。另 外，也可以根据运动行为所表现出的小波能量、加速度幅值来设定阈值，由此确定运动行为的开始和结束，进 而分割出有效的运动数据。

##### 运动行为特征识别方法

运动行为的识别通常不会直接使用所采集到的运
动数据，而是对数据进行特征提取，构建出特征向量后 再进行识别。这样可以降低识别模型的复杂度，同时也 有助于提高识别的准确率。特征提取方法主要包括时 域特征提取、频域特征提取两大类；

##### 时域特征多是运动数据片段的统计特征，其具有提取容易，运算量小，算法

复杂度低等优点，有利于降低运动行为识别过程的延 迟。频域特征则是通过计算运动数据的频谱得到，其特 征提取效果较好，但计算量相比时域特征大很多。此 外，由于运动数据的特征空间往往很大，常会通过特征选择从众多特征中找出关键特征，并通过特征降维来降 低特征向量的维度。这对减小运算量、提高识别精度都有帮助。

时域特征提取常用的时域特征包括均值标准
差、均方根、极值、平均绝对值、过零点、斜率符号变化等

频域及其他特征提取频域特征也常用于进行特征 提取，其可通过计算运动数据的频谱得到，而它的特征提取效果一般会优于时域特征提取。常见的频域特征 有平均频率、中值频率、峰值频谱功率、频谱功率均值等；

特征选择和降维在提取得到运动行为的各种特征 后，由于某些特征可能并不适合表征特定的运动行为，
同时如果特征数量过多将会导致运动行为的识别过程 变得复杂。因此，需要进行特征选择和降维来减少特征 数量，以实现使用尽量少的特征完成对运动行为的识 别。特征选择是从已有的众多特征中选择部分来构成运动行为识别所需的特征向量；采用了粒子群优化和蚁群优化两种方法，而特征降维是将特征向量从一个高维度映射到低维 度。HSU等采用结合了非参数加权特征提取(NWFE)和 主成份分析(PCA)的特征降维方法，将252个归一化特征降维到18个。

##### 难点

基于传感器的人体运动行为识别的研究已经有了 长足发展，也能够感受得到相关技术已经开始慢慢融入 我们的生活。但目前所面临的问题也不容小觑，其中较 为突出的有以下几点：

(1)  运动行为识别模型的通用性较差。现有研究多 是基于单个或少量实验对象进行的，因此所建立的识别 模型在实验对象身上表现良好，但将其应用到全新对象 时往往无法得到理想的结果。

(2)  数据分割窗口的不合理性。在运动数据的预处 理阶段常会采用一种数据分割窗口来分割数据，这样可 能使完整的运动信息被截断或者截取到完全不需要的 数据，这可能会增加识别模型的复杂度。

(3) 缺乏大量数据源。在目前的研究中，样本数据 多是来自研究人员自行采集的，数据的数量和质量都参 差不齐。另外一方面，现有运动行为识别模型的训练多 需要手工标记训练数据的标签，无法快速获得大量的训 练数据。

而随着传感器技术的发展以及机器学习技术的大 规模应用，可以看到以下几个方面将成为发展趋势：

(1)  硬件系统优化。现有的运动行为识别系统受限 于体积、功耗以及处理性能等，只能执行相对简单、固定 的任务。突破这些限制，可以使运动行为识别系统高度 集成化，并进行更为密集的计算，甚至做到单片集成传 感器、高性能处理器和网络连接器件。

(2)  模型优化。包括对模型结构的优化，以减小模 型占用空间。灵活的网络参数，可以在本地进行重新 训练并及时修改网络参数，以保持模型在任一时刻的 有效性。

(3)  个性化识别。关注用户产生的特定运动数据， 基于识别系统的硬件优化和模型优化，可以使识别系统 能够自动适配不同的用户个体。
@@ -0,0 +1,19 @@
# 基于Kinect与九轴传感器的篮球训练系统的应用研究

##### 系统总体设计

基于Kinect与九轴传感器的智能篮球训练系统，是由数据采集层、数据交互层以及信息处理层构成的。其中，数据采集层是以由Linect深度相机与九轴惯性传感器JY-901模块为核心单元进行数据存储和数据处理；数据交互以蓝牙4.0模块为核心进行数据通信与软硬件交互；信息处理层以IOS为开发平台进行算法编写、数据分析和功能实现；

##### 关键技术

利用kinect进行数据采集技术研究

对用户的动作进行捕捉，并得到关节在空间中的坐标对于本项目 至关重要，系统通过kinect的彩色图像相机获取实时图像，之后利用 opencv将彩色图像转换为hsv图像，转换完成之后将其二值化，并且 提取标志物的图像轮廓。最后通过图像轮廓确定图像中心点的位置来 确定它在深度相机中的位置，从而获得标志点的的空间坐标完成用户 运动数据的采集。

九轴惯性传感单元的动作捕捉技术研究

九轴惯性单元是由三轴加速度计、三轴陀螺仪和三轴磁强计组成
的。据三种惯性测量单元的不同特性，将其加以组合，优势互补，实 现对载体位置姿态的准确测量。由于三轴加速度计静态特性好，不存 在时间累积误差，因此可以利用三轴加速度计计算得到的姿态角来修
正陀螺仪计算的翻滚角和俯仰角，而根据磁强计动态反应慢，不存在 时间累积误差的特性，可以使用磁强计来修正陀螺仪计算的偏航角。 由此，综合各个惯性测量单元的优点，实现运动场景下对载体姿态的
精确测量。
@@ -0,0 +1,35 @@
# 基于MEMS六轴传感器的上肢运动识别系统

本文使用德州仪器（Texas Instruments, TTI) 公司的CC2650 SensorTag作为数据采集终端. 该设备使用CC2650无线MCU作为处理器，具 有10个低功耗MEMS传感器，包括加速度计、陀 螺仪、磁力计、磁传感器、数字麦克风、光、湿度、压 力、物体温度以及环境温度传感器.该设备体积仅 为 5. 0cmX6. 7cmX1. 4 cm,使用 CR2032 电池 供电，非常适合本文所研究的低功耗、小体积、低 成本的嵌入式应用

采集端主要由CC2650无线MCU、MPU- 9250九轴运动传感器及CR2032纽扣电池等组成

理论上说，加速度计通过测量施加于传感器上 的力来测量设备的加速度，根据牛顿第二定律，有

Ad =— ^Fs/m

其中Ad为设备的加速度，Fs为施加于传感器的 力，m为传感器的质量.

然而，重力总是会按照下式的关系影响加速

Ad=— g— ^F/m

其中g为重力加速度，F为传感器受到的除重力 以外的力.

因此，为了测量人体运动所产生的加速度，必 须将重力加速度从加速度计的数据中分离.即将 传感器测量值分解为重力加速度和线性加速度， 其中，线性加速度表示设备运动产生的加速度.使 用一阶低通滤波器可实现上述目的.根据一阶低 通滤波算法公式

y(n)^aXx(n)-(1~a)X^(n—1)

需要指出的是，由于人体运动过程中的微弱
抖动和传感器的噪声，加速度和角速度数据都具 有一定的抖动，这并不利于动作分析，因此在对数 据进行处理之前，应首先进行消抖.本文通过FIR
滤波器对采集到的数据进行消抖

##### 运动周期判别

对于具有周期性的运动，由于每个周期的运 动特征基本一致，故对每一个单独周期的运动数 据进行分析.本文规定，Ax、Ay、Az的平均值由负 值变为正值的点为周期起始点，一个周期起始点 至下一个周期起始点之间为_个运动周期.

##### 标准化

   对于同一动作，不同人的动作幅度和快慢均有差异，这会导致特征曲线的振幅和周期出现差 异.为了将采集到的运动曲线与数据库中的特征 曲线进行相关性分析，需将数据进行标准化处理. 标准化分为纵向标准化和横向标准化；

纵向标准化纵向标准化是指对加速度和角速度振幅的标准化.针对同一动作，线性加速 度和角速度的振幅差异反映出动作的速度和幅度 差异，重力加速度的振幅差异仅反映出传感器所 处的纬度差异.
@@ -0,0 +1,31 @@
# 基于九轴传感器的可穿戴式微功耗实时震颤监测系统

手部震颤是帕金森病的一项基本临床症状，对震颤的长时定量监测可为帕金森的临床诊断和治疗提供客 观依据，据此设计了基于九轴传感器的可穿戴式微功耗实时震颤监测系统，实现了对帕金森患者手部震颤特征的 长时间低负荷实时检测和无线传输记录.九轴传感器用于获取加速度、角速度和磁场强度多个参量，利用融合算法 分析上述参量可得到病人手部姿态数据，数据经微尺寸采集发射节点无线传输至上位机实时显示并保存

临床上常通过量表来对运动功能进行评估，以诊断病人患病程度然而，这种方式易受检测者主观因素影响，评估结果无法做到准确 客观，另外其灵敏度不高，无法测得微小变化， 不利于疾病早期诊断和评估治疗效果.通过对 震颤过程的长时定量监测，可避免结果受患者情绪干扰，弥补量表检查的固有缺陷，为患者的病情评估提供可靠数据，也为进一步研究优化治疗方案以及探寻PD病因提供量化信息；

本文在国内提出一种基于九轴传感器的手部震颤实时监测系统，相比现有的产品，本系统 尺寸小并具有更高的测量精度；同时长达18h 的连续工作时间和无线实时传输方式，可实现本系统的可穿戴化；

##### 系统总体设计

###### 设计要求

·监测设备不影响病人的震颤状态

·能实现长时间实时监测而非先存储后传输的非实时方式

·使用方便且尽可能获取多运动参量

·为处理和评估提供多样化信息.为此，监测设备本身应具有体积小、 重量轻的特点，并使用低容量小体积电池

###### 为满足低负荷、低功耗的需求，采用基于

Cortex M0内核的低功耗主控芯片nRF51822,
其自带无线传输功能，是一款为可穿戴设备量 身定做的小体积高集成度主控器.参数采集测
量采用世界上首款九轴数据传感器 MPU9150,尺寸为 4 mmX4 mmX1 mm,该传 感器额外增加了磁场强度信息用于消除六轴数 据传感器长期监测累积误差大的缺点

系统测试：

指标测试测试指标包括：传输距离、采
集发送节点工作电流、姿态融合算法的瞬态响 应时间和稳态精度.
@@ -0,0 +1,30 @@
# 基于九轴惯性传感器的运动姿态系统设计

文章首先介绍了运动指标采集系统的整体技术框架，阐明数据传输方面的技术方案按照室内与户外分为两种，室 外则是先将数据存入SD卡，事后拷入计算机的方式;室内采用wifi模块+路由器方式。接下来，论述了硬件平台的设计; 然后论述硬件程序设计，包括:主程序、数据存储程序和无线通信程序。最后，描述了计算机软件数据采集功能的设计与

实现。

##### 概述：

近年来，随着电子硬件体积不断的缩小和芯片运算速度 的提升'越来越多的国内外研究者己开始进行人体的运动姿 态研究。

九轴惯性传感器由三轴加速度、三轴陀螺仪和三轴磁力 计组成，最早应用于军事航天领域气随着微机械电子技术 的发展，惯性传感器的体积越来越小、成本越来越低、芯片处 理速度越来越快，其开始应用于运动姿态识别领域。

本文旨在设计一款基于九轴惯性传感器的运动姿态识别 系统，为在室内和户外都能采集到人体运动姿态数据提供新 的设计思路。

##### 户外数据采集模式

户外数据采集采用先将数据存入SD卡，事后拷入计算机 的方式。在人体各关节处都配有惯性传感器，用以感知这些 节点的运动信息。这些信息将会被单片机获取，并进行姿态 解算，最后定时向外发送，通信方式为wifi无线数据传输。

SD卡数据存储器通过相同的Wifi无线模块接受各惯性 节点的运动数据信息，并存入SD卡。计算机软件若要获取各 惯性节点的运动信息，需要使用读卡器读取SD卡中的数据。

为使系统的后续研究领域更为广阔，系统设计具备室内 数据采集模式。该模式下，惯性传感器部分不变，采用wifi无 线模块+路由器的方式。

计算机通过路由器接收各惯性节点发送而来的运动信息， 并以串口形式将接收到的信号向计算机传输。计算机用户终 端软件接收到各节点运动信息后，立即进行数据采集与解析。

##### 电路系统设计

九轴惯性传感器包括MPU-6050 芯片的3轴加速度计和3轴陀螺仪，以及HMC-5883的3轴 磁力计。加速度计用来测量加速度信息，陀螺仪用来测量角 速度速度，磁力计用来测量磁场大小。通过3个传感器的测 量数据，分析即可得到整个系统的姿态信息。

核心处理器采用STM32F103C8T8处理器，STM32系列 处理器具有高性能、低成本、低功耗等优势，目前被普遍运用 于嵌入式开发邻域。处理器通过UART串口通信技术采集传 感器测量的信息，信息采集后处理器还需进行传感数据的滤 波、姿态解算、数据融合等算法处理。
@@ -0,0 +1,45 @@
# 基于多特征组合的动态手势识别

为提高动态手势的识别效果，提出一种基于多特征组合的动态手势分类方法。对表面肌电（surface electromyography， SEMG) 和加速度计
（accelerometer， ACC) 传感器进行特征水平上的融合，分别对两类传感器提取多种类型特征并
组合，通过实验对比分析选出最优特征组合。为对短时间肌肉收缩有较好连续性，采用样本熵对表面肌电检测活动段起始 点，以隐马尔可夫模型（hidden Markov model，HMM)对手势动作进行识别。

动态手势识别中特征参数的选取对识别系统的性能和 计算复杂度有较大的影响，目前对SEMG和对ACC信号提 取的特征过于单一，虽然计算量小速度相对较快，但算法本身不是很完善，会限制其在实际中的应用。采用基于信息增益的特征选择算法选取最佳特征子集，虽然识别效果较好但是此方法需要综合考虑所选的算法是否适合所选的分类器，存在着不确定性。

//

为了提高系统性能以及识别效果，本文对SEMG和 ACC传感器进行特征水平上的融合，提出一种基于多特征 组合的动态手势动作分类方法，探究不同特征组合对手势 识别效果的影响。

//

##### 活动段分割

活动段分割的目的是从SEMG及ACC信号中分割出有 效手势活动段，从连续信号中自动确定活动段的起始点。 如何从连续手势信号中分割出有效手势目前还没有比较完 善的方法，SEMG信号能代表肌肉活动水平，当手势运动 从一个动作到另一个动作时，相应肌肉会出现短暂放松， 因此采用SEMG信号的幅值变化信息可以用于两类传感器 的数据分割，ACC信号流同步于SEMG信号。此外相 对于ACC的活动段提取方法，SEMG传感器检测手势是否 处于活动段的方法更为成熟。实验研究发现，相比于振幅 包络，移动平均法等分割方法，样本熵对手势分割具有更 好的效果，对运动插入噪声的抑制效果较好。

##### 特征提取

当有效手势被完整分割后，要用有效的特征向量对动 作进行描述。SEMG信号能够反映手的形态以及手腕屈伸 等信息，对运动尺度较小的手势区分能力好；ACC信号能 够反映手臂的动作轨迹以及位置等信息，能够较好地区分 出运动尺度较大的动作。由于肌电和加速度计数据表示不同的物理意义，特征提取之后也常常具有不可比性，因此 要对肌电和加速度计数据进行归一化处理。

##### 特征级融合

特征级融合按特征向量的产生方式分为特征选择和特 征组合两种方法。本文采用特征组合方法，将手形和轨迹 特征组合在一起构造串行联合特征矢量。特征级融合能够 减少_个分类器的使用，节省时间。

特征组合后用分类器进行识别，利用MATLAB软件进行仿真实验，得到识别率以及运行所用的时间。对比所 有的识别率以及运行时间，选出最优的特征组合，使得用
时较短识别率高

##### 分类识别

为了获得较高识别率，采用了 HMM的分类算法。 HMM模型是_种双重随机过程：_个是马尔可夫链，描 述了隐藏状态的转移；另一个是可观察的观察值序列，描 述了隐藏状态与观察状态之间的统计对应关系

HMM模型训练

HMM模型训练是对参数A = U，A，B}进行估计的过 程，常采用Baum-Welch算法，通过不断迭代去调整参数 A，让参数A不断趋于收敛，使得输出P(0|A)概率达到最大化。

Baum-Welch算法是一种迭代算法，视观测序列（离散 或连续）的不同，算法会有不同的形式。本文是对连续手 势进行识别，选取连续的观测序列B，通常采用高斯混合。

##### 信号采集实验

本研究利用惯用手（右手）进行手势运动，采用4通道 的SEMG和1个三轴ACC传感器进行数据采集。安放位置 如图2所示，三轴ACC传感器安放于前臂靠近腕部的背，用于捕捉手部的运动轨迹信息，4通道的SEMG传感 器分别安放于前臂指伸肌、伸指总肌、桡侧腕长伸肌和尺 侧腕屈肌，用于检测手的形态运动信息。本实验肌电数据 是由加拿大Thought Technology公司研制的型号是SA7500 表面肌电仪采集，采样率最大是2048 Hz，最小是256 Hz， AD分辨率是14bit，采用的是差分电极；三轴加速度计数 据是由荷兰Xsens公司生产的MEMS惯性传感器采集，采 样率是256 HZ。实验选取两类传感器采样率都为256 HZ。


 
