# T16 本地 GitHub 操作指引（Windows 版）

> 适用：小CEO 林兴明 · 本地 Windows 服务器（已备案域名 + GitHub 账号 `linxingming168`）
> 目标仓库：`open-city-ai/haidian`（base: `main`）
> 提交包（已完成 v2 合规化，本地 commit `2334c16`）：`E:\北京参赛\submissions\linxingming168\luoduo-agent-city\`
> 截止：**2026-08-31**，建议 **2026-08-26 前**跑通官方脚本自检

---

## 0. 先说清楚两件事

1. **本沙箱（WorkBuddy）没有 GitHub token，不能替你 push / 开 PR。** 下面所有 `git push` 和开 PR 必须你在本机做。
2. **官方三个校验脚本（`finalize` / `self_check` / `preflight`）只存在于官方仓库 `open-city-ai/haidian` 的 `scripts/` 目录。** 你 clone 自己的 fork 后自然就有，不需要另外下载。

---

## 1. 前置准备（一次性）

### 1.1 装 Git for Windows
- 下载：https://git-scm.com/download/win ，默认安装即可。
- 装完后**用「Git Bash」**执行下面所有命令（开始菜单搜 Git Bash）。本文命令都是 Git Bash 风格。

### 1.2 配置 Git 身份（若没配过）
```bash
git config --global user.name "linxingming168"
git config --global user.email "你的GitHub注册邮箱"
```

### 1.3 准备 GitHub 访问凭证（推送必须）
GitHub 已不支持密码推送，二选一：
- **方式 A（推荐，最简单）**：安装并登录 GitHub Desktop，或用 Git 凭据管理器——首次 `git push` 时弹窗登录一次即可，之后自动记住。
- **方式 B（PAT）**：GitHub 网页 → Settings → Developer settings → Personal access tokens → 生成 token（勾 `repo` 权限）→ 推送时用 token 当密码。

### 1.4 确认 Python 可用
Git Bash 里跑：
```bash
python --version      # 或 py --version
```
若提示找不到，去 https://www.python.org/downloads/windows/ 装一个（勾「Add to PATH」）。
安装官方脚本的依赖（只需要 `self_check` 用到）：
```bash
python -m pip install shapely pyproj jsonschema
# 若 clone 后仓库根目录有 requirements-review.txt，可直接：
python -m pip install -r requirements-review.txt
```

---

## 2. Fork 官方仓库（GitHub 网页，30 秒）

1. 打开 https://github.com/open-city-ai/haidian
2. 右上角点 **Fork** → 确认目标账号是 `linxingming168` → 创建。
3. 完成后你拥有 `https://github.com/linxingming168/haidian`。

---

## 3. Clone 你的 Fork 到本机

```bash
# 选一个工作目录，例如 C:\work 或你的常用盘
cd /c/work
git clone https://github.com/linxingming168/haidian.git
cd haidian
```

此时 `haidian/` 里就有完整的 `scripts/`（含 finalize / self_check / preflight / 三个 review 脚本）。

---

## 4. 把提交包复制进 Fork（关键一步）

