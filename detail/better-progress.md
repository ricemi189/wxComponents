# better-progress

仿 BootStrap 进度条组件

## 使用该组件

1、配置json

```json
{
  "usingComponents": {
    "better-progress": "/components/better-progress/index"
  }
}
```

2、基本视图层引入

> 目前该组件只有一个属性，那就是百分比，注意是不带 **%** 号的。

```html
<better-progress class="progress-bar-striped progress-bar-animated progress-bg-info" percentage="{{percentage}}"></better-progress>
```

3、高级视图层引入

`.progress-container` 和 `progress-tip` 都已经设置了默认样式，你也可以覆盖默认样式。

```html
<view class="progress-container">
  <better-progress class="progress-bar-striped progress-bar-animated" percentage="{{percentage}}"></better-progress>
  <view class="progress-tip">{{year}}年已经过去了{{percentage}}%</view>
</view>
```

4、自定义进度条样式

**进度条种类**

我这边提供了三种进度条，分别是基础进度条、条纹进度条、动画进度条，需要注意的是动画进度条是在条纹进度条的基础上实现的。

```html
<!--基本进度条-->
<better-progress percentage="{{percentage}}"></better-progress>
<!--条纹进度条-->
<better-progress class="progress-bar-striped" percentage="{{percentage}}"></better-progress>
<!--动画进度条-->
<better-progress class="progress-bar-striped progress-bar-animated" percentage="{{percentage}}"></better-progress>
```

**宽度设置：**

可以直接给组件设置行内样式 `style="height:50rpx"` 或者在css中按下面的设置：

```css
better-progress {
  height: 50rpx!important;
}
```

**背景颜色设置：**

背景颜色有两部分，一部分是整体进度条的颜色，一部分是已完成部分的背景色，那么我们怎么设置呢？

```css
/*整体背景色设置*/
better-progress {
  background-color: #d3d3d3!important;
}
/*已完成进度背景色设置*/
better-progress view {
  background-color: orange!important;
}
```

## 演示

![](http://cdn.wakeuptocode.me/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20180506212716.png)
