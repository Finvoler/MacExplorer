# MacExplorer 修改版 · Finvoler

这是 Finvoler 基于 **Binary Quest 的 MacExplorer 0.13.1** 维护的非官方开源修改版。原作由 Sazzad Hossain 开发，andyzoer 贡献了多语言界面和外部语言包支持。标签页、目录树和原生快速查看来自上游。[原项目](https://github.com/binaryquest/MacExplorer) · [原版说明](README.upstream.md)

Unofficial fork of Binary Quest’s MacExplorer, maintained by Finvoler. This version adds file services, a selection-driven preview pane and a shortcut to the native AirDrop window.

## 修改版功能

- **在 Explorer 中显示**。在访达或其他支持 macOS 文件服务的软件里右键本地文件，选择「服务 → 在 Explorer 中显示」，即可打开所在文件夹并选中文件。
- **复制文件地址**。在同一个「服务」菜单里复制完整路径。选中多个文件时，每个路径占一行。本机使用的访达一级菜单由独立的 Finder Sync 扩展提供，单独构建此仓库可使用「服务」入口。
- **右侧预览栏**。单击文件或用方向键切换，右侧随选区更新。支持系统快速查看可预览的文件，Markdown 在本地渲染。工具栏可开关预览，拖动分隔线可调宽，左侧目录树保留可用空间。
- **隔空投送和目录导航**。侧栏的「隔空投送」打开苹果自带的投送窗口。常用位置增加了「应用程序」等入口，顶部地址栏跟随当前目录更新。

[提交给上游的 PR #20](https://github.com/binaryquest/MacExplorer/pull/20)

## 在 Mac 上构建修改版

需要 macOS 14 或更高版本，以及支持 Swift 6 的工具链。在终端运行下面的命令，首次构建需要联网获取依赖。

```sh
git clone https://github.com/Finvoler/MacExplorer.git
cd MacExplorer
zsh scripts/build.sh
open build/Explorer.app
```

修改版与上游使用相同的应用名和 bundle ID。已经安装原版时，可先退出原版，再从构建目录打开修改版体验。[原版下载与发行说明](https://github.com/binaryquest/MacExplorer/releases)对应 Binary Quest 发布的版本。

## 许可证

MacExplorer 及本仓库修改使用 MIT 许可证。Markdown 预览使用随源码附带的 markdown-it。[项目许可证](LICENSE) · [markdown-it 许可证](Sources/ExplorerCore/Resources/Markdown/LICENSE-markdown-it.txt)
