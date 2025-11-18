# 🔐 图片加密解密工具 Pro

<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Web Crypto API](https://img.shields.io/badge/Web%20Crypto%20API-Enabled-green)
![QRCode.js](https://img.shields.io/badge/QRCode.js-1.0.0-orange)

**一款安全、美观、易用的纯前端图片加密解密工具**

支持 AES-GCM-256 加密 | PBKDF2 密钥派生 | 二维码生成 | 响应式 PEPC 布局

[在线演示](#) | [快速开始](#-快速开始) | [功能特性](#-功能特性) | [技术架构](#-技术架构)

</div>

---

## 📖 项目简介

**图片加密解密工具 Pro** 是一款基于现代 Web 技术开发的纯前端图片加密解密应用。本工具采用军用级 **AES-GCM-256** 加密算法，结合 **PBKDF2** 密钥派生函数（120,000 次迭代），为您的图片提供银行级安全保护。

### 🎯 核心特色

本项目基于原始的 **Text to QR Code Converter**（文本转二维码工具）进行深度开发和功能扩展，将简单的二维码生成器升级为功能完整的图片加密解密系统。

**原始功能**：
- 文本输入 → 二维码生成

**升级后功能**：
- 图片上传 → AES-GCM 加密 → Base64 文本 → 二维码生成
- 加密文本/二维码 → 输入密钥 → 解密还原图片
- 完整的加密解密生态系统

### ✨ 为什么选择本工具？

| 特性 | 说明 | 优势 |
|------|------|------|
| 🔒 **军用级加密** | AES-GCM-256 算法 | 与银行、军队使用的加密标准相同 |
| 🛡️ **防暴力破解** | PBKDF2(120K 迭代) + 随机盐值 | 即使密码泄露，暴力破解需数年时间 |
| 📱 **二维码分享** | 加密文本转二维码 | 方便手机扫码传输加密数据 |
| 💻 **完全离线** | 无服务器依赖 | 下载后可在无网环境使用 |
| 🎨 **现代设计** | 渐变+玻璃态+动画 | 流畅的用户体验和视觉享受 |
| 📐 **响应式布局** | PEPC 自适应设计 | 手机/平板/电脑完美显示 |
