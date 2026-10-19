### Lec 1 02/10/26

Part 1
- Analysis on $\mathbb{R}^n$
- Metric Spaces (distance)

Euclidean spaces ($\mathbb{R}^n$)
1. $(1, x, x^2, ..., x^n), x^i$ means i-th coordinate of $x$
2. $<\cdot ; \cdot> : \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}$
   1. $||x|| \geq 0$, = iff 0
   2. 数乘
   3. triagular inequality
3. Relation between different types of distances ($|\cdot|$ <dot product> on $\mathbb{R}$ and $||\cdot||$ <norm, $||x||$>)
   $\forall 1\leq k\leq n, x\in \mathbb{R}^n$
   $\min_{1\leq i\leq n} |x^i| \leq |x^k| \leq \sum_{i=1}^n |x^i|\leq \sqrt{n}||x||$ (Cauchy-Schwarz)
4. Convergence of sequence 
   1. seq: list $(x_i)$ s.t. $x_i \in \mathbb{R}$
   2. Def: $(x_i)$ converges to $x\in \mathbb{R}$ if: $\forall \epsilon >0, \exists i_0 = i_0(\epsilon)\geq 1$ s.t.: $\forall i\geq i_0, ||x^i - x||\leq \epsilon$
   3. Prop: $(x_i)$ converges $\iff$ for each $1\leq p\leq n, (x_i^p)_{i\geq 1}$ converges to $x^p$
5. Open sets

#####

### Lec 2 05/10/26
1. Open set in $\mathbb{R}^n$
   1. $a\in\mathbb{R}$,
   $$(a^1-\epsilon, a^1 + \epsilon) \times ... \times a^n-\epsilon, a^n + \epsilon)=\{x\in\mathbb{R}^m: \forall 1\leq i\leq n, |x^i-a^i|<\epsilon\}$$
   2. For $r>0$ define the open ball of radius $r$: $B_r(x) = B(x,r) = \{y\in\mathbb{R}^n, \mathbf{||y-x||<r\}}$
   3. (Open sets) A set $U\subset \mathbb{R}^n$, s.t. $\forall x\in U, \exists \delta_x, B_{\delta_x}(x)\subset U$, i.e.$\textbf{any point has an open ball in the set}$
2. Continuity at a point, on an open set
   1. Let $A\subset \mathbb{R}^n$ be an open set, define $f: A\to \mathbb{R}^m$, $f$ is continuous at $p$ if 
   $$\forall \epsilon>0, \exists \delta>0 s.t. \forall x\in A, ||x-p||<\delta\implies ||f(x)-f(p)||<\epsilon$$
   2. If $f$ is continuous on every point in $A$, then $f$ is continuous on $A$
   3. Equivalently, $f(A\cap B_\delta (p))\subset B(f(p),\epsilon)$ indicates continuity
   4. e.g. Linear map$\Lambda: \mathbb{R}^n\to \mathbb{R}^m$ satisfying $\Lambda (x+ry)=\Lambda (x)+ r\Lambda (y)$ is continuous
      1. Let $e^i = (0,...,1,...,0)\in \mathbb{R}^n$ with the i-th position 1 be canonical bases of $\mathbb{R}^n$
      2. $$\begin{align}
        \Lambda (x) - \Lambda (p) &= \Lambda (x-p)\\
        &= \Lambda (\sum_{i=1}^n (x^i-p^i)e^i)\\
        &= \sum_{i=1}^n \Lambda (x^i-p^i)e^i)\\
        &= \sum_{i=1}^n |x^i - p^i| \Lambda (e^i)\\
        &\leq \sqrt{\sum_{i=1}^n |x^i - p^i|^2} \sqrt{\sum_{i=1}^n \Lambda (e^i)}\\
        &= M||x-p||
        \end{align}$$
        by defining $M=\sum_{i=1}^n \Lambda (e^i)$
       3. By picking $\delta = \frac{\epsilon}{M}$ we have $|x-p|<\delta \implies |\Lambda (x)-\Lambda (p)<\frac{\epsilon}{M} \cdot M = \epsilon$
3. Thm(Composition)
   Let $A\subset \mathbb{R}^n$ and $B\subset\mathbb{R}^d$ be open sets and $f: A\to B, g: B\to \mathbb{R}^m$, if $f,g$ are continuous at $p$, then $g\circ f: A\to \mathbb{R}^m$ is continuous at $p$
4. Properties
   1. $f,g: A\to \mathbb{R}, +, \cdot$ continuous

#####

### Lec 3 12/10/26

1. Continuity: derived immediately from $\mathbb{R}$ to Euclidean space
2. Derivative (more geometric)
   1. Def
      1. let $\Omega$ be an open set in $\mathbb{R}^n, f: \Omega \to \mathbb{R}^m$ is differentiable if $\exists$ a linear map $\Lambda \in L(\mathbb{R}^n, \mathbb{R}^m)$ s.t.
      $$ \lim_{x\to p} \frac{||f(x)- f(p) - \Lambda (x-p)||}{||x-p||} = 0, Df(p):= \Lambda, \mathbb{R}^n \to \mathbb{R}$$
      2. ! $f$ differentiable at $p \nRightarrow \lim_{x\to p} \frac{f(x)-f(p)}{||x-p||}$ exists, since the direction of derivative is not considered (e.g. $x$ at $x=0$).
      3. Rmk: $Df$ also called the differential of $f$ at $p$; apply linear map: $\Lambda[p]$, otherwise $Df(p)$
      4. $\iff \exists \Lambda s.t. \lim_{h\to 0} \frac{||f(p+h)-f(p)-\Lambda[h]||}{||h||}$
   2. Let $m\geq 1$ and $f_1, \cdots, f_m: (a,b)\to \mathbb{R}$, then $f(x) = (f_1, \cdots, f_m)$ is differentiable at $p$ as soon as $f_i$ are differentiable at $p$, and $Df(p) = (f_1'(p), \cdots, f_m'(p))$
   3. Thm 1.33: if derivative exists, then it is unique.
   
#####

### Lec 4 16/10/26

1. Chain rule
   1. $g: (a,b)\to (c, d)$ differentiable at $(a,b), f: (c,d)\to \mathbb{R}$ differentiable at $(g(p))$, then $f\circ g: (a,b)\to \mathbb{R}$ is diferrentiable at $p$,
      \[ (f\circ g)'(p) = Df(g(p))Dg(p) \]
   2. Proof: replace by linear approximation at both $g,f$