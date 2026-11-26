# CYSY Spark AI Technology Club · 学生作品桌面

本仓库是 AI 兴趣社团的学生作品展示站，界面基于开源项目
[daedalOS](https://github.com/DustinBrett/daedalOS)（MIT 许可证）裁剪而成。

## 目录结构

```
.
├── out/            # 已构建好的静态网站（EdgeOne Pages 直接发布这个目录）
├── edgeone.json    # EdgeOne 配置：跳过安装/构建、输出目录、响应头
├── source/         # daedalOS 源码（修改界面或内容后在这里构建）
└── LICENSE         # daedalOS 的 MIT 许可证
```

## 为什么要把构建好的文件提交进仓库

daedalOS 的依赖约 1.3GB，EdgeOne 免费构建环境磁盘不够（会报 `ENOSPC`），
所以我们在本地构建，再提交 `out/`，由 EdgeOne 直接发布。

仓库根目录特意**不放** `package.json`，否则 EdgeOne 会误认为这是一个需要构建的 Next.js 项目。

## 更新流程

1. 在 `source/public/` 里增删内容（学生作品、文件等）。
2. 在 `source/` 目录安装依赖并构建：`yarn install` 然后 `yarn build`（需要 Node 22+）。
3. 用 `source/out/` 的内容替换根目录的 `out/`。
4. 提交并推送，EdgeOne 会自动发布。

## 已裁剪的应用

为减小体积，已移除：Quake III、Ruffle、Stable Diffusion、EmulatorJS、DX-Ball、
Space Cadet、ClassiCube、TIC-80、IRC，以及 Messenger 快捷方式。

## 安全提醒

- 不要提交 API Key、密码、Token。
- 学生作品上线前先由老师审核。
