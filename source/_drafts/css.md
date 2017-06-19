---
title: css
date: 2017-05-22 16:02:16
tags:
layout: false
---
![](http://upload-images.jianshu.io/upload_images/1768578-678f35e772132a47.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```css
font-family: Helvetica, Arial, sans-serif;
font-size: 60px;
text-transform: uppercase;  // 大写
text-decoration: underline;  // 下划线
color: #8001ff;
```
---

![](http://upload-images.jianshu.io/upload_images/1768578-ae3d31ed146b7798.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```css
border: 5px dashed salmon;
border-radius: 5px;
cursor: pointer;
box-shadow: 5px 5px 20px #ccc;
```

---

```css
display: block;  // 块元素
display: inline;  // 内联元素
```
`inline`, `weight` 和 `height` 无效。

---

```css
box-sizing: border-box;  // width 计算 padding 和 border
-webkit-box-sizing: border-box;
-moz-box-sizing: border-box;
-ms-box-sizing: border-box;
```

---

![](http://upload-images.jianshu.io/upload_images/1768578-470c41345887b0a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```css
text-align: justify;  // 左右对齐
```

---

垂直对齐

```css
vertical-align: top;
vertical-align: bottom;
vertical-align: middle;
```

---

行高

```css
line-height:1.2;
line-height:19.2px;
line-height:120%;
```

---

居中对齐

```css
margin: 0 auto;
```

---

```css
outline: 1px solid red  !important;  // border 外框，outline是不占空间的，既不会增加额外的width或者height，边框占用宽度
```

---

```css
@media only screen and (max-width: 300px) {
  /* style */
}
```

---

```css
img,
embed,
object,
video {
  max-width: 100%;
}
```

---

手指大约 40px，小屏按钮最小设置为 48 * 48px，两个之间最好空 40px

```css
min-height: 48px;
min-width: 48px;
```

---

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

```css
padding: 1.5em inhenit;
```

---

```css
display: flex;
flex-wrap: wrap;
```

---

```
calc(100px - 10%)
 *有效，* calc(100px-10%)
 *则无效
```

---

```css
`!important` 优先级最高

.testClass{
  color:blue !important;
}
```

---

你是否注意到，将 height
 和 width
 设置为 100vmax
 或 100vmin
 会如何改变图片的宽高比？它会将你的图片压缩成正方形，所以，如果你想要保留其他宽高比，请小心！

---

# 压缩、优化和自动化
开始编写你自己的自动化 ImageMagick 或 ImageOptim 工具前，你需要安装 [Node.js](https://nodejs.org/en/download/) 和 [npm](https://docs.npmjs.com/getting-started/installing-node)。 ImageMagick:
[ImageMagick](http://www.imagemagick.org/)
[Mac 上的一个简单的 ImageMagick 安装包](http://cactuslab.com/imagemagick/)
[GraphicsMagick](http://www.graphicsmagick.org/) (ImageMagick 的一个分叉)

Grunt:
[Grunt 简介](http://gruntjs.com/getting-started)
[Grunt 使用入门](http://24ways.org/2013/grunt-is-not-weird-and-hard/)
[用 Grunt 生成不同分辨率的图片](http://addyosmani.com/blog/generate-multi-resolution-images-for-srcset-with-grunt/)
[用于生成多张图片的 grunt-responsive-images 插件](https://github.com/andismith/grunt-responsive-images)
[用于响应式图片工作流的 grunt-respimg 插件](https://www.npmjs.com/package/grunt-respimg)

脚本编制示例中使用的文件：
[convert.sh](http://udacity.github.io/responsive-images/convert.sh) (含说明)
[Gruntfile.js](http://udacity.github.io/responsive-images/Gruntfile.js) (对于 Windows，移除第 7 行：engine: 'im',
)
[Imager.js](https://github.com/BBC-News/Imager.js/)：为 BBC 新闻开发的响应式图片加载。

图片处理工具：
[ImageOptim](http://imageoptim.com/) (Mac)
[Trimage](http://trimage.org/) - 和 ImageOptim 类似 (Windows, Mac, Linux)
[ImageAlpha](https://github.com/pornel/ImageAlpha)

# 图片压缩
[PageSpeed Insights 示例](https://developers.google.com/speed/pagespeed/insights/?url=simpl.info%2Fcssfilters)
[Grunt PageSpeed 插件](https://www.npmjs.com/package/grunt-pagespeed)
[PageSpeed Node module](https://github.com/addyosmani/psi/)
[cURL 示例](http://www.thegeekstuff.com/2012/04/curl-examples/)
[PageSpeed Insights Node module](https://github.com/addyosmani/psi/)

练习: 项目第 1 部分
请从 [此处](http://udacity.github.io/responsive-images/downloads/RI-Project-Part-1-Start.zip)下载项目文档。*
*请确保通过 localhost 运行项目。* 对于 Mac/Linux，请 cd
 至工作目录并设置一个[简单的 HTTP 服务器](http://www.linuxjournal.com/content/tech-tip-really-simple-http-server-python)。对于 Windows，请参见下文。
Make sure you are running the [Udacity Feedback Chrome Extension](https://chrome.google.com/webstore/detail/udacity-front-end-feedbac/melpgahbngpgnbhhccnopmlmpbmdaeoi) to get feedback. 确保你已经安装了[优达学城前端反馈插件](https://chrome.google.com/webstore/detail/udacity-front-end-feedbac/melpgahbngpgnbhhccnopmlmpbmdaeoi)。
*打开控制台，看看图片的总体积！*
[了解更多有关 figure 标签的信息！](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)

# 性能
延迟会什么会成为新的瓶颈？[看看 Ilya ](http://chimera.labs.oreilly.com/books/1230000000545/ch10.html#MORE_BANDWIDTH_DOESNT_MATTER_MUCH)在*高性能浏览器网络*中有什么要说的。请注意缩短延迟如何不断改善页面加载时间，而使带宽的图表趋于平缓：
![graph about latency](http://upload-images.jianshu.io/upload_images/1768578-826454c6055633cc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
要减少图片下载次数，你也可以使用 [CSS 图片精灵](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/CSS_Image_Sprites)或[响应式精灵](http://blog.brianjohnsondesign.com/responsive-background-image-sprites-css-tutorial/%EF%BC%89%E3%80%82[%E7%B2%BE%E7%81%B5%E9%A1%B5](https://www.google.co.uk/images/nav_logo195.png) 图片组合了大量图片，这些图片可以通过将精灵页设置为元素背景，然后通过 CSS 调整背景位置来单独显示。此技巧对图标和其他重复图形尤为有用。
**无论你采用何种技巧来避免延迟，都请注意 HTTP/2 带来的更改。**
简单地说，HTTP/2 表示请求多个文件的成本更小：准备停止使用脚本编写、连接和其他 HTTP/1 技巧！
如需了解更多信息，请查看[面向前端 Web 开发的 HTTP2](https://mattwilcox.net/web-development/http2-for-front-end-web-developers)。

---

CSS 背景图片
[Div with background image](http://udacity.github.io/responsive-images/examples/2-06/divWithBackgroundImage)
[CSS background-size: cover](http://udacity.github.io/responsive-images/examples/2-06/backgroundSizeCover)
[Body with background image](http://udacity.github.io/responsive-images/examples/2-06/bodyWithBackgroundImage)
[Body with background image and gradient](http://udacity.github.io/responsive-images/examples/2-06/bodyWithBackgroundImageAndGradient)
[Body with elaborate background using only CSS](http://udacity.github.io/responsive-images/examples/2-06/bodyWithElaboratePatternPureCSS)
[Using CSS background images for conditional image display](http://udacity.github.io/responsive-images/examples/2-06/backgroundImageConditional)
[Using CSS background images for alternative images](http://udacity.github.io/responsive-images/examples/2-06/backgroundImageAlternative)
[image-set()](http://udacity.github.io/responsive-images/examples/2-06/imageSet)

---

```css
background-color: cover;
background-color: contain;
```

---

符号字符
例子：[Unicode 代替图片](http://udacity.github.io/responsive-images/examples/2-08/unicodeStar)
[Unicode 字符集](http://unicode-table.com/en/sets/)
[Unicode 符号集合](http://en.wikipedia.org/wiki/List_of_Unicode_characters)

---

图标字体
[Zocial](http://zocial.smcllns.com/)
[Font Awesome](http://fortawesome.github.io/Font-Awesome/)
[We Love Icon Fonts!](http://weloveiconfonts.com/)
[Icon fonts on CSS-Tricks](https://css-tricks.com/examples/IconFont/)

---

SVG 和数据 URI 行内图片
例子：
[SVG Data URI in HTML](http://udacity.github.io/responsive-images/examples/2-11/svgDataUri)

[SVG Data URI in CSS](http://udacity.github.io/responsive-images/examples/2-11/svgDataUriCss)

[SVG text on a path](http://udacity.github.io/responsive-images/examples/2-11/svgTextOnAPath)

[SVG optimized and unoptimized](http://udacity.github.io/responsive-images/examples/2-11/svgUnoptimisedAndOptimised)

---

示例：
[srcset with w values](http://udacity.github.io/responsive-images/examples/3-03/srcsetWValues)
[srcset with w values, 50vw](http://udacity.github.io/responsive-images/examples/3-03/srcsetWValues50vw)

---

Sizes 属性
示例：
[srcset with w values](http://udacity.github.io/responsive-images/examples/3-03/srcsetWValues)
[srcset with w values, 50vw](http://udacity.github.io/responsive-images/examples/3-03/srcsetWValues50vw)

---

srcset 和 sizes 练习
我想总结你刚刚学习的关于图片属性 srcset
 和 sizes
 的内容。 你可以借此机会先详细了解每个属性的语法，然后在下面两道测试题中，在真正的页面上尝试使用它们。
在本测试题中，你将尝试使用 srcset
。在下一道测试题中，你将添加 sizes
，以便为浏览器提供更多信息。
语法
srcset
 有两种自定义方式，一种使用 x
 来区分设备像素比 (DPR)，另一种使用 w
 来描述图像的宽度。
对设备像素比的反应
<img src="image_2x.jpg" srcset="image_2x.jpg 2x, image_1x.jpg 1x" alt="a cool image">

将 srcset
 设置为与逗号分隔的一连串 filename multiplier
 对相等，其中每个 multiplier
 必须是后跟 x
 的整数。
例如，1x
 表示 1 倍显示屏，2x
 表示像素密度为两倍的显示屏，如 Apple 的 Retina 显示屏。
浏览器会下载与其 DPR 对应的最佳图片。
另请注意，有一个作为备用的 src
 属性。
对图片宽度的反应
<img src="image_200.jpg" srcset="image_200.jpg 200w, image_100.jpg 100w" alt="a cool image">

将 srcset
 设置为与逗号分隔的一连串 filename widthDescriptor
 对相等，其中每个 widthDescriptor
 都以像素为测量单位， 并且必须是后跟 w
 的整数。在这里，widthDescriptor
 指定每个图片文件的自然宽度，使浏览器能够根据窗口大小和 DPR 选择要请求的最适当的图片。 （如果没有 widthDescriptor
，浏览器需要下载图片才能知道其宽度！）
另请注意，有一个作为备用的 src
 属性。
准备好尝试一下？单击“继续”试试吧！

Here are my finished image tags:
DPR (海牙)
<img class="dpi" src="images/Den_Haag_2x.jpg" srcset="images/Den_Haag_2x.jpg 2x, images/Den_Haag_1x.jpg 1x" alt="Den Haag Skyline">

请注意我如何获得 src
 作为备份。srcset
 中的来源顺序无关紧要。此外，如果你遗漏了乘数，它将默认为 1x
，也就是说，
srcset="images/Den_Haag_2x.jpg 2x, images/Den_Haag_1x.jpg 1x"

等同于：
srcset="images/Den_Haag_2x.jpg 2x, images/Den_Haag_1x.jpg"

图片宽度（澳大利亚）
<img class="w" src="images/Australia_1280w.jpg" srcset="images/Australia_1280w.jpg 1280w, images/Australia_640w.jpg 640w" alt="Australia from Space">

同样地，会出现 src
 备份，你可以切换 srcset
 中的图片顺序。

包含大小的图片宽度
如果图片不以全窗口宽度显示会怎样？那么，除了 srcset
 外，你还需要其他元素（假设图片将为全窗口宽度）
向包含媒体查询的图片添加一个 sizes
 属性和一个 vw
 值。srcset
 和 sizes
 合起来可让浏览器知道图片的自然宽度以及图片相对于窗口宽度的显示宽度。 知道图片的显示宽度和可用图片文件的宽度后，浏览器将获得下载具有满足其需求的适当分辨率且尽可能小的图片所需的信息。 而且，浏览器在页面加载初期，解析 HTML 时即可做出此选择。
srcset 与 sizes 配合使用的语法
这里是一个示例：
<img src="images/great_pic_800.jpg" sizes="(max-width: 400px) 100vw, (min-width: 401px) 50vw" srcset="images/great_pic_400.jpg 400w, images/great_pic_800.jpg 800w" alt="great picture">

sizes
 由以逗号分隔的 mediaQuery width
 对组成。sizes
 会在加载流程初期告诉浏览器，该图片会在点击 mediaQuery
 时以某个 width
 显示。
实际上，如果 sizes
 缺失，浏览器会将 sizes
 默认为 100vw
，表示它预计图片将以全窗口宽度显示。
sizes
 会为浏览器额外提供一条信息，以确保它根据图片的最终显示宽度下载正确的图片文件。说明一下，它实际上*不会*调整图片的大小 - 这是 CSS 的工作。
在本示例中，如果浏览器的窗口宽度等于或小于 400 像素，浏览器知道图片将为全窗口宽度；如果窗口宽度大于 400 像素，则为一半窗口宽度。浏览器知道它具有两个图片选项 - 一个具有 400 像素的自然宽度，另一个具有 800 像素。
准备好帮助浏览器了？单击“继续”亲自试试吧！

这里是我已完成的图片标记：
<img class="w" src="images/Coffee_1280w.jpg" srcset="images/Coffee_1280w.jpg 1280w, images/Coffee_640w.jpg 640w" sizes="(max-width: 960px) 50vw, 100vw" alt="Coffee by Amy March from Turkey">

我没有在 sizes
 中包括第二个媒体查询，因为如果没有媒体查询，列出的宽度会被视为默认值。
另外请注意，sizes
 中的媒体查询与 CSS 匹配。说明一下，更改 sizes
 不会影响 CSS。它只会提醒浏览器注意最终需要在该处显示的图片。

---

网络广播从最初在系统上设置 Grunt 开始， 一直讲到设置完整的项目流程。
此处链接为 [关于此网络广播的详细论坛文章 ](https://discussions.udacity.com/t/grunt-and-setting-up-a-grunt-workflow-intermediate/21984)。 文章中包含对 Grunt 安装配置和设置任务 的相关向导。
此处链接为 [在网络广播中使用的 GitHub 存储库 ](https://github.com/JohnUdacity/grunt-workflow-guide)。
有关网络广播的详细整理，请访问 [此处](https://github.com/udacity/fend-office-hours/tree/master/Front%20End%20Tools/Gulp).

---

设置 Gulp 工作流演示（概要）
由学习教练 John 主讲，有关如何设置 Gulp 的现场演示。
Gulp 可代替前端开发人员完成所有必需的繁琐、 重复性任务：压缩、串联、lint 操作、 图像优化、Git 提交等多种任务， 都可以交由 Gulp 来实现。从而让你能够集中精力处理重要任务，也就是 编写代码。
网络广播从最初在系统上设置 Gulp 开始， 一直讲到设置完整的项目流程。
要查看网络广播的详细概要（包括代码 段），请参阅此 [论坛 文章](https://discussions.udacity.com/t/gulp-and-setting-up-a-gulp-workflow-intermediate/24359).
如果想要跟随演示学习，请在 [此存储库](https://github.com/JohnUdacity/gulp-start) 中下载起始代码。
有关网络广播的详细整理，请访问 [此处](https://github.com/udacity/fend-office-hours/tree/master/Front%20End%20Tools/Gulp).
