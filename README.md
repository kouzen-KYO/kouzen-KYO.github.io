# Haoran Jiang — Personal website

Static academic homepage for GitHub Pages. The included CV has no phone number.

## 首次发布

1. 在 kouzen-KYO 账号下创建公开仓库 `kouzen-KYO.github.io`。
2. 将本文件所在目录的所有内容放到仓库根目录，确保根目录直接包含 `index.html`。
3. 打开 Settings → Pages，选择 Deploy from a branch → main → /(root)，点击 Save。
4. 等待 GitHub Pages 发布完成，访问 https://kouzen-kyo.github.io/。

## 日常维护

可以直接在 GitHub 打开对应文件，点击编辑按钮，修改后选择 Commit changes。提交到 main 后，GitHub Pages 会重新发布。

| 内容 | 文件 |
| --- | --- |
| 个人介绍、教育背景 | `index.html` |
| 研究方向 | `research.html` |
| 论文列表 | `publications.html` |
| 获奖、报告、学术服务 | `activities.html` |
| 简历页面 | `cv.html` |
| 下载版简历 | `HaoranJiang_CV2026.pdf` |
| 字体、颜色、间距及手机布局 | `style.css` |

更新 PDF 时保留文件名，网站内现有下载链接即可继续使用。替换前检查文件中是否含不希望公开的联系方式。

姓名、侧栏和导航目前分别保存在五个 HTML 文件中；修改这类共用内容时，需要同步更新五个页面。没有数据库或后台管理系统，也不需要安装依赖或运行构建命令。

`.nojekyll` 告诉 GitHub Pages 直接发布这些静态文件。网站不依赖 ChatGPT Sites。请不要把其他 Sites 项目的 `.openai` 配置或 Git 历史复制到此仓库。
