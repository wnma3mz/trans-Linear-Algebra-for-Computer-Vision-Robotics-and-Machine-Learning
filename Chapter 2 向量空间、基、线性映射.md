第二章
向量空间、基、线性映射
2.1动机：线性组合、线性独立性和等级
在线性优化问题中，我们经常遇到线性方程组。例如，考虑在三个变量x1、x2、x3中解三个线性方程组的问题∈r：
x1+2x2−x3=1
2x1+x2+x3=2 x1−2x2−2x3=3。
解决这个问题的一种方法是引入“向量”u、v、w和b，由

把我们的线性系统写成
x1u+x2v+x3w=b.
在上述方程中，我们隐式地使用了一个事实，即向量z可以乘以一个标量λ∈r，其中
，
可以加上两个向量y和z，其中
y1 y1+z1 y+z=y2+z2 y2+z2。Y3 Z3 Y3+Z3型
十五

另外，给定一个向量
，
我们将x（发音为负x）的加性逆x定义为
.
观察−x=−1）x，x乘以−1的标量。
三分量矢量的集合用r3×1表示。使用符号r3×1而不是更传统的符号r3的原因是，r3×1的元素是列向量；它们由三行和一列组成，这解释了上标3×1。另一方面，r3=r×r×r由形式（x1，x2，x3）的所有三个三元组组成，其中x1，x2，x3∈r，这些都是行向量。然而，在r3×1和r3之间有一个明显的双射现象，通常被识别出来。为了清晰起见，在本文的介绍中，我们将用rn×1表示n个分量的列向量集。一种表达式，如
x1u+x2v+x3w
其中u、v、w是向量，xis是标量（在r中），称为线性组合。利用这个概念，解线性系统的问题
x1u+x2v+x3w=b.
相当于确定b是否可以表示为u、v、w的线性组合。
现在，如果向量u，v，w是线性无关的，这意味着没有三重（x1，x2，x3）=（06，0,0），这样
x1u+x2v+x3w=03，
可以看出，r3×1中的每一个矢量都可以写成u，v，w的线性组合。这里，03是零矢量。
.
习惯上滥用符号，写0而不是03。这很少引起问题，因为在大多数情况下，0表示标量零还是零向量都可以从上下文中推断出来。
实际上，每一个向量z∈r3×1都可以用一种独特的方式写成一个线性组合。
Z=x1u+x2v+x3w。
这是因为如果
Z=x1u+x2v+x3w=y1u+y2v+y3w，
然后使用我们的（线性！）对向量的运算，我们得到
（y1−x1）u+（y2−x2）v+（y3−x3）w=0，
这意味着
y1−x1=y2−x2=y3−x3=0，
线性独立。因此，
y1=x1，y2=x2，y3=x3，
这表明Z有一个独特的表达式作为线性组合，如声明的那样。那么我们的方程
x1u+x2v+x3w=b
有一个独特的解决方案，事实上，我们可以检查
x1=1.4 x2=-0.4 x3=-0.4
是解决方案。
但是，我们如何确定一些向量是线性无关的呢？
一个答案是计算一个数字量det（u，v，w），称为（u，v，w）的行列式，并检查它是否为非零。在我们的例子中，结果是
，
这证实了u，v，w是线性无关的。
对于具有大量变量的系统来说，其他更好的方法包括计算LU分解或QR分解，或由三列u、v、w组成的矩阵的SVD。
.
如果我们形成未知向量
，
那么我们的线性组合x1u+x2v+x3w可以写成矩阵形式
，
所以我们的线性系统表示为

或者更简明扼要地说	二
一
2	，
ax=b。
如果向量u，v，w是线性相关的呢？例如，如果我们考虑向量
2_
V=1，
1
我们看到了
u−v=w，
a	非平凡线性依赖。可以证明U和V仍然是线性无关的。现在来解决我们的问题
x1u+x2v+x3w=b
必须是b可以表示为u和v的线性组合的情况。但是，结果表明u，v，b是线性独立的（一种方法是计算行列式det（u，v，b）=-6），因此b不能表示为u和v的线性组合，因此，我们的系统没有单独的tion.
如果我们把向量b改为
3 b=3，
零
然后
b	=U+V，
所以这个系统
x1u+x2v+x3w=b
有解决方案
x1=1，x2=1，x3=0。
实际上，由于w=u-v，上述系统相当于
（x1+x3）U+（x2-x3）V=B，
因为u和v是线性无关的，所以x1+x3和x2-x3中的唯一解是
x1+x3=1 x2−x3=1，
它产生无穷多个由x3参数化的解，即
x1=1−x3 x2=1+x3。
总之，一个3×3线性系统可能有一个唯一的解，没有解，或无限多个解，这取决于线性独立性（和相依性）或向量u、v、w、b。这种情况可以推广到任何n×n系统，甚至任何n×m系统（m变量中的n个方程）。我们稍后会看到。
我们的线性系统以矩阵形式表示为a x=b的观点强调了这样一个事实：map x 7→ax是一个线性变换。这意味着
A（λx）=λ（ax）
对于所有x∈r3×1和所有λ∈r，以及
a（u+v）=au+av，
对于所有u，v∈r3×1。我们可以将矩阵A看作是表示从r3×1到r3×1的线性映射的一种方法，并且求解系统ax=b等于确定b是否属于该线性映射的图像。
给出3×3矩阵
，
其列是三个向量，分别表示a1、a2、a3，并且给定任何向量x=（x1、x2、x3），我们将积ax定义为线性组合。
.
常见的模式是，a x的第i个坐标由称为内积的某种积给出，行向量的第i行a乘以列向量x：
.
一般来说，给定任意两个向量x=（x1，…，xn）和y=（y1，…，yn）∈rn，它们的内积表示x·y，或hx，yi，是数字。
.
内部产品起着非常重要的作用。首先，我们数量

是向量长度的泛化，称为欧几里得范数或'2-范数。第二，可以证明我们有不等式
| X·Y≤KXKKYK，
因此，如果x，y=06，比值（x·y）/（kxkkkk）可以看作一个角的余弦，即x和y之间的角。特别是，如果x·y=0，那么向量x和y使角π/2，也就是说，它们是正交的。保留内积的（平方）矩阵q，在hqx，q yi=hx，yi对所有x，y∈rn的意义上，也起着非常重要的作用。它们可以被认为是广义旋转。
m返回到矩阵，如果a是由p n列n a1，…，an（in r）组成的m×n矩阵，b是由p列b1，…，b（in r）组成的n×p矩阵，我们可以形成p向量（in rm）。
AB1，…，ABP。
这些p向量构成m×p矩阵，表示为dj ab，其jth列为abj。但是我们知道AB的第i个坐标是A的第i行与B的第j列的内积，
.
因此，我们定义了矩阵上的乘法运算，即如果a=（aik）是m×n矩阵，如果b=（bjk）是n×p矩阵，则其乘积ab是m×n矩阵，其第i行和第j列上的项由a第i行的内积和b第j列给出。
.
注意，与实数（或复数）的乘法不同，如果a和b是两个n×n矩阵，一般来说，ab=6ba。
假设a是一个n×n矩阵，我们正试图解线性系统。
ax=b，
带b∈rn。假设我们能找到一个n×n矩阵b，这样
Bai=Ei，I=1，…，N，
 	一
零
…
零
零	零
一
…
零
零	小精灵
小精灵
···…
小精灵
小精灵	零
零
…
一
零	0℃
0_
…，
0 1
对于ei=（0，…，0,1,0…，0），其中第i个槽中的唯一非零条目是1。如果我们形成nn矩阵
1 0 0 0 0 0
称为单位矩阵，其第i列为ei，则上面的值等于
BA=英寸
如果ax=b，那么用左边的两边乘以b，我们得到
b（ax）=bb。
但很容易看出b（ax）=（ba）x=inx=x，所以我们必须
x=bb。
我们可以验证x=bb确实是一个解，因为可以证明
a（b b）=（ab）b=inb=b。
不明显的是，ba=in意味着ab=in，但这确实是可以证明的。矩阵B通常表示为A−1，称为A的逆矩阵。可以证明它是唯一的矩阵，因此
a a−1=a−1a=英寸。
如果一个方阵A有一个逆矩阵，那么我们说它是可逆的或非奇异的，否则我们说它是奇异的。稍后我们将证明一个平方矩阵是可逆的，如果它的列是线性无关的，如果它的行列式是非零的。
总之，如果a是平方可逆矩阵，那么线性系统a x=b的唯一解x=a−1b。实际上，这不是求解线性系统的好方法，因为计算a−1太昂贵。求解线性系统的一种实用方法是高斯消元法，将在第7章中讨论。求解线性系统ax=b的其他实用方法是利用a的因式分解（qr分解，svd分解），使用下一个定义的正交矩阵。
给定一个m×n矩阵a=（akl），n×m矩阵），其第i行是a的第i列，这意味着a>i j=aji（i=1，…，n和j=1，…，m）被称为a的转置。n×n矩阵q使得
q q>=q>q=in
称为正交矩阵。等效地，正交矩阵q的逆q−1等于其转置q>。正交矩阵起着重要作用。几何上，它们对应于保持长度的线性变换。线性代数的一个主要结果表明，每个m×n矩阵a都可以写成
A=V∑U>，
其中v是m×m正交矩阵，u是n×n正交矩阵，∑是m×n矩阵，其中只有非零项是非负对角项，σ1≥σ2≥···············································或SVD。
SVD可用于“求解”线性系统ax=b，其中a是m×n矩阵，即使该系统没有解。当存在更多的变量（m>n）方程时，可能会发生这种情况，在这种情况下，系统被过度确定。
当然，没有奇迹，无法解决的系统没有解决方案。但是我们可以寻找一个很好的近似解，也就是向量x，它可以最小化误差的某些度量，ax-b.legendre和gauss，这是误差的平方欧几里德范数。这个量是可微的，结果是有一个唯一的向量x+的最小欧几里得范数最小化。此外，x+由表达式x+=a+b给出，其中a+是a的伪逆，a+可以从a的svd a=v∑u>计算得出。实际上，a+=u∑+v>，其中∑+是从∑得到的矩阵，用其逆σi-1替换每个正奇异值σi，保留所有的零中心。S完好无损，并且正在换位。
我们不需要搜索最小欧几里得范数的向量，而是可以添加惩罚项（对于某些正值和最小化的量）。这种方法称为岭回归。结果发现，有一个独特的最小化x+，由x+=（a>a+kin）−1a>b给出，如第二卷所示。
另一种方法是替换惩罚条款，其中kxk1=x1|+
···+| xn（x的'1-范数）。值得注意的是，kax−bk22+k kxk1的最小值x趋于稀疏，这意味着x的许多分量等于零。这种被称为lasso的方法在机器学习中很流行，将在第二卷中讨论。
SVD的另一个重要应用是主成分分析（PCA），它是数据分析中的一个重要工具。
另一种解释系统ax=b的解决方案的有效方法是把这个问题看作一个交叉问题。实际上，每一个方程
x1+2x2−x3=1
2x1+x2+x3=2 x1−2x2−2x3=3
定义实际上是平面的r3的子集。第一个方程
x1+2x2−x3=1
定义穿过坐标轴上三个点（1,0,0），（0,1/2,0），（0,0，−1）的平面h1，第二个方程
2x1+x2+x3=2
定义穿过坐标轴上三个点（1,0,0）、（0,2,0）、（0,0,2）和第三个方程的平面h2
x1−2x2−2x3=3
定义穿过坐标轴上三个点（3,0,0）、（0、−3/2,0）、（0,0、−3/2）的平面H3。见图2.1。

图2.1：由前面的线性方程定义的平面。
任意两个不同平面hi和hj的交点hi hj是一条线，三个平面的交点h1 h2 h3由单点（1.4、-0.4、-0.4）组成，如图2.2所示。

图2.2：系统的解是三个平面中每个平面的共同点。
与系统相对应的平面
x1+2x2−x3=1
2x1+x2+x3=2 x1−x2+2x3=3，
如图2.3所示。这个系统没有解决方案，因为没有同时点-

