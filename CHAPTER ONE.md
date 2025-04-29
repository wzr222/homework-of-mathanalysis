# Set-Theoretic Notations and Terminology 
union and intersection of $\{A_\alpha\}$ $$\bigcup_{\alpha\in I}A_\alpha=\{x:x\in A_\alpha \text{for at least one } \alpha \in I\}$$$$\bigcap_{\alpha\in I}A_\alpha=\{x:x\in A_\alpha \text{for every one } \alpha \in I\}$$$$A-B=\{x:x\in A,x\not \in B\}$$ $$R^k=R^1\times\cdots\times R^1  \qquad k \text{ factors}$$ 
 $$[a,b]=\{x:a\le x\le b\},(a,b)=\{x:a<x<b\}$$ The symbol$$f:X\to Y$$means that $f$ is a function(or mapping or transformation)of the set $X$ into the set Y;
 $$f(A)=\{y:y=f(x)\text{ for some } x\in A\}$$ $$f^{-1}(B)=\{x:f(x)\in B\}$$ $$(g\circ f)(x)=g(f(x))$$
 ------- 
 
# The Concept of Measurablility
1.   $\varnothing\in\tau \text{ and }X\in\tau$ 
2.  If $V_i\in\tau$ for $i=1,\dots,n$,then $V_1\cap V_2\cap\cdots\cap V_n\in\tau$  
3. If$\{V_\alpha\}$ is an arbitrary collection of members of $\tau$(finite,countable,or uncountable),then$\bigcap_\alpha V_\alpha\in\tau$ .
同样的定义$\sigma-$algebra $(X,\mathfrak{M})$  
- $X\in\mathfrak{M}$ 
- If $A\in\mathfrak{M}$ ,then $A^c\in\mathfrak{M}$ 
- $A_1,\dots\in\mathfrak{M}$ ,$\bigcup_n A_n\in\mathfrak{M}$  （要求指标是可数的)
## continuous function and measurable function 
度量空间是一个拓扑，其中拓扑是由一些列开球的并组成的。
if $x \in B_1\cap B_2,d(x,y_1)<r_1,d(x,y_2)<r_2$ ,我们选取$B=\{y\in X:d(x,y)<\min(r_1-d(y_1,x),r_2,d(y_2,x))\}$  
所以这个$B$是以$x$为圆心的开球，并且$B\subset B_1\cap B_2$ ,所以当$x$取变得时候，我们得到了开球得交集，是可数个开球得并。
在$R^2$的开集是开圆盘的并，在$R$就是$(a,b)$的并。
$f$的点连续定义，$f(W)\in V$ $W$是$x$的一个邻域，然后$V$是$f(x)$的一个邻域。
---- --


如果$f$是可测函数，$g$是连续函数那么，$g\circ f$是可测函数，如果$f$是连续函数，那就是连续函数。这说明连续有保持的性质。按照定义验证。
在平面上的开集可以被可数个长方形开集表示。证明就是开集可以找到一个长方形子集，然后每个点都这样操作，然后长方形子集取一个有理数就可以证明是可数集合。
$u,v$是在$X$上的可测函数，$\Phi$是在$X^2$上的连续函数，那么$\Phi(u,v)$ 是可测函数。
由于前面的定理我们只需要证明$f(x)=(u(x),v(x))$是一个可测函数，那么对$X$的任意一个长方形，我们$f^{-1}(R)=u^{-1}(I_1)\bigcap v^{-1}(I_2)$  然后这是一个可测集合，由于$u,v$是可测函数，把开集映回可测集。对于所有长方形都成立，自然它的并成立。一些推论如下：
1. $f=u+iv$,$u,v$是可测的，$f$就可测。反之也成立.
2. $$ \chi_{E}(x) = \begin{cases} 1 & \text{if } x \in E, \\ 0 & \text{if } x \notin E. \end{cases} $$如果$E$是可测集，那么这个函数是可测函数，很容易证明，如果包含$1$，那么返回来的是$E$,不然返回$\varnothing$这都是可测集合。
 
3. If $f$ is a complex measurable function on $X$,there is a complex measurable function $\alpha$ on $X$ such taht $|\alpha|=1$ ,and $f=\alpha|f|$ 
先证明$E=\{x:f(x)=0\}$是可测集合 ,然后考虑$$
\alpha(x)=\frac{f(x)+\chi_{E}(x)}{|f(x)+\chi_{E}(x)|}$$
证明定义是合理的，然后前面的推论。
 ------------ - 
 
