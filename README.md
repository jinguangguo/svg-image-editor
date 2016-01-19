svg图片在线编辑
===================

提供图片的在线常用编辑功能,如——

> - 合并
> - 旋转
> - 放大
> - 缩小
> - 复制
> - 删除
> - 添加链接
> - 添加/编辑文本
> - 透明度
> - 另存为

后续还可以添加更丰富的功能,如丰富的字体库等,可参考[https://www.canva.com/](https://www.canva.com/)


### demo目录

```
app/page
├── h5pic-detail.html       # h5编辑页
├── h5pic-list.html         # h5编辑列表页
├── picEditor.html          # pc页
```


### 本地启动

安装

```
npm install
```

启动

```
gulp server:start
```

访问: [http://localhost:3000/app/page/picEditor.html](http://localhost:3000/app/page/picEditor.html)


### 本地构建

```
gulp deploy;
```



### svg相关知识

**1.基础API:**

> - [http://www.w3schools.com/svg/default.asp](http://www.w3schools.com/svg/default.asp)

**2.兼容性:**

> - PC端主要是IE8暂不支持，移动端主要是android2.3这等老版本浏览器不支持，不过可以优雅降级的方案，请参考[http://www.zhangxinxu.com/wordpress/2013/09/svg-fallbacks/](http://www.zhangxinxu.com/wordpress/2013/09/svg-fallbacks/)


**3.与后端的通信:**

> - 使用base64: 由svg变成canvas, 请参考[https://github.com/gabelerner/canvg](https://github.com/gabelerner/canvg), 然后再使用canvas的base64接口,请参考[https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/toDataURL](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/toDataURL)
> - 另存为: 提供给前端,window.location.href="base64OfImage"即可

**4.raphaeljs:**

svg基础封装库, 就如同jquery对js的封装

> - 参考[http://raphaeljs.com/](http://raphaeljs.com/)
> - API: [http://raphaeljs.com/reference.html](http://raphaeljs.com/reference.html)

**5.canvas和svg的比较**

Canvas
> - 依赖分辨率
> - 不支持事件处理器
> - 能够以 .png 或 .jpg 格式保存结果图像

SVG
> - 不依赖分辨率
> - 支持事件处理器
> - 复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）
