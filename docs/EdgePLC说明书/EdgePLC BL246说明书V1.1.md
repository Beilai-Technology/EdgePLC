<figure>
<img
src="EdgePLC BL246说明书V1.1-images/image2.jpeg"
style="width:2.97639in;height:3.98056in" alt="EdgePLC A款 (2)" />
<figcaption><p>版本：V1.1<br />
日期：2026-09-10<br />
版权：<strong>深圳市钡铼技术有限公司<br />
</strong>网址：<a
href="http://www.bliiot.cn">www.bliiot.cn</a></p></figcaption>
</figure>

EdgePLC BL246系列

<figure>
<img
src="EdgePLC BL246说明书V1.1-images/image1.png"
style="width:2.68681in;height:1.89653in" />
<figcaption><p>说明书</p></figcaption>
</figure>

EdgePLC BL246工业AI边缘控制器

**前言**

感谢您使用深圳市钡铼技术有限公司的BL246系列，阅读本产品说明书能让您快速掌握本产品的功能和使用方法。

> **版权声明**

本说明书之所有权由深圳市钡铼技术有限公司所有。未经本公司之书面许可，任何单位和个人无权以任何形式复制、传播和转载本手册之任何部分，否则一切后果由违者自负。

> **免责声明**

由于运营商升级网络造成设备无法继续使用的，本公司不能提供免费的升级服务。由于特殊原因造成运营商网络服务中断时，本机将无法正常工作，本公司不承担由此带来的后果。

本产品主要用于基于GPRS/网络的数据传输应用，请按照说明书提供的参数和技术规格使用，同时请注意无线电产品特别是GPRS产品使用时应该关注的注意事项，本公司不承担由于不正常使用或不恰当使用本产品造成的财产或人身伤害。

本产品包含开源软件或第三方组件。因开源软件的缺陷、漏洞、兼容性问题、停止维护或协议变更等原因导致的系统故障、数据丢失或安全问题，本公司概不负责。用户需自行承担使用开源组件的相关风险。

**修订记录**

|  |  |  |  |  |
|:--:|:--:|:--:|:--:|:--:|
| **更新日期** | **文档版本** | **说明** | **修订内容** | **作者** |
| 2026.4.24 | Ver.1.0 | 首次发布 |  | ZJX |
| 2026.7.31 | Ver.1.1 | 部分更新 | 完善RTD、NTC N板使用说明，增加量程模式修改，优化软件支持 | ZJX |

# 1.产品简介

## 1.1 概述

在工业自动化向“AI边缘计算+实时控制”深度融合的转型背景下，传统PLC面临智能计算的瓶颈，而通用工业计算机又难以满足高实时性控制的需求。EdgePLC
BL246系列工业AI边缘控制器应运而生，旨在打破IT与OT的融合壁垒，提供真正意义上的“边缘AI控算一体”解决方案。

BL246系列采用“树莓派5核心处理器 +
分布式I/O扩展”的架构，树莓派5以Broadcom
BCM2712为核心，基于四核Cortex-A76架构，在保障毫秒级实时控制的同时，搭配AI算力棒可具备强大的本地AI推理与数据处理能力。BL246系列接入树莓派软件生态，兼容主流开发工具、应用和硬件驱动库，同时拥有全球最大的爱好者社区，官方文档详尽，教程和开源项目极其丰富。

EdgePLC
BL246工业AI边缘控制器深度融合实时控制、AI边缘智能、协议转换、远程运维与二次开发等功能，支持IEC
61131-3标准编程环境（OpenPLC/NexPLC/CODESYS）、IGH
EtherCAT硬实时主站，并可扩展多达32块N系列分布式I/O模块，覆盖DI/DO/AI/AO/温度采集等多种信号类型。软件层面基于Ubuntu
20.04系统，集成Docker、Node-RED、Python/C++开发环境，以及YOLOv5/8+OpenCV等AI视觉工具栈，实现从数据采集、实时分析到智能决策的全流程闭环。

BL246系列工业AI边缘控制器专为智能产线控制、储能EMS、光伏逆变器管理、AGV机器人、机器视觉等“控制+计算”协同场景设计，通过将智能分析下沉至设备边缘，它不仅实现了控制逻辑的精准执行，更完成了数据价值的就地转化与智能决策，助力企业构建更敏捷、更智能、更高效的下一代工业控制系统，从容应对智能制造的未来挑战。

## 1.2 外形尺寸

产品外观结构与尺寸如下图：

<img
src="EdgePLC BL246说明书V1.1-images/image4.png"
style="width:2.29236in;height:2.85556in"
alt="F:/2025_9/EdgePLC/标签外壳/标准款清晰图片.png标准款清晰图片" /><img
src="EdgePLC BL246说明书V1.1-images/image5.png"
style="width:2.30972in;height:2.87986in"
alt="F:/2025_9/EdgePLC/标签外壳/A款清晰图片.pngA款清晰图片" />

## 1.3 技术参数

<table style="width:99%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 19%" />
<col style="width: 62%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"><strong>分类</strong></td>
<td style="text-align: center;"><strong>参数</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr>
<td rowspan="5" style="text-align: center;">系统</td>
<td style="text-align: center;">处理器型号</td>
<td>Broadcom BCM2712</td>
</tr>
<tr>
<td style="text-align: center;">处理器频率</td>
<td><p>四核 Arm Cortex-A76</p>
<p>主频： 2.4 GHz，带加密扩展，每核 512KB L2 缓存，2MB 共享 L3
缓存</p></td>
</tr>
<tr>
<td style="text-align: center;">GPU</td>
<td>GPU：VideoCore VII GPU，支持 OpenGL ES 3.1、Vulkan 1.2、4Kp60 HEVC
解码器</td>
</tr>
<tr>
<td style="text-align: center;">内存</td>
<td>2/4/8/16GByte LPDDR4X</td>
</tr>
<tr>
<td style="text-align: center;">存储</td>
<td>8/16/32/64GByte eMMC</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">电源</td>
<td style="text-align: center;">输入电压</td>
<td>DC 12-24V （输入：24V,输出：12V）</td>
</tr>
<tr>
<td style="text-align: center;">功耗</td>
<td><p>正常：318mA@12V（带4G模块），285mA@12V（不带4G模块）</p>
<p>最大：700mA@12V</p></td>
</tr>
<tr>
<td style="text-align: center;">反接防护</td>
<td>支持</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">网口</td>
<td style="text-align: center;">网口规格</td>
<td>RJ-45 接口，2~3个，1个10/100/1000M、2个10/100M 自适应网口</td>
</tr>
<tr>
<td style="text-align: center;">网口保护</td>
<td>ESD ±4kV（接触），±8kV（空气）；</td>
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
<td style="text-align: center;">USB接口</td>
<td style="text-align: center;">数量</td>
<td>1*micro USB，2*USB 3.0 HOST</td>
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
<td style="text-align: center;">M.2接口</td>
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
<td>STA</td>
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
<td>-20～85℃，5～95% RH</td>
</tr>
<tr>
<td style="text-align: center;">存储温度、湿度</td>
<td>-20～85℃，5～95% RH</td>
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
<td><p>Debian 12(Operating System: Raspberry Pi OS)</p>
<p>Kernel: Linux 6.6.78-v8-16k</p></td>
</tr>
</tbody>
</table>