图2.3：方程式x1+2x2−x3=1、2x1+x2+x3=2和x1−x2+2x3=3定义的平面。
完全包含在所有三个平面中；见图2.4。

图2.4：线性系统x1+2x2−x3=1，2x1+x2+x3=2，x1−x2+2x3=3没有解决方案。
最后，系统对应的平面
x1+2x2−x3=3
2x1+x2+x3=3 x1−x2+2x3=0，
如图2.5所示。

图2.5：方程式x1+2x2−x3=3、2x1+x2+x3=3和x1−x2+2x3=0定义的平面。
这个系统有无穷多的解，由（1−x3,1+x3，x3）参数给出。几何上，这是所有三个平面共用的一条线；见图2.6。
在上面的解释中，观察我们关注的是矩阵A的行，而不是它的列，如前面的解释中所述。

图2.6：线性系统x1+2x2−x3=3，2x1+x2+x3=3，x1−x2+2x3=0具有所有三个平面共用的红线。
线性代数被证明是非常有效的现实问题的另一个很好的例子是数据压缩问题，也就是说，用更小的存储量表示一个非常大的数据集。
通常，数据集表示为m×n矩阵a，其中每一行对应一个n维数据点，通常m≥n。在大多数应用中，数据不是独立的，因此a的秩比m in m，n小得多，低秩分解的目标是因子a作为两个矩阵b和c的乘积，其中b是m×k矩阵，c是k×n矩阵，其中（此处表示“远小于”）：
γ
γ
γ
γ
γ
γ	一	 
 
 
 
 
=	乙	 	C	γ
γ
mn__m×k_
k n
 	
 	
现在，像上面那样找到一个精确的因式分解通常是很昂贵的，所以我们寻找一个低阶矩阵a0，它是A的“好”近似值。为了使这句话精确，我们需要定义一个机制来确定两个矩阵有多接近。这可以通过使用矩阵规范来实现，这个概念在第8章中讨论过。矩阵A的范数是一个非负实数Kak，它的行为与实数X的绝对值X非常相似。那么我们的目标是找到一些低阶矩阵a0，使范数最小化。
kA−a0k2，
对于某些给定的矩阵，a0的秩至多为k。
低阶近似的一些优点是：

1.	表示a所需元素较少，即k（m+n）而不是mn。因此，重建A所需的存储和操作更少。
2.	通常，获取分解的过程公开了数据的底层结构。因此，可能会发现，“大部分”重要数据集中在一些称为主方向的方向上。
一组数据的低阶分解在工程上有许多应用，包括计算机科学（特别是计算机视觉）、统计学和机器学习。正如我们将在第21章后面看到的，奇异值分解（SVD）为低阶近似问题提供了一个非常令人满意的解决方案。然而，在许多情况下，数据集太大，需要另一个因素：随机化。然而，作为第一步，线性代数通常会产生一个好的初始解。
我们现在将更加精确地知道在向量上允许什么样的操作。在1900年初，矢量空间的概念作为处理“线性”物体的方便统一的框架出现，我们将在接下来的几节中讨论这个概念。
2.2向量空间
一个（实）向量空间是一个集合e加上两个运算，+：e×e→e和·：r×e→e，称为加法和标量乘法，满足一些简单的性质。首先，e在加法下必须是一个交换（或阿贝尔）群，这是我们接下来要讨论的概念。
然而，请记住，向量空间不仅是代数对象，它们也是几何对象。
定义2.1.一个群是一个具有二元运算·：G×G→G的集合G，它将一个元素A·B∈G与每对元素A、B∈G相关联，具有如下性质：·是关联的，具有一个同一元素E∈G，G中的每一个元素都是可逆的（W.R.T.·）。更明确地说，这意味着以下方程式适用于所有a、b、c∈g：
	（g1）a·（b·c）=（a·b）·c.	（结合性）；
	（g2）a·e=e·a=a。	（身份）；
	（g3）对于每个·a−1=aa−1∈ga，有一些=e.a−1∈g，这样	（反向）。
群G是交换的（或交换的），如果
a·b=b·a，对于所有a，b∈g。
一个集合m加上一个操作·：m×m→m和一个只满足条件（g1）和（g2）的元素e被称为单体。例如，自然数的集合n=0,1，…，n，…是一个（交换的）单体，与单位元0相加。
然而，它不是一个群体。
下面给出了一些组的例子。
例2.1。
1.	整数的集合z=…，−n，…，−1,0,1，…，n，…是加法下的交换群，具有标识元素0。然而，z=z−0不是乘法下的群；它是一个具有单位元1的交换单体。
2.	有理数（p，q∈z，q=0的分数p/q）6的集合q是一个加上的交换群，单位元为0。集合q=q−0也是一个带单位元素1的乘法下的交换群。
3.	同理，实数的集合r和复数的c是加法下的交换群（单位元为0），而r=r−0和c=c−0是乘法下的交换群（单位元为1）。
4.	实数或复数的n个元组的集合rn和cn是成分加法下的交换群：
（x1，…，xn）+（y1，…，yn）=（x1+y1，…，xn+yn）
具有标识元素（0，…，0）。
5.	对于任何非空集合s，f:s→s的双射集合，也称为s的排列，是函数组合下的一个组（即f和g的乘法是组合g_f），同一元素是同一函数ID。只要S有两个以上的元素，这个群就不是阿贝尔群。
6.	实数（或复数）系数的n×n矩阵集是矩阵相加下的一个交换群，其单位元为空矩阵。用mn（r）（或mn（c））表示。
7.	一个变量x中所有多项式的集合r[x]具有实数系数，
p（x）=anxn+an−1xn−1+····+a1x+a0，
（用ai∈r），是多项式加在一起的阿贝尔群。单位元是零多项式。
8.	具有实（复）系数的n×n可逆矩阵集是矩阵乘法下的一个群，其单位元为单位矩阵。这个群称为一般线性群，通常用gl（n，r）（或gl（n，c））表示。
9.	具有实（或复）系数和行列式+1的n×n可逆矩阵集是矩阵乘法下的一组，其单位元为单位矩阵。这个群称为特殊线性群，通常用sl（n，r）（或sl（n，c））表示。
10.	具有实系数的n×n可逆矩阵的集合，如r r>=r>r=in和行列式+1是一个称为特殊正交组的组（在矩阵乘法下），通常用so（n）表示（其中r>是矩阵r的转置，即r>的行是F R）。它对应于RN中的旋转。
11.	给定一个开放区间（a，b），连续函数f:（a，b）→r的集合c（a，b）是操作f+g下的一个交换群，定义如下：
（f+g）（x）=f（x）+g（x）
对于所有x∈（a，b）。
通常用+表示阿贝尔群G的运算，在这种情况下，元素A∈G的逆A−1用−A表示。
组的标识元素是唯一的。事实上，我们可以证明一个更普遍的事实：
提案2.1.如果一个二元运算·：m×m→m是关联的，如果e0∈m是左恒等式，e00∈m是右恒等式，这意味着
e0·a=a表示所有a∈m（g2l）
和
a·e00=a，所有a∈m，（g2r）
则e0=e00。
证据。如果方程（g2l）中a=e00，我们得到
e0·e00=e00，
如果我们在方程（g2r）中让a=e0，我们得到
e0·e00=e0，
因此，e0=e0·e00=e00，
如要求。
命题2.1意味着一个单体的同一元素是唯一的，并且由于每个群都是一个单体，所以一个群的同一元素是唯一的。此外，一个组中的每个元素都有一个唯一的逆矩阵。这是一个更普遍的事实的结果：
提案2.2.在具有单位元e的单元体m中，如果某个元素a∈m有左逆a0∈m和右逆a0∈m，这意味着
a0·a=e（g3l）
和
a·a00=e，（g3r）
则a0=a00。
证据。利用（g3l）和e是一个身份元素的事实，我们有
（a0·a）·a00=e·a00=a00。
同样，使用（g3r）和e是一个标识元素的事实，我们有
a0·（a·a00）=a0·e=a0。
然而，由于m是单体的，运算·是关联的，所以
a0=a0·（a·a00）=（a0·a）·a00=a00，
如要求。
注：公理（g2）和（g3）可以通过只要求（g2r）（正确身份的存在）和（g3r）（每个元素都存在一个正确的反义词）（或（g2l）和（g3l））而稍微减弱。证明群公理（g2）和（g3）遵循（g2r）和（g3r）是一个很好的练习。
向量空间是一个阿贝尔群E，它有一个称为标量乘法的附加运算·：k×e→e，它允许用k中的元素重新调整e中的向量。集合k本身是一个称为场的代数结构。场是一种特殊的结构，称为环。这些概念定义如下。我们从戒指开始。
定义2.2.加法）和：a a×ringa→是具有以下属性的seta（被称为带两个操作的被叫方+：乘法）：a×a→a:（称为
（r1）a是阿贝尔群w.r.t.+；
（r2）是关联的，并且具有一个标识元素1∈a；
（r3）是分布的w.r.t.+。
加法的单位元表示为0，a∈a的加法逆表示为−aa。更明确地说，一个环的公理是下列方程：对于所有a，b，c∈
	A+（B+C）=（A+B）+C（正的结合性）	（2.1）
	A+B=B+A（交换性为+）	（2.2）
	A+0=0+A=A（零）	（2.3）
	A+（−A）=（−A）+A=0（加性逆）	（2.4）
	A（B C）=（A B）C（关联性）	（2.5）
	A 1=1 A=A（标识为）	（2.6）
	（a+b）c=（a c）+（b c）（分布性）	（2.7）
A（B+C）=（A B）+（A C）（分布性）
如果
A B=B A代表所有A，B A。
	从（2.7）和（2.8）我们很容易获得	（2.8）
	A 0=0 A=0	（2.9）
	A（−B）=（−A）B=−（A B）。	（2.10）
