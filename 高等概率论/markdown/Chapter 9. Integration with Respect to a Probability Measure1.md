# Chapter 9. Integration with Respect to a Probability Measure1

**Background**

Let $(\Omega,\mathcal{A},P)$ be a probability space.
We want to define the expectation, or what is equivalent, the "integral", of general $r.v.$.
We have of course already done this for $r.v.s$ on a countable space $\Omega$.
The general case (for arbitrary $\Omega$) is more delicate.



**Definition 9.1**

1. A $r.v. \ X$ is called **simple** if it takes on only a finite number of values and hence can be written in the form
   $$
   X = \sum_{i=1}^{n} a_i I_{A_i} \tag{1}
   $$
   Where $a_i \in \R$, and $A_i \in \mathcal{A},1\le i \le n$ 

> > 若 $A_k \in \mathcal{F},k=1,2,...,n$两两不交，且
> > $\cup_{k=1}^n A_k = \Omega,a_k \in \hat{\mathcal{R}}^{(1)},k=1,2,...,n$ 
> > 则称函数 
> > $$
> > X(w) = \sum_{k=1}^n a_k I_{A_k}(w) \quad w \in \Omega \notag
> > $$
> > 为 $(\Omega,\mathcal{F})$上的简单函数

   - Such an $X$ is clearly measurable;   (Why?) 思考这里为什么$X$是可测的
     > $$
     > \forall B \in \mathcal{B}^k \\
     > \begin{array}{ll}
     > \begin{aligned}
     > 
     > X^{-1}(B) &= \{w: X(w) \in B\} \\
     > 		  &= \cup_{a_k \in B} \{w:X(w) = a_k\} \\
     > 		  &= \cup_{a_k \in B} A_k \\
     > 		  &\in \mathcal{F}
     > \end{aligned}
     > 
     > &
     > \begin{array}{ll}
     > \text{逆象的定义} \\
     > \text{简单函数的定义} \\
     > \text{简单函数的定义} \\
     > \text{简单函数中} A_k \in \mathcal{F} \Rightarrow \cup_{A_k \in B} A_k \in \mathcal{F}
     > \end{array}
     > \end{array}
     > $$
     

   由定理8.1可知$X$可测。

   - Conversely, if $X$ is measurable and takes on the values $a_1,...,a_n$ it must have the representation (1) with $A_i = \{X=a_i\}$ ;
   
   - A simple $r.v.$ has of course many different representation of the form (1).

2. If $X$ is simple, its **expectation** (or "integral" with respect to $P$) is the number
   $$
   E\{X\} = \sum_{i=1}^{n} a_i P(A_i) \tag{2}
   $$

   - This is also written $\int X(w) P(dw)$ and even more simply $\int X dP$;
   - A little algebra shows that $E\{X\}$ does not depend on the particular representation (1) chosen for $X$. 练习：



**Exercise**

Let $(\Omega,\mathcal{A},P)$ be a probability space
Let $X:\Omega \to \R$ be such that it admits two representations
$$
X = \sum_{i=1}^{n} a_i I_{A_i} \quad \text{and} \quad X = \sum_{j=1}^{m} b_j I_{B_j}
$$
where $a_i,b_j \in \R$ , and $A_i,B_j \in \mathcal{A}$ for all $i,j.$ Show that
$$
\sum_{i=1}^{n} a_i P(A_i) = \sum_{j=1}^{m} b_j P(B_j)
$$

-------------

