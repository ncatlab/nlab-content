
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Pure morphisms
* table of contents
{: toc}

## In general categorical setup

+-- {: .num_defn}
###### Definition

Given a [[regular cardinal]] $\kappa$, a [[morphism]] $f: A\to B$ in a [[category]] $C$ is **$\kappa$-pure** (or **$\kappa$-universally injective**) if for every [[commutative square]]

$$\array{
P & \stackrel{g}\to & Q\\
u\downarrow && \downarrow v \\
A &\stackrel{f}\to & B
}$$

in which $P$ and $Q$ are $\kappa$-[[presentable objects]], the morphism $u:P\to A$ factors through $g$, i.e. there is some $h: Q\to A$ with $u = h\circ g$.

=--

+-- {: .num_remark}
###### Remark

Notice that the above definition does not require that also the morphism $v$ is factored, hence it does _not_ express a [[lifting property]].

=--

+-- {: .num_prop}
###### Proposition


In a $\kappa$-[[accessible category]] $C$ every $\kappa$-pure morphism is [[monic]], hence exhibits a [[pure subobject]]. In a locally $\kappa$-[[locally presentable category|presentable category]] $\kappa$-pure morphisms are, moreover, [[regular monomorphisms]], and in fact coincide with the $\kappa$-[[directed colimits]] of [[split monomorphism]]s in the category of arrows $C^2 = Arr(C)$; more generally this characterization holds in all $\kappa$-accessible categories admiting [[pushouts]]. 

=--

([Adámek-Hub-Tholen 1996](#AHT96)).  


## In ring theory and for schemes

We work with unital, possibly commutative, [[rings]] and [[modules]].
Given a ring $R$, a morphism $f: M\to M'$ of left $R$-modules is pure if the tensoring the [[exact sequence]] of left $R$-modules

$$
0\to Ker f \to M\stackrel{f}\to M'\to Coker f\to 0
$$

with any right $R$-module $N$ (from the left) yields an exact sequence of abelian groups. 

Grothendieck has proved that faithfully flat morphisms of commutative schemes are of effective descent for the categories of quasicoherent $\mathcal{O}$-modules. But this was not entirely optimal, as there is in fact a more general class than faithfully flat morphisms which satisfy the effective descent. For a local case of commutative rings, [[Joyal]] and [[Tierney]] have then proved (unpublished) that the [[effective descent morphisms]] for modules are precisely the pure morphisms of rings (or dually of affine schemes). The result can be extracted also from their Memoirs volume on Galois theory. [[Janelidze]] and [[Tholen]] have reproved the theorem as a corollary of a result for noncommutative rings obtained using the Beck's [[comonadicity theorem]].

## Related concepts

* [[pure subobject]]


## References

#### General references

* The [Stacks Project](https://stacks.math.columbia.edu), 28.10. Radicial and universally injective morphisms (of schemes) [tag/01S2](https://stacks.math.columbia.edu/tag/01S2), 34.4. Descent for universally injective morphisms, [tag/08WE](https://stacks.math.columbia.edu/tag/08WE) 

#### Descent along pure morphisms

The following paper was the first with the result on that pure morhisms are of the effective descent but the proof has been omitted:

* Jean-Pierre Olivier, _Descente par morphismes purs_, C. R. Acad. Sci. Paris Sér. A-B __271__ (1970) A821–A823

The result is proved (within a larger context)

* [[André Joyal]], [[Myles Tierney]], _An extension of the Galois theory of Grothendieck_, Mem. Amer. Math. Soc. __309__ (1984) vol. 51, pages vii+71

Clean proofs are by Mesablishvili and by Janelidze,

* Bachuki Mesablishvili, _Pure morphisms of commutative rings are effective descent morphisms for modules -- a new proof_, Theory and Appl. of Categories __7__, 2000, No. 3, 38-42, [tac](http://www.tac.mta.ca/tac/volumes/7/n3/7-03abs.html)

* [[T. Brzeziński]], R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series __309__, Cambridge Univ. Press 2003; [errata pdf](http://maths.swan.ac.uk/staff/tb/corinerr.pdf)

* [[George Janelidze]], [[Walter Tholen]], _Facets of descent III: monadic descent for rings and algebras_,  Appl. Categ. Structures __12__ (2004), no. 5-6, 461&#8211;477, [MR2005i:13019](http://www.ams.org/mathscinet-getitem?mr=2107397), [doi](http://dx.doi.org/10.1023/B:APCS.0000049312.36783.0a)

#### Ziegler spectrum and connections to model theory

Ziegler spectrum of indecomposable pure injectives has been introduced in

* M. Ziegler, _Model theory of modules_, Ann. Pure Appl. Logic 26 (1984) 149 – 213. 

A textbook account is in 

* [[Mike Prest]], _Purity, spectra and localisation_, Enc. Math. Appl. __121__, Camb. Univ. Press 2011, 798 pages; publishers book [page](http://www.cambridge.org/gb/knowledge/isbn/item2327409/?site_locale=en_GB)

The relationship between the Ziegler spectrum of (the category of modules over) a ring and the Ziegler spectrum of its derived category is studied in

* G. Garkusha, M. Prest, _Triangulated categories and the Ziegler spectrum_, Algebras & Repres. Theory 8, 499–523 (2005) [doi](https://doi.org/10.1007/s10468-005-8147-2)

Other articles include

* M. Prest, P. Rothmaler, M. Ziegler, _Absolutely pure and flat modules and "indiscrete" rings_, J. Alg. __174__:2 (1995) 349-372 [doi](https://doi.org/10.1006/jabr.1995.1131)

* Christian U. Jensen, Helmut Lenzing, _Model theoretic algebra: with particular emphasis on fields, rings, modules_, Algebra, Logic and Applications __2__, Gordon and Breach 1989.

* I. Herzog, _The Ziegler spectrum of a locally coherent Grothendieck category_, Proc. London Math. Soc. __74__:3 (1997) 503-558 [doi](https://doi.org/10.1112/S002461159700018X)

#### Other articles in categorial context

* Ivo Herzog, _Pure-injective envelopes_, Journal of Algebra and Its Applications 2(4) (2003), 397-402 [pdf](http://lima.osu.edu/people/iherzog/env.pdf)

* {#AHT96} [[Jiří Adámek]], H. Hub, [[Walter Tholen]], _On pure morphisms in accessible categories_,  J. Pure Appl. Alg. __107__, 1 (1996), pp 1-8, <a href="http://dx.doi.org/10.1016/0022-4049(95)00037-2">doi</a>
 {#Adamek}

* Michel H&#233;bert, _Purity and injectivity in accessible categories_, <a href="http://dx.doi.org/10.1016/S0022-4049(97)00073-X">doi</a> 

* W.W. Crawley-Boevey, _Locally finitely presented additive categories_, Communications in Algebra __22__(5)(1994), 1641-1674.

* Rosanna Laking, _Purity in compactly generated derivators and t-structures with Grothendieck hearts_, Math. Zeitschrift, [doi](https://10.1007/s00209-019-02411-9) (2019).

[[!redirects pure morphisms]]
[[!redirects purity]]
[[!redirects universally injective morphism]]
