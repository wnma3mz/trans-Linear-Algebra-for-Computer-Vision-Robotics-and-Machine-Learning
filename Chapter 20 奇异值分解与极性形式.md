第二十章

# 奇异值分解与极性形式

## 20.1 f f的性质

在本节中，我们假设我们处理的是真正的欧几里得空间。设f:e→e为任意线性映射。一般来说，F不可能对角化。我们证明了如果我们愿意使用两个正交基，每个线性映射都可以对角化。这是著名的奇异值分解（SVD）。SVD的近亲是线性映射的极性形式，它显示了如何将线性映射分解为其纯旋转组件（可能带有翻转）和纯拉伸部分。关键的观察是f f自

h（f f）（u），v i=hf（u），f（v）i=hu，（f f）（v）i.

事实上

同样，事实上，这些f feigen值都是非负的是自伴的。f f fandandff ff是自伴的非常重要，因为根据定理可以对角化并且它们具有真正的特征值。如下面的命题所示。

16.8，它意味着f

提案20.1.f f和f f的特征值为非负。证据。如果u是特征值λ的f f的特征向量，那么

h（f_f）（u），u i=hf（u），f（u）i

h（f_f）（u），ui=λhu，ui，

因此，λhu，u i=hf（u），f（u）i，

这意味着λ≥0，因为h−，−i是正定的。类似的证据也适用于F F。

六百四十一

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image002.gif)

因此，上述考虑的特征值也适用于任何线性映射f f.f f的形式为f:或0，其中→：ff→在两个欧几里得式σi>之间为0f，类似地是唯一的

空格（E，H−、−I1）和（F，H−、−I2）。回忆一下伴随的f线性映射f这样

hf（u），vi2=hu，f（v）i1，对于所有u∈e和所有v∈f。

则f f和f f为自伴（证明与前一种情况相同），f f和f f的特征值为非负。

证据。如果λ是f f的特征值，而u（6=0）是对应的特征向量，我们得到

h（f_f）（u），ui1=hf（u），f（u）i2，

以及h（f_f）（u），ui1=λhu，ui1，

所以

λhu，ui1，=hf（u），f（u）i2，

这意味着λ≥0。类似的证据也适用于F F。

这种情况甚至更好，因为我们很快就会发现f f和f f具有相同的非零特征值。

注：任意两个线性映射f:e→f和g:f→e，其中dim（e）=n和dim（f）=m

λm det（λin−g f）=λn det（λim−f g），

因此，g f和f g总是具有相同的非零特征值；参见问题14.14。

定义的特征值20.1.f给定任何线性mapf（和f f）被取消：e→奇异值关闭，平方根sf。σi>0为正

定义20.2.称为正半定自伴线性映射（或正），iff:ef→也是可逆的，其特征值为非负的e称为正定。在后一种情况下，f的每个特征值都是严格正的。

如果f:e→f是任意线性映射，我们只证明f f和f f是半正定自伴线性映射。这一事实的显著结果是，每个线性映射都有两个重要的分解：

\1.    极地形态。

\2.    奇异值分解（SVD）。


 

20.1。f f的性质

奇异值分解的美妙之处在于，存在两个正交基（u1，…，un）和（v1，…，vm），因此，对于这些基，f是由奇异值f或0组成的对角矩阵。因此，在某种意义上，F总是可以相对于两个正交基对角化。SVD也是解决最小二乘意义上的超定线性系统和数据分析的一个有用工具，如我们稍后所示。

首先，我们展示了内核与f、f_、f_和f_f_图像之间的一些有用关系。回想一下，如果f:e→f是一个线性映射，f的图像imf是f的子空间f（e），f的秩是其图像的维数dim（imf）。还记得（定理5.8）dim（切口）+dim（imf）=dim（e），

对于e的每个子空间w（命题11.11和13.13），则

dim（w）+dim（w）=dim（e）。

提案20.2.给定任意两个欧几里得空间e和f，其中e有维数n，f有维数m，对于任何线性映射f:e→f，我们有

切口=KER（F F）

切口=KER（F F）

