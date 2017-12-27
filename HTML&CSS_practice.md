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









