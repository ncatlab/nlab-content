
$X=S^1$ and $Y=S^3$, then $\Sigma^\infty \Omega S^3\approx \mathbb{S}^2\vee \mathbb{S}^4\vee \mathbb{S}^6\vee\cdots $ is very unlike $\Omega \Sigma^\infty S^3\approx \mathbb{S}^2$

$Y=S^{n+1}$, not $Y=S^3$, but it is the same: $\Sigma^\infty\Omega S^{n+1}= \bigvee_{k\geq1} \mathbb{S}^{k n}$ while $\Omega \Sigma^\infty S^{n+1}= \mathbb{S}^n$

Here's how the calculus works in this case. Given a space $X$ there is a "fat diagonal" $\Delta^n X\subseteq X^{\times n}$, which is the subspace whose complement is labelled configurations of $n$ points in $X$.
For a based space $X$ let $X^{(n)}:= X^{\wedge n}/\overline{\Delta}^n X$, the quotient of the smash product by the image of the fat diagonal in the smash product. It has an action of $\Sigma_n$ (which is actually a free action away from the basepoint).
We are interested in $F=\Sigma^\infty \mathrm{Map}_*(X, -)$ a functor from based spaces to spectra. Assume $X$ is a finite CW complex.
There is a tower of functors $\{P_n\}$ under $F$, with $P_0=*$, and such that the fiber of $P_n(Y)\to P_{n-1}(Y)$ is $D_n(Y)=\mathrm{Hom}_{\mathrm{Sp}}(\Sigma^\infty X^{(n)}, \Sigma^\infty Y^{\wedge n})_{h\Sigma _n}$.
Furthermore, the tower converges $F(Y)=\lim_n P_n(Y)$ if $d \lt k$, where $d=$ dimension of $X$ and $k=$ connectivity of $Y$ (which I take to mean: "dimension of the lowest non-trivial homotopy group of $Y$"; though to be honest I'm not entirely sure of the conventions Arone is using here.)
Note that $X^{(n)}$ is $n d$ dimensional, and $Y^{\wedge n}$ is $n k$
connective, so that $D_n(Y)$ is $n(k-d)$-connective.
The map you are interested in is $p_1\colon F(Y)\to P_1(Y)=D_1(Y)$, whose fiber is built by fiber sequences using $D_n(Y)$ for $n\geq 2$, whence the fiber of $p_1$ is $2(k-d)$-connective.
I don't know what there is to say when $d\geq k$. 