# 工作评分系统 · PWA 部署说明

## 文件结构

```
workscore-pwa/
├── index.html       ← 应用主界面（已内置 PWA 支持）
├── manifest.json    ← PWA 配置（名称、图标、颜色）
├── sw.js            ← Service Worker（离线缓存）
├── icons/
│   ├── icon-192.png ← 应用图标（小）
│   └── icon-512.png ← 应用图标（大）
└── README.md        ← 本文件
```

---

## 部署到 GitHub Pages（免费，5分钟完成）

### 第一步：注册 GitHub
访问 https://github.com，注册一个免费账号。

### 第二步：新建仓库
1. 点右上角 **+** → **New repository**
2. Repository name 填：`workscore-app`
3. 选 **Public**
4. 点 **Create repository**

### 第三步：上传文件
在新建的仓库页面，点 **uploading an existing file**，
把整个 `workscore-pwa` 文件夹里的所有文件拖进去（注意 icons 文件夹也要上传），
点 **Commit changes**。

### 第四步：开启 GitHub Pages
1. 进入仓库 → **Settings** → 左侧 **Pages**
2. Source 选 **Deploy from a branch**
3. Branch 选 **main**，目录选 **/ (root)**
4. 点 **Save**

等待约 1 分钟，页面会显示你的网址，格式为：

```
https://你的用户名.github.io/workscore-app/
```

---

## 安装到桌面（Mac）

### Chrome / Edge 浏览器：
1. 用 Chrome 打开上面的网址
2. 地址栏右侧会出现 ⊕ 安装图标
3. 点击 → **安装**
4. Dock 栏里会出现「工作评分」图标，双击即可独立窗口运行

### Safari（iPhone / iPad）：
1. 用 Safari 打开网址
2. 点底部分享按钮 □↑
3. 选「添加到主屏幕」
4. 点「添加」

---

## PWA 的特点

| 特性 | 说明 |
|---|---|
| 离线可用 | 首次加载后，断网也能正常使用 |
| 数据本地存储 | 数据存在浏览器 localStorage，不上传服务器 |
| 独立窗口 | 安装后以独立窗口运行，没有浏览器地址栏 |
| 自动更新 | 有网络时自动获取最新版本 |

---

## 常见问题

**Q: 安装图标没出现？**
确认是用 Chrome 或 Edge 打开，Safari 在 Mac 上不支持安装 PWA。

**Q: 数据会丢失吗？**
数据存在浏览器本地，清除浏览器数据时会丢失。建议定期用应用内「导出数据」功能备份。

**Q: 能分享给朋友用吗？**
可以，把网址发给朋友，他们也可以安装。每个人的数据独立存在各自设备上。

**Q: 想用自己的域名？**
在 GitHub Pages 设置里填入自定义域名，再到域名服务商添加 CNAME 记录即可。
