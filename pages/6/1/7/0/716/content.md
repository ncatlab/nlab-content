
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **compact closed category**, or simply a **compact category**, is a [[symmetric monoidal category]] in which every object is [[dualizable object|dualizable]], hence a [[rigid monoidal category|rigid]] [[symmetric monoidal category]].

More generally, if we drop the symmetry requirement, we obtain a [[rigid monoidal category]], a.k.a. an *autonomous category*.  Thus a compact category may also be called a **rigid symmetric monoidal category** or a **symmetric autonomous category**.  A maximally clear, but rather verbose, term would be a **symmetric monoidal category with duals for objects**.

A compact closed category is a special case of the notion of [[compact closed pseudomonoid]] in a [[monoidal bicategory]], and similarly for the autonomous cases.

## Properties

### Internal hom and compact closure

A rigid symmetric monoidal category $(\mathcal{C}, \otimes)$ is in particular a [[closed monoidal category]], with the [[internal hom]] given by 

$$
  [A,B] \simeq A^* \otimes B
$$ 

(where $A^*$ is the [[dual object]] of $A$), via the [[adjunction]] [[natural equivalence]] that defines [[dual objects]]

$$
  \mathcal{C}(C,[A,B])
  \simeq
  \mathcal{C}(C, A^\ast \otimes B)
  \simeq
  \mathcal{C}(C \otimes A, B)
  \,.
$$

This is what the terminology "compact closed" refers to.

The inclusion from the category of compact closed categories into the category of closed symmetric monoidal categories also has a [[left adjoint]] ([Day 1977](#Day1977)).  Given a closed symmetric monoidal category $\mathcal{S}$, the free compact closed category $C(\mathcal{S})$ over $\mathcal{S}$ may be described as a [[localization]] of $\mathcal{S}$ by the maps

$$ \sigma : [A,B] \otimes C \to [A, B \otimes C] $$

corresponding to the [[tensorial strength]] of the functors $[A,-] : \mathcal{S} \to \mathcal{S}$.

### Relation to traced monoidal categories
 {#RelationToTracedMonoidalCategories}

Given a [[traced monoidal category]] $\mathcal{C}$, there is a [[free construction]] completion of it to a compact closed category $Int(\mathcal{C})$ &lbrack;[Joyal, Street & Verity 1996](#JoyalStreetVerity96)&rbrack;:

the objects of $Int(\mathcal{C})$ are pairs $(A^+, A^-)$ of objects of $\mathcal{C}$, a morphism $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ is given by a morphism of the form $A^+\otimes B^- \longrightarrow A^- \otimes B^+$ in $\mathcal{C}$, and [[composition]] of two such morphisms $(A^+ , A^-) \to (B^+ , B^-)$ and $(B^+ , B^-) \to (C^+ , C^-)$ is given by [[trace|tracing out]] $B^+$ and $B^-$ in the evident way.


### Relation to star-autonomous categories

A compact closed category is a [[star-autonomous category]]: the [[tensor unit]] is a [[dualizing object]]. Thus it is also an [[mix rule|isomix]] category. (But note that, for example, the symmetric monoidal category of [[sup-lattices]] is star-autonomous, with dualizing object given by the unit, but not compact closed. In a compact closed category, the dualizing functor is additionally monoidal.)

## Examples

\begin{example}
**(finite-dimensional vector spaces)**
\linebreak
The category [[FinDimVect]] of [[finite-dimensional vector spaces]] is compact closed with resoect to the usual [[tensor product of vector spaces]], see [there](finite-dimensional+vector+space#CompactClosure). 

  (It is not compact closed with the [[direct sum]] as monoidal product.)
\end{example}

\begin{example}
A compact closed [[discrete category]] is just an [[abelian group]].
\end{example}

\begin{example}
The [[delooping]] $\mathbf{B}M$ of a [[commutative monoid]] $M$ is a compact closed category, and conversely, any compact closed category (or more generally, any [[closed monoidal category]]) with a single object must be isomorphic to the delooping of some commutative monoid.
\end{example}

## Related concepts

* [[compact closed 2-category]]

* [[compact closed dagger category]]

* [[linear logic]]

## References

The characterization of the free compact closed category over a closed symmetric monoidal category is described in

* {#Day1977} [[Brian Day]], *Note on compact closed categories*, J. Austral. Math. Soc. (Series A) **24**  309-311 (1977) &lbrack;[doi:10.1017/S1446788700020334](https://doi.org/10.1017/S1446788700020334)&rbrack;

Discussion of [[coherence]] in compact closed categories is due to:

* {#KellyLaplaza80} [[Max Kelly]], [[M. L. Laplaza]], *Coherence for compact closed categories*, Journal of Pure and Applied Algebra, **19** 193-213 (1980) &lbrack;<a hef="https://doi.org/10.1016/0022-4049(80)90101-2">doi:10.1016/0022-4049(80)90101-2</a>, [pdf](https://core.ac.uk/download/pdf/82696829.pdf)&rbrack;

On the relation to [[traced monoidal categories]]:

* {#JoyalStreetVerity96} [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. **119** (1996) 447-468 &lbrack;[pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf), [doi:10.1017/S0305004100074338](https://doi.org/10.1017/S0305004100074338)&rbrack;

See also:

* Wikipedia, _[Compact closed category](http://en.wikipedia.org/wiki/Compact_closed_category)_


On the relation to [[quantum operations]] and [[completely positive maps]]:

* [[Peter Selinger]], *Dagger compact closed categories and completely positive maps*, Electronic Notes in Theoretical Computer Science **170** (2007) 139-163, &lbrack;[doi:10.1016/j.entcs.2006.12.018](https://doi.org/10.1016/j.entcs.2006.12.018)&rbrack;

On [[biproducts]]:

* [[Robin Houston]], *Finite products are biproducts in a compact closed category*, Journal of Pure and Applied Algebra **212** 2 (2008) 394-400 &lbrack;[arXiv:math/0604542](https://arxiv.org/abs/math/0604542), [doi:10.1016/j.jpaa.2007.05.021](https://doi.org/10.1016/j.jpaa.2007.05.021)&rbrack;



On compact closure in [[homotopical algebra]] and relating to the [Barrat-Priddy theorem](stable+cohomotopy#AsAlgebraicKTheoryOverTheFieldWithOneElement):

* [[Amit Sharma]], *Compact closed categories and Γ-categories (with an appendix by [[André Joyal]])*, Theory and Applications of Categories **37** 37 (2021) 1222-1261 &lbrack;[arXiv:2010.09216](https://arxiv.org/abs/2010.09216), [tac:37-37](http://www.tac.mta.ca/tac/volumes/37/37/37-37abs.html)&rbrack;




[[!redirects compact closed]]
[[!redirects compact closed categories]]
[[!redirects compact category]]
[[!redirects compact categories]]
[[!redirects symmetric monoidal category with duals for objects]]
[[!redirects symmetric monoidal categories with duals for objects]]
[[!redirects symmetric monoidal category with duals]]
[[!redirects symmetric monoidal categories with duals]]
[[!redirects compact closed monoidal category]]