注意，（2.9）意味着如果1=0，那么a=0 a is称为两个元素的b是一个交换环（带单位1），对于任何场平凡环a，b。对于1 a的环，通常用a=0表示所有a=06 aab，因此称为。nontrivialka，abellian=0。这个。乘法
多项式的阿贝尔群k[x]也是一个交换环（也有单位1）。剩余模M的集合z/mz，其中m是一个正整数，是一个交换环。
场是一个交换环k，其中k−0是一个乘法下的群。
定义2.3.如果集合k是一个环，则它是一个字段，并且以下属性保持不变：
（f1）0 6=1；
（F2）k=k−0是一组w.r.t.（即，每a 6=0有一个逆w.r.t.）；
（f3）是交换的。
如果不是交换的，但（f1）和（f2）保持不变，我们就说我们有一个斜场（或非交换场）。
注意，我们假设一个场的运算是交换的。这一惯例并不是普遍采用的，但由于对我们将遇到的大多数领域都是可交换的，所以我们也可以在定义中包括这一条件。
例2.2.
1.	环q、r和c是字段。
2.	剩余模p的集合z/pz，其中p是素数，则为字段。
3.	G（形式）分数集（x）不是零多项式，是多项式f（x），g（x）的f（x）/g（x），其中
向量空间定义如下。
定义2.4.实向量空间是一个集合e（向量），加上两个操作+：e×e→e（称为向量加法）和·：r×e→e（称为标量乘法），满足所有α、β∈r和所有u、v∈e的下列条件；
（v0）e是一个具有标识元素0的阿贝尔群w.r.t.+；
（v1）α·（u+v）=（α·u）+（α·v）；
（v2）（α+β）·u=（α·u）+（β·u）；
（v3）（αβ）·u=α·（β·u）；
（v4）1·u=u。
在（v3）中，表示R中的乘法。
给定α∈R和V∈E，元素α·V也用αV表示，R场常称为标量场。
在定义2.4中，R域可以被复数C域取代，在这种情况下，我们有一个复数向量空间。甚至可以用有理数q的字段或任意字段k（例如z/pz，其中p是质数）替换r，在这种情况下，我们有一个k向量空间（in（v3），表示字段中的乘法。本章中的所有结果都是hold fork）。在大多数情况下，场k是实数的场r，但在任意场上是向量空间。
从（v0），向量空间总是包含空向量0，因此是非空的。从（v1），我们得到α·0=0，α·（−v）=−（α·v）。从（v2）中，我们得到0.v=0和（−α）·v=−（α·v）。
公理的另一个重要后果是：
提案2.3.对于任何u∈e和任何λ∈r，如果λ6=0和λ·u=0，则u=0。
证据。实际上，由于λ=06，它有一个乘法逆λ−1，因此从λ·u=0，我们得到
λ−1·（λ·u）=λ−1·0。
然而，我们只是观察到λ−1·0=0，从（v3）和（v4），我们已经
λ−1·（λ·u）=（λ−1λ）·u=1·u=u，
我们推断u=0。
备注：您可能会怀疑是否真的需要AXIOM（v4）。它能从其他公理推导出来吗？答案是否定的。例如，可以取e=rn并定义
·R×RN→RN by
λ·（x1，…，xn）=（0，…，0）
对于所有（x1，…，xn）∈rn和所有λ∈r，公理（v0）–（v3）都满足，但（v4）失败。使用尚未定义的基的概念可以给出一些不那么简单的例子。
字段r本身可以看作是一个向量空间，向量的加法是字段中的加法，标量的乘法是字段中的乘法。
例2.3.
1.	r和c是r上的向量空间。
2.	Rn和Cn组是r上的向量空间，标量乘法由
λ（x1，…，xn）=（λx1，…，λxn）
对于任何λ∈r和with（x1，…，xn）∈rn或（x1，…，xn）∈cn，并且cn是c上的向量空间，具有如上所述的标量乘法，但带有λ∈c。
3.	实系数n次多项式的r[x]n环是r上的向量空间，复系数n次多项式的c[x]n环是c上的向量空间，多项式的标量乘λ·p（x）
p（x）=amxm+am−1xm−1+····+a1x+a0
（用ai∈r或ai∈c）用标量λ表示（用r或c表示），用m≤n表示，由
λ·p（x）=λamxm+λam−1xm−1+····+λa1x+λa0。
4.	所有实系数多项式的环r[x]都是r上的向量空间，所有复系数多项式的环c[x]都是c上的向量空间，其标量乘法与上述方法相同。
5.	n×n矩阵的环mn（r）是r上的向量空间。
6.	m×n矩阵的环mm，n（r）是r上的向量空间。
7.	连续函数f：（a，b）→r的环c（a，b）是r上的向量空间，函数f的标量乘λf：（a，b）→r由标量λ∈r给出：
（λf）（x）=λf（x），对于所有x∈（a，b）。
8.	向量空间的一个非常重要的例子是在第2.7节中定义的两个向量空间之间的一组线性映射。下面是一个例子，它将为我们准备线性映射的向量空间。设x为任意非空集，设e为向量空间。所有函数f:x→e的集合可以构成一个向量空间，如下所示：给定任意两个函数f:x→e和g:x→e，让（f+g）：x→e定义为：
（f+g）（x）=f（x）+g（x）
对于所有x∈x，并且对于每个λ∈r，让λf:x→e定义为：
（λf）（x）=λf（x）
对于所有的x∈x，向量空间的公理很容易被验证。
设e为向量空间。我们要定义线性组合和线性独立的重要概念。
在定义这些概念之前，我们需要讨论一个战略选择，它取决于如何解决，在处理诸如线性组合和线性依赖（或独立性）等概念时可能会减少或增加头痛。这个问题与使用向量集和向量序列有关。
2.3索引族；和符号pi∈i ai
我们的经验告诉我们，最好使用向量序列；更好的是，索引向量族。（我们不是唯一一个选择序列超过集合的人，而且我们有很好的合作关系，例如，Artin[3]、Axler[4]和Lang[41]使用序列。然而，一些著名的作者，如LAX[44]使用套装。我们把它留给读者对这个问题进行调查。）
在给定集合A的情况下，回想一个序列是一个有序的n-元组（a1，…，an）∈a中元素的a，对于某个自然数n。序列的元素不必是不同的，顺序是重要的。例如，（a1，a2，a1）和（a2，a1，a1）是a3中两个不同的序列。它们的基础集是a1，a2。
我们刚刚定义的是有限序列，也可以看作是从1,2，…，n到集合A的函数；序列的第i个元素（a1，…，an）是函数下i的图像。这个观点是卓有成效的，因为它允许我们定义（可数）无限

P i∈i
序列作为函数s:n→a。但是，为什么要将自己限制为有序集，如1，…，n或n作为索引集？
索引集的主要作用是唯一地标记每个元素，标记的顺序虽然方便，但并不重要。因此，定义索引族的概念是很自然的。
定义2.5.给定一个集合a，a元素的i-索引族，简而言之，是函数a:i→a，其中i是任何被视为索引集的集合。因为函数A是由它的图决定的
（i，a（i））i∈i，
A族可以看作是成对的A=（I，A（I））I∈I。为了表示简单，我们写a i而不是a（i），并用（ai）i∈i∈i表示家族a=（i，a（i））i∈i，例如，如果i=r，g，b，y和a=n，对的集合
A=（R，2），（G，3），（B，2），（Y，11）
是一个索引族。元素2在族中出现两次，分别带有两个不同的标记r和b。
当索引集i完全有序时，一个族（ai）i∈i通常称为i序列。有趣的是，集合可以看作是家庭的特殊情况。实际上，一个集合a可以被看作是与同一函数对应的a-索引族（a，a）a∈i。
备注：索引族不应与多重集混淆。对于任何集合A，多集都与集合相似，只是集合的元素可能出现多次。例如，如果a=a、b、c、d，则a、a、b、c、c、d、d是多集。每个元素都以一定的多重性出现，但元素的顺序并不重要。例如，a具有多重性3。形式上，多集是一个函数s:a→n，或等价于一组对（a，i）a∈a。因此，多重集是n个元素的a-索引族，而不是n-索引族，因为不同的元素可能具有相同的多重性（如上例中的c和d）。索引族是序列的泛化，而多重集是集合的泛化。
我们还需要注意一个恼人的技术性，即定义形式pi∈i a i的和，其中i是任何有限的索引集，（ai）i∈i是某个集合a中的一个元素族，该集合a装备有一个二元运算+：a×a→a，它是结合的（公理（g1））和交换的。当我们定义线性组合时，就会出现这种情况。
问题是，二元运算+只告诉我们如何计算a的两个元素的a1+a2，但它不告诉我们三个以上元素之和是什么。例如，应该如何定义A1+A2+A3？
我们要做的是用一系列步骤来定义a1+a2+a3，每个步骤都涉及两个元素，有两种可能的方法可以做到这一点：a1+（a2+a3）和（a1+a2）+a3。如果我们的操作+不是关联的，那么它们是不同的值。如果它是关联的，那么a1+（a2+a3）=（a1+a2）+a3，但是指数1、2、3还有六个可能的排列，如果+不是交换的，这些值通常是不同的。如果我们的操作是交换的，那么所有六个置换都有相同的值。因此，如果+是关联的和交换的，那么可以直观地看出形式pi∈i a i的和不依赖于用于计算它的操作的顺序。
确实如此，但严格的证据需要归纳，令人惊讶的是，这样的证据牵涉其中。读者可以不加证明地接受这样一个事实，即形式pi∈i ai的和确实定义得很好，并直接跳到定义2.6。对于那些想看到血淋淋细节的人，我们开始吧。
首先，我们定义和pi∈i a i，其中i是不同自然数的有限序列，比如i=（i1，…，im）。如果i=（i1，…，i m）m≥2，我们用i−i1表示序列（i2，…，im）。我们根据I的尺寸M进行归纳，让
X
ai=ai1，如果m=1，
我爱我
.
例如，如果我=（1,2,3,4），我们有
X
ai=a1+（a2+（a3+a4））。
我爱我
如果操作+不是关联的，则术语的分组很重要。例如，一般来说
A1+（A2+（A3+A4））=（6 A1+A2）+（A3+A4）。
但是，如果操作+是关联的，那么和pi∈i ai不应该依赖于i中元素的分组，只要它们的顺序保持不变。例如，如果i=（1,2,3,4,5），
j1=（1,2）和j2=（3,4,5），我们期望
.
这是事实，因为我们有以下的主张。
提案2.4.给定任意一个非空集a，装备有一个结合二元运算+：a×a→a，对于任意非空有限序列i的不同自然数，以及对于i到p的任何分区，非空序列i k1，…，i kp，对于某些非空序列k=（k1，…，kp），这样ki<kj意味着α<β对于所有α∈iki和所有β∈ikj，对于a中元素的每个序列（ai）i∈i，我们有
.
P i∈i
证据。我们根据i的大小n进行归纳。
如果n=1，那么我们必须有p=1和ik1=i，所以这个命题无关紧要。
接下来，假设n>1。如果p=1，那么ik1=i，公式很简单，所以假设p=2，然后写j=（k2，…，kp）。有两种情况。
案例1。序列ik1有一个单一元素，比如β，它是i的第一个元素。在这种情况下，通过删除i的第一个元素β，为从i获得的序列写c。通过
定义，
和
.
由于c=n−1，根据诱导假设，我们有
，
这就产生了我们的身份。
案例2。序列ik1至少有两个元素。在这种情况下，让β是i的第一个元素（因此是i k1的第一个元素），让i0是从i中通过删除第一个元素β获得的序列，让ik01是从ik1中通过删除第一个元素β获得的序列，让i=2，…，p。回想一下j=（k2，…，kp）和k=（k1，…，kp）。序列I0有n-1个元素，因此通过应用诱导假设，我们得到
.
如果我们把左手边加在Aβ上，根据定义我们得到
X
α。
我一世
如果我们用关联性和一个索引和的定义把右手边加到β上，我们得到
，
如要求。
如果i=（1，…，n），我们也写而不是pi∈i ai。由于+是关联的，命题2.4表明总和独立于其元素的分组，这证明了符号a1+·····+an（没有任何括号）的使用是合理的。
如果我们也假设A上的结合二元运算是交换的，那么我们可以证明和pi∈i ai不依赖于索引集i的次序。
提案2.5.对于任意两个不同自然数的非空有限序列i和j，如果任意一个非空集a配备有结合和交换二元运算+：a×a→a，那么j是i的置换（换句话说，i和j的基本集是相同的），对于每个序列（ai）。A中元素的i∈i，我们有
十倍
aα=aα。α∈iα∈j
证据。我们通过归纳i中元素的数量p来进行，如果p=1，我们就得到i=j，这个命题就无关紧要了。
如果p>1，为了简化表示法，假设i=（1，…，p）并且j是i的置换（i1，…，ip）。首先，假设2≤i1≤p−1，让j0是通过删除i1从j获得的序列，i0是通过删除i1从i获得的序列，让p=（1,2，…，i1−1）和q=（i1+1，…，p-1，p）。观察到序列I0是序列P和Q的串联。通过应用于j0和i0的诱导假设，然后通过应用于i0及其分区（p，q）的命题2.4，我们得出
.
如果我们将左手边添加到ai1，根据定义，我们得到
X
α。J·J
如果我们把右手边加在ai1上，我们得到
.
利用关联性，我们得到
，
然后多次使用关联性和交换性（更严格地说，使用归纳法
P i∈i
在I1-1），我们得到

如要求。
I1=1或I1=P的情况同样处理，但处理方式更简单，因为P=（或Q=）（其中（）表示空序列）。
做了所有这些之后，我们现在可以理解形式pi i ai的和，对于任何有限∈
索引集i和a中元素的任何族a=（ai）i∈i，其中a是一个具有结合性和交换性的二元运算+的集。
事实上，由于i是有限的，它与集合1，…，n是双射的，对于一些n∈n，并且任何全序都对应一个置换（在这里我们用它的图像识别一个置换）。对于所有订单，我们都会定义
.
那么，对于其他的全部订货，我们有
，
既然我和是1，…，n的不同排列，根据命题2.5，我们有
.
因此，sum不依赖于i的总排序。我们将pi i ai和定义为所有总排序的公共值。
γ
下面是一些a=r的例子：

