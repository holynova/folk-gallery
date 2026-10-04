# 印画图鉴 · Folk & Stamp Gallery

浏览农民画、文物橡皮图章、橡皮图章与游戏印章的静态图鉴。

A static visual collection of folk paintings, artifact stamps and game-inspired prints.

[在线体验](https://folk-gallery.xiaosang.cc/) · [源码](https://github.com/holynova/folk-gallery)

![印画图鉴 · Folk & Stamp Gallery：真实页面截图](./assets/readme/screenshot.png)

## 可以做什么

- 按图鉴类别浏览图像。
- 单页HTML与本地图片即可运行，无需构建。

## 图鉴内容

321幅图像，分为农民画·节日图鉴64幅、文物橡皮图章174幅、橡皮图章70幅与游戏印章13幅。图像保存在 `images/`，页面入口是 `index.html`。

## 本地运行

```bash
python3 -m http.server 8080
```

打开 http://localhost:8080/。使用本地HTTP服务即可，无需安装前端框架。

<img src="./assets/readme/qr.png" width="144" alt="扫码打开https://folk-gallery.xiaosang.cc/">

## 发布

```bash
npx --yes wrangler@4.128.0 deploy --dry-run --config wrangler.jsonc
npx --yes wrangler@4.128.0 deploy --config wrangler.jsonc
```

从 `main` 同一提交在本地手动发布到Cloudflare Workers。正式地址：[https://folk-gallery.xiaosang.cc/](https://folk-gallery.xiaosang.cc/)。 `.assetsignore` 限定公开播放器/站点资源，排除合成工程、开发文件与未供页面使用的大体积音频/字体。
