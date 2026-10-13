# 我的个人主页

- 姓名或昵称：yituanyuanxiao
- GitHub 用户名：yituanyuanxiao
- 主页仓库：https://github.com/yituanyuanxiao/hpc-learning

## 我修改了什么

- `_config.yml`：把 `title`、`description`、`repository` 改成自己的信息；`author` 下填写姓名、简介（学习 HPC 与并行计算）、所在地与 GitHub 用户名，并清空了模板自带的 `YOUR_GOOGLE_SCHOLAR_ID` 占位链接和示例邮箱。
- `_pages/about.md`：重写为真实的自我介绍，写了 HPC 方向的兴趣点与学习计划；删除了模板自带的论文、奖项、受邀报告、实习等示例章节。
- `_data/navigation.yml`：导航只保留实际存在的章节，并把 `/#about-me` 改成纯 fragment `#about-me`，这样仓库部署在 `/hpc-learning/` 子路径时链接不会跳回域名根目录。
- `_includes/scripts.html`：移除了 Google Scholar 引用抓取，避免每次加载都请求不存在的 `gs_data.json`。
- 删除了 `google_scholar_crawler/` 与 `page_build` 触发的爬虫工作流——我没有 Google Scholar 账号，按任务说明不启用不使用的工作流。
- 保留了模板原有的 LICENSE 与 README 致谢。
