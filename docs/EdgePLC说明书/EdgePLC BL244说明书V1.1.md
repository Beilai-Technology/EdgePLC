<figure>
<img
src="EdgePLC BL244说明书V1.1-images/image2.jpeg"
style="width:2.97639in;height:3.98056in" alt="EdgePLC A款 (2)" />
<figcaption><p>版本：V1.1<br />
日期：2026-09-10<br />
版权：<strong>深圳市钡铼技术有限公司<br />
</strong>网址：<a
href="http://www.bliiot.cn">www.bliiot.cn</a></p></figcaption>
</figure>

EdgePLC BL244系列

<figure>
<img
src="EdgePLC BL244说明书V1.1-images/image1.png"
style="width:2.68681in;height:1.89653in" />
<figcaption><p>说明书</p></figcaption>
</figure>

EdgePLC BL244工业AI边缘控制器

**前言**

感谢您使用深圳市钡铼技术有限公司的BL244系列，阅读本产品说明书能让您快速掌握本产品的功能和使用方法。

> **版权声明**

本说明书之所有权由深圳市钡铼技术有限公司所有。未经本公司之书面许可，任何单位和个人无权以任何形式复制、传播和转载本手册之任何部分，否则一切后果由违者自负。

> **免责声明**

由于运营商升级网络造成设备无法继续使用的，本公司不能提供免费的升级服务。由于特殊原因造成运营商网络服务中断时，本机将无法正常工作，本公司不承担由此带来的后果。

本产品主要用于基于GPRS/网络的数据传输应用，请按照说明书提供的参数和技术规格使用，同时请注意无线电产品特别是GPRS产品使用时应该关注的注意事项，本公司不承担由于不正常使用或不恰当使用本产品造成的财产或人身伤害。

本产品包含开源软件或第三方组件。因开源软件的缺陷、漏洞、兼容性问题、停止维护或协议变更等原因导致的系统故障、数据丢失或安全问题，本公司概不负责。用户需自行承担使用开源组件的相关风险。

**修订记录**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 16%" />
<col style="width: 17%" />
<col style="width: 27%" />
<col style="width: 12%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>更新日期</strong></td>
<td style="text-align: center;"><strong>文档版本</strong></td>
<td style="text-align: center;"><strong>说明</strong></td>
<td style="text-align: center;"><strong>修订内容</strong></td>
<td style="text-align: center;"><strong>作者</strong></td>
</tr>
<tr>
<td style="text-align: center;">2026.4.24</td>
<td style="text-align: center;">Ver.1.0</td>
<td style="text-align: center;">首次发布</td>
<td style="text-align: center;"></td>
<td style="text-align: center;">ZJX</td>
</tr>
<tr>
<td style="text-align: center;">2026.7.31</td>
<td style="text-align: center;">Ver.1.1</td>
<td style="text-align: center;">部分更新</td>
<td style="text-align: center;"><ol type="1">
<li><p>完善RTD、NTC N板使用说明，增加量程模式修改，优化软件支持</p></li>
<li><p>增加X91的CAN使用</p></li>
</ol></td>
<td style="text-align: center;">ZJX</td>
</tr>
</tbody>
</table>

# 1.产品简介

## 1.1 概述

在工业自动化向“AI边缘计算+实时控制”深度融合的转型背景下，传统PLC面临智能计算的瓶颈，而通用工业计算机又难以满足高实时性控制的需求。EdgePLC
BL244系列工业AI边缘控制器应运而生，旨在打破IT与OT的融合壁垒，提供真正意义上的“边缘AI控算一体”解决方案。

BL244系列采用“高性能ARM处理器 +
分布式I/O扩展”的架构，以瑞芯微RK3576J/RK3576为核心，集成6TOPS算力的专用NPU，支持四核Cortex-A72 +
四核Cortex-A53 +
三核Cortex-M0的异构计算，在保障毫秒级实时控制的同时，具备强大的本地AI推理与数据处理能力。

EdgePLC
BL244工业AI边缘控制器深度融合实时控制、AI边缘智能、协议转换、远程运维与二次开发等功能，支持IEC
61131-3标准编程环境（OpenPLC/NexPLC/CODESYS）、IGH
EtherCAT硬实时主站，并可扩展多达32块N系列分布式I/O模块，覆盖DI/DO/AI/AO/温度采集等多种信号类型。软件层面基于Ubuntu
20.04系统，集成Docker、Node-RED、Python/C++开发环境，以及YOLOv5/8+OpenCV等AI视觉工具栈，实现从数据采集、实时分析到智能决策的全流程闭环。

BL244系列工业AI边缘控制器专为智能产线控制、储能EMS、光伏逆变器管理、AGV机器人、机器视觉等“控制+计算”协同场景设计，通过将智能分析下沉至设备边缘，它不仅实现了控制逻辑的精准执行，更完成了数据价值的就地转化与智能决策，助力企业构建更敏捷、更智能、更高效的下一代工业控制系统，从容应对智能制造的未来挑战。

## 1.2 外形尺寸

产品外观结构与尺寸如下图：

<img
src="EdgePLC BL244说明书V1.1-images/image4.png"
style="width:2.29236in;height:2.85556in"
alt="F:/2025_9/EdgePLC/标签外壳/标准款清晰图片.png标准款清晰图片" /><img
src="EdgePLC BL244说明书V1.1-images/image5.png"
style="width:2.30972in;height:2.87986in"
alt="F:/2025_9/EdgePLC/标签外壳/A款清晰图片.pngA款清晰图片" />

## 1.3 技术参数

