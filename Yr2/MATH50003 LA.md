Lec 1 02/10/26

Three canonical forms
1. Similarity of matrices:
$$ B = P^{-1}AP $$
We write $A~B$
2. Diagonalisability: similar to a diagonal matrix
3. Triangularisation thm: can reduce an $n\times n$ matrix to an upper triangle (induction)
4. Jordan Canonical Form
   1. Jordan Blocks: $n\times n$
    $$ \begin{pmatrix}
    \lambda & 1 & 0 &\cdots & 0\\
    0 & \lambda & 1 & \cdots & 0\\
    \vdots & & \ddots & & \vdots \\
    0 & \cdots & \cdots & 0 & \lambda
    \end{pmatrix}
    $$
    2. Use JCF to find powers of non-diagonalisable matrices more easily, e.g. $A^k = P J^k P^{-1}$
    3. $J=$
    $$
    \begin{pmatrix}
    J_{m_1}(\lambda_1) & 0 & \cdots\\
    0 & J_{m_2}(\lambda_2) & \cdots\\
    \vdots & \ddots & \vdots\\
    0 & \cdots & J_{m_r}(\lambda_r)
    \end{pmatrix}$$
    4. Size of $J_m$: power of $\lambda_i$ in the char function, i.e. algebraic multiplicity; $r$: geometric multiplicity, i.e. $\dim \ker (A-\lambda_i)$, or $\dim E_i$
    5. JCF is unique
5. Companion matrix
6. Rational canonical form

- Matrix $[T]_B$ diagonal $\iff B$ consists of eigenvectors
- $V$ is over $\mathbb{C} \implies$ there always is $\lambda \in \mathbb{C}$
- $a(\lambda)$ the multiple of $\lambda$ as root of $p_T$
- $g(\lambda) := \dim E_{\lambda}$

#####

### Lec 2 

$p_T(x)=p(x)=\prod (x-\lambda_i)^{a(\lambda_i)}$
TFAE
1. $T$ diagonalisable
2. $\sum g(\lambda_i)=n$
3. $g(\lambda_i)=a(\lambda_i)$
Proof:
1. 2$\iff$3: $g(\lambda_i)\leq a(\lambda_i)$
2. 1 $\implies$ 2: Eigenspaces not intersect (by contradiction)
3. 2 $\implies$ 1

Diagonalisability test
1. Find $p_A$
2. Calculate $g(\lambda_i) = \dim E_{\lambda_i}$
3. If $\exists i$ s.t. $g(\lambda_i)\neq a(\lambda_i)$, NOT diagonalisable

Direct sum of subspaces
1. $U_1, U_2\leq V, U_1+U_2:=\{u_1+u_2|u_1\in U_1, u_2\in U_2\}$ is a subspace
2. dimension formula: $\dim (U_1+U_2) = \dim U_1 +\dim U_2 -\dim (U_1\cap U_2)$
3. Def Direct sum: $V=V_1\oplus V_2$ when 
   $$V = V_1 + V_2 \text{ and } \forall v\in V, \exists \text{ a unique way of writing } v=v_1+v_2, v_i\in V_i$$
4. Prop 4.2: $V_1, V_2\leq V$ TFAE
   1. $V=V_1\oplus V_2$
   2. $V_1\cap V_2 = \{0\} \land \dim V_1+\dim V_2 = \dim V$
   3. Proof
      1. 1 $\implies$ 2
         1. counterexample 0, uniqueness of expression
         2. formula
      2. 2 $\implies$ 1: formula implies the same vector space, contradiction implies uniqueness
5. Prop 4.3: $V_1, ..., V_k\leq V$, TFAE
   1. $V=\oplus V_i$
   2. $\dim V=\sum \dim V_i, B:=\cup B_i$ is a basis of $V$
   3. Proof
      1. 1 $\implies$ 2
         1. $B$ spans $V$, i.e. $\forall v\in V$, there is an expression of $v$ in terms of $B$. Prove by definition of direct sum and $B_i$ spans $V_i$.
         2. Property of direct sum: $0 = 0 + ... + 0$ is the unique expression.
         3. Lin ind by contradiction. Assume there is a linear dependency. Group by $B_i$. $0=\sum_{a\in B_1} \alpha_a a+ ... + \sum_{z\in B_k} \alpha_z z$
         4. By Prop 4.2 $B_i\cap B_j = \empty$, so $\dim B = |B| = \sum |B_i| = \sum \dim B_i$
      2. 2 $\implies$ 1
         1. Basis implies $\dim V = |B|$, so $|\cup B_i| = \sum |B_i|, B_i$ disjoint. 
         2. Uniqueness prove by contradiction. (No need to break down to every element in $B$)
   4. Insight: to prove direction sum
      1. check dimension sum
      2. check basis: write in a matrix, find det or check invertibility. If $\det \neq 0$ or invertible, $B$ is a basis.
6. Prop 4.6: $T$-invariant $\implies$ block diagonal.
   1. Def: $T: V\to V$, if $T(W)\subseteq W$, define $T_W: W\to W$ as the matrix of restriction.
   2. $T: V\to V, V = \oplus_{i=1}^k V_i, V_i$ are $T$-invariant. $A_i:= [T_{V_i}]_{B_i}$, then $[T]_B$ can be written in the block-diagonal form in $A_i$, i.e.
      $$[T]_B = \begin{pmatrix}
      A_1 & 0 & \cdots & 0\\
      0 & A_2 & \cdots & 0\\
      \vdots & \vdots & \ddots & \vdots \\
      0 & \cdots & 0 & A_k
      \end{pmatrix}$$
   3. Proof: write $T(v_i)$ in $B_1, v_i\in B_1$ gives a matrix $(a_{ij})$ which is $[T_{V_1}]_{B_1}$

