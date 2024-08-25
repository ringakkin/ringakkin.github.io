---
title: 黑曜石左拉
---
# 黑曜石左拉

[![](https://camo.githubusercontent.com/1d5ec435f65ca9b3a5d5ab1c25c27349318ca18dc423430b57fd566b7e2555cd/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f762f72656c656173652f70706565747465657272732f6f6273696469616e2d7a6f6c61)](https://camo.githubusercontent.com/1d5ec435f65ca9b3a5d5ab1c25c27349318ca18dc423430b57fd566b7e2555cd/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f762f72656c656173652f70706565747465657272732f6f6273696469616e2d7a6f6c61) [![](https://camo.githubusercontent.com/de840d9d223cf010cfaea38d4dbdf0355ceef30bce62e0b42ea59e2119d17523/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6973737565732d636c6f7365642d7261772f70706565747465657272732f6f6273696469616e2d7a6f6c61)](https://camo.githubusercontent.com/de840d9d223cf010cfaea38d4dbdf0355ceef30bce62e0b42ea59e2119d17523/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6973737565732d636c6f7365642d7261772f70706565747465657272732f6f6273696469616e2d7a6f6c61) [![](https://camo.githubusercontent.com/2ebf393f6cc610f2ae2883a8b3ca39f13d559bcf9e951a67bd21705246e4e8d4/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f64796e616d69632f6a736f6e3f636f6c6f723d626c756576696f6c6574266c6162656c3d746f6461792532377325323076696577732671756572793d2532342e6461746173657473253542312535442e76616c7565732535422532382534302e6c656e6774682d312532392535442675726c3d687474707325334125324625324679687970652e6d6525324661706925324663686172742532467265706f7369746f72795f76696577735f636f756e745f63686172745f636f6e74726f6c6c65722533467265706f7369746f72794e6f64654964253344525f6b67444f477048703441)](https://camo.githubusercontent.com/2ebf393f6cc610f2ae2883a8b3ca39f13d559bcf9e951a67bd21705246e4e8d4/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f64796e616d69632f6a736f6e3f636f6c6f723d626c756576696f6c6574266c6162656c3d746f6461792532377325323076696577732671756572793d2532342e6461746173657473253542312535442e76616c7565732535422532382534302e6c656e6774682d312532392535442675726c3d687474707325334125324625324679687970652e6d6525324661706925324663686172742532467265706f7369746f72795f76696577735f636f756e745f63686172745f636f6e74726f6c6c65722533467265706f7369746f72794e6f64654964253344525f6b67444f477048703441)

Obsidian Publish 的免费（但更好？）替代品。

> 该存储库包含一个易于使用（阅读：简单）的解决方案，用于将 Obsidian 个人知识管理系统（阅读：一堆随机 Markdown）转换为 Zola 站点。

致谢：这个仓库是从[Adidoks](https://github.com/aaranxu/adidoks)分叉的。

特别感谢：Wikilink 解析由[obsidian-export](https://github.com/zoni/obsidian-export)提供支持。

# [](https://github.com/ppeetteerrs/obsidian-zola#announcements)公告

**v1.3.0 满足功能要求！✨**

Bug修复：

- 修复了一些与非常规文件名相关的错误（例如包含“.”和其他特殊字符）

改进：

- 更好的本地测试设置（见`Local Testing`下文）
- 可配置的根部分名称
- 可配置的页脚内容

# [](https://github.com/ppeetteerrs/obsidian-zola#setup)设置

**第 1 步：设置 Netlify**

- 将您的 Obsidian 保管库文件夹转变为 Git 存储库
- 创建一个指向该 Git 存储库的 Netlify 站点

**第 2 步：编辑`netlify.toml`**

- `netlify.toml`在您的黑曜石保管库文件夹中创建
- 复制此存储库中的内容`netlify.example.toml`并替换适当的设置（`SITE_URL`，`REPO_URL`并且`LANDING_PAGE`不能留空）。

**第三步：你就完成了🎉！**

- 推动你的改变，准备好成名！
- 花哨一点：（`netlify.toml`例如`LANDING_TITLE`）中的所有文本字段设置都支持 HTML 语法。我还为那些想要添加个人风格的人添加了`Animate.css`++ ~`Hover.css``CSShake`

**第 4 步：问题和功能请求**

- 如果您遇到任何问题，请先参考[Config+FAQ](https://github.com/ppeetteerrs/obsidian-zola/blob/main/CONFIG.md)。如果仍未解决，只需在`Issues`选项卡中发布即可。如果问题与部署相关，最好包含在 Netlify 面板中找到的错误日志的副本。
- 如果您有任何功能请求，也请发布问题。但是，请注意，此存储库旨在作为一个文件设置。除非大多数用户需要，否则不会支持高级功能/详细的可配置性。不过，我可以帮助您实现适合您需求的分叉🥂。

**第 5 步：（可选增强功能）自动提交站点地图**

为了使您的网站对搜索引擎更加友好，您可以添加一个 netlify 插件，以便在每次重新部署网站时自动提交新的站点地图。只需将以下内容添加到您的`netlify.toml`. 请记住替换`baseUrl`为您的`SITE_URL`.

```toml
[[plugins]]
package = "netlify-plugin-submit-sitemap"

[plugins.inputs]

# The base url of your site (optional, default = main URL set in Netlify)
baseUrl = "https://peteryuen.netlify.app/"

# Path to the sitemap URL (optional, default = /sitemap.xml)
sitemapPath = "/sitemap.xml"

# Time in seconds to not submit the sitemap after successful submission
ignorePeriod = 0

# Enabled providers to submit sitemap to (optional, default = 'google', 'bing', 'yandex'). Possible providers are currently only 'google', 'bing', 'yandex'.
providers = [
  "google",
  "bing",
  "yandex",
]
```

# [](https://github.com/ppeetteerrs/obsidian-zola#example-site)示例站点

> 不要`netlify.toml`从示例站点复制，它不稳定。请参考来自`netlify.example.toml`.

该[示例站点](https://peteryuen.netlify.app/)展示了 的功能`obsidian-zola`。请注意，示例站点使用 的`dev`分支`obsidian-zola`。如果您看到示例站点中可用但主分支中尚不可用的功能，请考虑尝试`dev`（不稳定）分支。具体方法可以参考[示例仓库](https://github.com/ppeetteerrs/obsidian-pkm) `netlify.toml`的.

# [](https://github.com/ppeetteerrs/obsidian-zola#local-testing-ubuntu-thanks-trwbox)本地测试（Ubuntu）[感谢@trwbox]

- 根据网站上的说明安装 zola`https://www.getzola.org/documentation/getting-started/installation/`
- 运行以下命令来安装其他所需的依赖项`sudo apt install python-is-python3 python3-pip`和`pip3 install python-slugify rtoml`（或使用`conda`/ `mamba`）
- 用于`git clone https://github.com/ppeetteerrs/obsidian-zola`将存储库克隆到黑曜石保管库文件夹内以外的其他位置
- `.vault_path`使用文件或`$VAULT`环境变量设置 ObsisianVault 的路径
- 用于`./local-run.sh`运行网站

# [](https://github.com/ppeetteerrs/obsidian-zola#features)特征

**免责声明**

> 该工具专为使用 Obsidian 作为简单高效的笔记应用程序（或 PKM）的用户而设计。如果您为 Obsidian 配置了大​​量奇特的短代码、插件和特定于 Obsidian 的语法，则该工具不会（也无意）支持这些功能。

**支持的**

- 知识图谱（也可以将其视为反向链接）
- LaTEX（由 提供支持`KaTEX`，再见 MathJAX 粉丝👋）
- 部分字符串搜索（由 提供支持`elasticlunr`）
- 语法高亮 + Fira 代码！
- 可定制的动画
- 导航
- 表中的内容
- 典型的 Markdown 语法
- 删除线
- 表格
- 单行脚注（即`[^1]`在段落中及`[^1]: xxx`后面）
- 复选框
- 链接转义模式：`[Slides Demo](<Slides Demo>)`

**不支持**

- 非图像/注释嵌入（例如视频、音频、PDF）。它们将变成链接。
- 调整图像大小
- 突出显示文本
- 评论
- 内联/多行脚注
- 美人鱼图

# [](https://github.com/ppeetteerrs/obsidian-zola#gotchas)陷阱

1. 没有带有名称`index.md`或名称的文件`_index.md`
2. ~~不存在与其子文件夹同名的文件（例如同时存在`.../category1.md`且`.../category1/xxx.md`不允许）~~（固定的）
3. `LANDING_PAGE``SLUGIFY`如果打开，则需要设置为 slugified 文件名（例如，要使用`I am Home.md`，`LANDING_PAGE`需要`i-am-home`）

# [](https://github.com/ppeetteerrs/obsidian-zola#wips--ideas)WIP/想法

- （可能会做）反向链接/提及
- （也许）洛蒂动画？
- （不知道）可配置的折叠图标