1。如果i=1，，a=（1,2），（2，−3），（3，√2），则pi i ai=2−3+√2=−1+√2。
γ
2.4线性独立性，子空间
向量空间的一个最有用的性质是它们具有基。这意味着在每一个向量空间e中，都有一组向量，e1，…，en，这样每一个向量v∈e都可以写成一个线性组合，
V=λ1e1+····+λnen，
对于ei，对于某些标量，λ1，…，λn∈r。此外，n-元组（λ1，…，λn），如上所述是唯一的。
当e有一个有限的基础，e1，…，en时，这种描述是很好的，但情况并非总是如此！例如，实多项式的向量空间r[x]没有有限基，而是有无限基，即
1，x，x2，…，xn，…
给定一个集合a，回想一个i-索引族（ai）i∈i的元素（简而言之，一个族）是一个函数a:i→a，或等价于一组对（i，ai）i∈i。我们同意，当i=？，（ai）i∈i=？。族（a i）i∈i是有限的，如果我是有限的。
备注：在考虑家族（a i）i∈i时，没有理由假定我是有序的。关键的一点是，族中的每个元素都是由i元素唯一索引的。因此，除非另有规定，否则我们不假定索引集的元素是有序的。
给定两个不相交集i和j，两族（ui）i∈i和（vj）j∈j的并集，表示为
（ui）i （v j）j（vj）j（i（j）定义如下：wk=Uk，如果k（wi）i；（ui）i；（vj）j j）定义如下：wk（wk）k天在k/∈i.给定一个族（ui）i∈i时，（ui）i∈i的一个子族是一个族（uj）j∈j，其中j是i的任何子集。
在本章中，除非另有规定，否则假定所有标量族都是有限的（即，它们的索引集是有限的）。
定义2.6.设e为向量空间。向量v∈e是e的元素的族（ui）i∈i的线性组合，如果r中有一个标量的族（λi）i∈i，则
V=xλiui。
我爱我
当我=时，我们规定v=0。（根据命题2.5，形式pi∈iλi ui的和被很好地定义）我们说，对于r中的每一个scalars（λi）i∈i，一个家族（ui）i∈i是线性独立的iff，
=0表示所有i∈i的λi=0。

等价地，一个族（ui）i∈i是线性相关的，如果R中有一个标量的族（λi）i∈i，那么
X
一些j∈i的λiui=0和λj=06。
我爱我
我们同意当我为∅时，族∅是线性独立的。
注意，定义向量族的线性组合而不是向量集的线性组合的优点是被组合的向量不必是不同的。例如，对于i=1,2,3和族（u，v，u）和（λ1，λ2，λ1），线性组合
X
λiui=λ1u+λ2v+λ1u
我爱我
有道理。在线性组合的定义中使用一组向量不允许这样的线性组合；这太限制了。
解开定义2.6，一个族（ui）i∈i是线性相关的，如果i由单个元素组成，比如i，并且ui=0，或者i≥2，并且族中的一些uj可以表示为族中其他向量的线性组合。实际上，在第二种情况下，在r中有一些标量的族（λi）i∈i，这样
X
一些j∈i的λiui=0和λj=06，
我爱我
由于i≥2，集合i−j是非空的，我们得到
.
注意，定义向量族而不是向量集的线性依赖性的原因之一是，我们的定义允许一个向量多次出现。这很重要，因为矩阵可能包含相同的列，我们想说这些列是线性相关的。集合的线性依赖性的定义不允许我们这样做。
上述结果还表明，一个族（ui）i∈i是线性独立的iff，或者i=∅，或者i由单个元素i和ui=06组成，或者i≥2，并且族中没有向量uj可以表示为族中其他向量的线性组合。
当i非空时，如果族（ui）i∈i是线性独立的，注意ui=06表示所有i∈i，否则，如果ui=0表示某些i∈i，则我们通过选取任何非零的λi并让λk=0表示所有k∈i（k 6=i），得到一个非平凡的线性依赖pi∈iλiui=0，因为λi 0=0。如果i≥2，我们也必须有ui=6 uj代表所有i，j∈i代表i=6 j，因为否则我们通过选取任何非零λ的λi=λ和λj=−λ得到一个非平凡的线性依赖性，并且让λk=0代表所有k∈i代表k=6 i，j。
因此，线性独立的定义意味着一个非平凡的线性独立族实际上是一个集合。这解释了为什么某些作者选择定义向量集的线性独立性。这种方法的问题是线性依赖，即线性独立性的逻辑否定，然后只定义为一组向量。然而，正如我们前面所指出的，对于允许同一向量多次出现的族，定义线性相关性是非常可取的。
例2.4.
1.	R中的任何两个不同的标量λ，μ=06都是线性相关的。
2.	在r3中，向量（1,0,0）、（0,1,0）和（0,0,1）是线性无关的。见图
2.7。

图2.7:r3中红色矢量（1,0,0）、绿色矢量（0,1,0）和蓝色矢量（0,0,1）的视觉（箭头）描述。
3.	在R4中，向量（1,1,1,1）、（0,1,1,1）、（0,0,1,1）和（0,0,0,1）是线性无关的。
4.	在r2中，向量u=（1,1），v=（0,1）和w=（2,3）是线性相关的，因为
W=2U+V。
见图2.8。
当我是有限的，我们经常假设它是集合i=1,2，…，n。在这种情况下，我们将族（ui）i∈i表示为（u1，…，un）。
向量空间的子空间的概念定义如下。
定义2.7.给定一个向量空间e，e的一个子集f是e的一个线性子空间（或子空间），iff f是非空的，且所有u，v∈f，和所有λ，μ∈r的λu+μv∈f。
很容易看出，e的子空间f确实是一个向量空间，因为·：e×e→e到f×f的约束实际上是一个函数·：f×f→f，而·：r×e→e到r×f的约束实际上是一个函数·：r×f→f。
由于子空间f是非空的，如果我们选取任意向量u∈f，如果我们让λ=礹=0，那么λu+礹u=0u+0u=0，那么每个子空间都包含向量0。
以下事实也成立。证据留作练习。

图2.8：粉红色向量u=（1,1）、深紫色向量v=（0,1）和向量和w=2u+v的直观（箭头）描述。
提案2.6.
(1)	向量空间e的任何子空间族（甚至无穷大）的交集都是子空间。
(2)	设f为向量空间e的任意子空间，对于任意非空有限指数集i，ifp（i∈uii）λi∈iuii是向量的任意一个族∈f，ui∈f，（λi）i∈i是标量的任意一个族，那么
子空间0将用（0）表示，甚至用0表示（略带滥用符号）。
例2.5。
1.	在r2中，向量u=（x，y）的集合如下：
X+Y=0
子空间如图2.9所示。
2.	在r3中，一组向量u=（x，y，z），使得
X+Y+Z=0
子空间如图2.10所示。
3.	对于任意n≥0，次数的多项式f（x）∈r[x]集至多n是r[x]的子空间。

图2.9：子空间x+y=0是通过坡度为-1的原点的直线。它包含形式为λ（−1,1）的所有向量。

图2.10：子空间x+y+z=0是穿过原点的平面，且为法向（1,1,1）。4。上三角n×n矩阵集是n×n矩阵空间的一个子空间。
提案2.7.对于任何向量空间e，如果s是e的任何非空子集，则包含s的e的最小子空间hsi（或跨度）是s元素的所有（有限）线性组合的集合。
证据。我们证明了S元素的所有线性组合的集跨度是E的一个子空间，作为练习，验证了包含S的每个子空间也包含跨度。
首先，跨度是非空的，因为它包含s（非空）。如果u=pi iλiui
γ
而v=pj∈jμjvj是跨度（s）中任意两个线性组合，对于任意两个标量λ，μ∈r，
λu+μv=λxλiui+μxμjvj
i∈i j∈j
=xλλiui+x祄祄jvj
i∈i j∈j
=xλi ui+x（λi+祄祄）ui+x祄祄祄jvj，
i∈i−j i∈i j∈j−i
它是指数集i j的线性组合，因此λu+μv∈SPAN（s），证明SPAN（s）是一个子空间。
有人可能会想，如果我们在组成线性组合的系数中添加额外的条件，会发生什么。这里有三个很重要的自然约束（通常我们假设我们的索引集是有限的）：（1）考虑组合pi∈iλiui
.
这些被称为仿射组合。我们应该认识到每一个线性组合
pin II∈，如果我们把λiui看作仿射组合。例如，如果j=i k，uk=0，且λk=1−pλi，那么pj∈jkλ是一个指数，notjuj是一个仿射
我爱我
组合和
十倍
λiui=λjuj.
i∈i j∈j
然而，我们得到了新的空间。例如，在r3中，三个向量e1=（1,0,0）、e2=（0,1,0）和e3=（0,0,1）的所有仿射组合的集合是通过这三个点的平面。因为它不包含0=（0,0,0），所以它不是线性子空间。
（2）考虑组合pi∈iλiui，其中
λi≥0，对于所有i∈i。
这些被称为正（或圆锥）组合。结果表明，向量族的正组合是圆锥体。它们自然地出现在凸优化中。（3）考虑我们需要（1）和（2）的组合pi∈iλiui，即
，且所有i∈i的λi≥0。
这些被称为凸组合。对于任何有限的向量族，这些向量的所有凸组合的集合都是凸多面体。凸多面体在凸优化中起着非常重要的作用。
注：线性组合的概念也可以定义为无穷指数集i，为了保证和pi∈iλiui的意义，我们将注意力限制在有限支持族上。
定义2.8.对于任意的K域，如果对于i的某个有限子集j，所有i的λi=0，则一个标量族（λi）i∈i具有有限支持。
（由于有限线性组合可能是无限的）家族式yif（λi）i∈i是有限支持的标量家族，对于任何向量空间（ui）i∈i pof向量sj∈jλjuju，其中i∈e，我们定义线性组合j是ei的任何有限子集，这样在kp上，对于任意i∈λiλ=0iui
我
一般来说，有限族的结果也适用于有限支撑族。
2.5向量空间的基
给定一个向量空间e，给定一个族（v i）i∈i，由零向量0和（vi）i∈i的所有线性组合组成的e的子集v很容易被看作是e的一个子空间。如果不是多余的话。具有这样一个“高效”生成族（称为基）的子空间起着重要作用，并激发了以下定义。
定义2.9.在给定向量空间e和e的子空间v的情况下，向量v i∈v的族（vi）i∈i跨v或对每个v∈v生成v iff，在
R是这样的
V=xλivi.
我爱我
我们还说，（v i）i∈i的元素是v的生成元，v的范围是（vi）i∈i，或者由（vi）i∈i生成。如果e的子空间v是由有限族（vi）i∈i生成的，我们说v是有限生成的。跨越V且线性无关的族（ui）i∈i称为V的基。
例2.6.
1.	在r3中，如图2.9所示的向量（1,0,0）、（0,1,0）和（0,0,1）构成了一个基。
2.	矢量（1，1，1，1），（1，1，−1，−1），（1，−1，0，0），（0，0，1，−1）构成了称为HAAR基的R4的基。这一基础及其对维数2n的推广在小波理论中是至关重要的。
3.	在次数最多为n的r[x]多项式的子空间中，多项式1、x、x2、…、xn构成一个基。
4.	伯恩斯坦多项式也构成了这个空间的基础。这些多项式在样条曲线理论中起着重要作用。

线性代数的第一个关键结果是每个向量空间e都有一个基。我们从一个重要的引理开始，它使逐步构建基础的机制正式化。
引理2.8。给定一个向量空间E元素的线性独立族（ui）i∈i，如果v∈e不是（ui）i∈i的线性组合，则将v添加到族（ui）i∈i中得到的族（ui）i∈i∮k（v）是线性独立的（其中k/∈i）。
证明：μ有一个逆（因为μv+pr是一个场），因此对于任何族（λv i）=i∈i∈i∈i（μ−1λi）ru，我们都有∈iλiui=0。如果i，表明μ=06，那么v是（pλiui=0）的线性组合，并且自族以来i∈i与该假设相矛盾。因此，（ui）i∈i是线性无关的，我们有μ=0。但是，λi=0，我们有i∈i代表所有i∈i。
下一个定理一般成立，但对于没有有限生成集的向量空间，证明更为复杂。因此，在本章中，我们只证明有限生成向量空间的定理。
定理2.9。给定任意有限族s=（ui）i∈i生成向量空间e和任意线性无关子族l=（uj）j∈j（其中j i），e有一个基b，使得l b s。
证据。考虑线性独立族B的集合，使L B S。由于该集合是非空的和有限的，因此它有一些极大的元素（即，具有最大基数的H I的S的子族B=（uh）H∈H），说B=（uh）H∈H。我们声称B生成E。实际上，如果B不生成e，那么有一些上∈s，它不是b中向量的线性组合（因为s生成e），带有p/∈h。然后通过引理2.8，族b0=（uh）h∈h p是线性独立的，并且由于l b b0 s，这与b的最大性相矛盾。因此，b是e的一个基础，这就是T L B S.
注：定理2.9也适用于非有限生成的向量空间。在这种情况下，问题是要保证最大线性独立族B的存在，从而使L B S。这种最大族的存在可以用Zorn的引理表示；见lang[41]（定理5.1）。
需要定理2.9的完全一般性的情况是向量的情况。

