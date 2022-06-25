
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

An ordinary [[group]] is either an [[abelian group]] or not. For an [[∞-group]] there is an infinite tower of notions ranging from completely general non-abelian [[∞-groups]], over [[braided infinity-group|braided $\infty$-groups]], [[sylleptic infinity-groups|sylleptic $\infty$-groups]] ..., to ever more abelian groups  By an _abelian ∞-group_ (not an established term) one may want to mean an [[∞-group]] which is maximally abelian, in this sense. 

Technically, the level of abelianness may be encoded (see at *[[May recognition theorem]]*) by the [[En-operads|$E_n$-operads]] as $n$ ranges from 1 to $\infty$: On the non-abelian end, a general [[∞-group]] is equivalently a groupal [[algebra over an operad|algebra]] over $E_1$, also known as the [[associative operad]], hence is a  groupal [[A-∞ algebra]]; while at the abelian end a groupal [[E-infinity space|$E_\infty$-space]] is an *[[infinite loop space]]* or *[[connective spectrum]]*. See also the *[periodic table](k-tuply+groupal+n-groupoid#PeriodicTable)* of [[k-tuply monoidal n-groupoid|$k$-tuply monoidal $n$-groupoids]].

Notice that referring to [[connective spectra]] as "abelian $\infty$-groups" (which is not standard) matches the established terminology for *[[non-abelian cohomology]]* (which is standard): The qualifier "non-abelian" in [[non-abelian cohomology]] is in contrast to [[Whitehead-generalized cohomology theories]] which are [[Brown representability theorem|represented]] by [[spectra]].

In a more restrictive sense one may say that plain abelian [[cohomology]] is just *[[ordinary cohomology|ordinary]]* cohomology theory, subsuming only those [[Whitehead-generalized cohomology theories]] which are [[Brown representability theorem|represented]] specifically by [[Eilenberg-MacLane spectra]]. Under the [[Dold-Kan correspondence]] these are [[equivalence of (infinity,1)-categories|equivalently]] [[chain complexes]] of [[abelian groups]]. One may think of these as being yet more commutative than general spectra and might want to reserve the term "abelian $\infty$-group" for them.



## Proposition

### Relation to commutative $\infty$-rings

+-- {: .num_defn #GroupOfUnitsFunctor} 
###### Definition

Write

$$
  gl_1 \; \colon \;  CRing_\infty \to AbGrp_\infty
$$

for the [[(∞,1)-functor]] which sends a [[E-∞ ring|commutative ∞-ring]] to its [[∞-group of units]]. 

=--

+-- {: .num_defn}
###### Definition

The [[∞-group of units]] [[(∞,1)-functor]] of def. \ref{GroupOfUnitsFunctor} is a  right-[[adjoint (∞,1)-functor]] (or at least a [[right adjoint]] on [[homotopy category of an (∞,1)-category|homotopy categories]])

$$
  CRing_\infty 
  \stackrel{\overset{\mathbb{S}[-]}{\leftarrow}}{\underset{gl_1}{\to}}
  AbGrp_\infty
  \,.
$$

=--

This is ([ABGHR 08, theorem 2.1](#ABGHR08)).


## Examples

* A [[0-truncated]] abelian $\infty$-group is equivalently an [[abelian group]].

* A [[1-truncated]] abelian $\infty$-group is equivalently a [[symmetric 2-group]].

* A [[2-truncated]] abelian $\infty$-group is equivalently a [[symmetric 3-group]].

## Related concepts


[[!include k-monoidal table]]


* [[∞-group]], [[k-tuply groupal n-groupoid]]

* [[braided ∞-group]],

  * [[braided 2-group]]

  * [[braided 3-group]]

* [[sylleptic ∞-group]]

  * [[sylleptic 3-group]]

* **abelian ∞-group**

  * [[abelian group]]

  * [[abelian 2-group]]

  * [[abelian 3-group]]

## References

General discussion is in section 5 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_

Discussion in the context of [[E-∞ rings]] and [[twisted cohomology]] is in 

* {#ABGHR08} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 

[[!redirects abelian infinity-groups]]

[[!redirects k-monoidal ∞-group]]

[[!redirects abelian ∞-group]]
[[!redirects abelian ∞-groups]]

