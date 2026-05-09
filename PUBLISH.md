# 发布步骤（一次性操作）

## 1. 在 GitHub 上创建 Profile 仓库

> 仓库名必须与用户名完全一致：`LS-plan/LS-plan`，**Public**，**勾选 "Add a README file"** 之外其他不勾。
> 如果已经有同名仓库，跳过这一步。

打开： <https://github.com/new>
- Repository name: `LS-plan`
- Description: `Profile README`
- Public
- 不要初始化 README / .gitignore / license（我们已经准备好）
- 创建

## 2. 把本地内容推上去

在当前目录（`D:\Documents\data\TerminialBase\LS-plan-profile`）执行：

```bash
git init
git add .
git commit -m "feat: 初始化 Profile README 与贡献蛇形图工作流"
git branch -M main
git remote add origin https://github.com/LS-plan/LS-plan.git
git push -u origin main
```

## 3. 触发一次蛇形图生成

推送后，打开仓库 → Actions → 选择 **Generate Snake** → **Run workflow** → 选 `main` 分支运行。
首次运行会创建 `output` 分支并生成 `github-contribution-grid-snake.svg`，README 中的引用即可生效。

如果首次运行报权限错误，去 仓库 Settings → Actions → General → **Workflow permissions** → 选 **Read and write permissions** → 保存，再重跑。

## 4. 后续仓库治理（低风险）

不删除、不归档任何仓库，只做轻量优化：

为下面 4 个仓库分别补 description 与 topics（在仓库主页右上 ⚙️）：

| 仓库 | 建议 description | 建议 topics |
| --- | --- | --- |
| `ls-plan.github.io` | 个人主页与博客 | `personal-website` `blog` `github-pages` |
| `any-coder` | AI 编程助手相关实验 | `ai-agent` `ai-tools` `cli` |
| `elecmon` | 电子/电力监测原型 | `electronics` `monitoring` `dashboard` |
| `FBTI` | 数据可视化页面原型 | `visualization` `frontend` `prototype` |

## 5. 设置首页置顶仓库

GitHub 主页 → Customize your pins → 选 6 个：

1. `ls-plan.github.io`
2. `any-coder`
3. `elecmon`
4. `FBTI`
5. `LaTeX-Thesis-Writing` （体现学术工具链）
6. `AI-Session-Viewer` （AI 工具方向，即使是 fork 也有展示价值）

## 6. 可选：补充 bio 与 location

GitHub Settings → Profile：
- Name: `ShuyuS`
- Bio: `PhD @ BUPT · AI Agent / AI Tools / AI4S · 通信电子背景`
- Location: `Beijing, China`
- Website: `https://ls-plan.github.io`

---

## 后续维护

- 修改 README 直接编辑 `LS-plan/LS-plan` 仓库的 `README.md` 并 push
- 蛇形图无需人工维护，每天自动刷新
- 当出现新代表项目时，回到 `## 🚀 代表项目` 区块替换或追加