<table>
<colgroup>
<col style="width: 17%" />
<col style="width: 19%" />
<col style="width: 63%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>分类</strong></td>
<td style="text-align: center;"><strong>参数</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td rowspan="10" style="text-align: center;">系统</td>
<td style="text-align: center;">处理器型号</td>
<td>瑞芯微 RK3576J/RK3576，64bit，8nm</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">处理器频率</td>
<td><p>4x ARM Cortex-A72</p>
<p>RK3576J 主频：normal mode 1.6GHz，overdrive mode 2.1GHz</p>
<p>RK3576 主频：2.2GHz</p>
<p>备注：为保障处理器使用寿命，满足更多工业应用场景要求，我司已将RK3576J/RK3576
处理器 Cortex-A72 核心最高主频默认配置为 1.6GHz。</p></td>
</tr>
<tr>
<td><p>4x ARM Cortex-A53</p>
<p>RK3576J 主频：normal mode 1.4 GHz，overdrive mode 1.9 GHz</p>
<p>RK3576 主频：2.0GHz</p>
<p>备注：为保障处理器使用寿命，满足更多工业应用场景要求，我司已将RK3576J/RK3576
处理器 Cortex-A53 核心最高主频默认配置为 1.4GHz。</p></td>
</tr>
<tr>
<td>1x ARM Cortex-M0主频：400MHz</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">GPU</td>
<td>GPU：Mali-G52 MC3，支持 OpenGL ES 1.1/2.0/3.2、OpenCL 2.0、Vulkan
1.1</td>
</tr>
<tr>
<td>ISP:16M，支持HDR、3A、CAC、3DNR、2DNR等</td>
</tr>
<tr>
<td><p>Decoder：支持8K@30fps/4K@120fps H.265、4K@60fps H.264</p>
<p>Encoder：支持4K@60fps H.265/H.264</p></td>
</tr>
<tr>
<td style="text-align: center;">NPU</td>
<td><p>6TOPS</p>
<p>支持INT4/INT8/INT16/BF16/TF32</p>
<p>支持TensorFlow/PyTorch/Caffe/MXNet深度学习框架</p></td>
</tr>
<tr>
<td style="text-align: center;">内存</td>
<td>2/4/8GByte LPDDR4X</td>
</tr>
<tr>
<td style="text-align: center;">存储</td>
<td>16/32/64GByte eMMC</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">电源</td>
<td style="text-align: center;">输入电压</td>
<td>DC 12～24V（输入：24V,输出：12V）</td>
</tr>
<tr>
<td style="text-align: center;">功耗</td>
<td><p>正常：312mA@12V（带4G模块），252mA@12V（不带4G模块）</p>
<p>最大：700mA@12V</p></td>
</tr>
<tr>
<td style="text-align: center;">反接防护</td>
<td>支持</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">网口</td>
<td style="text-align: center;">网口规格</td>
<td>RJ-45 接口，2~3个，2个10/100/1000M、1个10/100M 自适应网口</td>
</tr>
<tr>
<td style="text-align: center;">网口保护</td>
<td>ESD ±6kV（接触），±8kV（空气）；</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">SIM卡</td>
<td style="text-align: center;">数量</td>
<td>1</td>
</tr>
<tr>
<td style="text-align: center;">规格</td>
<td>抽屉式接口</td>
</tr>
<tr>
<td rowspan="5" style="text-align: center;">串口（选配）</td>
<td style="text-align: center;">串口数量</td>
<td>2*RS485</td>
</tr>
<tr>
<td style="text-align: center;">串口波特率</td>
<td>300bps-115200bps</td>
</tr>
<tr>
<td style="text-align: center;">数据位</td>
<td>7,8</td>
</tr>
<tr>
<td style="text-align: center;">校验位</td>
<td>None, Even, Odd</td>
</tr>
<tr>
<td style="text-align: center;">停止位</td>
<td>1, 1.5,2</td>
</tr>
<tr>
<td rowspan="5" style="text-align: center;">N板数字输入（选配）</td>
<td style="text-align: center;">数量</td>
<td>16/32通道</td>
</tr>
<tr>
<td style="text-align: center;">输入类型</td>
<td>支持干接点或湿接点</td>
</tr>
<tr>
<td style="text-align: center;">干接点</td>
<td><p>闭合：短接</p>
<p>断开：端开路</p></td>
</tr>
<tr>
<td style="text-align: center;">湿接点</td>
<td><p>逻辑0：0-15VDC</p>
<p>逻辑1：16-24VDC</p></td>
</tr>
<tr>
<td style="text-align: center;">隔离保护</td>
<td>2KVrms</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">N板数字输出（选配）</td>
<td style="text-align: center;">数量</td>
<td>16/32通道</td>
</tr>
<tr>
<td style="text-align: center;">输出类型</td>
<td>SINK</td>
</tr>
<tr>
<td style="text-align: center;">输出容量</td>
<td>单路100mA</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">USB接口</td>
<td style="text-align: center;">数量</td>
<td>1*micro USB，2*USB 3.2 HOST</td>
</tr>
<tr>
<td style="text-align: center;">传输速度</td>
<td style="text-align: left;">最大104 MB/s</td>
</tr>
<tr>
<td style="text-align: center;">输出功率</td>
<td>100mA@5V</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">SD卡座</td>
<td style="text-align: center;">数量</td>
<td>1</td>
</tr>
<tr>
<td style="text-align: center;">规格</td>
<td>支持SD、SDHC和SDXC（UHS-I）卡</td>
</tr>
<tr>
<td style="text-align: center;">HDMI接口</td>
<td style="text-align: center;">数量</td>
<td>1</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">天线</td>
<td style="text-align: center;">天线接口数量</td>
<td>1*Wi-Fi/移动网天线，1*GPS天线</td>
</tr>
<tr>
<td style="text-align: center;">天线接口类型</td>
<td>SMA孔式</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">SSD接口</td>
<td style="text-align: center;">接口数量</td>
<td>1</td>
</tr>
<tr>
<td style="text-align: center;">接口类型</td>
<td>B&amp;M key</td>
</tr>
<tr>
<td style="text-align: center;">支持协议</td>
<td>NVME协议</td>
</tr>
<tr>
<td rowspan="6" style="text-align: center;">4G模块(选配功能)</td>
<td style="text-align: center;">L-E版本</td>
<td><p>GSM/EDGE:900,1800MHz</p>
<p>WCDMA:B1,B5,B8</p>
<p>FDD-LTE:B1,B3,B5,B7,B8,B20</p>
<p>TDD-LTE:B38,B40,B41</p></td>
</tr>
<tr>
<td style="text-align: center;">L-CE版本</td>
<td><p>GSM/EDGE:900,1800MHz</p>
<p>WCDMA:B1,B8</p>
<p>TD-SCDMA:B34,B39</p>
<p>FDD-LTE:B1,B3,B8</p>
<p>TDD-LTE:B38,B39,B40,B41</p></td>
</tr>
<tr>
<td style="text-align: center;">L-A版本</td>
<td><p>WCDMA:B2,B4,B5</p>
<p>FDD-LTE:B2,B4,B12</p></td>
</tr>
<tr>
<td style="text-align: center;">L-AU版本</td>
<td><p>GSM/EDGE:850,900,1800MHz</p>
<p>WCDMA:B1,B2,B5,B8</p>
<p>FDD-LTE:B1,B3,B4,B5,B7,B8,B28</p>
<p>TDD-LTE:B40</p></td>
</tr>
<tr>
<td style="text-align: center;">L-AF版本</td>
<td><p>WCDMA:B2,B4,B5</p>
<p>FDD-LTE:B2,B4,B5,B12,B13,B14,B66,B71</p></td>
</tr>
<tr>
<td style="text-align: center;">CAT-1版本</td>
<td><p>GSM:900,1800</p>
<p>FDD-LTE:B1,B3,B5,B8</p>
<p>TDD-LTE:B34,B38,B39,B40,B41</p></td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">5G模块(选配功能)</td>
<td style="text-align: center;">redcap版本</td>
<td><p>5G NR：N1/N3/N5/N8/N28/N41/N78/N79</p>
<p>LTE-FDD：B1/B3/B5/B8</p>
<p>LTE-TD：B34/B38/B39/B40/B41</p></td>
</tr>
<tr>
<td style="text-align: center;">N-CN版本</td>
<td><p>NR：N1/28/41/78/79</p>
<p>LTE：FDD B1/3/5/8</p>
<p>LTE：TDD B34/38/39/40/41</p>
<p>WCDMA：B1/8</p></td>
</tr>
<tr>
<td rowspan="10" style="text-align: center;">Wi-Fi(选配功能)</td>
<td style="text-align: center;">接口</td>
<td>PCIE</td>
</tr>
<tr>
<td style="text-align: center;">协议</td>
<td>IEEE 802.11b/g/n</td>
</tr>
<tr>
<td style="text-align: center;">模式</td>
<td>STA，AP</td>
</tr>
<tr>
<td style="text-align: center;">频段</td>
<td>2.4GHz</td>
</tr>
<tr>
<td style="text-align: center;">通道数</td>
<td>Ch1 ~ Ch13</td>
</tr>
<tr>
<td style="text-align: center;">安全性</td>
<td>Open、WPA、WPA2</td>
</tr>
<tr>
<td style="text-align: center;">加密</td>
<td>AES、TKIP、TKIPAES</td>
</tr>
<tr>
<td style="text-align: center;">连接数</td>
<td>8（Max）</td>
</tr>
<tr>
<td style="text-align: center;">速率</td>
<td>150Mbps（Max）</td>
</tr>
<tr>
<td style="text-align: center;">SSID广播开关</td>
<td>支持</td>
</tr>
<tr>
<td style="text-align: center;">指示灯</td>
<td style="text-align: center;">数量</td>
<td>LED*3（含两个可编程LED）</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">环境</td>
<td style="text-align: center;">工作温度、湿度</td>
<td>-40～85℃/0~70℃，5～95% RH</td>
</tr>
<tr>
<td style="text-align: center;">存储温度、湿度</td>
<td>-40～85℃，5～95% RH</td>
</tr>
<tr>
<td rowspan="5" style="text-align: center;">其他</td>
<td style="text-align: center;">外壳</td>
<td>铝合金外壳+不锈钢</td>
</tr>
<tr>
<td style="text-align: center;">尺寸</td>
<td>110*92*38mm</td>
</tr>
<tr>
<td style="text-align: center;">防护等级</td>
<td>IP30</td>
</tr>
<tr>
<td style="text-align: center;">安装方式</td>
<td>DIN35导轨安装</td>
</tr>
<tr>
<td style="text-align: center;">系统</td>
<td><p>Buildroot-2024.02(Linux-6.1.115、Linux-RT-6.1.115)</p>
<p>Ubuntu 22.04</p></td>
</tr>
</tbody>
</table>

## 1.4 设备选型

### 1.4.1 主型号选型

|          |                           |         |          |             |             |
|:--------:|:-------------------------:|:-------:|:--------:|:-----------:|:-----------:|
| **型号** |          **ETH**          | **USB** | **HDMI** | **N板IO槽** |  **尺寸**   |
|  BL244   |      2x10/100/1000M       |    2    |    0     |      1      | 38x92x110mm |
|  BL244A  | 2x10/100/1000M，1x10/100M |    2    |    1     |      1      | 38x92x110mm |

**BL244系列选型**

### 1.4.2 SOM选型表

可以根据需求，选择合适的ROM、RAM以及温度等级。

**BL244系列SOM选型表**

|          |         |          |         |          |             |                |
|:---------|:--------|:---------|:--------|:---------|:------------|:---------------|
| **型号** | **MCU** | **主频** | **NPU** | **eMMC** | **LPDDR4X** | **温度级别**   |
| SOM440   | RK3576J | 2.1GHz   | 6TOPS   | 16GByte  | 2GByte      | 工业级 -40~85℃ |
| SOM441   | RK3576J | 2.1GHz   | 6TOPS   | 32GByte  | 4GByte      | 工业级 -40~85℃ |
| SOM442   | RK3576J | 2.1GHz   | 6TOPS   | 64GByte  | 8GByte      | 工业级 -40~85℃ |
| SOM443   | RK3576  | 2.2GHz   | 6TOPS   | 32GByte  | 2GByte      | 宽温级 0~80℃   |
| SOM444   | RK3576  | 2.2GHz   | 6TOPS   | 32GByte  | 4GByte      | 宽温级 0~80℃   |
| SOM445   | RK3576  | 2.2GHz   | 6TOPS   | 64GByte  | 8GByte      | 宽温级 0~80℃   |

### 1.4.3 X系列板选型

可以根据需求，选择合适的X系列IO板，X系列IO板的PIN数要与外壳适配。

注意：本设备默认端口为RS485，如需RS232请向销售说明。

<table>
<colgroup>
<col style="width: 6%" />
<col style="width: 14%" />
<col style="width: 7%" />
<col style="width: 6%" />
<col style="width: 6%" />
<col style="width: 7%" />
<col style="width: 17%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr>
<td colspan="7"
style="text-align: center;"><strong>X系列IO板选型表</strong></td>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"><strong>型号</strong></td>
<td style="text-align: center;"><strong>RS232/RS485</strong></td>
<td style="text-align: center;"><strong>CAN</strong></td>
<td style="text-align: center;"><strong>DI</strong></td>
<td style="text-align: center;"><strong>DO</strong></td>
<td style="text-align: center;"><strong>GPIO</strong></td>
<td style="text-align: center;"><strong>GND</strong></td>
<td style="text-align: center;"><strong>PIN数</strong></td>
<td style="text-align: center;"><strong>备注</strong></td>
</tr>
<tr>
<td style="text-align: center;">X90</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">6PIN</td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;">X91</td>
<td style="text-align: center;">1</td>
<td style="text-align: center;">1</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">×</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">6PIN</td>
<td style="text-align: center;"></td>
</tr>
</tbody>
</table>

### 1.4.4 N系列IO板选型

16路以下尺寸：15.4x104.6x74.9mm，32路尺寸：28.4x104.6x74.9mm

