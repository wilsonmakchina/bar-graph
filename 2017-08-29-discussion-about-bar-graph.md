---
title: "漫谈条形图"
date: '2017-09-09'
author: 
   - 黄湘云 
   - 李宇轩
tags: ["条形图"]
slug: discussion-about-bar-graph
---

这篇文章的起因是源于COS论坛中的下图，该图引起了热烈的讨论，具体的探讨细节[见此](https://d.cosx.org/d/417769)。

![图0：起因条形图](https://user-images.githubusercontent.com/12031874/28810063-2fe63496-76ba-11e7-88be-e0c9d14dd486.png)

<center>图0：起因条形图</center>

这幅图中主要有三个问题：一是柱子过宽而纵坐标过窄导致的不成比例；二是纵坐标和颜色图例传达了同一份内容，因此只保留一个就可以，此外由于颜色并没有传达其他信息，其实可以让所有柱子用同一种颜色；三是使用的颜色图例不仅颜色太多使得图形显得非常乱，而且还和一部分的柱子出现了重叠，虽然没有影响信息解读，但有些难看。从这一张图中可以看出，为了赏心悦目地传递信息，条形图还是需要有一些作图规范的。

基本条形图要满足三个原则：**有效**，能够向读者传递重要信息；**简洁**，尽量用最少的图形传递最多的信息，不要有赘余；**美观**，图形做出来得让大家能看进去，不要太反人类。

横纵坐标的情况经常用来判定使用哪种类型的条形图，因此我们围绕横纵坐标的三类问题展开叙述：坐标长度问题、坐标分类问题、坐标数值问题。前两个问题着重点在于选择什么样的条形图，而第三个问题则着重在于坐标应该如何调整。在这三类问题之后，我们将立方条形图单独拿出来看看。

在解决这些问题的同时我们也来查看图形颜色的情况，整体来说图形颜色需要满足两个要求：第一个是颜色跨度要适中，不能跨度太小让大家辨别颜色太费劲，也不能跨度太大显得图形特别乱，找不到重点；第二个是要根据情况来决定使用渐变色还是分类色，让图形变得美观。事实证明，选择不应过多依赖图形的形状，而更多的应该在于利用好审美。

# 1.坐标长度问题

## 1.1 横躺条形图与竖立条形图

这个问题描述的是坐标名称特别长的情况下应该如何处理。当坐标比较短时，这也是绘制条形图的大部分情况，用正立条形图或者横躺条形图都是可以的，比如下图1，这个图横竖都非常美观，在此就不放横躺条形图的样式了。

![图1：泊松分布](https://user-images.githubusercontent.com/12031874/29483578-d90c9658-84db-11e7-85c9-d44db8994d33.png)

<center>图1：泊松分布</center>

当坐标比较长或者比较多时，在正立条形图和横躺条形图中我们就只能使用横躺条形图了，如下图2：

![图2：横躺条形图正例](https://user-images.githubusercontent.com/12031874/28816143-4c16e1e4-76d6-11e7-8176-cc3cf0ced603.png)

<center>图2：横躺条形图正例</center>

图2是横躺条形图的一个典型代表，分类变量又多又长，所以把它横过来放大家看着更方便一些。下图3则是这张图的反例：

![图3：正立条形图反例](https://user-images.githubusercontent.com/12031874/28815599-7b307cc6-76d4-11e7-88a4-f3c5284cda08.png)

<center>图3：正立条形图反例</center>

图3为了避免横坐标过长导致的图形过宽，因此将横坐标都做了一定角度的倾斜，这种倾斜自然影响了读者阅读这些横坐标，所以从简洁角度来讲，还是横躺条形图更美观一些。

如果坐标虽然很多，但是这些坐标是连续性的数字的话，我们依旧可以把它竖过来放，因为连续性坐标可以省略其中的大部分坐标，不用明确标出，如下图4：

![图4：竖立条形图](https://user-images.githubusercontent.com/12031874/29704567-f2af53fe-89ac-11e7-896a-53232349181a.png)

<center>图4：竖立条形图</center>

## 1.2 点图

除了横躺条形图之外，当坐标长度过长或者坐标过多时，我们还有另外一个选项，就是点图：

![图5：车型、气缸数和每加仑里程的关系](https://user-images.githubusercontent.com/12031874/29484779-6562d9d4-84f8-11e7-8955-4108a17d1984.png)

<center>图5：车型、气缸数和每加仑里程的关系</center>

这张点图要是把它竖过来放实在太恐怖了...我是没有勇气把它的反例放上来的。由此来说，在坐标特别多的时候，点图要更好用一些。下面这张点图也是如此：

![图6：CRAN上发布R包多于11个的人](https://user-images.githubusercontent.com/12031874/29740087-1378d40a-8a81-11e7-949f-3be5956df129.png)

<center>图6：CRAN上发布R包多于11个的人</center>

这张点图则是百尺竿头更进一步，不止是竖过来不忍直视，就连做成横躺条形图都会挤成一块，同样为了不让大家的视线受到过多的污染，我就不放这张图的反例了。由此来说的话，最开始引起争端的图0也可以绘制成横躺的点图，但在此就不放上来了。

## 1.3 图形颜色

图形颜色在正立条形图、横躺条形图中是一个大问题，因为本身图形简单，所以颜色的好坏便决定了这张图是否美观，也决定了这张图能否完整表达想要传达的信息。

对此我的建议是，如果颜色所传递的信息能由其他因素，比如说条形图柱子的高度来反映，那么这种颜色是着实没有必要的。所以对于那些没有什么特殊信息，只是想比较柱子高低的条形图，只用一种颜色就行了，我们先来看这种情况的反例：

![图7：图形颜色反例](https://user-images.githubusercontent.com/12031874/28810279-7aa94ecc-76bb-11e7-84f6-3f26bd5eaeaf.png)

<center>图7：图形颜色反例</center>

再拿这张之前用过的图形当正例作比较：

![图8：图形颜色正例](https://user-images.githubusercontent.com/12031874/28812405-2a9aca1c-76c7-11e7-9bbf-493a7e73e196.png)

<center>图8：图形颜色正例</center>

两张图我们仔细查看的话，可以发现传递的信息是一样的，但第一张图还要慢慢查看哪个柱子对应哪个图例，而第二张图则没有这个必要，也就是说第二张图更简洁；此外，第一张图中颜色太多，让人眼花缭乱，但实际上却没有什么重要作用，所以对于正立条形图和横躺条形图，如果颜色不能传达其他信息的话，最好统一颜色。颜色图例的使用是一个需要仔细琢磨的问题，个人认为颜色图例在普通的正立条形图和横躺条形图中的使用并不是很重要，因为这些条形图中柱子本身有高低，因此已经产生了区别，再使用颜色图例只是类似“锦上添花”，而非必要品，当然，如果我们想着重强调条形图中的某个或某些柱子，加上颜色加以区分是有必要的，因为此时的颜色可以突出一些关键信息，此时也要酌情来看是否需要加上图例。

# 2.坐标分类问题

## 2.1 分类条形图和堆积条形图
坐标分类一般都集中在横坐标，当坐标有两层分类时，我们一般有两种解决办法：绘制分类条形图或者堆积条形图。坐标分类本身并不是一个难事，大家看到了两层分类，自然就会想到使用这两种图形，重点在于颜色问题，我们首先来看最常见的分类条形图：

![图9：冈比亚儿童患疟疾情况](https://user-images.githubusercontent.com/12031874/29740264-234eedde-8a85-11e7-8425-5a60cda96845.png)

<center>图9：冈比亚儿童患疟疾的影响因素（是否有蚊帐，蚊帐是否杀虫，RDT表示快速诊断结果：\n0表示没有感染疟疾，1表示感染疟疾）</center>

图9这张分类条形图中规中矩，利用颜色区分了不同的情况，颜色的不同也产生了对比，此时颜色图例自然是有必要的。分类条形图在类型比较多时用的也较多，因为类型少时，我们同时可以使用堆积条形图，而类型多时，堆积条形图就没有那么直观了，如下图10：

![图10：1940年弗吉尼亚州各年龄段死亡率（单位千分之一）](https://user-images.githubusercontent.com/12031874/29483581-e44f0cee-84db-11e7-9b72-52b12b66cd11.png)

<center>图10：1940年弗吉尼亚州各年龄段死亡率（单位千分之一）</center>

图10颜色区别比较明显，同时颜色跨度又不是很大，不会显得图形非常乱。再请大家看下面这两张反例图（注意，前方高能！）：

![图11：美国每十年从欧洲移民情况1](http://gnuplot.sourceforge.net/demo/histograms.4.png)

<center>图11：美国每十年从欧洲移民情况1</center>

![图12：美国每十年从欧洲移民情况2](http://gnuplot.sourceforge.net/demo/histograms.6.png)

<center>图12：美国每十年从欧洲移民情况2</center>

这两张图实在是有些难以接受...两张图都是颜色过多，利用堆积条形图有些部分小的几乎可以忽略，另外竟然还有国家选的颜色特别相近，很难判定哪个是哪个。所以当堆积的有些多时，就不适合这种方式了，一方面是眼花缭乱，找不到重点；另外一方面是有些颜色趋于相近，可能会引起误解。整体来看，当分类的变量比较少时，利用堆积条形图是个不错的选择，但当分类变量较多时，再使用堆积条形图就会严重影响图形的美观与解读。

## 2.2 复合条形图

由此来看，在分类的变量比较多时，分类柱状图要好于堆积柱状图，但我们也要灵活使用。此时复合条形图就要登场了，复合条形图就是指既有分类，又有堆积的条形图，如下图：

![图13：1973年加州大学伯克利分校最大的六个系学生录取情况](https://user-images.githubusercontent.com/12031874/29483635-15bb4ac6-84dd-11e7-9c63-e36ef69a9eb5.png)

<center>图13：1973年加州大学伯克利分校最大的六个系学生录取情况</center>

复合条形图所传递的信息要多于其他的图形，上面这张图便是既展现了同一人群中录取和拒绝的区别，也展现了同一系中男女的区别。同样，内容较多时使用复合条形图要好于上述单独的分类条形图或者堆积条形图。比如下面两张图：

![图14：美国每十年从欧洲移民情况3](https://user-images.githubusercontent.com/12031874/29747239-77cf9c78-8b25-11e7-8c6c-11b80f8ed146.png)

<center>图14：美国每十年从欧洲移民情况3</center>

![图15：美国每十年从欧洲移民情况4](https://user-images.githubusercontent.com/12031874/29747240-7bb48e16-8b25-11e7-989d-f847501beda1.png)

<center>图15：美国每十年从欧洲移民情况4</center>

图15那张复合条形图明显要好于前面的图14，主要好在三点：一点是堆积的少，颜色变化也大，能看清楚；第二点是它相当于多加了一个地区的分类归组，可以再进行一些有趣的研究；第三点是由于横坐标很多，这样一个横坐标对应一个柱子还是容易看的，像反例那个分类条形图，柱子过多，有可能看一会就会搞混。

复合堆积条形图的效果也可以用马赛克图来呈现，如图16所示：

![图16：马赛克图示例](https://user-images.githubusercontent.com/12031874/29492195-2c1a2cfa-85a6-11e7-9c04-dbba83986442.png)
<center>图16：马赛克图示例</center>

总体来说，马赛克图中方块的大小在视觉上更容易识别，因此基于比例比较来说，马赛克图更有优势，但如果说硬要强调数值大小，那复合堆积条形图稍好。请大家根据下面的两幅图自行感受优劣：

![图17：复合堆积条形图](https://user-images.githubusercontent.com/12031874/29699745-a81b58a8-8991-11e7-9996-2f0a4ada46f7.png)

<center>图17：复合堆积条形图</center>

![图18：马赛克图](https://user-images.githubusercontent.com/12031874/29699751-b0485c24-8991-11e7-8f7f-e059959676c9.png)

<center>图18：马赛克图</center>

# 3.坐标数值问题

## 3.1 坐标跨度

坐标跨度的问题和颜色的关系不是很大，主要就是纵坐标的取值范围。我们通常都会将纵坐标从零开始，但是有些图形的纵坐标从零开始，会使得条形图中的柱子高度比较高，如图19：

![图19：国际航班乘客示意图](https://user-images.githubusercontent.com/12031874/29484850-10bf2d36-84fa-11e7-8343-3e7bb09209e8.png)

<center>图19：国际航班乘客示意图</center>

这张图中各柱子取值范围普遍都高于200，纵坐标从零开始取会显得图形占满了整片空间的大部分区域，非常不美观，条形图的美观很大程度上是由柱子的高低差异特别大而显现出来的，如我们之前用过的泊松分布：

![图20：泊松分布](https://user-images.githubusercontent.com/12031874/29483578-d90c9658-84db-11e7-85c9-d44db8994d33.png)

<center>图20：泊松分布</center>

图17中柱子高度的变化幅度大，使得这张图显得有层次感，高低不平，非常美观。因此我们要慎重选择图形坐标的跨度，如果条形图中柱子高度普遍低于或者高于某一数值时，我们应该及时根据这些情况进行调整。

## 3.2 坐标顺序

坐标顺序的问题主要是指如何对横坐标进行排序并绘图，我的建议是：如果横坐标本身就是有顺序的，比如连续性的数值或者月份，那么就按照横坐标自身的顺序进行排列就好，这两种类型的图形例如上面的图19和图20，在这里就不再放一次了；如果横坐标本身只是分类变量，没有固定顺序，那么最好按照柱子高度从高到底或者从低到高的顺序进行绘图，如下图21：

![图21：机器类型、价格及数量条形图](https://github.com/MikeLYX/picture/blob/master/some%20described%20picture/picture1.png?raw=true)

<center>图21：机器类型、价格及数量条形图</center>

图21既是一张正例图，又是一张反例图：正例图在于展现了从低到高的顺序，同时它也展现了颜色的另外一种用法，便是传递除纵坐标外的另一种信息，在这里就是指数量的多少；但说它也是一张反例图是因为它的纵坐标普遍高于20，因此为了图形美观，应该让纵坐标从20起始，此外，颜色越深，应该代表数量越多，但显然这张图中的颜色与我们通常的做法正好相反了。总体来说，坐标顺序的不同能很大程度影响图形的美观程度。

## 3.3 坐标大小

坐标大小的问题主要体现在横纵坐标的表现方式上，当横纵坐标数量级较小时，我们一般就会直接呈现数字大小，但是如果横纵坐标数量级较大的话，如达到十万、百万级别时，直接呈现数字会给读者阅读造成一定困难，因为坐标不是非常直观。由此则有两种解决办法，一种是科学计数法，如之前用过的图11，科学计数法就会显得非常美观；另一种则是取对数操作，取对数一方面好处是图形直观，另一方面好处是能够缩小柱子的高度差异，如果柱子之间高度差异过大，使用普通取值范围的条形图则会将某些柱子压的太低。正例如下图22：

![图22：R包与开发人数示意图](https://user-images.githubusercontent.com/12031874/29740193-954a5344-8a83-11e7-9108-f6ea78ccedbd.png)

<center>图22：R包与开发人数示意图</center>

反例在此就不放了，这张图的反例实在是辣眼睛。坐标的大小并不影响解读，它主要影响图形的美观，对坐标进行一定的处理，让它变得美观是很有必要的。

# 4.立方条形图

我们将单独把立方条形图拿出来，是因为立方条形图有两点和二维条形图有明显区别：第一点是立方条形图是三维的，呈现了两类横坐标与纵坐标之间的关系；
第二点是立方条形图中的渐变色运用很多，而二维条形图中渐变色运用较少。因此立方条形图中主要需要注意的就是颜色的变化情况，下面图形都是作为正例出现，不再举反例。

![图23：立方条形图1](https://user-images.githubusercontent.com/12031874/29819490-9035f152-8cf3-11e7-83c1-414ade485b7e.png)

<center>图23：立方条形图1</center>

这张图中的各个柱子没有明显趋势，但有明显分类，而这种横坐标之间也没有明显关系的图形，利用不同的颜色要比渐变色更好。渐变色更适合用于那些横坐标之间有连续关系的图形，如下面的图24,图25和图26：

![图24：立方条形图2](https://user-images.githubusercontent.com/12031874/29644438-993e3efc-88a8-11e7-94ba-c04e57f15e4c.png)

<center>图24：立方条形图2</center>

图24展现了每月航班人数的变化情况，这张图中的颜色从黄色渐变到最后的紫色，虽然跨度很大，但也不是很显乱。像这种希望能够凸显出最高的区域或者最低区域的图形，利用柱子高低顺序进行颜色变化是个不错的选择。

![图25：立方条形图3](https://user-images.githubusercontent.com/12031874/29819135-e7a3c4fc-8cf1-11e7-86c6-6aba140ff49f.png)

<center>图25：立方条形图3</center>

图25也是利用柱子高低变化产生了渐变色，但相比图21，这张图能够更直观展现柱子的高低程度，同时图形的角度也是一个俯视角度，虽然图形中没有什么明显的趋势，但能够把那些比较重要、比较突出的点更好地反映出来。

![图26：立方条形图4](https://user-images.githubusercontent.com/12031874/29818497-2c22c662-8cef-11e7-9c48-2b245d7d76f8.png)

<center>图26：立方条形图4</center>

相比图24和图25，图26则显得比较“单纯”,它的颜色渐变只是根据月份的逐步变化实现的，这张图中的颜色实际上只是起到了区分不同月份的作用。

当我们只关注立方条形图柱子的高低时，我们可以用棋盘图代替立方柱形图，用颜色代替柱形图的高低，就如同俯视立方条形图一样，如下图27：

![图27：棋盘图反例](https://user-images.githubusercontent.com/12031874/29750323-49f7f020-8b70-11e7-92a2-e542d381c33f.png)

<center>图27：棋盘图反例</center>

这张图的颜色的确代替了柱形图的高低，但是显然这张图中的渐变色跨度太小，因此颜色过于相近，整体解读以及美感自然都不如下面这张图28：

![图28：棋盘图](https://user-images.githubusercontent.com/12031874/29750324-4e1a69e4-8b70-11e7-8bc4-1e4593d3dd2d.png)

<center>图28：棋盘图</center>

# 5.总结

条形图的应用一共有三原则：有效、美观、简洁；条形图的颜色则有两要求：跨度适中、图形美观。条形图类型的选择会受到横纵坐标的限制，颜色则是为条形图“锦上添花”的。

但大多数情况下，正立条形图和横躺条形图都是可以使用的，只有在某些特定情况下，二者才会有优劣，点图亦是如此；相比之下，分类条形图和堆积条形图则不然，在类型特别多的情形下，分类条形图的确要比堆积条形图好用的多，但如果传递的信息太多或者分类层数过多，使用复合条形图或者马赛克图也是不错的选择；而立方条形图的颜色要比二维条形图颜色有更多的发挥空间，不过由于大部分横坐标的连续性，可能这种空间很多都发挥在了渐变色上面，因此使用立方柱状图制作的图形也可以制作成棋盘图。

# 参考文献

1. R Core Team (2017). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria.
  URL https://www.R-project.org/.

2. Karline Soetaert (2016). plot3D: Plotting Multi-Dimensional Data. R package version 1.1. https://CRAN.R-project.org/package=plot3D

3. Thomas Rahlf (2017). Data Visualisation with R – 100 Examples, Springer. eBook ISBN: 978-3-319-49751-8, Hardcover ISBN: 978-3-319-49750-1.

4. Jeffrey B. Arnold (2017). ggthemes: Extra Themes, Scales and Geoms for 'ggplot2'. R package version 3.4.0. https://CRAN.R-project.org/package=ggthemes

5. Hadley Wickham (2009). ggplot2: Elegant Graphics for Data Analysis, Springer-Verlag New York. ISBN: 978-0-387-98140-6. URL http://ggplot2.org

6. Daniel Lüdecke (2017). sjPlot: Data Visualization for Statistics in Social Science. R package version 2.3.2. https://CRAN.R-project.org/package=sjPlot

7. Daniel Lüdecke (2017). sjmisc: Miscellaneous Data Management Tools. R package version 2.6.0. https://CRAN.R-project.org/package=sjmisc 

8. Paulo J. Ribeiro Jr and Peter J. Diggle (2016). geoR: Analysis of Geostatistical Data. R package version 1.7-5.2. https://CRAN.R-project.org/package=geoR

9. Simon Garnier (2017). viridis: Default Color Maps from 'matplotlib'. R package version 0.4.0. https://CRAN.R-project.org/package=viridis

10. Alboukadel Kassambara (2017). ggpubr: 'ggplot2' Based Publication Ready Plots. R package version 0.1.4. https://CRAN.R-project.org/package=ggpubr

11. <https://datascienceplus.com/building-barplots-with-error-bars/>

12. <http://gnuplot.sourceforge.net/demo/histograms2.html>

13. <http://gnuplot.sourceforge.net/demo/histograms.html>

14. Hadley Wickham (2016). scales: Scale Functions for Visualization. R package version 0.4.1. https://CRAN.R-project.org/package=scales

15. Daniel Adler, Duncan Murdoch and others (2017). rgl: 3D Visualization Using OpenGL. R package version 0.98.1. https://CRAN.R-project.org/package=rgl

16. Bhaskar Karambelkar (2016). colormap: Color Palettes using Colormaps Node Module. R package version 0.1.4. https://CRAN.R-project.org/package=colormap