切口=（imf），

kerf=（imf），dim（imf）=dim（imf），

F、F、F F和F F具有相同的等级。

证据。为了简化表示法，我们将用相同的符号H−、−I（避免下标）来表示e和f上的内积。如果f（u）=0，那么（f（f）（u）=f（f（u））=f（0）=0，那么切口ker（f f）。根据F的定义，我们有

h f（u），f（u）i=h（f f）（u），用户界面

对于所有的u∈e，如果（f f）（u）=0，因为h−−i是正定的，我们必须有f（u）=0，所以ker（f f）kerf。因此，

切口=KER（F F）。

切口=KER（F F）的证据相似。

根据F的定义，我们有

hf（u），v i=hu，f（v）i表示所有u e和所有v f.（）

这立刻意味着

切口=（imf）和切口=（imf）。

让我们解释一下为什么kerf=（imf），这是另一个等式相似的证明。因为内积是正定的，对于每一个u∈e，我们有

•     u∈切口

•     iff f（u）=0

•     i f f hf（u），v i=0代表所有v，•by（）iff hu，f（v）i=0代表所有v，

•     iff u∈（imf）。

自从

dim（imf）=n−dim（切口）

和dim（imf）=n（imf），

从

切口=（imf）

我们还有dim（kerf）=dim（imf），

我们从中获得

dim（imf）=dim（imf）。

因为dim（ker（f f））+dim（im（f f））=dim（e），

ker（f f）=kerf和kerf=（imf），我们得到

dim（（im f））+dim（im（f f））=dim（e）。

因为dim（（imf））+dim（imf）=dim（e），

我们推导出dim（im f）=dim（im（f f））。

类似的证据表明

dim（im f）=dim（im（f_f）。

因此，F、F、F F和F F具有相同的等级。

20.2。方阵的奇异值分解

## 20.2平方矩阵的奇异值分解

现在我们将证明每个平方矩阵都有一个SVD。如果我们先考虑极性形式，然后从中导出SVD（极性分解具有唯一性），则可以得到更强有力的结果。就我们的目的而言，唯一性结果并没有那么重要，所以我们满足于存在结果，其证明更简单。读者对更普遍的治疗感兴趣，请参考加利尔[25]。

史都华[61]在一篇引人入胜的论文中描述了奇异值分解的早期历史。SVD独立于贝尔特拉米和卡米尔·乔丹（18731874）。高斯是所有这些的祖父，因为他在最小二乘（18091823）上的工作（但勒让德也发表了一篇关于最小二乘的论文！）然后是西尔维斯特、施密特和赫尔曼·韦尔。西尔维斯特的工作显然是“不透明的”，他给出了一种计算方法来寻找SVD。施密特的工作实际上与积分方程和对称和不对称内核有关（1907年）。韦尔的工作与微扰理论（1912）有关。Autonne提出了极地分解（19021915）。Eckart和Young将SVD扩展到了矩形矩阵（1936、1939）。

定理20.3。（奇异值分解）对于每个实n×n矩阵a，有两个正交矩阵u和v和一个对角矩阵d，其中a=v du>，其中d是

| 网络错误                                                     |                     |                     |                                           |
| ------------------------------------------------------------ | ------------------- | ------------------- | ----------------------------------------- |
| 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误 | 网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误 |

式中，σ1，…，σr是f的奇异值，即a>a和aa>的非零特征值的（正）平方根，以及σr+1=·····=σn=0。u列是a>a的特征向量，v列是aa>的特征向量。

证据。由于a>a是对称矩阵，实际上是半正定矩阵，因此存在一个正交矩阵u，使得

a>a=ud2u>，

d=diag（σ1，…，σr，0，…，0），其中a>a的非零特征值，其中r是a的秩；即，σ1，…，σr是a的奇异值，其结果如下：

u>a>au=（au）>au=d2，

如果我们让fj是j=1，…，n的au的jth列，那么我们有

hfi，fji=σi2δi j，1≤i，j≤r

和

fj=0，r+1≤j≤n。

如果我们定义（v1，…，vr）

