# flex.scss
> 兼容IE10，IE11等主流浏览器的flex布局

### 使用方法
1. 在对应的scss/css样式文件中引入
```
@import 'yourPath/flex.scss';
```
2. 使用常用布局时，直接`extend`即可
```
// 水平靠左，垂直居中
.example {
  @extend %flex-start-center;
}
```
等价于
```
.example {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
```
3. 非常用布局，使用`include`
```
.example {
  @include flex(1 0 auto);
}
```
等价于
```
.example {
  flex: 1 0 auto;
}
```
即
```
.example {
  flex-grow: 1;
  flex-shrink: 0;
  flex-base: auto;
}
```