**N系列IO板选型表**

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 38%" />
<col style="width: 2%" />
<col style="width: 8%" />
<col style="width: 42%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>型号</strong></td>
<td style="text-align: center;"><strong>描述</strong></td>
<td rowspan="12" style="text-align: center;"></td>
<td style="text-align: center;"><strong>型号</strong></td>
<td style="text-align: center;"><strong>描述</strong></td>
</tr>
<tr>
<td style="text-align: center;">N1161</td>
<td style="text-align: center;">16路DI模块NPN</td>
<td style="text-align: center;">N3046</td>
<td style="text-align: center;">4路16位AI模块差分输入±5V/±10V</td>
</tr>
<tr>
<td style="text-align: center;">N1162</td>
<td style="text-align: center;">16路DI模块PNP</td>
<td style="text-align: center;">N3087</td>
<td style="text-align: center;">8路电阻测量模块</td>
</tr>
<tr>
<td style="text-align: center;">N1163</td>
<td style="text-align: center;">16路干节点DI模块</td>
<td style="text-align: center;">N4081</td>
<td style="text-align: center;">8路16位AO模块输出0/4~20mA</td>
</tr>
<tr>
<td style="text-align: center;">N1321</td>
<td style="text-align: center;">32路DI模块NPN</td>
<td style="text-align: center;">N4086</td>
<td style="text-align: center;">8路16位AO模块输出±5V/±10V</td>
</tr>
<tr>
<td style="text-align: center;">N1322</td>
<td style="text-align: center;">32路DI模块PNP</td>
<td style="text-align: center;">N5041</td>
<td style="text-align: center;">4路RTD模块三线PT100</td>
</tr>
<tr>
<td style="text-align: center;">N1323</td>
<td style="text-align: center;">32路干节点DI模块</td>
<td style="text-align: center;">N5042</td>
<td style="text-align: center;">4路RTD模块三线PT1000</td>
</tr>
<tr>
<td style="text-align: center;">N2161</td>
<td style="text-align: center;">16路DO模块PNP</td>
<td style="text-align: center;">N5043</td>
<td style="text-align: center;">4路RTD模块四线PT100</td>
</tr>
<tr>
<td style="text-align: center;">N2162</td>
<td style="text-align: center;">16路DO模块NPN</td>
<td style="text-align: center;">N5044</td>
<td style="text-align: center;">4路RTD模块四线PT1000</td>
</tr>
<tr>
<td style="text-align: center;">N2321</td>
<td style="text-align: center;">32路DO模块PNP</td>
<td style="text-align: center;">N5088</td>
<td style="text-align: center;">8路TC模块</td>
</tr>
<tr>
<td style="text-align: center;">N2322</td>
<td style="text-align: center;">32路DO模块NPN</td>
<td style="text-align: center;">N7011</td>
<td style="text-align: center;">中继电源模块</td>
</tr>
<tr>
<td style="text-align: center;">N2084</td>
<td style="text-align: center;">8路DO模块继电器</td>
<td style="text-align: center;">N9081</td>
<td style="text-align: center;">3路脉冲计数+5DI</td>
</tr>
<tr>
<td style="text-align: center;">N3081</td>
<td style="text-align: center;">8路16位AI模块单端输入0/4~20mA</td>
<td style="text-align: center;"></td>
<td style="text-align: center;">N9082</td>
<td style="text-align: center;">6路脉冲输出+2DO</td>
</tr>
<tr>
<td style="text-align: center;">N3083</td>
<td style="text-align: center;">8路16位AI模块单端输入0~5/10V</td>
<td style="text-align: center;"></td>
<td style="text-align: center;">N9083</td>
<td style="text-align: center;">2路脉冲输出（脉冲个数控制）+4DI+2DO</td>
</tr>
</tbody>
</table>

## 硬件说明

## 2.1 N板介绍

<img
src="EdgePLC BL244说明书V1.1-images/image6.png"
style="width:3.14375in;height:1.87847in" alt="EdgePLC A款 (10)" /><img
src="EdgePLC BL244说明书V1.1-images/image7.png"
style="width:2.56042in;height:2.56042in" />

工业自动化控制系统中常见的分布式I/O模块，例如：右侧具体为32通道数字量输入模块，型号为N1321(NPN)。这类模块通常用于连接现场的传感器、按钮、限位开关等设备，将物理信号转换为PLC（可编程逻辑控制器）可识别的数字信号。

型号“N1321(NPN)”指明了其电气特性：NPN型输入，适用于漏型（Sink）输入电路，常用于连接NPN型传感器。

模块顶部有一个橙色的卡扣，用于将模块固定在DIN导轨上，便于安装和拆卸。

**接线端子**

模块底部排列着多组橙色的弹簧式接线端子，用于连接外部设备的信号线。

这些端子按通道编号（1-32）排列，方便用户快速接线和维护。

弹簧式端子设计使得接线无需工具，操作便捷，且连接可靠。

**连接端子**

模块化I/O系统内部通信和供电的背板总线连接器，它通常由一排精密的金属插针和插座组成，负责在相邻模块之间传递电源、数据和控制信号。

**散热与结构设计**

模块外壳采用白色工程塑料，表面有散热格栅设计，有助于在高密度安装或高温环境下散热。

整体结构紧凑，符合工业标准尺寸，可与其他模块组合使用，形成分布式I/O系统。

**应用场景与优势**

分布式控制：该模块通常与主PLC控制器通过现场总线（如EtherCAT、PROFINET等）连接，实现远程I/O扩展，减少布线成本，提高系统灵活性。

高密度输入：32通道的设计使其适用于需要大量输入点的场合，如大型生产线、自动化仓储系统等。

NPN输入特性：适用于连接NPN型传感器，这类传感器在工业现场应用广泛，具有抗干扰能力强、成本较低等优点。

## 2.2 电源接口

<img
src="EdgePLC BL244说明书V1.1-images/image8.png"
style="width:2.57639in;height:1.04931in"
alt="e2c8802fdadeb1e5530381aefa943291_origin(1)" />。

设备提供1路输入。支持DC12~24V输入，支持反接防护

## 2.3 模块端口说明

根据不同的X/N板，有不同的串口可选择。目前可选板型如下。

### 2.3.1 RS232/485模块

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr>
<td colspan="7" style="text-align: center;">X90模块（2个RS485）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">1</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">3</td>
<td style="text-align: center;">4</td>
<td style="text-align: center;">5</td>
<td style="text-align: center;">6</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">ttyS1-A</td>
<td style="text-align: center;">ttyS1-B</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">ttyS8-A</td>
<td style="text-align: center;">ttyS8-B</td>
<td style="text-align: center;">GND</td>
</tr>
</tbody>
</table>

### 2.3.2 CAN模块

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr>
<td colspan="7"
style="text-align: center;">X91模块（1路RS485和1路CAN）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">1</td>
<td style="text-align: center;">2</td>
<td style="text-align: center;">3</td>
<td style="text-align: center;">4</td>
<td style="text-align: center;">5</td>
<td style="text-align: center;">6</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">CAN0-H</td>
<td style="text-align: center;">CAN0-L</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">ttyS8-A</td>
<td style="text-align: center;">ttyS8-B</td>
<td style="text-align: center;">GND</td>
</tr>
</tbody>
</table>

### 2.3.3 DI模块

注意：DI模块默认供电24V

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N1161/N1162/N1163模块</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI2</td>
<td style="text-align: center;">DI4</td>
<td style="text-align: center;">DI6</td>
<td style="text-align: center;">DI8</td>
<td style="text-align: center;">DI10</td>
<td style="text-align: center;">DI12</td>
<td style="text-align: center;">DI14</td>
<td style="text-align: center;">DI16</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI1</td>
<td style="text-align: center;">DI3</td>
<td style="text-align: center;">DI5</td>
<td style="text-align: center;">DI7</td>
<td style="text-align: center;">DI9</td>
<td style="text-align: center;">DI11</td>
<td style="text-align: center;">DI13</td>
<td style="text-align: center;">DI15</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N1321/N1322/N1323模块</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI17</td>
<td style="text-align: center;">DI19</td>
<td style="text-align: center;">DI21</td>
<td style="text-align: center;">DI23</td>
<td style="text-align: center;">DI25</td>
<td style="text-align: center;">DI27</td>
<td style="text-align: center;">DI29</td>
<td style="text-align: center;">DI31</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI16</td>
<td style="text-align: center;">DI18</td>
<td style="text-align: center;">DI20</td>
<td style="text-align: center;">DI22</td>
<td style="text-align: center;">DI24</td>
<td style="text-align: center;">DI26</td>
<td style="text-align: center;">DI28</td>
<td style="text-align: center;">DI30</td>
<td style="text-align: center;">COM</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI1</td>
<td style="text-align: center;">DI3</td>
<td style="text-align: center;">DI5</td>
<td style="text-align: center;">DI7</td>
<td style="text-align: center;">DI9</td>
<td style="text-align: center;">DI11</td>
<td style="text-align: center;">DI13</td>
<td style="text-align: center;">DI15</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DI0</td>
<td style="text-align: center;">DI2</td>
<td style="text-align: center;">DI4</td>
<td style="text-align: center;">DI6</td>
<td style="text-align: center;">DI8</td>
<td style="text-align: center;">DI10</td>
<td style="text-align: center;">DI12</td>
<td style="text-align: center;">DI14</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

注意：上述两个DI模块采用共板形式，分别对应NPN型、PNP型、干接点

