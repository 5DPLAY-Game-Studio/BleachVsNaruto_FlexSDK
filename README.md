<p align = "center">
<a href  = "https://bvn-sports.com/"><img src = "title.png" /></a>
</p>

<p align = "center">
<img src = "https://img.shields.io/github/stars/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<img src = "https://img.shields.io/github/forks/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<img src = "https://img.shields.io/github/followers/5DPLAY-Game-Studio" />
<br />
<img src = "https://img.shields.io/github/contributors/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<img src = "https://img.shields.io/github/created-at/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<img src = "https://img.shields.io/github/license/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<br />
<img src = "https://img.shields.io/github/languages/top/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<img src = "https://img.shields.io/github/v/tag/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK" />
<br />
<strong>
<a href = "https://bvn-sports.com/">官网</a> |
<a href = "https://space.bilibili.com/1340107883">哔哩哔哩</a> |
<a href = "https://www.douyin.com/user/MS4wLjABAAAAJ2UeSAz7T6qx7XSSL70IgfuMsZZaxOIvPIL3Zdvmk8rSAoBfNfngGx7Zy2jFSnYj">抖音</a> |
<a href = "https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz=Mzg4ODE1MjgyNw==">微信公众号</a>
</strong>
</p>

## ⭐ 星标历史 <!-- omit in toc -->

<a href = "https://www.star-history.com/?repos=5DPLAY-Game-Studio%2FBleachVsNaruto_FlexSDK&type=date&legend=top-left">
 <picture>
   <source media = "(prefers-color-scheme: dark)" srcset  = "https://api.star-history.com/chart?repos=5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK&type=date&theme=dark&legend=top-left" />
   <source media = "(prefers-color-scheme: light)" srcset = "https://api.star-history.com/chart?repos=5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK&type=date&legend=top-left" />
   <img    alt   = "Star History Chart" src               = "https://api.star-history.com/chart?repos=5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK&type=date&legend=top-left" />
 </picture>
</a>

# 死神vs火影 FlexSDK <!-- omit in toc -->

**死神vs火影 FlexSDK** 是一个基于 **Flex** 框架与 **HarmanAirSDK** 合并得到的专项开发工具包。

最新版本请前往 [Release] 处下载。

## 目录 <!-- omit in toc -->

