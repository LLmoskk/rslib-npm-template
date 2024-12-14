# rslib-starter

[English](README.md) | [简体中文](README_ZH.md)

一个用于使用 rslib 开发 React 组件的启动模板，具有使用 semantic-release 进行自动版本控制和发布的功能。

## 特性

- 📦 使用 [rslib](https://github.com/web-infra-dev/rslib) 构建
- 🚀 使用 semantic-release 自动发布
- 🎯 TypeScript 支持
- 📝 自动生成更新日志
- 🔄 GitHub Actions 工作流程用于 CI/CD
- 📊 GitHub Pages 文档托管

## 开始使用

### 设置令牌

此模板使用 GitHub Actions 进行自动发布。您需要设置以下令牌：

#### 1. GitHub 令牌 (GH_TOKEN)

1. [创建 Github 个人访问令牌](https://github.com/settings/tokens)
2. 点击 `Generate new token`
3. 生成具有以下权限的新令牌：
   - Actions - read and write
   - Commit statuses - read and write
   - Contents - read and write
   - Deployments - read and write
   - Issues - read and write
4. 复制令牌并将其添加到您的仓库密钥中：
   - 进入仓库设置
   - 导航到 Secrets and variables > Actions
   - 创建一个名为 `GH_TOKEN` 的新密钥

#### 2. NPM 令牌 (NPM_TOKEN)

1. 访问 [npmjs.com](https://www.npmjs.com/)
2. 导航到您的个人设置
3. 选择 "Access Tokens"
4. 创建新的访问令牌（发布权限）
5. 复制令牌并将其添加到您的仓库密钥中：
   - 进入仓库设置
   - 导航到 Secrets and variables > Actions
   - 创建一个名为 `NPM_TOKEN` 的新密钥

#### 3. 开启 GitHub Actions

1. 进入仓库设置，点击 Pages
2. 构建和部署来源：选择 GitHub Actions

## 发布流程

此模板使用 semantic-release 进行自动版本控制和发布。当更改推送到主分支时，会自动触发发布流程。

提交消息应遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

- `feat: ...` - 新功能（次要版本发布）
- `fix: ...` - 错误修复（补丁版本发布）
- `BREAKING CHANGE: ...` - 破坏性更改（主要版本发布）