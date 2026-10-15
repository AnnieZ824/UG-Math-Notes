# MATH40005-Prob-Stats

13/02/26

PS3 Q3(c)
$G(X)\mathbb{I}(X>m) >= -(a-m)\mathbb{I}(X>m)$
$E(G(X)\mathbb{I}(X>m)) >= E(-(a-m)\mathbb{I}(X>m))$

Unbiased Estimator
$s^2 = 1/n \sum

## Final Revision

### 2025 MJ
#### Q1
1. $\sigma$-algebra guarantees $P(A^C)=1-P(A)$ by closure under complement and $P(\cup  A_i)=\sum P(A_i)$ by closure under finite unions.
2. *Visualisation of data: bar chart (discrete, nominal), pie chart (ratio), histogram (continuous, frequency or density), 
3. *Skewness: 
4. Median: $F_X(m) = \frac{1}{2}$

#### Q2
1. Discrete distribution
   1. Bernoulli: toss a coin, 1 and 0 are the only results.
        $$X~Bern(p):\ P(X=1)=p,P(X=0)=1-p.$$
   2. Binomial: toss several coins.
        $$X=\sum_{i=1}^n X_i, X_i\text{ are independent, conforms to Bernoulli with identical coefficient }.$$
        $$P(X=k) = \begin{pmatrix}
                    n\\
                    k
                    \end{pmatrix}
        p^k (1-p)^(n-k).$$
   3. Poisson: DISCRETE, rare cases, many trials(e.g. time: continuous), fixed $\lambda = np, \text{:=frequency per unit time}$.
        The number of trials per unit time (could be another fixed period, where $np=\lambda t$).
        $$P(X=k)=\frac{\lambda^k}{k!}e^{-\lambda}.$$
   4. Exponential: CTS, the time between two consecutive trials.
        $$P(X=k) = 1-e^{\lambda t}.$$
        Memoryless (the past doesn't affect the future)
     5. Bayes' Rule
        1. assumption, denote
        2. LTP
     6. Permutations: locate + arrange
     7. pdf
        1. non-negative
        2. =1
     8. mgf
        1. uniqueness

1. bayes
2. ltp
3. def
   1. exp
   2. var
   3. mgf, pgf
4. calculations
   1. exp: linearity
   2. var (a property, square)
   3. lotus
5.  likelihood
6.  regression
   