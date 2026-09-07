<!--
SPDX-FileCopyrightText: 2026 <你的名字 / Your Name>
SPDX-License-Identifier: AGPL-3.0-or-later AND CC-BY-ND-4.0
-->
# 项目名 / Project Name

> 一句话简介：这是一个 Scratch 3 (.sb3) 项目。
> A Scratch 3 (.sb3) project.

## 目录结构 / Layout

```
.
├── LICENSE                  # 总许可说明（双许可总纲，含 SPDX 表达式）
├── LICENSE-AGPLv3           # 代码许可：GNU AGPL v3（完整文本，GitHub 识别入口）
├── LICENSE-CC-BY-ND         # 素材许可：Creative Commons BY-ND 4.0（完整文本）
├── LICENSES/                # REUSE 规范目录（机器扫描用）
│   ├── AGPL-3.0.txt         #   - 与根目录 LICENSE-AGPLv3 内容一致
│   └── CC-BY-ND-4.0.txt     #   - 与根目录 LICENSE-CC-BY-ND 内容一致
├── .reuse/
│   └── dep5                 # REUSE 文件级许可归属声明（精确分流代码/素材）
├── README.md
├── project.sb3              # 打包后的 Scratch 项目（逻辑 + 素材 混合）
├── src/                     # 解包后的源代码（.json / .js 等）← AGPLv3
└── assets/                  # 素材（图片 / 造型 / 声音 / 音乐）  ← CC BY-ND 4.0
```

## Licensing / 许可协议

本仓库采用 **双许可（dual-licensing）** 方案，代码与素材分别使用不同许可证：

| 部分 / Part | 内容 / What | 许可证 / License |
|---|---|---|
| 代码 Code | `.sb3` 项目逻辑/脚本、解包后的 `.json` / `.js` 源码、构建/测试/工具脚本、文档 | **GNU AGPL v3 或更高版本** ([LICENSE-AGPLv3](./LICENSE-AGPLv3)) |
| 素材 Assets | 图片、造型(costume)、角色、背景、声音、音乐、录音、美术作品及其他媒体 | **CC BY-ND 4.0** ([LICENSE-CC-BY-ND](./LICENSE-CC-BY-ND)) |

- 法律文本（official legal code）：
  - AGPLv3: https://www.gnu.org/licenses/agpl-3.0.html
  - CC BY-ND 4.0: https://creativecommons.org/licenses/by-nd/4.0/legalcode
- SPDX 表达式：`AGPL-3.0-or-later AND CC-BY-ND-4.0`
- 文件级归属见 [`.reuse/dep5`](./.reuse/dep5)；可通过 [REUSE](https://reuse.software/) 工具做合规性 CI 扫描。

### 关于 .sb3 文件的说明

`.sb3` 是 ZIP 打包文件，内部同时包含代码（JSON）和素材（媒体文件），因此单个 `.sb3`
文件同时受到上述两个许可证约束：其中的脚本部分按 AGPLv3、媒体部分按 CC BY-ND 4.0。
建议同时发布解包后的 `src/` 与 `assets/` 目录，使许可边界清晰无歧义。

### 署名要求 / Attribution

使用或再分发本仓库内容时，请保留署名：

- 作者 / Author: `<你的名字>`
- 来源 / Source: `<你的仓库 URL>`

CC BY-ND 4.0 要求：共享时必须署名、不得修改原作品、不得基于其创作演绎作品。
AGPLv3 要求：修改后以网络服务形式提供时，须向用户提供相应源代码。

## 使用 / Usage

（在此填写如何打开、运行、修改本项目，例如用 Scratch 3 打开 `project.sb3`）

## 贡献 / Contributing

贡献的代码默认以 **AGPLv3 或更高版本** 许可。

SPDX-License-Identifier: AGPL-3.0-or-later AND CC-BY-ND-4.0
