# 奶绿桌宠 · Milky Green Desktop Pet

离线的桌面宠物：四个可换的角色、表情和互动，加一个会到点提醒的番茄钟。不需要账号、网络、AI 或在线语音服务。

当前版本：**0.1.1** · [下载与更新说明](https://github.com/tosya301/milky-green-desktop-pet/releases/tag/v0.1.1) · [发行包核验](docs/v0.1.1/发行包核验.md)

## 下载

| 平台 | 文件 | 大小 |
| --- | --- | --- |
| Apple Silicon Mac，macOS 13+ | [Mac arm64 App ZIP](https://github.com/tosya301/milky-green-desktop-pet/releases/download/v0.1.1/MilkyGreenPet-0.1.1-macos-arm64.zip) | 236.2 MiB |
| Windows 10 / 11 x64 | [便携 EXE](https://github.com/tosya301/milky-green-desktop-pet/releases/download/v0.1.1/MilkyGreenPet-0.1.1-windows-x64-portable.exe) | 183.1 MiB |
| Windows x64，完整运行目录 | [Windows 目录 ZIP](https://github.com/tosya301/milky-green-desktop-pet/releases/download/v0.1.1/MilkyGreenPet-0.1.1-windows-x64.zip) | 259.7 MiB |

[SHA-256 校验清单](https://github.com/tosya301/milky-green-desktop-pet/releases/download/v0.1.1/SHA256SUMS.txt) · [发行清单](docs/v0.1.1/release-manifest.json)

每个平台选一个包。Windows 的便携 EXE 和目录 ZIP 内容相同，二选一即可。当前不提供 Intel Mac 或 Windows ARM64 包。

这是安装包与说明的分发仓库，不发布应用源码。GitHub 自动生成的 **Source code** 归档只有本仓库的说明文件，安装请用上表的应用包。

## 第一次打开

**Mac**：解压得到「奶绿桌宠.app」，可以拖进「应用程序」。应用没有经过 Apple 公证，第一次打开会提示无法验证开发者：按住 Control 点按（或右键）应用，选「打开」，再点「打开」。也可以在「系统设置 › 隐私与安全性」里点「仍要打开」。

**Windows**：便携 EXE 直接双击运行，每次启动会先解压到临时目录，所以比目录版慢几秒。目录 ZIP 要完整解压，再运行其中的 `MilkyGreenPet.exe`，不要单独把 EXE 拿出来。应用没有发行者签名，SmartScreen 提示时点「更多信息」→「仍要运行」。

## 从 0.1.0 更新

退出正在运行的奶绿桌宠，下载新包替换旧的应用即可：Mac 用新的「奶绿桌宠.app」替换旧的，Windows 用新的便携 EXE 或整个新解压的文件夹替换旧的。设置、角色位置和番茄钟进度保存在下面「数据与卸载」写的数据目录里，不会因为替换应用而丢失。新包第一次打开时，同样需要按上一节的方法确认一次。

## 能做什么

- **四个角色**：奶绿 · 常服（半身 / 全身）、奶小绿、奶小绿 · 常服、奶小绿 · 女仆（可戴眼镜）。可以只显示一个，也可以打开多角色同时放最多四个，各自移动和缩放。
- **互动**：左键拖动，滚轮缩放，轻点会回弹或眨眼，连续点击会开心；眼睛会跟着鼠标看。右键角色打开菜单：更换角色、番茄钟、表情与设置、退出。
- **表情**：自然、浅笑、开心、左右眨眼、惊讶、思索等，选中的表情会一直保持。选「自然」时，没人互动的话每隔 30–60 秒会自己换一个待机表情，保持 16 秒再回到自然。
- **番茄钟**：独立的透明悬浮钟，可拖动、缩放、收起。默认专注 30 分钟、休息 5 分钟、1 轮，标题、时长和轮数都能改。收起后照常计时。
- **语音提醒**：到点播放内置的 21 段本地语音，分开始休息、休息结束、整组完成等几类，每类台词轮流播完才重复。播报时当前角色会按语音的实际响度动嘴。「表情与设置」里可以调语音音量，调到 0 就是静音。
- **入口**：Mac 在菜单栏，Windows 在任务栏右下角的通知区域（Windows 11 可能先收在「^」里，可以拖到任务栏上常驻），都有「显示立绘」「更换角色」「表情与设置」「Pomodori 番茄钟」和「退出奶绿桌宠」。

## 数据与卸载

设置和番茄钟进度保存在：

- Mac：`~/Library/Application Support/MilkyGreenPet`
- Windows：`%APPDATA%\MilkyGreenPet`

卸载时退出应用，删除应用本身（或解压出的文件夹），再删除上面的数据目录即可。应用不联网，不收集或上传任何数据。

## 测试范围与已知限制

- Mac 包在 Apple Silicon Mac 上做了完整的实际运行回归，包括拖动、点击、角色切换、番茄钟到点语音、嘴形同步、重启恢复和长时间使用。
- Windows 包只做了包体核验：程序架构、内容与 Mac 版一致、便携包与 ZIP 的往返校验、图标和托盘图标。**尚未在 Windows 真机上运行验收**，特别是多显示器、不同缩放比例下的拖动和位置。
- Mac 未经 Apple 公证，Windows 未签名，首次打开需要按上面的方法确认。

详细的验证内容见[发行包核验](docs/v0.1.1/发行包核验.md)（0.1.0 的见 [这里](docs/v0.1.0/发行包核验.md)）。遇到问题可以在 Issues 里反馈系统版本、使用的包和复现步骤，不要上传个人文件。

## 项目与素材

这是非官方的粉丝项目。角色、图像、声音和相关标识的权利归相应的创作者和权利人所有。公开本仓库不代表为应用、角色、图像或声音授予开源或素材许可。第三方组件的许可随应用包附在 `licenses` 目录中。详见 [NOTICE](NOTICE.md)。