Vj=σj−1fj，1≤j≤r，

然后我们有了

hvi，vji=δi j，1≤i，j≤r，

因此，将（v1，…，vr）完全转换为正态基（v1，…，vr，vr+1，…，vn）（例如，使用gram-schmidt）。既然fj=σjvj，对于j=1…，r，我们有

hvi，fji=σjhvi，vji=σjδi，j，1≤i≤n，1≤j≤r

既然j=r+1时fj=0，…，n，

hvi，fji=0 1≤i≤n，r+1≤j≤n。

如果v是列为v1，…，vn的矩阵，则v是正交的，上述方程证明

v>au=d，

根据需要，得出a=v du>。

方程式a=v du>意味着

a>a=ud2u>，aa>=v d2v>，

这表明A>A和AA>具有相同的特征值，U列是A>A的特征向量，V列是AA>的特征向量。

例20.1。下面是一个简单的例子，说明如何使用定理20.3的证明来获得SVD分解。让。然后，和

. 简单计算表明，a>a的特征值为2和0，以及

对于特征值2，单位特征向量为，而单位特征向量为

. 观察奇异值为σ1=√2和σ2=0。此外，

. 为了确定v，定理20.3的证明告诉我们首先

计算

然后设置

.

20.2。方阵的奇异值分解

一旦确定了v1，因为σ2=0，我们就可以自由地选择v2，这样（v1，v2）就形成了r2的正交基。当然，我们选择和设置。当然，我们可以通过直接计算aa>的特征值和特征向量找到v。我们把它留给读者检查一下

.

定理20.3给出了以下定义。

定义20.3.一种三重矩阵（u，d，v），其中a=v d u>，其中u和v是正交的，d是一个项为非负（正半定）的对角矩阵，称为a的奇异值分解（svd）。

用于计算矩阵a的svd a=v d u>的matlab命令是[v，d，u]

=SVD（A）。

定理20.3的证明表明，有两个正交基（u1，…，un）和（v1，…，vn），其中（u1，…，un）是a>a的特征向量，（v1，…，vn）是aa>的特征向量。此外，（u1，…，ur）是ima>的正态基础，（ur+1，…，un）是kera的正态基础，（v1，…，vr）是ima的正态基础，（vr+1，…，vn）是kera>的正态基础。

用第三章的注释，如果我们用u1，…，un表示u的列，用v1，…，vn表示v的列，那么我们可以写

.

因此，如果r比n小很多（我们写的），我们可以看到a可以用更少的元素从u和v重建。这个想法将被用来提供矩阵的“低阶”近似值。我们的想法是，对于一些σk+1，…σr非常小的情况，只保留k的顶部奇异值。

评论：

(1)    在Strang[64]中，矩阵u、v、d用u=q2、v=q1和d=∑表示，SVD写为。这具有q1在q2之前的优势。

. 这有一个缺点，即A映射了q2列（特征向量

a>a）到q1列的倍数（aa>的特征向量）。

(2)    实际计算矩阵SVD的算法在Golub和van Loan[30]、Demmel[16]和Trefethen和Bau[68]中给出，在这里，SVD及其应用也得到了广泛讨论。

(3)    如果A是一个对称矩阵，那么一般来说，在V=U的情况下，A的SVD V∑U>是不存在的，但是，如果A是半正定的，那么A的特征值是非负的，因此A的非零特征值等于A的奇异值，A的SVD的形式是

*A*    =V∑V>。

(4)    SVD也适用于复杂矩阵。在这种情况下，对于每个复杂的n×n矩阵

有两个单位矩阵u和v和一个对角矩阵d，这样

*A*    =v d u，

式中，d是由实数项σ1，…，σn组成的对角矩阵，其中，σ1，…，σr是a的奇异值，即a a和aa的非零特征值的正平方根，以及σr+1=。=σn=0。

## 20.3方阵的极性形式

与SVD密切相关的概念是矩阵的极性形式。

定义20.4.具有r正交和s对称半正定的a=rs的对（r，s）称为a的极分解。

定理20.3表明，对于每个实n×n矩阵a，都有一些正交矩阵