- [简介](#简介)
- [如何在本地自行合并](#如何在本地自行合并)
  - [环境需求](#环境需求)
  - [合并步骤](#合并步骤)
- [许可](#许可)
- [关注我们](#关注我们)

## 简介

本仓库存放适用于开发 **Flex** 应用程序的最新稳定 **FlexSDK** 版本。

过去，**FlexSDK** 是由 **Adobe** 作为 **Adobe FlashBuilder** 软件的一部分提供的。**FlexSDK** 能够开发以 **Flex** 框架为基础的 **Flex** 企业级应用程序。

2012 年，**Flex** 框架被 **Adobe** 捐赠给 **Apache** 开源基金会，并由其负责接手开发，**Adobe** 则完全停止分发包含了 **Flex** 框架的 **FlexSDK**，仅发行不带 **Flex** 框架的纯 **AdobeAirSDK**。如果需要使用 **Flex** 框架，则需要从 **Apache** 处获取并覆盖安装到最新的 **AirSDK** 中来完成 **FlexSDK** 的升级。

2021 年，**Adobe** 正式宣布 **Flash** 停止维护，旗下的 **AdobeAirSDK** 被 **[Harman]** 收购并更名为 **HarmanAirSDK**，但依旧不提供合并的版本，仍需开发者手动自行合并。

本仓库则依照前开发人员 **Josh Tynjala** 的教程 （<https://joshblog.net/2024/how-to-install-apache-flex-with-adobe-air-from-harman/>），手动在本地合并了最新的 **Apache Flex** 与当下稳定版本的 **HarmanAirSDK** ，组成了一个完整的 **FlexSDK** 版本。

## 如何在本地自行合并

如果出于安全考虑，您不想下载我们预构建合并的版本，或者您想合并其他版本的 AirSDK，您可参照如下步骤自行在本地手动合并。

### 环境需求

- **Java 1.8** 或更高版本
- 下载 [apache-ant-1.10.17-bin.zip] ，解压并配置 **环境变量**（需用到 **ant** 命令）。
- 下载 [apache-flex-sdk-4.16.1-bin.zip] 。
- 前往 HarmanAirSDK (<https://airsdk.harman.com/release_notes>) 下载页面，下载合适版本的 HarmanAirSDK ，其文件名应为 **AIRSDK_Flex_Windows.zip**，如果不是此文件名，则说明您下载的 SDK 不允许与 FlexSDK 合并。
- 最后，还需要下载一个安装脚本 [harman-installer.xml]，此脚本由 **Josh Tynjala** 提供。

注：由于 Harman 在 51.2 版本后对外隐藏了 HarmanAirSDK 的下载地址，推行 SDKManager，因此可以使用以下隐藏地址对版本号替换后下载所需的 SDK。

`https://airsdk.harman.com/api/versions/{具体版本号（例如：51.0.1.1）}/sdks/AIRSDK_Flex_Windows.zip?license=accepted`

### 合并步骤

- 将 apache-flex-sdk-4.16.1-bin.zip 解压到目录中，并为其命名，例如本仓库将要与 HarmanAirSDK 51.0.1.1 合并，那么可命名为 `flex4.16.1-air51.0.1.1`。
- 将下载好的 `AIRSDK_Flex_Windows.zip` 文件与 `harman-installer.xml` 脚本，放入上述 `flex4.16.1-air51.0.1.1` 目录中。
- 进入 `flex4.16.1-air51.0.1.1` 目录，执行以下命令：

```bash
#!/bin/bash

# 其中 -Dair.sdk.version = 51.0 为 HarmanAirSDK 的版本号，根据您下载的 SDK 版本号替换（仅需主次版本号即可）。
ant -f harman-installer.xml -Dair.sdk.version=51.0
```

- `harman-installer.xml` 脚本可能需要几分钟完成，如果脚本最后显示一条 **BUILD SUCCESSFUL** 消息，则表示一切正常，已成功合并完成。
- 合并完成后，您可以安全的删除 `AIRSDK_Flex_Windows.zip` 和 `harman-installer.xml` 文件。

注：若合并失败，可前往 **Josh Tynjala** 的教程，检查是否缺少了某些步骤或操作错误。

## 许可

**死神vs火影 FlexSDK** 使用 [GPL-3.0] 作为工程开发许可，您应该提前了解并充分理解许可内容：

- 本程序是免费软件： 您可以根据自由软件基金会发布的 GNU 通用公共许可证条款充分分发/修改它，无论是许可证第 3 版，或者（依据您选择的）任何更高版本。
- 本程序分发时希望它有用，但不提供任何保证，甚至没有适销性或适用于特定用途的默示担保。有关更多信息，请参阅 GNU 通用公共许可证。
- 您应该已经收到了 GNU 通用公共许可证的副本以及此程序。如果没有，请参阅 <http://www.gnu.org/licenses> 。

## 关注我们

[![Twitter:5Dplay](https://img.shields.io/twitter/follow/5Dplay)](https://x.com/5DPLAY) [![BiliBili:死神VS火影吧](https://badgen.net/badge/BiliBili/死神VS火影吧/)](https://space.bilibili.com/1340107883)

[Release]: https://github.com/5DPLAY-Game-Studio/BleachVsNaruto_FlexSDK/releases
[Harman]: https://airsdk.harman.com/
[apache-ant-1.10.17-bin.zip]: https://dlcdn.apache.org/ant/binaries/apache-ant-1.10.17-bin.zip
[apache-flex-sdk-4.16.1-bin.zip]: https://dlcdn.apache.org/flex/4.16.1/binaries/apache-flex-sdk-4.16.1-bin.zip
[harman-installer.xml]: https://raw.githubusercontent.com/joshtynjala/setup-apache-flex-action/master/harman-installer.xml
[GPL-3.0]: https://www.gnu.org/licenses/gpl-3.0.html
