# Haoran Jiang — 个人主页维护说明

[打开主页](https://kouzen-kyo.github.io/) · [发布设置](https://github.com/kouzen-KYO/kouzen-KYO.github.io/settings/pages)

在 GitHub 打开文件 → 点击铅笔编辑 → Commit changes，提交到 main 后会自动发布。通过 Actions 查看发布进度。

## 1. 修改个人照片

图片是仓库根目录的 **`portrait.jpg`**。点击 Add file → Upload files，上传同名 JPG，再 Commit changes，即可替换所有页面的头像。若换用 PNG，请同步修改六个 HTML 文件中的 `src="/portrait.jpg"`。照片按原始比例显示，不裁切脸部。

## 2. 添加 News

打开 `news.html`，搜索 `NEWS TEMPLATE`，复制下面这块，放在已有消息前面，修改日期和内容：

```html
<article class="news-item">
  <time datetime="2026-10">2026.10</time>
  <p>Your next news item.</p>
</article>
```

当前预印本消息使用你提供的文字，未添加未经提供的 arXiv 链接。

## 3. 修改 Research 内容和图片

打开 `research.html`，四个研究方向对应 `research-1` 至 `research-4`。

1. 把研究图上传到仓库根目录，例如 `research-1.jpg`。
2. 搜索 `IMAGE 1`，将紧接着的图片标签中 `src="/research-placeholder.svg"` 改为 `src="/research-1.jpg"`。
3. 同时把 `alt` 改为图片说明。其余三张图同理，搜索 `IMAGE 2`、`IMAGE 3`、`IMAGE 4`。

图片在右侧按比例完整显示；手机上排列在文字下方。添加新方向时复制完整的 `<article class="research-project">…</article>`，并使用新的唯一 id。

## 4. 修改论文 DOI

打开 `publications.html`。每篇论文下面都有：

```html
<a class="doi" href="https://doi.org/10.1016/j.partic.2026.09.001"
   target="_blank" rel="noopener noreferrer">DOI</a>
```

将 `href` 替换为对应论文的实际链接，保留 `DOI` 字样。**目前所有 25 条 DOI 都按要求指向上述同一个模板地址，并不代表已核实为对应论文的 DOI。**

## 文件对应表

| 内容 | 文件 |
| --- | --- |
| 个人介绍、教育背景、研究兴趣 | `index.html` |
| 动态 | `news.html` |
| 研究方向与图片位置 | `research.html` |
| 论文和 DOI | `publications.html` |
| 获奖、报告、学术服务 | `activities.html` |
| 简历页面 | `cv.html` |
| 下载版 CV（已去掉手机号） | `HaoranJiang_CV2026.pdf` |
| 个人照片 | `portrait.jpg` |
| 配色、字体、大小、布局 | `style.css` |

导航和个人信息侧栏直接写在六个 HTML 文件中，修改公共文字时请同步更新六个文件。照片与 CSS 是共享文件，只需替换一次。没有数据库或安装步骤；`.nojekyll` 让 GitHub Pages 直接发布静态文件。

视觉参考：[Ruidong Li 的学术主页](https://li-ruidong.com/)及其公开项目。研究、论文与个人资料来自 Haoran Jiang 提供的 CV；未使用参考作者的个人照片或研究配图。
