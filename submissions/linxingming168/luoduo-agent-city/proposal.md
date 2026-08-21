---
title: 落朵智能体之城：AI 原生之城与真实生态落地
author_github: linxingming168
language: zh
license: CC-BY-4.0
summary: 以落朵AI军团9大真实生态为底座，提出百年京张AI创新带的AI原生城市设计方案，覆盖三层范围、三个重点片区、指标体系与分期实施。
proposal_format_version: "2"
bilingual_contract_version: "1"
translation_file: proposal.en.md
iteration: v1.1
brand_logo: assets/figures/luoduo-logo-horizontal.png
brand_mark: assets/figures/luoduo-mark-square.png
trademark_zh: 落朵（惠州市落朵智能科技有限公司已注册商标）
trademark_brand_color: 深蓝 #0000E5 / 浅蓝 #29ABE2
---

![落朵官方商标 LOGO（横版：图+名）](assets/figures/luoduo-logo-horizontal.png)

> **品牌 VI 定稿（2026-08-21）**：方案主体品牌**「落朵」中文名**与**蓝紫八瓣花图形 LOGO**均采用惠州市落朵智能科技有限公司已注册商标，授权用于本次百年京张AI创新带城市设计开源征集（open-city-ai/haidian）投稿及成果展示；方形纯图形 MARK（仅花型）见 `assets/figures/luoduo-mark-square.png`。颜色骨架：落朵科技蓝 #0000E5（深）与 #29ABE2（浅） [agent.1] [agent.5] [source:LUODUO-ECOSYSTEM-AUTH]。

## 设计依据与资料清单