r和一些半正定对称矩阵s，这样

A=卢比。

这很容易展示，我们将在下面证明。此外，如果a是可逆的，r，s是唯一的，但这很难证明；见问题20.9。例如，矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image004.gif)

是正交和对称的，A=r s，R=a和S=i，这意味着A的一些特征值是负的。

注：在复杂情况下，极分解表明，对于每一个复杂的n×n矩阵a，都有一些幺正矩阵u和一些半正定厄米特矩阵h，这样

A=呃。

从极性形式到SVD很容易，反之亦然。

给定SVD分解a=v d u>，设r=v u>和s=ud u>。很明显，r是正交的，s是半正定对称的，并且

rs=v u>u d u>=v d u>=a。

20.3。方阵的极性形式

例20.2。从示例20.1中回忆，a=v du>其中v=i2和

.

设置r=v u>=u和

.

因为有特征值√2和0。我们把它留给读者来检查a=rs。

另一方面，给定极分解a=r1 s，其中r1是正交的，s是半正定对称的，有一个正交矩阵r2和一个半正定对角矩阵d，因此

，

其中v=R1r2和u=r2是正交的。

例20.3。Let和a=R1s，其中和s=

. 这是实施例20.2的极性分解。注意

.

设置u=r2并获得实施例20.1的SVD分解。

矩阵的特征值和奇异值通常没有任何明显的联系。例如，n×n矩阵

| 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

具有多重性n的特征值1，但其奇异值，σ1≥········································

| 网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 | 网络错误   网络错误   网络错误   网络错误   网络错误   网络错误 |
| -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
|          |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |                                                              |

=cond2（a）≥2n−1。

如果a是一个复n×n矩阵，a的特征值λ1，…，λn和奇异值σ1≥σ2≥·································

σ12··········································

和

|λ1···λn=Det（a），

所以我们有

|λ1···λn=σ1····σn.

一般来说，赫尔曼·韦尔证明了以下显著定理：

定理20.4.（Weyl's不等式，1949）对于任何复杂的n×n矩阵，a，如果λ1，…，λn∈c是a的特征值和σ1，…，σn∈r+是a的奇异值，列出如下：

|λ1≥······≥λn和σ1≥········≥σn≥0，则

|λ1···λn=σ1·····σn和

|λ1···λk≤σ1······σk，对于k=1，…，n−1。

定理20.4的证明可在Horn和Johnson[37]第3章第3.3节中找到，其中给出了更多关于矩阵特征值和奇异值的不等式。

定理20.3可以很容易地扩展到矩形m×n矩阵，如我们在下一节所示。有关矩形矩阵的SVD的各种版本，请参见Strang[64]Golub和van Loan[30]、Demmel[16]和Trefethen和Bau[68]。

## 20.4矩形矩阵的奇异值分解

这是定理20.3对矩形矩阵的推广。

20.4。矩形矩阵的奇异值分解

| 两个正交矩阵u（n×n）和v（m×m）以及一个对角线m×n矩阵d，使得   |             |         |          |                       |      |
| ------------------------------------------------------------ | ----------- | ------- | -------- | --------------------- | ---- |
| a=v   d u>，其中d是形式                                      |             |         |          |                       |      |
| σ1…γ   σ2…γ   ……………σ1   γ                                                             D=…σn或D=…   0..…0                                  ………………γ   γ   0……0_ | 西格玛2   … | …   ……… | …   西米 | 0…   0…   .   0…   0… | ，   |

定理20.5。（奇异值分解）对于每个实M×N矩阵A，有

其中，σ1，…，σr是f的奇异值，即a>a和aa>的非零特征值的（正）平方根，以及σr+1=。=σp=0，其中p=min（m，n）。u列是a>a的特征向量，v列是aa>的特征向量。

证据。在定理20.3的证明中，由于a>a是对称半正定的，所以存在一个n×n正交矩阵u，使得

A>A=U∑2U>，

当∑=diag（σ1，…，σr，0，…，0），其中是a>a的非零特征值，其中r是a的秩。观察r≤min m，n，au是m×n矩阵。接下来是