## 1.4 设备选型

### 1.4.1 主型号选型

|          |                           |         |          |             |             |
|:--------:|:-------------------------:|:-------:|:--------:|:-----------:|:-----------:|
| **型号** |          **ETH**          | **USB** | **HDMI** | **N板IO槽** |  **尺寸**   |
|  BL246   | 1x10/100/1000M, 1x10/100M |    2    |    0     |      1      | 38x92x110mm |
|  BL246A  | 1x10/100/1000M, 2x10/100M |    2    |    1     |      1      | 38x92x110mm |

**BL246系列选型**

### 1.4.2 SOM选型表

可以根据需求，选择合适的ROM、RAM以及温度等级。

**BL246系列SOM选型表**

|  |  |  |  |  |  |  |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **型号** | **MCU** | **主频** | **无线** | **eMMC** | **LPDDR4X** | **温度级别** |
| CM5002000（可选） | BCM2712 | 2.4GHz | x | 0GB (Lite) | 2GB | -20~85℃ |
| CM5002016 | BCM2712 | 2.4GHz | x | 16GB | 2GB | -20~85℃ |
| CM5002032 | BCM2712 | 2.4GHz | x | 32GB | 2GB | -20~85℃ |
| CM5004000（可选） | BCM2712 | 2.4GHz | x | 0GB (Lite) | 4GB | -20~85℃ |
| CM5004016 | BCM2712 | 2.4GHz | x | 16GB | 4GB | -20~85℃ |
| CM5004032 | BCM2712 | 2.4GHz | x | 32GB | 4GB | -20~85℃ |
| CM5008000（可选） | BCM2712 | 2.4GHz | x | 0GB (Lite) | 8GB | -20~85℃ |
| CM5008016 | BCM2712 | 2.4GHz | x | 16GB | 8GB | -20~85℃ |
| CM5008032 | BCM2712 | 2.4GHz | x | 32GB | 8GB | -20~85℃ |
| CM5016000（可选） | BCM2712 | 2.4GHz | x | 0GB (Lite) | 16GB | -20~85℃ |
| CM5016016（可选） | BCM2712 | 2.4GHz | x | 16GB | 16GB | -20~85℃ |
| CM5016032（可选） | BCM2712 | 2.4GHz | x | 32GB | 16GB | -20~85℃ |
| CM5016064（可选） | BCM2712 | 2.4GHz | x | 64GB | 16GB | -20~85℃ |
| CM5102000（可选） | BCM2712 | 2.4GHz | PCB/ext | 0GB (Lite) | 2GB | -20~85℃ |
| CM5102016（可选） | BCM2712 | 2.4GHz | PCB/ext | 16GB | 2GB | -20~85℃ |
| CM5102032（可选） | BCM2712 | 2.4GHz | PCB/ext | 32GB | 2GB | -20~85℃ |
| CM5104000（可选） | BCM2712 | 2.4GHz | PCB/ext | 0GB (Lite) | 4GB | -20~85℃ |
| CM5104016（可选） | BCM2712 | 2.4GHz | PCB/ext | 16GB | 4GB | -20~85℃ |
| CM5104032（可选） | BCM2712 | 2.4GHz | PCB/ext | 32GB | 4GB | -20~85℃ |
| CM5108000（可选） | BCM2712 | 2.4GHz | PCB/ext | 0GB (Lite) | 8GB | -20~85℃ |
| CM5108016（可选） | BCM2712 | 2.4GHz | PCB/ext | 16GB | 8GB | -20~85℃ |
| CM5108032（可选） | BCM2712 | 2.4GHz | PCB/ext | 32GB | 8GB | -20~85℃ |
| CM5108064（可选） | BCM2712 | 2.4GHz | PCB/ext | 64GB | 8GB | -20~85℃ |
| CM5116000（可选） | BCM2712 | 2.4GHz | PCB/ext | 0GB (Lite) | 16GB | -20~85℃ |
| CM5116016（可选） | BCM2712 | 2.4GHz | PCB/ext | 16GB | 16GB | -20~85℃ |
| CM5116032（可选） | BCM2712 | 2.4GHz | PCB/ext | 32GB | 16GB | -20~85℃ |
| CM5116064（可选） | BCM2712 | 2.4GHz | PCB/ext | 64GB | 16GB | -20~85℃ |

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
style="text-align: left;"><strong>X系列IO板选型表</strong></td>
<td style="text-align: left;"></td>
<td style="text-align: left;"></td>
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
<td style="text-align: center;">BL246不支持</td>
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
src="EdgePLC BL246说明书V1.1-images/image6.png"
style="width:3.14375in;height:1.87847in" alt="EdgePLC A款 (10)" /><img
src="EdgePLC BL246说明书V1.1-images/image7.png"
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
src="EdgePLC BL246说明书V1.1-images/image8.png"
style="width:2.57639in;height:1.04931in"
alt="e2c8802fdadeb1e5530381aefa943291_origin(1)" />。

设备提供1路输入。支持DC12~24V输入，支持反接防护

## 2.3 模块端口说明

根据不同的X/N板，有不同的串口可选择。目前可选板型如下。

### 2.3.1 RS485模块

<table style="width:100%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 13%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 13%" />
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
<td style="text-align: center;">ttyACM0-A</td>
<td style="text-align: center;">ttyACM0-B</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">ttyAMA2-A</td>
<td style="text-align: center;">ttyAMA2-B</td>
<td style="text-align: center;">GND</td>
</tr>
</tbody>
</table>

