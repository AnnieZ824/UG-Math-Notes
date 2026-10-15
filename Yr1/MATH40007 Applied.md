# MATH40007-Applied
11/02/26

VI = dissipation in the conductor 
$\epsilon (x) :=$ Sum of dissipation in all conductors $= e \cdot w = (-Ax)^T (-CAx) = x^T K x$
Recall: $Kx=f$
$$
\begin{pmatrix}
P & Q^T \\
Q & R
\end{pmatrix}
$$
effective conductance
Dirichlet's Principle: & KCL all others
Thomson's Principle: any w with unit current divergence at + node and -unit current divergence at - node & KCL at all other nodes, $\min\{\epsilon(w)\} = \min\{\sum{w_i^2}\} = C_{eff}$
#额没听懂，我要回去再听一下
Thomson: minimising loops; Dirichlet: minimising ?

18/02/26

$$S_4 =
\begin{pmatrix}
    0&1&0&0\\
    0&0&1&0\\
    0&0&0&1\\
    1&0&0&0
\end{pmatrix}$$
$S_4$ commutes, $S_4^4 = I_4$
Assume $\lambda$ is an eigenvalue of $P$
$$Px = \lambda x\\
QPx = \lambda Qx\\
P(Qx) = \lambda Qx$$
,which means $Qx$ is also an eigenvector of $P$
$P,Q$ commutes $\equiv dim(E_i)$ 

## 1 Incidence matrix
### 1.1 Def
- $m\times n$: $m$ edges, $n$ nodes
- $\forall$ edges, $+1$ starting point, $-1$ ending point
### 1.2 Property
- $\ker(A) = \# connected components$
- $LNS(A) = \# independent loops$
- Calculations with rank-nullity theorem

## 2 Resistive Circuit Theory
### 2.1 Def
$x$: potentials at nodes
$w_a$: net fluxes in edges
$f_I$: net divergence of currents at nodes
$A$: incidence matrix, representing the directed graph
$K$: (weighted) Laplacian matrix, $K = A^T (C) A$
- $K\in M_{n,n}(\mathbb{R})$, symmetric (det = 0)
- unweighted: $K = D - W$, $D$ is the degree matrix s.t. $D_ii$ =\#degree of node $i$, W is the adjacency matrix with $W_ij$ = \#edges connected between node $i$ and $j$
- weighted: 
- ? unable to represent a node connecting to itself
### 2.2 Formulae:
- Ohm's Law: $w_a = -c_a(x_j-x_i)$, a is the edge from node i to j, $w = -CAx$
- $f_I = -A^T w$ ($A^T$ sends edge fluxes to each node, with +1 leaving, -1 entering the node, so $A^T w$ is the net convergence, i.e. the external currents entering the circuit) $\mathbf{\to f_I = Kx}$
- KCL: net divergence = 0 if no external currents $\mathbf{\to f_i = 0}$
- More generally, $\sum{f_i}=0$, since $\mathbf{f}$ lies in the row space of $A$ which is perpendicular to the right null space, so $\mathbf{x_o f=0}$
### 2.3 Problems:
#### 2.3.1 The Neumann Problem (two-point)
Condition: 
- $\mathbf{f}=(+1,-1,0,...,0)$
- Known $\mathbf{f}$, find $\mathbf{x}$
- $Kx=f, rank(K)=rank(A)$

Method: $\mathbf{Grounding\ a\ node}$
- set $x_1 = 0$, eliminate 1 deg of freedom
- solve for $\mathbf{\hat x = \hat K^{-1} \hat f}$
#### 2.3.2 Dirichlet Problem (two-point, variant)
Condition:
- $x_1 = 1, x_2$ grounded
- $\mathbf{f} = (f,-f,0,...,0)$

Method: the Schur Complement
$$K=
\begin{pmatrix}
P & Q^T \\
Q & R
\end{pmatrix}
$$, $R$ is invertible. Let $b=|\text{boundary nodes}|, P\in \mathbb{R^{b\times b}}$ (can be grounded first, $(b-1)\times (b-1)$. So we have
$$
\mathbf{Kx=f} \iff
\begin{pmatrix}
P & Q^T \\
Q & R
\end{pmatrix}
\begin{pmatrix}
\hat e \\
\hat x
\end{pmatrix}
= \begin{pmatrix}
\hat f \\
\mathbf{0}
\end{pmatrix}
$$
,where
$$
\mathbf{\hat e} =
\begin{pmatrix}
1\\
0
\end{pmatrix},
\mathbf{\hat x} = 
\begin{pmatrix}
x_3\\
x_4\\
...\\
x_n
\end{pmatrix},
\mathbf{f}=
\begin{pmatrix}
f\\
-f
\end{pmatrix}. \\
$$
Solve for $\hat x$ and $\hat f$
$$
\mathbf{P\hat e+Q^T\hat x=\hat f} \\
\mathbf{Q\hat e+R\hat x=0} \\
\mathbf{\hat x = -R^{-1}Q\hat e} \\
\mathbf{\hat f = -P\hat e+Q^T R^{-1} Q\hat e = (Q^T R^{-1}Q-P)\hat e}
$$
#### 2.3.3 Effective Conductance
Def: net current flow between + and - (grounded) node with unit voltage drop
Method: set 
$$
\mathbf{x}=
\begin{pmatrix}
1\\
\phi_2\\
\dots\\
0
\end{pmatrix}
$$
and
$$
\mathbf{f}=
\begin{pmatrix}
C_{eff}\\
0\\
\dots\\
-C_{eff}
\end{pmatrix}
$$,
solve for $\mathbf{f=Kx}$
Conclusions:
- In parallel: sum
- In series: harmonic sum