> First, prove that $\cup_{i=1}^{ n}A_i = \cup_{j=1}^{m}B_j$.
>
> Assume $
> \begin{array}{lll}
> 	a_i \neq 0 & A_i \cap A_j = \empty \\
> 	b_j \neq 0 & B_i \cap B_j = \empty
> \end{array}
> (i\neq j)$ 
>
> > $$
> > \begin{array}{lll}
> > \hline
> > 	\begin{array}{lll}
> > 		\forall w \in \cup_{i=1}^{n} A_i \\
> > 		\exists i_0 \in \left\{ 1,2,...,n \right\} \\
> > 		s.t. \ X(w) = a_{i_0} \neq 0 \\
> > 		so \ w \in \cup_{j=1}^{m}B_j \\
> > 		\quad else \ X(w) = 0 \\
> > 		\therefore \ \cup_{i=1}^{n}A_i \subset \cup_{j=1}^{m}B_j \\
> > 	\end{array}
> > 	&
> > 	\begin{array}{lll}
> > 		\forall w \in \cup_{j=1}^{m}B_j \\
> > 		\exists j_0 \in  \left\{ 1,2,...,n \right\} \\
> > 		s.t. \ X(w) = b_{j_0} \neq 0 \\
> > 		so \ w \in \cup_{i=1}^{n}A_i \\
> > 		\quad else \ X(w) = 0 \\
> > 		\therefore \ \cup_{j=1}^{m}B_j \subset \cup_{i=1}^{n}A_i
> > 	\end{array} 
> > 	\\
> > 	 \Downarrow \\
> >  \cup_{j=1}^{m}B_j =  \cup_{i=1}^{n}A_i\\
> >  \hline
> > \end{array}
> > $$
>
>
> Second, if $A_i B_j \neq \emptyset$, for $w \in A_i B_j \quad X(w) = a_i = b_j$ 
>
> > $$
> > \begin{array}{lll}
> > \hline
> > 	\begin{aligned}
> > 		X &= \sum_{i=1}^{n} a_i I_{A_i} \\
> > 		  &= \sum_{i=1}^{n} a_i I_{A_i \cap ( \cup_{i=1}^n A_i)} \\
> > 		  &= \sum_{i=1}^{n} a_i I_{A_i \cap ( \cup_{j=1}^n B_j)} \\
> > 		  &= \sum_{i=1}^{n} a_i I_{ \cup_{j=1}^m A_i B_j} \\
> > 		  &= \sum_{i=1}^{n} \sum_{j=1}^{m} a_i I_{A_i B_j} \\
> > 	\end{aligned}
> > 	&
> > 	\begin{aligned}
> > 		X &= \sum_{j=1}^{m} b_j I_{B_j} \\
> > 		  &= \sum_{j=1}^{m} b_j I_{B_j \cap ( \cup_{j=1}^m B_j)} \\
> > 		  &= \sum_{j=1}^{m} b_j I_{B_j \cap ( \cup_{i=1}^n A_i)} \\
> > 		  &= \sum_{j=1}^{m} b_j I_{ \cup_{i=1}^n A_i B_j} \\
> > 		  &= \sum_{i=1}^{n} \sum_{j=1}^{m} b_j I_{A_i B_j} \\
> > 
> > 	\end{aligned}\\
> > 	\Downarrow \\
> > 	\text{for } w \in A_iB_j\neq \emptyset, X(w) = a_i = b_j
> > 	\\
> > \hline
> > \end{array}
> > $$
> >
> > 如果 $A_iB_j = \empty$ , $a_iP(A_iB_j)=b_jP(A_iB_j)=0$，不影响计算
>
> Last,Prove $EX=EY$
>
> > $$
> > \begin{array}{lll}
> > \hline
> > 	\begin{aligned}
> > 		EX &= \sum_{i=1}^{n} a_i P(A_i) \\
> > 		   &= \sum_{i=1}^{n} a_i P(A_i \cap (\cup_{i=1}^{n}A_i)) \\
> > 		   &= \sum_{i=1}^{n} a_i P(A_i \cap ( \cup_{j=1}^{m} B_j)) \\
> > 		   &= \sum_{i=1}^{n} a_i P( \cup_{j=1}^{m}A_i B_j) \\
> > 		   &= \sum_{i=1}^{n} \sum_{j=1}^{m} a_i P(A_i B_j) \\
> > 	\end{aligned}
> > 	&
> > 	\begin{aligned}
> > 		EY &= \sum_{j=1}^{m} b_j P(B_j) \\
> > 		   &= \sum_{j=1}^{m} b_j P(B_j \cap (\cup_{j=1}^m B_j)) \\
> > 		   &= \sum_{j=1}^{m} b_j P(B_j \cap ( \cup_{i=1}^{n}A_i)) \\
> > 		   &= \sum_{j=1}^{m} b_j P( \cup_{i=1}^{n}A_i B_j) \ \text{ pairwise disjoint}\\
> > 		   &= \sum_{i=1}^{n} \sum_{j=1}^{m} b_j P(A_i B_j) \\
> > 	\end{aligned}
> > 	\\
> > 	\Downarrow \because a_i = b_j \\
> > 	EX=EY \\
> > \hline
> > \end{array}
> > $$
----------------