### 2.3.2 DI模块

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

### 2.3.3 DO模块

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

### 2.3.4 AO模块

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

### 2.3.5 AI模块

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

### 2.3.6 RTD模块

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

### 2.3.7 TC模块

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

### 2.3.8 NTC模块

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

### 2.3.9 RS485使用

以x90为例，6PIN端口：

RS485传输

使用RS485串口时，将RS485线接至端口上（ttl转485），打开sscom5和mobaxterm对接收发。

x90是x23模块引出的设备带有其中2个RS485，先查看是否识别到串口设备ttyAMA和ttyACM。

ls /dev

<img
src="EdgePLC BL246说明书V1.1-images/image9.png"
style="width:5.76667in;height:1.52917in" />

如未识别到设备“ttyAMA2和ttyAMA4”，检查启动文件中是否添加如下配置，把UART复用到GPIO。

启用 UART2 并复用到 GPIO4 (TXD) 和 GPIO5 (RXD)。

sudo nano /boot/firmware/config.txt //打开启动文件

dtoverlay=uart2,txd2_pin=4,rxd2_pin=5 //在末尾添加语句

启用 UART4 并复用到 GPIO12 (TXD) 和 GPIO13 (RXD)。

dtoverlay=uart4,txd2_pin=12,rxd2_pin=13

<img
src="EdgePLC BL246说明书V1.1-images/image10.png"
style="width:5.76319in;height:0.69583in" />

设置完后重启设备通过指令查看

ls /dev/ttyA/*

<img
src="EdgePLC BL246说明书V1.1-images/image11.png"
style="width:5.76458in;height:0.54375in" />

BL246中“ttyACM0-TX”和“ttyACM0-RX”表示一组RS485串口线。使用RS485串口时，将RS485线接至端口上，如x90模块中有ttyACM0和ttyAMA2两个串口，以ttyAMA2为例，其设备文件为/dev/ttyACM2；设置其波特率设为
115200，8N1，无校验位。

stty -F /dev/ttyAMA2 ispeed 115200 ospeed 115200 cs8

echo 12345 /> /dev/ttyAMA2 //通过RS485-2端口发送数据

cat /dev/ttyAMA2 //等待查看接收到的数据

按“Ctrl+C”停止。

串口助手收到数据

<img
src="EdgePLC BL246说明书V1.1-images/image12.png"
style="width:5.76597in;height:0.19653in" />

串口助手发送数据

<img
src="EdgePLC BL246说明书V1.1-images/image13.png"
style="width:5.76042in;height:0.39861in" />

终端界面收到数据

<img
src="EdgePLC BL246说明书V1.1-images/image14.png"
style="width:5.76736in;height:0.50139in" />

按“Ctrl+C”停止。

更换ttyACM0串口继续调试。

### 2.3.10 N板端口使用

1)  **软件安装**

对应文件位置位于**/ion**文件夹下。实际目录请以文件为准。复制需要的bin文件到U盘。

插上网线写入ifconfig指令获取IP，通过SSH登录

<img
src="EdgePLC BL246说明书V1.1-images/image15.png"
style="width:5.76042in;height:1.14444in" />

<img
src="EdgePLC BL246说明书V1.1-images/image16.png"
style="width:5.76042in;height:3.58125in" />

通过左边文件夹页面在usr/demo/文件夹下，新建ion文件夹，把N板识别文件复制进去

<img
src="EdgePLC BL246说明书V1.1-images/image17.png"
style="width:5.75764in;height:1.77708in" />

对BEILAI_N_PLC_246_V1.0_20260522.bin执行chmod +x
BEILAI_N_PLC_246_V1.0_20260522.bin。然后安装软件。

root@bliiot:/# chmod +x BEILAI_N_PLC_246_V1.0_20260522.bin

root@bliiot:/# ./BEILAI_N_PLC_246_V1.0_20260522.bin

Md5 verify pass!

Created symlink
/etc/systemd/system/multi-user.target.wants/iolib.service →
/etc/systemd/system/iolib.service.

Install complete!

执行完毕后即可使用。

2)  **端口使用**

<!-- -->

1.  **DO使用**

这里以N2161为准（16路DO模块pnp），ion show查看IO板信息。ion
help查看命令帮助。

root@bliiot:/# ion help

输入ion show查看信息。

<img
src="EdgePLC BL246说明书V1.1-images/image18.png"
style="width:5.76389in;height:1.20417in" />

<img
src="EdgePLC BL246说明书V1.1-images/image19.png"
style="width:5.76736in;height:2.59375in" />

也可通过get命令获取通道值：

root@bliiot:/# ion get 1014 //通过address查看

address 1014 value 0

<img
src="EdgePLC BL246说明书V1.1-images/image20.png"
style="width:5.76528in;height:0.40486in" />

root@bliiot:/# ion set 1000 1 //通过address设置输出1

root@bliiot:/# ion get 1000 //通过address查看

<img
src="EdgePLC BL246说明书V1.1-images/image21.png"
style="width:5.76528in;height:0.71319in" />

设置通道值有信号量会亮灯

对应的N2321、N2322、N2162、N2084类似。

2.  **DI使用**

以N1161为例（16路DI模块湿节点），DI模块为例，输入ion show查看信息。

湿节点测试(带电干结点)：以N1161为例（NPN型）

1、外接电源：将外接电源的正负极接到电源两端，以通道15为例，电源的正极接到模块的公共端（COM/0V），负极接到模块的
DI 输入端子。

2、灯亮，终端输入ion show查看已闭合。

PNP型则公共端接负极，输入端子接正极。

<img
src="EdgePLC BL246说明书V1.1-images/image22.png"
style="width:5.76042in;height:1.96181in" />

通过get命令获取通道值以及ion show查看信息

root@bliiot:/# ion get 2014 //通过address查看

address 2014 value 0

<img
src="EdgePLC BL246说明书V1.1-images/image23.png"
style="width:5.76319in;height:0.22708in" />

将DI15（即为15通道）短接

<img
src="EdgePLC BL246说明书V1.1-images/image24.png"
style="width:5.76389in;height:2.11667in" />

观察N板灯亮情况，对应DI短接形成回路灯亮。对应的N1162、N1321、N1322类似。

干接点以N1163、N1323为例，短接即可和上述类似。

3.  **AO使用**

以N4081为例（8路输出模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL246说明书V1.1-images/image25.png"
style="width:5.76111in;height:1.10625in" />