系数q上的空间r。数字1和√2是线性无关的。

在q上，根据定理2.9，线性独立族L=（1，√2）可以扩展到r的基b。因为r不可数，q可数，所以这样的基必须不可数！
基的概念也可以用极大线性独立族和极小生成族的概念来定义。
定义2.10.假设（vi）i∈i是向量空间e中的向量族，我们说（vi）i∈i是e的最大线性独立族，如果它是线性独立的，并且如果对于任何向量w∈e，通过将w添加到族（vi）i∈i得到的族（vi）i∈i∮k w是线性相关的。我们认为（vi）i∈i是e的极小生成族，如果它跨越e，并且对于任何指数p∈i，通过从族（vi）i∈i中删除vp得到的族（vi）i∈i−p不跨越e。
下面给出了表征基的有用性质的命题是引理2.8的直接结果。
提案2.10.给定一个向量空间e，对于e的向量的任何族b=（vi）i∈i，下列性质是等价的：
(1)	B是E的基础。
(2)	B是E的最大线性独立族。
(3)	B是E的最小生成族。
证据。我们首先证明（1）和（2）的等价性。假设（1）。因为B是基，所以它是一个线性独立的族。我们认为B是一个最大线性独立族。如果b不是最大线性无关族，则存在一个向量w∈e，使得通过将w加到b得到的b0族是线性无关的。然而，由于b是e的基础，向量w可以表示为b中向量的线性组合，这与b0是线性无关的事实相矛盾。
相反，假设（2）。我们认为b跨e，如果b不跨e，那么在b中有一个向量w∈e，它不是向量的线性组合，通过引理2.8，把w加到b得到的b0族是线性无关的。由于b是b0的一个合适的亚科，这与b是最大线性独立族的假设相矛盾。因此，b必须跨越e，因为b也是线性无关的，所以它是e的基础。
现在我们将证明（1）和（3）的等价性。再次假设（1）。因为B是基，所以它是E的生成族，我们认为B是最小生成族。如果b不是最小生成族，那么b的一个合适的子族b0跨越e，那么每个w∈b−b0都可以表示为b0的向量的线性组合，这与b是线性独立的这一事实相矛盾。
相反，假设（3）。我们声称b是线性无关的。如果b不是线性独立的，那么一些向量w∈b可以表示为b0=b−w中向量的线性组合。由于b产生e，b0族也产生e，但b0是b的一个适当的亚科，与b的最小值相矛盾，因为b跨越e，是线性独立的，所以它是e的基础。
线性代数的第二个关键结果是，对于向量空间e的任意两个基（ui）i∈i和（vj）j∈j，索引集i和j具有相同的基数。特别地，如果e有n个元素的有限基，e的每个基都有n个元素，整数n称为向量空间e的维数。
为了证明第二个关键结果，我们可以使用下面的因steinitz而替换的引理。这一结果显示了向量空间有限线性独立族和有限生成族之间的关系。我们从引理的一个版本开始，这个版本有点非正式，但比命题2.12中给出的更精确和更正式的公式更容易理解。技术上的困难与一些指数需要重新命名的事实有关。
提案2.11.（替换引理，版本1）给定向量空间e，让（u1，…，um）是e中的任何有限线性独立族，让（v1，…，vn）是任何有限族，这样每个ui都是（v1，…，vn）的线性组合。那么我们必须使m≤n，并且用（u1，…，um）替换向量vj的m，这样在重命名vj的一些索引之后，族（u1，…，um，vm+1，…，vn）和（v1，…，vn）生成e的相同子空间。
证据。我们对m进行归纳，当m=0时，这个家族（u1，…，um）是空的，这个命题的意义很小。对于诱导步骤，我们有一个线性独立的家族（U1，…，Um，Um+1）。考虑线性独立族（u1，…，um）。根据诱导假设，m≤n，向量vj的m替换为（u1，…，um），这样在重命名了vs的一些指数后，家族（u1，…，um，vm+1，…，vn）和（v1，…，vn）生成了e的相同子空间。向量um+1也可以表示为一个线性组合。（v1，…，vn）和（u1，…，um，vm+1，…，vn）的组合产生了相同的子空间，因此，可以将um+1表示为（u1，…，um，vm+1，…，vn）的线性组合，例如
.
我们认为，对于一些m+1≤j≤n的j，λj=06，这意味着m+1≤n。否则，我们将
，
用户界面的一种非平凡线性依赖关系，这是不可能的，因为（u1，…，um+1）是线性无关的。
因此，m+1≤n，在必要时重新命名指数后，我们可以假定λm+1=06，因此我们得到
.
观察族（u1，…，um，vm+1，…，vn）和（u1，…，um+1，vm+2，…，vn）生成相同的子空间，因为um+1是（u1，…，um，vm+1，…，vn）的线性组合，vm+1是（u1，…，um+1，vm+2，…，vn）的线性组合。由于（u1，…，um，vm+1，…，vn）和（v1，…，vn）生成了相同的子空间，我们得出（u1，…，um+1，vm+2，…，vn）和（v1，…，vn）生成了相同的子空间，从而得出了诱导假设的结论。
下面是一个例子，说明了替代引理。考虑序列（u1、u2、u3）和（v1、v2、v3、v4、v5），其中（u1、u2、u3）是线性独立的族，uis用vjs表示如下：
U1=v4+v5 u2=v3+v4−v5 u3=v1+v2+v3。
从我们得到的第一个方程
v4=u1−v5，
通过代入第二个方程
u2=v3+v4−v5=v3+u1−v5−v5=u1+v3−2v5。
从上面的方程我们得到
v3=−u1+u2+2v5，
如此
u3=v1+v2+v3=v1+v2−u1+u2+2v5。
最后，我们得到
v1=u1−u2+u3−v2−2v5
所以我们有
v1=u1−u2+u3−v2−2v5 v3=−u1+u2+2v5 v4=u1−v5，
这表明（u1、u2、u3、v2、v5）与（v1、v2、v3、v4、v5）跨越相同的子空间。向量（v1、v3、v4）已被（u1、u2、u3）替换，剩余的向量为（v2、v5）。我们可以重命名它们（v4、v5）。
为了完整性起见，这里是替换引理（及其证明）的更正式的声明。
提案2.12。（替换引理，第2版）给定一个向量空间e，让（ui）i∈i是e中的任何有限线性独立族，其中i=m，让（vj）j∈j是任何有限族，这样每个ui都是（vj）j∈j的线性组合，其中j=n。然后存在一个集合l和一个注入ρ：l→j。（一个重新标号函数），使得l i（vρ（l））l l和（v j）j j产生相同的子空间。特别是m≤n。
证据。我们从i=m开始归纳，当m=0时，族（ui）i∈i是空的，并且命题与l=j（ρ是同一性）具有平凡的关系。假设i=m+1。考虑线性独立族（ui）i∈（i−p），其中p是i的任何成员。根据归纳假设，存在一个集合l和一个注入ρ：l→j，这样l（i−p）=∅，l=n−m，并且族（ui）i∈（i−p）（vρ（l））l∈l和（vj）j∈j生成相同的e的子空间。如果p∈l，我们可以用（l−p）p0替换l，其中p0不属于i l，用与l−p上的ρ一致的注射剂ρ0替换ρ，从而使ρ0（p0）=ρ（p）。因此，我们可以一直假设l i=∅。由于up是（v j）j∈j与族（ui）i∈（i−p）（vρ（l））l∈l与（vj）j∈j的线性组合生成e的相同子空间，up是（ui）i∈（i−p）（vρ（l））l∈l的线性组合。
上=xλiui+xλlvρ（l）。（1）
I∈（I−P）L∈L
如果所有l∈l的λl=0，我们有
，
与（ui）i∈i是线性无关这一事实相矛盾。因此，对于一些l∈l，λl=06，假设l=q。由于λq=06，我们得到
（2）
我们声称家族（ui）i    \123; \\\ l，by（1），vρ（q）是（ui）i∈i（vρ（l））l∈（l−q），by（2）的线性组合。因此，族（ui）i（vρ（l））l（l  123; \\ \123; \125;，（v j）j ；L−Q=N−（M+1）
其思想是，矢量vj的m可以用线性无关的uis替换，这样就可以生成相同的子空间。函数ρ：l→j的目的是选取j的n−m元素j1，…，jn−m，并将它们重新标记为l1，…，ln−m，这样这些新索引就不会与i中的索引冲突；这样，将“生存”的向量vj1，…，vjn−m重新标记为vl1，…，vln-m，其他m向量vj与j∈j−j1，…，jn−m替换为ui。这个新家族的索引集是I L。
事实上，我们可以证明，当向量空间有限生成时，命题2.12隐含定理2.9。把定理2.9和2.12放在一起，我们得到以下基本定理。
定理2.13。设e为有限生成的向量空间。任何族（ui）i∈i生成e都包含一个作为e基础的子族（uj）j∈j，任何线性独立族（ui）i∈i都可以推广到一个作为e基础的族（uj）j∈j（带有i j）。此外，对于e的每两个基（ui）i∈i和（vj）j∈j，对于某个固定整数n≥0，我们得到了i=j=n。
证据。第一部分紧接着应用定理2.9，其中l=∅和s=
（ui）i∈i.第二部分，考虑族S0=（ui）i∈i（vh）h∈h，其中（vh）h∈h是生成e的任意有限生成族，且具有i h∅。然后将定理2.9应用于l=（ui）i∈i和S0。对于最后一个陈述，假设（ui）i∈i和（vj）j∈j是e的基，因为（ui）i∈i是线性独立的，（vj）j∈j跨越e，命题2.12意味着i≤j。对称参数产生j≤i。
注：定理2.13也适用于非有限生成的向量空间。
定义2.11.当一个向量空间e不是有限生成时，我们说e是无限维的。有限生成向量空间e的维数是其所有基的公共维数n，用dim（e）表示。
显然，如果把r域本身看作一个向量空间，那么a∈r和a=06的每个族（a）都是基。因此，dim（r）=1。注意dim（0）=0。
定义2.12.如果e是尺寸n≥1的向量空间，对于e的任何子空间u，如果dim（u）=1，则u称为直线；如果dim（u）=2，则u称为平面；如果dim（u）=n-1，则u称为超平面。如果dim（u）=k，那么u有时被称为k平面。
设（ui）i∈i为向量空间e的基，对于任意向量v∈e，由于族（ui）i∈i生成e，在r中有一个标量的族（λi）i∈i，这样
.
一个非常重要的事实是家族（λi）i∈i是唯一的。
命题2.14.假设v=给定向量空间pi∈iλiui。那么家族，让（ui）（iλ∈ii）ibe一个向量家族，在∈i的标量中，这样ve。let=piv∈∈λieu，i
i是唯一的iff（ui）i∈i是线性独立的。
证据。首先，假设（ui）i∈i是线性无关的。如果（μi）i∈i是r中的另一个标量家族，使得v=pi∈i礽iui，那么我们有
，
由于（ui）i∈i是线性无关的，我们必须使所有i∈i的λi−μi=0，也就是说，所有i∈i的λi=μi。相反的是矛盾。如果（ui）i∈i是线性相关的，则会有一个scalars的族（祆i∈i，而不是全部为空，因此


