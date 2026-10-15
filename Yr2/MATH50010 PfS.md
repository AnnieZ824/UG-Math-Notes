### Lec 1
1. outcome (single, e.g. {H}{T}) vs event (subsets, e.g. {{HH},{TT}})
2. algebra: closed over finite $\cup$; $\sigma$-algebra: countable

#####

### Lec 2 06/10/26

def of prob
1. frequency: repeat the same experiment n times, $Pr(E)=\lim_{n\to \infty}\frac{m_E}{m}$
2. subjective: measure of my certainty/information/knowledge about the likelihood that the event occurs
3. classical

A probability space contains:
1. sample space $\Omega$: all possible outcomes
2. sigma-algebra $\mathcal{F}$: closed under complements, countable unions
3. prob function $Pr(\cdot)$ satisfies Kolmogorov axioms
   1. $Pr(\cdot) \geq 0$
   2. $Pr(\Omega)=1$
   3. Countable additive (disjoint)
LTP

**Continuity property
1. Let $A_1, A_2, ...$ be an increasing sequence of events, $ A_1\subset A_2\subset ...$. $A:=\cup_{i=1}^\infty A_i$, then $Pr( \cup_(n=1)^\infty A_n)=\lim_{n\to \infty} Pr(A_n)$
2. $B_i$ decreasing sequence, $B:= \cap$
3. Prove by setting disjoint unions for $A$, set $B_n=A_n^C$
4. Kolmogorov's countable additivity = finite additivity + continuity

Borel sigma-algebra
1. deal with uncountable sample space, e.g. $\mathbb{R}$
2. Let $\mathcal{F}_i, i\in I$ be the collection of all $\sigma$-algebras that contain all open intervals in $\mathbb{R}$. $\mathcal{B}:= \cap_{i \in I} \mathcal{F}_i$
3. Borel sets: sets in $\mathcal{B}$
4. By properties of $\sigma$-algebra, the followings are Borel sets:
   1. $(a,\infty) = \cup_{i=1}^n (a, n)$
   2. $[a,b] = ((-\infty,a)\cup (b, \infty))^C$
   3. $a = [a,a]$
   4. $\mathbb{N} = \cup \{n\}$

#####

### Lec 3 08/10/26

1. Pre-image: $X^{-1} (B) := {\omega|X(\omega)\in B}$
2. Random Variable is a function
   $$X: \Omega \to \mathbb{R}$$
   s.t. $\forall B\in \mathcal{B}, X^{-1}(B)\subseteq \mathcal{F}$
   1. not all sigma-algebra can give a random variable
   2. Another standard: $\forall x\in R, \{ \omega| X(\omega)\leq x\}\in \mathcal{F}$ which is easier than examining all B ($[x,\infty) is a Borel set$)
3. Distribution
   $${Pr}_X (B) = Pr(X^{-1}(B)) = Pr({\omega|X(\omega)\in B})$$
   1. Identically distributed: $Pr(X\in B)=Pr(Y\in B) \forall B\in \mathcal{B}$
   2. CDF: $F_X(x)=Pr(X\leq x)$

#####

### Lec 4 13/10/26
1. Recap: $(\Omega, \mathcal{F}, Pr)\to^X (\mathbb{R}, \mathcal{B}, P_X)$; r.v. is a function from sample space to $\mathbb{R}$ which is $\mathcal{F}$-measurable
2. Absolutely continuous: $F$ differentiable

#####

### Lec 5 15/10/26
1. $(\Omega, \mathcal{F}, Pr)\to (\mathbb{R}, \mathcal{B}, P_X)$