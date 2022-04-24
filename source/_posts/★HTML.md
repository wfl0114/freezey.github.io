---
title: HTML
---

## 开发工具

### 浏览器（显示）

- 谷歌（chrome）、火狐（firefox）、IE、Safari、Opera
- 浏览器内核

  - 内核引擎

    - 渲染引擎
    - JS 引擎

  - 常见内核

    - Trident(IE) 、Gecko(firefox)、webkit(Safari) 、Chromium/Blink(chrome) 、 Presto(Opera)

- 移动端浏览器内核

  - Android

    - Webkit

  - IOS

    - Safari、Trident

### 编辑器（书写）

Sublime、Webstorm10、Visual Studio Code、HBuilder、Dreamweaver

sublime 快捷键

![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202111436603.png)

### PS / Sketch（辅助切图）

## 网页

### Web 标准

- 结构标准 - html（超文本标记语言）

- 表现标准 - css

- 行为标准 - Javascript

### HTML 骨架格式

```html
<html>
  <head>
    <title></title>
  </head>
  <body></body>
</html>
```

## HTML 标签

<标签 属性="值">

### HTML 标签分类

- 双标签
- 单标签

### HTML 标签关系

- 嵌套（包含）关系
- 并列关系

### 常用标签

- 标题标签

  ```html
  <h1></h1>
  <h2></h2>
  <h3></h3>
  <h4></h4>
  <h5></h5>
  <h6></h6>
  ```

- 段落标签

  ```html
  <p>文本内容</p>
  ```

- 水平线标签

  ```html
  <hr />
  ```

- 换行标签

  ```html
  <br />
  ```

- 没有语义的 div span 标签

  ```
  div 独占一行
  span 同行显示
  ```

- 文本格式化标签

  - 加粗

    ```html
    <strong></strong> <b></b>
    ```

  - 斜体

    ```html
    <em></em> <i></i>
    ```

  - 删除线

    ```html
    <del></del> <s></s>
    ```

  - 下划线

    ```html
    <ins></ins> <u></u>
    ```

  - 上标

    ```html
    <sup></sup>
    ```

  - 下标

    ```html
    <sub></sub>
    ```

### 图像标签 img

```html
<img src="图片URL" alt="替换文本" title="悬停时显示文本" width="宽" height="高" border="边框宽" />
```

### 超链接 a

```html
<a href="跳转目标" target="目标窗口的弹出方式">目标</a>
```

- 内链 < a href="index.html"> 目标 </a >
- 外链 < a href="http://www.baidu.com"> 目标 </a >
- 空链 < a href="#"> 目标 </a >

- 链接方式

  - href：指定链接目标的 url 地址
  - target：指定链接页面的打开方式

    - \_self 默认当前页面
    - \_blank 新页面

- base 标签内设置整体页面的打开方式

  ```html
  <head></head>中base标签 <base target="_blank" />
  ```

- 文本、图片、视频、音频等元素

### 锚点

- 设置锚点

  ```html
  <p id="标记">目标</p>
  ```

- 找到锚点

  ```html
  <a herf="#标记">目标</a>
  ```

### 路径

- 相对路径

  - 同级向下

  ```
  "img01/img02/img001.jpg"
  ```

  - 同级向上

  ```
  "../../img001.jpg"
  ```

- 绝对路径

  ```
  "D:\web\img\logo.gif"
  "http://www.itcast.cn/images/logo.gif"
  ```

### 特殊字符

![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202111609007.png)

### H5 扩展布局标签（语义化标签）

- 头部

  ```html
  <header></header>
  ```

- 导航

  ```html
  <nav></nav>
  ```

- 文章

  ```html
  <article></article>
  ```

- 侧边栏

  ```html
  <aside></aside>
  ```

- 区块

  ```html
  <section></section>
  ```

- 底部

  ```html
  <footer></footer>
  ```

- IE9 以下兼容处理

  - 创建自定义标签

    ```
    document.createElement('tagName')
    ```

  - 检测 IE 版本，加载第三方 JS 库

    ```html
    <!--[if lte IE 8]>
      <script src="./libs/html5shiv.min.js"></script>
    <![endif]-->
    ```

### H5 扩展音频标签

```html
<audio src="a.mp3"></audio>
```

- autoplay 自动播放
- controls 是否显不默认播放控件
- loop 循环播放
- 多浏览器解决方案:

  ![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202141023021.png)

  ```html
  <audio controls>
    <source src="a.mp3" />
    <source src="a.wav" />
    <source src="a.ogg" />
    您的浏览器版本过低,请升级
  </audio>
  ```

### H5 扩展视频标签

