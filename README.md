# Yichen Chen - 个人作品集网站

一个现代化的个人作品集网站，采用极简杂志风格设计，使用 React、Tailwind CSS 和 Framer Motion 构建，展示设计作品与项目经历。

## 页面介绍

### 首页 (main.html / index.html)

网站首页由以下几个主要部分组成：

#### 1. 导航栏 (Navigation)
- 固定在页面顶部，始终可见
- 包含四个导航链接：**WORK**（作品）、**PROJECT**（项目经历）、**PROFILE**（个人简介）、**CONTACT**（联系方式）
- 采用混合差异模式 (mix-blend-difference)，在不同背景下自动调整颜色

#### 2. 英雄区 (Hero Section)
- 全屏展示的开场区域
- 大字体标题 "Innovative Strategist"，配合渐变动画效果
- 简短的个人定位描述
- 向下箭头提示用户继续滚动

#### 3. 精选项目横向滚动区 (Featured Projects)
- 横向滚动展示所有作品
- 鼠标悬停时显示 "View Project →" 提示
- 点击可进入作品详情页
- 右侧渐变遮罩提示可继续滚动

#### 4. 作品集网格 (Selected Works)
- 采用响应式网格布局（1-2列）
- 大作品占据两列，小作品占据一列
- 3D 卡片倾斜效果和发光悬停效果
- 点击进入作品详情页

#### 5. 项目经历 (Project Experience)
- 按年份分组展示（2025、2024、2023）
- 大字体年份数字，2025 年份带渐变动画效果
- 每年包含多个项目/经历详情
- 悬停时年份变为斜体

#### 6. 个人简介 (Profile)
- 深色背景，杂志风格排版
- 设计理念阐述
- 服务类型、荣誉奖项、兴趣爱好列表
- 个人照片（悬停时从黑白变为彩色）

#### 7. 联系方式 (Contact/Footer)
- 大字体邮箱地址，可直接点击发送邮件
- 社交媒体图标链接（Instagram、LinkedIn、Mail）
- 版权信息

### 作品详情页 (project-detail.html)

- 根据 URL 参数 `?id=` 动态加载对应作品
- 展示作品标题、类别、年份
- 图片瀑布流展示，支持视频播放
- 部分作品包含外部链接（如 VR 展示）
- 底部 "Back to All Projects" 按钮返回首页对应作品位置

## 特色动效

| 动效 | 描述 |
|------|------|
| 自定义光标 | 圆形光标跟随鼠标移动，悬停交互元素时放大 |
| 粒子背景 | 浮动的装饰性粒子元素 |
| 渐变文字 | 标题文字渐变色流动动画 |
| 3D 卡片 | 作品卡片根据鼠标位置产生 3D 倾斜效果 |
| 图片光晕 | 图片悬停时的光晕扫过效果 |
| 视差滚动 | 元素随滚动产生视差效果 |
| 入场动画 | 元素进入视口时的渐入动画 |

## 如何在本地运行

### 方法 1：直接打开（推荐）

1. 直接双击 `main.html` 或 `index.html` 文件，在浏览器中打开即可
2. 或者右键文件 → "打开方式" → 选择你的浏览器（Chrome、Edge、Firefox等）

### 方法 2：使用本地服务器（推荐用于开发）

如果你遇到跨域问题或想要更好的开发体验，可以使用本地服务器：

#### 使用 Python（如果已安装）

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

然后在浏览器访问：`http://localhost:8000`

#### 使用 Node.js（如果已安装）

安装 `http-server`：
```bash
npm install -g http-server
```

运行服务器：
```bash
http-server -p 8000
```

然后在浏览器访问：`http://localhost:8000`

#### 使用 VS Code Live Server 插件

1. 在 VS Code 中安装 "Live Server" 插件
2. 右键 `main.html` 或 `index.html` 文件
3. 选择 "Open with Live Server"

## 项目结构

```
mywebsire/
├── main.html              # 主页面文件
├── index.html             # 主页面文件（与 main.html 相同）
├── project-detail.html    # 作品详情页
├── portrait.jpg           # 个人照片
├── README.md              # 项目说明文档
└── 作品集/                # 作品集图片文件夹
    ├── 中药配伍/          # FormulaPro 项目
    ├── A design版面/      # A' Design Award 获奖作品
    │   ├── Reverba/
    │   └── SeaSavor Vessel/
    ├── Blueclip Buddies/  # 产品设计项目
    ├── Shared Dwelling/   # 空间设计项目
    ├── 墨迹/              # MoArt Essence 项目
    ├── VISTA/             # 概念车 HMI 设计
    ├── 逆水寒_四方行舟/   # 服务设计项目
    ├── 【时光年轮】慢闪空间提案/  # 空间设计项目
    └── Fact Sheet for UniversityWide Exchange Students/
```

## 技术栈

| 技术 | 用途 |
|------|------|
| **React 18** | 构建交互式用户界面 |
| **Tailwind CSS** | 快速构建现代化样式 |
| **Framer Motion** | 流畅的动画效果 |
| **Babel** | JSX 编译 |
| **CDN 引入** | 所有依赖通过 CDN 加载，无需 npm 安装 |

## 特性

- ✨ 现代化极简杂志风格设计
- 🎯 自定义鼠标光标效果
- 📱 完全响应式设计（移动端/平板/桌面端）
- 🎭 流畅的动画和过渡效果
- 🖼️ 作品集展示和详情页
- 📧 联系方式和社交媒体链接
- 🔗 返回首页时定位到对应作品位置
- 🌓 深浅色区块交替，视觉层次分明

## 浏览器兼容性

| 浏览器 | 支持情况 |
|--------|----------|
| Chrome/Edge | ✅ 推荐 |
| Firefox | ✅ 支持 |
| Safari | ✅ 支持 |
| IE | ❌ 不支持 |

> 需要支持 ES6+ 和现代 CSS 特性

## 自定义内容

如果你想修改网站内容：

| 修改项 | 位置说明 |
|--------|----------|
| **个人信息** | 搜索 "Yichen Chen" 并替换为你的名字 |
| **作品集数据** | 在 `projects` 数组中修改 |
| **项目经历** | 在 "Project Experience Section" 部分修改 |
| **个人简介** | 在 "About" 部分修改文字 |
| **联系方式** | 修改邮箱地址和社交媒体链接 |
| **个人照片** | 替换 `portrait.jpg` 文件 |

## 注意事项

- 确保 `作品集` 文件夹中的图片文件存在
- 图片路径区分大小写
- 建议使用现代浏览器以获得最佳体验
- 所有外部依赖（React、Tailwind、Framer Motion）都通过 CDN 加载，需要网络连接
- `main.html` 和 `index.html` 内容保持同步

## 问题排查

如果网站无法正常显示：

1. **检查浏览器控制台**：按 F12 打开开发者工具，查看是否有错误
2. **检查图片路径**：确认 `作品集` 文件夹和图片文件都在正确位置
3. **网络连接**：确保可以访问 CDN 资源（unpkg.com、googleapis.com）
4. **浏览器缓存**：尝试清除缓存或使用隐私/无痕模式

## 更新日志

### 2026-01-11
- 修复导航栏始终可见问题
- 修复项目经历年份显示截断问题
- 添加丰富的动画效果（粒子背景、3D卡片、渐变文字等）

---

© 2026 Yichen Chen | Designed with ❤️ in Hangzhou