先证明一个定理如果$\mathscr{F}$ is any collection of subsets of $X$,there exists a smallest $\sigma$-algebra $\mathfrak{M}$ in $X$ such that $\mathscr{F}\subset\mathfrak{M}^*$ .这个考虑所有包含$\mathscr{F}$的$\sigma$-algebra，然年取并集，显然这是最小的。然后存在。
## Borel Sets
Let $X$ be a topological space.自然就存在一个$\sigma$-algebra.我们称他的元素为Borel sets of $X$.
所以它具有拓扑和可测共同的性质，所有闭集和开集都是Borel sets.
### Borel mappings or Borel functions
Suppose $\mathfrak{M}$ is a $\sigma$-algebra in $X$, and $Y$ is a topological space.Let$f:X\to Y$ 
- If $\Omega$ is the collection of all sets $E\subset Y$ such that $f^{-1}(E)\in \mathfrak{M}$,then $\Omega$ is a $\sigma$-algebra in Y
- If $f$ is measurable and $E$  is a Borel set in $Y$ , then $f^{-1}(E)\in\mathfrak{M}$ 
- If $Y=[-\infty,\infty]$ and $f ^{-1}((\alpha,\infty])\in\mathfrak{M}$  for every real $\alpha$,then $f$ is measurable.
- Borel mapping 保可测性.
第二个由于$f$可测，所以$\Omega$包含了所有开集。然后又是$\sigma$-algebra因此$\Omega$包含了所有Borel sets.
第三个实际上就是证明$f ^{-1}((-\infty,\alpha))\in\mathfrak{M}$ 对所有$\alpha\in R,\alpha_n<\alpha$ ，since:
$$[-\infty,\alpha)=\bigcup_{n=1}^\infty[-\infty,\alpha_n]=\bigcup_{n=1}^\infty(\alpha_n,\infty]^c$$ 
## $\limsup$ $\liminf$ 
定义就是取一个新数列，然后新数列取后面的最大项，或者最小项。
$$(\sup_n f_n)(x)=\sup_n(f_n(x))$$ 如果$f_n$对每个$n$都可测，那么$g=\sup_{n\ge1}f_n$ $h=\limsup_{n\to\infty}f_n$ 都是可测的。
先证明$g$，注意到$g((\alpha,\infty))=\bigcap_{n\ge1} f_n((\alpha,\infty))$ 。然后:$$
h=\inf_{k\ge1}\{\sup_{i\ge k}f_i\}$$
## 推论
$f,g$可测$\max\{f,g\}$可测。这个也是利用类似的证法，但是我没有看出这个是怎么和上个证明的定理联系在一起的。如果$f_n$收敛的话，也可以收敛到一个可测函数，这是直接推论，因为收敛的话，$\sup,\inf$就都在一起了。
特别的和$f^+=\max\{f,0\}$ 类似的，$f^-$ 。如果$f=g-h,g\ge0,h\ge0$,那么$f^+\le g,f^-\le h$ 

 ------------------------------------------------ 
 # Simple Functions
 简单来说是只在地方取有限值。$$
 s=\sum_{i=1}^n\alpha_i\chi_{A_i}$$
 下面这个定理我觉得有点难理解。或者说现在想不到，这也是我准备记笔记的原因。
 如果$f:X\to[0,\infty]$是一个可测函数，那么存在一个单调递增并且一致收敛到$f$的简单函数列。
 证明：我尽量讲清楚把,Put $\delta_n=2^{-n}$ ,for each real number t corresponds a unique integer k that satisfies $k\delta_n\le t<(k+1)\delta_n$ ,这里也可以看出$k=\lfloor \frac{t}{\delta_n}\rfloor$  ,Define:
 $$\phi_n(t)=\begin{cases}k_n\delta_n\quad &\text{if }0\le t<n\\
 n    \qquad&\text{if }n\le t\le\infty\end{cases}$$
 $$t-\delta_n<\phi_n(t)\le t$$ $$s_n=\phi_n\circ f$$
 其中验证单调性需要利用$[m/n]\le[m]/n$  。我觉得首先这个函数要依靠$f$，但是单调性不好说，然后我们要对任意一个点进行逼近。这是一个技术活，我想不到。