<br />
<br />
<br />


**Remark**  [测度与概率—2.3节 期望与积分 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/100160279)

- Let $X,Y$ be two simple $r.v.s$ and $\beta$ a real number. We clearly have

  > $X = \sum_{i=1}^n a_i I_{A_i} \quad Y = \sum_{j=1}^m b_j I_{B_j}$ 
  > $EX = \sum_{i=1}^n a_i P(A_i) \quad EY = \sum_{j=1}^m b_j P(B_j)$ 

  - **$E\{\beta X\} = \beta E\{X\}$**;

    > $E\{\beta X\}=\sum_{i=1}^n \beta a_i P(A_i)=\beta \sum_{i=1}^n a_i P(A_i)=\beta E\{X\}$ 
  - **$E\{X+Y\}=E\{X\}+E\{Y\}$**;

    > $\begin{aligned} E\{X+Y\}  &= \sum_{i=1}^n \sum_{j=1}^m (a_i + b_j) P(A_i B_j) \\ &=  \sum_{i=1}^n \sum_{j=1}^m a_i  P(A_i B_j) + \sum_{i=1}^n \sum_{j=1}^m b_j P(A_i B_j) \\ &=  \sum_{i=1}^n a_i P(A_i) +  \sum_{j=1}^m b_j P(B_j) \\ &= E\{X\} +E\{Y\} \end{aligned}$ 
  - **If $X\le Y$,then $E\{X\}\le E\{Y\}$**.
    
    > $X\le Y \Rightarrow a_i \le b_j$
    > $\begin{aligned} E\{X\} = \sum_{i=1}^n a_i P(A_i) &= \sum_{i=1}^n \sum_{j=1}^m a_i P(A_i B_j) \\ &\le \sum_{i=1}^n \sum_{j=1}^m b_j P(A_i B_j) \\ &= \sum_{j=1}^m b_j P( B_j) \\ &= E\{Y\} \end{aligned}$ 

- Thus, expectation is linear on the vector space of all simple $r.v.s$.

   因此，对于向量空间中的简单随机变量，期望是线性的。
   
- Next, we define expectation for positive $r.v.s$.
  定义正的随机变量

  For $X$ positive,

  - By this, we assume that $X$ may take all values in $[0,\infty]$, including $+\infty$;
    在这种假设下，随机变量$X$的取值为$[0,\infty]$ 
  
  - This innocuous extension is necessary for the coherence of some of our further results.
    这种无害的扩展对于我们某些进一步结果的一致性是必需的。
  
    Let
    $$
  E\{X\} = \sup \{E\{Y\}: Y \text{ a simple r.v. with } 0\le Y \le X\} \tag{3}
    $$
    
  - This supremum always exists in $[0,\infty]$.
    这个上确界在 $[0,\infty]$ 上总是存在的
    
    Since expectation is a positive operator on the set of simple $r.v.'s$, 
    既然期望是在简单随机变量集合上的正的运算
    
    it is clear that the definition above for $E\{X\}$ <font color="red">coincides</font> with Definition 9.1.
    则上面的关于期望的定义和定义9.1是一致的
    
    > 定义9.1里面的关于期望的定义为 $E\{X\} = \sum_{i=1}^{n} a_i P(A_i)$ 
    > 思考这里的一致性是为什么？



**Remark**

- Note that $E\{X\}\ge 0$,but we can have $E\{X\}=\infty$,even when $X$ is never equal $+\infty$.
  注意到 $E\{X\}\ge 0$ ,但是我们可以有 $E\{X\}=\infty$，即使随机变量$X$不等于无穷。

- Finally, let $X$ be an arbitrary $r.v.$.
  最后，令 $X$ 为任意的随机变量
  
  Let $X^+ = max(X,0) \quad X^- = - min(X,0)$.
  
  Then
  $$
  X = X^+ - X^- \quad |X| = X^+ + X^-
  $$
  and $X^+,X^-$ are positive $r.v.s$.



