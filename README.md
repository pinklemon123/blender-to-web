# 🎨 Blender to Web - 3D 模型展示项目

这是一个使用 GitHub Pages 托管的 3D 模型展示网站，可以在浏览器中直接查看从 Blender 导出的 GLB 格式模型。

## ✨ 特性

- 📦 支持 GLB/GLTF 格式的 3D 模型
- 🖱️ 支持鼠标/触摸屏交互（旋转、缩放、移动）
- 🔄 自动旋转展示
- 📱 响应式设计，支持移动设备
- 🚀 通过 GitHub Pages 免费托管

## 🚀 快速开始

### 1. 从 Blender 导出模型

1. 在 Blender 中打开你的模型
2. 选择 **文件 > 导出 > glTF 2.0 (.glb/.gltf)**
3. 选择 **GLB 格式**（二进制，单文件）
4. 保存为 `.glb` 文件

### 2. 上传模型到项目

1. 将导出的 `.glb` 文件放入 `assets/models/` 文件夹
2. 重命名为 `your-model.glb`，或者修改 `index.html` 中的路径

### 3. 部署到 GitHub Pages

```bash
# 初始化 Git 仓库（如果还没有）
git init

# 添加所有文件
git add .

# 提交
git commit -m "Initial commit: Add 3D model viewer"

# 连接到远程仓库
git remote add origin git@github.com:pinklemon123/blender-to-web.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

### 4. 启用 GitHub Pages

1. 进入 GitHub 仓库页面
2. 点击 **Settings**（设置）
3. 在左侧菜单找到 **Pages**
4. 在 **Source** 下选择 **main** 分支
5. 保存后等待几分钟

你的网站将会在以下地址访问：
```
https://pinklemon123.github.io/blender-to-web/
```

## 📁 项目结构

```
blender-to-web/
├── index.html              # 主页面
├── assets/
│   └── models/            # 存放 3D 模型文件
│       └── your-model.glb # 你的模型文件
└── README.md              # 项目说明
```

## 🎮 使用说明

### 浏览器中的交互控制

- **旋转模型**：点击并拖动鼠标
- **缩放模型**：使用鼠标滚轮或双指捏合
- **移动视角**：按住右键拖动（或双指滑动）
- **自动旋转**：模型会自动缓慢旋转展示

## 🔧 自定义设置

### 修改模型路径

在 `index.html` 中找到以下代码：

```html
<model-viewer src="assets/models/your-model.glb" ...>
```

将 `your-model.glb` 替换为你的模型文件名。

### 调整显示效果

可以修改 `<model-viewer>` 的属性：

```html
<model-viewer 
  src="assets/models/your-model.glb" 
  alt="3D 模型"
  auto-rotate                    <!-- 自动旋转 -->
  camera-controls                <!-- 相机控制 -->
  shadow-intensity="1"           <!-- 阴影强度 -->
  exposure="1"                   <!-- 曝光度 -->
  shadow-softness="0.5"          <!-- 阴影柔和度 -->
  background-color="#f5f5f5">    <!-- 背景颜色 -->
</model-viewer>
```

## 📚 技术栈

- [Google Model Viewer](https://modelviewer.dev/) - 3D 模型查看器组件
- [GitHub Pages](https://pages.github.com/) - 静态网站托管
- [Blender](https://www.blender.org/) - 3D 建模软件

## 📝 注意事项

1. **文件大小**：GitHub 单文件限制为 100MB，建议优化模型大小
2. **浏览器兼容性**：现代浏览器（Chrome、Firefox、Safari、Edge）都支持
3. **HTTPS**：GitHub Pages 自动提供 HTTPS，确保模型安全加载

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📄 许可证

MIT License

---

**Made with ❤️ using Blender and GitHub Pages**