------
# Elementary Properties of Measures
- A positive measure is a function $\mu$,defined on a $\sigma$-algebra $\mathfrak{M}$,whose range is in $[0,\infty]$  and which is countably additive.$\{A_i\}$ 是一系列交集非空的可数可测集合。$$\mu(\bigcup_{i=1}^\infty A_i)=\sum_{i=1}^\infty\mu(A_i)$$
- 一个测度空间是一个正测度函数外加上$\sigma$代数
- A complex measure is a complex-valued countably additive function defined on a $\sigma$-algebra.
一些性质。
- 空集的测度为0
- 有限非空可测集合的并的测度等于可测集合的测度之和
- 测度有保序性
- $\mu(A_n)\to\mu(A)$ as $n\to \infty$ if $A=\bigcup_{n=1}^\infty A_n$,$A_n\in\mathfrak{M}$,$$A_1\subset A_2\subset A_3\subset\cdots.$$
- $\mu(A_n)\to\mu(A)$ as $n\to \infty$ if $A=\bigcap_{n=1}^\infty A_n$,$A_n\in\mathfrak{M}$,and $\mu(A_1)$  is finite.$$A_1\supset A_2\supset A_3\supset\cdots.$$
前面几个都是可以直接看出来的。我们证明倒数第二个，剩下一个是对偶命题类似的。我想到一个动机了，首先要利用性质，只能把它拆成都是disjoint的集合，那么就是
$$ B_n=A_{n}-A_{n-1}$$ $$\bigcup_{k=1}^n B_n=\bigcup_{k=1}^n A_{n}-A_{n-1}=A_{n}-A_0=A_n$$ 好像也是很平凡，之前属于我自己看不清楚题目。
对偶命题不限定$\mu(A_1)$有限的反例，$A_n=\{n,n+1,n+1,\dots\}$ ,$\bigcap A_n=\varnothing$ ,但是$\mu(A_n)=\infty$ 
## A Comment on Terminology
大概就是这些符号使用按照逻辑上说是臃肿的，但是我们还是使用它，这是因为我们保持数学使用习惯。
>This sort of tacit convention is used throughout mathematics. Most mathe matical systems are sets with some class of distinguished subsets or some binary operations or some relations (which are required to have certain properties), and one can list these and then describe the system as an ordered pair, triple, etc., depending on what is needed. For instance, the real line may be described as a quadruple$(R^1, +, \cdot, <)$, where +,$\cdot$ , and $<$ satisfy the axioms of a complete archimedean ordered field. But it is a safe bet that very few mathematicians think of the real field as an ordered quadruple.

-----
# Arithmetic in $[0,\infty]$ 
Let us define $a+\infty=\infty+a=\infty$if $0\le a\le \infty$,and$$
a\cdot\infty=\infty\cdot a=\begin{cases}\infty\quad &\text{if }0<a\le\infty\\
0\quad&\text{if } a=0;\end{cases}$$ 然后消去律需要修改，如果有正无穷的话无法成立。

---------------------
# Integration of Positive Functions
If $s:X\to[0,\infty)$ is a measurable simple function of the form$$
 s=\sum_{i=1}^n\alpha_i\chi_{A_i}$$
 where $\alpha_1,\dots,\alpha_n$ are the distinct values of s ,and if $E\in\mathfrak{M}$,we define$$\int_E s \ d\mu=\sum_{i=1}^n\alpha_i\mu({A_i\cap E})$$ If $f:X\to[0,\infty]$ is measurable,and $E\in\mathfrak{M}$,we define
 $$\int_E f\ d\mu=\sup\int_E s\ d\mu$$
 一些结论，但是比较熟知，但是我们这是一个新的定义:
 1. $0\le f\le g$, then $\int_E f\ d\mu\le\int_E f\ d\mu$ 
 2. If $A\subset B$ and $f\le 0$,then$\int_A f\ d\mu\le\int_B f\ d\mu$ 
 3. 具有线性，齐次性，极限的性质推论
 4. If $f(x)=0$ or $\mu(E)=0$ ，都可以推出积分为0，尽管另外一个无限大
 5. 我们可以用特征函数把一个区域放大到任意区域。
