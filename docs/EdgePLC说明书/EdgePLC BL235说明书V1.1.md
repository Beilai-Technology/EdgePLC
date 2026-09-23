

![EdgePLC A款 (2)](EdgePLC BL235说明书V1.1-images/image2.jpeg)

版本：V1.1

日期：2026-09-10

版权：**深圳市钡铼技术有限公司

**网址：[www.bliiot.cn](http://www.bliiot.cn)

EdgePLC BL235系列说明书

EdgePLC BL235工业边缘控制器


![EdgePLC A款 (2)](EdgePLC BL235说明书V1.1-images/image2.jpeg)


**前言**

感谢您使用深圳市钡铼技术有限公司的BL235系列，阅读本产品说明书能让您快速掌握本产品的功能和使用方法。

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

在工业自动化向“边缘计算+实时控制”深度融合的转型背景下，传统PLC面临智能计算的瓶颈，而通用工业计算机又难以满足高实时性控制的需求。EdgePLC
BL235系列工业边缘控制器应运而生，旨在打破IT与OT的融合壁垒，提供真正意义上的“边缘控算一体”解决方案。

BL235系列采用“高性能ARM处理器 + 分布式I/O扩展”的架构，以TI Sitara 系列
AM62x 处理器为核心，提供单核、双核或四核 ARM Cortex-A53和单核 ARM
Cortex-M4F的多核架构，在保障毫秒级实时控制的同时，具备强大的本地数据处理能力。

EdgePLC
BL235工业边缘控制器深度融合实时控制、边缘智能、协议转换、远程运维与二次开发等功能，支持IEC
61131-3标准编程环境（OpenPLC/NexPLC/CODESYS）、IGH
EtherCAT硬实时主站，并可扩展多达32块N系列分布式I/O模块，覆盖DI/DO/AI/AO/温度采集等多种信号类型。软件层面基于Ubuntu
20.04系统，集成Docker、Node-RED、Python/C++开发环境，实现从数据采集、实时分析到智能决策的全流程闭环。

BL235系列工业边缘控制器专为智能产线控制、储能EMS、光伏逆变器管理等“控制+计算”协同场景设计，通过将智能分析下沉至设备边缘，它不仅实现了控制逻辑的精准执行，更完成了数据价值的就地转化与智能决策，助力企业构建更敏捷、更智能、更高效的下一代工业控制系统，从容应对智能制造的未来挑战。

## 1.2 外形尺寸

产品外观结构与尺寸如下图：

![F:/2025_9/EdgePLC/标签外壳/标准款清晰图片.png标准款清晰图片](EdgePLC BL235说明书V1.1-images/image4.png)![F:/2025_9/EdgePLC/标签外壳/A款清晰图片.pngA款清晰图片](EdgePLC BL235说明书V1.1-images/image5.png)

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
<td>TI Sitara AM6232/AM6254，16nm</td>
</tr>
<tr>
<td style="text-align: center;">处理器频率</td>
<td><p>1/2/4x ARM Cortex-A53(64bit)，主频 1.4GHz。</p>
<p>1x Cortex-M4F，专用实时处理单元，主频 400MHz。</p>
<p>1x Cortex-R5F，主频 400MHz 备注：Cortex-R5F
主要负责系统启动、资源管理和电源管理功能。</p>
<p>1x PRU-ICSS，2 个 32 位可编程实时单元（PRU0 和 PRU1），主频 333MHz
备注：PRU-ICSS 支持 GPIO、UART、I2C
拓展，不支持工业通讯协议和网口拓展。</p></td>
</tr>
<tr>
<td style="text-align: center;">GPU</td>
<td>3D GPU：图形加速器，支持 OpenGL 3.x/2.0/1.1、Vulkan 1.2(AM6254
Only)</td>
</tr>
<tr>
<td style="text-align: center;">内存</td>
<td>512MB/1/2GByte DDR3</td>
</tr>
<tr>
<td style="text-align: center;">存储</td>
<td>8/16G NAND FLASH</td>
</tr>
<tr>
<td rowspan="3" style="text-align: center;">电源</td>
<td style="text-align: center;">输入电压</td>
<td>DC 12～24V （输入：24V,输出：12V）</td>
</tr>
<tr>
<td style="text-align: center;">功耗</td>
<td><p>正常：240mA@12V（带4G模块），220mA@12V（不带4G模块）</p>
<p>最大：700mA@12V</p></td>
</tr>
<tr>
<td style="text-align: center;">反接防护</td>
<td>支持</td>
</tr>
<tr>
<td rowspan="2" style="text-align: center;">网口</td>
<td style="text-align: center;">网口规格</td>
<td>2~3*RJ45，3x100M，自适应MDI/MDIX。</td>
</tr>
<tr>
<td style="text-align: center;">网口保护</td>
<td>ESD ±2kV（接触），±8kV（空气）；</td>
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
<td>1*micro USB，2*USB 2.0 HOST</td>
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
<td>LED*3</td>
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
<td><p>Yocto 3.1(dunfell)(Linux-5.10.168、Linux-RT-5.10.168)</p>
<p>Yocto 4.0(kirkstone)(Linux-6.1.80、Linux-RT-6.1.80)</p>
<p>Debian 12</p></td>
</tr>
</tbody>
</table>

## 1.4 设备选型

### 1.4.1 主型号选型

|          |         |         |          |             |             |
|:--------:|:-------:|:-------:|:--------:|:-----------:|:-----------:|
| **型号** | **ETH** | **USB** | **HDMI** | **N板IO槽** |  **尺寸**   |
|  BL235   | 2x100M  |    2    |    0     |      1      | 38x92x110mm |
|  BL235A  | 3x100M  |    2    |    1     |      1      | 38x92x110mm |

**BL235系列选型**

### 1.4.2 SOM选型表

可以根据需求，选择合适的ROM、RAM以及温度等级。

**BL235系列SOM选型表**

|          |         |          |               |          |          |                |
|:---------|:--------|:---------|:--------------|:---------|:---------|:---------------|
| **型号** | **MCU** | **主频** | **内核**      | **eMMC** | **DDR4** | **温度级别**   |
| SOM350   | AM6232  | 1.4GHz   | 2 x A53 + M4F | 4GByte   | 512MB    | 工业级 -40~85℃ |
| SOM351   | AM6232  | 1.4GHz   | 2 x A53 + M4F | 8GByte   | 1GByte   | 工业级 -40~85℃ |
| SOM352   | AM6254  | 1.4GHz   | 4 x A53 + M4F | 8GByte   | 1GByte   | 工业级 -40~85℃ |
| SOM353   | AM6254  | 1.4GHz   | 4 x A53 + M4F | 8GByte   | 2GByte   | 工业级 -40~85℃ |

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

![EdgePLC A款 (10)](EdgePLC BL235说明书V1.1-images/image6.png)![](EdgePLC BL235说明书V1.1-images/image7.png)

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

![e2c8802fdadeb1e5530381aefa943291_origin(1)](EdgePLC BL235说明书V1.1-images/image8.png)。

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
<td style="text-align: center;">ttyS4-A</td>
<td style="text-align: center;">ttyS4-B</td>
<td style="text-align: center;">GND</td>
<td style="text-align: center;">ttyS7-A</td>
<td style="text-align: center;">ttyS7-B</td>
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
<td style="text-align: center;">ttyS7-A</td>
<td style="text-align: center;">ttyS7-B</td>
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

使用RS485串口时，将RS485线接至端口上（ttl转485），打开sscom5和mobaxterm对接收发，如RS485-1端口（x90模块），其设备文件为/dev/ttyS4；设置其波特率设为
115200，8N1，无校验位。

stty -F /dev/ttyS4 ispeed 115200 ospeed 115200 cs8

echo 12345 /> /dev/ttyS4 //通过RS485-1端口发送数据

cat /dev/ttyS4 //等待查看接收到的数据

串口助手收到数据

![](EdgePLC BL235说明书V1.1-images/image9.png)

串口助手发送数据

![](EdgePLC BL235说明书V1.1-images/image10.png)

终端界面收到数据

![](EdgePLC BL235说明书V1.1-images/image11.png)

按“Ctrl+C”停止。

然后更换x90另外一个ttyS7口继续测试。

### 2.3.11 CAN使用

在进行 CAN
通信测试前，需先关闭目标接口，配置目标比特率，随后重新启动接口。以配置
CAN0 总线比特率为 1Mbps 为例，请在终端依次执行以下命令：

root@bliiot:~# ifconfig can0 down

root@bliiot:~# ip link set can0 type can bitrate 1000000

root@bliiot:~# ifconfig can0 up

![](EdgePLC BL235说明书V1.1-images/image13.png)

接口启动后，可使用 cansend 工具向 CAN 总线发送测试数据帧。以下命令将发送
ID 为 123、数据长度为 8 字节的标准帧：

root@bliiot:~# cansend can0 123#1122334455667788

![](EdgePLC BL235说明书V1.1-images/image14.png)

Cangaroo工具收到数据

![](EdgePLC BL235说明书V1.1-images/image15.png)

使用 candump 工具可实时监听并显示 CAN 总线上的接收数据。

root@bliiot:~# candump can0

![](EdgePLC BL235说明书V1.1-images/image16.png)

若CAN0接收正常，用其它设备发送该数据则应收到

root@bliiot:~# candump can0

can0 123 /[8/] 11 22 33 44 55 66 77 88

![](EdgePLC BL235说明书V1.1-images/image17.png)

### 2.3.12 N板端口使用

1)  **软件安装**

