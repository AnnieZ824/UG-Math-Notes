Lec 1 01/10/26

1. Triple scalar product: $a\cdot (b\times c) = (a\times b)\cdot c$
2. Triple vector product: $a\times (b\times c) = (a\cdot c)b - (a\cdot b)c$

Lec 2 06/10/26

1. Directional derivative along $\hat s$ (prepare: break down to x,y,z)
   1. $\frac{\delta \phi}{\delta s} = \frac{\delta \phi}{\delta n}<\hat n, \hat s>$, $\hat n$ is the direction of the normal
   2. Gradient (grad)
      1. $\nabla \phi = \frac{\delta \phi}{\delta n}\hat s$
      2. Cartesian (substitute i,j,k): 
         $$\nabla \phi= \frac{\delta \phi}{\delta x}\mathbf{i} + \frac{\delta \phi}{\delta y}\mathbf{j} + \frac{\delta\phi}{\delta z}\mathbf{k}$$
         substitute $\phi$ by the original point, $\hat s$ by the direction
      3. Cylindrical: 
         $$ \nabla \phi = \frac{\delta \phi}{\delta r} \mathbf{\hat r} + \frac{\delta \phi}{\delta \theta} \frac{\mathbf{\hat \theta}}{r} + \frac{\delta \phi}{\delta z} $$
         derived from:
         1. Def of $r$: $\mathbf{\hat r \times i} = i\cos{\theta} \cdot i + j\sin{\theta} \cdot i = \cos{\theta}, r = \sqrt{x^2 + y^2}, \theta = \arctan {\frac{y}{x}}$, ...
         2. Multivariate partial derivative chain rule: $\frac{\delta \phi}{\delta x} = \frac{\delta \phi}{\delta r}\frac{\delta r}{\delta x} + \frac{\delta \phi}{\delta \theta}\frac{\delta \theta}{\delta x}$
         3. Implicit partial derivative: 
            $$\begin{align}
            \frac{\delta \theta}{\delta x} &= \frac{\delta}{\delta x}(\arctan {\frac{y}{x}})\\
            &= \frac{1}{1+\left( \frac{y}{x} \right) ^2} \frac{\delta}{\delta x}\left( \frac{y}{x} \right)\\
            &= \frac{-y}{x^2 + y^2}\\
            &= -\frac{\sin{\theta}}{r}
            \end{align}$$
      4. $\nabla = \frac{\delta}{\delta x} + \frac{\delta}{\delta y} + \frac{\delta}{\delta z}$

Lec 3 08/10/26

1. Find the tangent plane
   1. $x_P, y_P, z_P$
   2. choose constant $\phi$ by rearranging the equation
   3. calculate $\nabla \phi$
   4. substitute $x_P, …$
   5. write the equation of the tangent plane:$\mathbf{r-r_P}(\nabla \phi)_P=0$
      1. In the form of $Ax+By+Cz=d$
      2. Get the normal of the surface $(A,B,C)$
2. Divergence, curl
   1. $\mathbf{A}$ is a vector function of position with continuous partial derivatives (vector field)
   2. Divergence(scalar): $\div \mathbf{A} = \nabla \cdot \mathbf{A}=\frac{\delta A_1}{\delta x} + ...$
      1. div=0: solenoidal
   3. Curl(vector): $\curl \mathbf{A} = \nabla \times \mathbf{A}$
      1. zero curl: irrotational
      2. related to rotation: global/microscopic
   4. N.B. not commute, $A_1\frac{\delta}{\delta x}\neq \frac{\delta A_1}{\delta x}$ which is a scalar operator

