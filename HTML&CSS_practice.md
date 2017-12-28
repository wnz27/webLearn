# HTML&CSS
## 使用CSS选择器定义标签
使用CSS，您可以使用数百种CSS属性来更改元素在页面上的显示方式。
当你输入`<h2 style="color: red">CatPhotoApp</h2>`时，你就给h2元素添加了inline style(内联样式)。
这是添加元素的样式的一种方法，但更好的方法是使用CSS，它代表(Cascading Style Sheets)层叠样式表。
在代码的顶端，创建一个如下所示的style元素，：
```
<style>    
</style>
```
在这个style元素的内部, 你可以为所有h2元素创建一个CSS选择器。例如，如果你希望所有的h2元素都设置为红色, 则你的样式元素将如下所示：
```
<style>    
  选择器 {属性名称: 属性值;}    
  h2 {color: red;}    
</style>
```
请注意，围绕每个元素的样式，打开和关闭花括号 ({ 和}) 很重要。您还需要确保元素的样式位于开始和结束样式标签之间。最后，请确保将分号添加到每个元素样式的末尾。
删除你的h2元素的样式属性，而不是创建一个CSSstyle元素。添加必要的CSS，以将所有h2元素变为蓝色。
```
<style>
h2 {
color: blue;
}
</style>
<h2>html编程入门教程</h2>
<p>在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情。</p>
```
## 使用一个CSS Class去给标签定义Style
类是可重用的样式，可以添加到HTML元素。
下面是一个CSS类声明的例子：
```
<style>    
  .blue-text {    
    color: blue;    
  }    
</style>
```
你可以看到我们已经在 <style> 标签中创建了一个名为 blue-text 的CSS类。
你可以将类应用于HTML元素，如下所示：
`<h2 class="blue-text">CatPhotoApp</h2>`
请注意，在CSS样式元素中，类选择器应该添加`.`为前缀。而在HTML元素的类声明中，类属性不能添加`.`为前缀。
在你的style元素中，将h2选择器修改为`.red-text`选择器，并将颜色值从blue修改为red。
最后，给你的 h2 元素的 class 属性的值为`.red-text`。
```
<style>
.red-text{
    color:red;
}
</style>
<h2 class="red-text">html编程入门教程</h2>
<p>在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
```
## HTML 为多个元素使用CSS类定义样式
请记住，你可以通过在相关元素的开始标签中使用 `class="your-class-here"`将类附加到HTML元素。
记住，CSS类选择器在开始时需要添加 . 为前缀，如下所示：
```
.blue-text {    
  color: blue;    
}
```
但是还要记住，在HTML中class属性的值不需要添加` . `为前缀，如下所示：
`<h2 class="blue-text">CatPhotoApp</h2>`
将 red-text 类应用于你的 h2 和 p 元素中。
```
<style>
.red-text {
color: red;
}
</style>
<h2 class="red-text">html编程入门教程</h2>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
```
## HTML 设置标签的字体大小
字体大小由 font-size CSS属性控制，如下所示：
```
h1 {    
  font-size: 30px;    
}
```
在现有 p 元素之后创建第二个 p 元素，并使用以下文本：
> 养动物有的时候，就是介于爱与恨之间，当你钦羡别人萌宠这么可爱的时候，你一定没有想过，狗狗和猫猫会到处拉屎，甚至会屯老鼠，啃鞋子，用爪子爬门，你不理它，它就挠你，你要对它发脾气，它会比你更来劲。所以，狗猫慎入，没有一定的准备，切勿随便去侍养动物。它们一旦认定你了，你就是它们的主人，如果你抛弃它们，它们必定心中重创。
在包含 red-text 类的同一 <style> 标签内，为 p 元素创建一个 font-size 属性，并将 font-size 设置为16像素（16px）。
任务：将第一个段落和第二个段落的 font-size 设置为 16px。
另外，请不要为第二个段落添加 class 属性。
```
<style>
  .red-text {
    color: red;
  }
  p {
      font-size: 16px
  }
</style>
<h2 class="red-text">我家的猫咪</h2>
<p class="red-text">在大家心目中，猫是慵懒的可爱的化身，它可以睡饱了再起来吃饭，可以逗趣小耗子，可以卖得了萌，使得了坏，这样百变的小怪兽就集结在一只宠物上，怎能不惹人怜爱。</p>
<p>养动物有的时候，就是介于爱与恨之间，当你钦羡别人萌宠这么可爱的时候，你一定没有想过，狗狗和猫猫会到处拉屎，甚至会屯老鼠，啃鞋子，用爪子爬门，你不理它，它就挠你，你要对它发脾气，它会比你更来劲。所以，狗猫慎入，没有一定的准备，切勿随便去侍养动物。它们一旦认定你了，你就是它们的主人，如果你抛弃它们，它们必定心中重创。</p>
```
## HTML 设置标签的字体样式
你可以使用 font-family 属性来设置元素的字体。
例如，如果要将 h2 元素的字体设置为 Sans-serif ，则可以使用以下CSS：
```
h2 {    
  font-family: Sans-serif;    
}
```
使不包含 red-text类的p元素都使用Monospace字体。
```
<style>
.red-text {
color: red;
}
.fon-text{
    font-family: Monospace
}
p {
font-size: 16px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="fon-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## 引入Google字体
现在, 让我们引入并应用 google 字体 (请注意, 如果 google 在你的国家被阻止, 你需要跳过这一挑战)。
首先，你需要用 link 标签来引入谷歌Lobster字体。
复制以下代码段并将其粘贴到代码编辑器的顶部：
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
```
现在，你可以将 Lobster 作为 font-family属性 的值应用于你的 h2 元素上。
将你的 h2 元素应用 font-family 属性，值为Lobster。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2{
    font-family: Lobster
}
p {
font-size: 16px;
font-family: Monospace;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 处理多个字体降级
在所有浏览器中都有几种可用的默认字体。这些包括 Monospace 、Serif 和 Sans-Serif。
当某种字体不可用时，你可以让浏览器将其 “降级” 为另一种字体。
例如，如果你希望元素使用 Helvetica 字体，但是当 Helvetica 不可用时也会降级为Sans-Serif 字体，则可以使用此CSS样式：
```
p {    
  font-family: Helvetica, Sans-Serif;    
}
```
现在，你可以注释掉对Google字体的使用，注释掉link标签，以使 Lobster 字体不可用。请注意观察它是如何降级为 Monospace 字体的。
```
<!--
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
-->
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 给页面添加图片
你可以使用 img 元素将图片添加到您的网站，并使用 src 属性指向一个图片的具体地址。
例子如下：
`<img src="https://www.your-image-source.com/your-image.jpg">`
img 元素具有 alt 属性。alt 属性中的文本用于屏幕阅读器以提高可访问性，并且如果图像无法加载，则会显示。
让我们在上面的 img 示例中添加一个 alt 属性：
```
<img src="https://www.your-image-source.com/your-image.jpg" alt="your-image">
```
请注意，img 元素是自关闭元素，不需要结束标签。
请用以下图片来测试：
`/statics/codecamp/images/relaxing-cat.jpg`
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
</style>
<h2 class="red-text">html编程入门教程</h2>
<img src="/statics/codecamp/images/relaxing-cat.jpg" alt="your image">
<p class="red-text">猫咪猫咪我就喜欢你</p>
<p class="red-text">深深地爱上你</p>
<p class="red-text">没有理由没有原因</p>
<p class="red-text">从见到你的那一天起</p>
<p class="red-text">你知道我在等你吗?</p>
<p class="red-text">你如果真的在乎我</p>
<p class="red-text">又怎会让无尽的夜陪我度过</p>
<p class="red-text">猫咪猫咪我就喜欢你</p>
<p class="red-text">深深地爱上你</p>
<p class="red-text">在黑夜里倾听你的声音</p>
```
## HTML 调整网页里图片大小
CSS包含一个 width 的属性，用于控制元素的宽度。就像使用字体一样，我们将使用 px（像素）来指定图片的宽度。
例如，如果我们要创建一个名为 larger-image 的CSS类，把HTML元素的宽度设定为500像素，我们将使用：
```
<style>    
  .larger-image {    
    width: 500px;    
  }    
</style>
```
任务：创建一个名为smaller-image的类，并使用它来调整图片的大小，使其只有100像素宽。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.smaller-image {
    width: 100px
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<img class="smaller-image" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 给标签增加边框
CSS 边框具有 style(样式)、color(颜色)、width(宽度) 等属性。
例如，如果我们想要设定一个HTML元素的边框颜色为红色、边框宽度为5像素(px)、边框样式为实线(solid)，代码如下所示:
```
<style>    
  .thin-red-border {    
    border-color: red;    
    border-width: 5px;    
    border-style: solid;    
  }    
</style>
```
任务：创建一个叫 thick-green-border的class，设定它的边框宽度为10px、边框样式为solid、边框颜色为绿色，并将该class应用于你的猫咪照片上。
请记住，你可以应用多个class到一个元素，只需要在多个class之间用空格分开即可。例如：
`<img class="class1 class2">`
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.smaller-image {
width: 100px;
}
.thick-green-border {
  border-width:10px;
  border-style:solid;
  border-color:green;   
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 给标签增加圆角边框
猫咪图片的边框目前有尖角。我们可以用一个叫 border-radius（边框半径）的CSS属性来改变它的边框变成圆角。
你可以使用像素来指定 border-radius 的属性值，给你的猫咪图片的 border-radius 设定为10px。
注意：这个任务允许有多种解决方案。例如，你可以添加border-radius到 `.thick-green-border `类或 `.smaller-image` 类。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 10px
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">html编程入门教程</h2>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">我家两岁的小公猫哈哈是个收藏家，臭鱼烂虾，鸡头猪手，无所不爱。清晨我还在睡梦中，突然觉得胸口一沉，恍惚中意识到哈哈又跑到我身上来撒娇，心里不由得滚起温暖的热流，拉过哈哈一把从头摸过背，小家伙顺势想往被子里钻，我一边拒绝着一边往上拉被子，突然脚下一凉，烂泥一样挂在我的大脚趾上的是一块垃圾箱里的鱼头！我顿时睡意全无，换床单洗被罩，天光放亮才勉强收拾妥当。害得我带着熊猫眼跑去上班，一天都没有好心情。实在搞不懂它为什么爱把垃圾叼上床，是故意恶作剧？还是我给的猫粮不够吃？</p>
<p class="red-text">有时候猫会把主人当成自己的孩子(听起来有点令人窝心)，这种行为是在给家里带来猎物。它把自己看成是家里的顶梁柱，有责任给不争气的主人找来食物——猫咪通过长时间对你的观察，沉痛地发现你不会打猎。经常出门的猫咪会把它逮到的老鼠、小鸟带回家里，不出门的就经常翻翻垃圾箱找点东西给你。这个时候，主人可不要责骂它，不然它会认为你对它带回来的食物不满意，下次去找更了不起的东西带回来，放在房间里最显眼的地方。但如果你看见它往家里运输死老鼠，最好也别谢它，别让它觉得你对这种猎物很满意，下次照单带回来。最好的办法是心里感念着猫咪所为你做的，并默默地收拾好一切。</p>
```
## HTML 给图像设置圆角边框
除了像素之外，你还可以使用百分比来指定 border-radius（边框半径）的值。
给你的猫咪图片设定 border-radius 为 50%。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 设置链接锚元素外部页面
a元素，也叫anchor（锚点）元素，用于链接到当前页面之外的内容。
下面是一张a元素的图示。在这种情况下，a元素位于段落元素的中间使用，这意味着链接将出现在段落的中间。
[image:CA91F90C-CCC1-4094-9D78-234C67436B28-285-000031DE4F4A80EB/1498550568787494.png]
以下是一个例子：
```
<p>这是一个a标签 <a href="https://www.w3cschool.cn">W3Cschool.cn</a>跳转到W3Cschool.cn</p>
```
任务：创建一个链接到`http://freecatphotoapp.com的a元素`，并将cat photos作为其anchor text（锚文本）。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<a href="http://freecatphotoapp.com">cat photos</a>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 在p标签内设置锚链接
Nesting（嵌套）就是把一个元素放在另一个元素中。
例如：
```
<p>Here's a <a href="https://www.w3cschool.cn"> link to W3Cschool.cn</a> for you to follow.</p>
```
任务：现在把你的a元素嵌入进一个新的p元素（在现有的h2元素之前），让段落的文本显示为View more cat photos，但只有cat photos是一个链接，其余的文字是纯文本。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
<p>View more <a href="https://www.w3cschool.cn">cat photos</a></p>
```
## HTML 使用#符合设置固定链接
有时你想要在你的网站上添加一个 a 元素，但你还不知道将它链接到哪里，这时你可以使用固定连接。
当你使用 jQuery 更改链接的行为时，这也很方便，我们稍后将会了解。
把 a 元素的 href 属性的值替换为一个 # （# 也称为哈希符号），将其转换为一个固定链接。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p>Click here for <a href="#">cat photos</a>.</p>
<img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg">
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 为图片设置超链接
你可以通过将某元素嵌套在a元素中使其变为一个链接。
把你的图片嵌入到a元素中。例子如下：
`<a href="#"><img src="/images/relaxing-cat.jpg"></a>`
请记住使用 # 作为元素的 href 属性, 以便将其转换为固定链接。
将现有的图像元素放置在锚点元素中。
完成后，把你的光标悬停在你的图片上。此时光标应该由光标指针变成手形指针。这张图片现在是一个链接了。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p>Click here for <a href="#"><img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg"></a>.</p>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 为图片添加alt描述
alt 属性,是当图片无法显示时的替代文本。alt 属性对于盲人或视觉障碍的用户理解图片中的内容非常重要，搜索引擎也会搜索alt 属性来了解图片的内容。
总而言之，alt 属性是一个必需的属性，为页面上的图片都加上 alt 属性是好习惯。
你可以像下面例子中一样为img元素添加一个alt属性：
```
<img src="www.your-image-source.com/your-image.jpg" alt="your alt text">
```
为你的猫咪图片添加一个 alt 属性，内容为A cute orange cat lying on its back。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p>Click here for <a href="#">cat photos</a>.</p>
<a href="#"><img class="smaller-image thick-green-border" src="/statics/codecamp/images/relaxing-cat.jpg" alt="A cute orange cat lying on its back"></a>
<p class="red-text">在大家心目中，也许编程是一件非常困难的事情，其实也是一件非常有乐趣的事情，只要掌握好编程入门的方法，就能慢慢进入一个全新的创造世界。</p>
<p class="red-text">可以学习的编程语言有很多，我们这个编程训练营里面有大量的编程实战实验，包括Html、css、Javascript、jquery、bootstrap等等前端编程实战课程，请大家耐心按阶段不断向前学习和通过一轮一轮的挑战，相信很快您的编程技术会得到很大的提升，为找到一份好的编程工作做好准备。</p>
```
## HTML 创建项目符号无序列表
HTML具有用于创建 ~**unordered lists（无序列表）**~ ，或带项目符号列表的特殊元素。
无序列表以 <ul> 元素开始，并包含一个或多个<li>元素。
例如：
```
<ul>    
  <li>milk</li>    
  <li>cheese</li>    
</ul>
```
将会创建一个带项目符号的"milk"和"cheese"列表。
删除最后两个 p 元素，并在页面底部创建一个有关猫咪喜欢的三件事情的无序列表。
```
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
<style>
.red-text {
color: red;
}
h2 {
font-family: Lobster, Monospace;
}
p {
font-size: 16px;
font-family: Monospace;
}
.thick-green-border {
border-color: green;
border-width: 10px;
border-style: solid;
border-radius: 50%;
}
.smaller-image {
width: 100px;
}
</style>
<h2 class="red-text">CatPhotoApp</h2>
<p>Click here for <a href="#">cat photos</a>.</p>
<a href="#"><img class="smaller-image thick-green-border" alt="A cute orange cat lying on its back" src="/statics/codecamp/images/relaxing-cat.jpg"></a>
<ul>
    <li>milk</li>
    <li>cheese</li>
    <li>eggs</li>
</ul>
```
  
## HTML 创建有序列表
HTML具有用于创建 ~**ordered lists（有序列表）**~, 或数字编号列表的特殊元素。
有序列表以<ol>元素开始，并包含一个或多个<li>元素。
例如：
```
<ol>    
  <li>Garfield</li>    
  <li>Sylvester</li>    
</ol>
```
将创建一个包含"Garfield"和"Sylvester"的数字编号列表。
创建一个有关 “Top 3 things cats hate:” （猫咪不喜欢三件事情）的有序列表。
```
<p>Things cats love:</p>
<ul>
<li>cat nip</li>
<li>laser pointers</li>
<li>lasagna</li>
</ul>
<p>Top 3 things cats hate:</p>
<ol>
    <li>Garfield</li>
    <li>Sylvester</li>
    <li>Quiet</li>
</ol>
```
## HTML 创建文本输入框
现在我们来创建一个Web表单。
文本输入框是获取用户输入的一种方便的方法。
你可以用如下方法创建：
`<input type="text">`
注意，input元素是自关闭的。
任务：在列表下创建一个type（类型）为 text 的input元素。
`<input type="text">`
## HTML 为文本输入框设定预定值
placeholder text（占位符）是用户在 input 框输入任何内容之前放置在 input 框中的预定义文本。
你可以创建如下所示的占位符：
<input type="text" placeholder="this is placeholder text">
将文本 input 框的placeholder的值设置为"cat photo URL"。
`<input type="text" placeholder="cat photo URL">`


## HTML 添加表单
你可以使用HTML来构建跟服务器交互的Web表单。你可以通过在form元素上添加一个action属性来执行此操作。
action属性的值指定了表单提交到服务器的地址。
例如：
`<form action="/url-where-you-want-to-submit-form-data"></form>`
把你的文本输入框嵌套到form元素中。并为此form元素添加`action="/submit-cat-photo"`。
```
<form action="/submit-cat-photo">
<input type="text" placeholder="cat photo URL">
</form>
```

## HTML 为表单添加提交按钮
我们在form中添加一个 submit (提交)按钮。点击此按钮，表单中的数据将会被发送到你使用表单 action 属性指定的地址上。
以下是一个submit按钮的例子：
`<button type="submit">this button submits the form</button>`
在你的 form 元素中添加一个提交按钮，并以类型为 submit， "Submit"为按钮文本。
```
<form action="/submit-cat-photo">
<input type="text" placeholder="cat photo URL">
<button type="submit">Submit</button>
</form>
```


## HTML 使用HTML5技术把表单设置为必填
对于表单，你可以指定某些选项为required（必填项），只有当用户填写了该选项后，用户才能够提交表单。
例如，如果你想要一个文本输入框设置为必填项，你可以在 input 元素中加上 required 属性，你可以使用： 
`<input type="text" required>`
任务：给你的文本输入框添加 required属性，这样用户不填写输入框就无法提交表单。
然后尝试不填写任何文本就提交表单。了解你的浏览器如何提示你该字段是必填项？
注意：required属性在Safari浏览器中不起作用，请用其他浏览器来练习学习。
```
<form action="/submit-cat-photo">
<input type="text" placeholder="cat photo URL" required>
<button type="submit">Submit</button>
</form>
```

## HTML 添加单选框
你可以使用单选按钮来解决你希望用户只给出一个答案的问题。
单选按钮是 input 输入框的一种类型。
每个单选按钮都应该嵌套在自己的 label(标签) 元素中。
所有关联的单选按钮应具有相同的 name 属性。
下面是一个单选按钮的例子：
`<label><input type="radio" name="indoor-outdoor"> Indoor</label>`
在你的表单中添加两个单选按钮，一个叫 indoor，另一个叫 outdoor。
```
<form action="/submit-cat-photo">
<label>
    <input type="radio" name="indoor-outdoor" placeholder="cat photo URL" required>indoor
</label>
<label>
   <input type="radio" name="indoor-outdoor">outdoor
</label>
<button type="submit">Submit</button>
</form>
```

## HTML 添加复选框
`checkboxes（复选按钮）`通常用于可能有多个答案的问题的形式。
复选按钮是 input 的输入框的一种类型。
每一个复选按钮都应嵌套在其自己的 label元素中。
所有关联的复选按钮输入应该具有相同的 name属性。
以下是一个复选按钮的示例：
`<label><input type="checkbox" name="personality"> Loving</label>`
任务：为你的表单添加三个复选按钮，每个复选按钮都应嵌套在其自己的 label 元素，所有复选按钮的name属性必须为personality。
```
<form action="/submit-cat-photo">
<label><input type="radio" name="indoor-outdoor"> Indoor</label>
<label><input type="radio" name="indoor-outdoor"> Outdoor</label>
<input type="text" placeholder="cat photo URL" required>
<label><input type="checkbox" name="personality">am</label>
<label><input type="checkbox" name="personality">you</label>
<label><input type="checkbox" name="personality">it</label>
<button type="submit">Submit</button>
</form>
```

## HTML 使用checked属性设置复选框和单选框默认被选中
使用 checked 属性，你可以设置一个单选框和复选框默认被选中。
为此，只需在 input 元素中添加属性checked 。例如：
`<input type="radio" name="test-name" checked>`
设置你的第一个单选框和第一个复选框都为默认选中。
```
<form action="/submit-cat-photo">
<label><input type="radio" name="indoor-outdoor" checked=""> Indoor</label>
<label><input type="radio" name="indoor-outdoor"> Outdoor</label>
<label><input type="checkbox" name="personality" checked=""> Loving</label>
<label><input type="checkbox" name="personality"> Lazy</label>
<label><input type="checkbox" name="personality"> Energetic</label>
<input type="text" placeholder="cat photo URL" required>
<button type="submit">Submit</button>
</form>
```

## HTML 在div元素中嵌套多个元素
**div 元素**，也被称作`division(层)元素`，是一个盛装其他元素的通用容器。
div 元素是最常用的HTML元素。所以可以利用CSS的继承关系把 div 上的CSS传递给它所有子元素。
你可以使用<div>来标记一个div元素的开始，并使用</div>来标记一个div元素的结束。
尝试在你的"Things cats love" p元素之前放置div的开始标记，在你的ol结束标记之后放置div的结束标记，这样你的两个列表就都嵌套在div中了。
把"Things cats love"和"Things cats hate"两个列表都嵌套在同一个div元素中。
```
<div>
<p>Things cats love:</p>
<ul>
<li>cat nip</li>
<li>laser pointers</li>
<li>lasagna</li>
</ul>
<p>Top 3 things cats hate:</p>
<ol>
<li>flea treatment</li>
<li>thunder</li>
<li>other cats</li>
</ol>
</div>
```

## HTML 为div元素设置背景颜色
你可以使用 `background-color`属性来设置一个元素的背景颜色。
例如，如果你想要设置一个元素的背景颜色为green，你可以将其放在你的 style 元素中：
```
.green-background {    
  background-color: green;    
}
```
创建一个叫 gray-background 的类选择器，设置其 background-color 为 gray，最后应用到你的 div 元素。
```
<style>
.gray-background{
    background-color: gray
}
</style>
<div class="gray-background">
<p>Things cats love:</p>
<ul>
<li>cat nip</li>
<li>laser pointers</li>
<li>lasagna</li>
</ul>
<p>Top 3 things cats hate:</p>
<ol>
<li>flea treatment</li>
<li>thunder</li>
<li>other cats</li>
</ol>
</div>
```

## HTML 为标签添加ID属性
除了 class属性之外，每一个 HTML 元素也可以具有 id 属性。
使用 id 属性有很多好处，一旦你开始使用jQuery，你将了解更多信息。
id 属性应该是唯一的。虽然浏览器不会强制唯一，但这是被广泛认可的。所以请不要给一个以上的元素相同的 id 属性。
以下是一个例子，说明如何设置h2 元素的id属性为cat-photo-app。
`<h2 id="cat-photo-app">`
任务：设置 form 元素的id属性为 `cat-photo-form`。
```
<form id="cat-photo-form" action="/submit-cat-photo">
<label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
<label><input type="radio" name="indoor-outdoor"> Outdoor</label>
<label><input type="checkbox" name="personality" checked> Loving</label>
<label><input type="checkbox" name="personality"> Lazy</label>
<label><input type="checkbox" name="personality"> Energetic</label>
<input type="text" placeholder="cat photo URL" required>
<button type="submit">Submit</button>
</form>
```

## HTML 使用ID属性设置标签样式
关于id属性的一个很酷的事情是，像类选择器一样，你可以使用CSS来设计样式。
以下是一个示例，说明如何使用 cat-photo-element 的id属性来获取元素 ，并设置背景颜色为绿色。在你的style 元素中：
```
#cat-photo-element {    
  background-color: green;    
}
```
请注意，在你的 style 元素中，定义类选择器必须添加 . 为前缀，定义ID选择器必须添加 # 为前缀。
任务：尝试给你的 form，添加一个值为 cat-photo-form 的 id 属性，一个绿色的背景。
```
<style>
#cat-photo-form{
    background-color: green
}
</style>
<form action="/submit-cat-photo" id="cat-photo-form">
<label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
<label><input type="radio" name="indoor-outdoor"> Outdoor</label>
<label><input type="checkbox" name="personality" checked> Loving</label>
<label><input type="checkbox" name="personality"> Lazy</label>
<label><input type="checkbox" name="personality"> Energetic</label>
<input type="text" placeholder="cat photo URL" required>
<button type="submit">Submit</button>
</form>
```

## HTML 使用padding布局页面标签
现在让我们把 Cat Photo App 暂时放一边，并了解学习更多关于的 HTML 样式。
你可能已经注意到了这一点，所有的 HTML 元素本质上都是一些小矩形块。
有三个重要的属性控制每个HTML元素的布局：padding(内边距)、margin(外边距)、border(边框)。
元素的 padding 控制元素与其边框 border 之间的距离。
在这里，我们可以看到，绿方块和红方块都位于黄方块中。请注意，红方块具有比绿方块具有更大的 padding。
当你增大绿方块的 padding时, 它将增加元素内容和元素边框之间的距离。
任务：修改绿方块的 padding ，以使它与红方块匹配。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 10px;
}
.red-box {
background-color: red;
padding: 20px;
}
.green-box {
background-color: green;
padding: 20px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## HTML 使用margin布局页面标签
元素的 margin （外边距）控制元素 border （边框）和周围元素实际所占空间的距离。
在这里，我们可以看到，绿方块和红方块都位于黄方块中。请注意，红方块具有比绿方块更大的 margin（外边距），使其看起来更小。
当你增大绿方块的 margin 时，它将增加元素边框和元素实际所占空间之间的距离。
修改绿方块的 margin ，以使它与红方块匹配。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 10px;
}
.red-box {
background-color: red;
padding: 20px;
margin: 20px;
}
.green-box {
background-color: green;
padding: 20px;
margin: 20px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```


## HTML 使用负值设置页面元素的margin属性
元素的 margin （外边距）控制元素的 border（边框）和周围元素实际所占空间的距离。
如果将一个元素的 margin 设置为负值，则元素将会变大。
尝试将 margin设置为负值，如红方块。
任务：把 green-box 的 margin 设置为 -15px，以使它将父容器(黄方块)的横向宽度填充。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 10px;
}
.red-box {
background-color: red;
padding: 20px;
margin: -15px;
}
.green-box {
background-color: green;
padding: 20px;
margin: -15px;
}
</style>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## HTML 为不同方向padding设置不同的值
有时你将需要自定义一个元素，使它的每一个边具有不同的 padding。
CSS 允许你使用 padding-top、padding-right、padding-bottom 和 padding-left属性来控制元素四个方向的 padding。
使你的 green-box class的顶部和左侧具有 40px 的 padding，而底部和右侧则是 20px。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 10px;
}
.red-box {
background-color: red;
padding-top: 40px;
padding-right: 20px;
padding-bottom: 20px;
padding-left: 40px;
}
.green-box {
background-color: green;
padding-top: 40px;
padding-left: 40px;
padding-bottom: 20px;
padding-right: 20px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## HTML 为不同方向margin设置不同的值
有时你将需要自定义一个元素，使它的每一个边具有不同的 margin。
CSS 允许你使用 margin-top、margin-right、margin-bottom 和 margin-left 属性来控制元素四个方向的margin。
使你的 green-box class的顶部和左侧具有 40px 的 margin，而底部和右侧则是 20px。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 10px;
}
.red-box {
background-color: red;
margin-top: 40px;
margin-right: 20px;
margin-bottom: 20px;
margin-left: 40px;
}
.green-box {
background-color: green;
margin-top: 40px;
margin-left: 40px;
margin-bottom: 20px;
margin-right: 20px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## HTML CSS中padding简写
除了分别指定元素的 padding-top、padding-right、padding-bottom 和 padding-left 属性外，你还可以集中起来指定它们，如下所示：
`padding: 10px 20px 10px 20px;`
这四个值以顺时针方式排列：顶部、右侧、底部、左侧，简称：上右下左。
使用顺时针表示法，给`".green-box" class`在其顶部和左侧具有 40px 的 padding，而底部和右侧具有 20px 的 padding。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 20px 40px 20px 40px;
}
.red-box {
background-color: red;
padding: 20px 40px 20px 40px;
}
.green-box {
background-color: green;
padding: 40px 20px 20px 40px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## HTML CSS中margin简写
让我们用 margin 再试一次。
除了分别指定元素的 margin-top、margin-right、margin-bottom 和 margin-left 属性外，你还可以集中起来指定它们，如下所示：
`margin: 10px 20px 10px 20px;`
这四个值以顺时针方式排列：顶部、右侧、底部、左侧，简称：上右下左。
使用 顺时针表示法 ，给 `“.green-box" class `的元素在其顶部和左侧具有 40px 的 margin，而底部和右侧具有 20px 的 margin。
```
<style>
.injected-text {
margin-bottom: -25px;
text-align: center;
}
.box {
border-style: solid;
border-color: black;
border-width: 5px;
text-align: center;
}
.yellow-box {
background-color: yellow;
padding: 20px 40px 20px 40px;
}
.red-box {
background-color: red;
margin: 20px 40px 20px 40px;
}
.green-box {
background-color: green;
margin: 40px 20px 20px 40px;
}
</style>
<h5 class="injected-text">margin</h5>
<div class="box yellow-box">
<h5 class="box red-box">padding</h5>
<h5 class="box green-box">padding</h5>
</div>
```

## CSS 样式的继承
现在让我们全新开始，并谈谈CSS 继承。
每一个 HTML 页面都有一个 body 元素。
我们可以证明body元素的存在，将其 background-color 设置为黑色。
我们可以通过将以下代码添加到我们的style元素中：
```
body {
  background-color: black;
}
```
```
<style>
body {
    background-color: black
}
</style>
```

## CSS 继承Body元素样式
现在我们已经证明，每个HTML页面都有一个body元素，并且它的body元素同样能够应用样式。
记住，你可以像任何其他HTML元素一样对你的body元素应用样式，并且所有其他元素都将继承你的body元素的样式。
首先，使用文本 Hello World创建一个 h1 元素。
然后，让我们通过向body元素的样式声明部分添加 color: green; 使页面上的所有元素的颜色为green。
最后，通过向 body 元素的样式声明部分添加 font-family: Monospace; 将 body 元素的 font-family（字体）设置为 Monospace。
```
<style>
body {
background-color: black;
color: green;
font-family: Monospace;
}
</style>
<h1>Hello World</h1>
```


## CSS 样式的覆盖
有时你的 HTML 元素会得到多个相互冲突的样式。
例如，你的 h1 元素不能同时为绿色和粉色。
让我们看看当我们创建一个使文本变成粉色的class，然后将它应用到一个元素时会发生什么。
我们的 class 会override（覆盖） body元素的`color: green;CSS` 属性吗？
创建一个名为pink-text的 CSS class，它使元素的颜色为粉色。
设置 h1 元素的 class 为 pink-text。
```
<style>
body {
background-color: black;
font-family: Monospace;
color: green;
}
.pink-text{
    color: pink;
}
</style>
<h1 class="pink-text">Hello World!</h1>
```

## CSS 多个class处理样式覆盖
我们的 "pink-text" class 覆盖了 body 元素的 CSS 声明！
我们刚刚证明了我们的 class 会覆盖 body 元素的 CSS。所以下一个合乎情理的问题就是，我们可以怎样来覆盖我们的 pink-text class ？
再创建一个名为 blue-text 的 CSS class，其颜色设置为蓝色的，确保它在 pink-text class 声明之下。
除了 pink-text class 之外，你还可以将 blue-text class 应用到你的 h1 元素，让我们看看哪一个会被应用。
如下例子所示，通过用空格分隔多个 class 属性，可让 HTML 元素应用多个 class 属性：
`class="class1 class2"`
注意：在 HTML元素中列出这些 class 的顺序并不重要。
然而，**<style> 部分中的 class 声明的顺序是重要的，第二个声明将始终优先于第一个声明。因为 .blue-text 是第二个声明，它会覆盖 .pink-text 的属性。**
```
<style>
body {
background-color: black;
font-family: Monospace;
color: green;
}
.pink-text {
color: pink;
}
.blue-text{
    color:blue;
}
</style>
<h1 class="pink-text blue-text" >Hello World!</h1>
```


## CSS 通过ID的样式属性覆盖class类的声明
我们刚刚证明了，浏览器是从上到下读取CSS。这意味着，如果发生冲突，浏览器将使用最后的任何CSS声明。
我们还有其他覆盖 CSS 的方法。你还记得 id 属性吗？
我们来覆盖你的 pink-text 和 blue-text class，并使你的 h1 元素变成橙色，给 h1元素一个id，然后对该id进行样式化。
给你的 h1 元素添加名为 orange-text 的 id 属性。记住，id 样式如下所示：
`<h1 id="orange-text">`
在你的 h1 元素中保留 blue-text 和 pink-text class。
为你的 style 元素中的 orange-text id 创建一个 CSS 声明。如下例子所示：
```
#brown-text {    
  color: brown;    
}
```
注意：你是否将这个css声明在pink-text class之上或之下无关紧要，因为id属性始终是具有更高的优先级。
```
<style>
body {
background-color: black;
font-family: Monospace;
color: green;
}
.pink-text {
color: pink;
}
.blue-text {
color: blue;
}
#orange-text{
    color: orange;
}
</style>
<h1 class="pink-text blue-text" id="orange-text">Hello World!</h1>
```


## CSS 通过内联样式覆盖class类的声明
我们已经证明了，id 声明都会覆盖 class 声明，不管它在你的 style 元素 CSS 的哪个位置进行声明。
还有其他方法可以覆盖CSS。你还记得内联样式吗？
使用 in-line style（内联样式）来尝试使我们的 h1 元素变为白色。记住，内联样式如下所示：
`<h1 style="color: white;">`或者`<h1 style="color: white">`
在你的 h1 元素上保留 blue-text 和 pink-text class。
```
<style>
body {
background-color: black;
font-family: Monospace;
color: green;
}
#orange-text {
color: orange;
}
.pink-text {
color: pink;
}
.blue-text {
color: blue;
}
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color:white">Hello World!</h1>
```


## CSS 通过使用Important覆盖所有其他样式
好极了！我们刚刚证明了内联样式将覆盖style 中定义的所有 CSS声明。
可是等等。有最后一个方法来覆盖CSS。这是所有的最强大的方法。但在我们这样做之前，让我们来谈谈你为什么要覆盖CSS。
在许多情况下，您将使用CSS库。这些可能会意外覆盖您自己的CSS。所以当你绝对需要确定一个元素具有特定的CSS时，可以使用 !important。
让我们回到之前的 pink-text class 声明。请记住，我们的 pink-text class 被后续的 class 声明、id 声明和内联样式覆盖了。
我们来给 pink-text 元素的 color 声明加上关键字 !important，以使 100% 确保你的 h1 元素是粉色的。
举例如下：
`color: pink !important;`
```
<style>
body {
background-color: black;
font-family: Monospace;
color: green;
}
#orange-text {
color: orange;
}
.pink-text {
color: pink !important;
}
.blue-text {
color: blue;
}
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>
```
## 优先级总结
1. `！important`
2. 内联样式inline的style声明
3. id样式属性
4. 多个class类，由在<style></style>中的类声明顺序有关，越靠后声明越优先，跟在html元素中的class类中的声明无关。
5. 单个class属性
6. body声明


## CSS 通过使用十六进制代码设置特定的颜色
你知道还有其他方式来表示CSS中的颜色吗？其中一种方式称为 hexadecimal code（十六进制编码），简写为 hex code。
我们通常使用 decimals，也就是十进制数字，它对每一位数字使用符号0到9来表示。Hexadecimals （或 hex）是十六进制数字，这意味着它使用十六个不同的符号。像十进制一样，符号 0-9 代表数值零到九，那么 A、B、C、D、E、F 代表数值十到十五。总共，用 0 到 F 可以表示 hexadecimal 中的每一位数字，共为我们提供 16 个可能的数值。
在 CSS 中，我们可以使用 6 个十六进制数字来表示颜色，每 2 个分别表示红 (R)、绿 (G) 和蓝(B) 成分。例如，#000000 是黑色，同时也是可能的数值中最小的。
把 body 元素的 background-color 由 black 替换成其 hex code 表示，即#000000。
```
<style>
body {
background-color: #000000;
}
</style>
```


## CSS 十六进制白色表达方式
数字 0 是十六进制代码中最低的数字，表示完全没有颜色。。
数字 F 是十六进制代码中最高的数字，表示最大可能的亮度。
现在，让我们通过 background-color 的 hex code 修改为` #FFFFFF` ，把body 元素的background-color 改为白色。
```
<style>
body {
background-color: #FFFFFF;
}
</style>
```
## CSS 十六进制RGB红色表达方式
hex code（十六进制代码） 遵循 red-green-blue（红-绿-蓝），或者叫 rgb 格式。hex code 中的前两位表示颜色中红色的数量，第三四位代表绿色的数量，第五六位代表蓝色的数量。
所以要得到绝对的纯红色，你只需要在第一和第二位使用 F （最大可能的数值），且在第三、第四、第五和第六位使用 0 （最小可能数值）。
通过对 background-color 应用 hex code 值 `#FF0000`,把 body 元素的 background-color 设置为红色。
```
<style>
body {
background-color: #FF0000;
}
</style>
```
## CSS 十六进制RGB绿色表达方式
hex code（十六进制代码） 遵循 red-green-blue（红-绿-蓝），或称为 rgb 格式。hex code 中的前两位表示颜色中红色的数量，第三四位代表绿色的数量，第五六位代表蓝色的数量。
所以要得到绝对的纯绿色，你只需要在第三和第四位使用 F （最大可能的数值），且在其它位使用 0 （最小可能数值）。
通过对 background-color 应用 hex code 值 `#00FF00` ，把body 元素的 background-color 设置为绿色。
```
<style>
body {
background-color: #00FF00;
}
</style>
```
## CSS 十六进制RGB蓝色表达方式
hex code（十六进制代码）遵循 red-green-blue（红-绿-蓝），或称为 rgb 格式。hex code 中的前两位表示颜色中红色的数量，第三四位代表绿色的数量，第五六位代表蓝色的数量。
所以要得到绝对的纯蓝色，你只需要在第五和第六位使用 F （最大可能的数值），且在其它位使用 0 （最小可能数值）。
通过对 background-color 应用 hex code 值 `#0000FF` ,把 body 元素的 background-color 设置为蓝色。
```
<style>
body {
background-color: #0000FF;
}
</style>
```


## CSS 十六进制RGB混合颜色
十六进制代码使用6个十六进制数字表示颜色，每 2 个分别表示红（R），绿（G）和蓝（B）成分。
从这三种纯色（红、绿、蓝），我们可以改变每种颜色创造超过1600万种其他颜色！
例如，橙色是纯红，与一些绿色混合，没有蓝色。在十六进制代码中，这转换为 ＃FFA500。
数字 0 是十六进制代码中最低的数字，表示完全没有颜色。
数字 F 是十六进制代码中最高的数字，表示最大可能的亮度。
用正确的十六进制代码替换 <style> 元素中的颜色词。
Color	          Hex Code
Dodger Blue	   #2998E4
Green         	#00FF00
Orange        	#FFA500
Red	              #FF0000
```
<style>
body {
background-color: #FFA500;
}
</style>
```


## CSS 灰色度设置
从这三种纯色（红、绿、蓝），我们能得到 1600 万种其它的颜色。
我们也可以通过平均混合所有三种颜色得到不同灰度等级的灰色。
通过对 background-color 应用 hex code 值 `#808080` ，把你的body 元素的 background-color 设置为灰色。
```
<style>
body {
background-color: #808080;
}
</style>
```

## CSS 不同等级的灰度设置
通过平均混合所有三种颜色，我们还可以得到其他色度等级的灰色，这样我们可以非常接近纯黑色。
通过对 background-color 应用 hex code 值 `#111111` ，把你的 body 元素的 background-color 设置为深灰色。
```
<style>
body {
background-color: #111111
}
</style>
```

## CSS 十六进制RGB表达式缩写
许多人对1600 万种颜色感到不可思议，并且 hex code（十六进制代码） 很难记住。幸运的是，你可以缩短它。
例如，红色的十六进制码 `#FF0000` 可以缩短为 `#F00`。这个缩写形式给出一个数字为红色，一个数字为绿色，一个数字为蓝色。
这将把所有可能的颜色总数减少到大约4000种，但是浏览器会把 `#FF0000` 和` #F00` 解释为完全相同的颜色。
继续，尝试使用缩写的十六进制代码对正确的元素进行着色。
```
<style>
body {
background-color: #F00;
}
</style>
```


## CSS 使用rgb属性设定颜色
在 CSS 中表示颜色的另一个方法是使用 RGB 值。
代表黑色的 RGB 值如下所示：
`rgb(0, 0, 0)`
代表白色的 RGB 值如下所示：
`rgb(255, 255, 255)`
使用 RGB，是使用RGB指定每个颜色的亮度，数字介于0到255之间，而不是像使用十六进制代码那样使用六个十六进制数字。
如果你做个算术，一个颜色的两位数字等于16 乘以 16，这给我们256个总值，因此，从零开始计数的 RGB 具有与十六进制代码完全相同数量的可能值。
现在，我们用黑色的 RGB 值 rgb(0, 0, 0) 替换掉 body 元素背景色的hex code（十六进制代码）。
```
<style>
body {
background-color:rgb(0,0,0);
}
</style>
```


## CSS 使用rgb属性设定白色
代表黑色的 RGB 值如下所示：
`rgb(0, 0, 0)`
代表白色的 RGB 值如下所示：
`rgb(255, 255, 255`)
使用 RGB，是使用RGB指定每个颜色的亮度，数字介于0到255之间，而不是像使用十六进制代码那样使用六个十六进制数字。
现在，将你的body元素的 background-color 从黑色的 RGB 值修改为白色的 `rgb 值 rgb(255, 255, 255)。`
```
<style>
body {
background-color: rgb(255, 255, 255);
}
</style>
```


## CSS 使用rgb属性设定红色
和使用 hex code（十六进制编码）一样，你可以通过不同数值的组合来表示 RGB 中不同的颜色。
这些数值遵循 RGB 顺序模式：第一位表示红色，第二位表示绿色，第三位表示蓝色。
使用 rgb 将你的 body 元素的 background-color 设置为红色的` RGB 值：rgb(255, 0, 0)。`
```
<style>
body {
background-color: rgb(255,0, 0);
}
</style>
```


## CSS 使用rgb属性设定绿色
使用 rgb 将你的 body 元素的 background-color 设置为绿色的 `RGB 值：rgb(0, 255, 0)。`
## CSS 使用rgb属性设定蓝色
使用 rgb 将你的 body 元素的 background-color 设置为蓝色的 `RGB 值：rgb(0, 0, 255)。`
## CSS 使用rgb属性设定混合颜色
就像十六进制代码一样，您可以通过使用不同值的组合来混合RGB中的颜色。
用我们的style元素中的颜色字替换正确的RGB值。
```
Color	        RGB
Blue	       rgb(0, 0, 255)
Red	          rgb(255, 0, 0)
Orchid    	rgb(218, 112, 214)
Sienna	       rgb(160, 82, 45)
```
任务：将 body 元素的背景色修改为橙色的 RGB 值： rgb(255, 165, 0)。
```
<style>
body {
background-color: rgb(255, 165, 0);
}
</style>
```