**Definition 9.2**

- A $r.v. \ X$ has a **finite expectation** (is "integrable") if both $E\{X^+\}$ and $E\{X^-\}$ are finite.
  若 $E\{X^+\}$ 和 $E\{X^-\}$ 都是有限的，则随机变量 $X$ 期望有限（也叫做可积）
  
  In this case, its expectation is the number 期望是两数之和
  $$
  E\{X\} = E\{X^+\} + E\{X^-\} \tag{4}
  $$
  

also written $\int X(w) dP(w)$ or $\int XdP$ 

  - If $X>0$ then $X^- =0$ and $X^+=X$ and, since obviously $E\{0\}=0$,this definition <font color="red">coincides</font> with (3)
    如果 $X>0$ ，则 $X^- =0$ 、$X^+=X$ 、$E\{0\}=0$，在这种情况下，和式(3)一致

  We write $\mathcal{L}^1$ to denote the set of all integrable $r.v.s$. (Sometimes we write $\mathcal{L}^1 (\Omega,\mathcal{A},P)$ to remove any possible ambiguity.)
  用 $\mathcal{L}^1$ 代表所有可积的随机变量的集合

- A $r.v. \ X$ admits an expectation if $E\{X^+\}$ and $E\{X^-\}$ are not both equal to $+\infty$.
随机变量$X$有期望，则 $E\{X^+\}$ 和 $E\{X^-\}$ 不都等于正无穷。
  
  - Then the expectation of $X$ is still given by (4), with the conventions $+\infty+a=+\infty$ and $-\infty+a=-\infty$ when $a\in \R$.
    则$X$的期望还是和(4)式一样，因为 $+\infty+a=+\infty$ 、 $-\infty+a=-\infty$   $a\in \R$.
  - If $X\ge 0$ this definition again coincides with (3)
    如果 $X\ge 0$ ，则(4)和(3)是一致的
  - Note that if $X$ admits an expectation, then $E\{X\} \in [-\infty,+\infty]$, and $X$ is integrable if and only if its expectation is finite.
    如果$X$有期望，则 $E\{X\} \in [-\infty,+\infty]$,
    $X$ 可积 $\Leftrightarrow$ 期望有限



**Remark 9.1**

When $\Omega$ is finite or countable we have thus two different definitions for the expectation of a $r.v. \ X$, the one above and the one given in Chapter 5.
当 $\Omega$ 是有限或可数，则有两个不同的关于随机变量 $X$ 的期望定义，一个是上面给出的，另一个是第五章给出的

In fact these two definitions <font color="red">coincides</font>: it is enough to verify this for a simple $r.v. \ X$, and in this case the formulas (5.1) and (9.2) are identical.
事实上，这两种定义是一致的

