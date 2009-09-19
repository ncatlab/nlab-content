#Idea#

The classical  _Moore path category_ of a [[topological space]] $X$ is a variant on the usual space of paths $I \to X$, but one which yields a strict category. 

#Definition#

Let $X$ be a [[topological space]]. Its **Moore path category** $M(X)$ has

* $Obj(M(X)) = X$

* Its set of all morphisms consists of pairs $a=(f,r)$ where $f:[0, \infty) \to X$ is continuous, $r \geq 0$ and $f$ is constant on $[r, \infty)$. The source of $a$ is $f(0)$ and the target of $a$ is $f(r)$. The number may be called the _shape_ of $a$. We may compose $a=(f,r)$ and $b=(g,s)$ to obtain $a \circ b= (h,r+s)$ where $h(t)= f(t)$ for $ t \leq r$ and $h(t) = g(t-r)$ for $t \geq r$. Identities are paths of shape $0$. 

The advantage of this definition as pairs is partly in giving a topology on $M(X)$, but also  in iteration. 

The reference below defines $M_*(X)$ as a strict cubical $\omega$-category. It also has connections, which satisfy all the laws except cancellation of $\Gamma^-_i$ and $\Gamma^+_i$ under composition. This structure seems a sensible home for $n$-paths in $X$ for all $n \geq 0$, and has the advantage  over simplicial or globular versions of "$\infty$-groupoids" of easily encompassing multiple compositions. 

##Reference##

* R. Brown, Moore hyperrectangles on a space form a strict cubical omega-category, arXiv 0909.2212v2 

