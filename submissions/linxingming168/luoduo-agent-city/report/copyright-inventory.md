---
title: "落朵智能体之城 · 逐资产版权清单"
author_agent: "落朵AI军团 · 运营版权Agent（agent.6 + 版权/授权要求）"
license: "CC-BY-4.0"
status: "concept"
source_of_truth: "proposal.md 第十四节；compliance_matrix.json agent.6；sources.json；metrics.json；geometry/*"
related_reports: ["report/ecosystem-auth.md"]
---

# 逐资产版权清单（字体 / 第三方图源 / GeoJSON / 许可范围）

> **合规边界（强制）**：本清单登记本方案各资产的版权与授权状态。原则：① 落朵生成内容按仓库许可（CC-BY-4.0）开源；② 引用第三方须署名与授权 `[charter.5]` `[charter.6]`；③ 未经授权商标/字体/图片/肖像/论文图像一律规避 `[boundary_clause.forbidden]`；④ 涉及京张铁路历史遗存仅作公共文化遗产叙事引用，不使用未授权版权素材。

## 一、字体（SimHei 嵌入授权说明）

- **使用场景**：方案正文（proposal.md / 本报告）与可视化（assets/figures/*.png、visual/index.html）中文字符显示采用 **SimHei（黑体 / 简体中文）** 作为排版字体。
- **授权性质（待核验）**：SimHei 为 Microsoft Windows 系统随附字体，其分发与**嵌入（embedding）**受微软最终用户许可协议（EULA）与字体版权约束。本方案当前以"文档显示引用"方式使用，尚未取得将 SimHei 字形**嵌入** PDF / 网页静态资源或打包分发的明确授权。
- **处置建议（非结论）**：
  1. 提交物若需打包字体，**优先替换为明确允许嵌入的开源中文字体**（如思源黑体 Source Han Sans / Noto Sans CJK，SIL Open Font License），以规避嵌入授权风险；
  2. 若保留 SimHei，仅作"系统显示依赖"声明、不嵌入二进制字形，并在 manifest/README 注明"排版字体 SimHei，随 Windows 系统提供，渲染环境需具备该字体"；
  3. 嵌入授权证明由林总（小CEO）确认后补充（见 `ecosystem-auth.md` 通用授权字段模板）。
- **状态**：`pending_embedding_license`（嵌入授权待确认）。

## 二、第三方图源

- **本方案可视化资产**：`assets/figures/site-overview.png`、`land-use-structure.png`、`key-areas.png`、`mobility-bluegreen.png`、`metrics-evidence.png` 及 `visual/index.html` 均由落朵 AI 军团基于自有机理（geometry/*.geojson 几何 + 指标复算）生成，**非外部图片素材**，不依赖第三方图源。
- **引用图片**：proposal.md 中未嵌入任何第三方摄影、地图瓦片、论文插图或商标图像。全球参考案例（proposal.md 三节 6 例）仅为文字方法论参照，未复制其图像。
- **京张铁路历史素材**：仅作公共文化遗产叙事文本引用，未使用未授权历史照片、影片或受版权保护的影像。
- **状态**：`clean`（未发现第三方图源依赖，待最终素材审计复核）。

## 三、GeoJSON 数据（provisional 来源与精度声明）

- **数据来源**：`geometry/*.geojson`（site_boundary / key_areas / land_use / buildings / roads / green_space / public_space / phasing）均基于官方 `provisional_boundaries.geojson` 与落朵 AI 军团在 provisional 边界内生成的概念几何 `[source:PROVISIONAL-BOUNDARIES]`。
- **精度与 CRS**：交换格式 EPSG:4326（WGS84 经纬度），面积/长度复算采用 EPSG:4548（高斯-克吕格，北京域）`[source:SITE-PACKAGE]`；复算由 Python 纯几何实现（高斯正算），未依赖外部商业 GIS。
- **provisional 声明（强制）**：所有边界为 `provisional_constraint`，**非官方红线**；面积置信度标记为 `medium`，官方 polygon 到位后必须重算 `[assumption:A-BOUNDARY-001]`。下列指标为 provisional 复算值，非法定规划指标：
  - `site_area_sqm = 11,412,825 m²`（≈ 1141.3 万㎡）
  - `phase1_area_sqm = 4,124,934.63 m²`（PH-1 几何声明值）
  - 各地类 / 重点区 / 建筑规模指标见 `metrics.json`（均 `medium` 置信度，部分 `low` 如 `proposed_total_floor_area_sqm`）。
- **使用限制**：几何仅供概念研究与专业团队深化参考，**不构成规划审批、土地权属或工程结论**；正式评分以官方 polygon 为准。
- **状态**：`provisional`（来源与精度已声明，待官方边界复核）。

## 四、CC-BY-4.0 适用范围与局限

- **适用范围**：本仓库由落朵 AI 军团生成的可复用内容（文本、几何、指标、矩阵、图纸、可视化）按 **CC-BY-4.0** 授权（`proposal.md` frontmatter `license: CC-BY-4.0`），允许他人在署名（署名"惠州市落朵智能科技有限公司 · 落朵AI军团"）与非额外限制前提下复制、改编、分发。
- **局限与例外（重要）**：
  1. **第三方资产不随 CC-BY-4.0 自动授权**：字体（SimHei）、任何未来引入的第三方图片/数据、商标与品牌标识，其版权归各自权利人，须单独取得授权，不因本仓库 CC-BY-4.0 而获得使用权。
  2. **生态系统权属**：落朵 9 大生态（tyb/yd/jt/cj/sj/forum_hub/登登WiFi/康养机器人等）的商标、系统与数据权属见 `ecosystem-auth.md`，其授权状态为"待核验"，不视为本仓库 CC-BY-4.0 可自由使用。
  3. **官方资料**：官方公告、任务书、场地包等受官方使用条款约束，引用须遵守其许可，不以本仓库 CC-BY-4.0 替代。
  4. **政府/文保约束**：涉及京张铁路遗存等公共文化遗产，仅作叙事引用，任何商用衍生须另行合规。
- **署名要求**：任何基于本方案的衍生作品须保留原作者署名与许可声明，并注明"概念建议，非政府审定结论"。

## 五、资产版权状态汇总

| 资产类别 | 具体资产 | 授权状态 | 备注 |
|----------|----------|----------|------|
| 文本 | proposal.md / report/*.md / 各 json | CC-BY-4.0 | 落朵生成，可署名复用 |
| 字体 | SimHei（显示引用） | 嵌入待确认 | 建议替换为 SIL OFL 字体 |
| 可视化 | assets/figures/*.png | CC-BY-4.0（自生成） | 无第三方图源 |
| 可视化 | visual/index.html | CC-BY-4.0（自生成） | 同上 |
| 几何 | geometry/*.geojson | CC-BY-4.0（provisional 数据） | 精度 medium，待官方复核 |
| 指标 | metrics.json | CC-BY-4.0 | 含 unknown 控制项待补 |
| 生态 | 9 大生态接口/商标 | 待核验 | 见 ecosystem-auth.md |
| 官方 | 公告/任务书/场地包 | 官方条款 | 不以本仓库许可替代 |

---

*落朵 AI 军团 · 运营版权 Agent · 概念机制建议 · 2026-08-10*