对应文件位置位于**/ion**文件夹下。实际目录请以文件为准。

插上网线写入ifconfig指令获取IP，通过SSH登录

![](EdgePLC BL235说明书V1.1-images/image18.png)

![](EdgePLC BL235说明书V1.1-images/image19.png)

通过左边文件夹页面在usr/demo/文件夹下，新建ion文件夹，把N板识别文件复制进去

![](EdgePLC BL235说明书V1.1-images/image20.png)

对BEILAI_N_PLC_235_V1.0_20260824.bin执行chmod +x
BEILAI_N_PLC_235_V1.0_20260824.bin。然后安装软件。

root@bliiot:/# cd /usr/demo/ion

root@bliiot:/# chmod +x BEILAI_N_PLC_235_V1.5_20260824.bin

root@bliiot:/# ./BEILAI_N_PLC_235_V1.5_20260824.bin

Md5 verify pass!

Created symlink
/etc/systemd/system/multi-user.target.wants/iolib.service →
/etc/systemd/system/iolib.service.

Install complete!

2)  **端口使用**

<!-- -->

1.  **DO使用**

这里以N2161为准（16路DO模块pnp），ion show查看IO板信息。ion
help查看命令帮助。

root@bliiot:/# ion help

输入ion show查看信息。

![](EdgePLC BL235说明书V1.1-images/image21.png)

