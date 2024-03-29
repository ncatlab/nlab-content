
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _comodule_ is to a [[comonoid]] as a [[module]] is to a [[monoid]]. Where a [[module]] is equipped with an [[action]], a comodule is dually equipped with a _coaction_.

## Definition

Given a [[comonoid]] $C$ with comultiplication $\Delta_C: C\to C\otimes C$ and counit $\epsilon:C\to \mathbf{1}$ in a [[monoidal category]] $\mathcal{M}$, and an [[object]] $M$ in $\mathcal{M}$,
a __left $C$-coaction__ is 

* a [[morphism]] $\rho: M\to C\otimes M$ 

* which is 

  * co[[associative]] i.e. (for $\mathcal{M}$ nonstrict use the canonical isomorphism $C\otimes (C\otimes M)\cong (C\otimes C)\otimes M$ to compare the sides) $(\Delta_C\otimes\mathrm{id}_M)\circ\rho = (\mathrm{id}_C\otimes\rho)\circ\rho: M\to C\otimes C\otimes M$

  * and co[[unital]] i.e. $(\epsilon\otimes \mathrm{id}_M)\circ\rho = \mathrm{id}_M$ (in this formula, $\mathbf{1}\otimes M$ is identified with $M$). 

In some monoidal categories, e.g. of (super)[[vector space]]s, and of [[Hilbert space]]s, one often says (left/right) [[corepresentation]] instead of (left/right) coaction. 

## The category of comodules

Let $k$ be a [[commutative ring]] and let $\mathcal{M} = Mod(k)$.  Then one has the following properties:

* The category of comodules over a [[coalgebra]] is [[comonadic]] over $Mod(k)$.
* It is [[cocomplete]] and [[complete category|complete]].
* It has a [[cogenerator]].

See [Wischnewsky](#Wischnewsky).

## Examples

* [[Hopf algebra]], [[Hopf algebroid]]

* The category of [[linear representations]] of an [[affine group]] is equivalent to the category of comodules over a [[Hopf algebra]].

## Related concepts

* [[dg-comodule]]

* [[comodule spectrum]]


## References

Properties of the category of comodules over a [[coalgebra]] are studied in

* {#Wischnewsky} Manfred Wischnewsky, _On linear representations of affine groups, I_, Pacific Journal of Mathematics, Vol. 61, No. 2, 1975, [Project Euclid](http://projecteuclid.org/euclid.pjm/1102868049).


On [[locally presentable category|local presentability]] of [[CocommCoalg|categoris of coalgebras]] and their comodules:

* [[Hans-Eberhard Porst]], *On corings and comodules*, Archivum Mathematicum **42** 4 (2006) 419-425 &lbrack;[dmlcz:108017](https://dml.cz/handle/10338.dmlcz/108017), [pdf](http://dml.cz/bitstream/handle/10338.dmlcz/108017/ArchMathRetro_042-2006-4_7.pdf)&rbrack; 



[[!redirects comodules]]
[[!redirects co-module]]
[[!redirects co-modules]]
[[!redirects coaction]]
[[!redirects coactions]]
[[!redirects co-action]]
[[!redirects co-actions]]