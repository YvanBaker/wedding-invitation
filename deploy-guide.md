# 📱 婚礼请柬手机部署指南

## 方式一：本地手机直接查看 ⚡（最简单）

### 1️⃣ 电脑上操作
1. 打开文件资源管理器，进入项目目录：
   ```
   /mnt/c/Users/ZhuanZ（无密码）/WeChatProjects/h5
   ```

2. 将以下文件添加到你的照片：
   - `couple-photo-1.jpg` - 第一张合照
   - `couple-photo-2.jpg` - 第二张合照  
   - `background.jpg` - 背景图（可选）
   - `share-cover.jpg` - 分享封面图

3. 将整个 `h5` 文件夹复制到手机

### 2️⃣ 手机上操作
1. **安装文件管理器**：
   - 推荐：ES文件浏览器 或 MT管理器

2. **打开 HTML 文件**：
   - 在文件管理器中找到 `index.html`
   - 点击选择"使用浏览器打开"
   - 选择 Chrome 或 Safari 浏览器

3. **在微信中分享**：
   - 复制浏览器地址栏的链接（file://开头）
   - 在微信中发送给朋友测试

---

## 方式二：在线部署 🌐（推荐）

### GitHub Pages 部署（免费）

#### 1️⃣ 上传到 GitHub
```bash
# 1. 在 GitHub 创建新仓库（如：wedding-invitation）

# 2. 在项目目录下初始化 git
git init
git add .
git commit -m "Wedding invitation for 黄培真 ♥ 黄贝佳"

# 3. 关联远程仓库并推送
git branch -M main
git remote add origin https://github.com/your-username/wedding-invitation.git
git push -u origin main
```

#### 2️⃣ 开启 Pages 服务
1. 进入 GitHub 仓库设置页面
2. 找到 "Pages" 选项
3. Source 选择 "Deploy from a branch"
4. Branch 选择 "main"
5. 点击 Save

#### 3️⃣ 获取访问链接
- 等待几分钟后，GitHub 会生成链接：
  `https://your-username.github.io/wedding-invitation/`

#### 4️⃣ 微信分享
- 直接在微信中发送这个链接
- 朋友点击就能看到精美的婚礼请柬

---

## 方式三：快速在线部署 ⚡

### 使用 Netlify（推荐新手）

#### 1️⃣ 打包文件
1. 将整个 `h5` 文件夹压缩成 `.zip` 文件

#### 2️⃣ 上传部署
1. 访问：https://www.netlify.com
2. 注册登录账号
3. 点击 "Deploy" 按钮
4. 直接拖拽 zip 文件到页面
5. 等待部署完成（通常1-2分钟）

#### 3️⃣ 获取链接
- Netlify 会自动生成一个链接，如：
  `https://amazing-wedding-12345.netlify.app`

#### 4️⃣ 微信使用
- 这个链接可以直接在微信中打开
- 支持分享到朋友圈
- 加载速度很快

---

## 微信优化小贴士 💡

### 1️⃣ 图片优化
```bash
# 推荐图片处理网站：
https://tinypng.com  # 图片压缩

# 建议尺寸：
合照：800×600 像素，< 300KB
背景：768×1024 像素，< 500KB  
封面：400×400 像素，< 200KB
```

### 2️⃣ 微信分享设置
在 `index.html` 的 `<head>` 中已经配置了：
```html
<meta name="description" content="黄培真 & 黄贝佳 诚邀您见证我们的爱情盛典">
<meta property="og:title" content="黄培真 ♥ 黄贝佳 | 我们的婚礼">
<meta property="og:description" content="黄培真 & 黄贝佳 诚邀您见证我们的爱情盛典">
<meta property="og:image" content="./images/share-cover.jpg">
```

### 3️⃣ 测试清单
- ✅ 手机浏览器能正常打开
- ✅ 照片能正常显示  
- ✅ 动画效果流畅
- ✅ 微信内能正常访问
- ✅ 可以转发给朋友
- ✅ 朋友圈分享正常

---

## 🚀 快速部署命令

### 如果你熟悉命令行：
```bash
# 进入项目目录
cd "/mnt/c/Users/ZhuanZ（无密码）/WeChatProjects/h5"

# 添加你的照片到 images 文件夹
# couple-photo-1.jpg, couple-photo-2.jpg, background.jpg, share-cover.jpg

# 如果要用 GitHub Pages：
git init
git add .
git commit -m "黄培真 ♥ 黄贝佳 婚礼请柬"
git branch -M main
git remote add origin [你的GitHub仓库地址]
git push -u origin main

# 然后到 GitHub 仓库设置中开启 Pages
```

---

## ❓ 常见问题

**Q: 在微信里打开很慢？**
A: 压缩图片大小，确保每张图片小于300KB

**Q: 照片显示不出来？**
A: 检查文件路径和文件名是否正确

**Q: 能否添加背景音乐？**  
A: 可以，但微信对音频有限制，建议测试后再添加

**Q: 如何修改文字内容？**
A: 编辑 `index.html` 文件中的文字内容

**Q: 可以换个配色吗？**
A: 编辑 `style.css` 文件，搜索颜色代码进行替换

---

## 📞 技术支持

如有问题，检查这些文件：
- `index.html` - 主页面内容
- `style.css` - 样式和配色  
- `script.js` - 交互功能
- `images/` - 图片文件夹

祝你们婚礼美满！💕