![](EdgePLC BL235说明书V1.1-images/image22.png)

也可通过get命令获取通道值：

root@bliiot:/# ion get 1014 //通过address查看

address 1014 value 0

![](EdgePLC BL235说明书V1.1-images/image23.png)

root@bliiot:/# ion set 1000 1 //通过address设置输出1

root@bliiot:/# ion get 1000 //通过address查看

![](EdgePLC BL235说明书V1.1-images/image24.png)

设置通道值有信号量会亮灯

对应的N2321、N2322、N2162、N2084类似。

2.  **DI使用**

以N1323为例（32路DI模块干接点），DI模块为例，输入ion
show查看信息。这边以17-32路端口单板为例。

![](EdgePLC BL235说明书V1.1-images/image25.png)

通过get命令获取通道值以及ion show查看信息

root@bliiot:/# ion get 2024 //通过address查看

address 2024 value 0

![](EdgePLC BL235说明书V1.1-images/image26.png)

将DI24（即为24通道）短接

![](EdgePLC BL235说明书V1.1-images/image28.png)

观察N板灯亮情况，对应DI短接形成回路灯亮。对应的N1163类似。

湿节点测试(带电干结点)：以N1161为例（NPN型）

1、外接电源：将外接电源的正负极接到电源两端，电源的正极接到模块的公共端（COM/0V），负极接到模块的
DI 输入端子。

2、灯亮，终端输入ion show查看已闭合。

PNP型则公共端接负极，输入端子接正极。

类似N1162、1321、1322对应其湿接点。

3.  **AO使用**

以N4081为例（8路输出模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

![](EdgePLC BL235说明书V1.1-images/image30.png)

也可通过get命令获取通道值：

root@bliiot:/# ion get 4000 //通过address查看

address 4000 value 4

![](EdgePLC BL235说明书V1.1-images/image32.png)

root@bliiot:/# ion set 4000 10 //通过address设置输出10mA

root@bliiot:/# ion get 4000 //通过address查看

![](EdgePLC BL235说明书V1.1-images/image34.png)

通过高精度万用表直流电流档查看实际值与设置值是否相符,若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

对应的N4086差分输出电压类似。

![](EdgePLC BL235说明书V1.1-images/image36.png)

4.  **AI使用**

以N3081为例（8路输入模块单端电流），量程设为0-20mA，输入ion
show查看信息。

root@bliiot:/# ion show

![](EdgePLC BL235说明书V1.1-images/image38.png)

使用信号发生器输出目标电流值，观察实际值是否与输入值保持一致，如对第一个通道输出20mA,通过ion
show查看数值，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

以第一通道为例，设定输出20mA，界面显示的数值即为该通道的实际输出值。

root@bliiot:/# ion show

![](EdgePLC BL235说明书V1.1-images/image39.png)

