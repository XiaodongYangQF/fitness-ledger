# Fitness Training Ledger PWA v2

这是一个适合 iPhone 使用的训练记录 Web App / PWA。

## 主要功能

- 8 周训练计划
- “今天 / 计划 / 历史 / 设置”四个页面
- 每组分别记录 `kg × reps`
- 可随时新增或删除一组
- 跑步记录：距离、时间、平均心率、RPE
- 每日训练完成按钮
- 每日备注
- 体重、腰围、静息心率、当前目标
- localStorage 自动保存
- JSON 导入 / 导出备份
- PWA 离线缓存
- iPhone safe-area 和触控优化

## iPhone 使用方式

要获得最稳定的体验，建议把整个文件夹部署到 HTTPS 网站，例如 GitHub Pages。

部署后：

1. 在 iPhone 上用 Safari 打开网页网址。
2. 点击 Safari 的“分享”按钮。
3. 选择“添加到主屏幕”。
4. 主屏幕会出现 `Fitness Ledger` 图标。
5. 以后像普通 App 一样打开即可。

> iPhone Chrome 可以正常访问部署后的网址，但“添加到主屏幕”建议使用 Safari。

## GitHub Pages 最简部署

1. 新建一个 GitHub repository，例如 `fitness-ledger`.
2. 上传本文件夹中的：
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `icon.svg`
3. Repository → Settings → Pages。
4. `Build and deployment` 选择 `Deploy from a branch`。
5. Branch 选择 `main` / root。
6. GitHub 会给出一个 HTTPS 地址。
7. 用 iPhone Safari 打开该地址，再添加到主屏幕。

## 数据说明

记录保存在浏览器的 localStorage 中，因此：
- 同一个设备/浏览器会自动保留；
- iPhone 与 Mac **不会自动同步**；
- 清理浏览器网站数据可能会删除记录。

建议每周使用“导出 JSON”备份一次。

## 如果以后需要跨设备同步

下一阶段可以加入云端数据层，例如 Supabase / Firebase / 自建数据库，从而实现 iPhone 与 Mac 同步。