u>a>au=（au）>au=∑2，

如果我们让Fj∈Rm为j=1，…，n的au的jth列，那么我们得到

hfi，fji=σi2δi j，1≤i，j≤r

和

fj=0，r+1≤j≤n。

| 如果我们定义（v1，…，vr）  |            |
| -------------------------- | ---------- |
| Vj=σj−1fj，   然后我们有了 | 1≤J≤R，    |
| hvi，vji=δij，             | 1≤i，j≤r， |

因此，将（v1，…，vr）完全转换为正态基（v1，…，vr，vr+1，…，vm）（例如，使用gram-schmidt）。

既然fj=σjvj，对于j=1…，r，我们有

hvi，fji=σjhvi，vji=σjδi，j，1≤i≤m，1≤j≤r

既然j=r+1时fj=0，…，n，我们有

hvi，fji=0 1≤i≤m，r+1≤j≤n。

如果v是列为v1，…，v m的矩阵，那么v是m×m正交矩阵，如果m≥n，我们将

，

否则，如果n≥m，那么我们让

.

无论哪种情况，上述方程都证明了

v>au=d，

根据需要，得出a=v du>。

方程式a=v du>意味着

和

aa>=v dd>v>=v诊断（，

M r

这表明A>A和AA>具有相同的非零特征值，U列是A>A的特征向量，V列是AA>的特征向量。

一种三重（u，d，v），使a=v，d，u>称为a的奇异值分解（svd）。

例20.4。让。然后，和aa>。=

.读者应确认a>a=u∑2u>其中∑和

20.4。矩形矩阵的奇异值分解

. 从那以后，

并通过赋值完成r3的正交基，和。因此

v=i3，读卡器应验证a=v du>，其中。

尽管矩阵d是一个m×n的矩形矩阵，但由于它的唯一非零项是在降对角线上，所以我们仍然认为d是一个对角线矩阵。

用于计算矩阵a的svd a=v du>的matlab命令也是[v，d，

U]=SVD（A）。

如果我们把a看作线性映射f:e→f的表示，其中dim（e）=n和dim（f）=m，定理20.5的证明表明e和f分别有两个正交基（u1，…，un）和（v1，…，vm），其中（u1，…，un）是f f和（v1，…，vm）的特征向量是特征向量。F F的任务大纲。此外，（u1，…，ur）是imf的正态基，（ur+1，…，un）是kerf的正态基，（v1，…，vr）是imf的正态基，（vr+1，…，vm）是kerf的正态基。

矩阵的SVD可用于定义矩形矩阵的伪逆矩阵；我们将在第21章中这样做。读者也可以参考Strang[64]、Demmel[16]、Trefethen和Bau[68]以及Golub和van Loan[30]。

谱定理之一指出对称矩阵可以由正交矩阵对角化。计算对称矩阵A特征值的数值方法有多种，其中一种方法是三对角化A，即存在一些正交矩阵P和一些对称的三对角矩阵T，从而a=p t p>。事实上，这可以通过户主转换来实现；见定理17.2。然后可以使用基于sturm序列的二分法计算t的特征值。也可以使用雅可比方法。有关详细信息，请参见Golub和van Loan[30]、第8章、Demmel[16]、Trefethen和Bau[68]、第26讲、Ciarlet[14]和第17章。计算矩阵A的SVD更为复杂。大多数方法首先找到正交矩阵u和v以及双对角矩阵b，使a=v bu>；参见问题12.8和问题20.3。这也可以通过户主转换来实现。观察b>b为对称三对角。因此，原则上，可以应用先前的对称三对角矩阵对角化方法。但是，显式地计算b>b是不明智的，最后一步使用更精细的方法；可以使用问题20.1的矩阵，见问题20.3。同样，见Golub和van Loan[30]，第8章，Demmel[16]，Trefethen和Bau[68]，第31课。

