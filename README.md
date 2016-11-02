# **图片水平垂直居中**
[github link](https://github.com/ogoss/image-middle)
## 代码事例
- 基础样式
```
.container {
  position: relative;
  width: 300px;
  height: 300px;
  background-color: #e3e3e3;
}

img {
  width: 200px;
  height: auto;
}
```

- 使用背景图
```
<div class="container" id="m1"></div>
```

```
#m1 {
  background-image: url(pic1.jpg);
  background-repeat: no-repeat;
  background-position: center center;
  background-size: 200px auto;
}
```

- 使用绝对定位1
```
<div class="container"><img src="pic1.jpg" alt="" id="m2"></div>
```

```
#m2 {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}
```

- 使用绝对定位2
```
<div class="container"><img src="pic1.jpg" alt="" id="m3"></div>
```

```
#m3 {
  position: absolute;
  top: 50%;
  left: 50%;
  height: 142px;
  margin-top: -71px;
  margin-left: -100px;
}
```

- 使用表格样式
```
<div class="container" id="m4"><img src="pic1.jpg" alt=""></div>
```

```
#m4 {
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}
```

- 使用flex
```
<div class="container" id="m5"><img src="pic1.jpg" alt=""></div>
```

```
#m5 {
  display: flex;
}

#m5 > img {
  margin: auto;
}
```

- 使用transform
```
<div class="container"><img src="pic1.jpg" alt="" id="m6"></div>
```

```
#m6 {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

- 使用before伪类
```
<div class="container" id="m7"><img src="pic1.jpg" alt="" class="content"></div>
```

```
#m7 {
  text-align: center;
}

#m7:before {
  display: inline-block;
  height: 100%;
  content: '';
  vertical-align: middle;
}

#m7 > .content {
  display: inline-block;
  vertical-align: middle;
}
```
