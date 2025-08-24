# AR.js Demo 项目

## 项目简介
这是一个基于AR.js的H5 AR演示项目，用于验证图像识别AR功能。

## 功能特性
- 📱 手机摄像头实时识别
- 🎯 图像Marker识别
- 🎨 3D模型展示
- ✨ 动画效果
- 👆 交互功能

## 技术栈
- AR.js - WebAR框架
- A-Frame - 3D场景框架
- Three.js - 3D渲染引擎

## 快速开始

### 1. 环境要求
- 支持WebRTC的现代浏览器
- HTTPS环境（必需）
- 摄像头权限

### 2. 启动项目
```bash
# 使用Python启动本地服务器
python -m http.server 8000

# 或使用Node.js
npx http-server -p 8000

# 或使用PHP
php -S localhost:8000
```

### 3. 访问项目
在浏览器中访问：`https://localhost:8000`

### 4. 使用说明
1. 允许摄像头权限
2. 下载Hiro marker图片：https://raw.githubusercontent.com/AR-js-org/AR.js/master/data/images/HIRO.jpg
3. 将marker图片显示在另一个设备上或打印出来
4. 将摄像头对准marker
5. 观察3D模型出现

## 项目结构
```
arjs-demo/
├── index.html          # 主页面
├── index-local.html    # 备用版本
├── README.md           # 说明文档
└── assets/             # 资源文件（可选）
    ├── models/         # 3D模型
    └── textures/       # 纹理文件
```

## 自定义配置

### 修改Marker
```html
<!-- 使用自定义marker -->
<a-marker type="pattern" url="path/to/your/marker.patt">
    <!-- 3D内容 -->
</a-marker>
```

### 添加3D模型
```html
<a-marker preset="hiro">
    <!-- GLTF模型 -->
    <a-entity
        position="0 0 0"
        scale="1 1 1"
        gltf-model="url(path/to/model.gltf)">
    </a-entity>
</a-marker>
```

## 常见问题

### Q: 摄像头无法启动？
A: 确保使用HTTPS协议，并允许浏览器摄像头权限。

### Q: 识别不到marker？
A: 确保marker图片清晰，光照充足，摄像头与marker距离适中。

### Q: 3D模型不显示？
A: 检查模型文件路径是否正确，格式是否支持。

## 扩展功能
- 添加更多3D模型
- 实现手势识别
- 添加音效
- 实现多人协作
- 添加物理效果

## 参考资源
- [AR.js官方文档](https://ar-js-org.github.io/AR.js/)
- [A-Frame文档](https://aframe.io/docs/)
- [Three.js文档](https://threejs.org/docs/)
