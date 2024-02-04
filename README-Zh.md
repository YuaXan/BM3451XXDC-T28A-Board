<div align="center">
<h1>
<a href="https://github.com/YuaXan/BM3451XXDC-T28A-Board">BM3451XXDC-T28A-Board</a></h1>

**基于BM3451电池充电保护板**
______________________________________________________________________

[![KiCad Version: 7.0.6](https://img.shields.io/badge/KiCad-7.0.6%7C7.0.10%7Cnightly--7.99%7Cnightly--8.0.0-blue?logo=kicad)](https://www.kicad.org/)
![Design Rule Check: passing](https://img.shields.io/badge/DRC-passing-brightgreen.svg)
![GitHub Release](https://img.shields.io/github/v/release/YuaXan/BM3451XXDC-T28A-Board)
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/YuaXan/BM3451XXDC-T28A-Board/total)
![GitHub contributors](https://img.shields.io/github/contributors/YuaXan/BM3451XXDC-T28A-Board)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-brightgreen.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-brightgreen.svg)](https://creativecommons.org/licenses/by/4.0/)
</div>

## 产品介绍
该板使用 `BM3451XXDC-T28A` 来保护3/4/5节充电电池组。持续监测每节电池的电压、充电或放电电流以及环境温度，提供过充、过放、放电过流、短路、充电过流和过温保护等等，另外还可以通过设置外部电容来改变过充、过放、放电过流的保护延时时间。
![Charge or discharge mosfets](/png/BM3451XXDC-T28A-Board.png "Charge or discharge mosfets")

## 应用场景
1. 电动工具
2. 电动自行车
3. UPS电源应用
4. 等等

## 产品概述
该板工作电压范围在5-30V，充电或者放电电流最高为30A。

通过替换`Q8`, `Q9`, `Q10`, `Q11`这四个MOS管和两个电流采样电阻`RSENSE1`和`RSENSE2`可达到更高的电流输出。

![Charge or discharge mosfets 3D](/png/charge-or-discharge-mosfets-3D.png "Charge or discharge mosfets 3D")

![Charge or discharge mosfets](/png/charge-or-discharge-mosfets.png "Charge or discharge mosfets")

![Jepsun current resistors 3D](/png/jepsun-current-resistors-3D.png "Jepsun current resistors 3D")

![Jepsun current resistors](/png/jepsun-current-resistors.png "Jepsun current resistors")

---

选择电池数量是基于`RSET1`和`RSET2`贴上0Ω电阻来决定。

当`RSET1`和`RSET2`都没有贴0Ω电阻时，`SET`引脚处于高组态的状态，同时该板可接上5串电池。

当`RSET1`贴上电阻，`RSET2`没有贴电阻，同时短接`B1`与`B-`，该板子可以接上4串电池

当`RSET1`没有贴电阻，`RSET2`贴上电阻，同时短接`B2`、`B1`和`B-`，该板子可以接上3串电池

**[警告]: 不能`RSET1`和`RSET2`全贴上0Ω电阻，这个行为会造成短路**

![B2/B1/B- Conncets](/png/B2-B1-B--conncets.png "B2/B1/B- Conncets")

![SET PIN and resistors 3D](/png/SET-PIN-and-resistors-3D.png "SET PIN and resistors 3D")

![SET PIN and resistors](/png/SET-PIN-and-resistors.png "SET PIN and resistors")

![3/4/5 cells application selection](/png/3-4-5-cells-application-selection.png "3/4/5 cells application selection")

---

有5个LED来监控电池均衡状态，当其中一个LED点亮，意味着对应的电池开始启动均衡。

 `LED1`、`LED2`、`LED3`、`LED4`和`LED5` 分别对应`B1`、`B2`、`B3`、`B4`和`B5`：
![balance led 3D](/png/balance-led-3D.png "balance led 3D")

 ---
 
与此同时，`DO`与`CO`分别对应`DO_LED1`与`CO_LED1`，这样就可以检查放电与充电的状态。
 
![CO DO led 3D](/png/CO-DO-led-3D.png "CO DO led 3D")

 ---

提供光耦合器的控制放电过流释放端口，安全可靠。

通过`XH P2.5mm 3pin`端子控制`OCCT`引脚。

**[警告]: `OCCT`引脚未经过测试，数据手册中并无使用说明，使用说明等待该板测试完毕后提供。**

![OCCT 3D](/png/OCCT-3D.png "OCCT 3D")


## 产品使用
该板连接方式如下图所示：
![BM3451XXDC-T28A-Board Connection Diagram](/png/BM3451XXDC-T28A-Board-Connection-Diagram.png "BM3451XXDC-T28A-Board Connection Diagram")

## TODO
- [ ] 板子已经制造出来。
- [ ] 板子已经测试完毕。
- [ ] 知道`OCCT`如何使用.
- [ ] 捐赠渠道已经开通。

## 贡献者
非常感谢大家对本仓库的每一份贡献！如果您发现任何错误或问题，请打开一个问题或拉动请求，以便为大家修正。

对于功能请求： 请提交问题，一旦我有时间，我就会在未来的版本中添加该功能。

## 捐助者
捐款渠道目前尚未开通，敬请期待。

## 许可证
对于电子爱好者或者极客而言，遵守[CC-BY-NC-SA 4.0](/LICENSE.txt)许可证。对于贡献者与捐赠者而言，你可以遵循[CC-BY 4.0](/LICENSE-CC-BY-4.0.txt)许可证，这意味着支持商业使用与随意分发。

## 资料
[BM3451XXDC-T28A 数据手册](http://www.bydmicro.com/params/field/preview/PDF_PRODUCT_202304141002.pdf)