对应的N3083单端输入电压类似。

![](EdgePLC BL235说明书V1.1-images/image41.png)

5.  **RTD使用**

以N5041为例（4路RTD模块三线PT100），量程设为-200-850℃，输入ion
show查看信息。

root@bliiot:/# ion show

![](EdgePLC BL235说明书V1.1-images/image42.png)

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值（对应pt100/1000温度阻值对应表）的偏差在允许误差范围内，即视为校准通过。

对应的N5042、N5043、 N5044类似。

![](EdgePLC BL235说明书V1.1-images/image44.png)

![](EdgePLC BL235说明书V1.1-images/image45.png)

![](EdgePLC BL235说明书V1.1-images/image46.png)

6.  **NTC使用**

以N3087为例（8路NTC模块10K3A1），量程为184.8-667828，输入ion
show查看信息。

root@bliiot:/# ion show

使用电阻箱设置阻值对应温度值改变到合适的范围，若显示值与理论值的偏差在允许误差范围内，即视为校准通过。

![](EdgePLC BL235说明书V1.1-images/image48.png)

3)  **量程模式修改**

通过ion help命令，可以看到config的命令格式。

![](EdgePLC BL235说明书V1.1-images/image49.png)

在终端中执行以下命令，以获取设备当前的运行状态及模式设置指令：

root@bliiot:/# ion getmode

![](EdgePLC BL235说明书V1.1-images/image50.png)

确认目标模式对应的数值后，使用以下命令进行模式切换：例如将N4081的量程设置为4~20MA。

root@bliiot:/# ion setmode /<slot/> /<mode/>

root@bliiot:/# ion setmode 4 4

2.  

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

![EdgePLC A款 (1)](EdgePLC BL235说明书V1.1-images/image61.jpeg)

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

## 2.6 网络接口

![EdgePLC A款 (1)](EdgePLC BL235说明书V1.1-images/image62.png)

如图所示，设备配备了三个百兆网口ETH1、ETH2、ETH3

将网线插入ETH1，输入命令：

root@BL235:~# ifconfig -a

![](EdgePLC BL235说明书V1.1-images/image63.png)

此时ETH1应显示为设定的静态IP地址192.168.1.226。

更换网口测试时关闭其他网口：

关闭网口1：ifconfig eth1 down

关闭网口3：ifconfig eth3 down

或者手动获取到IP

root@BL235-bliiot:~# udhcpc -i eth1

![](EdgePLC BL235说明书V1.1-images/image65.png)

ping百度：ping 8.8.8.8 ，Ctrl+c结束

![](EdgePLC BL235说明书V1.1-images/image66.png)

此时LINK灯亮。

## 2.7 USB接口

![EdgePLC A款 (1)](EdgePLC BL235说明书V1.1-images/image68.png)

如图，设备带有2个USB2.0 HOST接口。支持FAT32格式U盘。

1.  接入测试用的U盘，这边run/media/sda为挂载文件夹，输入以下指令卸载并查看U盘是否可以检测：

lsblk（查看是否挂载） mkfs.vfat /dev/sda1(格式化分区更好测速)

umount /run/media/sda1（没有挂载就跳过）

lsblk

2.  可以看到sdb1，并且能够看到实际的内存大小

![](EdgePLC BL235说明书V1.1-images/image69.png)

3.  安装fio工具

apt update

apt install fio -y //有就跳过，出厂一般自带

4.  然后输入以下指令测试写入：（第一次写入可以调成size=2G）

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=write -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

5.  可以看到写入的速度。

![](EdgePLC BL235说明书V1.1-images/image71.png)

6.  再输入以下指令测试读取：

fio -filename=/dev/sda1 -ioengine=psync -iodepth=1 -iodepth_batch=1
-iodepth_low=1 -iodepth_batch_complete=1 -direct=1 -rw=read -bs=1024K
-size=1G -numjobs=1 -thread -group_reporting -name=write_job
-ramp_time=1

7.  可以看到读取的速度。

    ![](EdgePLC BL235说明书V1.1-images/image73.png)

8.  说明这个USB接口没有问题。

9.  更换下一个USB口，需要执行

ps aux /| grep fio //检查是否有残留进程，必要时用 kill+ID
命令终止，然后再对进程同步sync

![](EdgePLC BL235说明书V1.1-images/image75.png)

10. 重复B~F操作，没有问题说明USB端口正常。

![](EdgePLC BL235说明书V1.1-images/image76.png)

## 2.8 HDMI接口

![EdgePLC A款 (1)](EdgePLC BL235说明书V1.1-images/image78.png)

