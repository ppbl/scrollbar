# 自定义滚动条

基于-webkit-scrollbar原生实现的自定义滚动条样式  

scss代码改成css代码即可  

给需要使用的盒子一个固定的高度，加上对应的class即可

```scss
// 自定义滚动条~hover时显示
.beautiful-scroll-bar-hover {
  overflow-y: auto;
  &::-webkit-scrollbar {
    width: 10px;
  }
  &:hover {
    &::-webkit-scrollbar-thumb {
      background: #c6d0da;
    }
  }
  &::-webkit-scrollbar-thumb {
    border-radius: 10px;
    background: transparent;
    &:hover {
      background: #b5bec7;
    }
    &:active {
      background: #9ea1a5;
    }
  }
}

// 自定义滚动条~一直显示
.beautiful-scroll-bar {
  overflow-y: auto;
  &::-webkit-scrollbar {
    width: 10px;
  }
  &::-webkit-scrollbar-thumb {
    border-radius: 10px;
    background: #c6d0da;
    &:hover {
      background: #b5bec7;
    }
    &:active {
      background: #9ea1a5;
    }
  }
}
```