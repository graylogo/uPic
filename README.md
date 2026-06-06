<div align="right"><strong>🇨🇳中文</strong>  | <strong><a href="./README-en.md">🇬🇧English</a></strong></div>
<div align="center">
  <img src="https://raw.githubusercontent.com/gee1k/oss/master/screenshot/uPic/logo.png" alt="uPic">
  <br>
  <br>
  <p>
    Picture and file upload tool for macOS. - A native, powerful, beautiful and simple
  </p>

  <p>

  [![Travis Build Status](https://img.shields.io/travis/gee1k/uPic.svg?style=flat-square&logo=Travis)](https://travis-ci.org/gee1k/uPic) [![MIT](https://img.shields.io/github/license/gee1k/uPic?style=flat-square)](https://github.com/gee1k/uPic/blob/master/LICENSE)

[![Donate on PayPal](https://img.shields.io/badge/support-PayPal-blue?style=flat-square&logo=PayPal)](https://paypal.me/geeee1k) [![Chat on Telegram](https://img.shields.io/badge/chat-Telegram-blueviolet?style=flat-square&logo=Telegram)](https://t.me/upic_host) [![Follow My Twitter](https://img.shields.io/badge/follow-Tweet-blue?style=flat-square&logo=Twitter)](https://twitter.com/realSvend) [![Follow My Twitter](https://img.shields.io/badge/follow-Weibo-red?style=flat-square&logo=sina-weibo)](https://weibo.com/643660358)

  </p>
</div>

---

## 🔧 Fork 版本说明

> ⚠️ **此为 graylogo 的 Fork 版本，专门适配 macOS 26 和 Xcode 26**

### ✨ 本版本更新内容

**v1.4.8-macOS26** (2024-06-06)

#### 核心兼容性升级

1. **WCDB 数据库升级**
   - 升级 WCDB 从 2.1.9 到 **2.1.16**
   - 修复 Swift 6 编译兼容性问题
   - 修复 C++ 标准库的特殊化错误

2. **移除不兼容的 libminipng 框架**
   - 移除预编译的 libminipng.framework（与 Swift 6 不兼容）
   - 改用 macOS 原生 `NSBitmapImageRep` 进行 PNG 图片压缩
   - 保持原有的图片压缩功能不变

3. **Xcode 26 适配**
   - 更新 entitlements 文件配置
   - 最低系统要求提升至 **macOS 13**
   - 优化 Swift 6 编译设置

#### 🔄 与上游版本差异

- 基于原作者 v0.21.1 之后的最新代码
- 包含原作者的所有功能更新
- 专注于 macOS 26/Xcode 26 兼容性修复

#### ⚠️ 系统要求

- **最低**: macOS 13 (Ventura) 或更高版本
- **推荐**: macOS 14 (Sonoma) 或 macOS 26
- **Xcode**: Xcode 15+ (推荐 Xcode 26)

#### 📥 安装方式

**方式一：编译安装**
```bash
# 克隆此仓库
git clone https://github.com/graylogo/uPic.git
cd uPic

# 编译 Release 版本
xcodebuild -project uPic.xcodeproj -scheme "uPic(Release)" -configuration Release build

# 应用将生成在
# ./build/Build/Products/Release/uPic.app
```

**方式二：命令行安装**
```bash
# 编译后复制到应用程序文件夹
cp -R ./build/Build/Products/Release/uPic.app /Applications/

# 启动应用
open -a uPic
```

#### 🔄 保持与上游同步

此 Fork 会定期从原作者仓库同步更新：

```bash
# 添加上游仓库（如果还没有）
git remote add upstream https://github.com/gee1k/uPic.git

# 同步上游更新
git fetch upstream
git merge upstream/master
git push origin master
```

#### 📚 相关资源

- **原作者仓库**: [gee1k/uPic](https://github.com/gee1k/uPic)
- **此 Fork 仓库**: [graylogo/uPic](https://github.com/graylogo/uPic)
- **详细使用指南**: [FORK_GUIDE.md](./FORK_GUIDE.md)

---

**👬联系： _[Telegram](https://t.me/upic_host), [Twitter](https://twitter.com/realSvend), [微博](https://weibo.com/643660358)_**

**☕️赞助： _[Paypal](https://paypal.me/geeee1k), [支付宝](https://raw.githubusercontent.com/gee1k/oss/master/qrcode/alipay.JPG), [微信支付](https://raw.githubusercontent.com/gee1k/oss/master/qrcode/wechat_pay.JPG)_**

**📱uPic for iOS: [![uPic for iOS](https://cdn.jsdelivr.net/gh/gee1k/oss@master/uPic/app-store-black.svg)](https://apps.apple.com/us/app/id1510718678)**

## 📑 简介

> **uPic(upload Picture) 是一款 Mac 端的图床(文件)上传客户端**

**💡 特点：** 无论是本地文件、或者屏幕截图都可自动上传，菜单栏显示实时上传进度。上传完成后文件链接自动复制到剪切板，让你无论是在写博客、灌水聊天都能快速插入图片。
连接格式可以是普通 URL、HTML 或者 Markdown，仍由你掌控。

**🔋 支持图床：** [smms](https://sm.ms/)、 [又拍云 USS](https://www.upyun.com/products/file-storage)、[七牛云 KODO](https://www.qiniu.com/products/kodo)、 [阿里云 OSS](https://www.aliyun.com/product/oss/)、 [腾讯云 COS](https://cloud.tencent.com/product/cos)、 [百度云 BOS](https://cloud.baidu.com/product/bos.html)、[微博](https://weibo.com/)、[Github](https://github.com/settings/tokens)、 [Gitee](https://gitee.com/profile/personal_access_tokens)、 [Amazon S3](https://aws.amazon.com/cn/s3/)、[Imgur](https://imgur.com/)、[自定义上传接口](https://blog.svend.cc/upic/tutorials/custom)、...

## 🚀 如何安装

### 下载安装
#### 1.AppStore(推荐):

> 只有 AppStore 才是最新的版本。其他方式安装的停留在 `v0.21.1`，可以自行拉取代码编译打包。

 [![uPic for macOS](https://cdn.jsdelivr.net/gh/gee1k/oss@master/uPic/app-store-black.svg)](https://apps.apple.com/cn/app/id1549159979)


#### 2.Homebrew
```bash
brew install bigwig-club/brew/upic --cask
```


#### 3.手动
从 [Github release](https://github.com/gee1k/uPic/releases) 下载。

**如果在国内访问 Github 下载困难的，可以从[Gitee release](https://gitee.com/gee1k/uPic/releases)下载。**

### 检查系统分享权限

- 1.打开 uPic

- 2.确保应用有完全磁盘访问权限，可在`偏好设置` - `高级` 中授权

  <center>
    <img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/full-disk-access.png" height="300">
  </center>

## 🕹 使用方式


| 功能 | 描述 | 预览 |
| --- | --- | --- |
| **🖥 选择文件上传** | 从`Finder`选择文件上传。`可设置全局快捷键` | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/selectFile.gif) |
| **⌨️ 复制文件上传** | 上传已拷贝到剪切板的文件。`可设置全局快捷键` | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/pasteboard.gif) |
| **📸 截图上传** | 直接拉框截图上传。`可设置全局快捷键` | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/screenshot.gif) |
| **🖱 拖拽本地文件上传** | 拖拽文件到状态栏上传 | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/dragFile.gif) |
| **🖱 拖拽浏览器图片上传** | 从浏览器拖拽图片到状态栏上传 | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/dragFromBrowser.gif) |
| **📂 系统分享上传** | 右击文件选择分享到uPic上传 | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/share.gif) |
| **⌨️ 命令行上传** | 通过执行命令调用 uPic 上传文件 | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/cli.gif) |


## 🧰 更多功能

### 1.全局快捷键
<img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/shortcuts.png" height="300">

### 2. 上传历史
<img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-cn/history.png" height="300">

## 优秀软件推荐

- [Bob:macOS 平台上最强的翻译和 OCR 软件](https://github.com/ripperhe/Bob)



## ✨ Contributors

### Code Contributors

This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].
<a href="https://github.com/gee1k/uPic/graphs/contributors"><img src="https://opencollective.com/uPic/contributors.svg?width=890&button=true" /></a>


### Other Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://alley.js.org"><img src="https://avatars1.githubusercontent.com/u/19723234?v=4" width="100px;" alt="alley"/><br /><sub><b>alley</b></sub></a><br /><a href="#translation-m01i0ng" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/Jackxun123"><img src="https://avatars2.githubusercontent.com/u/33611532?v=4" width="100px;" alt="Jackxun123"/><br /><sub><b>Jackxun123</b></sub></a><br /><a href="#translation-Jackxun123" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/kkkkkkyrie"><img src="https://avatars2.githubusercontent.com/u/30786071?v=4" width="100px;" alt="eleven"/><br /><sub><b>eleven</b></sub></a><br /><a href="#translation-kkkkkkyrie" title="Translation">🌍</a></td>
    <td align="center"><a href="https://immx.io/"><img src="https://avatars1.githubusercontent.com/u/16921591?v=4" width="100px;" alt="zhucebuliaomax"/><br /><sub><b>zhucebuliaomax</b></sub></a><br /><a href="#design-ihatework" title="Design">🎨</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

-----

**uPic** © [Svend](https://github.com/gee1k), Released under the [MIT](./LICENSE) License.<br>
Authored and maintained by Svend with help from contributors ([list](https://github.com/gee1k/uPic/contributors)).