2.6。一些j∈i的矩阵和μj=06。但是，
，
自λiu礹i.j=06以来，对于λj=6λj+p礹j，与（λi）i∈i是唯一族的假设相矛盾，使得v=i∈i
定义2.13.如果（i）i i i是向量空间E的一个基，对于任何向量v* e，如果（Xi）i i是R中的唯一标量族，则
V=xxiui，
我爱我
每个XI被称为V的索引I的分量（或坐标）相对于基（UI）i i。
2.6矩阵
在第2.1节中，我们非正式地介绍了矩阵的概念。在本节中，我们将精确地定义矩阵，并介绍一些关于矩阵的操作。结果表明，矩阵形成了一个向量空间，该空间配备了一个具有关联性但非交换性的乘法运算。我们将在第3.1节中解释矩阵如何用于表示下一节中定义的线性映射。
≤≤≤≤
以k表示的标量，用数组表示	
γ
A11 A12…
A21 A22……………
γ
γ
AM1 AM2…	A1N A2N
…。
AMN
定义2.14.如果k=r或k=c，k上的m×n矩阵是一个族（a i j），1 i m，1 j n
在m=1的特殊情况下，我们有一个行向量，用表示
（A11···A1n）
在n=1的特殊情况下，我们有一个列向量，用
.
在最后两种情况下，我们通常省略常量索引1（行的第一个索引，列的第二个索引）。所有m×n矩阵的集合用mm、n（k）或mm、n表示。n×n矩阵称为n维数的平方矩阵。n维数的所有平方矩阵的集合用mn（k）或mn表示。
注：根据定义，矩阵a=（a i j）1≤i≤m，1≤j≤n是一个族，即从1,2，…，m×1,2，…，n到k的函数。因此，没有理由对指数进行排序。因此，通过对行或列采用不同的顺序，矩阵A可以用许多不同的方式表示为一个数组。然而，习惯上（并且通常方便）假定集合1,2，…，m和1,2，…，n的自然顺序，并根据行和列的顺序将表示为数组。我们在矩阵上定义了一些操作，如下所示。
定义2.15.给定两个m×n矩阵a=（aij）和b=（bij），我们将它们的和a+b定义为矩阵c=（cij），这样cij=aij+bij；也就是说，
γ
全部
A21
……
γ
γ
AM1	A12 A22
…
AM2	…
……
…	A1N A2N
…
AMN	B11
B21
+…
 
 
骨形态发生蛋白1	B12…B1N B22…B2N
………BM2…BMN			
					γ
A11+B11
A21+B21
=……
γ
γ
AM1+BM1	A12+B12 A22+B22
…
AM2+BM2	…
……
…	A1N+B1N_
A2N+B2N_
…。AMN+BMN
对于任何矩阵a=（aij），我们让−a作为矩阵（−aij）。给定一个标量λ∈k，我们将矩阵λa定义为矩阵c=（cij），这样cij=λaij；即
.
给定m×n矩阵a=（aik）和n×p矩阵b=（bkj），我们将它们的乘积ab定义为m×p矩阵c=（cij），以便
，
对于1≤i≤m和1≤j≤p，产品ab=c如下所示
γ
全部
A21
……
γ
γ
AM1	A12 A22
…
小精灵	…
……
…	A1N A2N
…
AMN	γ
B11
B21…
γ
γ
BN1	B12 B22型
…
BN2	…
……
…	b1p c11 b2p c21
…=…
BNP CM1公司	C12和C22
…
CM2	…
……
…	c1p c2p
…，
化学机械抛光
注意，通过矩阵a和b相乘得到的矩阵ab的索引i和j的条目可以用第i行对应的行矩阵的乘积来标识。
2.6。A的矩阵与B的J列对应的列矩阵：
.
定义2.16.在维度n中，对角线上包含1，其他地方包含0的平方矩阵称为单位矩阵。它由表示
γ
一
次级方案0
在=…
γ
γ
零	零
一
…
零	…
……
…	0℃
0℃
__
一
定义2.17.给定m×n矩阵a=（a i j），其转置a>=（a>j i）是n×m矩阵，因此a>j i=aij，对于所有i，1≤i≤m，以及所有j，1≤j≤n。
矩阵A的转置有时用at表示，甚至用ta表示。请注意，矩阵A的转置A>具有以下特性：A>的第j行是A的第j列。换句话说，转置交换矩阵的行和列。下面是一个例子。如果a是5×6矩阵
1
7 A=8
γ
9
十	二
一
七
八
九	三
二
一
七
八	四
三
二
一
七	5 6 6
4 5 5
3 4_
2 3_
1 2
那么A>是6×5矩阵	七
一
二
三
四
五	八
七
一
二
三
四	九
八
七
一
二
三	10℃
9℃
8 7。
1 2
下面的观察将在稍后讨论SVD时有用。给定任意m×n矩阵a和任意n×p矩阵b，如果我们用a1，…，an表示a的列，用b1，…，bn表示b的行，那么我们得到
ab=a1b1+·····+anbn。
对于每一个尺寸为n的正方形矩阵a，立即验证ain=ina=a。
定义2.18。对于尺寸n的任何正方形矩阵a，如果存在a b=ba=in的矩阵b，则它是唯一的，称为a的逆矩阵。矩阵b也由a-1表示。可逆矩阵也称为非奇异矩阵，不可逆矩阵称为奇异矩阵。
利用命题2.19和矩阵表示线性映射的事实，可以证明，如果一个正方形矩阵A有一个左逆矩阵，即矩阵B，使得b a=i，或右逆矩阵，即矩阵C，使得a c=i，那么a实际上是可逆的；因此b=a−1和c=a−1。这些事实也来源于5.11号提案。
立即证明m×n矩阵的集合mm，n（k）是矩阵加上和矩阵乘上标量的向量空间。
定义2.19.m×n-矩阵eij=（ehk）的定义是，如果h=6 i或k=6 j，eij=1，ehk=0；换句话说，（i，j）-项等于1，所有其他项均为0。
以下是m=2和n=3的EIJ矩阵：
.
很明显，每个矩阵a=（aij）∈mm，n（k）都可以用一种独特的方式写成
.
因此，族（eij）1≤i≤m，1≤j≤n是向量空间mm，n（k）的基础，其尺寸为mn。
注：当k是一个（交换）环而不是场时，定义2.14和定义2.15也是完全合理的。在这个更一般的设置中，向量空间的框架太窄，但是我们可以考虑交换环a上满足定义2.4的所有公理的结构。这种结构称为模块。模理论比向量空间更为复杂。例如，模块并不总是有基础的，而向量空间的其他属性对于模块来说通常是失败的。当一个模块有基础时，它被称为自由模块。例如，当a是交换环时，结构an是一个模，使得（ei）i=1的矢量ei和（ei）j=0（j=6i）构成a的基。向量空间的许多性质仍然适用于。因此，AN是一个自由模块。例如，当a是交换环时，m m，n（a）是基（ei，j）1≤i≤m，1≤j≤n的自由模。交换环上的多项式也形成无限维的自由模。
命题2.15中列出的性质很容易得到验证，尽管有些计算有点繁琐。命题3.1给出了一个更具概念性的证明。

提案2.15。（1）给定任意矩阵a∈mm，n（k），b∈mn，p（k），c∈mp，q（k），我们得到
（ab）c=a（bc）；
也就是说，矩阵乘法是关联的。
（2）给定任意矩阵a，b∈mm，n（k）和c，d∈mn，p（k），对于所有的λ∈k，我们得到
（A+B）C=AC+BC
A（C+D）=AC+AD
（λa）c=λ（ac）
A（λc）=λ（ac）
使矩阵乘法·：mm，n（k）×mn，p（k）→mm，p（k）为双线性。
命题2.15的性质以及所有平方n×n矩阵的a in=in a=a的事实表明，mn（k）是一个单位在（事实上，是一个结合代数）中的环。这是一个具有零除数的非交换环，如下面的示例所示。例2.7。例如，假设a，b是2×2矩阵
然后
，
和
因此a b=6b a，ab=0，即使a，b=0.6
2.7线性图
既然我们了解了向量空间以及如何生成它们，我们希望能够将一个向量空间e转换为另一个向量空间f。保持向量空间结构的两个向量空间之间的函数称为向量空间的同态，或线性映射。线性映射使函数的线性概念形式化。
记住，线性映射是空间的变换，通常比空间本身更重要。
在本节的其余部分中，我们假定所有向量空间都是实向量空间，但所有结果都适用于任意场上的向量空间。
定义2.20。给定两个向量空间e和f，e和f之间的线性映射是满足以下两个条件的函数f:e→f：
f（x+y）=f（x）+f（y）表示所有x，y∈e；
f（λx）=λf（x）表示所有的λ∈r，x∈e。
在第一个恒等式中设置x=y=0，我们得到f（0）=0。线性映射的基本性质是将线性组合转换为线性组合。给定e中向量的任意有限族（ui）i∈i，给定r中标量的任意族（λi）i∈i，我们得到
.
利用定义2.20的属性，通过i上的归纳显示上述身份。
例2.8。
1.	图f:r2→r2定义如下：

是一个线性映射。读者应通过以下方式检查旋转的构成

π/4，放大率√2。
2.	对于任何向量空间e，标识映射id:e→e由
id（u）=u表示所有u∈e
是一个线性映射。当我们想要更精确的时候，我们写的是IDE而不是ID。
3.	地图D:R[X]→R[X]定义如下：
d（f（x））=f0（x），
其中，f0（x）是多项式f（x）的导数，是线性映射。
4.	地图Φ：c（[a，b]）→r由

其中c（[a，b]）是在区间[a，b]上定义的一组连续函数，是一个线性映射。
5.	函数h−、−i:c（[a，b]）×c（[a，b]）→r由

在每个变量f，g中都是线性的。它还满足hf，gi=hg，fi和hf的性质，fi=0 iff=0。它是一个内部产品的例子。
定义2.21。对于线性映射f:e→f，我们将其图像（或范围）imf=f（e）定义为集合
imf=y∈f（x∈e）（y=f（x）），
其内核（或空空间）kerf=f−1（0），作为集合
切口=x∈e f（x）=0。
例2.8（3）中的导数映射d:r[x]→r[x]的核是常数多项式，因此kerd=r。如果我们考虑二阶导数d d:r[x]→r[x]，则d d的核由度≤1的所有多项式组成。n d:r[x]→r[x]的图像实际上是r[x]本身，因为每个多项式p（x）=a0x+······+an−1x+an的次n是n+1的多项式q（x）的导数，由

