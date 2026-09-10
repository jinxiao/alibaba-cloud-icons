# 阿里云 Iconfont 原色分类图标库

本包包含 9 个 Iconfont 原始分类、888 个条目，保留各自配色，包括不同颜色版本及 UI 图标；不是 888 个独立云服务。

1. 双击 `index.html`，点击 **复制全部分类配置**。
2. 在 draw.io 的 **其他 → 配置 → JSON** 粘贴、应用并刷新；简洁界面在 Settings 菜单。
3. 若未显示，进入“更多图形”，勾选 **阿里云 Iconfont 全部分类**。
4. 展开分类、拖入图标。默认没有文字，双击后在下方填写标签。

“更多图形”中的分类预览已内嵌到 JSON，可离线显示。旧配置若没有预览，请替换为本包中的新版阿里云分组，应用并刷新。单独查看预览可打开 `previews/alibaba-cloud.svg`。

已有自定义配置时，将阿里云 `libraries` 分组与 `defaultLibraries` 中的 `alibaba-cloud-iconfont` 合并到原配置，保留其他字段。

从旧版迁移：先删除旧阿里云 `libraries` 分组及 `defaultLibraries` 中的 `alibaba-cloud-services`，关闭旧 XML 面板或卸载旧插件，然后加载新版。已有图纸的图标不会自动换色。新版不再使用统一蓝色/蓝底白色主题或旧 19 类目录。

| 文件 | 用途 |
| --- | --- |
| `config/alibaba-cloud.json` | 原生单文件分类配置 |
| `plugins/alibaba-cloud.js` | 自托管 JS 插件，见 [PLUGIN.md](PLUGIN.md) |
| `drawio/01-cloud-infrastructure.xml` 等 | 单分类库，通过“文件 → 打开图库 → 设备”导入 |
| `drawio/all-icons.xml` | 平铺总库，一个面板，无可折叠子分类 |
| `svg/` | 以 Iconfont ID 命名的单个 SVG |
| `catalog.csv` | 分类、命名状态、色值和来源 |
| `SHA256SUMS.json` | 文件校验和 |

基础设施蓝、大数据蓝紫、AI 紫、安全绿等均来自原始 SVG，底板和留白不额外加工。分类色条仅提示主色，图标保留自身细微色差。上游 31 个未明确命名画板仍可使用；它们不是缺图服务的文字占位。

配置和插件选择一种。公共 app.diagrams.net 不接受任意 JS URL，官方文档说明桌面版不支持插件；普通用户使用 JSON 配置即可。

卸载时删除新版阿里云配置分组和 `defaultLibraries` 中对应 ID，并关闭对应面板。

请实际检查分类折叠、图标原色、搜索、空标签、下方文字编辑、连线、缩放及保存重新打开。

代码与第三方素材许可分开，参见 [NOTICE.md](NOTICE.md)、[SOURCES.md](SOURCES.md)、[COLORS.md](COLORS.md)。