### 2.3.4 DO模块

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N2161模块（PNP）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO2</td>
<td style="text-align: center;">DO4</td>
<td style="text-align: center;">DO6</td>
<td style="text-align: center;">DO8</td>
<td style="text-align: center;">DO10</td>
<td style="text-align: center;">DO12</td>
<td style="text-align: center;">DO14</td>
<td style="text-align: center;">DO16</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO1</td>
<td style="text-align: center;">DO3</td>
<td style="text-align: center;">DO5</td>
<td style="text-align: center;">DO7</td>
<td style="text-align: center;">DO9</td>
<td style="text-align: center;">DO11</td>
<td style="text-align: center;">DO13</td>
<td style="text-align: center;">DO15</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N2162模块（NPN）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO2</td>
<td style="text-align: center;">DO4</td>
<td style="text-align: center;">DO6</td>
<td style="text-align: center;">DO8</td>
<td style="text-align: center;">DO10</td>
<td style="text-align: center;">DO12</td>
<td style="text-align: center;">DO14</td>
<td style="text-align: center;">DO16</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO1</td>
<td style="text-align: center;">DO3</td>
<td style="text-align: center;">DO5</td>
<td style="text-align: center;">DO7</td>
<td style="text-align: center;">DO9</td>
<td style="text-align: center;">DO11</td>
<td style="text-align: center;">DO13</td>
<td style="text-align: center;">DO15</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 12%" />
<col style="width: 10%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N2321模块（PNP）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO17</td>
<td style="text-align: center;">DO19</td>
<td style="text-align: center;">DO21</td>
<td style="text-align: center;">DO23</td>
<td style="text-align: center;">DO25</td>
<td style="text-align: center;">DO27</td>
<td style="text-align: center;">DO29</td>
<td style="text-align: center;">DO31</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO16</td>
<td style="text-align: center;">DO18</td>
<td style="text-align: center;">DO20</td>
<td style="text-align: center;">DO22</td>
<td style="text-align: center;">DO24</td>
<td style="text-align: center;">DO26</td>
<td style="text-align: center;">DO28</td>
<td style="text-align: center;">DO30</td>
<td style="text-align: center;">COM</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO1</td>
<td style="text-align: center;">DO3</td>
<td style="text-align: center;">DO5</td>
<td style="text-align: center;">DO7</td>
<td style="text-align: center;">DO9</td>
<td style="text-align: center;">DO11</td>
<td style="text-align: center;">DO13</td>
<td style="text-align: center;">DO15</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO0</td>
<td style="text-align: center;">DO2</td>
<td style="text-align: center;">DO4</td>
<td style="text-align: center;">DO6</td>
<td style="text-align: center;">DO8</td>
<td style="text-align: center;">DO10</td>
<td style="text-align: center;">DO12</td>
<td style="text-align: center;">DO14</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 12%" />
<col style="width: 10%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N2322模块（NPN）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO17</td>
<td style="text-align: center;">DO19</td>
<td style="text-align: center;">DO21</td>
<td style="text-align: center;">DO23</td>
<td style="text-align: center;">DO25</td>
<td style="text-align: center;">DO27</td>
<td style="text-align: center;">DO29</td>
<td style="text-align: center;">DO31</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO16</td>
<td style="text-align: center;">DO18</td>
<td style="text-align: center;">DO20</td>
<td style="text-align: center;">DO22</td>
<td style="text-align: center;">DO24</td>
<td style="text-align: center;">DO26</td>
<td style="text-align: center;">DO28</td>
<td style="text-align: center;">DO30</td>
<td style="text-align: center;">COM</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO1</td>
<td style="text-align: center;">DO3</td>
<td style="text-align: center;">DO5</td>
<td style="text-align: center;">DO7</td>
<td style="text-align: center;">DO9</td>
<td style="text-align: center;">DO11</td>
<td style="text-align: center;">DO13</td>
<td style="text-align: center;">DO15</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">DO0</td>
<td style="text-align: center;">DO2</td>
<td style="text-align: center;">DO4</td>
<td style="text-align: center;">DO6</td>
<td style="text-align: center;">DO8</td>
<td style="text-align: center;">DO10</td>
<td style="text-align: center;">DO12</td>
<td style="text-align: center;">DO14</td>
<td style="text-align: center;">COM</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 16%" />
<col style="width: 10%" />
<col style="width: 0%" />
<col style="width: 7%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 0%" />
<col style="width: 9%" />
<col style="width: 0%" />
<col style="width: 9%" />
<col style="width: 0%" />
<col style="width: 9%" />
<col style="width: 9%" />
</colgroup>
<tbody>
<tr>
<td colspan="14" style="text-align: center;">N2084模块（继电器）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td colspan="2" style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td colspan="2" style="text-align: center;">B5</td>
<td colspan="2" style="text-align: center;">B6</td>
<td colspan="2" style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td colspan="2" style="text-align: center;">SW1</td>
<td style="text-align: center;">SW2</td>
<td style="text-align: center;">SW3</td>
<td style="text-align: center;">SW4</td>
<td style="text-align: center;">SW5</td>
<td colspan="2" style="text-align: center;">SW6</td>
<td colspan="2" style="text-align: center;">SW7</td>
<td colspan="2" style="text-align: center;">SW8</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td colspan="2" style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td colspan="2" style="text-align: center;">A5</td>
<td colspan="2" style="text-align: center;">A6</td>
<td colspan="2" style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">SW1</td>
<td colspan="2" style="text-align: center;">SW2</td>
<td style="text-align: center;">SW3</td>
<td style="text-align: center;">SW4</td>
<td colspan="2" style="text-align: center;">SW5</td>
<td colspan="2" style="text-align: center;">SW6</td>
<td colspan="2" style="text-align: center;">SW7</td>
<td style="text-align: center;">SW8</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

### 2.3.5 AO模块

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10"
style="text-align: center;">N4081模块（0/4~20mA）（±0.1误差）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">A1+</td>
<td style="text-align: center;">A2+</td>
<td style="text-align: center;">A3+</td>
<td style="text-align: center;">A4+</td>
<td style="text-align: center;">A5+</td>
<td style="text-align: center;">A6+</td>
<td style="text-align: center;">A7+</td>
<td style="text-align: center;">A8+</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">A1-</td>
<td style="text-align: center;">A2-</td>
<td style="text-align: center;">A3-</td>
<td style="text-align: center;">A4-</td>
<td style="text-align: center;">A5-</td>
<td style="text-align: center;">A6-</td>
<td style="text-align: center;">A7-</td>
<td style="text-align: center;">A8-</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10"
style="text-align: center;">N4086模块（±5V/±10V）（±0.1误差）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">AO1</td>
<td style="text-align: center;">AO2</td>
<td style="text-align: center;">AO3</td>
<td style="text-align: center;">AO4</td>
<td style="text-align: center;">AO5</td>
<td style="text-align: center;">AO6</td>
<td style="text-align: center;">AO7</td>
<td style="text-align: center;">AO8</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

注意：采用 24V DC 直流电源供电。

### 2.3.6 AI模块

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 8%" />
</colgroup>
<tbody>
<tr>
<td colspan="10"
style="text-align: center;">N3081/N3083模块（±0.1误差）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">AI1-</td>
<td style="text-align: center;">AI2-</td>
<td style="text-align: center;">AI3-</td>
<td style="text-align: center;">AI4-</td>
<td style="text-align: center;">AI5-</td>
<td style="text-align: center;">AI6-</td>
<td style="text-align: center;">AI7-</td>
<td style="text-align: center;">AI8-</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">AI1+</td>
<td style="text-align: center;">AI2+</td>
<td style="text-align: center;">AI3+</td>
<td style="text-align: center;">AI4+</td>
<td style="text-align: center;">AI5+</td>
<td style="text-align: center;">AI6+</td>
<td style="text-align: center;">AI7+</td>
<td style="text-align: center;">AI8+</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

注意：上述AI模块采用共板形式，分别对应单端0/4~20mA、单端输入0~5V/10V，采用
24V DC 直流电源供电。

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 14%" />
</colgroup>
<tbody>
<tr>
<td colspan="6" style="text-align: center;">N3046模块（±5V/±10V）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">AI1-</td>
<td style="text-align: center;">AI2-</td>
<td style="text-align: center;">AI3-</td>
<td style="text-align: center;">AI4-</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">AI1+</td>
<td style="text-align: center;">AI2+</td>
<td style="text-align: center;">AI3+</td>
<td style="text-align: center;">AI4+</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

### 2.3.7 RTD模块

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
</colgroup>
<tbody>
<tr>
<td colspan="10"
style="text-align: center;">N5041/N5042/N5043/N5044模块（±0.5误差）</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">RTD1+</td>
<td style="text-align: center;">1+</td>
<td style="text-align: center;">1-</td>
<td style="text-align: center;">RTD1-</td>
<td style="text-align: center;">RTD3+</td>
<td style="text-align: center;">3+</td>
<td style="text-align: center;">3-</td>
<td style="text-align: center;">RTD3-</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">RTD2+</td>
<td style="text-align: center;">2+</td>
<td style="text-align: center;">2-</td>
<td style="text-align: center;">RTD2-</td>
<td style="text-align: center;">RTD4+</td>
<td style="text-align: center;">4+</td>
<td style="text-align: center;">4-</td>
<td style="text-align: center;">RTD4-</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

注意：上述RTD模块采用共板形式，分别对应三线PT100电阻、三线PT1000电阻、四线PT100电阻、四线PT1000电阻。

### 2.3.8 TC模块

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 9%" />
<col style="width: 10%" />
<col style="width: 10%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N5088模块</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">T1+</td>
<td style="text-align: center;">T2+</td>
<td style="text-align: center;">T3+</td>
<td style="text-align: center;">T4+</td>
<td style="text-align: center;">T5+</td>
<td style="text-align: center;">T6+</td>
<td style="text-align: center;">T7+</td>
<td style="text-align: center;">T8+</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">T1-</td>
<td style="text-align: center;">T2-</td>
<td style="text-align: center;">T3-</td>
<td style="text-align: center;">T4-</td>
<td style="text-align: center;">T5-</td>
<td style="text-align: center;">T6-</td>
<td style="text-align: center;">T7-</td>
<td style="text-align: center;">T8-</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

### 2.3.9 NTC模块

<table style="width:100%;">
<colgroup>
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 10%" />
<col style="width: 6%" />
</colgroup>
<tbody>
<tr>
<td colspan="10" style="text-align: center;">N3087模块</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">B2</td>
<td style="text-align: center;">B3</td>
<td style="text-align: center;">B4</td>
<td style="text-align: center;">B5</td>
<td style="text-align: center;">B6</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">B9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">NTC1-</td>
<td style="text-align: center;">NTC2-</td>
<td style="text-align: center;">NTC3-</td>
<td style="text-align: center;">NTC4-</td>
<td style="text-align: center;">NTC5-</td>
<td style="text-align: center;">NTC6-</td>
<td style="text-align: center;">NTC7-</td>
<td style="text-align: center;">NTC8-</td>
<td style="text-align: center;">PE</td>
</tr>
<tr>
<td style="text-align: center;">端口号</td>
<td style="text-align: center;">A1</td>
<td style="text-align: center;">A2</td>
<td style="text-align: center;">A3</td>
<td style="text-align: center;">A4</td>
<td style="text-align: center;">A5</td>
<td style="text-align: center;">A6</td>
<td style="text-align: center;">A7</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">A9</td>
</tr>
<tr>
<td style="text-align: center;">名称</td>
<td style="text-align: center;">NTC1+</td>
<td style="text-align: center;">NTC2+</td>
<td style="text-align: center;">NTC3+</td>
<td style="text-align: center;">NTC4+</td>
<td style="text-align: center;">NTC5+</td>
<td style="text-align: center;">NTC6+</td>
<td style="text-align: center;">NTC7+</td>
<td style="text-align: center;">NTC8+</td>
<td style="text-align: center;">PE</td>
</tr>
</tbody>
</table>

### 2.3.10 RS485使用

以X90为例，6PIN端口：

RS485传输

使用RS485串口时，将RS485线接至端口上（ttl转485），打开sscom5和mobaxterm对接收发，如RS485-1端口（x90模块），其设备文件为/dev/ttyS1；设置其波特率设为
115200，8N1，无校验位。

stty -F /dev/ttyS1 ispeed 115200 ospeed 115200 cs8

echo 12345 /> /dev/ttyS1 //通过RS485-1端口发送数据

