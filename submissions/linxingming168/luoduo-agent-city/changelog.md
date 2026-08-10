# 变更日志 / Changelog

> 本文件记录落朵智能体之城方案的修复与交付变更。格式：日期 / 变更 / 影响。

## 2026-08-10 · 运营版权 Agent（agent.6）交付补齐

- **执行 Agent**：运营版权 Agent（对应官方 agent.6 + 版权/授权要求），受总指挥公狼派遣。
- **变更**：
  - 新增 `report/annual-activities.md`：年度活动机制（赛事/论坛/开放日/黑客松/双年展），含年度节奏与招商价值（机制化，未写为政府/政策承诺）。
  - 新增 `report/dev-community.md`：开发者社区运营机制 + 招引转化路径（参赛者→贡献者→企业→落地）。
  - 新增 `report/update-roadmap.md`：18 项更新项目逐项清单（编号/内容/KPI/停止条件）；并说明三期面积 796.7/384.2/728.8 万㎡ 与 site 1141.3 万㎡ 的去重/重叠关系（三期非互斥切片，重叠≥768.4 万㎡；与 geometry/phasing.geojson 仅 PH-1=412.49 万㎡ 的口径差异待复核）。
  - 新增 `report/copyright-inventory.md`：逐资产版权清单（SimHei 嵌入授权待确认、第三方图源清洁、GeoJSON provisional 来源与精度声明、CC-BY-4.0 适用范围与局限）。
  - 新增 `report/ecosystem-auth.md`：9 大生态授权（LUODUO-ECOSYSTEM-AUTH）状态表，全部标记为「待核验（pending verification）」，并给出林总需填写的核验模板/字段。
  - 更新 `agent.json`：新增 `deliverables` 数组，登记上述 5 个交付物引用（保留原有全部字段）。
  - 更新 `compliance_matrix.json`：保留 23 个 requirement_id（含 agent.1–agent.6），为每项补充 `status` 与 `evidence`；本次补齐项 agent.6 标记 `satisfied`、1.5.2.2 标记 `partial`，evidence 引用到 `report/*.md`。
- **影响**：
  - agent.6（全球活动与长期运营）由提案级概念补全为可执行的年度活动 + 社区运营 + 更新路线图 + 版权/授权机制，合规红线（agent.6.forbidden）全程规避。
  - 9 大生态授权与 SimHei 嵌入授权、第三方图源等版权风险点被显式登记为「待核验」，降低提交物合规风险；待林总回填授权证明后，可将 agent.6 / agent.2 相关 evidence 由「待核验」升级为「已核验」。
  - 未修改 `proposal.md` / `spatial.json` / `metrics.json` / `manifest.json`，与既有指标口径保持一致（update-roadmap 已注明 renewal_project_count 12 vs 18 的层级差异待归并）。
- **待办（依赖林总）**：回填 `report/ecosystem-auth.md` 核验模板；确认 SimHei 嵌入授权或替换为 SIL OFL 字体；补充 geometry/phasing.geojson 的 PH-2、PH-3 以重算三期去重面积。
