### Gauge fixing ###

In the [[Quantization as a Kan Extension|Freed and Alm-Schreiber approach to quantization]], the action is a functor 
$$
e^{iS}:X \to nVect,
$$ 
where $X$ is some $(\infty,n)$-groupoid called the _space of fields_. The space of fields comes equipped with a projection $\pi:X\to M$ to an $(\infty,n)$-groupoid $M$ called the _moduli space_ of the quantum theory. Then the (path integral) quantization is, if it exists, the [[Kan extension]] $Z:M\to nVect$ of $e^{iS}$ along $\pi$. The functor $Z$ is customary called the _partition function_ of the theory. 

A **gauge fixing** is a choice of a subgroupoid $X_{gf}$ of $X$ such that the inclusion $X_{gf}\hookrightarrow X$ is an equivalence. The basic idea of gauge fixing is that the gauge fixed partition functions $Z_{gf}$, when they exist, are independent of the particular gauge fixing (since gauge fixing are all equivalent each other) and are equivalent to the original partition function $Z$ (since $X_{gf}$ is equivalent to $X$).

A classical instance of gauge fixing is when $X=\tilde{X}//G$ is an action groupoid, for the action of some group $G$ (the gauge group) on a manifold $\tilde{X}$. In this case a classical gauge fixing is the choice of a _slice_ $S$ in $\tilde{X}$ intersecting each orbit of $G$ exactly once. If the action of $G$ on $\tilde{X}$ is not free, there still will be nontrivial automorphisms in the groupoid $S//G$; these residual internal symmetries are sometimes called _ghost symmetries_

#### Classical gauge fixings ####

* [[BRST complex]]
* [[BV theory]]
  





     