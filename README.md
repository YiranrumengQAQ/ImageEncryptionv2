# 🔐 图片加密解密工具 (Image Encryption v2)

> 一个基于现代 Web 技术构建的安全、美观、纯本地运行的图片/文件加密工具。

[在线演示](https://Yiranrumengqaq.github.io/ImageEncryptionv2/)

## 📖 项目介绍

本项目是一个轻量级的网页版图片加密工具，采用了 **Picocrypt** 的视觉风格。它允许用户在浏览器端直接对图片进行高强度的加密和解密，而无需将文件上传到任何服务器。

核心理念是 **"数据不离本地，隐私绝对安全"**。所有的加密运算均利用浏览器的 Web Crypto API 和 JavaScript 在用户的设备上完成。

## ✨ 核心功能

* **🛡️ 军工级加密**：使用 **XChaCha20-Poly1305** 算法进行加密。
* **🚫 零服务器交互**：纯前端实现，无后端数据库，杜绝隐私泄露风险。
* **💻 现代化 UI**：清新简洁的蓝色渐变主题，响应式设计，支持夜间模式。
* **⚡ 极速体验**：加密/解密瞬间完成并自动触发下载。
* **👁️ 可视化反馈**：提供清晰的状态预览与动画交互。

## 🔧 技术栈

* **核心语言**：HTML5, CSS3, JavaScript (ES6+)
* **加密库**：
    * [`@stablelib/xchacha20poly1305`](https://www.npmjs.com/package/@stablelib/xchacha20poly1305)
    * [`@stablelib/random`](https://www.npmjs.com/package/@stablelib/random)

## 🔐 加密原理详情

本工具生成的加密文件结构严谨，具体参数如下：

* **Salt (盐值)**：每次加密生成 **32 字节**随机盐，防止彩虹表攻击。
* **Key Derivation (密钥派生)**：使用用户密码和盐值，通过 **PBKDF2-HMAC-SHA256** 迭代 **100,000 次**生成 256 位密钥。
* **Nonce (随机数)**：生成 **24 字节**随机数，用于 XChaCha20 算法。
* **Encryption (加密)**：使用生成的密钥和 Nonce，对文件二进制数据进行 **XChaCha20-Poly1305** 加密。

## 🚀 快速开始

### 在线使用
直接访问部署地址：[https://Yiranrumengqaq.github.io/ImageEncryptionv2/](https://Yiranrumengqaq.github.io/ImageEncryptionv2/)

### 本地运行
1.  克隆或下载本项目。
2.  直接双击打开 `index.html` 文件即可使用。
3.  **注意**：首次加载需要互联网连接以获取 CDN 上的加密库资源。

## 🌐 离线使用说明

当前版本默认使用 CDN 加载加密库。如果您需要在**无网络环境（局域网/内网）**下使用，请按照以下步骤操作：

1.  下载代码中引入的两个 JS 库文件（ESM 版本）：
    * `@stablelib/xchacha20poly1305`
    * `@stablelib/random`
2.  将这两个 `.js` 文件保存到项目本地文件夹中（例如 `lib/` 目录）。
3.  修改 `index.html` 底部的 `<script type="module">` 引用路径：
    ```javascript
    // 将 CDN 链接修改为本地相对路径
    import { XChaCha20Poly1305 } from './lib/xchacha20poly1305.js';
    import { randomBytes } from './lib/random.js';
    ```
4.  修改后即可在完全断网的环境下运行。

## 📝 使用指南

### 加密图片
1.  切换到 **"🔒 加密图片"** 标签页。
2.  点击选择文件或拍照。
3.  设置一个强密码（至少6位）。
4.  点击 **"加密并下载"**，保存 `.encrypted` 文件。

### 解密图片
1.  切换到 **"🔓 解密图片"** 标签页。
2.  选择之前下载的 `.encrypted` 文件。
3.  输入加密时设置的密码。
4.  点击 **"解密并下载"** 恢复原图。

## ⚠️ 注意事项

1.  **请务必牢记您的密码！** 由于采用对称加密且无服务器存储，一旦密码丢失，文件将**无法找回**。
2.  本工具虽然主要用于图片，但实际上支持对任何格式的小型文件进行加密。

---
*Created by Yiranrumengqaq*
