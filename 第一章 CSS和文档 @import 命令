###前言
import命令使用的我平常碰见并不多，主要是使用link来引入样式，关于import的知识点，个人觉得更多是在于面试题中；
主要是区分import和link方式的区别，以及各自的有确定比较！
import语句需要放在css文件或者style标签中，且必须放在开头部分！

###import和link方式的细微差别：

1. **link属于XHTML标签，而@import完全是CSS提供的一种方式。** link标签除了可以加载CSS外，还可以做很多其它的事情，比如定义RSS，定义rel连接属性等，@import就只能加载CSS了。
2. **加载顺序的差别。**比如，在a.css中使用import引用b.css, 只有当使用当使用import命令的宿主css文件a.css被 被下载、解析之后，浏览器才会知道还有另外一个b.css需要下载，这时才去下载，然后下载后开始解析、构建render tree等一系列操作.
3. **兼容性的差别。**由于@import是CSS2.1提出的所以老的浏览器不支持，@import只有在IE5以上的才能识别，而link标签无此问题。
4. **当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的。**对于可换皮肤的网站而言，可以通过改变link便签这两个的href值来改变应用不用的外部样式表，但是对于import是无法操作的，毕竟不是标签。
 
      关于imoport标签，是不推荐使用的，从优化性能的角度看，应该尽量避免使用 @import 命令！
 
      至于为什么会影响细性能，的确是因为提到的第二点，加载顺序的问题，但是原因绝不是网上流传的“ 使用css @import， 相当于把import的css文件放在了页面底部，而是这样做会导致css无法并行下载”，而是import的css文件必须等宿主css下载完成，解析之后，浏览器才会去下载，解析import的css文件，** 因此css @import引起的css解析延迟会加长页面留白期。** 所以，要尽量避免使用css @import而尽量采用link标签的方式引入。
 
 
摘抄一位网友提供的外文文献 
> Avoid CSS @import 
>Overview 
 
>Using CSS @import in an external stylesheet can add additional delays during the loading of a web page. 
>Details 
 
>CSS @importallows stylesheets to import other stylesheets. When CSS @import isused from an external stylesheet, the >browser is unable to downloadthe stylesheets in parallel, which adds additional round-trip timesto the overall page load. >For instance, iffirst.css contains the following content: 
 
>@import url("second.css") 
 
>The browser must download, parse, andexecute first.css before it is able to discover that itneeds to downloadsecond.css. 
>Recommendations 
 
>Use the <link> tag instead of CSS @import 
>Instead of @import, use a <link> tag for each stylesheet. This allows the browser to download stylesheets in parallel, >which results in faster page load times: 
 
><link rel="stylesheet" href="first.css"> 
><link rel="stylesheet" href="second.css"> 
 
###参看文章链接
- <http://www.5icool.org/a/201306/a1898.html>
- <http://www.jb51.net/css/126892.html>
