# 方案迭代记录

## v1.0 - 2026-08-09

- 基于落朵 AI 军团草案与官方 provisional 边界，重建 formal 参赛包：重建 geometry（9 个 GeoJSON，覆盖 site 全 bbox、裁剪至边界、对齐 layer 枚举）、重算 34 项 metrics、生成 compliance/standard/design_depth 三矩阵（0 error）。
- 生成 proposal.md（中英双语，13 章节，5 嵌入图，每节证据引用）与 proposal.en.md；生成 5 张 PNG、2 个 A3/A0 PDF 图纸及各自 .en 副本；生成 report/proposal.html（中英）与 visual/index.html（中英，14 文本标记 + data-metric 一致）。
- finalize 至 ready_for_review；self_check 四关复核（确定性/空间/可视化/专业）。
- 已知开放问题：官方精确红线与三处重点区域 polygon 暂缺，所有面积指标为 provisional 概念性测算，官方多边形补齐后须整体重算。

## v1.1 - 2026-08-21

- 品牌 VI 定稿：落朵中文名 + 蓝紫八瓣花 LOGO（惠州市落朵智能科技已注册商标）授权用于本次征集；assets 补充横版/竖版/方版 LOGO 及 .en 副本。
- 落朵 9 大真实生态证据体系成形，写入 proposal 正文与 E1–E11 证据附录；sources.json 登记 LUODUO-ECOSYSTEM-AUTH 运行授权。

## v1.2 - 2026-08-26（评审阻断项修复）

- 移除投稿根目录自定义 evidence_manifest.json（评审要求证据并入既有结构化文件或移至允许的 assets/ 路径）；manifest.json 将未定义 role `evidence` 改为 schema 允许的 `evidence_data`。
- 上述修复使 `submission-validation` CI 由失败转为通过（08-28 本地 Gate 四关全 PASS）。

## v1.3 - 2026-08-28（回应 AI 评审 55/100）

- 针对七维加权 55/100、19 项 required repairs 的逐维修复已规划（见 PR 评论与 REVIEW_RESPONSE.md）：风险合规与可实施性维度优先闭环。

## v1.4 - 2026-08-31（风险合规与可实施性收口）

- 风险合规维度：脱敏 proposal 正文 SSH 用户名/公网 IP/内网端口/进程拓扑（E1–E11 附录）；登记此前未登记的 source `LUODUO-COMPUTE-LANDING`（算力核验方法与“参与者自述·样机级”限定）；将“评审可放心引用/直接证明/verified”等绝对措辞改为与证据等级一致的状态；登记 8 个全球案例来源 `GLOBAL-SMART-CITY-CASES`（方法论启发，非事实宣称）。
- 可实施性维度：修正三期面积“互斥分期、逐期净增”与“累计实施总量大于基地净用地”的语义矛盾，明确为“三期累计实施覆盖口径（各期含道路/绿地/公共服务等非建筑用地）”，公式/GeoJSON/metrics/正文/图件统一同一可复算口径。
- self_check 时间戳刷新至 2026-08-31；manifest 各改动文件 sha256 同步刷新。
- 表达完整度（空白核心指标图/地图文字重叠/中文缺字）与 12 项场景卡深化、区域协同、跨域AI规划机制图等深度项，受限于截止期与专业设计/渲染管线，列为后续条件触发项，待官方 polygon 与控规到位后由专业团队深化。