也可通过get命令获取通道值：

root@bliiot:/# ion get 4000 //通过address查看

address 4000 value 0

<img
src="EdgePLC BL246说明书V1.1-images/image26.png"
style="width:5.76806in;height:0.27222in" />

root@bliiot:/# ion set 4000 10 //通过address设置输出10mA

root@bliiot:/# ion get 4000 //通过address查看

<img
src="EdgePLC BL246说明书V1.1-images/image27.png"
style="width:5.76319in;height:0.60694in" />

通过高精度万用表直流电流档查看实际值与设置值是否相符,若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

对应的N4086差分输出电压类似。

<img
src="EdgePLC BL246说明书V1.1-images/image28.png"
style="width:5.76111in;height:1.21806in" />

4.  **AI使用**

以N3081为例（8路输入模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL246说明书V1.1-images/image29.png"
style="width:5.76389in;height:1.27708in" />

使用信号发生器输出目标电流值，观察实际值是否与输入值保持一致，如对第一个通道输出20mA,通过ion
show查看数值，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

以第一通道为例，设定输出20mA，界面显示的数值即为该通道的实际输出值。

root@bliiot:/# ion show

<img
src="EdgePLC BL246说明书V1.1-images/image30.png"
style="width:5.76319in;height:1.40972in" />

对应的N3083单端输入电压类似。

<img
src="EdgePLC BL246说明书V1.1-images/image31.png"
style="width:5.76597in;height:1.4375in" />

5.  **RTD使用**

以N5041为例（4路RTD模块三线PT100），量程设为-200-850℃，输入ion
show查看信息。

root@bliiot:/# ion show

<img
src="EdgePLC BL246说明书V1.1-images/image32.png"
style="width:5.76806in;height:0.90278in" />

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

对应的N5042、N5043、 N5044类似。

<img
src="EdgePLC BL246说明书V1.1-images/image33.png"
style="width:5.76389in;height:0.77917in" />

<img
src="EdgePLC BL246说明书V1.1-images/image34.png"
style="width:5.76389in;height:0.69931in" />

<img
src="EdgePLC BL246说明书V1.1-images/image35.png"
style="width:5.76111in;height:1.01458in" />

6.  **NTC使用**

以N3087为例（8路NTC模块10K3A1），量程为184.8-667828，输入ion
show查看信息。

root@bliiot:/# ion show

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

<img
src="EdgePLC BL246说明书V1.1-images/image36.png"
style="width:5.76458in;height:1.45903in" />

3)  **量程模式修改**

通过ion help命令，可以看到config的命令格式。

<img
src="EdgePLC BL246说明书V1.1-images/image37.png"
style="width:5.7625in;height:0.82847in" />

在终端中执行以下命令，以获取设备当前的运行状态及模式设置指令：

root@bliiot:/# ion getmode

<img
src="EdgePLC BL246说明书V1.1-images/image38.png"
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
src="EdgePLC BL246说明书V1.1-images/image39.jpeg"
style="width:1.36319in;height:3.39514in" alt="EdgePLC A款 (1)" />

LED指示灯如图,从左至右的顺序为LED2、LED1、LED0。其中LED2为POWER指示灯，上电后电源正常时常亮；LED1为RUN灯，系统正常运行时闪烁；LED0为LINK灯，使用有线网络连接互联网时常亮，4G或Wi-Fi时闪烁。文件为/etc/beilai_led.sh。

用户可通过wiringpi来控制led灯的亮灭

进入到gpio控制界面

root@BL246:~#cd /usr/demo/wiringpi/

输入gpio readall查看可控制的GPIO口：

root@BL246:~#usr/demo/wiringpi# gpio readall

控制led0亮：

root@BL246:~#usr/demo/wiringpi# gpio write 0 1

控制led1灭：

root@BL246:~#usr/demo/wiringpi# gpio write 8 0

## 2.5 配置ETH1的静态IP

在命令窗格执行如下命令：

sudo nano /etc/NetworkManager/system-connections/static-eth0.nmconnection
//修改静态地址配置文件

/[connection/]/
id=static-eth1 //要修改的网口连接id/
type=ethernet/
interface-name=eth1 //要修改的网口名称/
autoconnect=true/
/
/[ipv4/]/
method=manual //设为手动获取IP/
addresses1=192.168.1.110/24,192.168.1.1 //修改的地址和网关/
dns=8.8.8.8;1.1.1.1;/
/
/[ipv6/]/
method=auto //设置为自动获取IP

## 2.6 网络接口

<img
src="EdgePLC BL246说明书V1.1-images/image40.png"
style="width:1.02847in;height:2.53819in" alt="EdgePLC A款 (1)" />

如图所示，设备配备了一个千兆网口ETH1 、两个百兆网口ETH2、ETH3

将网线插入ETH3，输入命令：

root@BL246:~# ifconfig

<img
src="EdgePLC BL246说明书V1.1-images/image41.png"
style="width:5.7625in;height:1.00903in" />

此时ETH2应显示为设定的静态IP地址192.168.1.19。

更换网口测试时关闭其他网口：

关闭网口1：ifconfig eth1 down

关闭网口2：ifconfig eth2 down