cat /dev/ttyS1 //等待查看接收到的数据

串口助手收到数据

<img
src="EdgePLC BL244说明书V1.1-images/image9.png"
style="width:5.77153in;height:0.22708in" />

串口助手发送数据

<img
src="EdgePLC BL244说明书V1.1-images/image10.png"
style="width:5.77153in;height:0.52986in" />

终端界面收到数据

<img
src="EdgePLC BL244说明书V1.1-images/image11.png"
style="width:5.76736in;height:0.50347in" />

按“Ctrl+C”停止。

然后更换x90另外一个ttyS8口继续测试。

### 2.3.11 CAN使用

1)  CAN-FD

在配置和使用 CAN
总线前，需确保系统已安装必要的通信工具包。请在终端执行以下命令完成
can-utils 工具的安装：

root@bliiot:~# apt install can-utils

<img
src="EdgePLC BL244说明书V1.1-images/image12.png"
style="width:5.76319in;height:1.77986in" />

在进行任何参数配置前，必须先关闭接口，否则配置将无法生效，配置 CAN0
的仲裁域波特率为 1000000，数据域波特率为 5000000，并强制开启 FD
功能。参数配置完成后，激活 CAN0 端口以准备通信。

root@bliiot:~# ip link set can0 down

root@bliiot:~# ip link set can0 type can bitrate 1000000 dbitrate
5000000 fd on

root@bliiot:~# ip link set can0 up

<img
src="EdgePLC BL244说明书V1.1-images/image13.png"
style="width:5.76319in;height:1.70972in" />

使用 cansend 命令向指定 ID 发送数据。以下示例向 ID 为 543 的节点发送 8
字节数据（00 01 02 03 04 05 06 07），其中000代表一位标识符和两位数据位：

root@bliiot:~# cansend can0 543##000.01.02.03.04.05.06.07

<img
src="EdgePLC BL244说明书V1.1-images/image15.png"
style="width:5.76319in;height:0.39653in" />

GCAN Tools工具收到数据

<img
src="EdgePLC BL244说明书V1.1-images/image16.png"
style="width:5.76181in;height:0.25694in" />

使用 candump 命令实时监听并打印 can0 接口接收到的所有数据：

root@bliiot:~# candump can0

<img
src="EdgePLC BL244说明书V1.1-images/image18.png"
style="width:5.76389in;height:0.34514in" />

若CAN0接收正常，用其它设备发送该数据则应收到

root@bliiot:~# candump can0

can0 000 /[8/] 11 22 33 44 55 66 77 88

<img
src="EdgePLC BL244说明书V1.1-images/image20.png"
style="width:5.76458in;height:0.45417in" />

<img
src="EdgePLC BL244说明书V1.1-images/image21.png"
style="width:5.76111in;height:0.51181in" />

扩展帧类似：

<img
src="EdgePLC BL244说明书V1.1-images/image22.png"
style="width:5.76736in;height:0.33611in" />

2)  CAN-2.0B

由于 CAN FD 硬件支持双模式，在初始化接口时可根据需求灵活配置。

root@bliiot:~# ip link set can0 down

root@bliiot:~# ip link set can0 type can bitrate 1000000 fd off

root@bliiot:~# ip link set can0 up

发送标准帧格式为cansend /<接口名/>
/<3位十六进制ID/>#/<数据/>，扩展帧必须严格补齐为 8 位十六进制字符（不足
8 位需在高位补零），具体格式为cansend /<接口名/>
/<8位十六进制ID/>#/<数据/>，这里以2.0B为例：向29位最大合法ID的节点发送数据长度为8字节的扩展帧。

root@bliiot:~# cansend can0 1FFFFFFF#AABBCCDDEEFF1122

<img
src="EdgePLC BL244说明书V1.1-images/image23.png"
style="width:5.76181in;height:0.35486in" />

GCAN Tools工具收到数据

<img
src="EdgePLC BL244说明书V1.1-images/image24.png"
style="width:5.76458in;height:0.37639in" />

使用 candump 命令实时监听并打印 can0 接口接收到的所有数据：

root@bliiot:~# candump can0

<img
src="EdgePLC BL244说明书V1.1-images/image18.png"
style="width:5.76389in;height:0.34514in" />

若CAN0接收正常，用其它设备发送该数据则应收到

root@bliiot:~# candump can0

can0 1FFFFFFF /[8/] AA BB CC DD EE FF 11 22

<img
src="EdgePLC BL244说明书V1.1-images/image25.png"
style="width:5.7625in;height:0.45347in" /><img
src="EdgePLC BL244说明书V1.1-images/image26.png"
style="width:5.76111in;height:0.49375in" />

### 2.3.12 N板端口使用

1)  **软件安装**

对应文件位置位于目录ion文件夹下,实际目录请以文件为准。

插上网线写入ifconfig指令获取IP，通过SSH登录

<img
src="EdgePLC BL244说明书V1.1-images/image27.png"
style="width:5.76319in;height:1.03264in" />

<img
src="EdgePLC BL244说明书V1.1-images/image29.png"
style="width:5.75903in;height:3.78958in" />

通过左边文件夹页面在usr/demo/文件夹下，新建ion文件夹，把N板识别文件复制进去

<img
src="EdgePLC BL244说明书V1.1-images/image31.png"
style="width:5.76319in;height:1.55833in" />

对BEILAI_N_PLC_244_V1.0_20260522.bin执行chmod +x
BEILAI_N_PLC_244_V1.0_20260522.bin。然后安装软件。

root@bliiot:/# chmod +x BEILAI_N_PLC_244_V1.0_20260522.bin

root@bliiot:/# ./BEILAI_N_PLC_244_V1.0_20260522.bin

Md5 verify pass!

Created symlink
/etc/systemd/system/multi-user.target.wants/iolib.service →
/etc/systemd/system/iolib.service.

Install complete!

2)  **端口使用**

<!-- -->

1.  **DO使用**

这里以N2162为准（16路DO模块NPN模块），ion show查看IO板信息。ion
help查看命令帮助。

root@bliiot:/# ion help

输入ion show查看信息。

<img
src="EdgePLC BL244说明书V1.1-images/image33.png"
style="width:5.76181in;height:0.86042in" />

<img
src="EdgePLC BL244说明书V1.1-images/image34.png"
style="width:5.76667in;height:2.14097in" />

也可通过get命令获取通道值：

root@bliiot:/# ion get 1014 //通过address查看

address 1014 value 0

<img
src="EdgePLC BL244说明书V1.1-images/image35.png"
style="width:5.76111in;height:0.25764in" />

root@bliiot:/# ion set 1000 10 //通过address设置输出10

root@bliiot:/# ion get 1000 //通过address查看

<img
src="EdgePLC BL244说明书V1.1-images/image36.png"
style="width:5.76458in;height:0.50347in" />

设置通道值有信号量会亮灯

对应的N2321、N2322、N2161、N2084类似。

2.  **DI使用**

以N1321为例（32路DI模块湿节点），DI模块为例，输入ion show查看信息。

湿节点测试(带电干结点)：以N1321为例（NPN型）

1、外接电源：将外接电源的正负极接到电源两端，以通道15为例，电源的正极接到模块的公共端（COM/0V），负极接到模块的
DI 输入端子。

2、灯亮，终端输入ion show查看已闭合。

PNP型则公共端接负极，输入端子接正极。

<img
src="EdgePLC BL244说明书V1.1-images/image37.png"
style="width:5.76042in;height:3.86181in" />

通过get命令获取通道值以及ion show查看信息

root@bliiot:/# ion get 2014 //通过address查看

address 2014 value 0

<img
src="EdgePLC BL244说明书V1.1-images/image38.png"
style="width:5.76597in;height:0.24722in" />

将DI15（即为15通道）短接

<img
src="EdgePLC BL244说明书V1.1-images/image39.png"
style="width:5.76806in;height:3.69583in" />

观察N板灯亮情况，对应DI短接形成回路灯亮。对应的N1162、N1161、N1322类似。

干接点以N1163、N1323为例，短接即可和上述类似。

3.  **AO使用**

以N4081为例（8路输出模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL244说明书V1.1-images/image40.png"
style="width:5.76528in;height:1.20625in" />

也可通过get命令获取通道值：

root@bliiot:/# ion get 4000 //通过address查看

address 4000 value 0

<img
src="EdgePLC BL244说明书V1.1-images/image41.png"
style="width:5.7625in;height:0.27014in" />

root@bliiot:/# ion set 4000 10 //通过address设置输出10mA

root@bliiot:/# ion get 4000 //通过address查看

<img
src="EdgePLC BL244说明书V1.1-images/image42.png"
style="width:5.76319in;height:0.49167in" />

通过高精度万用表直流电流档查看实际值与设置值是否相符,若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

对应的N4086差分输出电压类似。

<img
src="EdgePLC BL244说明书V1.1-images/image43.png"
style="width:5.76389in;height:1.35208in" />

4.  **AI使用**

以N3081为例（8路输入模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL244说明书V1.1-images/image44.png"
style="width:5.76736in;height:1.20139in" />

使用信号发生器输出目标电流值，观察实际值是否与输入值保持一致，如对第一个通道输出20mA,通过ion
show查看数值，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

以第一通道为例，设定输出20mA，界面显示的数值即为该通道的实际输出值。

root@bliiot:/# ion show

<img
src="EdgePLC BL244说明书V1.1-images/image45.png"
style="width:5.76528in;height:1.35903in" />

对应的N3083单端输入电压类似。

<img
src="EdgePLC BL244说明书V1.1-images/image46.png"
style="width:5.76319in;height:1.34583in" />

5.  **RTD使用**

以N5041为例（4路RTD模块三线PT100），量程设为-200-850℃，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL244说明书V1.1-images/image47.png"
style="width:5.7625in;height:0.87431in" />

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

对应的N5042、N5043、 N5044类似。

<img
src="EdgePLC BL244说明书V1.1-images/image48.png"
style="width:5.76597in;height:0.79583in" />

<img
src="EdgePLC BL244说明书V1.1-images/image49.png"
style="width:5.7625in;height:0.73681in" />

<img
src="EdgePLC BL244说明书V1.1-images/image50.png"
style="width:5.76597in;height:0.99028in" />

6.  **NTC使用**

以N3087为例（8路NTC模块10K3A1），量程为184.8-667828，输入ion
show查看信息。