极性形式在连续介质力学中有应用。实际上，在任何变形中，将拉伸与旋转分开都是很重要的。这正是QS所实现的。正交部分q对应于旋转（可能带有附加反射），对称矩阵s对应于拉伸（或压缩）。S的实际特征值σ1，…，σr是拉伸系数（或压缩系数）（见Marsden和Hughes[47]）。事实上，S可以由一个正交矩阵对角化对应于轴的自然选择，主轴。

SVD应用于数据压缩，例如图像处理。其思想是只保留数量足够大的奇异值。当其他方法如高斯消去产生非常小的支点时，SVD也可以用来确定矩阵的秩。支持向量机的主要应用之一是伪逆的计算。伪逆是求解各种优化问题的关键，尤其是最小二乘法。本主题将在下一章（第21章）中讨论。本章材料的应用可在Strang[64，63]、Ciarlet[14]、Golub和van Loan[30]中找到，其中包含许多其他参考文献；Demmel[16]、Trefethen和Bau[68]。

## 20.5 KY Fan规范和Schatten规范

矩阵的奇异值可以用来定义矩阵上的各种范数，这些范数在量子信息理论和谱图理论中有着最新的应用。根据Horn和Johnson[37]（第3.4节），我们可以做出以下定义：

定义20.5.对于任意矩阵a∈m m，n（c），设q=min m，n，如果σ1≥······································

nk（a）=σ1+·····+σk，

称为A的KY范k-范数。

更一般地说，对于任何p≥1和任何k（1≤k≤q），让

，

称为a的ky fan p-k-norm。当k=q，nq；p也称为schatten p-norm。

注意，当k=1时，n1（a）=σ1，而ky-fan范数n1只是第8章中的谱范数，它是与欧几里得范数相关联的次矩阵范数。当k=q时，Ky扇范数nq由下式给出：

nq（a）=σ1+·····+σq=tr（（a a）1/2）

称为痕迹规范或核规范。当p=2和k=q时，ky fan nq；2范数由下式给出

···我是说，

这是A的Frobenius规范。

可以看出，nk和nk；p是统一不变范数，当m=n时，它们是矩阵范数；见Horn和Johnson[37]（第3.4节，推论3.4.4和问题

3）。

20.6。总结

## 20.6总结

本章的主要概念和结果如下：

•     对于欧几里得空间E上的任何线性映射f:e→e，该映射f f和f f是自伴半定的。

•     线性映射的奇异值。

•     正半定和正定自伴映射。

•     imf、kerf、imf和kerf之间的关系。

•     平方矩阵的奇异值分解定理（定理20.3）。

•     矩阵的SVD。

•     矩阵的极分解。

•     韦尔不等式。

•     m×n矩阵的奇异值分解定理（定理20.5）。

•     KY-Fan k-规范，KY-Fan p-k-规范，Schatten p-规范。

## 20.7问题

问题20.1。（1）设a为实n×n矩阵，并考虑（2n）×（2n）实对称矩阵

.

假设a的秩为r，如果a=v∑u>是a的SVD，用∑=diag（σ1，…，σn）和σ1≥·······················································Nding特征向量。-

暗示。对于k=1，…，n，我们有auk=σk vk。表明，对于k=1，…，r，a>vk=σkuk，而对于k=r+1，…，n，a>vk=0。回想一下，ker（a>）=ker（aa>）。

(2)      证明（1）中s的2n特征向量是成对正交的。检查A是否具有等级R，则S是否具有等级2R。

(3)      假设A是实M×N矩阵，考虑（M+N）×实对称矩阵

.

假设a有秩r，如果a=v∑u>是a的SVD，则证明σk是具有相应特征向量的s的特征值，而−σk是具有相应特征向量的s的特征值。-

找到与特征值0相关的s的剩余m+n−2r特征向量。

(4)      证明了S的M+N特征向量是成对正交的。

问题20.2。设a为秩r的实m×n矩阵，设q=min（m，n）。（1）考虑（m+n）×（m+n）实对称矩阵