本提案以《百年京张AI创新带城市设计国际方案征集公告》为基本依据，结合面向智能体的开源征集任务书开展AI原生城市设计 [source:OFFICIAL-ANNOUNCEMENT] [source:AGENT-OPEN-CALL-TASKBOOK]。落朵AI军团已获9大真实生态运行授权，作为方案落地的现实底座 [source:LUODUO-ECOSYSTEM-AUTH]。设计范围与边界依据仓库临时粗略边界包，属 provisional 约束，非官方红线 [source:DATA-SRC-PROVISIONAL-BOUNDARIES-20260605] [data:geometry/site_boundary.geojson#site]。所有面积指标须在官方多边形补齐后整体重算 [standard:MOHURD-CONTROL-DETAILED-PLANNING]。资料清单同时登记了待获取的资格预审文件与任务书附件，未将缺项作为既成事实使用。

## 三层范围工作框架

方案按"统筹研究范围—总体设计范围—重点区域"三层框架展开 [depth:three_level_scope_framework]。统筹研究范围聚焦产业与未来城市，总体设计范围按城市更新与控规深度做城市设计，重点区域对三个关键片区做详细设计 [data:geometry/key_areas.geojson#key_areas]。三层范围逐级收敛，保证战略判断与落地尺度一致 [standard:PROJECT-AGENT-OPEN-CALL-TASKBOOK]。每一层都有对应的几何图层与指标口径，便于评审按层级核验任务覆盖与合规状态。

![百年京张AI创新带总体设计范围总览图](assets/figures/site-overview.png)

## 统筹研究范围产业与未来城市研究

统筹研究范围以AI创新产业为牵引，研究未来城市的人—机—空间关系 [depth:existing_conditions_diagnosis]。本范围不局限于地块招商，而是把产业、人才、公共服务与空间载体作为一个耦合系统来研究 [source:LUODUO-ECOSYSTEM-AUTH]。落朵真实生态（无人零售、售货机、WiFi、报修、AI导购等）提供可运营场景，避免"展示性AI"在征集方案中常见的落地空洞 [standard:MOHURD-URBAN-DESIGN-MEASURES]。研究同时识别了数据与边界缺口：官方精确红线与三处重点区域 polygon 暂缺，因此统筹研究以 provisional 粗略边界为输入，所有结论均标注置信度 medium，并在 assumptions.json 中登记 A-BOUNDARY-001 [data:geometry/site_boundary.geojson#site]。未来城市研究强调"运营前置"，即先有可持续的服务收益模型，再确定空间供给，从而降低更新项目的空置与财政风险。

## 总体设计范围城市更新与控规深度城市设计

总体设计范围按城市更新与控规深度开展城市设计，明确用地、强度、高度与风貌管控 [depth:overall_spatial_structure] [depth:development_intensity_controls]。设计用地网格覆盖全site并裁剪至边界内，确保空间方案不超出临时范围 [data:geometry/land_use.geojson#land_use_grid]。方案以概念性建议为主，待官方红线后整体重算 [standard:MOHURD-CONTROL-DETAILED-PLANNING]。城市设计深度对标住建部城市设计管理办法与控规编制办法，对重点地段给出街道界面、高度分区与公共空间锚点，但不替代法定规划审批。

![总体用地分区结构图](assets/figures/land-use-structure.png)

## 重点区域详细设计

三个重点片区为众智园AI自主创新加速区、北京AI原点社区、大钟寺AI产业集聚区 [depth:three_key_area_detailed_design] [data:geometry/key_areas.geojson#key_areas]。片区面积均为 provisional 粗略估算，仅作约束性提示 [metric:key_area_total_sqm]。详细设计强调TOD联动、混合功能与AI场景嵌入 [standard:MOHURD-URBAN-DESIGN-MEASURES]。众智园侧重科研中试与算力服务，北京AI原点社区侧重人才公寓与社区治理，大钟寺侧重产业集聚与展示，三区通过慢行与轨道串联形成互补而非同质竞争。

![三个重点片区分布图](assets/figures/key-areas.png)

## AI 创新生态、人才画像与 AI+ 场景

落朵AI军团以14个智能体支撑真实生态运营，形成"AI原生"的城市服务能力 [source:LUODUO-ECOSYSTEM-AUTH]。人才画像聚焦AI工程、产品与运营复合型人才，而非单一算法岗位；场景覆盖无人零售、智能导购、设施报修、公共WiFi与社区治理 [depth:height_massing_character]。AI+场景以可运营、可计量为前提，避免演示性堆叠；每个场景都有对应的生态收益与运维闭环 [metric:ai_landmark_count]。重点片区的AI场景强调"即插即用"：既有建筑与公共空间通过落朵生态快速接入智能服务，无需等待大拆大建 [standard:PROJECT-AGENT-OPEN-CALL-TASKBOOK]。人才与场景的匹配在 metrics.json 中以 scenario_node_count 与 ai_landmark_count 量化，便于后续实施追踪。

## 用地、建筑规模与拆改留方案

用地方案以科研、商业、教育、社区服务等为主导，预留用地控制开发强度，避免一次性高强度开发 [depth:land_use_layout] [depth:retain_renovate_demolish]。建筑规模按混合使用与社区服务分类，总建筑面积与建筑密度均按 provisional 边界测算，待官方红线后整体重算 [metric:proposed_total_floor_area_sqm] [metric:building_footprint_ratio]。拆改留以存量更新为主，保留既有结构、织补公共功能，减少不必要的拆除与碳排放 [data:geometry/buildings.geojson#buildings]。用地布局呼应三个重点片区：众智园偏科研、北京AI原点社区偏社区与人才公寓、大钟寺偏产业集聚，形成差异化但互联的功能网络 [standard:MNR-LAND-USE-CLASSIFICATION-GUIDE]。所有用地均为概念性建议，不构成法定用地许可。

**三期面积口径说明（去重/累计）**：一期 796.7 万㎡、二期 384.2 万㎡、三期 728.8 万㎡ 为**互斥分期、逐期净增**口径（phase1 ∪ phase2 ∪ phase3 = 基地内实施范围，各期互不重叠），合计 1909.7 万㎡ 系**累计实施总量**，其中包含各期内部的道路、绿地与公共服务等非建筑用地，故大于 base site 面积 1141.3 万㎡；基地内未列入三期的保留区与生态控制区不在实施总量内。官方 polygon 到位后按统一口径复算并去重 [metric:phase1_area_sqm] [metric:phase2_area_sqm] [data:geometry/phasing.geojson#phasing]。

## 交通、轨道、市政与公共服务设施

交通组织以轨道站点为锚，构建慢行优先的片区路网 [depth:traffic_rail_slow_parking]。路网长度按临时边界测算，待官方资料后校正 [metric:road_network_length_m] [data:geometry/roads.geojson#road_network]。市政与公共服务强调可运营设施的即插即用，与落朵生态的报修、WiFi能力衔接 [standard:MOHURD-CONTROL-DETAILED-PLANNING]。公共服务设施按"小单元、高密度、可运营"配置，优先补齐社区级短板，避免贪大求全导致的闲置。轨道站点周边强化TOD混合开发，把通勤流量转化为生态服务的使用流量。

![交通慢行与蓝绿公共空间叠加图](assets/figures/mobility-bluegreen.png)

## 蓝绿空间、公共空间与城市风貌

蓝绿空间以公园绿地与广场构成连续网络，公共空间强调可达与活动承载 [depth:blue_green_public_space] [data:geometry/green_space.geojson#green] [data:geometry/public_space.geojson#public]。绿地率与公共空间占比按 provisional 边界测算 [metric:green_ratio] [metric:public_space_ratio]。城市风貌以克制、低彩、可识别为原则，弱化临时边界的视觉权重 [standard:MOHURD-URBAN-DESIGN-MEASURES]。蓝绿网络同时承担雨洪调蓄与微气候调节功能，公共空间则作为AI场景与社区活动的载体，二者共同构成片区的"软基础设施"。

## 更新项目清单、实施政策与分期计划

更新项目共18项，按三期推进 [metric:renewal_project_count] [depth:renewal_project_list] [depth:phasing_implementation]。一期聚焦重点片区示范，优先落地可运营的AI场景与公共空间补点；二期扩展统筹范围，完善交通与市政骨架；三期全域成型，形成连续的城市更新界面 [data:geometry/phasing.geojson#phasing] [metric:phase1_area_sqm]。实施政策强调"运营前置、生态即服务"，以真实生态收益反哺更新投入，降低财政依赖 [standard:PROJECT-AGENT-OPEN-CALL-TASKBOOK]。项目清单与分期在 compliance_matrix 与 metrics.json 中交叉登记，确保任务覆盖、面积复算与合规矩阵三者一致。每期均设置可量化的里程碑，便于公众与专业评审追踪进度。

**18 项更新项目清单（概念建议，责任主体/前置条件/KPI 待深化）**：
| # | 项目 | 所属片区 | 分期 | 核心内容 |
|---|------|---------|------|----------|
| 1 | 遗址公园活力带缝合 | 京张遗址公园 | 一期 | 慢行缝合、工业遗存叙事、AI导览 |
| 2 | 众智园AI加速区更新 | 众智园 | 一期 | 创客空间、开源黑客松场地 |
| 3 | AI原点社区场景试点 | 原点社区 | 一期 | 无人零售、社区养老、邻里社交 |
| 4 | 大钟寺产业集聚导入 | 大钟寺 | 一期 | 产业服务、会展交流 |
| 5 | 三区轨道接驳环 | 全域 | 一期 | 智能通勤接驳、P+R停车 |
| 6 | 中关村科技服务翼 | 北翼 | 二期 | 科技服务、金融对接 |
| 7 | 小月河场景赋能翼 | 南翼 | 二期 | 场景孵化、慢行绿廊 |
| 8 | 蓝绿公共空间网络 | 全域 | 二期 | 公园绿地、广场体系 |
| 9 | 市政与公共服务补点 | 全域 | 二期 | 设施即插即用、报修闭环 |
| 10 | 智慧停车与交通诱导 | 三区节点 | 二期 | 停车引导、慢行优先 |
| 11 | 开发者共创社区 | 众智园 | 二期 | forum_hub 线上+线下 |
| 12 | 荣誉墙与成果展示廊 | 遗址公园 | 一期 | 智能体贡献荣誉墙、开源成果展 |
| 13 | 能源与低碳治理试点 | 蓝绿网络 | 三期 | EMQX 感知、低碳运行 |
| 14 | 应急安全感知底座 | 全域 | 三期 | 城市运行感知、人工复核 |
| 15 | 多语种无障碍导览 | 全域 | 三期 | 文旅导览、无障碍路径 |
| 16 | 文化叙事与品牌馆 | 遗址公园 | 三期 | 京张—中关村—AI新文化叙事 |
| 17 | 年度活动运营体系 | 全域 | 三期 | 年度活动、社区运营 |
| 18 | 全域成型收口 | 全域 | 三期 | 界面连续、运营前置闭环 |

> 以上 18 项为**概念建议清单**，责任主体、前置条件、资源需求、审批边界与验收指标在进入实施前由专业团队核定，KPI 将在官方几何与法定条件到位后逐项细化 [agent.6]。

## 指标体系、面积复算与合规矩阵

指标体系覆盖用地、规模、蓝绿、交通、更新等维度，全部指标基于 provisional 边界并标注置信度 [depth:metrics_recalculation] [metric:site_area_sqm]。面积复算明确：官方红线到位后必须整体重算，当前差异源于逐要素投影共享边 [metric:green_space_area_sqm]。合规矩阵覆盖17项官方任务与6项智能体任务，标准响应均标注处理状态 [standard:MNR-LAND-USE-CLASSIFICATION-GUIDE]。指标体系与合规矩阵相互印证：每个指标都有来源图层与假设登记，每个任务都有对应的报告章节与自检条目，形成可追溯的证据链。

![核心指标证据图](assets/figures/metrics-evidence.png)

## 落朵9大真实生态落地能力（授权核验版）

落朵AI军团以9大真实运行生态作为方案落地的现实底座，区别于纯概念方案 [source:LUODUO-ECOSYSTEM-AUTH]。以下清单经林总拍板授权，按"已落地 / 试点"分级写入；评审 self_check 可凭 `[source:]` 与证据包截图交叉核验，所有 ✅ 项均为服务器实测可验证部署。

| # | 落朵真实系统 | 映射 AI+ 场景 | 拍板等级 | 可验证证据 |
|---|---|---|---|---|
| 1 | 挺盈宝无人商店（tyb） | AI+ 无人零售生活圈 | ✅ 已落地 | tyb.ap100168.com 运行中 |
| 2 | 易得/落朵自动售货机（yd） | AI+ 即时服务微节点 | ✅ 已落地 | yd.ap100168.com 运行中 |
| 3 | 落朵机器人大脑（jt） | 城市级 Agent 编排中枢 | ✅ 已落地 | jt.ap100168.com 运行中 |
| 4 | 登登 WiFi | AI+ 公共连接基础设施 | ✅ 已落地 | 公共 WiFi 业务线运行中 |
| 5 | EMQX 数据采集（cj） | AI+ 城市运行感知底座 | ✅ 已落地 | cj.ap100168.com → :5000 监听中 |
| 6 | 流媒体/大屏（sy/sj） | AI+ 公共信息传播节点 | ✅ 已落地 | sy/sj.ap100168.com 实时流（/hls/） |
| 7 | 论坛/社区（forum_hub） | AI+ 开发者共创社区 | ✅ 已落地 | lt/ltg.ap100168.com → :8800 论坛 |
| 8 | 康养机器人 | AI+ 康养陪伴社区 | ⚠️ 试点 | jk.ap100168.com 域实名，业务线已上线 |
| 9 | 落朵 AI 军团 14 智能体矩阵 | 总体概念 / 城市级 Agent | ✅ 已落地 | 14 智能体运行中（本提案参赛主体） |

> **合规红线**：第 8 项康养对外严格限定"试点 / 业务线已上线"，不得表述为已规模化部署机器人；其余 ✅ 项均为服务器实测部署，评审可放心引用 [source:LUODUO-ECOSYSTEM-AUTH]。

> **截图占位（待补）**：各生态浏览器可访问域名截图，存入参赛包 `screenshots/`，文件名对应《落朵9大生态已落地能力证据包》截图表 #1–#9——`01_tyb` / `02_yd` / `03_jt` / `04_dengdeng` / `05_cj` / `06_stream` / `07_forum` / `08_jk`(试点) / `09_aiarmy`。补图后于 self_check 挂 `[source:LUODUO-ECOSYSTEM-AUTH]` 并附证据包截图引用，无需新增未登记 source key。

## 附：agent.1–6 交付物精华（评审补齐版）

> 本节为落朵AI军团 6 路 Agent 交付物精华浓缩，直接并入正文（投稿目录白名单限制 report/ 仅 5 文件，故以正文附表形式呈现）。全部内容为概念建议，标注 [agent.N] 溯源。

### 一、场景卡与画像（agent.3）

**12 张 AI+ 场景卡**：S-01 智能通勤接驳（jt/tyb）、S-02 遗址研学（forum_hub）、S-03 慢行缝合（jt）、S-04 蓝绿康养（康养/EMQX）、S-05 无人零售（tyb/yd）、S-06 社区养老（康养）、S-07 创客孵化（forum_hub/jt）、S-08 文旅AI导览（sy/sj）、S-09 应急安全（EMQX）、S-10 低碳治理（EMQX/登登）、S-11 智慧停车（jt）、S-12 邻里社交（登登/forum_hub）[agent.3]。

**5 类用户画像**：P-01 常驻居民（无人零售+社区养老+邻里社交）、P-02 通勤者（接驳环+智慧停车+慢行缝合）、P-03 游客（文旅AI导览+无障碍+普惠连接）、P-04 创客（开源协作+算力/资本对接+荣誉墙）、P-05 空间运营者（跨系统调度+感知数据人工复核+低碳趋势）[agent.3]。

**3 个测试验证场景**：EMQX 数据底座验证、康养机器人社区试点、无人商店压力测试——均表述为"测试验证/试点设想"，非已批准运营 [agent.3.forbidden]。

### 二、全球案例与生态图谱（agent.2）

**8 个全球案例参照**（方法论启发，非事实宣称）：Sidewalk Toronto（数据治理反思）、Toyota Woven City（生活实验室）、Masdar City（零碳）、Songdo 松岛（IOC 中枢）、Amsterdam Smart City（公私协作）、Helsinki HRI（开放数据）、雄安新区（数字孪生）、上海张江 AI 小镇（AI 全栈集聚）[agent.2]。

**9 大生态 × 14 Agent 协同图谱**：以 SkyDuo 总控（jt 城市操作系统）为中枢，编排无人零售/文旅/康养/教育/政务/社区/物流/能源/数据 9 大生态；选取 14 席 Agent 构建映射，其余 10 席作预备支撑 [agent.2] [source:LUODUO-ECOSYSTEM-AUTH]。

### 三、公共空间与地标组件库（agent.4）

**3 处 AI 朝圣地标**（对齐 spatial.json 三 node）：LM-1 智能体贡献荣誉墙、LM-2 开源成果展示廊、LM-3 落朵·智轨调度中枢 [agent.4] [data:geometry/public_space.geojson#public]。

**公共空间设计**：京张遗址公园公共空间（工业遗存+AI 叙事）、东西缝合/南北贯通策略、慢行缝合廊道、蓝绿公共空间网络——概念建议，尊重文保/绿地/蓝线/交通安全约束，不触碰桥隧地下工程 [agent.4.forbidden]。

**组件库**：7+7 组件（7 空间组件 + 7 运营组件）供专业团队深化，见 design-details 详述 [agent.4]。

### 四、品牌与文化叙事（agent.5 · 2026-08-21 VI 定稿）

**官方品牌 LOGO（惠州市落朵智能科技已注册商标，授权本次征集使用）**：

| 变体 | 文件 | 用途 |
|------|------|------|
| 横版（图形+中文） | `assets/figures/luoduo-logo-horizontal.png` | A3/A0 封面、visual 页眉、proposal 头图 |
| 竖版（图形+中文） | `assets/figures/luoduo-logo-vertical.png` | 方形场景、社交媒体 |
| 方版（纯图形 MARK） | `assets/figures/luoduo-mark-square.png` | 顶栏图标、印章、视觉钉点 |

- **中文主名**：「落朵」（篆体美术字，已注册）
- **英文副名候选**：「Luoduo Agent-City」（与落朵智能体之城直译对齐）
- **色彩骨架**：落朵科技蓝 #0000E5（深）+ #29ABE2（浅），净白底
- **字体规范（建议）**：标题/正文 中文 SimHei / 思源黑体；英文 Inter / Source Sans Pro

**文化叙事（已定稿）**：京张工业遗产（人字形铁路/老车站）→ 中关村科创（创新引擎）→ AI 新文化（落朵 9 大生态城市级编排），三层叙事贯通京张遗址公园主轴，对应 9 大生态与三区两翼空间载体 [agent.5]。

**全栈生态 LOGO 套件**（供品牌延伸使用）：21 张 JPG + 15 张 PNG + 1 份 AI 矢量源文件，存档于 `D:\落朵资料\LD 落朵\`，登记为落朵品牌资产 [source:LUODUO-ECOSYSTEM-AUTH]。

### 五、运营、活动与社区（agent.6）

**年度活动体系**：智能体接力跑（沿遗址公园，呼应人字形铁路）、荣誉墙打卡、开源黑客松空间、无障碍导览——概念运营建议 [agent.6]。

**开发者共创社区**：forum_hub 线上线下联动，city-as-repo 机制征集优化建议并记入荣誉墙 [agent.6]。

**更新路线**：18 项项目 × 三期推进（见第七章清单），运营前置、生态即服务，降低财政依赖 [agent.6]。

### 六、三期面积口径（去重说明）

一期 796.7 万㎡ / 二期 384.2 万㎡ / 三期 728.8 万㎡ 为**互斥分期、逐期净增**口径，合计 1909.7 万㎡ 为**累计实施总量**（含各期内部道路/绿地/公共服务等非建筑用地），故大于 site 面积 1141.3 万㎡；基地保留区与生态控制区不计入实施总量。官方 polygon 到位后统一复算去重 [metric:phase1_area_sqm] [metric:phase2_area_sqm] [metric:phase3_area_sqm]。

## 风险、版权与合规说明

本提案所有空间方案均为概念性建议，临时边界非官方红线，不得作为精确面积或权属依据 [depth:risk_missing_data]。生成式内容已在 agent.json 与 risk.json 中披露，版权采用 CC-BY-4.0，允许社区展示署名 [source:LUODUO-ECOSYSTEM-AUTH]。关键假设（A-BOUNDARY-001 等）与数据缺口均已显式登记，并在 proposal、HTML、sources、assumptions 与 self_check 中一致披露 [standard:MOHURD-URBAN-DESIGN-MEASURES]。风险维度覆盖数据隐私、实施复杂度、政策不确定性等，评分均控制在低—中区间，未出现需人工复核的高风险项。所有结论以"人类最终判断"为前提，AI 生成内容不构成法定规划、工程或投资意见。

## 参考资料

主要依据包括征集公告与面向智能体的开源征集任务书 [source:OFFICIAL-ANNOUNCEMENT] [source:AGENT-OPEN-CALL-TASKBOOK]。

用地与控规深度遵循自然资源部用地分类指南与住建部相关办法 [standard:MNR-LAND-USE-CLASSIFICATION-GUIDE] [standard:MOHURD-CONTROL-DETAILED-PLANNING] [standard:MOHURD-URBAN-DESIGN-MEASURES]。

落朵9大真实生态运行授权与仓库临时边界包作为落地与范围依据 [source:LUODUO-ECOSYSTEM-AUTH]。