root@bliiot:/# ion show

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

<img
src="EdgePLC BL244说明书V1.1-images/image51.png"
style="width:5.76458in;height:1.49444in" />

3)  **量程模式修改**

通过ion help命令，可以看到config的命令格式。

<img
src="EdgePLC BL244说明书V1.1-images/image52.png"
style="width:5.7625in;height:0.82847in" />

在终端中执行以下命令，以获取设备当前的运行状态及模式设置指令：

root@bliiot:/# ion getmode

<img
src="EdgePLC BL244说明书V1.1-images/image53.png"
style="width:5.76319in;height:0.66944in" />

确认目标模式对应的数值后，使用以下命令进行模式切换：例如将N4081的量程设置为4~20MA。

root@bliiot:/# ion setmode /<slot/> /<mode/>

root@bliiot:/# ion setmode 4 4

## 2.4 LED

<table style="width:63%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 49%" />
</colgroup>
<tbody>
<tr>
<td>LED灯</td>
<td>说明</td>
</tr>
<tr>
<td>PWR</td>
<td><p>电源灯，接入电源正常时常亮。</p>
<p>用户不可编辑。</p></td>
</tr>
<tr>
<td>RUN</td>
<td><p>默认设置：CPU使用率低于90%时闪烁，90%以上常亮。</p>
<p>用户可编辑。</p></td>
</tr>
<tr>
<td>LINK</td>
<td><p>默认设置：有互联网连接时常亮，无互联网连接时熄灭。</p>
<p>用户可编辑。</p></td>
</tr>
</tbody>
</table>

<img
src="EdgePLC BL244说明书V1.1-images/image54.jpeg"
style="width:1.36319in;height:3.39514in" alt="EdgePLC A款 (1)" />

LED指示灯如图,从左至右的顺序为LED2、LED1、LED0。其中LED2为POWER指示灯，上电后电源正常时常亮；LED1为RUN灯，系统正常运行时闪烁；LED0为LINK灯，使用有线网络连接互联网时常亮，4G或Wi-Fi时闪烁。文件为/etc/beilai_led.sh。

查看触发条件：cat /sys/class/leds/user-led0/trigger

root@bliiot:~# cat /sys/class/leds/user-led0/trigger

/[none/] rc-feedback mmc0 mmc1 mmc2 timer oneshot heartbeat backlight
gpio cpu0 cpu1 cpu2 cpu3 default-on transient

其中/[none/]表示当前led0的触发条件为无。往trigger中写上述字符串，可以修改触发条件。

当led触发条件设置为none时，用户可通过命令来控制led灯的亮灭

控制led0亮：echo 1 />/sys/class/leds/user-led0/brightness

root@bliiot:~# echo none />/sys/class/leds/user-led0/brightness

root@bliiot:~# echo 1 />/sys/class/leds/user-led0/brightness

控制led1灭：echo 0 />/sys/class/leds/user-led1/brightness

## 2.5 网络接口

<img
src="EdgePLC BL244说明书V1.1-images/image55.png"
style="width:1.02847in;height:2.53819in" alt="EdgePLC A款 (1)" />

如图所示，设备配备了两个千兆网口ETH1、ETH2，一个百兆网口ETH3

将网线插入ETH2，输入命令：

root@BL244:~# ifconfig

<img
src="EdgePLC BL244说明书V1.1-images/image56.png"
style="width:5.76806in;height:3.09931in" />

此时ETH2应显示为设定的静态IP地址192.168.1.167。

更换网口测试时关闭其他网口：

关闭网口1：ifconfig eth1 down

关闭网口3：ifconfig eth3 down

ping百度：ping 8.8.8.8 ，Ctrl+c结束

<img
src="EdgePLC BL244说明书V1.1-images/image57.png"
style="width:5.7625in;height:1.22847in" />

此时LINK灯亮。

## 2.6 USB接口

<img
src="EdgePLC BL244说明书V1.1-images/image58.png"
style="width:1.44722in;height:3.39167in" alt="EdgePLC A款 (1)" />

如图，设备带有2个USB2.0 HOST接口。支持FAT32格式U盘。

1.  接入测试用的U盘，这边run/media/sda为挂载文件夹，输入以下指令卸载并查看U盘是否可以检测：

lsblk（查看是否挂载） mkfs.vfat /dev/sda1(格式化分区更好测速)

umount /run/media/sda1（没有挂载就跳过）

lsblk

2.  可以看到sdb1，并且能够看到实际的内存大小

<img
src="EdgePLC BL244说明书V1.1-images/image59.png"
style="width:5.7625in;height:0.45208in" />

3.  安装fio工具

apt update

apt install fio -y //有就跳过，出厂一般自带

4.  然后输入以下指令测试写入：（第一次写入可以调成size=2G）

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=write -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

5.  可以看到写入的速度。

<img
src="EdgePLC BL244说明书V1.1-images/image60.png"
style="width:5.76597in;height:0.69097in" />

6.  再输入以下指令测试读取：

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=read -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

7.  可以看到读取的速度。

    <img
    src="EdgePLC BL244说明书V1.1-images/image61.png"
    style="width:5.76806in;height:0.64167in" />

8.  说明这个USB接口没有问题。

9.  更换下一个USB口，需要执行

ps aux /| grep fio //检查是否有残留进程，必要时用 kill
命令终止，然后再对进程同步sync

10. 重复B~F操作，没有问题说明USB端口正常。

<img
src="EdgePLC BL244说明书V1.1-images/image62.png"
style="width:5.76806in;height:0.44514in" />

## 2.7 HDMI接口

<img
src="EdgePLC BL244说明书V1.1-images/image63.png"
style="width:1.18611in;height:3.03611in" alt="EdgePLC A款 (1)" />

HDMI接口如图所示。支持HDMI 1.4和HDMI
2.0标准。系统默认支持的分辨率为1920x1080@60fps，最高支持HDMI显示分辨率为
4K。

将HDMI连接设备和显示器，此时显示器应显示桌面系统。若没有显示可尝试重启设备。

<img
src="EdgePLC BL244说明书V1.1-images/image64.png"
style="width:4.51528in;height:2.75833in" />

## 2.8 调试串口

<img
src="EdgePLC BL244说明书V1.1-images/image65.png"
style="width:3.82361in;height:1.42708in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

调试接口如图。可通过该端口进入设备系统。

## 2.9 SIM卡插槽

<img
src="EdgePLC BL244说明书V1.1-images/image66.png"
style="width:3.44583in;height:1.28681in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

SIM卡槽如图所示。

## 2.10 SD卡插槽

<img
src="EdgePLC BL244说明书V1.1-images/image67.png"
style="width:3.41458in;height:1.27431in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

SD卡槽如图所示，支持FAT32格式SD卡，以sd卡烧录为例。

1.  接入SD卡，属于系统启动卡，工作状态下，输入

fdisk -l

<img
src="EdgePLC BL244说明书V1.1-images/image68.png"
style="width:5.76667in;height:3.21111in" />

2.  系统识别到存储介质包含两个有效大分区，后续读写性能测试将限定在SD卡路径下进行”，并且可直观读取到该存储设备的实际物理容量。

3.  执行卸载指令

umount /dev/mmcblk1p8

4.  然后输入以下指令测试写入：

fio --filename=/dev/mmcblk1p8 --ioengine=psync --rw=write --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=write_job
--ramp_time=1 --direct=1

5.  可以看到工作状态下的（负载）写入的速度。

    <img
    src="EdgePLC BL244说明书V1.1-images/image69.png"
    style="width:5.76319in;height:0.73264in" />

6.  读取前需清除写入带来的缓存。

sync; echo 3 /| tee /proc/sys/vm/drop_caches

7.  再输入以下指令测试读取：

fio --filename=/dev/mmcblk1p8 --ioengine=psync --rw=read --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=read_job
--ramp_time=1 --direct=1

8.  可以看到工作状态下读取的速度。

    <img
    src="EdgePLC BL244说明书V1.1-images/image70.png"
    style="width:5.76667in;height:0.78611in" />

    A~F步骤都正常说明这个SD卡接口没有问题。

9.  测试完同步数据，重新测试需要清除缓存

sync; echo 3 /| tee /proc/sys/vm/drop_caches

## 2.11 重启按钮

<img
src="EdgePLC BL244说明书V1.1-images/image71.png"
style="width:3.48681in;height:1.30139in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

重启按钮如图所示。按下松开后设备重启。

注意：如需自定义RST按钮，请于下单前联系业务人员，默认配置为硬件复位。

## 2.12 PCIE接口

PCIE接口支持4G和Wi-Fi功能。

### 2.12.1 4G模块

此处使用移远EC200模块为例（AT命令端口为/dev/ttyUSB1），测试程序位于/usr/demo/4G目录下。插入电话卡，连接好天线。

（1）网络功能

ls /dev 看有没有ttyUSB开头的设备，没有就是没识别到模块

<img
src="EdgePLC BL244说明书V1.1-images/image72.png"
style="width:5.76181in;height:0.36319in" />

stty -F /dev/ttyUSB1 ispeed 115200 ospeed 115200 cs8 raw -echo
//设置串口

<img
src="EdgePLC BL244说明书V1.1-images/image73.png"
style="width:5.76736in;height:0.20833in" />

查信号 20以上 ：

cat /dev/ttyUSB1 & echo -e "AT+CSQ/r" /> /dev/ttyUSB1（输入1/2遍）

<img
src="EdgePLC BL244说明书V1.1-images/image74.png"
style="width:5.76389in;height:0.56806in" />

查是4G模块否能正常和SIM卡通讯：

echo -e "AT+CPIN?/r" /> /dev/ttyUSB1

<img
src="EdgePLC BL244说明书V1.1-images/image75.png"
style="width:5.76597in;height:0.46528in" />

EC200还需加一条拨号指令

echo -e "AT+QNETDEVCTL=3,1,1/r" /> /dev/ttyUSB1

查是否连接运营商，

echo -e "AT+COPS?/r" /> /dev/ttyUSB1

<img
src="EdgePLC BL244说明书V1.1-images/image76.png"
style="width:5.76181in;height:0.46111in" />

然后输入

udhcpc -i usb0

此时usb0应获取IP。

udhcpc: started, v1.30.1

udhcpc: sending discover

udhcpc: sending discover

udhcpc: sending select for 192.168.43.100

udhcpc: lease of 192.168.43.100 obtained, lease time 86400

