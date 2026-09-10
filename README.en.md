# Alibaba Cloud Iconfont collections for draw.io

[中文](README.md) · [Sources and colors](docs/COLORS.md) · [Plugin installation](docs/PLUGIN.md)

[Download the complete package](https://github.com/jinxiao/alibaba-cloud-icons/releases/latest/download/alibaba-cloud-drawio.zip) · [Download the category configuration](https://github.com/jinxiao/alibaba-cloud-icons/releases/latest/download/alibaba-cloud.json) · [Releases](https://github.com/jinxiao/alibaba-cloud-icons/releases)

**Original categories and colors** from the Alibaba Cloud Design Center on Iconfont. Includes offline previews, native draw.io configuration, a self-contained JS plugin, XML libraries and SVG files. Icons have empty canvas labels; double-click to enter text below them. Source names remain searchable.

Snapshot 2026-09-10: **9 collections, 888 entries**, including different color versions and UI symbols. This is not a count of distinct cloud services or a claim of complete coverage of current Alibaba Cloud products.

| Collection | Entries | Main source colors |
| --- | ---: | --- |
| Cloud Infrastructure | 132 | Blue `#2B85FB` |
| Big Data | 23 | Blue-violet `#4D3CFF` |
| Security | 28 | Green `#63BA4D` |
| Artificial Intelligence | 39 | Purple `#6415FF` |
| Enterprise Applications | 38 | Deep blue `#0649D0` / `#0549D0` |
| Developer Services | 22 | Cyan `#04A2B8` |
| IoT | 21 | Orange `#FF8A00` |
| Orange Collection | 286 | Orange `#FF6A00` |
| Supplemental Icons | 299 | Original black/gray and other colors |

Every path retains its own source paint, including minor color differences. No new backgrounds or rounded tiles are added. All 31 upstream unnamed artboards remain available with explicit status labels. Product names containing “backup” are not filtered out.

## Use

Extract a generated `alibaba-cloud-drawio.zip` and open `index.html`, or build the source and open `dist/index.html`. Click **复制全部分类配置** (Copy all categories), paste into draw.io **Extras → Configuration → JSON**, apply and reload. Enable **阿里云 Iconfont 全部分类** in **More Shapes** if necessary.

For an existing configuration, merge the Alibaba `libraries` section and append `alibaba-cloud-iconfont` to `defaultLibraries`. Remove the previous project's `alibaba-cloud-services` bundle and old XML palettes first. Existing diagrams do not automatically change colors.

The previous uniform blue/orange themes and 19 product-page categories have been replaced by the 9 actual Iconfont collections. The source orange collection remains independently available.

The More Shapes entry includes an embedded SVG preview of all 9 categories. If an older installed configuration shows only text, replace its Alibaba section with the new version, apply and reload. The preview requires no network access.

- `dist/config/alibaba-cloud.json`: one file with all categories.
- `dist/plugins/alibaba-cloud.js`: plugin for self-hosted draw.io builds; see [PLUGIN.md](docs/PLUGIN.md).
- `dist/drawio/*.xml`: each file creates one palette via File → Open Library from → Device. `all-icons.xml` is flat.
- `dist/svg/`: SVG files named by upstream icon ID.
- `dist/catalog.csv`: original names, categories, colors and sources.

## Build and update

Python 3.10+, standard library only. Node.js 18+ is needed for plugin tests only.

```sh
uv run python scripts/build_libraries.py
uv run python -m unittest discover -s tests
node --test tests/test_plugin.cjs
```

The builder reads local `data/`; templates are in `src/`, tools in `scripts/`, tests in `tests/`, documentation in `docs/`. Generated `dist/` and downloaded `.cache/` are ignored by Git. Unused legacy data and product-page mappings have been removed.

```sh
uv run python scripts/sync_sources.py --refresh
uv run python scripts/prepare_catalog.py --snapshot-date YYYY-MM-DD
uv run python scripts/build_libraries.py
```

Use the actual collection date. Review publisher collection changes, counts, source names and colors before committing. New or paginated collections cause preparation to stop for review. Contributions should preserve source identity and paint. Publish the generated ZIP as a Release asset, or host `dist/` as a static gallery.

Tests cover vector/color preservation and a mock plugin host. Manually verify the blue, purple and green palettes, empty labels, label editing and save/reopen in your draw.io version.

New code is [MIT licensed](LICENSE); third-party artwork and trademarks are excluded. See [NOTICE.md](NOTICE.md).
