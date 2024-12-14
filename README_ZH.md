# rslib-starter

[English](README.md) | [简体中文](README_ZH.md)

一个用于开发 React 组件的启动模板，使用 rslib 构建，具有使用 semantic-release 的自动版本控制和发布功能。

## 特性

- 📦 使用 [rslib](https://github.com/web-infra-dev/rslib) 构建
- 🚀 使用 semantic-release 实现自动发布
- 🎯 TypeScript 支持
- 📝 自动生成更新日志
- 🔄 GitHub Actions 工作流程实现 CI/CD
- 📊 GitHub Pages 文档托管

## 开始使用

### 配置令牌

本模板使用 GitHub Actions 进行自动发布。你需要设置以下令牌：

#### 1. GitHub 令牌 (GH_TOKEN)

1. 进入你的 GitHub 账户设置
2. 导航到 开发者设置 > 个人访问令牌 > 令牌（经典）
3. 生成一个具有以下权限的新令牌：
   - `repo`（私有仓库的完全控制权）
   - `write:packages`（向 GitHub 包注册表上传包的权限）
4. 复制令牌并将其添加到你的仓库密钥中：
   - 进入仓库设置
   - 导航到 密钥和变量 > Actions
   - 创建一个名为 `GH_TOKEN` 的新密钥

#### 2. NPM 令牌 (NPM_TOKEN)

1. 访问 [npmjs.com](https://www.npmjs.com/)
2. 导航到你的个人设置
3. 选择"访问令牌"
4. 创建一个新的访问令牌（发布权限）
5. 复制令牌并将其添加到你的仓库密钥中：
   - 进入仓库设置
   - 导航到 密钥和变量 > Actions
   - 创建一个名为 `NPM_TOKEN` 的新密钥

## 发布流程

本模板使用 semantic-release 进行自动版本控制和发布。当更改推送到主分支时，发布流程会自动触发。

提交信息应遵循 [约定式提交](https://www.conventionalcommits.org/zh-hans/) 规范：

- `feat: ...` - 新功能（次要版本发布）
- `fix: ...` - 错误修复（补丁版本发布）
- `BREAKING CHANGE: ...` - 破坏性变更（主要版本发布）