# 行程 · 杭州 / 澳门 / 东京 / 香港

2026 年 12 月 5–20 日行程网页，2 人（Edwyn + 大莉）。

- 杭州：12 月 5–7 日，住万象城附近，12 月 7 日 12:05 飞深圳
- 澳门：12 月 9–11 日，住 YOHO 荷里活罗斯福酒店 2 晚，12 月 11 日 09:30 飞东京
- 东京：12 月 11–19 日，住 Tora Hotel 池袋 11–17 日 6 晚，17–19 日酒店未定；富士山主选 12 月 14 日
- 香港：12 月 19–20 日，住木的地酒店豪华特大床房 1 晚（原价 AUD 530，已订），12 月 20 日晚高铁回深圳

## 怎么看

直接打开 `index.html` 就能看；图片以 base64 文本存在 `assets_b64/` 里，页面滚动到哪张图就加载哪张，GitHub Pages 上可正常显示。

在线版用 GitHub Pages：https://edwynl.github.io/trip-xmax/

## 为什么图片是 .b64 文本文件

GitHub 的推送工具只接受 UTF-8 文本文件，不能直接推 JPG/WebP 二进制，所以图片先转成 base64 文本（`assets_b64/*.b64`，解码后和原图完全一致），`index.html` 里用一小段脚本在图片进入视口时取回还原。`.nojekyll` 是为了让 GitHub Pages 原样提供所有文件，不经过 Jekyll 处理。

## 部署说明

- 这是纯静态网页，没有后端，不用构建，直接部署 `index.html` + `assets/` 即可。
- GitHub Pages：仓库 Settings → Pages → Deploy from a branch → main / root。
- Vercel 也可以部署这个仓库，但在国内访问 `vercel.app` 经常需要 VPN，大莉在国内建议优先用 GitHub Pages 或直接发 `index.html` 文件用手机浏览器打开。