Let $s$ and $t$ be nonnegative measurable simple functions on $X$.For $E\in\mathfrak{M}$,define
$$\phi(E)=\int_E s\ d\mu$$ Then $\varphi$ is a measure on $\mathfrak{M}$.Also$$\int_X(s+t)\ d\mu=\int_X s\ d\mu+\int_X t\ d\mu$$ 这是很简单的，我们可以通过上一个的命题5，转换到对同一个区域的求和，然后利用线性。注意这个线性是极限的直接推论，$$
	\begin{align*}\varphi(E)&=\sum_{i=1}^n\alpha_i\mu(A_i\cap E)\\
	&=\sum_{i=1}^n\alpha_i\sum_{r=1}^\infty\mu(A_i\cap E_r)\\
	&=\sum_{r=1}^\infty\sum_{i=1}^n\alpha_i \mu(A_i\cap E_r)
	\\&=\sum_{r=1}^\infty\varphi(E_r)\end{align*}$$
来说一下这个证明,首先是定义，然后拆成disjoint的集合区域，交换求和，然后证明完成。

## Lebesgue's Monotone Conergence Theorem
Let $\{f_n\}$ be a sequence of measureable function on $X$,and suppose that 
1. $0\le f_1(x)\le f_2(x)\le\cdots\le\infty$ for every $x\in X$,
2. $f_n(x)\to f(x)$ as $n \to\infty$,for every $x\in X$.
Then $f$ is measurable,and$$
\int_X f_n\ d\mu\to\int_X f\ d\mu\quad\text{as }n\to \infty$$ $f$ 是可测函数，可由可测函数的极限推出。简单可测函数$0\le s\le f$,let $c$ be a constant,$0<c<1$,and define$$E_n=\{x:f_n(x)\ge cs(x)\}$$ $E_n$是可测集合构造$\bigcap_{k=1}^\infty\{x:f_n(x)-cs(x)>\frac1k\}$ ，然后$E_1\subset E_2\subset\cdots$ ,$X=\bigcup E_n$ ,$$
\int_X f_n\ d \mu\ge\int_{E_{n}}f_n\ d\mu\ge c\int_{E_{n}}s\ d\mu$$然后对$n$取极限，然后在对$s$取极限，夹逼后就出来。
推论：
>If $f_n:X\to[0,\infty]$ is measurable, for $n=1,2,3,\dots,$and$$
f(x)=\sum_{n=1}^\infty f_n(x)\quad(x\in X)$$then$$\int_X f\ d\mu=\sum_{n=1}^\infty\int_X f_n\ d\mu$$ If $a_{ij}\ge 0$ for $i$ and $j=1,2,3,\dots,$ then$$\sum_{i=1}^\infty\sum_{j=1}^\infty a_{ij}=\sum_{j=1}^\infty\sum_{i=1}^\infty a_{ij}$$
# Fatou's Lemma
If $f_n:X\to[0,\infty]$ is measurable ,for each postive integer $n$,then$$
\int_X(\liminf_{n\to \infty}f_n)\ d\mu\le\liminf_{n\to\infty}\int_X f_n\ d\mu$$ Put$$g_k(x)=\inf_{i\ge k}f_i(x)$$
Then $g_k\le f_k$,然后$g_k$单调递增收敛到$\liminf f_n(x)$ 

Suppose $f:X\to[0,\infty]$ is measurable,and$$\varphi(E)=\int_E f\ d\mu\quad(E\in\mathfrak{M})$$
Then $\varphi$ is a measure on $\mathfrak{M}$ ,and
$$\int_X g\ d\varphi=\int_X gf\ d\mu$$ for every measurable $g$ on $X$ with range in$[0,\infty]$.

----------

# Integration of Complex Functions
We define $L^1(\mu)$ to be the collection of all complex measureable functions $f$ on $X$ for which $$\int_X|f|\ d\mu<\infty$$
The members of  $L^1(\mu)$ are called *Lebesgue integrable* functions (with respect to $\mu$ )

