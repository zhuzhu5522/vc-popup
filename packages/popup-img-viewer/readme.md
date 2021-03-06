
## vc-popup-img-viewer

-----

模仿微信的图片浏览器~

### 添加依赖

```shell
> yarn add vc-popup-img-viewer || npm i vc-popup-img-viewer || cnpm i vc-popup-img-viewer --by=yarn
```

### 引入

```javascript
import Vue from 'vue'
import VcPopupImgViewer from 'vc-popup-img-viewer'
// 这里名字可以随意

Vue.use(VcPopupImgViewer)
```

### 在具体页面中使用

```javascript
this.imgViewer = new this.$popup.ImgViewer({
  ...config
  propsData: {}
})

this.imgViewer.open(e, {
  ...config
  propsData: {}
})

this.imgViewer.close()
```

> e为事件Event, 比如click时候取得的evt, 与一些定位方法相关
> config可参考[popup-base/readme.md](https://github.com/deepkolos/vc-popup/blob/master/packages/popup-base/readme.md)

### propsData配置定义

```js
{
  e: Object // 从open(e, {})传进来的e
  imgs: {   // img标签的数组
    type: [Array, HTMLCollection],
    required: true
  },
  loop: {   // 是否允许循环滑动
    type: Boolean,
    default: false
  },
  gap: {    // 图片之间的间隙
    type: Number,
    default: 16
  }
}
```

### 效果预览

<div>
  <img src="https://raw.githubusercontent.com/deepkolos/vc-popup/master/static/popup-img-viewer.gif" width = "250" alt="" style="display:inline-block;"/>
</div>

### License

MIT 一起来扣细节~
