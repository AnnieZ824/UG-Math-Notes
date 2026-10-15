\usepackage

# MATH40003 Linear Algebra & Groups

13/02/26 Groups 1

Galois theory: symmetries
Common groups:
- $O_n(\mathbb{R})$: preserve length
- $GL_n$

Symmetries are
- functions: e.g. A $\to$ A
- multiply functions like that
- invertible
- identity

Binary operation \*: $S\times S \to S$
So necessarily, $a*b\in S\forall a, b\in S$
  
(G, \*) is a group if $\exists$ a binary operation $G \times G \to G$
- G1: \* is associative, $a*b*c = a*(b*c)$
- G2: $\exists$ identity e s.t. $\forall g \in G, \exists g*e = e*g = g$
- G3: $\exists$ inverse: $\forall g \in G,\ \exists h \in G\ s.t.\ gh = hg = e$ (hg for h*g)

Fact:
- identity is unique
- inverse is unique

Lemma(goal: cancel by inverse):
- left/right inverse
- inverse of composite

Def
$(G,\cdot)$ is abelian (or commutative) if $ab = ba\ \forall a,b \in G$
e.g. $(\mathbb{Z},+)$
Subgroup
Cyclic group
    For multiplications: $U_n = \{g\mid g^n = 1, n\in \mathbb{Z}\}$
Sym(X) is the permutations of X

## Final Revision
### 1st Term
#### 1. Vector Space
   1. Def: $(V,+), (V,\cdot)$ commutative groups
     1. Associativity: $ (u+v)+w = u+ (v+w)$
     1. $\exists$ identity
     2. $\exists$ inverse
     3. Commutative: $u+v=v+u$
#### 2. Subspaces
   1. Def: $W\subset V$ if 
      1. $\mathbf{0}\in W$
      2. Closure under +
      3. Closure under scalar product
   2. Prop: $U,W\subset V\rightarrow U\cup W, U+W \subset V$, but $U\cup W \nsubseteq V$ in general
#### 3. Gaussian Elimination
#### 4. Finite Dimensional
   1. Def: $V$ is f.d. if $\exists$ a $\textbf{finite spanning subset } W$ (finite basis)
   2. Prop:
      1. Bases same size; max linearly independent set / Min spanning set -- Basis.
      2. (Linearly independent / spanning) + (size = $\text{dim} V$) $\to $ Basis; $|X| = n \rightarrow$ (lin. ind. $\iff$ spanning)
      3. $U,W$ are subspaces and $U\subset W$, $\text{dim} U \leq \text{dim}W$
      4. Uniqueness of expansion in basis: lin. ind. at most 1 expression; spanning at least; basis exactly
      5. $\text{dim}(U+W) = \text{dim}U+\text{dim}W-\text{dim}(U\cap W)$
      6. Rows of AB are linear combinations of rows of B, so $\text{rowspace}(AB)\subset \text{rowspace}(B)$ (extreme case: there is a 0 col in AB, and B are formed by a basis, so a row in B is not used)
      7. $\text{rk}(A)=\text{dim rowspace}(A)=\text{dim colspace}(A)=\# \text{ pivots in ref}$
      8. Rank-nullity: $\text{M}_{m,n}(F), \text{rk}(A)+\text{dim ker}(A)=n, \text{rk}(A)+\text{dim LNS}(A)=m$, LNS for left null space
      9. Invertibility: for an $n\times n$ square matrix, $\exists$ left inverse $\iff$ right inverse $\iff$ invertible $\iff \text{rk}=n$
