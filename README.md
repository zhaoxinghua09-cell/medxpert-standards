# medxpert-standards · 标准官
## 许可说明 · License Notice

- **权利状态**：本仓库以 **MIT 许可** 许可发布，可依该许可证条款自由使用、修改与再分发。
- **引用建议**：引用时请标注仓库名与原文链接 `https://github.com/zhaoxinghua09-cell/medxpert-standards`
  与权利人「赵兴华 / Steven Zhao·China」。
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
© 2026 MedXpert。本包以 MIT 许可发布，按"现状"（AS IS）提供，不含任何明示或暗示担保；输出仅供方法论参考，不构成法规、法律或医疗建议。
