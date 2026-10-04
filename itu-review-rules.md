<!--
  本文件由 ITU 专家（standards-participation-officer）维护。
  它是 lgd-itu-review.yml 加载的「ITU 专项规则集」，决定 ITU 仓 PR 的专项审阅口径。
  修改须 ITU 专家定稿；版本化记录在此文件顶部。
  版本：v1.1 · 2026-10-05 红队轮扩面
-->

# ITU 专项审核规则集（v1.1）

> 维护者：ITU 专家 `standards-participation-officer`
> 作用：被 `lgd-itu-review.yml` 注入为 AI 审阅的 system 上下文；并触发「递交纪律」硬检查。

## 1. 术语与引用格式

- ITU-T 建议书引用须为标准格式：`ITU-T Rec. X.xxx`（或 `Y.xxx` / `Z.xxx` 按系列）。
- FG-TIDA（Focus Group on AI for Autonomous and Assisted Driving）相关主题须标注所属 FG 与议题编号。
- 不使用未定义缩写；首次出现给出全称。

## 2. 标准参编合规勾稽

- 贡献须定位为「议题（issue/contribution）」而非「我方出版物投稿」——出版物留自有仓/Zenodo/官网。
- 跨参考（cross-reference）到自有出版物时，仅一行中性指引外链真源，**不在流程仓正文搬运整块**。

## 3. 递交纪律（机器自动执行，见 lgd-itu-review.yml）

以下模式命中即标红、禁止出门（2026-10-02 全机禁令 + 红队轮 v1.1 扩面）：

- 内部流程注释：`<!-- 示例注释 -->`、英文 `<!-- internal -->` / `<!-- draft -->`、`须过 xx 机器闸`、专家终审日期等；
- 品牌块 / 权属宣告块：`SynomosAI` / `MedXpert` 正文品牌块，以及裸权利宣告 `Copyright` / `All rights reserved` / `版权所有` / `权利声明` / `©`（无品牌名也拦）；
- 身份信号：`ORCID`（含 `0000-xxxx-xxxx-xxx` 形态）；
- 出版物锚：`canonical pin` / `canonical:` / `Zenodo DOI` / `10.5281/zenodo.xxx` / `doi.org/10.5281/...`。

## 4. 评审关注点（供 AI 审阅）

- 技术论点是否清晰、可被第三方独立复核（北极星 B1）；
- 是否暴露不可逆权利风险（专利窗口/署名）——有则提示维护者；
- 是否与既有 ITU 讨论脉络一致，避免重复/冲突提案。

---

## 修订记录

- v1.0 (2026-10-05)：初版。术语格式 + 合规勾稽 + 递交纪律硬检查 + 评审关注点。
- v1.1 (2026-10-05)：红队轮扩面。硬检查正则加 ORCID / 裸权利宣告(©/Copyright/版权所有) / DOI-URL(10.5281/zenodo) / 英文/草稿注释；secret-scan 支持 push 与 ghp_/AKIA/PEM 形态；L1/L2 未配 BYOK 时显式告警而非静默绿勾；issue_comment 重跑改用 issue.number。
