<div align="right"><strong><a href="./README.md">🇨🇳中文</a></strong>  | <strong>🇬🇧English</strong></div>
<div align="center">
  <img src="https://raw.githubusercontent.com/gee1k/oss/master/screenshot/uPic/logo.png" alt="uPic">
  <br>
  <br>
  <p>
    Picture and file upload tool for macOS. - A native, powerful, beautiful and simple
  </p>

  <p>

  [![Travis Build Status](https://img.shields.io/travis/gee1k/uPic.svg?style=flat-square&logo=Travis)](https://travis-ci.org/gee1k/uPic)  [![MIT](https://img.shields.io/github/license/gee1k/uPic?style=flat-square)](https://github.com/gee1k/uPic/blob/master/LICENSE)

[![Donate on PayPal](https://img.shields.io/badge/support-PayPal-blue?style=flat-square&logo=PayPal)](https://paypal.me/geeee1k) [![Chat on Telegram](https://img.shields.io/badge/chat-Telegram-blueviolet?style=flat-square&logo=Telegram)](https://t.me/upic_host) [![Follow My Twitter](https://img.shields.io/badge/follow-Tweet-blue?style=flat-square&logo=Twitter)](https://twitter.com/realSvend) [![Follow My Weibo](https://img.shields.io/badge/follow-Weibo-red?style=flat-square&logo=sina-weibo)](https://weibo.com/643660358)

  </p>
</div>

---

## 🔧 Fork Version Info

> ⚠️ **This is graylogo's Fork version, specifically adapted for macOS 26 and Xcode 26**

### ✨ This Version Updates

**v1.4.8-macOS26** (2024-06-06)

#### Core Compatibility Upgrades

1. **WCDB Database Upgrade**
   - Upgraded WCDB from 2.1.9 to **2.1.16**
   - Fixed Swift 6 compilation compatibility issues
   - Fixed C++ standard library specialization errors

2. **Removed Incompatible libminipng Framework**
   - Removed pre-compiled libminipng.framework (incompatible with Swift 6)
   - Switched to macOS native `NSBitmapImageRep` for PNG image compression
   - Maintained original image compression functionality

3. **Xcode 26 Adaptation**
   - Updated entitlements file configuration
   - Minimum system requirement raised to **macOS 13**
   - Optimized Swift 6 compilation settings

#### 🔄 Difference from Upstream

- Based on latest code after author's v0.21.1
- Includes all author's feature updates
- Focused on macOS 26/Xcode 26 compatibility fixes

#### ⚠️ System Requirements

- **Minimum**: macOS 13 (Ventura) or higher
- **Recommended**: macOS 14 (Sonoma) or macOS 26
- **Xcode**: Xcode 15+ (Xcode 26 recommended)

#### 📥 Installation

**Method 1: Compile and Install**
```bash
# Clone this repository
git clone https://github.com/graylogo/uPic.git
cd uPic

# Compile Release version
xcodebuild -project uPic.xcodeproj -scheme "uPic(Release)" -configuration Release build

# App will be generated at
# ./build/Build/Products/Release/uPic.app
```

**Method 2: Command Line Install**
```bash
# After compilation, copy to Applications folder
cp -R ./build/Build/Products/Release/uPic.app /Applications/

# Launch app
open -a uPic
```

#### 🔄 Keeping in Sync with Upstream

This Fork will periodically sync updates from the author's repository:

```bash
# Add upstream repository (if not already done)
git remote add upstream https://github.com/gee1k/uPic.git

# Sync upstream updates
git fetch upstream
git merge upstream/master
git push origin master
```

#### 📚 Related Resources

- **Author's Repository**: [gee1k/uPic](https://github.com/gee1k/uPic)
- **This Fork**: [graylogo/uPic](https://github.com/graylogo/uPic)
- **Detailed Usage Guide**: [FORK_GUIDE.md](./FORK_GUIDE.md)

---

**👬Chat: _[Telegram](https://t.me/upic_host), [Twitter](https://twitter.com/realSvend), [Weibo](https://weibo.com/643660358)_**

**☕️Donate: _[Paypal](https://paypal.me/geeee1k), [Alipay](https://raw.githubusercontent.com/gee1k/oss/master/qrcode/alipay.JPG), [WechatPay](https://raw.githubusercontent.com/gee1k/oss/master/qrcode/wechat_pay.JPG)_**

**📱uPic for iOS: [![uPic for iOS](https://cdn.jsdelivr.net/gh/gee1k/oss@master/uPic/app-store-black.svg)](https://apps.apple.com/us/app/id1510718678)**

## 📑 Introduction

> **uPic(upload Picture) is a image(file) hosting client for Mac.** 

**💡 Tips：** They can automatic uploading local file and screenshot, meanwhile the menu bar shows the uploading progress constantly. File's link will automatically copied to the clipboard when finish upload, make you insert pictures quickly when you are blogging or chatting. Link's format can be a normal URL, HTML or Markdown, it's totally up to you.

**🔋 Support image hosting：**[smms](https://sm.ms/), [UPYUN USS](https://www.upyun.com/products/file-storage), [qiniu KODO](https://www.qiniu.com/products/kodo), [Aliyun OSS](https://www.aliyun.com/product/oss/), [TencentCloud COS](https://cloud.tencent.com/product/cos), [BaiduCloud BOS](https://cloud.baidu.com/product/bos.html), [Weibo](https://weibo.com/), [Github](https://github.com/settings/tokens), [Gitee](https://gitee.com/profile/personal_access_tokens), [Amazon S3](https://aws.amazon.com/cn/s3/), [Imgur](https://imgur.com/), [custom upload api](https://blog.svend.cc/upic/tutorials/custom), ...

## 🚀 How to install


### 1. AppStore(Recommend):

> Only AppStore is the latest version. Other installations stay at `v0.21.1'.and you can pull the code to compile and package by yourself.

 [![uPic for macOS](https://cdn.jsdelivr.net/gh/gee1k/oss@master/uPic/app-store-black.svg)](https://apps.apple.com/cn/app/id1549159979)


### 2.Homebrew
```bash
brew install bigwig-club/brew/upic --cask
```

### 3. Download from github
 Click [release](https://github.com/gee1k/uPic/releases) to download.

 **If you have difficulty accessing Github in mainland China, you can download it from [Gitee release](https://gitee.com/gee1k/uPic/releases).**

### Check System Share Permission

- 1. Run uPic

- 2. Make sure the app has Full Disk Access permission, which can be authorized in `Preferences` - `Advanced`

  <center>
    <img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/full-disk-access.png" height="300">
  </center>



## 🕹 How to use it

| Upload method | Description | Preview |
| ------------- | ----------- | ------- |
| **🖥 Select files** |  Select the file to upload from `Finder`.  `Can set global shortcuts`  | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/selectFile.gif) |
| **⌨️ Copy file upload** | Upload a file that has been copied to the clipboard.  `Can set global shortcuts` | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/pasteboard.gif) |
| **📸 Screenshot upload** | Directly pull frame screenshot upload.  `Can set global shortcuts` | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/screenshot.gif) |
| **🖱 Drag and drop local file upload** | Drag and drop files to the status bar to upload | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/dragFile.gif) |
| **🖱 Drag and drop browser image upload** | Drag image from browser to status bar to upload | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/dragFromBrowser.gif) |
| **📂 Share Extension upload** | Right click on file and share to uPic | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/share.gif) |
| **⌨️ Command line upload** | Invoke uPic to upload files by executing commands | ![](https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/cli.gif) |

## 🧰 More features

### 1. Global shortcut key
<img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/shortcuts.png" height="300">

### 2. Upload history
<img src="https://cdn.jsdelivr.net/gh/gee1k/oss@master/screenshot/uPic-en/history.png" height="300">


## Software recommendation

- [Bob:The most powerful translation and OCR software on macOS](https://github.com/ripperhe/Bob)

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