> $$
> E\{X\} = \sum_{j \in T'} j P(X=j) \tag{5.1} \\
> $$
>
> $$
> E\{X\} = \sum_{i=1}^n a_i P(A_i) \tag{9.2}
> $$

这个留作练习，下次课讲



**Theorem 9.1**

- (a) $\mathcal{L}^1$ is a vector space, and expectation is a linear map on $\mathcal{L}^1$, and it is also positive ($i.e. X \ge 0 \Rightarrow E\{X\}\ge 0$).
  $\mathcal{L}^1$ 是一个向量空间，期望是$\mathcal{L}^1$上的线性映射，它也是正的。
  

If further $0\le X \le Y$ are two $r.v.s$ and $Y \in \mathcal{L}^1$ and $E\{X\}\le E\{Y\}$.

- (b) $X\in \mathcal{L}^1$ iff $|X| \in \mathcal{L}^1$ and in this case $|E \left\{ X \right\}| \le E \left\{ |X| \right\}$.

    In particular any bounded $r.v.$ is integrable.

- (c) If $X = Y$ almost surely ($s.a.$) , then $E \left\{ X \right\}= E \left\{ Y \right\}$.

    > $$
    > X = Y \text{ a.s. if } P(X=Y)=P(\{w:X(w)=Y(w)\})=1
    > $$

- (d) (Monotone convergence theorem): 单调收敛定理

    If the $r.v.s$ $X_n$ are positive and increasing $a.s.$ to $X$, then $\lim_{n\to \infty}E \left\{ X_n \right\} = E \left\{ X \right\}$ (even if $E \left\{ X \right\}= \infty$).
- (e) (Fatou's lemma): 

    If the $r.v.s$ $X_n$ satisfy $X_n > Y$ $a.s.$ ($Y \in \mathcal{L}^1$), all $n$, we have
$$
E \left\{ \lim_{n \to \infty} \inf E \left\{ X_n \right\} \right\} \le \lim_{n \to \infty} \inf E \left\{ X_n \right\}
$$
In particular, if $X_n \ge 0$ $a.s.$ then
$$
E \left\{ \lim_{n \to \infty} \inf X_n \right\} \le \lim_{n \to \infty} \inf E \left\{ X_n \right\}
$$
- (f) (Lebesgue's dominated convergence theorem): 勒贝格控制收敛定理

    If the $r.v.s$ $X_n$ converge $a.s.$ to $X$ and if $|X_n|\le Y \ a.s. \in \mathcal{L}^1$, all $n$,

    then $X_n \in \mathcal{L}^1, X \in \mathcal{L}^1$ and $E \left\{ X_n \right\} \to E \left\{ X \right\}$.


**Statement**

- The $a.s.$ equality between $r.v.s$ is clearly an equivalence relation, and two equivalent (i.e. almost surely equal) r.v.s have the same expectation: 
    在随机变量间的几乎必然相等时一个等价关系，两个几乎必然相等的随机变量具有相同的表示。

    Thus :

    <font color="blue">one can define a space $L^1$ by considering " $\mathcal{L}^1$ modulo this equivalence relation"</font>
    
- In other words, an element of $L^1$ is an equivalence class, that is a collection of all $r.v.$ in $\mathcal{L}^1$ which are pairwise $a.s.$ equal.
    $L^1$ 是一个相等的类，是所有在 $\mathcal{L}^1$ 上的两两相等的类

- In view of (c) above, one may speak of the "expectation" of the equivalence class (which is the expectation of any one element belonging to this class).
    鉴于上面的（c），可以说等价类的“期望”（对属于该类的任何一个元素的期望）。

- Since further the addition of $r.v.s$ or the product of a $r.v.$ by a constant preserve $a.s.$ equality, the set $L^1$ is also a vector space.
    随机变量的加法或者乘法by a constant preserve $a.s.$ equality，则 $L^1$ 集合也是一个向量空间。

    Therefore, we commit the (innocuous) abuse of identifying a $r.v.$ with its equivalence class, and commonly write $X \in L^1$ instead of $X \in \mathcal{L}^1$.

- If $1\le p < \infty$, we define $\mathcal{L}^p$ to be the space of $r.v.s$ such that $|X|^p \in \mathcal{L}^1$ ;

    $L^p$ is defined analogously to $L^1$.
    $L^p$和$L^1$的定义类似

    That is, $L^p$ is $\mathcal{L}^p$ modulo the equivalence relation "almost surely".

- Put more simply, two elements of $\mathcal{L^p}$ that are $a.s.$ equal are considered to be representatives of one element of $L^p$.

<br />
<br />

**Two auxiliary results.**

<font color="bule">Result 1</font>

&emsp; For every positive r.v. $X$ there exists a sequence $\{X_n\}_{n\ge 1}$ of positive simple r.v.s which increases toward $X$ as $n$ increases to infinity.

&emsp; An example of such a sequence is given by 为什么要定义为 $\frac{k}{2^n}$ 
$$
X_n(w) = \left\{ 
\begin{array}{lll}
	\frac{k}{2^n} & if \ \frac{k}{2^n} \le X(w) < \frac{k+1}{2^n} \ and \ 0 \le k \le n2^{n}-1 \\
        n   & if \ X(w) \ge n
\end{array}
\right.
$$



<font color="bule">Result 2</font>

​	If $X$ is a positive r.v., and if $\{X_n\}_{n\ge 1}$ is any sequence of positive simple r.v.s increasing to $X$,  then $E\{X_n\}$ increases to $E\{X\}$. 