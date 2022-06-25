@[TOC](一些定理与知识点的总结)
# 三角函数
## 几个新的三角函数
我们在1013的课堂上引入了三个新的三角函数：
$$
csc\ x\ =\ \frac{1}{sin\ x}
\\
sec\ x\ =\ \frac{1}{cos\ x}
\\
cot\ x\ =\ \frac{1}{tan\ x}
$$
以及有关反三角函数
$$
arcsin\ x\ =\ sin^{-1}\ x\ 
\\
arccos\ x\ =\ cos^{-1}\ x\ 
\\
arctan\ x\ =\ tan^{-1}\ x\ 
\\
arccsc\ x\ =\ csc^{-1}\ x\ 
\\
arcsec\ x\ =\ cos^{-1}\ x\ 
\\
arccot\ x\ =\ cot^{-1}\ x\ 
\\
when\ x\ \in\ some\ sets
$$
反三角函数与三角函数的反函数其实并不一样，因为根据反函数的定义，只有所谓$one\ to\ one\ function$才有反函数，所以三角函数的反函数只能是反三角函数的一部分。通常三角函数的反函数值域都是从原点开始考虑。因为反函数的值域是原函数的定义域，反函数的定义域是原函数的值域。
## 有关反三角函数的计算
有关反三角函数与三角函数嵌套的计算，绝大部分思路其实都是直接画出一个三角形来计算，比如：
$$
计算：arcsin(cos\ \theta)?
$$
我们现在脑补一个直角三角形，主要是图片太麻烦博主懒得搞了。它有一个非直角的角，我们记这个角为$\theta$，于是我们设出以及脑补出这个三角形的一些参数来：
$$
\theta\ opposite：x
\\\theta\ adjacent：1
\\\theta\ hypotenuse: \sqrt{x^{2}+1}
\\\ another\ angle:\frac{\pi}{2} - \theta
$$
于是乎我们分别表示一下：
$$
cos\ \theta\ =\ \frac{1}{\sqrt{x^{2}+1}}
\\so\ we\ need\ to\ solve\ the\ following\ equation:
\\ sin \ \theta^{'}\ =\ \frac{1}{\sqrt{x^{2}+1}}
\\so\ \theta^{'}\ =\ \frac{\pi}{2} - \theta
$$
如果是三角函数在外也是同理：
$$
Calculate：sin(arccos\ \frac{1}{\sqrt{x^{2}+1}})?
\\origianl\ equation\ =\ sin\ \theta\ =\ \frac{x}{\sqrt{x^{2}+1}}
$$
## 三角双曲函数
仅仅是在某次tutorial的习题中遇见了三角双曲函数，但上课也没提过，然后tutorial也就开学的时候去过一次，也不知道之后有没有再出现过，于是当前阶段也只是把公式搬运一遍留个印象而已。
首先我们要知道两个正弦与余弦两个双曲函数：
$$
sinh\ x\ =\ \frac{e^{x}-e^{-x}}{2}
\\
cosh\ x\ =\ \frac{e^{x}+e^{-x}}{2}
$$
然后其他的函数也就呼之欲出了：
$$
tanh\ x\ =\ \frac{sinh\ x}{cosh\ x}
\\csch\ x\ =\ \frac{1}{sinh\ x}
\\sech\ x\ =\ \frac{1}{cosh\ x}
\\coth\ x\ =\ \frac{1}{tanh\ x}
$$
然后额外补充一些性质：
$$
sinh\ x\ is\ odd
\\cosh\ x\ is\ even
\\we\ have\ t\ \in\ R\ then\ 
\\cosh^{2}\ t\ -\ sinh^{2}\ t\ =\ 1
$$
其实最后一个结论的几何意义也就是等轴双曲线的一支，而且很显然焦点在$x$轴上的友半支或者是焦点在$y$轴的上半支，这就取决于你认为谁是横坐标谁是纵坐标了。
## 和差化积与积化和差公式
记得高中的时候老师就在课上提到过这些个公式，在大学有提到了这些个公式，高中时因为知道记了没用于是乎直接放弃，到了大学好像在上课时睡过去了导致再次错过
### 公式表述
1.首先是积化和差
$$
sin\ \alpha\ +\ sin\ \beta\ =\ 2sin\ \frac{\alpha+\beta}{2}cos\ \frac{\alpha-\beta}{2}
\\sin\ \alpha\ -\ sin\ \beta\ =\ 2cos\ \frac{\alpha+\beta}{2}sin\ \frac{\alpha-\beta}{2}
\\cos\ \alpha\ +\ cos\ \beta\ =\ 2cos\ \frac{\alpha+\beta}{2}cos\ \frac{\alpha-\beta}{2}
\\cos\ \alpha\ -\ cos\ \beta\ =\ -2sin\ \frac{\alpha+\beta}{2}sin\ \frac{\alpha-\beta}{2}
$$
2.然后是和差化积
$$
sin\ \alpha\ cos\ \beta\ =\ \frac{sin\ (\alpha+\beta)\ +\ sin\ (\alpha-\beta)}{2}
\\cos\ \alpha\ sin\ \beta\ =\ \frac{sin\ (\alpha+\beta)\ -\ sin\ (\alpha-\beta)}{2}
\\cos\ \alpha\ cos\ \beta\ =\ \frac{cos\ (\alpha+\beta)\ +\ cos\ (\alpha-\beta)}{2}
\\sin\ \alpha\ sin\ \beta\ =\ -\frac{cos\ (\alpha+\beta)\ -\ cos\ (\alpha-\beta)}{2}
$$
有一说一是真的难记
### 公式证明
当然真正证明其实构造扩展然后打开一边应该是很显然，虽然我还没有试过，1013不考证明，但我认为最重要的是怎么正着推出这个公式来避免在考场上忘记或者记错。

1.对于积化和差
我认为我们在记录积化和差时其实只要抓住一个比较重要的点，就是把两边的自变量尽量凑成差不多的：
$$
\alpha\ =\ \frac{\alpha+\beta}{2}\ +\ \frac{\alpha-\beta}{2}
\\
\beta\ =\ \frac{\alpha+\beta}{2}\ -\ \frac{\alpha-\beta}{2}
$$
然后我们拿第一个式子来练练手：
$$
sin\ \alpha\ +\ sin\ \beta
\\=sin\ (\frac{\alpha+\beta}{2}\ +\ \frac{\alpha-\beta}{2})\ +\ sin\ (\frac{\alpha+\beta}{2}\ -\ \frac{\alpha-\beta}{2})
\\=2sin\ \frac{\alpha+\beta}{2}cos\ \frac{\alpha-\beta}{2}
\\(Evidently) 
$$
2.对于和差化积
这个很是简单，我们只要写出三角函数的四个展开式然后倒一倒就可以了，本来觉得太麻烦了实在不想写，最后还是觉得写一遍加深印象，顺便当作是熟悉markdown用法了
$$
sin (\alpha+\beta)\ =\ sin\ \alpha\cos\ \beta\ +\ sin\ \beta\ cos\ \alpha\\
sin (\alpha-\beta)\ =\ sin\ \alpha\cos\ \beta\ -\ sin\ \beta\ cos\ \alpha\\
cos (\alpha+\beta)\ =\ cos\ \alpha\cos\ \beta\ -\ sin\ \beta\ sin\ \alpha\\
ocs (\alpha-\beta)\ =\ cos\ \alpha\cos\ \beta\ +\ sin\ \beta\ sin\ \alpha\\
$$
前两个式子一加除以$2$就是我们给出的第一个公式
# 极限
## 某些重要定理（及其可能比较重要的极限）
### Sandwich Theorem
#### 定理表述
又被称为夹逼定理，也咩有什么好证明的，不过是要注意一下前提条件之类的，还有就是其实有的时候也不一定能想起来这个定理，于是还是把它写一遍，再用它证明一些极限，强化一下记忆。
$$
Firstly\ we \ note\ a\ range\ I\ that\ for\ f(x),g(x),h(x)\ are\ all\ defined\ in\ this\ range
\\also,\ in\ this\ range:
\\g(x)\le f(x) \le h(x),(x\in I\ and\ x\ne a)
\\then\ for\ the\ value\ a\in I
\\\lim_{x \rightarrow a}g(x)=L
\\\lim_{x \rightarrow a}h(x)=L
\\then:
\\\lim_{x \rightarrow a}f(x)=L
$$
定理的表述看起来有些复杂，不过具体使用时好像还是比较清楚的。
**这里有一个坑需要注意的是我们在遇到某些两边不是$\le$的情况，只要能在所得点夹挤仍然可以是使用夹挤定理的，例子详见证明：$\lim_{x\rightarrow 0}sin\ x=0$**
#### 定理的证明
本来觉得这样一个简单的定理应该是很显然不用证明的，结果看到了WIKI最下面的内容，竟一时间没有理解，于是先在这里贴出证明，慢慢消化了。~~不过话说考试也不可能考证明。~~ 
![留着坑待再复习到时填吧](https://img-blog.csdnimg.cn/7f3f7a2b1777421199a40f4b879c9bc3.png?x-oss-process=image/watermark,type_ZHJvaWRzYW5zZmFsbGJhY2s,shadow_50,text_Q1NETiBARXJpY0xZdW5xaQ==,size_20,color_FFFFFF,t_70,g_se,x_16#pic_center)

#### 定理的应用
~~见“一些三角函数的极限”~~ 
## 某些重要极限及其证明
### 写在最前
这一部分包括了一些憨憨博主（很菜）感觉到比较有趣的极限，主要是因为我太蒻，导致可能很多基本的东西对我来说就是天书，所以还是总结一下，反正到了大学也不会有人刷题了吧。不会吧不会吧。
### $e= \lim_{x\rightarrow \infty}(1+\frac{1}{x})^{x}$
有一说一这个极限好像没法证明，因为他本来就是$e$的定义啊，跳过跳过。
加一个另一种写法：
$$
e=\lim_{x\rightarrow \infty}(1+x)^{\frac{1}{x}}
$$
对于新加的写法，在“solution to application”里已经有了解释，现在对第一种·标题里的写法我们再做一下解释：
$$
as\ we\ know\ that:
\\1^{\infty}=1
\\however,if\ f(x)\rightarrow 1\ and\ g(x)\rightarrow\infty\ (f(x)>1)
\\\lim f(x)^{g(x)}=e
$$
APPLICATION:
$$
Calculate\ following\ limits:
\\ 1.\lim_{x\rightarrow \infty}(1-\frac{1}{x}-\frac{1}{x^2})^x
\\ 2.\lim_{x\rightarrow \infty}(1+\frac{2}{x+3})^x
$$
### 一些三角函数的极限
#### $\lim_{x \rightarrow a}sin\ x=sin\ a$
PROOF:
$$
Actually\ it\ is\ not\ a\ simple\ question,\ just\ as\ the\ normal\ ways,\ we\ firstly\ consider\ the\ special\ cases:
\\when\ x\rightarrow 0
\\Firstly\ as\ we\ know\ for\ 0 \le x\le \frac{\pi}{2}:
\\0< sin\ x\le1
\\according\ to\ the\ sandwich\ theorem:
\\when\ is\ bigger\ than\ 0\ and\ approch\ 0,we\ can\ know:
\\\lim_{x\rightarrow 0^{+}}sin\ x=0
\\when\ x<0:
\\\lim_{x\rightarrow 0^{-}}sin\ x=\lim_{x\rightarrow 0^{-}}-sin\ (-x)=\lim_{-x\rightarrow 0^{+}}-sin\ (-x)=0
\\ \ \ 
\\when\ x\ne0:
\\firstly\ we\ recall\ an\ equation:
\\sin\ \alpha-sin\ \beta=2sin\ \frac{\alpha-\beta}{2}cos\ \frac{\alpha+\beta}{2}
\\so\ it\ is\ obviously\ that:
\\|sin\ x-sin\ a|= |2sin\ \frac{x-a}{2}cos\ \frac{x+a}{2}|\le|2sin\ \frac{x-a}{2}|
\\actaully\ here\ we\ find\ a\ useful\ method\ in\ solving\ limit\ problems:
\\Using\ the\ absolute \ value\ to\ creat\ Sandwich\ Theorem:
\\it\ is\ obviously\ that:
\\-|2sin\ \frac{x-a}{2}|\le sin\ x-sin\ a\le |2sin\ \frac{x-a}{2}|
\\so\ by\ apply\ Sandwich\ Theorem:
\\\lim_{x\rightarrow a}sin\ x=sin\ a
\\ \ \ \ 
\\so\ from\ the\ two\ cases,we\ finally\ prove\ the\ theorem
$$
#### $\lim_{x \rightarrow 0}\frac{sin\ x}{x}=1$
PROOF:
$$
According\ to\ the\ unknow\ problems\ so\ the\ proof\ has\ been\ gugugu
\\PIGEON\ HERE
$$
APPLICATION：
$$
Calculate\ the\ following\ limits:
\\1. \lim_{x\rightarrow 0}\frac{sin(sin\ x)}{x}
\\ 2. \lim_{x\rightarrow \infty} 2^{x}sin\frac{sin\ a}{2^{x}}
$$
####  $\lim_{x \rightarrow 0}x^{2}sin\ \frac{1}{x}=0$
PROOF;
$$
as\ we\ firstly\ see\ this\ formula\ we\ can\ be\ sure\ to\ use\ Sandwich\ Theorem :
\\for\ the\ sin,cos...\ we\ need\ to\ use\ its\ range\ and\ absolute\ value\ to\ construct\ Sandwich\ Theorem:
\\when\ 0<x\le \frac{\pi}{2}
\\|x^2sin\ \frac{1}{x}|\le x^2
\\\rightarrow -x^2\le x^2sin\ \frac{1}{x}\le x^2
\\and\ when\ x=0,\ both\ x^2\ and\ -x^2\ equal\ 0
\\so\ it\ is\ obviously\ that:
\\\lim_{x\rightarrow\ 0}x^2sin\ \frac{1}{x}=0
$$
### solution to the APPLICATION of important limits
为什么要写这个呢，主要是因为把博客快写完之后才发现原来最重要的极限基本都默认的是这两个，所以就把网上比较经典的应用整理了下来，做一个总结，计算完之后可能会得出一些对于极限求法的思考吧（雾）
$$
\\At\ first\ we\ add\ a\ new\ law\ of\ limits\ because\ it\ is\ useful\ especally \ useful\ when\ calculating\ limits\ about\ e
\\\lim_{x\rightarrow a}f(x)=A\ and\ \lim_{x\rightarrow a}g(x)=B
\\so:\lim_{x\rightarrow a}f(x)^{g(x)}=A^B
\\Also\ as\ we\ talk\ this\ form\ of\ limits,\ we\ need\ to\ know\ that:
\\\infty ^{0}\ne1
\\(not\ a\ precise\ foemula,\ but\ enough\ to\ show\ what\ I mean)
\\actually\ it's\ easy\ to\ understand\ because\ we\ know:
\\ \lim_{x\rightarrow \infty}(1+x)^{\frac{1}{x}}=e
\\ \ \ \ 
\\solution\ here:
\\ 1.\lim_{x\rightarrow \infty}(1-\frac{1}{x}-\frac{1}{x^2})^x
\\ =\lim_{x\rightarrow \infty} (\frac{x^2-x-1}{x^2})^x=\lim_{x \rightarrow \infty} (1+\frac{-(x+1)}{x})^x
\\=\lim_{x\rightarrow \infty}(1+\frac{-(x+1)}{x})^{\frac{-x}{x+1}\times \frac{-x+1}{x^2}}
\\=\lim_{x\rightarrow \infty}((1+\frac{-(x+1)}{x})^{\frac{-x}{x+1})^{\frac{-x+1}{x^2}}}
\\=\lim_{x\rightarrow \infty}(1+\frac{-(x+1)}{x})^{\frac{-x}{x+1}\times \lim_{x\rightarrow \infty}\frac{-x+1}{x^2}}
\\=(e^{-1})^0=\frac{1}{e}
\\ \ \ \ 
\\ \ \ \ \ 
2.\lim_{x\rightarrow \infty}(1+\frac{2}{x+3})^x
\\=\lim_{x\rightarrow \infty}(1+\frac{1}{\frac{x+3}{2}})^x=\lim_{x\rightarrow \infty}(1+\frac{1}{\frac{(x+3)}{2}})^{\frac{x+3}{2}\times\frac{2x}{x+3}}
\\=\lim_{x\rightarrow \infty}((1+\frac{1}{\frac{(x+3)}{2}})^{\frac{x+3}{2})^{\lim_{x\rightarrow\infty}\frac{2x}{x+3}}}=e^{2\times \lim_{x \rightarrow \infty}\frac{x}{x+3}}=e^2
\\ \ \ \ 
\\ \ \ \ 
3.\lim_{x\rightarrow 0}\frac{sin(sin\ x)}{x}
\\=\lim_{x\rightarrow 0}(\frac{sin(sin\ x)}{sin\ x}\times\frac{sin\ x}{x})=\lim_{sin\ x\rightarrow 0}\frac{sin(sin\ x)}{sin\ x}\times\lim_{x\rightarrow 0}{\frac{sin\ x}{x}}
\\=\lim_{u\rightarrow 0}{\frac{sin\ u}{u}}\times\lim_{x\rightarrow 0}{\frac{sin\ x}{x}}=1
\\(which\ u=sin\ x)
\\ \ \ \ 
\\\ \ \ 
4.\lim_{x\rightarrow \infty}2^xsin\frac{sin\ a}{2^x}
\\=\lim_{x\rightarrow \infty}(\frac{sin\frac{sin\ a}{2^x}}{\frac{sin\ a}{2^x}}\times sin\ a)=1\times \lim_{x\rightarrow\infty}sin\ a
\\=sin\ a
\\\ \ \ \ 
\\\ \ \ 
KEY:try\ to\ use\ multiplication\ and\ division(better\ than\ add\ and\ minus)to\ change\ the\ formula\ to\ the\ important\ limits
$$
# 导数
## 隐函数求导
~~想想自己高考压轴题好像是因为用了隐函数求导才扣了分，如果不扣是不是可以140+了呢？这么一说高中还不如不掌握。~~ 
### 高中的simple  task
第一次听说隐函数求导是在高中的时候，如果没记错的话是老师在圆锥曲线中补充的内容，因为上课抛出了一个问题：怎么在短时间内快速地求出圆锥曲线在某一点的切线方程，尤其对于双曲线与椭圆来说。因为我们知道圆锥曲线的解析几何表达本质上只是一种$x$与$y$的对应关系，虽然它不是函数，但是还是可以求出$y$对于$x$的导数然后求出结果。为了让这篇博客看起来更长，我们先回忆一下三种最基本的圆锥曲线：
$$
\frac{x^{2}}{a^{2}}\ +\ \frac{y^{2}}{b^{2}}\ =\ 1
\\\frac{x^{2}}{a^{2}}\ -\ \frac{y^{2}}{b^{2}}\ =\ 1
\\y^{2}\ =\ 2px
$$
我们仅讨论高中时候遇到最多的情况，焦点在$x$轴上，现在我们来回忆一下实现思路：
把$x$与$y$分别放在等号的两边，然后抓住重点就是两边同时求导，并且我们注意到此时$y$是复合函数，这也是这种方法的关键所在，我们就愉快地求出了切线方程的通式：
$$
y^{2}=b^{2}\ -\ \frac{a^{2}}{b^{2}}x^{2}
\\simultaneous\ derivation\ of\ both\ sides:
\\2y\ \times\ y^{'}=-2\frac{a^{2}}{b^{2}}x
\\y^{'}=-2\frac{a^{2}x}{b^{2}y}
$$
### 大学的hard task（雾）
粗略阅读Weiping的笔记，我们发现其实很大一部分仍然是两边同时求导，只不过可能会麻烦一些，基础思路都是把$y^{'}$单独表示出来，然后还有一类是要通过取对数变换这些操作完成，我们以一个经典题目为例，为什么说它经典，是因为从高中听到大学，老师讲了两年，但我仍未掌握，与其说没掌握，不如说没听过。
$$
find \ the\ derivative\ of\ the\ following\ function:
\\y=x^{x}
$$
我们先观察一下这种阴间结构没办法用最基本的法则表达出来，然后我们想到一个万金油思路，***在高等代数中，碰到难以解决的高次项问题，我们的第一思路是取对数降次，所以我们选择自然对数***，其实这是一种很重要的思想，取对数往往能将看似复杂的问题变得异常简单。要得开干！
$$
y=x^{x}
\\natural\ log\ for\ both\ sides:
\\ln\ y=xln\ x
\\calculate\ the\ dirvative\ of\ both\ sides:
\\y^{'}\times\frac{1}{y}=1\ +\ ln\ x
\\y^{'}=y\ +\ yln\ x
\\or\ we\ note\ it\ as\ (the\ better\ and\ former\ expression):
\\y^{'}=x^{x}(1\ +\ ln\ x)
$$
我们最后能化成只有自变量的是最好的，注意完美性与鲁棒性。值得一提的是其实作为一个水题自己却搁置了很久，然后第一遍上手还做错了，最主要的是右边少乘了一个$y$,只能说彩笔本质暴露无遗。
### 新的思考
正当我准备进行下一part的总结时，破天荒的头一次细看了一下note，居然发现了一些新的东西。原来之前自己的格局小的不行了，一直觉得隐函数求导只能用于基础法则不适用的函数，但对于某些复杂的函数也有奇效，我们先再看一道$Weiping's \ note$的例题，再来分析一下在大格局中它的用处。
$$
find\ the\ dirvative\ of\ the\ following\ function:
\\y=\frac{e^{x}\sqrt{1-x^{2}}}{1+x+x^{2}}
$$
当然对于头铁的人来说强上一点问题都没有，不过我们仔细观察一下这个函数的结构，存在自然对数，三个子函数之间都是用乘法与除法相连接起来。我们回忆一下高中数学的内容，什么运算符有加减运算法则而没有乘除运算法则呢？——原来是两边取对数。
~~**格局打开**~~ 
其实这又回到了我们刚刚总结过的问题，也就是在代数中碰到复杂的式子，尤其涉及到乘除运算时，取对数一定是我们的第一选择，再加上隐函数求导已经不是非法手段，所以可以随便取了。不说废话了，开始表演。
$$
natural\ log\ for\ both\ sides:
\\ln\ y=ln\ (\frac{e^{x}\sqrt{1-x^{2}}}{1+x+x^{2}})
\\ln\ y=ln\ e^{x}\ +\ ln\ (\sqrt{1-x^{2}})\ -\ ln\ (1+x+x^{2})
\\ln\ y=x\ +\ \frac{1}{2}ln\ (1-x^{2})\ -\ ln\ (1+x+x^{2})
\\find\ the\ dirvative\ of\ both\ sides:
\\\frac{y^{'}}{y}=1\ +\ \frac{-2x}{2(1-x^{2})}\ +\ \frac{1+2x}{1+x+x^{2}}
\\y^{'}=y(1\ +\ \frac{-2x}{2(1-x^{2})}\ +\ \frac{1+2x}{1+x+x^{2}})
\\y^{'}=\frac{e^{x}\sqrt{1-x^{2}}}{1+x+x^{2}}(1\ -\ \frac{x}{(1-x^{2})}\ +\ \frac{1+2x}{1+x+x^{2}})
\\pay\ attention\ to\ the\ simplest\ expression
$$
至此我们回忆一下其实最重要的是其中蕴含的两种思想，一种**是对于难处理的式子进行取对数降次**，一种是**两边同时求导等式仍然成立**
~~感觉写了一堆就这两句话有用~~ 
## 反函数与原函数的导数关系
讨论之前我们先做一个假设：
$$
now\ we\ have\ function\ f(x)\ and\ its\ inverse\ function\ f^{-1}(x)
$$
然后回忆一下对于导数的两种表示方法：
$$
f^{'}(x)=\frac{df(x)}{dx}
$$
所以不难想出对于它的反函数来说，***导数应该是原函数导数的倒数*** ，于是：
$$
we\ note \ g(x)\ as\ f^{'}(x)\ 
\\g^{'}(x)=\frac{dg(x)}{dx}=\frac{dg(x)}{df(g(x))}=\frac{1}{f^{'}(g(x))}
$$
其实好像这里不是很清晰的说明了这个问题，于是我们参考一下知乎与$Weiping$的笔记。然后我们发现他们的证明基本是大同小异，具体都是使用$Chain\ Rule$然后得到；
$$
f^{'}(g(x))\times g^{'}(x)=1
$$
简略的记录一下具体得到的过程：
$$
firstly\ we\ know\ that:
\\f(g(x) )= x
\\so\ find\ the\ dirvative\ of\ f(x):
\\f(g(x))^{'}=f^{'}(g(x))\times g^{'}(x)=1
$$
写到这里憨憨博主才意识到一个问题，原来自己一直没有理解这两个导数之间的关系，并不只是简单的倒数，**而需要我们用牛莱两种表示方法重新写一下这个定理：**
$$
g^{'}(x)=\frac{1}{f^{'}(g(x))}
\\or
\\\frac{dg(x)}{dx}=\frac{1}{\frac{df(u)}{du} \lvert _{u=g(x)}}
$$
其实说到这里我们举个例子也就很显然了：
$$
(e^{x})^{'}=e^{x}
\\(lnx^{'})=\frac{1}{x}
\\notr\ f(x)=e^{x}\ and\ use\ the\ rule\ above:
\\lnx=g(x)=f^{-1}(x)
\\g^{'}(x)=\frac{1}{e^{lnx}}=\frac{1}{x}
\\which\ is\ evident
$$
写在最后的就是一定要记住这个公式不是简单的倒数关系，每次不确定时就想想如上举的例子就行了。
## 利用导数进行估算
这一点也是在$Weiping$的note中发现的，可能上课确实讲过，不过因为证明过于绕，所以甚至都没记住结论，于是我们在最先先给出结论：
$$
f(x)\approx f(a)+f^{'}(a)\times (x-a)
$$
然后我们参考note，来思索一下它的证明：
$$
firstly\ we\ know:
\\f^{'}(a)=\lim_{x\rightarrow a}\frac{f(x)-f(a)}{x-a}
\\and\ we\ know\ that\ f^{'}(a)\ is\ a\ const\ number:
\\\lim_{x\rightarrow a} (\frac{f(x)-f(a)}{x-a}-f^{'}(a))=0
\\now\ we\ note\ that:
\\\epsilon = \frac{f(x)-f(a)}{x-a}-f^{'}(a)
\\so:
\\\lim_{x \rightarrow a} \epsilon = 0
\\also\ we\ know\ that:
\\f(x) = f(a)+f^{'}(a)\times(x-a)+\epsilon \times(x-a)
\\both\  \epsilon \ and\ (x-a)\ are \ so\ small\ which\ are\ almost\ 0
\\so\ we\ can\ say\ that:
\\f(x)\approx f(a)+f^{'}(a)\times (x-a)
$$
我们在看完了整个证明过程后，其实发现与其说是证明不如说是在求导过程中意外发现的一个结论，这里需要注意的是$a$与$f(x)$的选取，是一个会出现坑的地方，例如：
$$
Question: \sqrt{1.02} \approx?
$$
其实我们可以有很多种选取方法，不过note中提到了一种我认为最简单的方法：
$$
we\ note\ that:
\\f(x)=\sqrt{1+x}\ and\ a=0
\\so:
\\\sqrt{1.02}=f(0.02)
\\f(0.02)\approx f(0)+f^{'}(0)\times(0.02-0)=1.01
$$
看到这里我们不禁想起了这样一个让我永远无法忘记的问题：
$$
we\ know\ that:
\\a=2ln1.01\ and\ b=ln1.02\ and\ c=\sqrt{1.04}-1
\\find \ the\ biggest\ and\ smallest\ number\ of\ three
$$
来自2021普通高等学校招生全国统一考试数学乙卷12题，虽然说当时是想出了严格正解，但四个月后坐在HKUST的图书馆里，我早就忘记了如何切线不等式倒出了结果。（雾）
$$
it\ is\ obviously\ that:
\\a=ln1.01^{2}=ln1.0201>ln1.02\ \rightarrow \ a>b
\\so\ we\ need\ to\ get\ the\ approximate\ value\ of\ c:
\\we\ note\ that:
\\f(x)=\sqrt{1+x}\ and\ a=0
\\so:
\\\sqrt{1.04}=f(0.04)
\\f(0.04)\approx f(0)+f^{'}(0)\times(0.04-0)=1.02
\\c\approx0.02
\\\\we\ note\ that:
\\g(x)=ln(1+x)\ and\ a=0
\\ln(1.02) = g(0.02)
\\g(0.02)\approx g(0)+g^{'}(0)\times(0.02-0)=0.02
$$
~~于是就麻了~~ 
其实很简单的一个道理就是因为取值的不同会导致可能是不足估计值也可能是过剩估计值，其实也就图一乐，真正比大小还得看切线不等式。于是激起了憨憨博主的好胜心。
~~告辞了，哪天闲了再填坑~~ 
## 与绝对值有关
Y1S1好像这一部分的内容都和note有关，都是从note上扒下来的，主要是这样一个问题，参数带绝对值时求导所得和不带绝对值时求导所得是否相同？
不过又说起来带绝对值了以后可导不可导都两说。那我们考虑一个可导的例子：
$$
y=ln\vert x\vert
$$
反正在代数中，带有绝对值的问题我们从来都是分类讨论的，于是尝试一下：
$$
when\ x>0:
\\evidently:y^{'}=\frac{1}{x}
\\when\ x<0
\\y=ln(-x)
\\y^{'}=\frac{1}{-x}\times(-1)=\frac{1}{x}
\\so\ we\ can\ say:
\\(ln\vert x \vert)^{'}=\frac{1}{x}
$$
大致就是在定义域\可导范围内分类讨论就vans了，不过说到这里还是记得判断一下可导不可导比较OK。
## local maximum and absolute maximum
暂时不考先鸽掉
## Tricky Question
$$
Problem1:as\ we\ know\ f(x)=x^x\ and\ g(x)\ is\ its\ inverse\ function
\\find \ g'(4)
\\\ \ \ \ 
\\Problem2:find\ the\ divrative\ of\ tan^{-1}(cos\ 6x)
\\ \ \ \ \ 
\\Problem3:as\ we\ know\ f(x)=\sqrt{|x|}\ tan\ |x|^{\frac{3}{2}},
\\find\ f'(0)
\\\ \ \ \ \ 
\\Problem4:as\ we\ know\ f(x)=\frac{4^x-2^x}{x}
\\find\ \lim_{x\rightarrow 0}f(x)\ and \ without\ Lobita's\ Rule
$$
## Solution to Tricky Question
$$
Sol.1
\\firstly\ let's\ review\ how\ to\ find\ derivative\ of\ an\ inverse\ function:
\\write\ in\ two\ different\ giants'\ ways(suppose\ g(x)\ is\ an\ inverse\ function\ of\ f(x)):
\\g'(x)=\frac{1}{f'(g(x))}
\\\frac{dg(x)}{dx}=\frac{1}{\frac{df(u)}{du}|_{u=g(x)}}
\\With\ it\ is\ almost\ impossible\ to\ find\ g(x),\ we\ just\ consider\ f'(x)\ in\ one\ point
\\according\ to\ our\ former\ record,\ we\ know\ that:
\\f^{'}(x)=x^{x}(1\ +\ ln\ x)
\\according\ to\ the\ connection\ of\ inverse\ function\ and\ original\ function
\\f(g(x))=x:
\\f(g(4))=4\rightarrow g(4)=2
\\so\ g'(4)=\frac{1}{f'(2)}=\frac{1}{4+4ln2}
\\ \ \ \ 
\\Sol.2
\\Also\ about \ inverse\ function\ and\ original\ function\ and\ I\ made\ a\ mistake\ at\ the\ first\ time
\\as\ the\ formula\ in\ Sol.1,firstly:
\\note\ f(x)=tan^{-1}(cos\ 6x)\ and\ u=cos\ 6x
\\so\ f'(x)=f'(u)\times u'
\\f'(u)=\frac{1}{\frac{1}{cos^2(tan\ u)}}=\frac{1}{1+u^2}
\\u'=-6sin\ 6x
\\so\ f'(x)=-6sin\ 6x\times \frac{1}{1+u^2}=\frac{-6sin\ 6x}{1+cos^2\ 6x}
\\\ \ \ \ 
\\Sol.3
\\Actually\ it\ is\ tricky\ because\ it\ is\ really\ easy\ to\ make\ mistake\ on\ this\ problem
\\because\ if\ we\ insist \ finding\ the\ dervative\ of\ f(x)\ (when\ x\ge 0):
\\we\ may\ ignore\ that\ for\ \sqrt{x},the\ slope\ of\ its\ tagent\ line(when\ x=0)\ is\ infinity,
\\which\ means\ its\ dervative\ when\ x=0\ doesn't\ exist.
\\It\ is\ as\ a\ REMINDER\ when\ we\ use\ rules\ of\ dervative,\ we\ must\ first\ judge\ if\ its\ dervative\ exist.
\\so\ we\ apply\ the\ definition：
\\f'(0)=\lim_{x\rightarrow 0}\frac{f(x)-f(0)}{x-0}
\\and\ divide\ it\ into\ two\ cases:
\\case1:
\\\lim_{x\rightarrow 0^+}\frac{f(x)-f(0)}{x-0}
\\=\lim_{x\rightarrow 0^+}\frac{\sqrt{x}\ tan\ x^{\frac{3}{2}}}{x}=\lim_{x\rightarrow 0^+}\sqrt{x}\frac{sin\ x^\frac{3}{2}}{cos\ x^\frac{3}{2}x}
\\=\lim_{x\rightarrow 0^+}\frac{sin\ x^\frac{3}{2}}{x^\frac{3}{2}}\times \lim_{x\rightarrow 0^+}\frac{x}{cos\ x^\frac{3}{2}}=1
\\case2:
\\\lim_{x\rightarrow 0^-}\frac{f(x)-f(0)}{x-0}
\\=\lim_{x\rightarrow 0^-}\frac{\sqrt{-x}\ tan\ (-x)^{\frac{3}{2}}}{x}=1(as\ the\ same\ way)
\\ \ \ \ \ 
\\Sol.4
\\\lim_{x\rightarrow 0}f(x)
\\=\lim_{x\rightarrow 0}\frac{4^x-2^x}{x}=\lim_{x\rightarrow 0}\frac{2^x(2^x-1)}{x}
\\=1\times\lim_{x\rightarrow 0}\frac{2^x-2^0}{x-0}=1\times (2^x)'|_{x=0}
\\=1\times2^xln\ 2|_{x=0}=ln\ 2
\\we\ may\ conclude\ from\ Problem\ 4\ that\ limits\ and\ dervatives\ have\ close\ connection
\\we\ may\ use\ definition\ to\ find\ a\ dervative\ if\ the\ rules\ are\ not\ fit
\\we\ may\ change\ limits\ to\ dervatives\ if\ it's\ not\ clear\ for\ calculating\ limits(\frac{0}{0},\frac{\infty}{\infty},etc.)
$$