```html
<video src="a.mp4"></video>
```

- autoplay 自动播放
- controls 是否显示默认播放控件
- loop 循环播放
- width 设置播放窗口宽度
- height 设置播放窗口的高度
- 多浏览器解决方案:

  ![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202141024202.png)

  ```html
  <video>
    <source src="movie.mp4" />
    <source src="movie.ogg" />
    <source src="movie.webm" />
  </video>
  ```

## 列表

### 无序列表 ul

```html
<ul>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
  ......
</ul>
```

### 有序列表 ol

```html
<ol>
  <li>列表项1</li>
  <li>列表项2</li>
  <li>列表项3</li>
  ......
</ol>
```

### 自定义列表

```html
<dl>
  <dt>名词1</dt>
  <dd>名词1解释1</dd>
  <dd>名词1解释2</dd>
  ...
  <dt>名词2</dt>
  <dd>名词2解释1</dd>
  <dd>名词2解释2</dd>
  ...
</dl>
```

### 清除默认列表符号

```css
list-style: none;
```

## 表格

### 书写标准

```html
<table>
  <tr>
    <td>单元格内的文字</td>
    ...
  </tr>
  ...
</table>
```

### 表格属性

![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202141040005.png)

### 表格结构

- 表格的头部

  ```html
  <thead></thead>
  ```

- 表格的主体

  ```html
  <tbody></tbody>
  ```

- 表格的页脚

  ```html
  <tfoot></tfoot>
  ```

### 表头标签

位于第一行或者第一列，加粗且居中

```html
<th></th>
```

### 表格标题

紧随 table 标签后，居中表格之上

```html
<caption></caption>
```

### 表格边框合并（细线边框）

```css
border-collapse: collapse;
```

### 合并单元格

- rowspan 跨行合并（垂直方向的列合并）
- colspan 跨列合并（水平方向的行合并）

## 表单

在 HTML 中，一个完整的表单通常由表单控件（也称为表单元素）、提示信息和表单域 3 个部分构成

- 表单域（form）
  > 一个容器，容纳所有的表单控件和提示信息，上传后台服务器
- 提示信息
  > 说明性的文字
- 表单控件（表单元素）
  > 单行文本输入框、密码输入框、复选框、提交按钮、重置按钮等

### 表单域 form

```html
<form action="url地址" method="提交方式" name="表单名称">表单控件</form>
```

- 容器，容纳所有的表单控件和提示信息，上传后台服务器

- method 提交方式

  - get 默认通过地址栏，不安全
  - post 貌似安全
  - put
  - delete

### 输入框 input

![](https://gitee.com/wfl0114/image-hosting/raw/master/img/2022/202202141053381.png)

- <input />标签为单标签
- 多选 multiple
- 提示信息 placeholder="灰色字体内容"
- 默认选中项 checked="checked" 可简写为 checked
- :checked 表示检测选中的表单元素
- 单选按钮实现单选效果，将单选的 name 值设置相同，name="gender"
- 清除轮廓线 outline: none / 0;
- 获取光标焦点的状态 input: focus;
- H5 扩展表单元素

  - 输入邮箱格式

    ```html
    <input type="email" />
    ```

  - 输入手机号码格式

    ```html
    <input type="tel" />
    ```

  - 输入 url 格式

    ```html
    <input type="url" />
    ```

  - 输入数字格式

    ```html
    <input type="number" />
    ```

  - 输入日期

    ```html
    <input type="date" />
    ```

- H5 扩展表单属性

  - 占位符

    ```html
    <input type="text" placeholder="请输入用户名" />
    ```

  - 自动获得焦点

    ```html
    <input type="text" autofocus />
    ```

  - 自动完成

    ```html
    <input type="text" autocomplete="off（默认 on）" />
    ```

  - 必填项

    ```html
    <input type="text" required />
    ```

### 文本域 textarea

```html
<textarea cols="每行中的字符数" rows="显示的行数">文本内容</textarea>
```

- 多行文本输入框，双标签
- rows 行数
- cols 一行输入的字符长度
- resize 是否可以操作元素大小（css3）
  - none 不能调节尺寸
  - both 可以调节尺寸
  - horizontal 只可以调节宽度
  - inherit 只可以调节高度

### 下拉菜单 select

```html
<select>
  <option>选项1</option>
  <option>选项2</option>
  <option>选项3</option>
  ...
</select>
```

- selected = "selected" 默认选中项
- select 里至少要包含一项 option

### 标签 label

```html
<label for="male">Male</label><input type="radio" name="sex" id="male" value="male" />
```

绑定一个表单元素，点击获得输入焦点
