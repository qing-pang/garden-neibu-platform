# 园林分院内务管理平台（静态站点）

本仓库是「园林分院内务管理平台」的纯静态发布版本，托管于 GitHub Pages，公网长期稳定可访问（替代原 CloudStudio 分享，后者对外分享记录已失效）。

## 访问地址
- 平台首页：https://qing-pang.github.io/garden-neibu-platform/
- 考勤及补助栏目：https://qing-pang.github.io/garden-neibu-platform/kaoqin.html

## 登录
- 账号：员工姓名全拼（见平台登录页名单）
- 密码：`123456`（纯前端登录门，仅做访问门槛，非真安全）

## 目录结构
- `index.html` —— 周例会总结栏目（各期周例会纪要 + 数据看板）
- `kaoqin.html` —— 考勤及补助栏目（考勤记录、补助计算、排名、导出）
- `data.json` —— 周例会看板数据
- `attendance.json` —— 考勤及补助数据（示例数据，待接真实钉钉数据）
- `docs/` —— 各期周例会总结 Word 成稿

## 如何更新数据（无需改代码）
1. 修改 `data.json`（周例会看板）或 `attendance.json`（考勤补助）；
2. 在本地仓库目录执行：
   ```
   git add -A
   git commit -m "更新数据 YYYYMMDD"
   git push
   ```
3. GitHub Pages 会在 1–2 分钟内自动重新构建并生效。

## 重新部署完整站点
将本目录全部内容 push 到仓库的 `main` 分支根目录即可；GitHub Pages 源已设为 `main` 分支 `/`(root)。

## 注意事项
- 本站点全部为前端静态文件，无后端；考勤补助规则写在 `kaoqin.html` 的 `RULE` 常量中，调整规则改该常量后重新 push。
- 登录门密码为前端硬编码，请勿用于敏感数据保护。
- 原 CloudStudio 链接（328e23709…app.workbuddy.host/link）已废弃，以本仓库 GitHub Pages 地址为准。
