# Knot Theory

## Session 1

### Recap
1. Knot: an embedding of a circle in $\mathbb{R}^3$
2. Link: an embedding of two or more circles in $\mathbb{R}^3$
3. Ambient Isotropy: equivalent under Reidemeister moves
4. Reidemeister move
   1. twist
   2. poke: 2 parallel strands, bend one under another
   3. slide (under a crossing)

left-handed: over strand right-down to left-up

### Building knots
1. Mirror knots: reflect, $m(K)$
2. Amphichiral: $K \neq m(K)$, otherwise chiral
3. Oriented knots
   1. over / under-crossing along direction of arrow
4. Reverse knots
   1. Reverse knot $K^{-1}$: change orientation
   2. Invertibility: $K$ equivalent to $K^{-1}$
5. Knot composition $\#$
   1. Def
      1. cut 2 oriented knots
      2. composed with corresponding orientation
      3. no new crossings introduced
      4. prime: cannot be composed of non-trivial oriented knots
   2. Properties (integer multiplication)
      1. commutative
      2. associative
      3. identity
      4. NO inverses: unknot is prime
      5. Prime factorisation of knots
6. Alternating knots: over & under-crossings alternates as traveling along a knot in a fixed direction
   1. e.g. trefoil going twice
   2. cannot twist or poke preserving alternative

### Notations of knots   
1. Gauss notation (not useful)
   1. give a number for each crossing
   2. start from the top, anti-clockwise, + over-crossing, - under-crossing
2. Dowker-Thistlethwaites (drow the graph with numbers)
   1. double marking crossings along the knot, write down even numbers corresponds to 1357...
   2. $+$ if even is over-crossing
   3. all + if alternating
3. Alexander-Briggs
   1. Determine crossing numbers
   2. Underscore knots under each crossing number
4. Conway: tangles (most useful)
   1. Tangle: a region of knot / link projection s.t. exactly 4 strands cross the boundary, denote as NW, SW, NE, SE
   2. over-strand goes up: + (positive gradient)
   3. Join north / south strands
   4. Compose
      1. start from a plain region e.g. +2
      2. reflect the graph (not the knot) over $y=-x$
      3. shift the original to the left, compose with another region
   5. Continued fraction: denominator contains the sum of another fraction (infinite or finite)
      1. $a_1 + \frac{1}{a_2 + \frac{1}{a_3 + ...}}$
      2. same tangle same continued fraction

### Counting knots
1. Tait's Menage Problem
2. Crossing numbers $c(K)$: min # of crossings in any projection of $K$
3. Thm: reduced (no simplifications under I and II) alternating projection with n crossings, $c(K)=n$


Useful: search knot atlas