HDMI接口如图所示。支持HDMI 1.4和HDMI
2.0标准。系统默认支持的分辨率为1920x1080@60fps，最高支持HDMI显示分辨率为
4K。

将HDMI连接设备和显示器，此时显示器应显示企鹅图标。若没有显示可尝试重启设备。

## 2.9 调试串口

![c8c1b31cf4c96155d490e919f7fb7263_compress](EdgePLC BL235说明书V1.1-images/image80.png)

调试接口如图。可通过该端口进入设备系统。

## 82.10 SIM卡插槽

![c8c1b31cf4c96155d490e919f7fb7263_compress](EdgePLC BL235说明书V1.1-images/image81.png)

SIM卡槽如图所示。

## 2.11 SD卡插槽

![c8c1b31cf4c96155d490e919f7fb7263_compress](EdgePLC BL235说明书V1.1-images/image82.png)

SD卡槽如图所示，支持FAT32格式SD卡，以sd卡烧录为例。

1.  接入SD卡，属于系统启动卡，工作状态下，输入

fdisk -l

![](EdgePLC BL235说明书V1.1-images/image83.png)

2.  系统识别到存储介质包含两个有效大分区，后续读写性能测试将限定在SD卡路径下进行”，并且可直观读取到该存储设备的实际物理容量。

3.  可以通过指令查看k1p3分区能不能读写

blkid /dev/mmcblk1p3

![](EdgePLC BL235说明书V1.1-images/image85.png)

识别到为系统备份分区，可读写即可使用

4.  执行卸载指令

umount /dev/mmcblk1p3

5.  然后输入以下指令测试写入：

fio --filename=/dev/mmcblk1p3 --ioengine=psync --rw=write --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=write_job
--ramp_time=1 --direct=1

6.  可以看到工作状态下的（负载）写入的速度。

    ![](EdgePLC BL235说明书V1.1-images/image87.png)

7.  读取前需清除写入带来的缓存。

sync; echo 3 /| tee /proc/sys/vm/drop_caches

8.  再输入以下指令测试读取：

fio --filename=/dev/mmcblk1p3 --ioengine=psync --rw=read --bs=1024k
--size=1G --numjobs=1 --thread --group_reporting --name=read_job
--ramp_time=1 --direct=1

9.  可以看到工作状态下读取的速度。

    ![](EdgePLC BL235说明书V1.1-images/image89.png)

    A~F步骤都正常说明这个SD卡接口没有问题。

10. 测试完同步数据，重新测试需要清除缓存

sync; echo 3 /| tee /proc/sys/vm/drop_caches

## 2.12 重启按钮

![c8c1b31cf4c96155d490e919f7fb7263_compress](EdgePLC BL235说明书V1.1-images/image91.png)

重启按钮如图所示。按下松开后设备重启。

注意：如需自定义RST按钮，请于下单前联系业务人员，默认配置为硬件复位。

## 2.13 PCIE接口

PCIE接口支持4G和Wi-Fi功能。

### 2.13.1 4G模块

此处使用移远EC200模块为例（AT命令端口为/dev/ttyUSB1），测试程序位于/usr/demo/4G目录下。插入电话卡，连接好天线。

（1）网络功能

ls /dev 看有没有ttyUSB开头的设备，没有就是没识别到模块

![](EdgePLC BL235说明书V1.1-images/image92.png)

stty -F /dev/ttyUSB1 ispeed 115200 ospeed 115200 cs8 raw -echo
//设置串口

![](EdgePLC BL235说明书V1.1-images/image94.png)

查信号 20以上 ：

cat /dev/ttyUSB1 & echo -e "AT+CSQ/r" /> /dev/ttyUSB1（输入1/2遍）

![](EdgePLC BL235说明书V1.1-images/image96.png)

查是4G模块否能正常和SIM卡通讯：

echo -e "AT+CPIN?/r" /> /dev/ttyUSB1

![](EdgePLC BL235说明书V1.1-images/image98.png)

EC200还需加一条拨号指令

echo -e "AT+QNETDEVCTL=3,1,1/r" /> /dev/ttyUSB1

查是否连接运营商，

echo -e "AT+COPS?/r" /> /dev/ttyUSB1

![](EdgePLC BL235说明书V1.1-images/image100.png)

然后输入

udhcpc -i usb0

此时usb0应获取IP。

udhcpc: started, v1.30.1

udhcpc: sending discover

udhcpc: sending discover

udhcpc: sending select for 192.168.43.100

udhcpc: lease of 192.168.43.100 obtained, lease time 86400

![](EdgePLC BL235说明书V1.1-images/image102.png)

