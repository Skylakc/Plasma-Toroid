# 等离子环制作说明

作者 *对角巷魔法商店*

淘宝[购买](https://item.taobao.com/item.htm?id=762339447892)套件or成品

淘宝店铺搜索：[对角巷魔法商店](https://shop508227956.taobao.com/)

[成品效果视频](https://www.bilibili.com/video/BV1YQ4y157gs)

[立创开源平台](https://oshwhub.com/skylake/plasmatoroid-drive-circuit)

[详细制作教程](./Documents/Tutorial.md)

<img src=./imgs/cover.jpg width=100% />

## 免责声明
在您使用本文档制作等离子环前，请仔细阅读以下重要安全警告和免责说明。使用本文档即表示您已充分了解并同意以下条款：
- 等离子环的危险性：等离子环在运行时玻璃瓶身会产生高温，存在低温烧伤风险。任何时候都不建议用手直接触摸正在运行的玻璃瓶，以免烧伤。
- 磁场警告：等离子环在运行时会产生较强磁场。对于佩戴心脏起搏器及其他医疗设备的人群，强磁场可能会影响设备正常工作。我们建议这部分用户应远离正在工作的等离子环，避免可能的健康风险。
- 高电压风险：等离子环的驱动电路在工作时会产生高电压。高电压存在触电或灼伤的危险，请在电路工作时不要触碰任何元件，包括初级线圈，以免触电或烧伤。
- 元件温度：请注意，电路的某些元件在运行时可能会变得非常热，这可能会造成烫伤。请在设备运行时，特别是长时间运行后，不要触摸这些元件。

使用本文档意味着您已经了解并同意自担使用风险，对于不遵守安全指南而造成的任何直接或间接损害，作者不承担任何责任。

谨慎DIY，安全至上！


## 等离子环（Plasma Toroid）的工作原理解析

  - 辉光放电现象：在特定条件下，气体会在强电场的作用下发生辉光放电。这一过程中，气体分子的电子受激发后跃迁至更高能级轨道。由于这些电子在高能态下并不稳定，它们会自主回落至原始低能轨道，同时根据能量守恒定律释放出能量差对应的光子。这一现象就是辉光放电，它被应用于霓虹灯等装置中。等离子环的发光过程与此类似。

  - 等离子体的性质：除了常见的固体、液体和气态，等离子体是存在于宇宙中的另一种物质状态，火焰便是包含等离子体的例子。当气体受到高温的影响时，分子间的碰撞会使得外层电子脱离其轨道，形成一种由带电粒子组成的等离子体。这种带电的离子混合物具有导电性。
  - 环形电磁场的产生：通过在环形线圈中通入高频交变电流，可以根据麦克斯韦方程组得出其周围电场分布为环形。我们使用自激的Class E震荡电路来生成频率为10MHz左右的交流电。

  - 等离子环的生成过程：在一个封有低压氙气的球形玻璃瓶内，氙气在强电场的作用下被电离，形成等离子体。这些导电的氙气等离子体在外加环形电场的影响下，形成稳定的环状结构。在等离子体中，带电粒子的碰撞产生辉光放电，进而发出淡紫色的光芒，这使得等离子环可见。

**请您在使用和展示等离子环时，确保理解其工作原理和相应的安全措施，以保障使用者的安全。**

## 版权声明©

此文档仅供个人学习制作等离子环使用，未经作者同意，任何人不得修改、重新发布、发行本文档内容。严禁使用本文档进行任何商业行为。