<img
src="EdgePLC BL244说明书V1.1-images/image77.png"
style="width:5.76736in;height:0.6375in" />

然后通过ping www.baidu.com /8.8.8.8-I usb0 测试上网。

Ping不通百度加以下指令

echo "nameserver 8.8.8.8" /> /etc/resolv.conf

<img
src="EdgePLC BL244说明书V1.1-images/image78.png"
style="width:5.76806in;height:0.99653in" />

（2）短信功能

在测试程序目录下执行测试命令即可测试短信功能：

./send_sms /<device/> /<phonenumber/> /<text/>

命令说明：/<device/>为4G模块设备节点。/<phonenumber/>为发送短信目标手机号。/<text/>为短信发送内容，短信内容字符之间不可有空格，否则会提示错误。

例如：./send_sms /dev/ttyUSB1 152/*/*/*/*/*/*/*/* “test”

此时对应号码应收到内容为“test”的短信。

（3）通话功能

在测试程序目录下执行测试命令即可测试拨号功能：

./phone_call /<device/> /<phonenumber/>

命令说明：/<device/>为4G模块设备节点。/<phonenumber/>为拨打目标手机号。

例如：./phone_call /dev/ttyUSB1 152/*/*/*/*/*/*/*/*

此时对应号码应收到设备来电。

（4）GPS功能

在测试程序目录下执行测试命令即可测试GPS功能：

./get_location /<device/> /<timeout/>