If $f=u+iv$ ,where $u$ and $v$ are real measurable functions on $X$,and if $f\in L^1(\mu)$ ,we define
$$\int_E f\ d\mu=\int_E u^+\ d\mu-\int_E u^-\ d\mu+i\int_E v^+\ d\mu-i\int_E v^-\ d\mu$$for every measurable set $E$
$L^1(\mu)$具有线性性质。
If $f\in L^1(\mu)$ ,then
$$\left|\int_X f\ d\mu\right|\le\int_X|f|\ d\mu$$ Put $z=\int_X f\ d\mu$,there is a complex number $\alpha$,with $|\alpha|=1$ ,such that $\alpha z=|z|$ .Let $u$ be the real part of $\alpha f$.Then $u\le |\alpha f|=|f|$ .Hence
$$\left|\int_X f\ d\mu\right|=\alpha\int_X f\ d\mu=\int_X \alpha f\ d\mu=\int_X u\ d\mu\le\int_X|f|\ d\mu$$ 
## Lebesgue's Dominated Convergence Theorem
Suppose $\{f_n\}$ is a sequence of complex measureable functions on $X$ such that $$f(x)=\lim_{n\to\infty}f_n(x)$$ exists for every $x\in X$. If there is a function $g\in L^1(\mu)$ such that$$|f_n(x)|\le g(x)$$
then $f \in L^1(\mu)$,
$$\lim_{n\to\infty}\int_X|f_n-f|\ d\mu=0$$
and$$\lim_{n\to\infty}\int_X f_n\ d\mu=\int_X f\ d\mu$$ 
>证明:Factou's lemma applies to the functions $2g-|f_n-f|$ and yields
$$ \begin{align*}\int_X 2g\ d\mu &\le\liminf_{n\to\infty}\int_X(2g-|f_n-f|)\ d\mu\\
&=\int_X 2g\ d\mu+\liminf_{n\to\infty}\int_X -|f_n-f|\ d\mu \\
&=\int_X 2g\ d\mu-\limsup_{n\to\infty}\int_X |f_n-f|\ d\mu 
\end{align*} $$
Since $\int_X 2g\ d\mu$ is finite,we may subtract it and obtain$$\limsup_{n\to\infty}\int_X |f_n-f|\ d\mu\le0$$
# The Role Played by Sets of Measure Zero 
## Definition
Let $P$ be a property which a point $x$ may or may not have. For instance, $P$ might be the property "$f(x) > 0$" if $f$ is a given function, or it might be " $\{f_n(x)\}$ converges" if $\{f_n\}$ is a given sequence of functions.
If $\mu$ is a measure on a a-algebra $\mathfrak{M}$ and if $E\in\mathfrak{M}$, the statement " $P$ holds almost everywhere on $E$" (abbreviated to " P holds a.e. on $E$") means that there exists an $N\subset \mathfrak{M}$  such that $\mu(N)=0$,$N\subset E$  and $P$  holds at every point of $N-E$ . This concept of a.e. depends of course very strongly on the given measure, and we shall write " a.e. $[\mu]$$ " whenever clarity requires that the measure be indicated.
For example, if I and g are measurable functions and if:
$$\mu(\{x:f(x)\not =g(x)\})=0$$
we say that $f=g$ a.e.$[\mu]$ on $X$,and we may write $f\sim g$ This is easily seen to be an equivalence relation. The transitivity ($f\sim g$ and $g\sim h$ implies $f\sim h$ ) is a consequence of the fact that the union of two sets of measure 0 has measure 0.
Note that if $f\sim g$,then, for every $E\in\mathfrak{M}$$$\int_E f\ d\mu=\int_E g\ d\mu$$
Let $(X,\mathfrak{M},\mu)$ be a measure space,let $\mathfrak{M}^*$ be the collection of all $E\subset X$ for which there exist set $A$ and $B\in\mathfrak{M}$ such that $A\subset E\subset B$ and $\mu(B-A)=0$, and define $\mu(E)=\mu(A)$ in this situation.Then $\mathfrak{M}^*$ is a $\sigma$-algebra,and $\mu$ is a measure on $\mathfrak{M}^*$ 

This extended measure $\mu$ is called *complete*.

Let us call a function $f$ defined on a set $E\in\mathfrak{M}$ measurable on $X$ if $\mu(E^c)=0$ and if $f^{-1}(V)\cap E$ is measurable for every open set $V$