另一方面，如果我们考虑d对次数≤n的多项式的向量空间r[x]n的限制，则d的核仍然是r，但d的图像是r[x]n-1，次数≤n-1的多项式的向量空间。
提案2.16。给定线性映射f:e→f，集imf是f的子空间，集kerf是e的子空间。线性映射f:e→f是内射iff kerf=（0）（其中（0）是平凡子空间0）。
证据。对于任何x，y∈imf，有一些u，v∈e，这样x=f（u）和y=f（v），并且对于所有的λ，μ∈r，我们有
F（λu+μv）=λf（u）+μf（v）=λx+μy，
因此，λx+μy∈imf，表明imf是f的一个子空间，给定任意x，y∈kerf，我们得到f（x）=0和f（y）=0，因此，
F（λx+μy）=λf（x）+μf（y）=0，
也就是说，λx+μy∈切口，表明切口是e的一个子空间。
首先，假设切口=（0）。我们需要证明f（x）=f（y）意味着x=y。然而，如果f（x）=f（y），那么f（x）−f（y）=0，通过f的线性，我们得到f（x−y）=0。因为切口=（0），我们必须有x-y=0，也就是x=y，所以f是内射的。相反，假设f是内射的。如果x∈切口，即f（x）=0，因为f（0）=0，我们得到f（x）=f（0），通过注入率，x=0，这证明切口=（0）。因此，f是注射剂iff kerf=（0）。
由于命题2.16，线性映射f的图像imf是f的子空间，我们可以将f的秩rk（f）定义为imf的维数。
定义2.22.对于线性映射f:e→f，f的秩Rk（f）是f的图像imf的维数。
向量空间中的基的一个基本性质是，它们允许将线性映射定义为唯一的同态扩展，如下面的命题所示。
提案2.17。给定任意两个向量空间e和f，给定e的任何基（ui）i∈i，给定f中的任何其他向量族（vi）i∈i，存在一个唯一的线性映射f:e→f，使得f（ui）=vi对于所有i∈i。此外，f是内射iff（vi）i∈i是线性独立的，f是外射iff（vi）i∈i生成f。
证据。如果存在这样一个线性映射f:e→f，由于（ui）i∈i是e的基础，因此每个向量x∈e都可以唯一地作为线性组合写入。
x=xxiui，
我爱我
根据线性度，我们必须
f（x）=xxif（ui）=xxivi.
I∈I I∈I
定义函数f:e→f，方法是
f（x）=xxivi
我爱我
每x=pi∈i xiui。很容易验证f确实是线性的，根据前面的推理它是唯一的，显然，f（ui）=vi。
现在假设f是内射的。设（λi）i∈i为标量的任何族，并假定
X
λivi=0.
我爱我
因为每个i∈i的vi=f（ui），我们有
f（xλiui）=xλ，如果（ui）=xλivi=0。
i∈i i∈i i∈i
既然f是注射剂iff kerf=（0），我们有
，
由于（ui）i∈i是一个基，我们得到所有i∈i的λi=0，这表明（vi）i∈i是线性的独立的。相反，假设（e，每个向量x∈e是一个线性组合vi）i∈i是线性独立的。因为（x=pi∈iλi ui of（ui）i∈i.如果ui）i∈i是一个基础
f（x）=f（xλiui）=0，
我爱我
然后
xxx
λivi=λif（ui）=f（λiui）=0，
i∈i i∈i i∈i
所有i∈i的λi=0，因为（vi）i∈i是线性无关的，这意味着x=0。因此，切口=（0），这意味着f是内射的。其中f是主观性的部分作为一个简单的练习。
图2.11给出了当e=r3和v=r2时2.17号提案的说明。

图2.11：给定u1=（1,0,0），u2=（0,1,0），u3=（0,0,1）和v1=（1,1），v2=-1,1），v3=（1,0），定义唯一线性映射f:r3→r2 x f（u1）=v1，f（u2）=v2，和f（u3）=v3。由于f（u1−u2）=f（u1）−f（u2）=（1,1）−（−1,1）=（2,0）=2f（u3）=f（2u3），因此此图是推测的，但不是内射的。
在命题2.17的第二部分，一个内射线性映射f:e→f发送一个基
（ui）i∈i到f的线性独立族（f（ui））i∈i，这也是f为双目标时的基础。当e和f具有相同的有限维n时，（ui）i∈i是e的基，f:e→f是内射的，（f（ui））i∈i是f的基（由命题2.10）。下面的简单命题也很有用。
提案2.18。给定任意两个向量空间e和f，其中f非平凡，给定e中向量的任意族（ui）i∈i，则以下性质成立：
(1)	族（ui）i∈i在f中为每个向量族（vi）i∈i生成e iff，其中至多有一个线性映射f:e→f，这样f（ui）=vi代表所有i∈i。
(2)	族（ui）i∈i是线性独立的i f f，对于每个向量族（vi）i∈i，在f中有一些线性映射f:e→f，这样f（ui）=vi代表所有i∈i。
证据。（1）如果有任何线性映射f:e→f，使得f（ui）=vi对于所有i∈i，因为（ui）i∈i生成e，每个向量x∈e都可以写成某种线性组合。
x=xxiui，
我爱我
根据线性度，我们必须
f（x）=xxif（ui）=xxivi.
I∈I I∈I
这表明f是唯一的，如果它存在的话。相反，假设（ui）i∈i不生成e，因为f是非平凡的，所以有一些向量y∈f，使得y=06。由于（ui）i∈i不生成e，在（ui）i∈i生成的子空间中有一个不存在的向量w∈e，根据定理2.13，在（ui）i∈i生成相同子空间时，存在一个线性独立的子族（ui）i∈i0。由于假设w∈e不在（ui）i∈i0、引理2.8和定理2.13生成的子空间中，又有e的一个基（e j）j∈i0 j，使得ei=ui代表所有i∈i0，w=e j0代表一些j0∈j，让（vi）i∈i代表f中的族，这样vi=0代表所有i∈i，defining f:e→f是一个常数线性映射，其值为0，我们有一个线性映射，使f（ui）=0表示所有i∈i。根据命题2.17，有一个唯一的线性映射，g:e→f表示g（w）=y，而g（e j）=0表示所有j∈（i0 j）−j0。根据e的基（e j）j i0 j的定义，对于所有i i，我们都有g（ui）=0，并且由于f 6=g，这与这样的映射最多只有一个这一事实相矛盾。见图2.12。
（2）如果族（ui）i∈i是线性独立的，那么根据定理2.13，（ui）i∈i可以推广到e的基，其结论由命题2.17得出。相反，假设（ui）i∈i是线性相关的。然后有一个标量（不是全部为零）的族（λi）i∈i，这样
X
λiui=0.
我爱我
假设任意非零向量y∈f，对于每一个i∈i，都有一个线性映射fi:e→f，这样fi（ui）=y，fi（uj）=0，对于j∈i−i。然后我们会得到
0=fi（xλiui）=xλifi（ui）=λiy，
I∈I I∈I
由于y=06，这意味着每一个i∈i的λi=0，因此，（ui）i∈i是线性无关的。
在给定向量空间e、f和g以及线性映射f:e→f和g:f→g的情况下，很容易证明f和g的组合g f:e→g是线性映射。


图2.12：设e=r3，f=r2。矢量u1=（1,0,0），u2=（0,1,0）不生成r3，因为零映射和映射g（其中g（0,0,1）=（1,0）都将桃xy平面发送到原点。
定义2.23。线性映射f:e→f是同构的，如果存在线性映射g:f→e，那么
G F=IDE和F G=IDF。（）
定义2.23中的图G是唯一的。这是因为如果g和h都满足g_f=ide、f_g=idf、h_f=ide和f_h=idf，那么
g=g idf=g（f h）=（g f）h=ide h=h。
上面满足（）的图G称为n f的倒数，它也用f-1表示。
观察命题2.17表明，如果f=r，那么我们得到了维度j=n和rn的任何向量空间e之间的同构。命题2.17还表明，如果e和f是两个向量空间，（ui）i∈i是e的基础，f:e→f是一个线性映射，它是
一个同构，那么这个族（可以证明如果f:e→ff（uis是一个双目标线性映射，那么它的逆i））i∈i是f.f−1:f→e的基础，作为一个函数，也是一个线性映射，因此f是一个同构。命题2.17的另一个有用推论是：
提案2.19。设e为有限维n≥1的向量空间，设f:e→e为任意线性映射。以下属性保留：
(1)	如果f有一个左逆g，也就是说，如果g是一个线性映射，这样g f=id，那么f是同构的，f−1=g。
(2)	如果f有一个右逆h，也就是说，如果h是一个线性映射，这样f h=id，那么f是同构，f−1=h。
证据。（1）方程g f=id表示f是内射的；这是关于函数的标准结果（如果f（x）=f（y），那么g（f（x））=g（f（y）），这意味着自g f=id以来x=y）。假设（u1，…，un）是e的任何基。根据命题2.17，因为f是内射的，（f（u1），…，f（un））是线性独立的，并且由于e有维n，所以它是e的基（如果（f（u1），…，f（un））不跨越e，那么它可以严格地扩展到维的基大于n，这与OREM 2.13）。然后F是双射的，根据先前的观测，它的逆是一个线性图。我们也有
G=G ID=G（F F−1）=（G F）F−1=ID F−1=F−1。
(2)	方程f h=id表示f是可射的；这是关于函数的标准结果（对于任何y∈e，我们有f（h（y））=y）。假设（u1，…，un）是e的任何基础。根据命题2.17，因为f是主观性的，（f（u1），…，f（un））跨越e，并且因为e有维n，所以它是e的基础（如果（f（u1），…，f（un））不是线性独立的，那么因为它跨越e，它包含的维的基础严格小于n，矛盾ng定理2.13）。然后F是双射的，根据先前的观测，它的逆是一个线性图。我们也有
H=ID H=（F−1 F）H=F−1（F H）=F−1 ID=F−1。
这就完成了证明。
定义2.24.两个向量空间e和f之间的所有线性映射集都用hom（e，f）或l（e；f）表示（符号l（e；f）通常保留给连续线性映射集，其中e和f是赋范向量空间）。当我们想要更精确地定义向量空间e和f的K域时，我们写homk（e，f）。
集合hom（e，f）是在示例2.3中定义的操作下的向量空间，即
（f+g）（x）=f（x）+g（x）
对于所有x∈e，和
（λf）（x）=λf（x）
对于所有x∈e，值得仔细检查的一点是，λf确实是一个线性映射，它使用了在k域中的交换性（通常，k=r或k=c）。事实上，我们有
（λf）（μx）=λf（μx）=λμf（x）=λf（x）=μ（λf）（x）。
当e和f有有限维时，向量空间hom（e，f）也有有限维，稍后我们将看到。

2.8。线性形式与对偶空间
定义2.25。当e=f时，线性映射f:e→e也被称为自同态。空间hom（e，e）也用end（e）表示。
同样重要的是要注意的是，组成赋予了HOM（e，e）一个环结构。实际上，组合是一个操作：hom（e，e）×hom（e，e）→hom（e，e），它是关联的，具有标识ide，并且分布性属性保持：
（g1+g2）f=g1 f+g2 f；g（f1+f2）=g f1+g f2。
环hom（e，e）是非交换环的一个例子。
很容易看出，f:e→e的双射线性映射集是一个组合下的群。
定义2.26.双射线性映射f:e→e也称为自同构。e的自同构群称为一般线性群（e），用gl（e）或aut（e）表示，当e=r n时，用gl（n，r）表示，甚至用gl（n）表示。
2.8线性形式和对偶空间
我们已经观察到场k本身（k=r或k=c）是一个向量空间（在其自身之上）。从E到K场的线性映射的向量空间hom（e，k），即线性形式，起着特殊的作用。在这一部分中，我们只定义线性形式，并证明每个有限维向量空间都有一个对偶基。第10章给出了对偶空间和对偶性的更高级的表示。
定义2.27。对于向量空间e，从e到场k的线性映射的向量空间hom（e，k）称为e的对偶空间（或对偶空间）。空间hom（e，k）也用e表示，e中的线性映射称为线性形式，或covector。空间e的双空间e称为e的双空间。
记法上，线性形式f:e→k也用星号表示，如u、x等。
如果e是有限维n的向量空间，并且（u1，…，un）是e的基础，对于任何线性形式f∈e，对于每个x=x1u1+······+xnun∈e，通过线性我们得到

当λi=f（ui）k为每i，1≤i≤n时，因此，对于基（u1，…，un），线性形式f由行向量表示。
（λ1···λn）
我们有
，
x坐标的线性组合，我们可以把线性形式f看作一个线性方程。如果我们决定使用系数的列向量

