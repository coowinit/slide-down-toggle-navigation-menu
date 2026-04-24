# Slide Down Toggle JS 导航菜单

一个基于 **HTML + CSS + jQuery** 的响应式下拉导航菜单组件示例。项目内置桌面端多级下拉菜单、Mega Menu、半宽菜单、图片菜单、表单菜单、移动端折叠导航、主题配色切换和下拉动画效果，适合用于企业官网、产品展示站、营销落地页或静态 HTML 页面导航区域。

> 当前项目为静态前端导航菜单示例，不包含后台管理、构建工具、NPM 发布配置或服务端接口。

## 项目特点

- 响应式导航菜单，桌面端与移动端自动适配
- 支持普通下拉菜单、多级子菜单、Mega Menu、半宽 Mega Menu
- 支持图片内容、产品列表、文章摘要、网格布局、联系表单等菜单内容
- 移动端使用 `slideToggle` 实现菜单展开与收起
- 内置 16 套颜色皮肤：白色系与渐变色系
- 内置 6 套下拉动画：Fade Down、Fade Up、Fade Left、Fade Right、Rotate X、Rotate Y
- 基于 Bootstrap 栅格系统，可快速扩展复杂菜单内容
- 文件结构简单，可直接部署到 GitHub Pages、Netlify、Vercel 或普通静态服务器

## 技术栈与依赖

| 依赖 | 用途 | 项目内位置 |
| --- | --- | --- |
| HTML5 | 页面结构与菜单示例 | `index.html` |
| CSS3 | 菜单样式、响应式布局、动画效果 | `webslidemenu/` |
| jQuery 3.2.1 | 菜单折叠、移动端展开收起、演示切换 | `vendor/jquery/jquery-3.2.1.min.js` |
| Bootstrap | 栅格系统与基础样式 | `vendor/bootstrap/` |
| Font Awesome 5.7.2 | 菜单图标 | CDN 引入 |

## 目录结构

```text
Slide-Down-Toggle-JS/
├── index.html
├── images/
│   ├── logo.png
│   ├── menu-logo.png
│   ├── topbg.jpg
│   ├── headbg.png
│   └── image01.jpg ~ image06.jpg
├── vendor/
│   ├── bootstrap/
│   │   ├── bootstrap.min.css
│   │   └── bootstrap.min.js
│   └── jquery/
│       └── jquery-3.2.1.min.js
└── webslidemenu/
    ├── webslidemenu.css
    ├── webslidemenu.js
    ├── demo.css
    ├── color-skins/
    │   ├── white-blue.css
    │   ├── white-green.css
    │   ├── white-gry.css
    │   ├── white-orange.css
    │   ├── white-pink.css
    │   ├── white-purple.css
    │   ├── white-red.css
    │   ├── white-yellow.css
    │   ├── grd-black.css
    │   ├── grd-blue.css
    │   ├── grd-green.css
    │   ├── grd-gry.css
    │   ├── grd-light-green.css
    │   ├── grd-orange.css
    │   ├── grd-pink.css
    │   └── grd-red.css
    └── dropdown-effects/
        ├── fade-down.css
        ├── fade-up.css
        ├── fade-left.css
        ├── fade-right.css
        ├── rotate-x.css
        └── rotate-y.css
```

## 快速开始

### 1. 下载或克隆项目

```bash
git clone https://github.com/your-username/slide-down-toggle-navigation-menu.git
cd slide-down-toggle-navigation-menu
```

### 2. 直接打开演示页面

双击打开：

```text
index.html
```

也可以使用本地静态服务器预览：

```bash
python -m http.server 8000
```

然后在浏览器访问：

```text
http://localhost:8000
```

## 页面说明

项目当前只有一个主演示页面：

| 文件 | 说明 |
| --- | --- |
| `index.html` | 导航菜单完整演示页面，包含普通下拉、多级菜单、Mega Menu、图片菜单、Typography、Grid System、联系表单、配色切换与动画切换 |

## 菜单功能说明

### 普通下拉菜单

使用 `.sub-menu` 定义下拉菜单，可继续嵌套子级菜单。

```html
<li aria-haspopup="true">
  <a href="#">Dropdown <span class="wsarrow"></span></a>
  <ul class="sub-menu">
    <li><a href="#">Submenu item</a></li>
    <li><a href="#">Submenu item</a></li>
  </ul>
</li>
```

### Mega Menu

使用 `.wsmegamenu` 创建宽屏 Mega Menu，可结合 Bootstrap 栅格系统排版。

```html
<li aria-haspopup="true">
  <a href="#">Mega menu <span class="wsarrow"></span></a>
  <div class="wsmegamenu clearfix">
    <div class="container-fluid">
      <div class="row">
        <ul class="col-lg-3 col-md-12 link-list">
          <li class="title">Product Header</li>
          <li><a href="#">Submenu link style</a></li>
        </ul>
      </div>
    </div>
  </div>
</li>
```

### 半宽菜单

