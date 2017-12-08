# chimee-plugin-gesture

>该插件是一个基础插件，移动端的插件可以继承它，为这些插件提供手势事件，暴露给上层插件使用

## install

安装

```shell
# 依赖于 chimee， 首先需要安装 chimee
npm install chimee
# 安装手势组件
npm install chimee-plugin-gesture
```

使用

```javascript
import chimee from 'chimee';
import gestureFactory from 'chimee-plugin-gesture';

// 安装插件
const mobiControlbar = gestureFactory({
  name: 'mobiControlbar',
})
chimee.install(mobiControlbar);
const player = new chimee({
  // ...
  // 使用插件
  plugin: [
    mobiControlbar.name // 或者 'mobiControlbar'
  ]
});
```

## 配置

chimee 配置 events 不用在监听 touchstart/ touchmove/touchend 事件中监听以下操作就好了，支持前缀 'w_'(wrap dom), 'c_'(container dom), 'd_'(插件自身 dom)

1. tap
2. swipe
3. press
4. panstart
5. panmove
6. panend