Suppose $\{f_n\}$ is a sequence of comples measurable functions defined a.e. on $X$ such tath $$
\sum_{n=1}^\infty \int_{X}|f_{n}|\ d\mu<\infty
$$Then the series $$
f(x)=\sum_{n=1}^\infty f_{n}(x)
$$
converges for almosts all $x$,$f\in L^1(\mu)$ ,and $$
\int_{X}f\ d \mu=\sum_{n=1}^\infty \int_{X}f_{n}(x)
$$
-----

# Exercises
1. Does there exist an infinite a-algebra which has only countably many members?
   证明：只需要证明所有交集非空的集合是一个子集，然后我们可以对这些集合进行排序，可以构成一个对正整数的双射，然后我们有结论正整数的所有子集不可数。
2. Prove an analogue of Theorem 1.8 for n functions.  
   证明:实际上只需要证明对可测函数$u_{1},u_{2},\cdots,u_{n}$ ,$$
f(x)=(u_{1},u_{2},\cdots,u_{n})
			$$是可测函数。先证明对$\cup U_{i}$中的开集可以被可数个开长方形组成。然后对这个空间的任意开长方形($I_{1}\times I_{2}\times\cdots\times I_{n}$)我们有 $$
f^{-1}(I_{1}\times I_{2}\times\cdots\times I_{n})=u^{-1}(I_{1})\bigcup \cdots\bigcup u^{-1}(I_{n})
	$$对于每个开区间$I_{i}$，可测函数$u_i$ 都返回一个可测集合，然后可测集合的并自然是可测集合。所以这个函数是可测函数

3. Prove that if $f$ is a real function on a measurable space $X$ such that $\{x:f(x)\ge r\}$  is measurable for every rational $r$, then $f$ is measurable.
   证明:考虑$A_{n}=\left\{  f(x)> r-\frac{1}{n}  \right\}$ 这是一个开集然后 $$
\{ x:f(x)\ge r \}=f^{-1}(\bigcap_{i}A_{i})=\bigcap_{i}f^{-1}(A_{i})$$ 然后$f$是可测函数，因此这个集合是一个可测集合.
4. Let $\{a_{n}\}$ and $\{b_{n}\}$ be sequences in $[-\infty,\infty]$,and prove the following asertions:
	+ $$\limsup_{n \to \infty }(-a_{n})=-\liminf_{ n \to \infty }a_{n}$$
	+ $$
\limsup_{ n \to \infty }(a_{n}+b_{n})\le\limsup_{ n \to \infty } a_{n}+\limsup_{ n \to \infty } b_{n}
	$$              provided none of the sums is of the form $\infty-\infty$
	+ If $a_{n}\le b_{n}$ for all $n$,then $$
\liminf_{ n \to \infty } a_{n}\le\liminf_{ n \to \infty }b_{n}
$$
5. 可测函数的四则运算是可测函数，可测函数的极限是可测函数
6. Let $X$ be an uncountable set, let $\mathfrak{M}$ be the collection of all sets $E \subset$such that either $E$ or $E^c$ is at most countable, and define $\mu(E)$  in the first case,$\mu(E)=1$ in the second. Prove that $\mathfrak{M}$ is a a-algebra in $X$ and that $\mu$ is a measure on $\mathfrak{M}$. Describe the corresponding measurable functions and their integrals.
   证明：
	1. $X\in \mathfrak{M}$
	 2. $E\in \mathfrak{M}$,$E^c\in \mathfrak{M}$
	 3. $E_{i}\in \mathfrak{M}$ ,$\bigcup E_{i} \in \mathfrak{M}$ 
	 下面描述测度函数以及积分。
	 测度函数发射到$\left\{ 1,0 \right\}$ ，然后我们验证对于可数交集非空的一组集合满足可加性。如果所有集合都是可数集合，那么显然。如果有一个不可数集合，不妨设为$A_{i}$，那么$A_{i}^c$是可数集合，并且由于他们交集非空，所以都是$A_i^c$的子集，显然都是可数集合，因此两边的值都是1。
