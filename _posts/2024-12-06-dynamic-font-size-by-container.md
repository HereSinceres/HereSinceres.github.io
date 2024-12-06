## 元素字体大小，跟随容器大小变化

## 代码

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      /* 设置整体布局 */
      .layout {
        display: grid;
        grid-template-columns: 200px 1fr;
        /* 左侧导航栏固定宽度，右侧内容区域自适应 */
        height: 100vh;
        /* 占满整个视口高度 */
      }

      /* 导航栏样式 */
      .sidebar {
        background-color: #2c3e50;
        color: #ffffff;
        padding: 20px;
        display: flex;
        flex-direction: column;
      }

      .sidebar ul {
        list-style: none;
        padding: 0;
      }

      .sidebar li {
        margin: 10px 0;
      }

      /* 内容区域样式 */
      .content {
        background-color: #ecf0f1;
        padding: 20px;
        /* 超出时滚动 */
      }

      /* 网格容器 */
      .grid-container {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        /* 每行 6 个等宽元素 */
        gap: 10px;
        /* 元素间距 */
        /* 启用容器单位 */
      }

      /* 网格项 */
      .grid-item {
        background-color: #ffffff;
        border: 1px solid #ccc;
        text-align: center;
        aspect-ratio: 1 / 1;
        /* 高宽比为 1:1 */
        display: flex;
        justify-content: center;
        align-items: center;
        line-height: 1;
        /* 容器必须设置 */
        container-type: inline-size;
      }

      .cell {
        /* 字体大小为容器宽度的 20% */
        font-size: 20cqw;
        border: 1cqw solid #ccc;
      }
    </style>
  </head>

  <body>
    <div class="layout">
      <nav class="sidebar">
        <ul>
          <li>导航项 1</li>
          <li>导航项 2</li>
          <li>导航项 3</li>
        </ul>
      </nav>
      <div class="content">
        <div class="grid-container">
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
          <div class="grid-item">
            <div class="cell">cell</div>
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
```

## 参考资料

- https://hackmd.io/@yuna9068/BJgGL9S36?utm_source=preview-mode&utm_medium=rec#%E5%AE%B9%E5%99%A8%E6%9F%A5%E8%A9%A2%E5%96%AE%E4%BD%8D