使用 `.halfmenu` 或 `.halfdiv` 可以创建较窄的菜单区域，适合展示少量链接、表单或联系信息。

```html
<div class="wsmegamenu clearfix halfmenu">
  ...
</div>
```

### 移动端折叠菜单

`webslidemenu.js` 会自动为 `.wsmenu` 添加移动端开关按钮，并通过 jQuery `slideToggle()` 控制菜单展开和收起。项目默认在 **991px 以下** 切换为移动端菜单样式。

## 引入方式

在 HTML 页面中引入依赖和菜单资源：

```html
<!-- Vendor -->
<script src="vendor/jquery/jquery-3.2.1.min.js"></script>
<script src="vendor/bootstrap/bootstrap.min.js"></script>
<link rel="stylesheet" href="vendor/bootstrap/bootstrap.min.css">
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css">

<!-- WebSlide Menu -->
<link id="effect" rel="stylesheet" href="webslidemenu/dropdown-effects/fade-down.css">
<link rel="stylesheet" href="webslidemenu/webslidemenu.css">
<link id="theme" rel="stylesheet" href="webslidemenu/color-skins/white-gry.css">
<script src="webslidemenu/webslidemenu.js"></script>
```

> 如果需要离线使用，请将 Font Awesome 资源下载到本地，并把 CDN 地址替换为本地路径。

## 更换颜色皮肤

项目内置两类颜色皮肤：

### 白色系皮肤

- `white-blue.css`
- `white-green.css`
- `white-gry.css`
- `white-orange.css`
- `white-pink.css`
- `white-purple.css`
- `white-red.css`
- `white-yellow.css`

### 渐变色皮肤

- `grd-black.css`
- `grd-blue.css`
- `grd-green.css`
- `grd-gry.css`
- `grd-light-green.css`
- `grd-orange.css`
- `grd-pink.css`
- `grd-red.css`

修改 `index.html` 中的主题 CSS 即可切换默认皮肤：

```html
<link id="theme" rel="stylesheet" href="webslidemenu/color-skins/white-gry.css">
```

例如改为蓝色主题：

```html
<link id="theme" rel="stylesheet" href="webslidemenu/color-skins/white-blue.css">
```

## 更换下拉动画

可在 `webslidemenu/dropdown-effects/` 中选择不同动画文件：

- `fade-down.css`
- `fade-up.css`
- `fade-left.css`
- `fade-right.css`
- `rotate-x.css`
- `rotate-y.css`

修改 `index.html` 中的动画 CSS：

```html
<link id="effect" rel="stylesheet" href="webslidemenu/dropdown-effects/fade-down.css">
```

## 自定义菜单内容

### 修改 Logo

替换以下图片即可：

```text
images/logo.png
images/menu-logo.png
```

### 修改菜单文字和链接

在 `index.html` 中查找：

```html
<ul class="wsmenu-list">
```

然后根据需要修改 `<li>`、`<a>`、`.sub-menu`、`.wsmegamenu` 等结构。

### 删除演示切换面板

`index.html` 中包含主题色和动画切换演示代码。如果正式项目不需要，可以删除以下部分：

```html
<link rel="stylesheet" href="webslidemenu/demo.css">
```

以及对应的演示切换 HTML 和 JavaScript。

### 修改移动端断点

默认移动端断点在 `webslidemenu/webslidemenu.css` 中：

```css
@media only screen and (max-width: 991px) {
  ...
}
```

如需适配其他断点，可根据项目布局调整该数值。

## 部署到 GitHub Pages

1. 新建 GitHub 仓库
2. 上传本项目所有文件
3. 进入仓库 `Settings` → `Pages`
4. Source 选择 `Deploy from a branch`
5. Branch 选择 `main`，目录选择 `/root`
6. 保存后等待 GitHub Pages 生成访问地址

确保 `index.html` 位于仓库根目录，这样 GitHub Pages 可以直接作为首页加载。

## 使用建议

- 正式上线前建议删除演示切换面板，只保留实际项目需要的主题和动画文件
- 如果项目不依赖 Bootstrap，可根据实际情况移除未使用的 Bootstrap 样式，但 Mega Menu 的栅格布局需要同步调整
- 如果需要更现代的兼容性，可将 jQuery 和 Bootstrap 升级到新版本，并重新测试菜单交互
- 建议将外部 CDN 资源本地化，以保证国内访问速度和离线部署稳定性
- 联系表单只是前端示例，不包含真实提交逻辑，正式使用时需要对接后端接口

## 注意事项

- 本项目为静态 HTML/CSS/JS 示例，不包含打包、编译或自动化构建流程
- 原始样式文件注释中包含第三方授权信息，公开上传到 GitHub 前请确认你拥有合法使用、分发或展示该模板的权利
- 如果作为公开仓库发布，建议移除无授权图片素材，或替换为自有素材 / 开源素材

## License

请根据你实际拥有的模板授权方式补充许可证说明。若该项目来自商业模板或第三方组件包，请遵循原作者授权协议。
