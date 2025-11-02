# Assets 文件夹

此文件夹用于存放网站的静态资源文件。

## 需要的文件

### 1. favicon.ico
- **位置**: `./assets/favicon.ico`
- **说明**: 网站图标，显示在浏览器标签页上
- **格式**: ICO 格式
- **建议尺寸**: 16x16, 32x32, 48x48 像素（多尺寸ICO）

### 2. avatar.jpg（可选）
- **位置**: `./assets/avatar.jpg`
- **说明**: 个人头像图片
- **格式**: JPG 或 PNG
- **建议尺寸**: 至少 248x248 像素（推荐 500x500 像素）
- **使用方式**: 
  在 `index.html` 第 290 行，将：
  ```html
  <div class="avatar" id="avatar" title="头像占位：替换为你的图片">
      LI
  </div>
  ```
  替换为：
  ```html
  <div class="avatar" id="avatar" title="头像占位：替换为你的图片">
      <img src="./assets/avatar.jpg" alt="li">
  </div>
  ```

### 3. bg.jpg（可选）
- **位置**: `./assets/bg.jpg`
- **说明**: 背景图片，可替换默认的渐变背景
- **格式**: JPG 或 PNG
- **建议尺寸**: 1920x1080 或更高分辨率
- **使用方式**: 
  在 CSS 中修改 `.bg-slot` 样式，添加 `background-image` 属性

## 注意事项

- 所有图片文件建议进行压缩以优化加载速度
- 确保文件名和路径与代码中的引用一致
- 如果不需要某些文件，可以保留默认的样式效果

