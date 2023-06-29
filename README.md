# wx-miniprogram-note

## page 参数

```js
// 传递参数
wx.navigateTo({
  url: `page/index/index?id=${id}`
})
```

```js
// 接收参数
onLoad: function (options) {
  console.log(options.id)
}
```

## component 参数

```js
// 传递参数
<component-tag-name id="Some text"></component-tag-name>
```

```js
// 接收参数
Component({
  properties: {
    id: {
      type: String,
      value: 'default value',
    }
  },
  attached: function () {
    console.log(this.properties.id)
    // 也可以直接在 wxml 中使用 {{id}}
  }
})
```
