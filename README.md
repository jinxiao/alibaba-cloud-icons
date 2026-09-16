# 阿里云 Iconfont 原色分类图标库 · draw.io

[English](README.en.md) · [来源记录](docs/SOURCES.md) · [配色说明](docs/COLORS.md) · [JS 插件安装](docs/PLUGIN.md)

[在线预览与下载](https://jinxiao.github.io/alibaba-cloud-icons/) — 按分类浏览、搜索图标，一键加载到网页版 draw.io。

[下载完整图标包](https://github.com/jinxiao/alibaba-cloud-icons/releases/latest/download/alibaba-cloud-drawio.zip) · [下载分类 JSON 配置](https://github.com/jinxiao/alibaba-cloud-icons/releases/latest/download/alibaba-cloud.json) · [所有版本](https://github.com/jinxiao/alibaba-cloud-icons/releases)

按照 Iconfont「阿里云设计中心」发布的图标集分类整理，**保留每个 SVG 的原始颜色和形状**。提供离线预览页、一次加载全部分类的 JSON 配置、JS 插件、分类 XML 和单个 SVG。

2026-09-10 快照：**9 个图标集、888 个条目**。其中包含彩色分类版、橙色全集和 UI 补充图标；同形的不同颜色版本分别保留，888 不是独立云服务数量，也不代表覆盖当前所有阿里云产品。

图标拖入画布后**默认没有文字**，双击后可在下方填写标签；原始名称仍用于搜索、悬停提示和图形元数据。

## 分类与原色

| Iconfont 分类 | 数量 | 主要原色 | 来源 |
| --- | ---: | --- | --- |
| 云计算基础 Cloud Infrastructure | 132 | 蓝 `#2B85FB` | [21530](https://www.iconfont.cn/collections/detail?cid=21530) |
| 大数据 Big Data | 23 | 蓝紫 `#4D3CFF` | [21419](https://www.iconfont.cn/collections/detail?cid=21419) |
| 安全 Security | 28 | 绿 `#63BA4D` | [21426](https://www.iconfont.cn/collections/detail?cid=21426) |
| 人工智能 Artificial Intelligence | 39 | 紫 `#6415FF` | [21532](https://www.iconfont.cn/collections/detail?cid=21532) |
| 企业应用 Enterprise Applications | 38 | 深蓝 `#0649D0` / `#0549D0` | [21533](https://www.iconfont.cn/collections/detail?cid=21533) |
| 开发者服务 Developer Services | 22 | 青 `#04A2B8` | [21538](https://www.iconfont.cn/collections/detail?cid=21538) |
| 物联网 IoT | 21 | 橙 `#FF8A00` | [21539](https://www.iconfont.cn/collections/detail?cid=21539) |
| 橙色全集 Orange Collection | 286 | 橙 `#FF6A00` | [21408](https://www.iconfont.cn/collections/detail?cid=21408) |
| UI 补充 Supplemental Icons | 299 | 黑、灰等原色 | [27723](https://www.iconfont.cn/collections/detail?cid=27723) |

表中是主要色值；个别路径中的细微色差、多色及白色部分均保留，不按主色统一替换。原始图标没有的底板、圆角不会额外添加。颜色由 SVG 决定，分类由发布者的集合归属决定。

上游有 31 项名称为“1备份…”或“画板…”，这里保留原始图形和名称，标记为“上游未明确命名”。“数据库备份”和“混合云备份”是正常产品名称，完整保留。

## 快速使用：一次加载所有分类

直接打开[在线预览页](https://jinxiao.github.io/alibaba-cloud-icons/)，或下载 `alibaba-cloud-drawio.zip` 后解压并打开 `index.html`。源码仓库不提交生成目录；克隆源码后先按下文构建，再打开 `dist/index.html`。

**网页版一键加载：** 点击 **一键加载全部分类到 draw.io**，在新标签页打开网页版并加载 9 个独立分类面板，无需复制配置。也可以先选择分类，再点击 **加载当前分类到 draw.io**。加载范围不受搜索筛选影响。首次打开若出现存储位置或新建图表提示，按页面提示继续。

一键加载使用 draw.io 官方支持的 [`clibs` URL 参数](https://www.drawio.com/docs/reference/supported-url-parameters/)，需要联网访问公开 XML 图库。本地文件或本地 HTTP 预览使用本项目已发布的在线图库；部署到 HTTPS 网站后使用该网站当前目录下的图库，因此兼容 Fork 的站点路径。本地尚未发布的图标更改请使用配置或 XML 导入。

**离线或桌面版配置：**

1. 在预览页点击 **复制全部分类配置**；浏览器不允许直接复制时，页面会选中配置供手动复制。
2. 在 draw.io 选择 **其他 → 配置 → JSON**（Extras → Configuration；简洁界面在 Settings 菜单），粘贴、应用并刷新或重启。
3. 若分类未显示，在“更多图形”勾选 **阿里云 Iconfont 全部分类**。
4. 展开各分类，拖入图标；双击输入自己的标签，文字显示在图标下方。

“更多图形”中的“阿里云 Iconfont 全部分类”带有 9 类代表图标的预览图，已内嵌到 JSON，无需联网。若此前安装的配置只显示描述文字，请用新版替换原阿里云分组，应用并刷新；已安装的配置不会随本地文件自动更新。

也可以直接复制 `dist/config/alibaba-cloud.json`。已有其他自定义配置时，将本项目的 `libraries` 分组合并进去，把 `alibaba-cloud-iconfont` 追加到 `defaultLibraries`，保留其他设置。

**一个普通 XML 只能创建一个面板**，所以 `all-icons.xml` 是平铺总库。一键加载链接会同时打开 9 个分类 XML，形成 9 个独立面板。若希望在“更多图形”中通过一个阿里云分组统一勾选，使用 JSON 配置或插件。[draw.io 原生配置格式](https://www.drawio.com/docs/reference/configure-diagram-editor/#libraries)

## 从此前版本迁移

此前版本优先选择橙色全集，再统一生成蓝色或蓝底白色，并按官网产品目录分成 19 类。这不符合 Iconfont 各分类的原始配色，本版已改为上表的 **9 个来源分类**。

安装新版前，删除配置中旧的阿里云 `libraries` 分组及 `defaultLibraries` 中的 `alibaba-cloud-services`，关闭旧 XML 面板，再安装新版。只保留新版 `alibaba-cloud-iconfont` 分组；其他自定义配置继续保留。

若以前安装了 JS 插件，移除旧插件后加载新版并刷新。已有图纸内嵌的图标不会自动换色；需要从新版图库重新拖入替换。

本次删除了失去引用的旧素材归档、官网目录映射和补图配置，以及旧的三个配色版本。橙色全集作为 Iconfont 发布的独立图标集继续保留，不再作为其他分类的优先来源。

## 输出与目录

| 文件 | 用途 |
| --- | --- |
| `dist/index.html` | 搜索预览、一键加载网页版、分类下载和复制配置 |
| `dist/config/alibaba-cloud.json` | 一份配置加载 9 个分类 |
| `dist/plugins/alibaba-cloud.js` | 自托管 draw.io 插件，详见 [安装说明](docs/PLUGIN.md) |
| `dist/drawio/01-cloud-infrastructure.xml` 等 | 单个分类；“文件 → 打开图库 → 设备”导入 |
| `dist/drawio/all-icons.xml` | 保留不同版本的平铺总库 |
| `dist/svg/iconfont-<id>.svg` | 单个 SVG，文件名对应上游图标 ID |
| `dist/catalog.csv` | 原始名称、分类、色值和来源链接 |
| `dist/alibaba-cloud-drawio.zip` | 完整分发包 |

项目源码分为 `data/`（SVG、目录、来源锁）、`src/`（插件与预览页）、`scripts/`（采集、整理、构建）、`tests/` 和 `docs/`。`dist/` 与下载缓存 `.cache/` 不入 Git。

## 构建与检查

Python 3.10+，仅使用标准库；图标数据已在仓库内，构建不访问来源站点。推荐通过 [uv](https://docs.astral.sh/uv/) 运行：

```sh
uv run python scripts/build_libraries.py
uv run python -m unittest discover -s tests
node --test tests/test_plugin.cjs
```

Node.js 18+ 只用于插件测试。构建会生成分发包和 SHA-256 清单，检查每个 XML；测试检查原色与路径保留、分类归属、空标签、SVG 安全边界和插件注册行为。模拟插件 API 测试不代替真实 draw.io 兼容性测试。

请打开 `dist/index.html`，分别查看基础设施蓝色、大数据蓝紫色、安全绿色和 AI 紫色；在 draw.io 应用配置，检查 9 个分类折叠、搜索、拖入后无文字、下方标签编辑，以及保存重新打开。

## GitHub Pages 发布

站点地址：**https://jinxiao.github.io/alibaba-cloud-icons/**。使用 GitHub 默认域名，不配置自定义域名或 `CNAME`。

[发布工作流](.github/workflows/pages.yml)从仓库内的图标快照构建 `dist/`，通过 Python 和插件测试后，将整个目录作为 Pages artifact 发布。无需提交 `dist/`，也无需维护 `gh-pages` 分支；构建不会重新抓取 Iconfont。

- **手动发布**：打开 [Actions → Deploy GitHub Pages](https://github.com/jinxiao/alibaba-cloud-icons/actions/workflows/pages.yml)，点击 **Run workflow**，选择 `main` 后运行。
- **Release 自动发布**：发布新 Release 时触发（`release: published`，包括预发布），构建对应 Release 标签的代码。草稿保存和普通代码推送不触发部署。
- **部署记录**：在工作流的 `Deploy dist` 作业或仓库的 `github-pages` 环境查看状态和站点链接。测试失败时不会进入部署。

在线站点包含预览页、分类 JSON、XML、SVG、插件和完整 ZIP 下载；手动部署的版本可能比最新 Release 更新。此工作流不创建 Release，也不上传 Release 附件。

Fork 后，在仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**，再手动运行工作流。默认访问地址为 `https://<账号>.github.io/<仓库名>/`；相对资源路径支持仓库子路径。

若 `github-pages` 环境限制可部署的分支或标签，请在 **Settings → Environments → github-pages** 中允许 `main` 分支和 Release 标签（例如标签规则 `*`）。另外，GitHub 会继承个人/组织主页的自定义域名；若要使用默认 `github.io` 域名，个人/组织主页也必须解除该绑定，见 [GitHub 域名继承说明](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)。

## 更新和贡献

```sh
uv run python scripts/sync_sources.py --refresh
uv run python scripts/prepare_catalog.py --snapshot-date YYYY-MM-DD
uv run python scripts/build_libraries.py
```

日期替换为实际采集日期。来源锁包含发布者图标集列表；增加、减少分类或列表分页不完整时，整理脚本会停止，要求维护者检查分类定义。审核条目数量、颜色和命名变化后再提交，不把原始 API 中无关的用户信息复制到发布数据。

贡献应包含原始 Iconfont 集合及图标 ID，保持来源颜色和分类；不要通过关键词猜测未命名画板的产品身份。发布时上传生成 ZIP 为 Release 附件，或把 `dist/` 托管为静态预览站。

新增项目代码使用 [MIT](LICENSE)。图标及商标不在代码许可授权范围，见 [NOTICE.md](NOTICE.md)。本项目是社区格式转换工具，非阿里云或 draw.io 官方项目。