然后通过ping www.baidu.com /8.8.8.8-I usb0 测试上网。

Ping不通百度加以下指令

echo "nameserver 8.8.8.8" /> /etc/resolv.conf

![](EdgePLC BL235说明书V1.1-images/image104.png)

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

此处使用的Wi-Fi模块为BL-R8188EU2（2.4G频段）。测试程序及驱动位于/usr/demo/Wi-Fi路径下，连接好天线。若无wlan0网卡，可按下方步骤安装驱动。

（1）STA功能

先查看该版本系统是否已自动加载wlan0网口：

ifconfig

![](EdgePLC BL235说明书V1.1-images/image106.png)

进入测试程序目录下，关闭其他网络，仅保留Wi-Fi网络，加载Wi-Fi驱动。

cd /usr/demo/wifi/ /# 进入驱动目录

ifconfig eth1 down

ifconfig eth2 down

ifconfig eth3 down //关闭其他网络

连接Wi-Fi：

ifconfig wlan0 up /#打开wlan0

./wifi_setup.sh -i bliiot -p bebetter
/#连接Wi-Fi，-i后面接Wi-Fi名，-p后面接密码

![](EdgePLC BL235说明书V1.1-images/image108.png)

ifconfig /#查看wlan0有无IP

![](EdgePLC BL235说明书V1.1-images/image110.png)

最后ping百度测试：

ping -4 www.baidu.com （百度域名不一定成功转IP，使用百度IP）

![](EdgePLC BL235说明书V1.1-images/image112.png)

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

配置文件如果没有添加下列指令

interface=wlan0

driver=nl80211

ssid=rtl8188eu

channel=6

hw_mode=g

auth_algs=1

wpa=2

wpa_passphrase=88888888

wpa_key_mgmt=WPA-PSK

rsn_pairwise=CCMP

修改AP参数

nano ap_setup.sh

找到对应指令，输入指令修改

udhcpd -f -I 192.168.0.1 ./udhcpd.conf &

打开分配脚本

nano udhcpd.conf

没有则添加以下指令

start 192.168.0.100

end 192.168.0.200

interface wlan0

max_leases 10

option subnet 255.255.255.0

option router 192.168.0.1

option dns 8.8.8.8

然后在执行AP模式指令

./ap_setup.sh

![](EdgePLC BL235说明书V1.1-images/image114.png)

系统可能在启动时连接WiFi默认配置STA功能，需要在rc.local文件隐藏，通过reboot重启设备即可。

![](EdgePLC BL235说明书V1.1-images/image116.png)

重新测试通过ps查看进程号杀掉udhcpd和hostapd旧进程即可

ps

kill 1959 1960 2100 //对应两个程序进程号

![](EdgePLC BL235说明书V1.1-images/image117.png)

重新运行脚本

./ap_setup.sh

## 2.14 硬件看门狗

看门狗控制引脚：PE0，置1时关闭硬件看门狗。喂狗引脚：PG16。硬件看门狗超时时间为30ms。

## 2.15 外部RTC

本设备含一个外部RTC时钟。

查看外部 RTC 设备节点：

root@BL235-bliiot:~# ls /dev/rtc/*

/dev/rtc /dev/rtc0

root@BL235-bliiot:~# dmesg /| grep rtc0

/[ 4.319167/] rtc-isl1208 5-006f: rtc core: registered rtc-isl1208 as
rtc0

查看系统时钟：

root@BL235-bliiot:~# date

Thu 23 Apr 10:28:42 BST 2026

设置RTC时间：

root@BL235-bliiot:~# sudo hwclock --set --date="2026-4-23 17:30:00"

root@BL235-bliiot:~# sudo hwclock -r

同步RTC时钟至系统时钟：

root@BL235-bliiot:~# sudo hwclock -s

同步系统时钟到 RTC 的时钟：

root@BL235-bliiot:~# sudo hwclock -w

再次查看时间

root@BL235-bliiot:~# date

Thu 23 Apr 17:31:56 BST 2026

## 2.16 加密芯片

加密芯片型号为RJGT102。基于SHA-256的加密认证算法,
同时提供可配置的看门狗定时器和对外复位功能，与MCU通过 I²C-5
串行接口通信，芯片

支持低功耗模式。

设备内使用加密芯片的demo，是通过将/proc/sys/kernel/random/uuid写入加密芯片，同时保留uuid至/usr/rjgt_unique.json，使用时取出加密芯片数据进行对比,外部数据与加密芯片内部数据相同，则通过加密验证。

使用请自行修改Makefile文件中交叉编译器路径，再make编译；或参考《RJGT102数据手册》。