ping百度：ping [www.baidu.com](http://www.baidu.com) ，Ctrl+c结束

<img
src="EdgePLC BL246说明书V1.1-images/image42.png"
style="width:5.76458in;height:1.175in" />

此时LINK灯亮。

## 2.7 USB接口

<img
src="EdgePLC BL246说明书V1.1-images/image43.png"
style="width:1.44722in;height:3.39167in" alt="EdgePLC A款 (1)" />

如图，设备带有2个USB3.0 HOST接口。支持FAT32格式U盘。

1.  接入测试用的U盘，这边run/media/sda为挂载文件夹，输入以下指令卸载并查看U盘是否可以检测：

lsblk（查看是否挂载） mkfs.vfat /dev/sda1(格式化分区更好测速)

umount /run/media/sda1（没有挂载就跳过）

lsblk

2.  可以看到sdb1，并且能够看到实际的内存大小

<img
src="EdgePLC BL246说明书V1.1-images/image44.png"
style="width:5.76458in;height:0.45764in" />

3.  然后输入以下指令测试写入：（第一次写入可以调成size=2G）

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=write -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

4.  可以看到写入的速度。

<img
src="EdgePLC BL246说明书V1.1-images/image45.png"
style="width:5.76042in;height:0.80972in" />

5.  再输入以下指令测试读取：

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=read -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

6.  可以看到读取的速度。

    <img
    src="EdgePLC BL246说明书V1.1-images/image46.png"
    style="width:5.76042in;height:0.72222in" />

7.  说明这个USB接口没有问题。

8.  更换下一个USB口，需要执行

ps aux /| grep fio //检查是否有残留进程，必要时用 kill
命令终止，然后再对进程同步sync

<img
src="EdgePLC BL246说明书V1.1-images/image47.png"
style="width:5.76042in;height:0.34306in" />

9.  重复B~F操作，没有问题说明USB端口正常。

<img
src="EdgePLC BL246说明书V1.1-images/image48.png"
style="width:5.76389in;height:0.65972in" />

## 2.8 HDMI接口

<img
src="EdgePLC BL246说明书V1.1-images/image49.png"
style="width:1.18611in;height:3.03611in" alt="EdgePLC A款 (1)" />

HDMI接口如图所示。支持HDMI 1.4和HDMI
2.0标准。系统默认支持的分辨率为1920x1080@60fps，最高支持HDMI显示分辨率为
4K。

将HDMI连接设备和显示器，此时显示器应显示系统桌面的图标。若没有显示可尝试重启设备。

## 2.9 调试串口

<img
src="EdgePLC BL246说明书V1.1-images/image50.png"
style="width:3.82361in;height:1.42708in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

调试接口如图。可通过该端口进入设备系统。

## 2.10 SIM卡插槽

<img
src="EdgePLC BL246说明书V1.1-images/image51.png"
style="width:3.44583in;height:1.28681in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

SIM卡槽如图所示。

## 2.11 SD卡插槽

<img
src="EdgePLC BL246说明书V1.1-images/image52.png"
style="width:3.41458in;height:1.27431in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

SD卡槽如图所示，带EMMC版本的核心板不支持使用SD卡。只有不带EMMC版本的核心板可以使用SD卡作为系统启动卡。

1.  接入SD卡，属于系统启动卡，工作状态下，输入

fdisk -l

<img
src="EdgePLC BL246说明书V1.1-images/image53.png"
style="width:5.76319in;height:0.40903in" />

2.  系统识别到存储介质包含两个有效分区，后续读写性能测试将限定在系统的临时文件夹（/tmp）路径下进行”，并且可直观读取到该存储设备的实际物理容量。

3.  进入临时目录

cd /tmp

4.  然后输入以下指令测试写入：

fio --filename=/tmp/testfile --ioengine=psync --rw=write --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=write_job
--ramp_time=1 --direct=1

5.  可以看到工作状态下的（负载）写入的速度。

    <img
    src="EdgePLC BL246说明书V1.1-images/image54.png"
    style="width:5.76389in;height:0.69583in" />

6.  读取前需清除写入带来的缓存。

sync; echo 3 /| sudo tee /proc/sys/vm/drop_caches

7.  再输入以下指令测试读取：

fio --filename=/tmp/testfile --ioengine=psync --rw=read --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=read_job
--ramp_time=1 --direct=1

8.  可以看到工作状态下读取的速度。

    <img
    src="EdgePLC BL246说明书V1.1-images/image55.png"
    style="width:5.76458in;height:0.68264in" />

    A~F步骤都正常说明这个SD卡接口没有问题。

9.  测试完同步数据，重新测试需要清除缓存和同步以及查看是否有文件夹并且删除。

sync; echo 3 /| sudo tee /proc/sys/vm/drop_caches

ls

rm /tmp/testfile

<img
src="EdgePLC BL246说明书V1.1-images/image56.png"
style="width:5.76806in;height:1.30556in" />

## 2.12 重启按钮

<img
src="EdgePLC BL246说明书V1.1-images/image57.png"
style="width:3.48681in;height:1.30139in"
alt="c8c1b31cf4c96155d490e919f7fb7263_compress" />

重启按钮如图所示。长按大概5s后设备掉电关机，再短按一下后设备重启。

注意：如需自定义RST按钮，请于下单前联系业务人员，默认配置为硬件复位。

## 2.13 PCIE接口

PCIE接口支持4G和Wi-Fi功能。

### 2.13.1 4G模块

此处使用移远EC200模块为例（AT命令端口为/dev/ttyUSB1），测试程序位于/usr/demo/4G目录下。插入电话卡，连接好天线。

（1）网络功能

ls /dev //看有没有ttyUSB开头的设备，没有就是没识别到模块

<img
src="EdgePLC BL246说明书V1.1-images/image58.png"
style="width:5.76806in;height:2.02361in" />

将其他网络关闭，仅保留4G模块网络(ETH4(自带Wi-Fi模块的核心板ETH2))。

ifconfig eth1 down

ifconfig eth4 down

ifconfig eth3 down

ifconfig

此时应有网络节点eth2生成IP。若无该节点IP，可能是模块未默认使能网络功能，可尝试执行如下命令配置4G模块。（EC200系列模块AT命令端口为/dev/ttyUSB1）

安装 minicom

sudo apt-get update

sudo apt-get install minicom

启动 minicom 软件，并强制它连接名为 /dev/ttyUSB1 的串口设备

minicom -D /dev/ttyUSB1 //使用EC25模块时，设备节点为/dev/ttyUSB2

输入AT指令

AT+QCFG="USBNET",1 //echo -e "AT+QCFG=//USBNET//,1/r" /| sudo tee
/dev/ttyUSB1

使用EC200模块，还需增加一条命令才可联网：

AT+QNETDEVCTL=3,1,1 //echo -e "AT+QNETDEVCTL=3,1,1/r" /| sudo tee
/dev/ttyUSB1

<img
src="EdgePLC BL246说明书V1.1-images/image59.png"
style="width:5.76597in;height:1.49028in" />

查看IP有没有多余的以太网节点，一般是ETH4(自带Wi-Fi模块的核心板ETH2)。

<img
src="EdgePLC BL246说明书V1.1-images/image60.png"
style="width:5.76042in;height:0.93333in" />

然后通过ping www.baidu.com /8.8.8.8-I eth2 测试上网。

<img
src="EdgePLC BL246说明书V1.1-images/image61.png"
style="width:5.76597in;height:0.99583in" />

如果无法ping通，有可能是DNS设置问题，按如下指令添加DNS地址：

sudo nano /etc/resolv.conf

文件中添加nameserver 8.8.8.8

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

### 2.13.2 Wi-Fi模块

树莓派核心板自带Wi-Fi模块。连接好天线，即可连接Wi-Fi网络。

带HDMI接口的版本可直接在桌面图标上连接Wi-Fi。

连接Wi-Fi网络默认使用核心板板载天线，如果使用外部天线需要在/boot/firmware/config.txt
中添加。

sudo nano /boot/firmware/config.txt //打开文件，可先跳过执行连接Wi-Fi

dtparam=ant1 //选择使用板载天线

dtparam=ant2 //选择使用外部天线

sudo reboot //重启设备

设置无线网络的国家代码。

sudo raspi-config nonint do_wifi_country /<country/>

（1）STA功能

连接Wi-Fi网络。

sudo ifconfig eth1 down

sudo ifconfig eth2 down

sudo ifconfig eth3 down //关闭其他网络

sudo nmcli radio wifi on //启用Wi-Fi

sudo nmcli dev wifi list //查看可用的Wi-Fi网络

<img
src="EdgePLC BL246说明书V1.1-images/image62.png"
style="width:5.76389in;height:2.00972in" />

sudo nmcli dev wifi connect /<SSID/> password /<password/>

//将/<SSID/>替换为你的Wi-Fi名称，/<password/>替换为你的Wi-Fi密码

<img
src="EdgePLC BL246说明书V1.1-images/image63.png"
style="width:5.76597in;height:0.43403in" />

sudo nmcli dev wifi connect /<SSID/> hidden yes

//连接到隐藏的网络

sudo nmcli connection modify /<SSID/> connection.autoconnect yes

//设置自动连接

sudo systemctl restart NetworkManager //重启 NetworkManager 服务

nmcli device status //等待几秒钟，然后查看状态

<img
src="EdgePLC BL246说明书V1.1-images/image64.png"
style="width:5.76597in;height:0.55139in" />

可通过ifconfig查看获取到的IP地址，执行如下命令测试网络功能是否正常。

ping [www.baidu.com](http://www.baidu.com) -I wlan0

或者用图形界面连接，输入sudo nmtui指令进入界面，选择Activate a
connect进入Wi-Fi选择界面，选中Wi-Fi输入密码即可连接。

<img
src="EdgePLC BL246说明书V1.1-images/image65.png"
style="width:5.76597in;height:1.65069in" />

<img
src="EdgePLC BL246说明书V1.1-images/image66.png"
style="width:5.76597in;height:2.42847in" />

执行如下命令测试网络功能是否正常。

ping [www.baidu.com](http://www.baidu.com) -I wlan0

<img
src="EdgePLC BL246说明书V1.1-images/image67.png"
style="width:5.76319in;height:0.98889in" />

（2）AP功能（暂时只支持核心板自带的WI-FI模块）

使用以下指令快速创建热点

sudo nmcli device wifi hotspot ssid hotspot password 88888888

//ssid后为热点名称，password后为热点密码

也可以创建独立的热点连接配置。

断开网卡进行重置:

sudo nmcli device disconnect wlan0

sudo nmcli connection delete my-hotspot //删除旧的错误配置

sudo nmcli connection add type wifi ifname wlan0 con-name my-hotspot
autoconnect yes ssid "Myhotspot" /wifi.mode ap /ipv4.method shared
/wifi-sec.key-mgmt wpa-psk /wifi-sec.psk "88888888"

//创建热点连接配置（con-name后面是配置连接名，ssid后面是Wi-Fi名）

//配置热点安全参数，88888888是Wi-Fi密码

//配置IP和网络共享

sudo nmcli connection up my-hotspot

//启动网络

用你的电脑或者手机就可以搜索到你的Wi-Fi热点了。

<img
src="EdgePLC BL246说明书V1.1-images/image68.png"
style="width:5.76458in;height:0.45764in" />

也可以使用图形用户界面来设置热点配置

输入sudo nmtui指令进入图形界面，选择Edit a
connection,再选择Add进入创建网络界面。

<img
src="EdgePLC BL246说明书V1.1-images/image69.png"
style="width:2.72361in;height:2.66458in" /><img
src="EdgePLC BL246说明书V1.1-images/image70.png"
style="width:2.58819in;height:2.76458in" />

选择Wi-Fi进入网络配置设置界面，在Mode处选择Access
Point即是热点模式，按需求设置相关配置，OK保存后使用启动指令nmcli
connection up 设置的连接名（Profile name） 即可开启热点。

<img
src="EdgePLC BL246说明书V1.1-images/image71.png"
style="width:5.76458in;height:2.55556in" />

<img
src="EdgePLC BL246说明书V1.1-images/image72.png"
style="width:5.76667in;height:2.46806in" />

使用以下指令禁用热点

sudo nmcli device disconnect wlan0 //禁用热点

sudo nmcli device up wlan0 //重新连接Wi-Fi

## 2.14 M.2接口

### 2.14.1 SSD卡

1.  M.2接口插入固态硬盘，查看是否能检测出固态硬盘，输入以下指令，在返回列表中，查找名为
    nvme0n1 的设备及其容量大小。

lsblk -l

<img
src="EdgePLC BL246说明书V1.1-images/image73.png"
style="width:5.76667in;height:0.67708in" />

2.  测试前需要保证固态硬盘不是已经挂载的状态，为保证固态硬盘没有被挂载，所以执行卸载指令：

umount /run/media/nvme0n1 //已卸载则跳过

3.  写入测试数据：

fio -filename=/dev/nvme0n1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=write -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

<img
src="EdgePLC BL246说明书V1.1-images/image74.png"
style="width:5.76667in;height:0.75694in" />

4.  观察输出结果中的 WRITE 行，查看带宽（bw）数值，通常 NVMe
    固态硬盘写入速度应在 数百 MB/s
    以上（具体取决于硬盘性能）。若无报错且有速度数据输出，说明写入功能正常。

5.  读取测试：

fio -filename=/dev/nvme0n1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=read -bs=1024K
-size=5G -numjobs=1 -thread -group_reporting -name=read_job -ramp_time=1

<img
src="EdgePLC BL246说明书V1.1-images/image75.png"
style="width:5.76111in;height:0.825in" />

6.  观察输出结果中的 READ
    行，查看带宽（bw）数值。若无报错且有速度数据输出，说明读取功能正常。则硬盘本身功能正常。

### 2.14.2 Hailo算力模块

本设备支持通过 M.2 接口扩展 Hailo 算力模块，以提供高性能、低功耗的边缘
AI 推理能力。以下是Hailo-8L模块的驱动配置及状态检测规范。

设备出厂系统集成基础驱动支持，首次使用或需更新时，请按以下流程操作：

系统更新：连接网络后，在终端执行以下命令更新软件源及固件：

apt update

rpi-eeprom-update

rpi-eeprom-update -a

安装 AI 运行环境：执行以下命令安装 Hailo 专用驱动套件：

apt install hailo-all

重启生效：安装完成后，必须重启设备以加载 PCIe 硬件驱动：

reboot //安装完成后重启设备

在终端执行以下指令查询连接的设备信息：

hailortcli fw-control identify

<img
src="EdgePLC BL246说明书V1.1-images/image76.png"
style="width:5.76319in;height:1.49375in" />

也可执行以下命令查看系统内核日志，确认是否存在硬件通信记录

dmesg /| grep -i hailo

<img
src="EdgePLC BL246说明书V1.1-images/image77.png"
style="width:5.76597in;height:2.86458in" />

## 2.15 硬件看门狗

硬件看门狗默认超时时间为30ms，如需关闭硬件看门狗：

root@BL246:~#gpio write 22 1

如果硬件看门狗模组未正常启动，需要到/lib/modules/6.6.78-v8-16k/kernel/drivers/目录下重新加载w_dog.ko模块：

root@BL246:~#sudo insmod /lib/modules/6.6.78-v8-16k/kernel/drivers/w_dog/w_dog.ko.xz

## 2.16 外部RTC

本设备含一个外部RTC时钟。

查看外部 RTC 设备节点：

root@BL246:~# ls /dev/rtc/*

/dev/rtc /dev/rtc0

root@BL246:~# dmesg /| grep rtc0

/[ 4.319167/] rtc-isl1208 5-006f: rtc core: registered rtc-isl1208 as
rtc0

查看系统时钟：

root@BL246:~# date

Thu 23 Apr 10:28:42 BST 2026

设置RTC时间：

root@BL246:~# sudo hwclock --set --date="2026-4-23 17:30:00"

root@BL246:~# sudo hwclock -r

同步RTC时钟至系统时钟：

root@BL246:~# sudo hwclock -s

同步系统时钟到 RTC 的时钟：

root@BL246:~# sudo hwclock -w

再次查看时间

root@BL246:~# date

Thu 23 Apr 17:31:56 BST 2026

## 2.17 加密芯片

加密芯片型号为RJGT102。基于SHA-256的加密认证算法,
同时提供可配置的看门狗定时器和对外复位功能，与MCU通过 I²C-5
串行接口通信，芯片

支持低功耗模式。

设备内使用加密芯片的demo，是通过将/proc/sys/kernel/random/uuid写入加密芯片，同时保留uuid至/usr/rjgt_unique.json，使用时取出加密芯片数据进行对比,外部数据与加密芯片内部数据相同，则通过加密验证。

使用请自行修改Makefile文件中交叉编译器路径，再make编译；或参考《RJGT102数据手册》。

运行示例程序rigt102，若uuid正确，则会出现如下回复。

root@BL246:~#usr/demo/rjgt# ./rigt102

open unique file failed, create unique file!

random uuid would write rjgt102 : b6275e22-4928-4828-88fb-54a6fd8!

Contrast success

root@BL246:~#usr/demo/rjgt#./rigt102

Contrast success

# 3.设备登录

## 3.1 USB登录

进入此电脑——管理——设备管理器，打开端口，插入USB线到micro
USB，此时刷新的端口即为连接设备的端口。

<img
src="EdgePLC BL246说明书V1.1-images/image78.png"
style="width:3.62222in;height:2.76319in" />

此处以SecureCRT为例，在软件中新建连接，选择串口登录，选择对应的端口，波特率115200，数据位8，校验位None，停止位1。点击connect即可进入设备。

**Linux系统默认无登录密码**

**Ubuntu系统默认登录账号：bliiot 密码：bliiot**

<img
src="EdgePLC BL246说明书V1.1-images/image79.png"
style="width:2.10625in;height:1.92083in" />

您可以通过以下命令行更改当前用户账户的密码：

root@BL460:~#sudo raspi-config

要添加新用户，请输入以下命令：

root@BL460:~#sudo adduser /<username/>

要删除用户，请运行以下命令：

root@BL460:~#sudo deluser -remove-home /<username/>

要创建root用户，请运行以下命令：

root@BL460:~#sudo su //切换到 root 用户

root@BL460:~#sudo passwd root //设置 root 密码

root@BL460:~#sudo passwd -u root //启用root用户

## 3.2 SSH2登录

在使用网口登录前需设置对应网口的IP。此处以ETH2为例。此处ETH2已连接路由器，获取到的IP为192.168.2.107。电脑IP在2网段。

<img
src="EdgePLC BL246说明书V1.1-images/image80.png"
style="width:4.06875in;height:2.46944in" />

点击创建连接，选择协议为SSH2，主机名填写为设备IP：192.168.2.107，端口22，用户名root，点击Connect连接。

<img
src="EdgePLC BL246说明书V1.1-images/image81.png"
style="width:2.83958in;height:2.64653in" />

选择接受，即连接成功。

<img
src="EdgePLC BL246说明书V1.1-images/image82.png"
style="width:3.92778in;height:1.66389in" />

系统可能默认禁止root用户登录ssh，通过指令开启ssh.config文件，改写permitRootLogin对应的参数为yes。

sudo nano /etc/ssh/sshd_config

PermitRootLogin yes

<img
src="EdgePLC BL246说明书V1.1-images/image83.png"
style="width:5.76319in;height:0.30764in" />

<img
src="EdgePLC BL246说明书V1.1-images/image84.png"
style="width:5.76042in;height:0.58333in" />

重启服务即可

sudo systemctl restart ssh

# 4.系统烧录

## 4.1 Micro SD卡启动

### 4.1.1 启动卡制作

将空白Micro SD卡连接至电脑，下载并打开烧录工具Raspberry Pi Imager。<img
src="EdgePLC BL246说明书V1.1-images/image85.png"
style="width:4.90556in;height:3.43958in" alt="IMG_256" />

1：选择要烧写的硬件，CM5选择PI5。/
2：选择镜像，多个版本选择适合自己的（下面也可以选择格式化或者选择自己的备份的系统）。/
3：选择要烧录的盘符，只支持移动盘符（USB扩展的盘符），选我们的SD卡。/
4：全部选择好就可以点击NEXT，如果选择是树莓派OS，那么会出现下图，如果不需要个性化设置点“不”，如果之前保存过配置可以直接点“是”，第一次使用时，若需要设置请点“编辑设置”。<img
src="EdgePLC BL246说明书V1.1-images/image86.png"
style="width:4.91111in;height:3.43333in" alt="IMG_256" />

5:使用全新的系统默认不配置用户名和密码，用户可以直接在配置界面配置用户名和密码，如果不配置则需要再开机后连接键盘鼠标配置用户名和密码。

### 4.1.2从启动卡启动

烧录完毕后取出MICRO SD卡。将MICRO SD 接入底板MICRO SD
卡卡槽，连接CM5核心，上电即可。

注：烧录完第一次启动系统，可能会重启两次，属正常现象。

## 4.2 EMMC启动

### 4.2.1进入烧录模式

1.  先拆除外壳上下两面的四个螺丝，打开上盖，再拔出上侧边盖。移除Y板和X板（若有）。拆X/Y板时，先拔插针部分，把侧边盖往外稍微拨一下可拔出Y1板。

2.  将拨码开关的1和4向ON的方向拨，2和3向相反的方向拨，将跳线帽跳至如图所示位置。

    <img
    src="EdgePLC BL246说明书V1.1-images/image87.png"
    style="width:1.95486in;height:1.94792in" alt="000003" /> <img
    src="EdgePLC BL246说明书V1.1-images/image88.png"
    style="width:1.89306in;height:1.92222in" alt="000005" />

3.  将USB_OTG端口的拨码开关(序号5)向上拨码。

    <img
    src="EdgePLC BL246说明书V1.1-images/image89.emf"
    style="width:5.76042in;height:3.03125in" />

4.  使用底板上方的Type C 接口进行烧录连接。

    <img
    src="EdgePLC BL246说明书V1.1-images/image90.png"
    style="width:2.92847in;height:1.67639in" alt="IMG_256" />

### 4.2.2识别核心板EMMC为移动硬盘

下载并以管理员权限打开软件rpiboot。关闭杀毒软件以安装驱动程序和启动工具。安装成功之后在安装目录下有一个rpiboot.exe。

<img
src="EdgePLC BL246说明书V1.1-images/image91.png"
style="width:5.0625in;height:2.1875in" alt="IMG_256" />

1.通过Type C 接口（SLAVE 接口） 转USB接口连接电脑。

2.此时连接电脑并且给主板供电，电脑设备管理器中会识别出一个BCMxxx的设备（CM5是BCM2712，CM4是BCM2711）如果驱动没有安装成功，设备是在其他设备中。

<img
src="EdgePLC BL246说明书V1.1-images/image92.png"
style="width:1.96875in;height:0.47917in" alt="IMG_256" />

然后运行rpiboot(请勿使用管理员权限运行)，选择对应的可执行程序或者脚本。

<img
src="EdgePLC BL246说明书V1.1-images/image93.png"
style="width:3.70833in;height:0.52083in" alt="IMG_256" />

例如连接的是CM5。

<img
src="EdgePLC BL246说明书V1.1-images/image94.png"
style="width:5.19097in;height:2.50486in" alt="IMG_256" />3.等待运行结束，在我的电脑上面会出现一个新的盘符mmcblk0。

<img
src="EdgePLC BL246说明书V1.1-images/image95.png"
style="width:2.11458in;height:0.65625in" />

### 4.2.3系统烧录

<img
src="EdgePLC BL246说明书V1.1-images/image85.png"
style="width:4.72569in;height:3.31319in" alt="IMG_256" />1：打开Raspberry
Pi Imager，选择要烧写的硬件（前面步骤下载的），CM5选择PI5。

2：选择镜像，多个版本选择适合自己的（下面也可以选择格式化或者选择自己的备份的系统）。/
3：选择要烧录的盘符，即4.2.1生成的移动盘符（USB扩展的盘符）。/
4：全部选择好就可以点击NEXT，如果选择是树莓派OS，那么会出现个性化配置界面，如果不需要点“不”，如果之前配置保存过可以直接点“是”，第一次使用需要设置点“编辑设置”。

<img
src="EdgePLC BL246说明书V1.1-images/image86.png"
style="width:4.64653in;height:3.24861in" alt="IMG_256" />

5：烧录完毕断开电源，断开和电脑的连接线。

6：将拨码开关的2和3向ON的方向拨，1和4向相反的方向拨，再将跳线帽跳至如图所示位置。

<img
src="EdgePLC BL246说明书V1.1-images/image96.png"
style="width:2.63542in;height:2.11528in" alt="000003" /> <img
src="EdgePLC BL246说明书V1.1-images/image97.png"
style="width:2.19514in;height:2.14236in" alt="000004" />

7：将USB_OTG端口的拨码开关（序号5）向下拨码短接到地。

<img
src="EdgePLC BL246说明书V1.1-images/image98.emf"
style="width:3in;height:2.90625in" />

8：装回外壳，给设备上电即可。

注：烧录完第一次启动系统，可能会重启两次，属正常现象。

# 5.导轨安装

配备导轨卡扣分为下段式短款导轨结构。此设计预留了充足的螺丝锁付空间，便于用户进行安装操作。

<img
src="EdgePLC BL246说明书V1.1-images/image99.png"
style="width:1.42569in;height:2.77153in"
alt="8aec9eb215acbbce3b8954b2e1062111_compress" /><img
src="EdgePLC BL246说明书V1.1-images/image100.png"
style="width:1.41389in;height:2.76042in"
alt="8aec9eb215acbbce3b8954b2e1062111_compress" />

将卡扣垂直向下按压，直至其完全嵌入并锁定于导轨底部，即可完成安装。长导轨卡无需额外卡扣，因其内部已预设专用凹槽结构，可直接实现稳固连接。

<img
src="EdgePLC BL246说明书V1.1-images/image101.png"
style="width:0.83611in;height:1.94236in"
alt="ac31d771be6b72005cba9ec2e46da2bc_compress" />

# 6.软件支持

- OpenPLC

  详细使用方法请参考《OpenPLC使用说明书》

- Node-Red

  详细使用方法请参考《Node-Red使用说明书》

<!-- -->

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