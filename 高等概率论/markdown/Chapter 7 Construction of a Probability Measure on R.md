## Chapter 7 Construction of a Probability Measure on $\R$

This chapter is an important special case of what we dealt with in Chapter 6. We assume

+ $\Omega = \R$
+ $\mathcal{B}$ be the Borel $\sigma$-algebra of $\R$
  + That is, $\mathcal{B} = \sigma(\mathcal{O})$ ,  where $\mathcal{O}$ are the open subsets of $\R$



**Definition 7.1**

The distribution function induced by a probability $P$ on $(\R; \mathcal{B})$ is the function
$$
F(x) = P((-\infty,x])
$$

> 定义了一个分布函数，跟本科学的不一样，按照现在的定义来说，分布函数是 $F(x) = P((-\infty,x])$ ，$P$是定义在$\Omega$即($\R$)上的
>
> 记$P$为原概率测度， $(-\infty,x] \in \mathcal{B}$ 
>
> 本科：$X(w) \sim F(x) = P(\{ w \in \Omega:X(w) \le x \}) = P(\{ w \in \Omega,X(w) \in (-\infty,x]\})$ 
>
> 现在：$P((-\infty,x])=...=P^X( (-\infty,x])$
>
> $(-\infty,x]$是原来的原像的集合



**Theorem 7.1**

The distribution function $F$ characterizes the probability. 
分布函数$F$ (唯一的)定义了概率测度$P$

> 给一个 $F$，在 $\R$和 Borel-$\sigma$-代数上确定概率$P$
> 定义：给一个$P$，定义一个$F$
> 即 $F$与$P$之间 characterize
> 特征函数也能和唯一定义概率

> 证明：思路 证明 $F=G$时，$P=Q$ 
> $$
> F(x) = P((-\infty,x]) \\
> G(x) = Q((-\infty,x])
> $$

