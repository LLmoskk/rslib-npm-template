# rslib-starter

[English](README.md) | [简体中文](README_ZH.md)

A starter template for developing React components with rslib, featuring automated versioning and publishing using semantic-release.

## Features

- 📦 Built with [rslib](https://github.com/web-infra-dev/rslib)
- 🚀 Automated releases with semantic-release
- 🎯 TypeScript support
- 📝 Automated changelog generation
- 🔄 GitHub Actions workflow for CI/CD
- 📊 GitHub Pages for documentation

## Getting Started

### Setting up tokens

This template uses GitHub Actions for automated releases. You'll need to set up the following tokens:

#### 1. GitHub Token (GH_TOKEN)

1. [Github Personal Access Token](https://github.com/settings/tokens)
2. Click `Generate new token`
3. Generate a new token with the following permissions:
   - Actions - read and write
   - Commit statuses - read and write
   - Contents - read and write
   - Deployments - read and write
   - Issues - read and write
4. Copy the token and add it to your repository's secrets:
   - Go to your repository settings
   - Navigate to Secrets and variables > Actions
   - Create a new secret named `GH_TOKEN`

#### 2. NPM Token (NPM_TOKEN)

1. Go to [npmjs.com](https://www.npmjs.com/)
2. Navigate to your profile settings
3. Select "Access Tokens"
4. Create a new access token (Publish)
5. Copy the token and add it to your repository's secrets:
   - Go to your repository settings
   - Navigate to Secrets and variables > Actions
   - Create a new secret named `NPM_TOKEN`


#### 3. Open GitHub Actions

1. Go to your repository Settings Click Pages
2. Build and deployment sorce: GitHub Actions

## Release Process

This template uses semantic-release for automated versioning and publishing. The release process is triggered automatically when changes are pushed to the main branch.

Commit messages should follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

- `feat: ...` - New feature (minor release)
- `fix: ...` - Bug fix (patch release)
- `BREAKING CHANGE: ...` - Breaking change (major release)
