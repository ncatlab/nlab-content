
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### The general abstract principle

In [[higher category theory]] it is a tautological fact that a $1$-[[transfor]]mation $\lambda$ between [[n-functor]]s $F,G : C \to D$ between [[n-categories]] $C$ and $D$

$$
  \lambda : F \Rightarrow G
$$

is itself, in components, given by an $(n-1)$-functor

$$
  \eta : sk_{n-1} C \to D^{\Delta^1}
  \,.
$$

This may be seen as the generalization to [[directed homotopy theory]] of what in [[homotopy theory]] is the maybe even more tautological fact, that a [[homotopy]] $\eta$ is a map

$$
  \eta : C \times \Delta^1 \to 
  \,.
$$

As with various other almost-tautologies in [[category theory]] they become interesting statements when realized in a concrete context where certain structures are modeled by $n$-[[functor categories]] for all $n$.


### Its application to functorial QFT

For instance in [[FQFT]] one models $n$-dimensional [[topological quantum field theories]] as [[(∞,n)-functor]]s on a flavor of an [[(∞,n)-category of cobordisms]]

$$
  Z : Bord_{n}^S \to \mathcal{C}
$$

(where the superscript $S$ is to remind us that this may be [[cobordism]]s equipped with some extra [[stuff, structure, property|structure]]).

It follows that with $Z_1, Z_2$ two such $n$-dimensional QFTs, a transformation $B : Z_1 \Rightarow Z_2$ does look in components itself like an QFT -- which is _zwisted_ by $Z_1$ and $Z_2$ in some sense (see [below]()) -- , but in dimension $(n-1)$.

More specifically, if $\mathcal{C}$ is a [[symmetric monoidal (∞,n)-category]] with tensor unit $1$ there is the trivial FQFT $\mathbf{1}$ given by the constant $(\infty,n)$-functor $\mathbf{1} : Bord_n \to \mathcal{C}$.

One can see in examples that the transformations

$$
  B : Z \Rightarrow \mathbf{1}
$$

encode boundary _boundary conditions_ on cobordisms with boundary for the theory $Z$. Conversely, this means that one discovers on the boundary of the $n$-dimensional QFT $Z$ the $(n-1)$-dimensional QFT $B$.

For the case of $n=2$ and 2-dimensional cobordisms without any extra structure, a detailed version of these statements are given in ([Schommer-Pries](#SchommerPries)). For $n=3$ some remarks are in ([Schreiber](#Schreiber))

In the study of [[quantum field theory]] and [[string theory]] such kinds of relations between $n$-dimensional QFTs and $(n-1)$-dimensional QFTs on their boundary have been called the _[[holographic principle]]_ . The degree to which this principle has been formalized and the degree to which this formalization has been verified varies greatly. Examples include

* The boundary theory of 3-dimensional [[Chern-Simons theory]] is the 2-dimensional [[WZW-model]]. 

  This is probably the oldest known holographic relation between QFTs.

* In the 2-d QFT called the [[Poisson sigma-model]] with target the [[Poisson Lie algebroid]] comind from a [[Poisson manifold]] the boundary 3-point function computes the [[deformation quantization]] of the classical system described by that Poisson manifold. 

  (This was in fact used implicitly by [[Maxim Kontsevich]] to solve deformation quantization. The relation to the Poisson sigma-model was made explicit by Cattaneo and Felder.)

* The boundary theory of the 2-dimensional [[A-model]] QFT on a target space that is a complexification of a classical [[phase space]] is the 1-dimensional QFT (= [[quantum mechanics]]) that is the [[geometric quantization]] of this phase space. 

  This is described at [[quantization via the A-model]]. 

* The [[AdS/CFT correspondence]] conjectures specifically a holographic relation between [[quantum gravity]] on a 10-dimensional asymptotically [[anti-de Sitter spacetime]] and a superconformal [[Yang-Mills theory]] on its asymptotic boundary. More generally, this specific construction is supposed to apply, with variations, in many different dimensions.


## References

The discussion of transformations between 2d FQFTs and how these encode boundary 1-[[brane]]s and defect 1-[[bi-brane]]s is in

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0))
{#SchommerPries}

from slide 65 on.

A comparatively very well formally understood case of QFT holography is the relation between 3-dimensional [[Chern-Simons theory]] and the 2-dimensional [[WZW-model]]. This is formalized by the [[Reshetikhin?Turaev model]] on the 3-dimensional side and the [[Fuchs-Runkel-Schweigert construction]] on the 2-dimensional side.

Remarks on how the relation between Reshitikhin-Turaev and FSR seem to have an interpretation in terms transformations between 3-functors are at

* [[Urs Schreiber]], _Towards 2-functorial CFT_ ([blog entry](http://golem.ph.utexas.edu/category/2007/08/dbranes_from_tin_cans_part_x.html))
{#Schreiber}

There is it discussed how the basic [[string diagram]] that in FSR formalism encodes a field insertion on, possibly, a defect line and encodes the disk amplittudes of the CFT is the string diagram Poincar&#233;-dual to the cylinder in a 3-category of [[n-vector space|3-vector space]]s.

For references on the [[holographic principle]] in QFT, see there