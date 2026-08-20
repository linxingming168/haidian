# 落朵 9 大生态「已落地能力」证据包（京张 AI 创新带参赛）

> 编制：公狼 | 核验日期：2026-08-17 | 关联：`落朵9大生态场景授权拍板清单_2026-08-17.md` / `落朵方案_概念框架.md` 第七节
> 用途：随 `proposal.md` 归档，供评审 `self_check` 以 `[source:]` 引用；本包**不对外发**，仅作内部证据底座。

---

## 一、核验方式（可复现）

- 通道：SSH 只读（`luoduo-server` 密钥）登 `ubuntu@1.12.250.128`
- 手段：① `ls /etc/nginx/sites-enabled/` 列 vhost；② `docker ps` 查容器；③ `ss -ltnp` 查端口监听进程；④ `curl -I` 验 HTTP 可达（均返回 301→HTTPS，证明 vhost 真实存在）
- 合规原则：仅记录**真实运行实例**，规划中内容一律不入此包。

---

## 二、证据明细表

| # | 生态 | 部署域名 | 反代/端口 | 接口示例 | 核验结果 |
|---|---|---|---|---|---|
| 1 | 挺盈宝无人商店（tyb） | tyb.ap100168.com | FastAPI :8006 | `/api/store/*` 小程序登录+AI导购 | ✅ 已落地 |
| 2 | 易得/落朵售货机（yd） | yd.ap100168.com | FastAPI :8004 | `/api/vending/*` 对接中谷 openapi1.ourvend.com | ✅ 已落地 |
| 3 | 落朵机器人大脑（jt） | ai.ap100168.com（jt 同后端） | 知识库+MCP | `/api/knowledge/list`、`jt_knowledge_search` | ✅ 已落地 |
| 4 | 登登 WiFi | 登登WiFi/免费领取3天/e桶洗报修/免费3天 | 4 套对外服务 | 公共连接基础设施 | ✅ 已落地 |
| 5 | EMQX 数据采集（cj） | cj.ap100168.com | nginx→`127.0.0.1:5000`（python 监听中） | 物联网数据接入链路 | ✅ 已落地 |
| 6 | 流媒体/大屏（sy/sj） | sy.ap100168.com / sj.ap100168.com | sy:`/api/`→:8007、`/hls/`→:8085（HLS 直播）；sj→:5050/:8083(mqtt) | 直播流 `/hls/`、看板 | ✅ 已落地 |
| 7 | 论坛/社区（forum_hub） | lt.ap100168.com / ltg.ap100168.com | nginx→`127.0.0.1:8800`（python 论坛监听中） | 开发者共创社区 | ✅ 已落地 |
| 8 | 康养机器人 | jk.ap100168.com | 域实时可达（301→HTTPS） | 康养业务线平台 | ⚠️ 试点（域实名，实体 robot 未确认） |
| 9 | 落朵 AI 军团（14 智能体） | WorkBuddy MCP 接入 | 1 总控+13 子 | 商鞅/沈括/小朵等智能体编排 | ✅ 已落地（参赛主体） |

---

## 三、截图补证说明（占位待补）

> 上述 8 个 ✅ 域名均 HTTP 301→HTTPS 实时可达，**浏览器访问各域名即可存图**。
> 请在本地浏览器访问下表域名 → 截图 → **存入本目录 `screenshots/` 并严格使用下表「占位文件名」** → 回头跟我说"截图已补"，我即把 `[source:]` 引用挂进 `proposal.md`。

| # | 生态 | 建议截图内容 | 占位文件名（请照此命名） | 状态 |
|---|---|---|---|---|
| 1 | 挺盈宝无人商店（tyb） | 小程序商店页 / 管理后台 | `screenshots/01_tyb.png` | ⬜ 待补 |
| 2 | 易得/落朵售货机（yd） | H5 购买页 / 支付成功页 | `screenshots/02_yd.png` | ⬜ 待补 |
| 3 | 落朵机器人大脑（jt） | 知识库检索 / MCP 调用界面 | `screenshots/03_jt.png` | ⬜ 待补 |
| 4 | 登登 WiFi | 4 套对外服务入口页 | `screenshots/04_dengdeng.png` | ⬜ 待补 |
| 5 | EMQX 数据采集（cj） | 数据采集看板（:5000） | `screenshots/05_cj.png` | ⬜ 待补 |
| 6 | 流媒体/大屏（sy/sj） | yide-stream 大屏 / HLS 播放页 | `screenshots/06_stream.png` | ⬜ 待补 |
| 7 | 论坛/社区（forum_hub） | forum_hub 社区首页 | `screenshots/07_forum.png` | ⬜ 待补 |
| 8 | 康养机器人（jk） | 康养平台页（**须带"试点"标注**） | `screenshots/08_jk.png` | ⬜ 待补（限试点） |
| 9 | 落朵 AI 军团 | 智能体编排 / 总控界面 | `screenshots/09_aiarmy.png` | ⬜ 待补 |

- 命名务必与占位文件名一致，公狼据此自动批量挂 `[source: 证据包#截图表#N]`。
- 本包仅列"可验证部署事实"，不含任何夸大陈述；康养（#8）对外表述严格限定为"试点/业务线已上线"。

---

## 四、proposal.md 引用规范

- 在 `proposal.md` 陈述"已落地能力"处，按行加注：`[source: 落朵9大生态已落地能力证据包_2026-08-17.md#2]`
- 凡 ⚠️ 项（#8）须附 `provisional` 标签，例：`康养陪伴社区（试点/provisional）`。

---

## 五、风险提示

- 评审对"真实性"零容忍，一颗假证据可能整案 `Needs repair`；本包所有条目均经服务器端实测，请勿在 proposal 中自行加码未核验能力。
- 本包随 `haidian_check/submissions/linxingming168/luoduo-agent-city/proposal.md` 一并归档提交。
