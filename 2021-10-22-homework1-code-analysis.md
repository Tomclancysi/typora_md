---
layout: post
title: homework1 analysis
---



### engine.js

1. 使用`document.querySelector('#glcanvas');`来选择一个标签，返回的对象还能继续query,使用css[选择器语法](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Selectors)

2. ```
   canvas.width vs gl.canvas.clientWidth
   canvas的逻辑pxcel数量   物理真正绘图所占大小
   ```

<img src="C:\Users\theda\AppData\Roaming\Typora\typora-user-images\image-20211022110139925.png" alt="image-20211022110139925" style="zoom:50%;" />

3. `window.addEventListener('resize', () => setSize(canvas.clientWidth, canvas.clientHeight));`

   窗口添加listener,其他标签canvas也能这么搞吗

4. 定义数组Array  `var a = [1,2,3]`
5. 用dat.gui.js实现[gui](http://www.yanhuangxueyuan.com/Three.js_course/datgui.html).

### loadOBJ.js

1. `import *  as THREE from '.....js'`

   或者直接`import {funcname} from 'sds'`

2. JS[导入](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/import)   [导出](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/export)配合，在html里面的按先后顺序执行，先执行的设置的全局变量可供后执行的使用。、我们也可以用import直接引入而不需修改HTML，但必须成对存在，没有export就没有import。