源（已 v2 合规、无 .py 残留）：
`E:\北京参赛\submissions\linxingming168\luoduo-agent-city\`

目标（必须严格这个路径）：
`haidian\submissions\linxingming168\luoduo-agent-city\`

在 Git Bash 里执行（注意把 `/c/work` 换成你实际 clone 的位置）：

```bash
SRC="/e/北京参赛/submissions/linxingming168/luoduo-agent-city"
DST="/c/work/haidian/submissions/linxingming168/luoduo-agent-city"
mkdir -p "$DST"
cp -r "$SRC/." "$DST/"
```

> 用 `cp -r` 即可——本包已无辅助 `.py`，不会污染 fork。若你担心误带，可改用：
> `rsync -a --exclude='*.py' "$SRC/" "$DST/"`

复制后核对（应**不含**任何 `.py`）：
```bash
ls "$DST"
# 预期含：manifest.json proposal.md proposal.en.md spatial.json *.json geometry/ assets/figures/ report/ visual/ drawings/
```

---

## 5. 跑官方脚本（在 `haidian/` 根目录执行）

### 5.1 finalize（生成/校验正式产物、重算 SHA）
```bash
cd /c/work/haidian
python scripts/finalize_submission.py submissions/linxingming168/luoduo-agent-city
```
✅ 成功表现：无报错，manifest 的 `package_state` 被置为可评审状态，SHA256 刷新。

### 5.2 self_check（贡献者预检，含几何/空间/视觉/专业深度校验）
```bash
python scripts/self_check_submission.py submissions/linxingming168/luoduo-agent-city
```
✅ 成功表现：输出各 check 为 `pass` / `ok`，无 `FAIL`、无 blocker。
⚠️ 它依赖 `shapely/pyproj/jsonschema`（第 1.4 步已装）。若报 `missing module`，回头装依赖再跑。

### 5.3 preflight（push 前工作区/范围/权限检查）
```bash
python scripts/participant_preflight.py submissions/linxingming168/luoduo-agent-city --pr-author linxingming168 --check-push
```
✅ 成功表现：workspace / scope / size / remote / submission 各项 OK；`--check-push` 会用 `git push --dry-run` 验证你对 origin 的推送权限（首次会弹窗要凭证）。

---

## 6. 遇到 FAIL / blocker 怎么办

官方深度校验比我们沙箱里的轻量检查（18/18 PASS）更严，可能点名具体问题。处理方式：

1. **把报错原文整段复制**发给我（贴到对话里）。
2. 我据此改 `E:\北京参赛\submissions\linxingming168\luoduo-agent-city\` 里的对应文件 → 你重新 `cp -r` 覆盖到 fork → 重跑第 5 步。
3. 反复到三条命令**全 PASS / OK / 无 blocker** 为止。

常见坑（提前心里有数）：
- **SHA 不匹配**：跑完 finalize 它会重写 manifest，无需手动；若你手动改了文件，重跑 finalize 即可。
- **几何/坐标报错**：我们面积按 EPSG:4548（中央经线 117°E）复算，与官方口径一致；若报精度问题，多半是属性字段，我补。
- **proposal 内容/证据断链**：professional_review 会查 source/assumption ID 是否闭合，我们已对齐，通常没问题。

---

## 7. 提交、推送、开 PR

### 7.1 提交到 fork
```bash
cd /c/work/haidian
git add submissions/linxingming168/luoduo-agent-city
git commit -m "feat: 落朵AI军团 百年京张AI创新带 参赛提交包 v0.1.0 (ready_for_review)"
git push -u origin main
```
> 若 fork 默认分支叫 `master` 而非 `main`，把 `origin main` 改成 `origin master`。

### 7.2 网页开 PR
1. 打开 https://github.com/linxingming168/haidian
2. 点 **Contribute / Open pull request**
3. base repository = `open-city-ai/haidian`，base = `main`；head = `linxingming168/haidian:main`
4. 标题：`feat: 落朵AI军团 百年京张AI创新带 参赛提交包 v0.1.0`
5. 提交，留意官方 CI / 评审留言，及时响应。

---

## 8. 收尾提醒

- 截止前（2026-08-31）确保 PR 处于可评审状态；建议 **2026-08-26 前**完成全部自检与推送，留缓冲。
- 本机 `E:\北京参赛\` 是内部版本归档（已 commit `2334c16`），不直连 GitHub；正式提交以上述 fork + PR 为准。
- 仍有两项待你拍板：**落朵真实生态授权范围（LUODUO-ECOSYSTEM-AUTH）**、**VI 主视觉**——不影响提交动作，但建议 PR 前定稿。

---

### 附：本包体量自检（避免大文件被拒）
- 单文件均 < 1 MB，整包 < 200 MB（preflight 的 `LARGE_PACKAGE_WARNING` 阈值），无超大文件风险。
- drawings/a3-booklet.pdf ≈ 0.85 MB、drawings/a0-boards.pdf ≈ 0.48 MB，均在安全线内。