######

### Lec 3 09/10/26

1. Quotient space
   1. Vectors in quotient space are cosets: $W+v:=\{w+v: w\in W\}$. Two cosets $W+v_1 = W + v_2 \iff v_1-v_2\in W$
   2. To define a vector space, define the operations
      1. $W+v_1 + W+v_2 = W + (v_1+v_2)$
      2. $\lambda (W+v_1) = W + \lambda v$
      3. Check well-definedness (different expressions of cosets give same results in operations)
   3. Axioms of a vector space
      1. Addition: abelian group with identity element
         1. closure
         2. commutative
         3. associative
         4. identity
         5. inverse
      2. scalar multiplication
         1. closure
         2. distributive (vector/scalar) $\lambda (v+u), \lambda \mu v$
         3. associative
         4. identity
   4. dimension $\dim V/W = \dim V - \dim W$
      1. extend basis of $W: \{ w_1, \cdot , w_r\}$ to basis of $V: \{w_1, \cdots, w_r, v_1, \cdots, v_s\}$. Show that $W+v_i$ is a basis of $V/W$.
2. Quotient spaces and linear maps
   1. Quotient map: $\bar T : V/W\to V/W, \bar T (W+v) = W + \bar T(v)$; $B_W$ is a basis of $W$, extend it to basis of $V$ then the rest $\bar B$ is a basis of $V/W$
   2. Prop 5.4
      1. $X:= [T_W]_{B_W}, Y:=[\bar T]_{\bar B}$, then
         $$[T]_B = \begin{pmatrix}
         X & Z\\
         0 & Y
         \end{pmatrix}$$

#####

### Lec 4 
1. Proof of prop 5.4
   1. plug in $T(w_i) = T_W (w_i) = \sum x_{ji} w_j$. The matrix $X = (x_{ji})$.
   2. $T(v_i) = \sum z_{ji} w_j + \sum y_{ji} v_j$, so $\bar T(W + v_i) = W + T(v_i) = W + \sum y_{ji} v_j
   3. e.g. When finding $[T]_B$, plug in basis into transformations, write in forms of $B_W, \bar B$ respectively.
2. Cor 5.6 (char function, product): 
   1. $T: V\to V, T$-invariant $W\leq V$. Suppose $c, c_1, c_2$ are teh char poly of $T, T_W, \bar T$ respectively. Then
      $$ c = c_1\cdot c_2
   2. Proof:
      1. $A:=[T]_B, c(x) = \det (xI_n - A) = \det (xI_n - X)\det (xI_n - Y) = c_1 (x)c_2(x)$
3. Triangularisation
   1. Prop 6.1: $A,B$ upper-triangular
      $$A = \begin{pmatrix}
      \lambda_1 & & * \\
       & \ddots &  \\
      0 & & {\lambda}_n
      \end{pmatrix},
      B = \begin{pmatrix}
      \mu_1 & & * \\
       & \ddots & \\
      0 & & {\mu}_n
      \end{pmatrix}$$
      then the eigenvalues of $A$ are $\lambda_i$; $c_A(x) = \prod (x-\lambda_i)$; $\det (A) = \prod \lambda_i$; $AB$ is upper-triangular with diagonal entries $\lambda_i \mu_i$
   2. Thm 6.2 (Triangularisation Thm, converse of 6.1, transformation)
      1. $T: V\to V, V = F^n$. If $c_T(x) = \prod (x-\lambda_i)$ (linear products) then there exists a basis $B$ s.t. $[T]_B$ is upper-triangular.
      2. Proof: induction on the dimension of $V$.
         1. $n = 1$, obvious
         2. Assume when $\dim V = n-1$ the statement holds. 
         3. For $\dim V = n$ with characteristic function in linear products, $\exists \lambda \in F$ s.t. $T(w) = \lambda w. W:= \text{Span}(w), V/W = W+v, \bar T$ the quotient map. By prop 5.4, $$[T]_B = \begin{pmatrix}
            \lambda & Z\\
            0 & [\bar T]_{\bar B}
            \end{pmatrix}. $$
            By Cor 5.6, $c_{\bar T}|c_T$ is in the form of linear products.
            Since $[\bar T]_{\bar B}$ is $(n-1)$-dimensional whose characteristic function is in the form of linear products, by assumption $\exists \bar B'$ s.t. $[\bar T]_{\bar B'}$ is upper-triangular.
            Hence by prop 5.4 $\exists B'$ s.t. $$[T]_B' = \begin{pmatrix}
            \lambda & Z\\
            0 & [\bar T]_{\bar B'}
            \end{pmatrix} $$ which is upper-triangular.
   3. Cor 6.3 (converse matrix form): $A\in M_{n\times n}(\mathcal{F})$ factorises in linear factors, then $A$ is similar to an upper-triangular matrix.
      1. Proof: let $V = F^n$ and apply Thm 6.2 to the linear map given by $T(v) = Av$.
      2. Algorithm to triangularise: find eigenvector $w_1, W + w_1, \cdots$ of $T, W + w_1, \cdots$ until obtain $B=\{w_1, \cdots, w_n\}$, then $[T]_B$ is upper-triangular. (particularly, find $P$ s.t. $A = P T P^{-1}$ is upper-triangular)

### Lec 16/10/26
Cayley-Hamilton
1. Def: char poly of transformations/matrix, $p(T) = \sum a_i T^i$
2. Thm: $A\in M_{n\times n}(F), p_A(A) =0$
   1. Proof
      1. diagonal matrix
      2. triangularisable over $\mathbb{C}$
      3. Other: strong induction, discussed by invariant subspace