1.  Linear Transformations
    1.  Def
        1.  Addition & scalar product.
        2.  (Linear) Isomorphism: a linear map is $\text{bijective}; if $T$ is an isomorphism, $T^{-1}$ is also linear.
        3.  Change-of-basis Matrix: $B[I]_{B'}$, writing source basis $B'$, in forms of  target basis $B$. $v_i'=a_{1i}v_1 + ... + a_{ni}v_n$, $B[I]_{B'}=A_ij$
    2.  Idea
        1.  To study the behaviour of vectors in a vector space, look at the behaviour of bases.
        2.  $T$: Vector space $V$ -- $F^m$ in basis $B$ -$(CT_B)$- $F^n$ in basis $C$ -- vector space $W$; 
            1.  $[Tv]_C = C[T]_B [v]_B$
            2.  Composition: $$D[T\cdot S]_B = D[T]_C C[S]_B$$
        3.  To consider a linear transformation, examine the domain
        4.  Change of Basis
            1.  Writing source basis in terms of target basis - change-of-basis matrix
                e.g. $B'
            2.  Formula: $C'[T]_B' = C'[I]_C C[T]_B B[I]_{B'}$, let $Q=C[I]_{C'}, P=B[I]_{B'}$, then $$C'[T]_B' = Q^{-1} C[T]_B P$$
            3.  If $P=B[I]_{B'}$, then $P^{-1}= B'[I]_B$
            4.  Steps
                1.  Begin with $E[T]_E$
                2.  Composite with change-of-basis matrix to obtain, for instance, $C[T]_B$
        5.  Rank
            1.  $\text{rk }T:=\text{dim(im}(T))$, $\text{im}T = \text{colspace}T$
        6.  Dual Vector Space (not important)
            1.  Def
                1.  $V^* := {T: V\to F\text{ linear}}$, space of mappings
                2.  Dual Transformation (mapping between functions): $T^* : W^*\to V^*, T^*(f):=f\circ T$
                3.  Double Dual Subspace: $\iota : V\to (V^*)^*, v \mapsto \iota_{v}, \iota_{}(f) = f(v)$, insert specific value into mappings.
            2.  Prop
                1.  Composition: $(TS)^* = S^* T^*$
                2.  Basis of $V^* := v_i^\vee(\lambda_1 v_1 + ... + \lambda_n v_n) = \lambda_i$, if $v_i$ is any basis of $V$, i.e. $$v_i^\vee(v_j) = \delta_{ij} := 
                    \begin{cases}
                        1, i = j\\
                        0, i\neq j
                    \end{cases}
                    $$
                3.  $\iota$ is an isomorphism, due to basis + dimension.



### 2nd Term
#### Part 1: LA
1. Change-of-basis: $B[\phi]_B([\phi]_B) \to C[T]_C([\phi]_C)$
   1. $[v]_C = C[I]_B [v]_B$, $C[I]_B$ writes bases B in terms of bases C
   2. Let $P=C[I]_B$. $$[\phi]_C = P[\phi]_B P^{-1}$$
2. Determinants
   1. Expansion along a row / col, $(-1)^{i+j}$
   2. Operations
      1. Taking out factors in a row
      2. Linearity on rows
      3. Identical rows: $\text{det }A = 0$
      4. Row ops
      5. Product
   3. $\text{det }A \neq 0 \iff invertible \iff non-singular \iff lin. ind. rows \iff ~I$
   4. Invert matrices: $A^{-1} = \frac{1}{\text{det }A}adj{A}$, the adjugate of $A$, transpose of cofactors.
   5. Cramer's rule (solve for $Ax=b$): $$x_i = \frac{\det A_i}{\det A}$$, $A_i$ substitutes the $i-\text{th}$ col of $A$ by $b$.
   6. Determinants of linear transformations do not depend on bases.
3. Eigenvalues & Eigenspaces
   1. To find
      1. Solve for $\det (A-\lambda I)=0$, obtain $\lambda_i$
      2. Solve $v$ for $(A-\lambda_i I)v = 0$ by Gaussian, eigenspace $E_i = \text{Span}(v) \forall v$ corresponds to this $\lambda_i$
      3. Diagonalisable?
         1. all $v_i$ compose a basis of the vector space, i.e. $v_i$ lin. ind.
         2. OR $\sum |E_i| = |V|$
         3. OR $n$ distincts eigenvalues
   2. Gram-Schmidt Process: for any basis, to create a new orthonormal basis, minus $$\sum^n\text{proj}_{v_{n+1}} w_i$$, where $\text{proj}_\mathbf{b}\mathbf{a} = \frac{\mathbf{a\cdot b}}{||\mathbf{b}||}\cdot\mathbf{\frac{b}{||b||}}$
   3. Symmetric -> Diagonalisable

#### Part 2: GT

1. Groups and Subgroups
   1. Def
      1. Group $(G,*)$
         1. $G0$: Closure - $g,k\in G, g*k\in G$ (Binary op - $S\times S\to S$)
         2. $G1$: \* is associative, $a*b*c = a*(b*c)$
         3. $G2$: exists identity $e\in G$ s.t. $\forall g \in G, \exists g*e = e*g = g$
         4. $G3$: exists inverses: $\forall g \in G,\ \exists h \in G\ s.t.\ gh = hg = e$
      2. Abelian: commutative
      3. Symmetric Group, 
         1. e.g. $$\begin{pmatrix}
            1 & 2 & 3 & 4\\
            2 & 4 & 1 & 3
            \end{pmatrix}$$
            Numbers represent the content, e.g. $\alpha(2)=4$
          2. $(\text{Sym}(X)(all permutations of set $X$),\circ) is a group
          3. $|S_n| = n!$
       4. Finite Group: $G$ finite $(\implies l\neq m, g^l = g^m)$; order of group:= $|G|$
       5. Subgroup $H\leq G$
          1. $H\subset G$ is a group
          2. Test $H\subset G$
             1. $H\neq \emptyset$
             2. Closure under group op
             3. Closure under inverses
          3. Cyclic Subgroup generated by $g$, $\lang g\rang := \{g^m| m\in \mathbb{Z}\}$
       6. Cyclic Group:= $\lang g\rang = G$, g is a generator
          1. $g$ finite order: $\exists n\in \mathbb{N},g^n = e$. Least $n = \text{ord}(g)$
          2. Modulo: $g^l = g^m \iff n|(l-m)$; negative $\to$ positive powers
          3. $\text{ord}(n) = |\lang g\rang|$
          4. If $G$ finite
             1. $\forall g\in G, \text{ord}(g)$ finite
             2. $H\subset G \land$ closure under group op (inverse: met by modulo, neg to pos power)
          5. If $G$ cyclic
             1. $H\leq G \implies H$ cyclic
             2. Order = n, $m\in \mathbb{Z},$d= \gcd(m,n)$
                $$\implies \lang g^m\rang = \lang g^d\rang, 
          6. Idea
             1. Division algorithm
             2. Modulo (period)
             3. Bezout thm: $d = \gcd(m, n)\implies \exists k,l\in \mathbb{N}, d= km+ln$
             4. To prove $\lang g\rang = \lang h\rang$, $\implies g\in \lang h\rang$, vice versa

#### Past Paper 2025 MJ
1. Permutation
   1. Order: # rounds it takes to back to the original state, lcm of the size of disjoint cycles
   2. Disjoint cycles: abelian; joint: non

### Revision Class 1
1. $C[T]_B: Tv_i = a_{1i}w_1 + ... + a_{mj}w_m$
2. Basis
3. Dimension := size of basis
   1. independent of the choice of basis
   2. f.d.: basis of finite size
4. Rank-nullity: $T: V\to W$
   1. $\text{dim }V = \text{rk }T + \text{ker }T$
5. Subspace 
   1. e.g. kernal, image, $U+W, U\cup W$
   2. formula for dimension of $U+W$
6. Field
   1. $\mathbb{Z}\to F$, sum of "1"s
7. Invertibility
   1. equivalent: rk, det, ~ $I$
   2. $F=\mathbb{F}_3, \text{det}(A)=3$, not invertible; $\pm 1$ is non-zero in every field

### Revision Class 2
1. Coset
   1. def: $gH := \{gh | h\in H\}$
   2. $H\leq G, |G: H| := $# distinct cosets - {cosets of H}???
   3. Thm (Lagrange): $|G| = |H||G:H|$
   4. Q: Finding isomorphism
   5. Dihedral group: group of symmetry
2. Determinants
   1. computations
   2. laplace expansion
   3. row reduction (swap, scale, addition)
3. Cramer's rules (2*2)
4. Eigenvalues, eigenvectors
   1. Find $\chi_A$
   2. Find eigenspaces
   3. Solve linear recurrence
   4. Compute power and roots of matrices
5. Orthogonal vectors and matrices
   1. Gram-Schmidt
   2. Spectral thm: real symm matrix, diagonalisable with orthogonal 
   3. Inner product and properties ???
6. Group
   1. def
      1. group
      2. subgroup
      3. homomorphism
      4. isomorphism
   2. e.g.
      1. cyclic: $(\mathbb{Z},+), \infty$
      2. symm
      3. Inv. matrices $\text{GL_n}(F)$
      4. mult group of a field: $F^\times$, excluding 0
   3. Subgroups
   4. Coset
      1. Lagrange

