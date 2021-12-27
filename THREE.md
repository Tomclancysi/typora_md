1. `THREE.Object3D` 是所有3d物体的基类（Mesh，Scene，Group），scene也是。它们都可以作为树中的节点，obj loader返回结果就是棵树。想要修改scene，1通过traverse便利场景。通过scene remove函数，修改children数组（splice）。注意每次修改后需要设置对应属性的标记：

   ```js
   planeMesh.geometry.attributes.position.needsUpdate = true; //每次修改后更新位置
   ```

   每个object3D都有其对应的位置`.position`，旋转，缩放`.scale`，因此我们可以直接修改对应的属性值，实现修改，更新需要通知

2. box就是一个BufferGeometry（Geometry已经被淘汰），它的多个面可以使用数组分配不同的材质(这是通过`box.groups给不同的定点分配不同的materialIndex实现的`)。
3. 灯光使用上，light cast shadow， plane cast & receive shadow，`cam.shadow.camera`使用的正射投影，其参数需要设计。
4. UV一节中简述了怎么使用BufferAttribute给BufferGeometry赋属性值，`UV映射原理(顶点纹理坐标)`

5. learnopengl提到了漫反射、高光shininess参数、法线贴图，光照贴图等等



他们的代码都用到three的Stats 这是优化？？

反射很好实现cubecamera + envmap