7. Suppose $f_{n}:X\to[0,\infty]$ is measurable for $n=1,2,3,\dots,f_{1}\ge f_{2}\ge f_{3}\ge \cdots\ge0$,$f_{n}(x)\to f(x)$ as $n\to \infty$,for every $x \in X$ ,and$f_{1}\in L^1(\mu)$.Prove that then $$
\lim_{ n \to \infty } \int_{X}f_{n}\ dx=\int_{X}f\ d\mu
		$$and show that this conclusion does not follow if the condition "$f_{1}\in L^1(\mu)$" isomitted.
	证明:$f$是可测函数，这是因为是可测函数的极限不妨设$\lim\limits_{ n \to \infty }\int_{X}f_{n}\ dx=\alpha$,然后$\alpha\ge \int_{X} f\ d \mu$ , 
	不会做，之间套勒贝格控制收敛定理吧。
8. Put $f_{n}=\chi_{E}$ if $n$ is odd,$f_{n}=1-\chi_{E}$ if $n$ is even. What is the relevance of this example to Fatou's lemma?
	  这是一个严格的不等号， 当且仅当$\mu(X)=\mu\left( E\bigcap X \right)$ 成立$$
\int_{X}\liminf_{ n \to \infty } f_{n}=0<\liminf_{ n \to \infty } \int_{X}f_{n}=\min \left\{ \mu(X)-\mu\left( E\bigcap X \right),\mu\left( X\bigcap E \right) \right\}
$$
9. Suppose $\mu$ is a positive measure on $X$,$f:X\to [0,\infty]$ is measurable,$\int_{X}f\ d\mu=c$,where $0<c<\infty$,and $\alpha$ is a constant.Prove that $$
\lim_{ n \to \infty } \int_{X}n\log\left[ 1+\left( \frac{f}{n} \right)^\alpha \right]\ d\mu=\begin{cases}
\infty  & \text{if } 0<\alpha<1,\\ 
c & \text{if }\alpha=1, \\
0 & \text{if }1<\alpha<\infty
\end{cases}
	$$
		Hint:If $\alpha\ge 1$, the integrands are dominated by $\alpha f$.If $\alpha<1$,Fatou's lemma[[CHAPTER ONE#Fatou's Lemma]] can be applied.
	证明：按照提示，$\alpha\ge 1$我们可以使用勒贝格控制收敛定理，如果$\alpha<1$ 我们使用Fatou's Lemma,取被击函数的下极限也就是$\infty$ ,然后极限传递性得到。
10. Suppose $\mu(X)<\infty$,$\left\{ f_{n} \right\}$ is a sequence of bounded complex measurable function on $X$, and $f_{n}\to f$ uniformly on $X$.Prove that $$
\lim_{ n \to \infty } \int_{X}f_{n}\ d\mu=\int_{X}f\ d\mu
		$$
	and show that the hypothesis "$\mu(X)<\infty$" cannot be omitted.
	想办法凑出一个界，然后使用勒贝格控制收敛定理。
11. Show that $$
A=\bigcap_{n=1}^\infty \bigcup_{k=n}^\infty E_{k}
	$$
	and hence prove the theorem without any reference to integration.
	$\mathbf{Solution}$: $A$ is defined as the collections of all $x$ which lie in infinitely many $E_{k}$ .Thus $x \in A \Leftrightarrow x\in \bigcup_{k=n}^\infty E_{k}\forall n\in \mathbb{N}$ ;and so $$
A=\bigcap_{n=1}^\infty \bigcup_{k=n}^\infty E_{k}
$$
	Now let $\epsilon>0$.Since $\sum_{k=1}^\infty\mu(E_k)<\infty$ ,therefore there exists $n_{0}\in\mathbb{N}$ such that $\sum_{k=n_{0}}^\infty \mu(E_{k})<\epsilon$ .And
	$$
\begin{align*}
\mu(A)&=\mu\left( \bigcap_{n=1}^\infty \bigcup_{k=n}^\infty E_{k} \right)\\
&\le\mu\left( \bigcup_{k=n}^\infty E_{k}\right)\\
&\le\sum_{k=n_{0}}^\infty\mu(E_{k})\\
&<\epsilon
\end{align*}
$$
	不是很难，但是我现在做题完全不想动脑子。
12. Suppose $f\in L^1(\mu)$.Prove that to each $\varepsilon>0$ there exists a $\delta>0$ such that $\int_{E}|f|\ d\mu<\epsilon$ whenever $\mu(E)<\delta$ .



跳转下一章[[CHAPTER TWO]]