> $Q$是另一个概率测度
>
> 首先，令 $\mathcal{B}_0$是$(x,y]$这种形式的区间的有限交组成的集合，$-\infty \le x \le y \le +\infty$ 
>
> 当 $x=y$时，$(x,y]=\emptyset$
>
> > $(x,y]=(-\infty,y] \cap (-\infty,x]^c$ 
> > 若$x=y$，则上述集合为空集（一个集合与其补集之交为空集）
>
> 证明$\mathcal{B}_0$是一个代数
>
> > 1. $\empty \in \mathcal{B}_0,\quad \R =(-\infty,\infty)\in \mathcal{B}_0 $ 
> > 2. 若 $A \in \mathcal{B}_0$，则 $A = \cup_{i=1}^{n} (x_i,y_i]$ 
> >    不妨设 $y_i < x_{i+1}$ ，保证$A$里面的集合两两不交
> >    $A^c = (-\infty,x_1) \cup (y_1,x_2]\cup ... \cup (y_{n-1},x_{n}) \cup (y_{n},+\infty) \in \mathcal{B}_0$ （定义）
> > 3. 对有限交封闭
> >    $A \in \mathcal{B}_0,B \in \mathcal{B}_0$，不妨设
> >    $A = (x_1,y_1] \cup (x_2,y_2]$
> >    $B = (x_1',y_1'] \cup (x_2',y_2']$
> >    分类讨论：...
>
> 说明 $\mathcal{B}_0$生成的最小$\sigma$代数是一个博雷尔$\sigma$代数
>
> > + 如果$(a,b)$是一个开区间，则$(a,b) = \cup_{n=N}^{\infty} (a,b-\frac{1}{N}]$   （这里从$N$开始，保证了 $a<b-\frac{1}{N}$ )
> >   则 $\sigma(\mathcal{B}_0)$包含了所有的开区间
> >
> > > $\because \ (a,b) = \cup_{n=N}^{\infty} (a,b-\frac{1}{N}]$
> > > $\quad \sigma(\mathcal{B}_0): \empty,\Omega,\mathcal{B}_0,\mathcal{B}_0^c$      $\sigma(\mathcal{B}_0)$是一个$\sigma$代数
> > >      则 $(a,b)\in \sigma(\mathcal{B}_0)$ 
> > >      即 $\sigma(\mathcal{B}_0)$包含了所有的开区间
> >
> > + 任一个开集合可以分解为可列个开区间的并，则 $\sigma(\mathcal{B}_0)$包含了所有的开集合，$\mathcal{B}$是最小的包含了所有开集合的 $\sigma$ 代数
> >
> > > $\mathcal{B}$是$\R$上的博雷尔集
> > > $\mathcal{B}$是$\R$上所有开集生成的最小$\sigma$代数
> > > 则$\mathcal{B} \subset \sigma(\mathcal{B_0})$
> >
> > + $\cap_{n=1}^{\infty}(a,b+\frac{1}{n}) = (a,b]$ 
> >
> > > $\cap_{n=1}^{\infty}(a,b+\frac{1}{n}) \in \mathcal{B}$
> > > $\cap_{n=1}^{\infty}(a,b+\frac{1}{n}) = (a,b] \in \mathcal{B}_0$ 
> > > $\forall B \in \mathcal{B}_0,B = \cup_{i=1}^{m}(a_i,b_i] = \cup_{i=1}^{m } \cap_{n=1}^{\infty}(a_i,b_i+\frac{1}{n}) \in \mathcal{B}$ 
> > > 则 $\mathcal{B}_0 \subset \mathcal{B}$
> >
> > + 则 $\sigma(\mathcal{B}_0) = \mathcal{B}$ 
> >
> > > $\sigma(\mathcal{B}_0)$是包含$\mathcal{B}_0$的最小$\sigma$代数，是包含开区间的最小$\sigma$代数   $\mathcal{B} \subset \sigma(\mathcal{B_0})$
> > > $\mathcal{B}$是包含$\mathcal{B}_0$的$\sigma$代数，是包含开区间的最小$\sigma$代数    $\mathcal{B}_0 \subset \mathcal{B}$
> > > 则$\mathcal{B} \subset \sigma(\mathcal{B}_0) \subset \mathcal{B}$
> > > 即 $\sigma(\mathcal{B_0}) = \mathcal{B}$ 
>
> The relation (15) implies that   $P((x,y])=F(y) - F(x)$
>
> > > $F(x) = P((-\infty,x])$
> > > $F(y) = P((-\infty,y])$
> > > $$
> > > \begin{array}
> > > 	+P((x,y]) &= P( (-\infty,y] \cap (-\infty,x]^c ) \\
> > > 			  &= P( \{(-\infty,y]^c \cup (-\infty,x]\}^c ) \\
> > > 			  &= 1-P( (-\infty,y]^c \cup (-\infty,x] ) \\
> > > 			  &= 1-(F((-\infty,y]^c) + F((-\infty,x])) \\
> > > 			  &= 1-(1-F(y) + F(x)) \\
> > > 			  &= F(y) - F(x) \\
> > > \end{array}
> > > $$
> >
> > If $A \in \mathcal{B}_0 \quad A = \cup_{1\le i \le n} (x_i,y_i] \text{ with } y_i < x_{i+1}$ 
> > $\Rightarrow \quad P(A) = \sum_{1 \le i \le n} \{ F(y_i) - F(x_i) \}$
>
> 若 $Q$是另一个概率测度 $F(x) = Q((-\infty,x])$
> 则在先前的证明中 ，在 $\mathcal{B}_0$上 $P=Q$
> 由定理 6.1 可知，在 $\mathcal{B}$上 $P=Q$，则这是同样的概率测度
>
> > > 定理6.1：每一个定义在代数$\mathcal{A}_0$上的概率 $P$，在 $\mathcal{A}$上都有一个唯一的拓展
> > > $\mathcal{A}_0$是代数，$\mathcal{A}$是$\sigma$代数
> > > 一一对应起来
> > > $$
> > > \begin{array}{cc}
> > > \mathrm{The 6.1} & \mathrm{The7.1} \\
> > > \hline \\
> > > \mathrm{algebra}\ \mathcal{A}_0 & \mathrm{algebra}\ \mathcal{B}_0 \\
> > > \sigma\mathrm{-algebra}\ \mathcal{A} & \sigma \mathrm{-algebra}\ \mathcal{B} \\
> > > \mathcal{A} = \sigma(\mathcal{A}_0) & \mathcal{B} = \sigma(\mathcal{B}_0) \\
> > > \hline
> > > \end{array}
> > > $$
> > > 则可知，对于每一个定义在代数$\mathcal{B}_0$上的概率 $P$，在 $\mathcal{B}$上都有一个唯一的拓展



注：定理7.1就是想证明唯一性，概率$P$的存在性并不需要证明。而且对于概率$P$，只要满足概率的两条性质（正则性、可列可加性），则就是一个概率。







**Theorem 7.2**

A function $F$ is the distribution function of a (unique) probability on $(\R; \mathcal{B})$ if and only if one has:

1. $F$ is non-decreasing;
2. $F$ is right continuous;
3. $\lim_{x \to -\infty}F(x)=0$  and  $\lim_{x \to \infty}F(x)=1$