命令说明：/<device/>为设备节点，以"ls
/dev/ttyUSB/*"命令查看结果为准，重启设备后可能会变化。/<timeout/>为等待返回经纬度信息的时间（单位为秒）。

例如：./get_location /dev/ttyUSB1 1

获取经纬度需等待几分钟时间，若获取失败、超时，请检查天线是否接好，并确保处于开阔场地进行测试。

### 2.12.2 Wi-Fi模块

此处使用的Wi-Fi模块为BL-R8188EU2（2.4G频段）。测试程序及驱动位于/usr/demo/Wi-Fi路径下，连接好天线。若无wlan0网卡，可按下方步骤安装驱动。

（1）STA功能

先查看该版本系统是否已自动加载Wi-Fi驱动：

lsmod

<img
src="EdgePLC BL244说明书V1.1-images/image79.png"
style="width:5.76597in;height:0.45347in" />

进入测试程序目录下，关闭其他网络，仅保留Wi-Fi网络，加载Wi-Fi驱动。

cd /usr/demo/wifi/ /# 进入驱动目录

ifconfig eth1 down

ifconfig eth2 down

ifconfig eth3 down //关闭其他网络

insmod -f 8188eu.ko //加载Wi-Fi驱动，有就跳过

连接Wi-Fi：

ifconfig wlan0 up /#打开wlan0

./wifi_setup.sh -i bliiot -p bebetter
/#连接Wi-Fi，-i后面接Wi-Fi名，-p后面接密码

<img
src="EdgePLC BL244说明书V1.1-images/image80.png"
style="width:5.75972in;height:2.34583in" />

ifconfig /#查看wlan0有无IP

<img
src="EdgePLC BL244说明书V1.1-images/image81.png"
style="width:5.76181in;height:0.70278in" />

最后ping百度测试：

ping www.baidu.com （百度域名不一定成功转IP，使用百度IP）

<img
src="EdgePLC BL244说明书V1.1-images/image82.png"
style="width:5.7625in;height:0.95833in" />

（2）AP功能

重启系统后，进入测试程序所在目录，关闭其他网络，仅保留Wi-Fi网络，加载Wi-Fi驱动。

ifconfig eth1 down

ifconfig eth2 down

ifconfig eth3 down //关闭其他网络

insmod -f 8188eu.ko //加载Wi-Fi驱动，有就跳过

执行如下命令，将Wi-Fi模块设置为AP模式。

./ap_setup.sh

默认设置的Wi-Fi名称为：rtl8188eu，密码为：88888888，可在rtl_hostapd_2G.conf配置文件内进行修改。

nano rtl_hostapd_2G.conf

## 2.13 M.2接口

### 2.13.1 SSD卡

1.  M.2接口插入固态硬盘，查看是否能检测出固态硬盘，输入以下指令，在返回列表中，查找名为
    nvme0n1 的设备及其容量大小。

lsblk -l

<img
src="EdgePLC BL244说明书V1.1-images/image83.png"
style="width:5.76181in;height:0.44514in" />

2.  测试前需要保证固态硬盘不是已经挂载的状态，为保证固态硬盘没有被挂载，所以执行卸载指令：

umount /run/media/nvme0n1 //已卸载则跳过

3.  写入测试数据：

fio -filename=/dev/nvme0n1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=write -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

<img
src="EdgePLC BL244说明书V1.1-images/image84.png"
style="width:5.76458in;height:0.54306in" />

4.  观察输出结果中的 WRITE 行，查看带宽（bw）数值，通常 NVMe
    固态硬盘写入速度应在 数百 MB/s
    以上（具体取决于硬盘性能）。若无报错且有速度数据输出，说明写入功能正常。

5.  读取测试：

fio -filename=/dev/nvme0n1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=read -bs=1024K
-size=5G -numjobs=1 -thread -group_reporting -name=read_job -ramp_time=1

<img
src="EdgePLC BL244说明书V1.1-images/image85.png"
style="width:5.76111in;height:0.61667in" />

6.  观察输出结果中的 READ
    行，查看带宽（bw）数值。若无报错且有速度数据输出，说明读取功能正常。则硬盘本身功能正常。

## 2.14 硬件看门狗

看门狗控制引脚：PE0，置1时关闭硬件看门狗。喂狗引脚：PG16。硬件看门狗超时时间为30ms。

## 2.15 外部RTC

本设备含一个外部RTC时钟。

查看外部 RTC 设备节点：

root@BL244-bliiot:~# ls /dev/rtc/*

/dev/rtc /dev/rtc0

root@BL244-bliiot:~# dmesg /| grep rtc0

/[ 4.319167/] rtc-isl1208 5-006f: rtc core: registered rtc-isl1208 as
rtc0

查看系统时钟：

root@BL244-bliiot:~# date

Thu 23 Apr 10:28:42 BST 2026

设置RTC时间：

root@BL244-bliiot:~# sudo hwclock --set --date="2026-4-23 17:30:00"

root@BL244-bliiot:~# sudo hwclock -r

同步RTC时钟至系统时钟：

root@BL244-bliiot:~# sudo hwclock -s

同步系统时钟到 RTC 的时钟：

root@BL244-bliiot:~# sudo hwclock -w

再次查看时间

root@BL244-bliiot:~# date

Thu 23 Apr 17:31:56 BST 2026

## 2.16 加密芯片

加密芯片型号为RJGT102。基于SHA-256的加密认证算法,
同时提供可配置的看门狗定时器和对外复位功能，与MCU通过 I²C-5
串行接口通信，芯片

支持低功耗模式。

设备内使用加密芯片的demo，是通过将/proc/sys/kernel/random/uuid写入加密芯片，同时保留uuid至/usr/rjgt_unique.json，使用时取出加密芯片数据进行对比,外部数据与加密芯片内部数据相同，则通过加密验证。

使用请自行修改Makefile文件中交叉编译器路径，再make编译；或参考《RJGT102数据手册》。

运行示例程序rigt102，若uuid正确，则会出现如下回复。

root@BL244:~#usr/demo/rjgt# ./rigt102

open unique file failed, create unique file!

random uuid would write rjgt102 : b6275e22-4928-4828-88fb-54a6fd8!

Contrast success

root@BL244:~#usr/demo/rjgt#./rigt102

Contrast success

# 3.设备登录

## 3.1 USB登录

进入此电脑——管理——设备管理器，打开端口，插入USB线到micro
USB，此时刷新的端口即为连接设备的端口。

<img
src="EdgePLC BL244说明书V1.1-images/image86.png"
style="width:3.62222in;height:2.76319in" />

此处以SecureCRT为例，在软件中新建连接，选择串口登录，选择对应的端口，波特率115200，数据位8，校验位None，停止位1。点击connect即可进入设备。

**Linux系统默认无登录密码**

**Ubuntu系统默认登录账号：root 密码：root**

<img
src="EdgePLC BL244说明书V1.1-images/image87.png"
style="width:2.10625in;height:1.92083in" />

## 3.2 SSH2登录

在使用网口登录前需设置对应网口的IP。此处以ETH2为例。此处ETH2已连接路由器，获取到的IP为192.168.2.107。电脑IP在2网段。

<img
src="EdgePLC BL244说明书V1.1-images/image88.png"
style="width:4.06875in;height:2.46944in" />

点击创建连接，选择协议为SSH2，主机名填写为设备IP：192.168.2.107，端口22，用户名root，点击Connect连接。

<img
src="EdgePLC BL244说明书V1.1-images/image89.png"
style="width:2.83958in;height:2.64653in" />

选择接受，即连接成功。

<img
src="EdgePLC BL244说明书V1.1-images/image90.png"
style="width:3.92778in;height:1.66389in" />

# 4.系统烧录

## 4.1 Micro SD卡启动

### 4.1.1 启动卡制作

由于BL244的镜像所需内存通常会大于4GB，所以在制作启动卡时需要将内存卡格式化为NTFS格式，并编辑“config.ini”文件。

<img
src="EdgePLC BL244说明书V1.1-images/image91.png"
style="width:5.3125in;height:2.23958in" alt="IMG_256" />

找到“System”项中添加“USER_DISK_FS=NTFS”内容，否则会导致烧录失败。

<img
src="EdgePLC BL244说明书V1.1-images/image92.png"
style="width:2.77083in;height:2.17917in" alt="IMG_256" />

将空白Micro
SD卡连接至电脑，打开“SDDiskTool_v1.69”文件夹，右键"SD_Firmware_Tool.exe"点击“以管理员身份运行(A)”。

<img
src="EdgePLC BL244说明书V1.1-images/image93.png"
style="width:5.76667in;height:1.82431in" />

在“第一步：选择可移动设备”中选择可移动磁盘设备，然后点击“恢复磁盘”进行格式化，如下图所示。

<img
src="EdgePLC BL244说明书V1.1-images/image94.png"
style="width:3.15486in;height:2.68403in" />

请确认所选的可移动磁盘设备无误，在弹出窗口中点击“是(Y)”进行格式化。

<img
src="EdgePLC BL244说明书V1.1-images/image95.png"
style="width:2.46736in;height:1.34028in" />

<img
src="EdgePLC BL244说明书V1.1-images/image96.png"
style="width:3.3in;height:2.81111in" />

等待格式化完成后，在弹出窗口中点击“确定”。

<img
src="EdgePLC BL244说明书V1.1-images/image97.png"
style="width:1.8125in;height:1.71875in" />

勾选“SD启动”选项，点击“选择固件”选择目标系统镜像文件，点击“开始创建”，在弹出窗口中点击“是(Y)”，制作SD启动卡。

<img
src="EdgePLC BL244说明书V1.1-images/image98.png"
style="width:2.90486in;height:2.4875in" />

<img
src="EdgePLC BL244说明书V1.1-images/image99.png"
style="width:3.36458in;height:1.72917in" />

<img
src="EdgePLC BL244说明书V1.1-images/image100.png"
style="width:4.94792in;height:4.20833in" />

在弹出的窗口中点击“确定”，此时 SD 启动卡制作完成。

<img
src="EdgePLC BL244说明书V1.1-images/image101.png"
style="width:2.00833in;height:1.69167in" />

### 4.1.2 从启动卡启动

将启动卡插至设备Micro
SD卡槽，然后将设备上电，系统将从启动卡启动后自动登录root用户，串口调试终端会打印如下类似启动信息。"Bootdev(atags):
mmc 1"表示从Micro SD卡启动。

<img
src="EdgePLC BL244说明书V1.1-images/image102.png"
style="width:5.76111in;height:2.53333in" />

## 4.2 EMMC启动

### 4.2.1 烧录卡制作

注意：eMMC 烧录过程依赖 SD 卡作为中转介质，其文件系统要求与 SD
卡启动完全一致。若未正确配置 config.ini，将导致镜像写入中断或 eMMC
无法识别系统分区。

将空白Micro
SD卡连接至电脑，打开“SDDiskTool_v1.69”文件夹，右键"SD_Firmware_Tool.exe"点击“以管理员身份运行(A)”。

<img
src="EdgePLC BL244说明书V1.1-images/image93.png"
style="width:5.76667in;height:1.82431in" />

工具运行后会自动识别接入到PC端的Micro SD卡，如下图所示。

在“第一步：选择可移动设备”中选择可移动磁盘设备，然后点击“恢复磁盘”进行格式化，如下图所示。

<img
src="EdgePLC BL244说明书V1.1-images/image103.png"
style="width:2.89167in;height:2.46389in" />

请确认所选的可移动磁盘设备无误，在弹出窗口中点击“是(Y)”进行格式化。

<img
src="EdgePLC BL244说明书V1.1-images/image95.png"
style="width:2.46736in;height:1.34028in" />

<img
src="EdgePLC BL244说明书V1.1-images/image104.png"
style="width:2.73542in;height:2.34375in" />

等待格式化完成后，在弹出窗口中点击“确定”。

<img
src="EdgePLC BL244说明书V1.1-images/image97.png"
style="width:1.8125in;height:1.71875in" />

勾选“固件升级”选项，点击“选择固件”选择目标系统镜像文件，点击“开始创建”，在弹出窗口中点击“是(Y)”，制作SD启动卡。

<img
src="EdgePLC BL244说明书V1.1-images/image105.png"
style="width:2.87639in;height:2.47222in" />

<img
src="EdgePLC BL244说明书V1.1-images/image106.png"
style="width:2.80139in;height:2.39722in" />

<img
src="EdgePLC BL244说明书V1.1-images/image107.png"
style="width:3.08889in;height:2.6375in" />

点击“是”。

<img
src="EdgePLC BL244说明书V1.1-images/image108.png"
style="width:3.08542in;height:2.60833in" />

开始烧写系统。

<img
src="EdgePLC BL244说明书V1.1-images/image109.png"
style="width:2.95556in;height:2.53403in" />

提示创建成功。

<img
src="EdgePLC BL244说明书V1.1-images/image110.png"
style="width:2.98472in;height:2.52014in" />

### 4.2.2 系统烧录

将制作好的SD卡插至设备Micro
SD卡槽，上电后将从SD卡启动，并自动固化系统至eMMC中。等待约5分钟。当系统固化完成后，设备将自动掉电。串口打印如下。

<img
src="EdgePLC BL244说明书V1.1-images/image111.png"
style="width:5.76111in;height:2.29306in" />

若为Ubuntu20.04系统则会弹出下图：

<img
src="EdgePLC BL244说明书V1.1-images/image112.png"
style="width:5.10903in;height:2.59514in" />

取出SD卡，波特率设置为115200，重新上电，设备将从eMMC启动系统，系统启动后自动登录root用户，串口调试终端会打印如下类似启动信息。"Bootdev(atags)：mmc
0"表示从eMMC启动。

<img
src="EdgePLC BL244说明书V1.1-images/image113.png"
style="width:5.55208in;height:3.04167in" />

# 5.导轨安装

配备导轨卡扣分为下段式短款导轨结构。此设计预留了充足的螺丝锁付空间，便于用户进行安装操作。

<img
src="EdgePLC BL244说明书V1.1-images/image114.png"
style="width:1.42569in;height:2.77153in"
alt="8aec9eb215acbbce3b8954b2e1062111_compress" /><img
src="EdgePLC BL244说明书V1.1-images/image115.png"
style="width:1.41389in;height:2.76042in"
alt="8aec9eb215acbbce3b8954b2e1062111_compress" />

将卡扣垂直向下按压，直至其完全嵌入并锁定于导轨底部，即可完成安装。长导轨卡无需额外卡扣，因其内部已预设专用凹槽结构，可直接实现稳固连接。

<img
src="EdgePLC BL244说明书V1.1-images/image116.png"
style="width:0.83611in;height:1.94236in"
alt="ac31d771be6b72005cba9ec2e46da2bc_compress" />

# 6.软件支持

- OpenPLC

  详细使用方法请参考《OpenPLC使用说明书》

- Node-Red

  详细使用方法请参考《Node-Red使用说明书》

<!-- -->

- QuickConfig

  详细使用方法请参考《QuickConfig使用说明书》

- BLRAT

  详细使用方法请参考《BLRAT使用说明书》

- 

- 

- EdgeCoder

  详细使用方法请参考《EdgeCoder使用说明书》

- Codesys

  详细使用方法请参考《Codesys使用说明书》

NexPLC、BLIoTLink、FUXA等软件平台将持续迭代更新。如需获取进一步的技术支持或了解后续规划，欢迎随时与我们联系。

# 7.电磁兼容性

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 17%" />
<col style="width: 20%" />
<col style="width: 10%" />
<col style="width: 19%" />
<col style="width: 7%" />
<col style="width: 16%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>测试类别</strong></td>
<td style="text-align: center;"><strong>测试项目</strong></td>
<td style="text-align: center;"><strong>测试标准</strong></td>
<td style="text-align: center;"><strong>测试等级</strong></td>
<td style="text-align: center;"><strong>测试条件</strong></td>
<td style="text-align: center;"><strong>测试结果</strong></td>
<td style="text-align: center;"><strong>备注</strong></td>
</tr>
<tr>
<td rowspan="2"
style="text-align: center;"><strong>电磁发射</strong></td>
<td style="text-align: center;">传导发射</td>
<td style="text-align: center;"><p>GB/T 9254 Class A/</p>
<p><strong>CISPR 32</strong> Class A</p></td>
<td style="text-align: center;">Class A</td>
<td style="text-align: center;">150 kHz - 30 MHz</td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">满足普通工业环境限值要求</td>
</tr>
<tr>
<td style="text-align: center;">辐射发射</td>
<td style="text-align: center;"><p>GB/T 9254 Class A/</p>
<p><strong>CISPR 32</strong> Class A</p></td>
<td style="text-align: center;">Class A</td>
<td style="text-align: center;">30 MHz - 1 GHz</td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">满足普通工业环境限值要求</td>
</tr>
<tr>
<td rowspan="6"
style="text-align: center;"><strong>抗扰度测试</strong></td>
<td style="text-align: center;">静电放电（ESD）</td>
<td style="text-align: center;">GB/T 17626.2/<strong>IEC
61000-4-2</strong></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>接触放电 +/-4 kV</p>
<p>空气放电 +/-8 kV</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
<tr>
<td style="text-align: center;">射频辐射抗扰度</td>
<td style="text-align: center;"><p>GB/T 17626.3/</p>
<p><strong>IEC 61000-4-3</strong></p></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>场强 10 V/m，</p>
<p>80 MHz - 1 GHz</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
<tr>
<td style="text-align: center;">电快速瞬变脉冲群（EFT）</td>
<td style="text-align: center;">GB/T 17626.4/ <strong>IEC
61000-4-4</strong></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>电源线 2 kV</p>
<p>信号线 1 kV</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
<tr>
<td style="text-align: center;">浪涌（Surge）</td>
<td style="text-align: center;">GB/T 17626.5/ <strong>IEC
61000-4-5</strong></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>差模 2 kV</p>
<p>共模 4 kV</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
<tr>
<td style="text-align: center;">电压暂降和中断</td>
<td style="text-align: center;">GB/T 17626.11/ <strong>IEC
61000-4-11</strong></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>电压暂降70%</p>
<p>持续500ms，</p>
<p>完全中断10 ms</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
<tr>
<td style="text-align: center;">工频磁场抗扰度</td>
<td style="text-align: center;">GB/T 17626.8/ <strong>IEC
61000-4-8</strong></td>
<td style="text-align: center;">III 级</td>
<td style="text-align: center;"><p>测试强度30 A/m</p>
<p>工频50 Hz</p></td>
<td style="text-align: center;">合格</td>
<td style="text-align: center;">—</td>
</tr>
</tbody>
</table>

注：如果电快速瞬变脉冲群（EFT）需要达到3级标准，需要单独购买我公司的滤波模块。

# 8.保修条款

1/) 此设备从购买之日算起，为期一年内有任何材料或质量问题，免费维修。

2/) 此一年保修不包括任何人为损坏、操作不当等造成的产品故障问题。

# 9.技术支持

深圳市钡铼技术有限公司

电话：0755-29451836

网址：[http://www.bliiot.com](http://www.4g-iot.com)

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 7%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 14%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td colspan="8" style="text-align: left;"></td>
</tr>
</tbody>
</table>