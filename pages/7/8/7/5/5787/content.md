# Pure morphisms
* table of contents
{: toc}

## In general categorical setup

Given a [[regular cardinal]] $\kappa$, a [[morphism]] $f: A\to B$ in a [[category]] $C$ is $\kappa$-pure if for every [[commutative square]]

$$\array{
P & \stackrel{g}\to & Q\\
u\downarrow && \downarrow v \\
A &\stackrel{f}\to & B
}$$

in which $P$ and $Q$ are $\kappa$-[[presentable objects]], the morphism $u:P\to A$
factors through $g$.  In other words, $f$ has the [[right lifting property]] with respect to all morphisms between $\kappa$-presentable objects.

In a $\kappa$-[[accessible category]] $C$ every $\kappa$-pure morphism is [[monic]]. In a locally $\kappa$-[[locally presentable category|presentable category]] $\kappa$-pure morphisms are, moreover, [[regular monomorphisms]], and in fact coincide with the $\kappa$-[[directed colimits]] of [[split monomorphism]]s in the category of arrows $C^2 = Arr(C)$; more generally this characterization holds in all $\kappa$-accessible categories admiting [[pushouts]] (Ad&#225;mek, Hub, Tholen).  


## In ring theory and for schemes

We work with unital, possibly commutative, [[rings]] and [[modules]].
Given a ring $R$, a morphism $f: M\to M'$ of left $R$-modules is pure if the tensoring the [[exact sequence]] of left $R$-modules

$$
0\to Ker f \to M\stackrel{f}\to M'\to Coker f\to 0
$$

with any right $R$-module $N$ (from the left) yields an exact sequence of abelian groups. 

Grothendieck has proved that faithfully flat morphisms of commutative schemes are of effective descent for the categories of quasicoherent $\mathcal{O}$-modules. But this was not entirely optimal, as there is in fact a more general class than faithfully flat morphisms which satisfy the effective descent. For a local case of commutative rings, [[Joyal]] and Tierney have then proved (unpublished) that the effective descent morphisms for modules are precisely the pure morphisms of rings (or dually of affine schemes). Janelidze and Tholen have reproved the theorem as a corollary of a result for noncommutative rings obtained using the Beck's [[comonadicity theorem]].


## References

* Bachuki Mesablishvili, _Pure morphisms of commutative rings are effective descent morphisms for modules -- a new proof_, Theory and Appl. of Categories __7__, 2000, No. 3, 38-42, [tac](http://www.tac.mta.ca/tac/volumes/7/n3/7-03abs.html)

* T. Brzezi&#324;ski, R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series __309__, Cambridge Univ. Press 2003.

* Janelidze, Tholen, _Facets of descent III: monadic descent for rings and algebras_,  Appl. Categ. Structures __12__ (2004), no. 5-6, 461&#8211;477, [MR2005i:13019](http://www.ams.org/mathscinet-getitem?mr=2107397), [doi](http://dx.doi.org/10.1023/B:APCS.0000049312.36783.0a)

* J. Ad&#225;mek, H. Hub, W. Tholen, _On pure morphisms in accessible categories_, 
J. Pure Appl. Alg. __107__, 1 (1996), pp 1-8, <a href="http://dx.doi.org/10.1016/0022-4049(95)00037-2">doi</a>

* Michel H&#233;bert, _Purity and injectivity in accessible categories_, 
<a href="http://dx.doi.org/10.1016/S0022-4049(97)00073-X">doi</a> 

[[!redirects pure morphisms]]
[[!redirects purity]]