![img](file:///C:/Users/ADMINI~1/AppData/Local/Temp/msohtmlclip1/01/clip_image006.gif)

并证明

.

用上述方程证明

det（zim+n−s）=tn−m det（t2im−aa>）。

（2）证明S的特征值为±σ1，…，±σq，加m−n 0。问题20.3。设b为形式的实双对角矩阵

| a1 b1 0_0 a2 b2   γ   B=………   γ   0···0   0 0个···   设A为（2n）×（2n）对称矩阵 | 小精灵   …   …   安1   零 | 0℃   0℃   …。   Bn−1_   安 |
| ------------------------------------------------------------ | ------------------------- | -------------------------- |
|                                                              |                           |                            |

，

设p为p=[e1，en+1，e2，en+2，···，en，e2n]给出的置换矩阵。

| 形状的对角线                                      |                                   |                                 |                                            |                                   |                                |                            |                                        |
| ------------------------------------------------- | --------------------------------- | ------------------------------- | ------------------------------------------ | --------------------------------- | ------------------------------ | -------------------------- | -------------------------------------- |
| γ   零   α1   0   γ   0   T=……   γ   0 0   γ   零 | A1 0   B1   零   …   零   零   零 | 零   b1 0 a2   …   零   零   零 | 0 0 A2   零   …   小精灵   小精灵   小精灵 | 0 0   零   B2   …   安1   零   零 | 0 0   0 0   …   零   BN 1   零 | ·········   ···…   bn−10安 | 0℃   0℃   0_   0_   …。   0_   安   零 |

(1)      证明t=p>ap是一个主零点的对称三对角（2n）×2n矩阵

20.7。问题

(2)      证明了如果Xi是T的特征值Li i的单位特征向量，则Li I＝±Sigi I，其中Sigi I是B的奇异值，并且

，

其中，ui是b>b的单位特征向量，vi是bb>的单位特征向量。问题20.4。找到矩阵的SVD

.

问题20.5。设u，v∈rn为两个非零向量，a=uv>为相应的秩1矩阵。证明了A的非零奇异值是kuk2 kvk2。

问题20.6。设a为n×n实矩阵。证明如果σ1，…，σn是a的奇异值，那么aa>a的奇异值。

问题20.7。设A为实n×n矩阵。

（1）证明a的最大奇异值σ1由下式给出：

，

这个上确界是在x=u1处得到的，在svd a=v∑u>中u的第一列。（2）将上述结果扩展到实M×N矩阵。

问题20.8。设A为实M×N矩阵。证明如果b是a的任何子矩阵（通过保持m≤m行，n≤n列a），则（σ1）b≤（σ1）a（其中（σ1）a是a的最大奇异值，与（σ1）b相似）。

问题20.9。设A为实n×n矩阵。

(1)      假设a是可逆的。证明如果a=q1 s1=q2 s2是a的两个极分解，那么q1=q2，s1=s2。

暗示。，具有s1和s2对称正定。然后使用问题16.7。

(2)      现在假设a是单数。证明如果a=q1 s1=q2 s2是a的两个极分解，那么s1=s2，但q1可能不等于q2。

问题20.10。（1）设A为任意可逆（实）n×n矩阵。证明对于每个SVD，a=v du>a，产品v u>是相同的（即，如果，那么

）v u>与a的极性形式有什么关系？

（2）给定任意可逆（实）n×n矩阵，a，证明存在唯一的正交矩阵q∈o（n），使得ka−qkf最小（在frobenius范数下）。事实上，证明了q=v u>，其中a=v du>是a的一个svd，并且，如果det（a）>0，则表明q∈so（n）。

如果a是单数（即不可逆），你能说什么？

问题20.11。（1）证明对于任意n×n矩阵a和任意正交矩阵q，我们有max tr（qa）q∈o（n）=σ1+······+σn，

其中，σ1≥··············································

（2）通过将上述结果与a=z>x和q=r>一起应用，推导出以下结果：对于任意两个固定的n×k矩阵x和z，集合的最小值

kx−zrkf r∈o（k）

对于任何SVD分解V∑U>=Z>X，通过R=V U>实现。

注：找到一个正交矩阵r，使zr尽可能接近x的问题称为正交procrustes问题；该问题的历史见strang[65]（第4.9节）。