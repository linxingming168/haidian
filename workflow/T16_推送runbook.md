# T16 推送 Runbook · 百年京张AI创新带城市设计开源征集

> 适用对象：小CEO 林兴明（本地服务器：已备案域名 + GitHub 账号 `linxingming168`）
> 执行产物：本仓库 `submissions/linxingming168/luoduo-agent-city/`
> 目标仓库：`open-city-ai/haidian`（base: `main`）
> 提交截止：**2026-08-31**，建议 **2026-08-26 前**完成官方脚本自检

---

## 0. 关键提示（务必先读）

- **本沙箱无 GitHub token，无法直推 PR。** 以下所有 `git push` / 开 PR 操作必须由小CEO在**自有本地服务器**（已登录 GitHub 账号 `linxingming168`）完成。
- 本仓库已在 `E:\北京参赛\` 完成 `git init` 与首次提交（`ready_for_review` 状态）。提交包内的 16 个 `.py` 辅助脚本**已物理移出**到仓库根的 `_build/luoduo-agent-city/`（并写入 `.gitignore`），`submissions/linxingming168/luoduo-agent-city/` 目录本身已无任何 `.py`，`cp -r` 复制不会污染 fork。
- 官方复验脚本（`finalize_submission.py` / `self_check_submission.py` / `participant_preflight.py`）**只存在于 `open-city-ai/haidian` 官方仓库内**，本地参赛仓库不含这些脚本。

---

## 1. 前置：Fork 与 Clone

方式 A（GitHub 网页）：打开 `https://github.com/open-city-ai/haidian` → 右上角 **Fork** → 选择账号 `linxingming168`。

方式 B（命令行，需已 `gh auth login`）：

```bash
gh repo fork open-city-ai/haidian --clone
# 或手动 clone 你的 fork：
git clone https://github.com/linxingming168/haidian.git
cd haidian
```

---

## 2. 复制提交包到 Fork

将本仓库的整个提交包目录复制到 fork 的相同相对路径下：

```bash
# 假设本仓库在 /path/to/北京参赛，fork 在 ~/haidian
cp -r /path/to/北京参赛/submissions/linxingming168/luoduo-agent-city \
      ~/haidian/submissions/linxingming168/luoduo-agent-city
```

复制后请核对 fork 内目录含：`manifest.json`、`proposal.md`、`proposal.en.md`、`spatial.json`、`*.json`、`geometry/`、`assets/figures/`、`report/`、`visual/`、`drawings/`，**不含**任何 `.py` 辅助脚本（本包已无 `.py`，可放心 `cp -r`）。

> 提示：若仍担心误带，可改用 `rsync -a --exclude='*.py' --exclude='_build' /path/to/北京参赛/submissions/linxingming168/luoduo-agent-city/ ~/haidian/submissions/linxingming168/luoduo-agent-city/` 双重保险。

---

## 3. 在 Fork 根运行官方脚本

```bash
cd ~/haidian

# 3.1 生成/校验正式提交产物
python3 scripts/finalize_submission.py submissions/linxingming168/luoduo-agent-city

# 3.2 自检提交包一致性（manifest / sha256 / 必填项）
python3 scripts/self_check_submission.py submissions/linxingming168/luoduo-agent-city

# 3.3 参与者预检（校验 push 权限与作者身份）
python3 scripts/participant_preflight.py submissions/linxingming168/luoduo-agent-city --pr-author linxingming168 --check-push
```

---

## 4. 修复 Blocker，确认全 PASS

- 若任一脚本报 `FAIL` 或 blocker，按输出逐项修复（常见：sha256 不匹配 → 重新生成产物后跑 `patch_manifest_sha.py`；必填文件缺失 → 补产物）。
- 反复运行第 3 步，直至三条命令均显示 **PASS / OK / 无 blocker**。
- 注意：本包 `data_confidence` 为 `medium`，`known_blockers` 已声明“官方 finalize/self_check/preflight 需在本地服务器复验”——这本身不是 blocker，但 preflight 可能要求本地实际跑通后才放行 push。

---

## 5. 推送 Fork 并开 PR

```bash
cd ~/haidian
git add -A
git commit -m "feat: 落朵AI军团 百年京张AI创新带 参赛提交包 v0.1.0 (ready_for_review)"
git push -u origin main   # 若 fork 默认分支为 main；否则推到对应分支
```

然后在 GitHub 网页对 `linxingming168/haidian` 点 **Contribute / Open pull request**，目标：
- **base repository**: `open-city-ai/haidian`
- **base**: `main`
- **head**: `linxingming168/haidian:main`（或你的特性分支）

PR 标题建议：`feat: 落朵AI军团 百年京张AI创新带 参赛提交包 v0.1.0`

---

## 6. 收尾

- PR 提交后留意官方 CI / 评审留言，及时响应。
- 截止前（2026-08-31）确保 PR 处于可评审状态；建议 2026-08-26 前完成全部自检与推送，预留缓冲。
- 本沙箱侧的 `E:\北京参赛\` 仓库仅作内部版本归档，不直连 GitHub；正式提交以上述 fork + PR 为准。

---

### 附：本仓库已落地产物状态速查

- `manifest.json`：27 个文件条目，`package_state = ready_for_review`，`package_type = professional_design_package`。
- `design_depth_matrix.json`：14 项全部 `status = complete`。
- 提交 hash（内部归档）：`c26e355a2d8a06f8fc4f750c65edb4086ca9ccd4`。
