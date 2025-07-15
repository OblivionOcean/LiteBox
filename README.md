# LiteBox

一个超轻量级的图片灯箱组件，使用原生JavaScript和CSS实现，无需任何外部依赖。
它提供了丰富的图片查看功能，同时保持极小的代码体积(JS ～5.5KiB + CSS ~2.5KiB, Gzip后JS ～2KiB + CSS ～900B)

## 功能特点

### 🚀 轻量高效

- 核心代码仅8KiB, Gzip后2.87KiB (JS ～5.5KiB + CSS ~2.5KiB, Gzip后JS ～2KiB + CSS ～900B)
- 零外部依赖，纯原生实现
- 流畅动画效果

### ✨ 完整功能集

- **图片缩放**：支持放大/缩小查看细节
- **翻页浏览**：左右箭头切换图片
- **图片旋转**：90度旋转功能
- **重置视图**：一键恢复原始大小和位置
- **键盘快捷键**：支持ESC关闭、方向键翻页等

### 🎨 优雅UI

- 现代化卡片式布局
- 半透明玻璃态控制面板
- 平滑的过渡动画效果
- 直观的图标按钮控制

## 安装与使用

### 基本使用

```html
<!DOCTYPE html>
<html>

<head>
</head>

<body>
    <main>
        <div class="gallery">
            <!-- Sample images -->
            <div class="thumbnail">
                <img src="https://images.unsplash.com/photo-1501854140801-50d01698950b?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
                    alt="自然风光" data-src="https://images.unsplash.com/photo-1501854140801-50d01698950b"
                    data-caption="自然风景 - 山脉与湖泊" data-title="山脉湖泊">
                <div class="title">山脉湖泊</div>
            </div>

            <div class="thumbnail">
                <img src="https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
                    alt="森林晨曦" data-src="https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05"
                    data-caption="森林晨曦 - 阳光穿透雾气" data-title="森林晨曦">
                <div class="title">森林晨曦</div>
            </div>

            <div class="thumbnail">
                <img src="https://images.unsplash.com/photo-1519681393784-d120267933ba?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
                    alt="雪山星空" data-src="https://images.unsplash.com/photo-1519681393784-d120267933ba"
                    data-caption="雪山星空 - 壮丽的银河景观" data-title="雪山星空">
                <div class="title">雪山星空</div>
            </div>

            <div class="thumbnail" data-caption="宁静森林 - 秋季的金黄色调" data-title="宁静森林">
                <img src="https://images.unsplash.com/photo-1505142468610-359e7f316449?ixlib=rb-1.2.1&auto=format&fit=crop&w=400&q=80"
                    data-src="https://images.unsplash.com/photo-1505142468610-359e7f316449"
                    data-caption="宁静森林 - 秋季的金黄色调">
                <div class="title">宁静森林</div>
            </div>
        </div>
    </main>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@oblivionocean/litebox/dist/index.css">
    <script src="https://cdn.jsdelivr.net/npm/@oblivionocean/litebox/dist/index.min.js"></script>
</body>

</html>
```

### 快速集成

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@oblivionocean/litebox/dist/index.css">
<script src="https://cdn.jsdelivr.net/npm/@oblivionocean/litebox/dist/index.min.js"></script>
```

### img 标签属性

| 属性 | 说明 |
| --- | --- |
| data-src | 高清晰图片地址，没有高清图片地址时，会自动使用 src 属性作为图片地址 |
| src | 缩略图地址 |
| alt | 图片描述 |
| data-title | 图片标题 |
| data-caption | 图片描述 |

## 使用方法

### 基本操作

1. 点击任意缩略图打开灯箱
2. 使用控制按钮进行操作：
   - **← →** 按钮：前后切换图片
   - **+/-** 按钮：放大/缩小图片
   - **↻** 按钮：旋转图片
   - **↔** 按钮：重置缩放和位置
   - **×** 按钮：关闭灯箱

### 键盘快捷键

- **ESC**：关闭灯箱
- **左右箭头**：切换图片
- **+/-**：放大/缩小图片
- **0**：重置缩放
- **R**：旋转图片

## 核心实现

- 使用HTML5 `<dialog>`元素作为灯箱容器
- CSS transform实现高性能动画
- CSS变量控制缩放和旋转效果
- 原生JavaScript处理交互逻辑

## 浏览器兼容性

LiteBox支持所有现代浏览器，包括：

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)

对于不支持`<dialog>`元素的旧版浏览器，LiteBox会自动降级为常规弹窗实现。

## 贡献与许可

欢迎贡献代码和提出改进建议！本项目采用MIT许可证开源。

**MIT License** - 自由使用、修改和分发代码
