# 等离子环制作说明

此文档更新于2024年1月28日

作者 *对角巷魔法商店*

[成品效果视频](https://www.bilibili.com/video/BV1YQ4y157gs)

[立创开源平台](https://oshwhub.com/skylake/plasmatoroid-drive-circuit)

等离子环开源技术交流QQ群  736688139


<img src=../imgs/cover.jpg width=100% />

## 版权声明©

此文档仅供个人学习制作等离子环使用，未经作者同意，任何人不得修改、重新发布、发行本文档内容。严禁使用本文档进行任何商业行为。

## 免责声明
在您使用本文档制作等离子环前，请仔细阅读以下重要安全警告和免责说明。使用本文档即表示您已充分了解并同意以下条款：
- 等离子环的危险性：等离子环在运行时玻璃瓶身会产生高温，存在低温烧伤风险。任何时候都不建议用手直接触摸正在运行的玻璃瓶，以免烧伤。
- 磁场警告：等离子环在运行时会产生较强磁场。对于佩戴心脏起搏器及其他医疗设备的人群，强磁场可能会影响设备正常工作。我们建议这部分用户应远离正在工作的等离子环，避免可能的健康风险。
- 高电压风险：等离子环的驱动电路在工作时会产生高电压。高电压存在触电或灼伤的危险，请在电路工作时不要触碰任何元件，包括初级线圈，以免触电或烧伤。
- 元件温度：请注意，电路的某些元件在运行时可能会变得非常热，这可能会造成烫伤。请在设备运行时，特别是长时间运行后，不要触摸这些元件。
- 电磁干扰：等离子环运行时会发射10MHz左右的电磁波，该波段对人体无伤害，但可能干扰此频段运行的部分电子设备，例如触摸板和刷卡机，请将这些设备远离正在工作的驱动电路。

使用本文档意味着您已经了解并同意自担使用风险，对于不遵守安全指南而造成的任何直接或间接损害，作者不承担任何责任。

谨慎DIY，安全至上！

## 等离子环（Plasma Toroid）的工作原理解析

  - 辉光放电现象：在特定条件下，气体会在强电场的作用下发生辉光放电。这一过程中，气体分子的电子受激发后跃迁至更高能级轨道。由于这些电子在高能态下并不稳定，它们会自主回落至原始低能轨道，同时根据能量守恒定律释放出能量差对应的光子。这一现象就是辉光放电，它被应用于霓虹灯等装置中。等离子环的发光过程与此类似。

  - 等离子体的性质：除了常见的固体、液体和气态，等离子体是存在于宇宙中的另一种物质状态，火焰便是包含等离子体的例子。当气体受到高温的影响时，分子间的碰撞会使得外层电子脱离其轨道，形成一种由带电粒子组成的等离子体。这种带电的离子混合物具有导电性。
  - 环形电磁场的产生：通过在环形线圈中通入高频交变电流，可以根据麦克斯韦方程组得出其周围电场分布为环形。我们使用自激的Class E震荡电路来生成频率为10MHz左右的交流电。

  - 等离子环的生成过程：在一个封有低压氙气的球形玻璃瓶内，氙气在强电场的作用下被电离，形成等离子体。这些导电的氙气等离子体在外加环形电场的影响下，形成稳定的环状结构。在等离子体中，带电粒子的碰撞产生辉光放电，进而发出淡紫色的光芒，这使得等离子环可见。

**请您在使用和展示等离子环时，确保理解其工作原理和相应的安全措施，以保障使用者的安全。**


## 准备材料

<img src=../imgs/all_components.jpg width=100% />

- 充有氙气的玻璃瓶80mm(在淘宝搜索等离子环可找到,更大的玻璃球无法安装到本项目的支架中)
- 漆包线 —— 绕线电感 （作者使用的漆包线都是1.2mm的）
- 漆包线 —— 初级线圈
- 电路板PCB (可用洞洞板或者搭棚替代)
- 散热片与风扇
- MOS管 IRFP260N
- 电位器 10k（最好是蓝色的多圈电位器）
- 电阻470（在新版本中这个电阻被换为了1k）
- 电阻1k
- 瓷片电容 30pf * 4
- 瓷片电容 4.7nF * 2
- TVS 15V （双向）
- 稳压二极管 12V
- 输入滤波电容 电解电容 63V 220uf * 3 
- 接线端子
- 打火机中拆出来的压电陶瓷 (用于初始点亮)
- 24v电源适配器
- XL4015限流模块

## 制作教程
难度 ★★★☆☆

### 工具
- 万用表 
- 电烙铁 
- 焊锡丝 
- 小刀 
- 斜口钳 
- 内六方螺丝刀套装

<img src=../imgs/tools.jpg width=100% />

### 步骤
- 烧热烙铁，准备好六个初级线圈架，插在底座上，用焊锡焊接固定。尽可能保证支架和底板处于垂直状态。
<img src=../imgs/coil0.jpg width=100% />

- 把漆包线按照线圈架的直径弯曲三圈后剪短

- 把截下的漆包线留出约一指长作为接头拉出备用，按照小孔从上到下穿入，共三圈。穿好后另一头用同样方式拉出。孔位较小，可以通过推拉的方式穿入。

<img src=../imgs/coil1.jpg width=100% />

- 用小刀刮开线头漆皮，露出漆包线内部的铜芯。用烙铁和焊锡为铜芯镀锡
  
- 制作扼流电感。取出较长的漆包线，绕成直径大概25mm的线圈，绕20圈即可，最后用尼龙扎带固定住线圈。扼流电感也可以使用现成的10uH电感，但发热比手绕电感大一些。

<img src=../imgs/Coil.jpg width=100% />

- 制作带限流保护的电源，准备好24V电源和XL4015限流模块，将电源线剪开，把模块串联在中间，将XL4015模块调输出电压的电位器顺时针拧到头，将限流电位器拧到3.5A的位置，确定该电位器位置的方法是:将万用表打到10A电流档，两个表笔对到输出上（此时相当于短路了输出），万用表显示的数值就是限流模块的限流值。注意，使用没有限流的电源会十分容易烧毁mos管，如果已经有可调电源则可以跳过这一步。下图中模块左边的电位器是调节输出电压，右边的电位器是调节限流。
<img src=../imgs/XL4015.jpg width=100% />
<img src=../imgs/power_source.jpg width=100% />

- 将元件按照型号分别插入电路板 (先不要安装MOS管)，由于电路在持续更新，实际电路板上的元件以最新版为准。
  
  > 电阻分辨方式
  >  - 色环电阻上带有紫色环的为470电阻(470电阻也可换为1k电阻)
  >	 - 只有棕色和黑色环的为1K电阻

  > 电容分辨方式
  > 蓝色电容上有数字说明其属性
  > - 30pF电容正面有300K字样
  > - 4.7nF电容正面有472字样

<img src=../imgs/PCB.jpg width=100% />
<img src=../imgs/PCB1.jpg width=100% />

- 将元件按照其属性分别放入PCB上等待焊接。为了方便焊接，可以将管脚进行简单折弯固定。
- 开始焊接，**注意烙铁高温，小心烫伤。**

<img src=../imgs/Solder.jpg width=100% />

- 将所有元件焊接好后，剪去管脚。请尽量保证焊点饱满圆润，去除管脚时请从根部开始。

<img src=../imgs/fin.jpg width=100% />

- 将散热片四周螺丝孔内拧入铜柱。
- 开始安装MOSFET。将MOS管有字的一面***向上***，将另一面涂上硅脂后用螺丝穿过螺丝孔固定在散热片上，MOS有字的一面面对自己，管脚***向下***，此时管脚左中右分别为G D S极。

<img src=../imgs/heatsink.jpg width=100% />

- 将管脚弯曲后插入PCB焊接。
**注意：弯曲时请勿从管脚根部开始，应当从小节开始**
- 将PCB对准散热片铜柱螺丝孔，用新的铜柱固定。
- 固定风扇,所有层的连接关系如下图所示，风扇的风冲着散热片吹（朝上吹）。

  <img src=../imgs/assemble.jpg width=100% />
  
- 将所有电路连接好，放上瓶子，并确保电位器位于逆时针最大处
- 通电，请注意安全！手远离初级线圈附近。千万不要一个手拿着瓶子一个手触摸电路上的电位器，因为瓶子上的高压静电会损坏电路。
- 慢慢向顺时针拧电位器，拧到一半的时候即可看到等离子环生成，此时再逆时针轻轻拧动，保持等离子环稳定即可。有的时候可能不会自启动，只需要用压电陶瓷打一下电火花即可出环。
- **注意：顺时针拧电位器会增大功率，长时间大功率运转会烧坏电路，建议把电位器保持在等离子环刚好不消失的位置！使用完后一定要拔掉电源！**

<img src=../imgs/Turning.jpg width=100% />

### 参考电路图
注意，此电路图仅供参考，实际电路和元件参数我们做了调整，以元件清单中的为准。

<img src=../imgs/sch.jpg width=100% />

### FAQ


鸣谢： Tate McAluney
