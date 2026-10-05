# FZU-ASC · 第一个 Pull Request

欢迎来到超级计算团队的 GitHub 协作练习！

这次任务是：**Fork 一个个人主页模板，填写自己的信息，再向本仓库提交一个 PR，分享你的主页仓库地址。** 。

## 你将练习什么

- Fork 开源项目，阅读 README 并修改配置。
- 用 Git 提交和推送自己的改动。
- 通过分支与 Pull Request（PR）参与团队协作。
- 写清楚变更，响应 Review，而不是只上传一个链接。

整个任务涉及两个不同的仓库：

| 仓库 | 用途 | 你需要做什么 |
| --- | --- | --- |
| [AcadHomepage 模板](https://github.com/RayeRen/acad-homepage.github.io) | 搭建个人主页 | Fork 到个人账号，修改个人信息并提交 |
| [FZU-ASC/PR-test](https://github.com/FZU-ASC/PR-test) | 收集任务提交，练习协作 | Fork 到个人账号，添加自己的记录，再向组织仓库发 PR |

**主页代码保留在你的主页仓库中；本仓库只接收提交记录。** 请不要把整个主页项目复制到 PR-test，也不要向模板作者的仓库提交这次作业 PR。

## 1. Fork 主页模板

1. 登录自己的 GitHub 账号，打开 [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io)，点击右上角 **Fork → Create fork**，将仓库放到个人账号下。
2. 如果希望使用 `https://你的用户名.github.io/` 作为个人主页，可以将仓库命名为 `你的用户名.github.io`。已经有同名仓库时，不要覆盖已有项目；可以保留模板仓库名，部署方式参考模板文档。
3. 阅读模板的 [中文 README](https://github.com/RayeRen/acad-homepage.github.io/blob/master/docs/README-zh.md)。使用你自己的 Fork 中的文件进行修改。

## 2. 修改成自己的信息

至少检查以下位置：

| 文件 | 修改内容 |
| --- | --- |
| `_config.yml` | `title`、`description`、`repository`；`author` 下的姓名或昵称、简介、学校/所在地、GitHub 等信息 |
| `_pages/about.md` | 自我介绍、兴趣方向、目前的学习经历或项目；删除不属于自己的论文、奖项和示例经历 |
| `images/` | 需要时替换头像，并让 `author.avatar` 指向正确文件 |

`repository` 填写实际的 `GitHub用户名/主页仓库名`。没有论文、Google Scholar 账号或研究成果完全没关系，写真实的兴趣和学习计划即可；未使用的示例链接应清空或移除。Google Scholar 引用爬虫和 Google Analytics 都是可选功能，本任务不要求配置，也不要求启用不使用的工作流。

只填写愿意公开的信息。不要上传密码、API Key、登录令牌、学号或其他不必要的个人信息。保留模板原有的许可证与致谢信息。

下面的 `YOUR_USERNAME` 和 `YOUR_HOMEPAGE_REPO` 必须换成你自己的实际值：

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_HOMEPAGE_REPO.git
cd YOUR_HOMEPAGE_REPO
# 修改文件并保存之后：
git status
git diff
git add _config.yml _pages/about.md
# 若新增或替换了头像，还需 git add 对应图片文件
git commit -m "feat: personalize my homepage"
git push
```

推送时使用 GitHub 支持的认证方式；提交署名配置不等于账号登录，HTTPS Git 操作不能直接使用账号密码。需要帮助时参考 [GitHub Git 设置指南](https://docs.github.com/en/get-started/git-basics/set-up-git)。

**部署 GitHub Pages。** 按模板 README 与 [GitHub Pages 文档](https://docs.github.com/en/pages) 配置后，打开网址，检查个人信息、图片和链接。也可以按模板说明安装 Jekyll 并使用 `bash run_server.sh` 本地预览。

## 3. 向组织仓库提交 PR

主页仓库修改完成后，再来提交记录。组织仓库的目标分支为 `main`。

### 方式 A：使用 GitHub 网页

1. 打开 [FZU-ASC/PR-test](https://github.com/FZU-ASC/PR-test)，再次点击 **Fork**，将这个仓库也 Fork 到个人账号。
2. 在你自己的 PR-test Fork 中，点击 **Add file → Create new file**。
3. 文件名填写 `members/你的GitHub用户名.md`，例如 GitHub 用户名是 `octocat`，则文件名为 `members/octocat.md`。请使用实际用户名，不要使用示例用户名。
4. 复制下方模板并填写自己的信息。提交文件时选择创建新分支，例如 `add-homepage-octocat`，不要直接改组织仓库。
5. 点击 **Contribute → Open pull request**，或在 Pull requests 页面点击 **New pull request → compare across forks**，确认：
   - **base repository**：`FZU-ASC/PR-test`
   - **base branch**：`main`
   - **head repository**：`你的GitHub用户名/PR-test`
   - **compare branch**：你刚创建的提交分支
6. 检查 **Files changed**，应只包含你自己的提交文件。PR 标题建议为 `Add homepage: 你的GitHub用户名`，正文说明改了哪些个人信息、如何检查，以及需要帮助的地方。

### 提交文件模板

在 `members/你的GitHub用户名.md` 中填写：

```markdown
# 我的个人主页

- 姓名或昵称：
- GitHub 用户名：
- 主页仓库：https://github.com/你的GitHub用户名/你的主页仓库名

## 我修改了什么

-
-
-

### 方式 B：使用本地 Git

先在网页上 Fork PR-test，再执行下面的命令。示例中的 `YOUR_USERNAME` 都需要替换为自己的实际用户名。

```bash
git clone https://github.com/YOUR_USERNAME/PR-test.git
cd PR-test
git switch -c add-homepage-YOUR_USERNAME
mkdir -p members
# 创建 members/YOUR_USERNAME.md，按上面的模板填写并保存
git add members/YOUR_USERNAME.md
git commit -m "docs: add my homepage submission"
git push -u origin add-homepage-YOUR_USERNAME
```

然后在 GitHub 网页上按方式 A 的第 5、6 步创建 PR。请确认克隆和推送的是自己的 PR-test Fork，最终 PR 的接收方是组织仓库。

## 4. 等待 Review，并在原 PR 中修改

发出 PR 后，保留 PR 地址并关注评论。如果需要修改，在原来的提交分支中继续编辑、提交和推送，**同一个 PR 会自动更新**，不必重复创建 PR。

你能打开目标为 `FZU-ASC/PR-test:main` 的 PR，并看到自己的提交文件，说明提交流程已经走通；合并由维护者 Review 后处理。

## 卡住了怎么办

- **主页还是模板作者的信息**：检查自己的 `_config.yml`、`_pages/about.md` 和提交记录；已部署时再检查部署状态与页面。
- **网页打不开**：先区分 GitHub 仓库地址和 GitHub Pages 网址，Pages 部署是可选项，且需要单独配置。
- **PR 发错地方**：重新核对 base repository 和 base branch；这次任务提交到 `FZU-ASC/PR-test`，不是模板仓库，也不是自己的主页仓库。
- **Review 要求修改**：继续推送到原 PR 的 head 分支，别另开一个 PR。
- **仍然无法解决**：带上操作系统、命令、完整报错、预期结果和已尝试的办法求助。复制信息前遮掉密钥与令牌。