运行示例程序rigt102，若uuid正确，则会出现如下回复。

root@BL235:~#usr/demo/other# ./rjgt102

open unique file failed, create unique file!

random uuid would write rjgt102 : b6275e22-4928-4828-88fb-54a6fd8!

Contrast success

root@BL235:~#usr/demo/other#./rjgt102

Contrast success

# 3.设备登录

## 3.1 USB登录

进入此电脑——管理——设备管理器，打开端口，插入USB线到micro
USB，此时刷新的端口即为连接设备的端口。

![](EdgePLC BL235说明书V1.1-images/image118.png)

此处以SecureCRT为例，在软件中新建连接，选择串口登录，选择对应的端口，波特率115200，数据位8，校验位None，停止位1。点击connect即可进入设备。

**Linux系统默认无登录密码**

**Ubuntu系统默认登录账号：root 密码：root**

![](EdgePLC BL235说明书V1.1-images/image119.png)

## 3.2 SSH2登录

在使用网口登录前需设置对应网口的IP。此处以ETH2为例。此处ETH2已连接路由器，获取到的IP为192.168.2.107。电脑IP在2网段。

![](EdgePLC BL235说明书V1.1-images/image120.png)

点击创建连接，选择协议为SSH2，主机名填写为设备IP：192.168.2.107，端口22，用户名root，点击Connect连接。

![](EdgePLC BL235说明书V1.1-images/image121.png)

选择接受，即连接成功。

![](EdgePLC BL235说明书V1.1-images/image122.png)

# 4.系统烧录

## 4.1 Micro SD卡启动

修改系统启动方式，需要拆开设备的外壳，找到拨码开关。

![IMG_256](EdgePLC BL235说明书V1.1-images/image123.png)

### 4.1.1 启动卡制作

1)  挂载Micro SD卡

将 Micro SD 卡通过读卡器连接至 PC 机，Ubuntu 系统识别后，一般会自动挂载
Micro SD 卡分区，如下图所示。

![](EdgePLC BL235说明书V1.1-images/image124.png)

若 Ubuntu 系统未自动识别，请右击右下角的 USB
大容量存储设备图标，再点击"Connect (Disconnect from Host)"进行识别。

![](EdgePLC BL235说明书V1.1-images/image125.png)

若无以上图标或者连接不成功，请尝试如下方法：

1.  请将 Micro SD 卡通过读卡器插至 PC 机 USB2.0 接口，而不是 USB3.0
    接口，部分版本 VMware 可能不兼容 USB3.0。

2.  请将 Micro SD 卡插在 PC 机上，然后重启 Ubuntu，在 Ubuntu
    重启过程中请勿取出。Ubuntu 系统重启后，存储设备图标会重新出现。

<!-- -->

2)  Micro SD卡设备节点名确认执行如下命令，确认 Micro SD 卡在 Ubuntu
    系统的设备节点名。

fdisk -l

![](EdgePLC BL235说明书V1.1-images/image126.png)

可看到 Micro SD 卡设备节点是"/dev/sdb"，并且有三个分区，分别为
sdb1、sdb2 和sdb3
分区。设备节点名字是可变的，一般插拔多次或者使用不同的卡插拔后，可能会显示
sdc、sdd 等。

3)  PV工具安装

PV(Pipe
Viewer)是一种基于终端的工具，用于通过管道监测数据的进度。为了更直观地显示系统启动卡的制作进度，系统启动卡制作过程中会使用到
PV 工具。

请执行如下命令通过网络安装PV工具，如未安装PV工具将会导致系统启动卡制作失败。

sudo apt-get install pv

![](EdgePLC BL235说明书V1.1-images/image127.png)

4)  系统启动卡制作

如下为系统启动卡制作命令。命令中"/dev/sdb"为 Micro SD
卡设备节点，请确认命令中设备节点无误后，再执行命令。若错误输入其他存储介质设备节点，将会造成存储介质数据损坏。

sudo ./mksdboot.sh -d /dev/sdb

![](EdgePLC BL235说明书V1.1-images/image128.png)

根据提示按回车键，进行系统启动卡制作。

![](EdgePLC BL235说明书V1.1-images/image129.png)

耗时约
10~15min，系统启动卡制作完成。同时，终端将会打印提示信息，如下图所示。制作时间与系统大小、Micro
SD 卡容量和接口性能有关。

![](EdgePLC BL235说明书V1.1-images/image130.png)

