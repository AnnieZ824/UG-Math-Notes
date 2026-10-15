# MATH40002 Analysis

## Final Revision

### Term 1
#### Write definition in proofs
1. Limit of sequence: $\epsilon-N$
   1. Proof of convergence: start from $x_n<L$, find the condition on $N$ s.t. <\epsilon.
   2. Trick: Rationalise $\sqrt{}$ to get $\frac{C}{N^\alpha}$, put $N$ on the denominator.
2. Subsequences
   1. Idea: $x_n\to L$, $x_{n_k}\to L$
      1. $x_{n_l}\to L, x_{n_m}to M, L\neq M \implies$ divergent
   2. Bolzano-Weierstrass: every bounded sequence has a convergent subsequence
3. Series
   1. Def: series converges if partial sum converges
   2. Test
      1. Necessarily, $a_n\to 0$
      2. Positive series: bounded above to converge
      3. Leibniz Test (alternating)
         1. Condition: positive, decreasing, $a_n\to 0$
         2. Alternating sum $\sum (-1)^n a_n$ converges, $$|S_N-S|\leq a_{N+1}$$
      4. Absolute convergent $\sum |a_n|$ 
         1. ratio / root test: $\left| \frac{a_{n+1}{a_n} \right| / \sqrt[n]{a_n}, L< 1$ convergent, $>1$ divergent
         2. $L=0$ use separate analysis
            1. p-test: $\frac{1}{n^p}$, converges if $p> 1$
            2. Leibniz Test
            3. Comparison Test
   3. Power series: $P(z) = c_n z^n$
      1. Radius of converges: $R:= \sup \{|z|| P(z) \text{ convergent}\}$
      2. $|z|=R$ can't judge, check separately
      3. Trick
         1. Prove for $|z|<1$, $c_n$ is bounded $\implies$ geometric series
         2. Prove $R\geq 1$: prove abs convergent

### Term 2
#### Convexity
1. Def: $f((1-t)a+tb)\leq (1-t)f(a)+tf(b)$. NO second derivatives: some are not differentiable.
2. Prop
   1. For a convex
   
#### Darboux integration