而不是行向量，则线性形式f定义为
f（x）=c>x。
上面的符号通常用于机器学习。
例2.9.给定任意可微函数f:rn→rn，根据定义，对于任意x∈rn，f在x处的总导数dfx是线性形式dfx:r→r，因此对于所有u=（u1，…，un）∈rn，
.
例2.10。设c（[0,1]）为连续函数f[0,1]→r的向量空间，映射i:c（[0,1]）→r由
对于任意f∈c（[0,1]）
是线性形式（积分）。
例2.11。考虑实n×n矩阵的向量空间mn（r）。设tr:mn（r）→r为tr（a）=a11+a22+·····+ann给出的函数，
称为A的迹线。它是一种线性形式。设为：mn（r）→r为
，
其中a=（aij）。立即证明S是线性形式。
2.8。线性形式与对偶空间
给定一个向量空间e和任意基（u i）i∈i for e，我们可以将一个线性形式u i∈e与每个ui关联，并且u i具有一些显著的性质。
定义2.28。给定一个向量空间e和任意基（u i）i∈i for e，通过命题2.17，对于每个i∈i，都有一个唯一的线性形式u i，这样
，
对于每一个j∈i，线性形式u i称为索引i的坐标形式w.r.t.的基础
（ui）i∈i。
注：对于指数集i，作者通常定义所谓的“克罗内克符号”δij，以便
J J，
对于所有i，j∈i，那么，u i（uj）=δij。
术语坐标形式的原因如下：如果e有有限维，如果（u1，…，un）是e的基础，对于任何向量。
V=λ1u1+····+λnun，
我们有
u i（v）=u i（λ1u1+····+λnun）
=λ1u i（u1）+····+λiu i（ui）+···+λnu i（un）=λi，
因为u i（uj）=δij。因此，u i是一个线性函数，它返回在基上表示的向量的第i个坐标（u1，…，un）。
下面的定理表明，在有限维中，向量空间e的每一个基（u1，…，un）都产生了对偶空间e的基（），称为对偶基。
定理2.20。（双基的存在）设e为维数n的向量空间，其性质如下：对于e的每一个基（u1，…，un），坐标形式族是e的基（称为（u1，…，un）的双基）。证据。（a）如果v∈e是任何线性形式，考虑线性形式
.
注意这是因为，
f（ui）=（v（u1）u 1+·····+v（u n）u（ui）
=v（u1）u 1（u i）+····+v（ui）u i（ui）+····+v（u n）u n（ui）
=v（ui）
因此F和V_在基础上（U1，…，Un）达成一致，这意味着
.
因此，（）跨度e。我们声称这些弯曲器是线性独立的。如果不是，我们有一个非平凡的线性依赖
，
如果我们将上述线性形式应用到每个用户界面，使用一个族计算，我们得到
，
证明这确实是线性无关的。因此，（）是
E.
特别是，定理2.20给出了一个有限维向量空间，它的对偶E具有相同的维数。
2.9总结
本章的主要概念和结果如下：
•	向量空间的概念。
•	病媒家族。
•	向量的线性组合；向量族的线性依赖性和线性独立性。
•	线性子空间。
•	生成（或生成）族；生成器，有限生成的子空间；子空间的基础。
•	每个线性独立的族都可以扩展到一个基（定理2.9）。
•	向量B族是一个基本的iff，它是一个极大的线性独立的家族iff，它是一个极小的生成家族（命题2.10）。
•	替代引理（建议2.12）。
•	有限生成向量空间e中任意两个基的元素数目相同；这是e的维数（定理2.13）。
•	超平面。

•	每一个向量在一个基上都有一个唯一的表示（以坐标表示）。
•	矩阵
•	列向量，行向量。
•	矩阵运算：加法、标量乘法、乘法。
•	k域上m×n矩阵的向量空间mm，n（k）；k域上n×n矩阵的环mn（k）。
•	线性映射的概念。
•	线性映射f的图像imf（或范围）。
•	线性映射f的核切口（或空空间）。
•	线性映射f的秩Rk（f）。
•	线性映射的图像和核心是子空间。线性映射是内射的，如果它的核心是平凡空间（0）（命题2.16）。
•	关于基的线性映射的唯一同态延拓性质（命题2.17）。
•	线性映射的向量空间homk（e，f）。
•	线性形式（covector）和双空间e。
•	坐标形式。
•	双基的存在（有限维）。
2.10问题
问题2.1。设h为3×3上三角矩阵的集合，由
.
(1)	用矩阵乘法的二元运算证明h是一个群，显式地求h中每个矩阵的逆。h是交换的吗？
(2)	给定两个组g1和g2，回忆一个同态，如果一个函数_：g1→g2，使得_（a b）=（a）（b），a，b∈g1。
证明_（e1）=e2（其中ei是gi的同一元素），以及
⑨（a−1）=（⑨（a））−1，a∈g1。
(3)	设s1为单位圆，即
s1=eiθ=cosθ+isinθ0≤θ<2π，
并设_为下式给出的函数
.
证明了ω是g=r×r×s1上的一个射函数，如果我们定义了
在这个集合上乘以
（x1，y1，u1）·（x2，y2，u2）=（x1+x2，y1+y2，eix1y2u1u2）
那么G是一个群，而_是从H到G的群同态。
(4)	一个同态的核，定义为：g1→g2
Ker（_）=a∈g1 _（a）=e2。
显式地求出_的核，表明它是H的一个子群。
问题2.2.对于m>0的任何m∈z，子集mz=m k k∈z是z的一个阿贝尔子群。检查这个。
(1)	给出从mz到z的群同构（可逆同态）。
(2)	检查由i（mk）=mk给出的包含图i:mz→z是否为群同态。证明如果m≥2，则没有群同态p:z→mz，这样p i=id。
注：上述结果表明，阿贝尔群不具备向量空间的某些性质。稍后我们将显示满足条件p i=id的线性映射始终存在。
问题2.3。设e=r×r，定义加法运算
（x1，y1）+（x2，y2）=（x1+x2，y1，+y2），x1，x2，y1，y2∈r，
乘法运算·：r×e→e by
λ·（x，y）=（λx，y），λ，x，y∈r.
证明e与上述运算+和·不是向量空间。哪些公理被违反了？
问题2.4.（1）证明向量空间的公理意味着
α·0=0
0·v=0α·（−v）=−（α·v）（−α）·v=−（α·v），
对于所有v∈e和所有α∈k，其中e是k上的向量空间。
(2)	对于每个λ∈r和每个x=（x1，…，xn）∈r，定义λx
λx=λ（x1，…，xn）=（λx1，…，λxn）。
回想一下，每个向量x=（x1，…，xn）∈rn可以唯一地写为
x=x1e1+·····+xnen，
式中，ei=（0，…，0,1,0，…，0），位置i中只有一个1。对于任何操作·：r×rn→r，如果·满足向量空间的公理（v1），则证明对于任何α∈r，我们有
α·x=α·（x1e1+····+xnen）=α·（x1e1）+····+α·（xnen）。
结论·······································
(3)	使用（2）定义满足公理（v1–v3）但公理v4失败的操作·：r×rn→rn。
(4)	对于任何操作·：r×rn→rn，证明如果···········································
r·x=r（1·x）。
在上述方程中，1·x是一个向量（y1，…，yn）∈rn不一定等于x=
（x1，…，xn）和r（1·x）=（ry1，…，ryn）
如第（2）部分所述。
利用（4）得出结论，满足公理（v1-v3）n的任何操作·：q×rn→rn完全由1对e1，…，en所跨越的r的一维子空间的作用决定。
问题2.5。设A1为下列矩阵：
.
证明A1的柱是线性无关的。在由A1列向量组成的基础上找到向量X的坐标=（6,2、-7）。
问题2.6.设a2为下列矩阵：
.
将A2的第四列表示为A2前三列的线性组合。向量x=（7,14、−1,2）是A2列的线性组合吗？
问题2.7。设a3为下列矩阵：
.
证明A1的柱是线性无关的。在由列向量a3组成的基础上，求出向量x的坐标=（6,9,14）。
问题2.8。设A4为下列矩阵：
.
证明A4列是线性无关的。在A4列向量组成的基础上，找到向量x的坐标=（7,14、-1,2）。问题2.9.考虑下面的haar矩阵
.
证明H的柱是线性无关的。暗示。计算产品h>h。
问题2.10。考虑下面的Hadamard矩阵
.
证明了H4的色谱柱是线性无关的。
暗示。计算产品。
问题2.11.在解决这个问题时，不要使用行列式。
(1)	让（u1，…，um）和（v1，…，vm）是某个向量空间e中的两个向量族。假设每个vi都是uj的线性组合，因此
vi=ai1u1+······+aimum，1≤i≤m，
矩阵a=（a i j）是一个上三角矩阵，这意味着如果1≤j<i≤m，那么aij=0。证明如果（u1，…，um）是线性无关的，如果a的所有对角线项都是非零的，那么（v1，…，vm）也是线性无关的。
暗示。在M上使用感应。
(2)	设a=（aij）为上三角矩阵。证明如果a的所有对角线项都不为零，则a是可逆的，a的逆a−1也是上三角形。
暗示。在M上使用感应。
证明如果a是可逆的，那么a的所有对角线项都是非零的。
(3)	证明了如果族（u1，…，um）和（v1，…，vm）与（1）相关，那么（u1，…，um）是线性无关的，iff（v1，…，vm）是线性无关的。
问题2.12。在解决这个问题时，不要使用行列式。考虑n×n
矩阵							
	γ
一
次级方案0
γ
0 A=…
γ
γ
次级方案0
γ
次级方案0
γ
零	二
一
零
…
零
零
零	0 2
一
…
…
…
…	零
零
二
…
零
零
零	…
…
……
一
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
(1)	求线性系统的解x=（x1，…，xn）
ax=b，
对于
.
(2)	证明矩阵A是可逆的，并求其逆矩阵A−1。假设宇宙中的原子数估计为≤1082，比较系数的大小，如果n≥300，a与1082的倒数。
(3)	假设b受到少量∆b的扰动（注意∆b是一个矢量）。找到系统的新解决方案
A（X+∆X）=B+∆B，
其中∆x也是一个矢量。如果b=（0，…，0,1）和∆），则表明
②
（其中（∆x）1是∆x的第一个分量）。
(4)	证明（a−i）n=0。
问题2.13。如果存在一个r≥1的整数，那么n×n矩阵n是幂零的，因此nr=0。
(1)	证明如果n是幂零矩阵，那么矩阵i−n是可逆的，并且
（i−n）−1=i+n+n2+····+nr−1。
(2)	使用（1）计算下列矩阵A的逆矩阵：
1 2 3 4 5_
0 1 2 3 4_
A=0 0 1 2 3。
	
0 0 1 2_
0 0 0 0 1
问题2.14。（1）设A为N×N矩阵。如果a是可逆的，证明对于任何x∈rn，如果ax=0，那么x=0。
（2）设A为m×n矩阵，设B为n×m矩阵。证明im−ab是可逆的，如果在−banis中是可逆的。
暗示。如果对于所有x∈r，mx=0意味着x=0，那么m是可逆的。
问题2.15。考虑以下n×n矩阵，对于n≥3：
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
网络错误
(1)	如果我们用b1，…，bn表示b的列，证明
（n−3）b1−（b2+·····+bn）=2（n−2）e1 b1−b2=2（e1+e2）b1−b3=2（e1+e3）……
b1−bn=2（e1+en）
其中e1，…，en是rn的标准基向量。
(2)	证明b是可逆的，其逆a=（aij）由下式给出

和

(3)	证明了n个对角n×n矩阵di的定义是，di的对角项等于b的第i列的项（从上到下）构成n×n对角矩阵空间的基础（除对角线上可能外，到处都是零的矩阵）。例如，当n=4时，我们有
 	网络错误
网络错误
网络错误
网络错误	 	 	网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误	网络错误
 	网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误
网络错误	 	网络错误
网络错误
网络错误
网络错误	网络错误
网络错误
网络错误	网络错误
问题2.16。给定任意m×n矩阵a和任意n×p矩阵b，如果我们用a1，…，a表示a的列，用b1，…，bn表示b的行，证明
ab=a1b1+·····+anbn。
问题2.17。让f:e→f是一个线性映射，它也是一个双射（它是内射和外射的）。证明反函数f−1:f→e是线性的。
问题2.18。在给定两个向量空间e和f的情况下，设（ui）i∈i为e的任意基，设（vi）i∈i为f中的任意向量族，证明了唯一线性映射f:e→f，使f（ui）=vi为所有i∈i的主观性iff（vi）i∈i跨越f。
问题2.19。设f:e→f为Dim（e）=n，Dim（f）=m的线性映射，证明f的秩为1，iff用该形式的m×n矩阵表示。
A=紫外线>
用u表示维数m的非零列向量，v表示维数n的非零列向量。
问题2.20。找出线性形式_（x，y，z）=2x−y+3z，_（x，y，z）=3x−5y+z，_（x，y，z）=4x−7y+z之间的非平凡线性相关性。
问题2.21。证明线性形式_（x，y，z）=x+2y+z，_（x，y，z）=2x+3y+3z，_（x，y，z）=3x+7y+z
线性无关。将线性形式（x，y，z）=x+y+z表示为垂直1，垂直2，垂直3的线性组合。
