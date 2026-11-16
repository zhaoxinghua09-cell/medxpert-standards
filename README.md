# medxpert-standards · 标准官

> **Status: this pack is an expert/agent card, not a server — and the connector it depends on exists.**
> `medxpert-ortho-mcp` is published on PyPI and in the official MCP Registry, and a real `uvx` handshake
> returns its 8 tools. Install it:
>
> ```bash
> uvx medxpert-ortho-mcp
> ```
>
> **The version number is deliberately not written here.** It changed twice in one day; a number frozen in
> a card goes stale without anyone noticing. Ask the registry instead
> (`io.github.zhaoxinghua09-cell/medxpert-ortho-mcp`), or just run the install line above.
>
> The tools run on illustrative sample data and mark every result `sample_data: true`. Point
> `ORTHO_DATA_DIR` at your own datasets for real work, and run
> `python -m medxpert_ortho.server --validate-data` first — it fails loudly on a wrong path, a broken JSON
> file or a structurally bad dataset rather than quietly answering from the samples.
>
> This repository still ships no `server.py`: it is a card that a host loads, and the capability lives in
> the connector.
>
> **状态：本包是专家/Agent 卡片，不是服务；它所依赖的连接器已经存在。**`medxpert-ortho-mcp` 已发布在 PyPI 与官方 MCP Registry，并由真实 `uvx` 握手验证——返回 8 个工具。安装：
>
> ```bash
> uvx medxpert-ortho-mcp
> ```
>
> **版本号有意不写在这里。** 它在一天之内变了两次；冻在卡片里的数字会悄悄过期。要版本请查 Registry（`io.github.zhaoxinghua09-cell/medxpert-ortho-mcp`），或者直接跑上面的安装命令。
>
> 工具跑在示例数据上，每个返回值都标 `sample_data: true`。正式使用请把 `ORTHO_DATA_DIR` 指向你自己的数据集，并先跑 `python -m medxpert_ortho.server --validate-data`——路径错、JSON 坏、结构不合规都会报错退出，而不是拿示例悄悄作答。
>
> 本仓仍然没有 `server.py`：它是宿主加载的卡片，能力在连接器里。

## 许可说明 · License Notice

- **权利状态**：本仓库以 **MIT 许可** 许可发布，可依该许可证条款自由使用、修改与再分发。
- **引用建议**：引用时请标注仓库名与原文链接 `https://github.com/zhaoxinghua09-cell/medxpert-standards`
  与权利人：© 2026 赵兴华 / Steven Zhao (ORCID 0009-0001-0512-1237). All rights reserved.
- **品牌状态限定**：MedXpert、SynomosAI、LGD 等为相关项目标识，
  **均未申请实体注册、未申请商标注册**；出现仅作来源标识，
  不构成对法人实体或商标权的任何主张。
- **完整条款**：见仓库根目录 [LICENSE](LICENSE)。
- **联系**：zhaoxinghua06@126.com ｜ ORCID 0009-0001-0512-1237

---


医械法规标准知识库 **MedXpert-RA-Knowledge** 的导航专家包。通过 `medxpert-ortho-mcp`（标准已作为其 module 合并）查询标准/判定引擎/时间轴，强制双时态版本判定，按来源等级给话术。

## 组成
- **插件（本包）**：导航 agent `medxpert-standards` + 技能 `medxpert-standards`，负责正确地问、正确地答。
- **MCP 服务（共用 `medxpert-ortho-mcp`）**：标准能力已作为 module 并入这唯一共享连接器（与骨科检测对接同一 MCP），提供标准工具 query_standard / find_judgment_tree / get_region_path / check_timeline / report_gap(仅标记) / evolve_status / reindex，外加原检测对接工具（match_labs / calc_quote / check_udi 等）。

## 依赖
- 必须先在 MCP 配置中加入 `medxpert-ortho-mcp`（唯一共享连接器），并设置环境变量 `KB_ROOT` 指向你的 MedXpert-RA-Knowledge 知识库目录。本包通过 `dependencies.connectors` 声明该依赖。
- 本包与 `medxpert-registration-ops`（注册老炮）、`medical-device-testing-link`（检械通）共享同一知识库，标准事实以 `06-术语与标准/检测标准索引.md` 为单一事实源。

## 红线
- 禁止自动改写活库（只标记，守知识进化协议红线①）。
- 不确定的不答、自建推导不冒充官方、案例不得反推、不构成合规意见。

## 版权
代码许可 (code license) : MIT (see LICENSE)
© 2026 赵兴华 / Steven Zhao (ORCID 0009-0001-0512-1237). All rights reserved.
本包按"现状"（AS IS）提供，不含任何明示或暗示担保；输出仅供方法论参考，不构成法规、法律或医疗建议。
