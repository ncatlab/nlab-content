
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[2-category]]-theory, by a **PIE-limit** one means a [[strict 2-limit]] which can be constructed from 

1. (P) strict [[cartesian product|products]], 

1. (I) [[strict inserters]], 

1. (E) [[strict equifiers]].  

More precisely, the class of PIE-limits is the [[saturation of a class of weights|saturation]] of the class containing products, inserters, and equifiers.  Any PIE-limit is in particular a [[flexible limit]], and therefore also a (non-strict) [[2-limit]].

Furthermore, all [[strict pseudo-limits]] are PIE-limits, and therefore any [[strict 2-category]] which admits all PIE-limits also admits all non-strict 2-limits, although it may not have all strict 2-limits.  This is the case, for instance, for the 2-category of strict algebras and pseudo morphisms over a [[strict 2-monad]].

Some examples of PIE-limits are:

- [[comma object|Comma objects]]
- [[pseudo limit|Pseudo limits]]
- [[lax limit|Lax limits]]
- [[oplax limit|Oplax limits]]
- [[Eilenberg–Moore objects]] for [[monads]]
- [[power|Powers]]
- [[iso-inserter|Iso-inserters]]
- [[inverters|Inverters]]
- [[descent object|Descent objects]]

An intuition is that PIE-limits are those 2-dimensional limits that do not impose any equations between 1-cells. For instance, [[equalizers]] and [[pullbacks]] are not PIE-limits.

PIE-limits can also be characterized as the coalgebras for a [[pseudo morphism classifier]] [[comonad]], exhibiting them as a 2-categorical version of the notion of [[rigged limit]].

## Characterisation of PIE-weights

A PIE-limit is one whose [[weighted limit|weight]] is PIE.  [Power and Robinson](#PowerRobinson) characterised such weights $W : J^{op} \to Cat$ as those for which the induced functor $ob \circ W_0 \colon J^{op}_0 \to Cat_0 \to Set$ is [[multirepresentable]]. This holds if and only if each connected component of the [[category of elements]] of $ob \circ W_0$ has an [[initial object]].

## Related pages

* [[flexible limit]]

## References

* Blackwell, [[Max Kelly|Kelly]], and [[John Power|Power]], *Two-dimensional monad theory*, Journal of Pure and Applied Algebra 59 (1989) 1-41. doi:[10.1016/0022-4049(89)90160-6](https://doi.org/10.1016/0022-4049%2889%2990160-6)

* {#PowerRobinson} [[John Power]], [[Edmund Robinson]], *A characterization of pie limits*, Math. Proc. Cam. Phil. Soc.  **110** (1991) 33 &lbrack;[doi:10.1017/S0305004100070092](https://doi.org/10.1017/S0305004100070092)&rbrack;

* [[John Bourke]], *Codescent objects in 2-dimensional universal algebra*, PhD Thesis (2010), University of Sydney.

On $\lambda$-small objects in PIE-limits:

* [[Leonid Positselski]], _Notes on limits of accessible categories_, [arXiv:2310.16773](https://arxiv.org/abs/2310.16773).


[[!redirects PIE-limit]]
[[!redirects PIE limit]]
[[!redirects PIE-limits]]
[[!redirects PIE limits]]
[[!redirects pie-limit]]
[[!redirects pie limit]]
[[!redirects pie-limits]]
[[!redirects pie limits]]

[[!redirects PIE 2-limit]]
[[!redirects PIE 2-limits]]

