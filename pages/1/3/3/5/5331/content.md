
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--






#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$,  a **Poisson $n$-algebra** $A$ is a [[Poisson algebra]] $A$ in a [[category of chain complexes]] with Poisson bracket of degree $(1-n)$ (which is a bracket of degree 0 on $\mathbf{B}^{n-1} A$). 


## Properties

### Relation to $E_n$-algebras
 {#RelationToEnAlgebras}

The [[homology]] of an [[E-n algebra]] for $n \geq 2$ is a Poisson $n$-algebra. 

Moreover, in [[chain complexes]] over a [[field]] of [[characteristic]] 0 the [[E-n operad]] is [[formal dg-algebra|formal]], hence equivalent to its homology, and so in this context $E_n$-algebras are equivalent to Poisson $n$-algebras.

This fact is a higher analog of [[Kontsevich formality]]. It means that every higher dimensional [[prequantum field theory]] giveny by a $P_n$ algebra does have a [[deformation quantization]] (as [[factorization algebras]]) and that the space of choice of these a torsor over the [[automorphism infinity-group]] of $E_n$, a higher analog of the [[Grothendieck-Teichmüller group]].

See also tho _[MO discussion](#MODiscussion) linked to below_.

### Relation to $L_\infty$-algebras
 {#RelationToLInfinityAlgebras}

There is a [[forgetful functor]] from Poisson $n$-algebras to [[dg-Lie algebras]] given by forgetting the [[associative algebra]] structure and by [[suspension of a chain complex|shifting]] the underlying chain complex by $(n-1)$.

Conversely, this functor has a [[derived functor|derived]] [[left adjoint]] which sends a [[dg-Lie algebra]] $(\mathfrak{g},d)$ to its _[[universal enveloping E-n algebra|universal enveloping Poisson n-algebra]]_ $(Sym(\mathfrak{g}[n-1], d))$. (See also [Gwilliam, section 4.5](#Gwilliam)).


## Examples

* A Poisson 1-algebra is a [[Poisson algebra]].

* A Poisson 2-algebra is a [[Gerstenhaber algebra]].

* The [[Chevalley-Eilenberg algebra]] of a [[symplectic Lie n-algebroid]] (see there for details) is naturally a Poisson $(1+n)$-algebra. 

* A [[classical BV complex]] is naturally (if obtained as a [[derived critical locus]], or else by definition) a Poisson 0-algebra.

## Related concepts

* [[BV-algebra]]


* [[higher Poisson structure]]

  * [[Nambu bracket]]

  * [[Poisson bracket Lie n-algebra]]



[[!include Isbell duality - table]]

[[!include deformation quantization - table]]


## References

* [[Alberto Cattaneo]], [[Domenico Fiorenza]], R. Longoni, _Graded Poisson Algebras_, Encyclopedia of Mathematical Physics, eds. J.-P. Fran&#231;oise, G.L. Naber and Tsou S.T. , vol. 2, p. 560-567 (Oxford: Elsevier, 2006). ([pdf](http://www.math.uzh.ch/fileadmin/math/preprints/15-05.pdf))

An introduction to Poisson $n$-algebras in [[dg-geometry]]/[[symplectic Lie n-algebroids]] is in section 4.2 of 

* [[Alberto Cattaneo]], [[Florian Schätz]], _Introduction to supergeometry_, Lecture notes of a course held at the school Poisson 2010 at IMPA, July 2010; 21  ([arXiv:1011.3401](http://arxiv.org/abs/1011.3401))

For discussion in the context of [[perturbation theory|perturbative]] [[quantum field theory]]/[[factorization algebras]]/[[BV-quantization]] see

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in perturbative quantum field theory : $P_0$-operad_ ([wiki](http://math.northwestern.edu/~costello/factorization_public.html#[[P_0%20operad]]), [pdf](http://math.northwestern.edu/~gwilliam/factorization.pdf)) 

* {#Gwilliam} [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([pdf](http://math.berkeley.edu/~gwilliam/thesis.pdf))
 


and for further references along these lines see at _[[factorization algebra]]_.

For general discusison of the relation to [[E-n algebras]] see

* MO discussion, _[Poisson algebras as deformations vs. Poisson algebras in algebraic topology](http://mathoverflow.net/questions/74405/poisson-algebras-as-deformations-vs-poisson-algebras-in-algebraic-topology/75194#75194)_
 {#MODiscussion}

[[!redirects Poisson n-algebras]]

[[!redirects Poisson 0-algebra]]
[[!redirects Poisson 1-algebra]]
[[!redirects Poisson 2-algebra]]
[[!redirects Poisson 3-algebra]]

[[!redirects P-n algebra]]
[[!redirects P-0 algebra]]
[[!redirects P-1 algebra]]
[[!redirects P-2 algebra]]

[[!redirects P-n algebras]]
[[!redirects P-0 algebras]]
[[!redirects P-1 algebras]]
[[!redirects P-2 algebras]]


[[!redirects Poisson 0-algebras]]
[[!redirects Poisson 1-algebras]]
[[!redirects Poisson 2-algebras]]
[[!redirects Poisson 3-algebras]]


[[!redirects Pn-algebra]]
[[!redirects Pn-algebras]]