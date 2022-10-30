A [[topological space]] $X$ is **sober** if its points are exactly determined by its open-set lattice.  Different equivalent ways to say this are:

* $X$ is isomorphic to the space of points of the [[locale]] it gives rise to.

* The points of $X$ are in bijection with the _completely prime filters_ of its open-set lattice.

* (Assuming classical logic) $X$ is $T_0$ and every irreducible closed set (closed set that is not the union of any two smaller closed sets) is the closure of a point.

Sobriety is a separation property that is stronger than $T_0$, but incomparable with $T_1$.  With classical logic, every Hausdorff ($T_2$) space is sober, but this can fail [[constructive mathematics|constructively]].

Any nontrivial indiscrete space is not sober, since it is not $T_0$. More interestingly, the space $R^2$ with the [[Zariski topology]] is $T_1$ but not sober, since every subvariety is an irreducible closed set which is not the closure of a point.  Its _soberification_ is, unsurprisingly, the [[scheme]] $Spec(R[x,y])$, which contains "generic points" whose closures are the subvarieties.  On the other hand, the [[Alexandrov topology]] on any nontrivial [[partial order|poset]] is sober but not $T_1$.