重新将读卡器连接，执行如下命令，可看到新制作的系统启动卡共有
BOOT、rootfs 和 rootfs-backup 三个分区。其中 BOOT 分区为 FAT32
格式，rootfs 分区和 rootfs-backup 分区 为 EXT4 格式。FAT32 格式分区在
Windows 系统下可见，EXT4 格式分区在 Windows 系统 下不可见，三个分区在
Linux 系统下均可见。

![](EdgePLC BL235说明书V1.1-images/image131.png)

BOOT 分区：主要存放 U-Boot 启动镜像 u-boot.img、tiboot3.bin、tispl.bin
等文件，从制卡工具包 boot
目录拷贝而来。使用系统启动卡启动系统时，将使用此目录的文件启动U-Boot。

rootfs 分区：存放文件系统。rootfs 分区 boot
目录主要存放内核镜像、设备树文件等,从制卡工具包"filesystem/boot/"目录拷贝而来。使用系统启动卡启动系统时，将使用此目录的文件启动。

rootfs-backup
分区：存放备份的文件系统。系统固化时，将其内容固化至存储设备对应文件系统分区。

点击右下角的大容量存储设备图标，选择"Disconnect(Connect to
host)"选项（如下图），断开 Micro SD 卡与 Ubuntu
之间的连接，完成系统启动卡制作。

![](EdgePLC BL235说明书V1.1-images/image132.png)

### 4.1.2 从启动卡启动

将系统启动卡插至评估板 Micro SD 卡槽，根据评估底板丝印将启动方
式选择拨码开关拨为 00011000(1~8)，此档位为 SD
启动模式。将调试接口连接到PC
机，设备重新上电启动，串口调试终端会打印如下类似 启动信息。其中，mmc1
表示从 MicroSD 卡启动。

![IMG_256](EdgePLC BL235说明书V1.1-images/image133.png)

内核启动打印信息如图所示，可以从打印信息中查看当前评估板型号。

![IMG_256](EdgePLC BL235说明书V1.1-images/image134.png)

系统启动后，会自动登录 root
用户，串口调试终端将会打印如下类似信息，说明使
用系统启动卡启动设备成功。

![IMG_256](EdgePLC BL235说明书V1.1-images/image135.png)

查看当前 Linux 内核版本信息。

cat /proc/version

![IMG_256](EdgePLC BL235说明书V1.1-images/image136.png)

### 4.1.3 将系统固化到eMMC

系统启动卡制作时，已将固化系统的脚本文件 mkemmcboot.sh
拷贝至系统启动卡文 件系统的"/opt/tools/"目录下。

![IMG_256](EdgePLC BL235说明书V1.1-images/image137.png)

执行如下指令将系统固化到eMMC中：

/opt/tools/mkemmcboot.sh

![IMG_256](EdgePLC BL235说明书V1.1-images/image138.png)

整个过程耗时约 5~10min，成功固化 Debian 系统至
eMMC。脚本文件将会进行如下操作：

1)  清除 U-Boot 环境变量。

2)  将 eMMC 格式化为 BOOT 、rootfs 分区。

3)  将系统启动卡 BOOT 分区中的 u-boot.img 、tiboot3.bin 、tispl.bin
    固化至 eMMC 对 应分区。

4)  将系统启动卡 rootfs-backup 分区中的文件系统固化至 eMMC 的 rootfs
    分区，包括内核镜像和设备树文件。

至此系统固化完成，从eMMC启动需要先将设备断电，再将拨码开关改成00001000(1~8)，然后重新上电。如果系统显示为mmc0表示已经正常eMMC启动。

![IMG_256](EdgePLC BL235说明书V1.1-images/image139.png)

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 22%" />
<col style="width: 54%" />
</colgroup>
<tbody>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td rowspan="6" style="text-align: center;"></td>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td rowspan="6" style="text-align: center;"></td>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
<tr>
<td style="text-align: center;"></td>
<td style="text-align: center;"></td>
</tr>
</tbody>
</table>

# 5.导轨安装

配备导轨卡扣分为下段式短款导轨结构。此设计预留了充足的螺丝锁付空间，便于用户进行安装操作。

![8aec9eb215acbbce3b8954b2e1062111_compress](EdgePLC BL235说明书V1.1-images/image140.png)![8aec9eb215acbbce3b8954b2e1062111_compress](EdgePLC BL235说明书V1.1-images/image141.png)

将卡扣垂直向下按压，直至其完全嵌入并锁定于导轨底部，即可完成安装。长导轨卡无需额外卡扣，因其内部已预设专用凹槽结构，可直接实现稳固连接。

![ac31d771be6b72005cba9ec2e46da2bc_compress](EdgePLC BL235说明书V1.1-images/image142.png)

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
