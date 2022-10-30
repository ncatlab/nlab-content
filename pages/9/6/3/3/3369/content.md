
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--



This entry is about the article

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], 
 
  _Topological Quantum Field Theories from Compact Lie Groups_ 

  in P. R. Kotiuga (ed.) _A celebration of the mathematical legacy of Raoul Bott_ AMS (2010)

  ([arXiv:0905.0731](http://arxiv.org/abs/0905.0731))

on 

1. in sections 3 and 8; a central topic in [[higher category theory and physics]]: the [[higher category theory|abstract higher categoretic]] conception of [[path integral]] [[quantization]] of classical [[action functionals]] to [[FQFT|extended quantum field theories]], realized here for finite [[higher gauge theories]] [[Dijkgraaf-Witten theory]]-type theories (see also at [[prequantum field theory]])

1. the [[extended TQFT]]-[[quantization]] of $G$-[[Chern-Simons theory]] for abelian [[Lie groups]] $G$.

More on the story of sections 3 and 8 is in 

* [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_, talk at _Notre Dame Graduate Summer School on Topology and Field Theories_ and _Harvard lecture_ 2012 ([video part 1](http://www.youtube.com/watch?v=eQayYLDw1VA), [part 2](http://www.youtube.com/watch?v=OEShrQyvmS4), [part 3](http://www.youtube.com/watch?v=nOIcdn1iUR4) [part 4](http://www.youtube.com/watch?v=ZwnClYedaYM), [pdf lecture notes](http://www.math.northwestern.edu/~celliott/notre_dame_notes/Lurie_notes.pdf) by Chris Elliott)


#Contents#
* table of contents
{:toc}


## Preliminaries

The non-toy example application that gives the paper its title is to [[Chern-Simons theory]].


The notion of quantization discussed builds on the notion of $(\infty,n)$-categories of _families of $\infty$-groupoids_ that appears in some of the later sections of

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

Together with a notion of $n$-vector spaces (the [[vertical categorification]] of [[vector space]] and [[2-vector space]]) the article sketches a general abstract formalsim making precise the notion of [[path integral]] [[quantization]] for "finite" theories such as [[Dijkgraaf-Witten theory]]. 

The development, sketching a rather grand picture, remains somewhat sketchy, though, possibly due to the fact that this is a conference proceedings. Also some of the ideas claimed to now be fully generalized have appeared elsewhere before. Notably the notion of the quantization map $Fam_n(C) \to C$ (see below) is effectively what [[John Baez]], [[Jim Dolan]] call in their program on [[groupoidification]] call _degroupoidification_ . The general idea underlying this, that spaces of states are computed as colimits of sections, has been made clear previously by [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))



## The general abstract notion of quantization for discrete theories

> Here is a summary of the general quantization aspect of the article, together with some additional remarks on how to think of all this by [[Urs Schreiber|an nLab author]].

The following is the formalization of the notion of [[quantization]] for discrete theories (such as [[Dijkgraaf-Witten theory]]) as presented in the article.

Fix some $n \in \mathbb{N}$, the dimension of the [[quantum field theory]] to be described.

In 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ .

are described the following two [[(∞,n)-category|(∞,n)-categories]]

* the [[(∞,n)-category of cobordisms]] $Bord_n$: its [[k-morphism]]s are roughly $k$-dimensional [[manifold]]s with boundaries and corners;

* for $C$ any [[(∞,n)-category]] the [[(∞,n)-category of spans]] over $C$, denoted $Fam_n(C)$,

  whose 

  * [[object]]s are [[∞-groupoid]]s $P$ equipped with functors $F_P :P \to C$ 

  * [[morphism]]s are [[span]]s of [[∞-groupoid]]s with [[natural transformation]]s between the corresponding functors ([[bi-brane]]s)

    $$
      \array{
         && P
         \\
         & \swarrow && \searrow
         \\
         P_{in} &&\swArrow&& P_{out}
         \\
         & {}_{\mathllap{\exp(S(-))_{in}}}\searrow
         && \swarrow_{\mathrlap{\exp(S(-))_{out}}}
         \\
         && C
      }
    $$

  * "and so on".

For the application to [[quantization]] of [[sigma-model]] theories we want to be thinking of the data encoded by these $(\infty,n)$-categories as follows:

* An [[k-morphism]] $\Sigma$ in $Bord_n$ is a piece of $k$-dimensional "worldvolume" of some extended object, whose quantum dynamics we want to describe; we may roughly think of this as a [[cospan]]

  $$
    \array{
      && \Sigma
      \\
      & \nearrow && \nwarrow
      \\
      \Sigma_{in} &&&& \Sigma_{out}
     }
  $$

  where $\Sigma_{in}$ and $\Sigma_{out}$ are pieces of the boundary of $\Sigma$. We think of $\Sigma_{in}$ as the "incoming" piece of the object that we want to describe, which then experiences a self-interaction as described by the topology of $\Sigma$ and comes out in the shape of $\Sigma_{out}$ (for instace $\Sigma$ might be the three-holed sphere, $\Sigma_{in}$ the disjoint unions of two of its bounding circles and $\Sigma_{out}$ the remaining one, modelling the interaction where two strings merge to a single one).

* An [[morphism]] in $Fam_n(C)$ is to be thought of as

  * two **configuration spaces of fields** $P_{in}, P_{out}$ 
    of some field theory;

  * together with an [[action functional]] on it in the form of an
    higher vector bundle ("[[gerbe]]") $\exp(S_P()) : P \to C$;
    being the component of the [[natural transformation]]
    that assigns to each _path_ $P$ between field
    configuration a _phase_ ;    

In these terms the **kinematics of a classical field theory** is a choice of $(\infty,n)$-functor

$$
  kin : Bord_n \to Fam_n(*)
$$

whereas the **dynamics of a classical field theory** -- the specificaton of an [[action functional]] on the given configuration spaces,  is a lift of that to $Fam_n(C)$

$$
  \array{
    && Fam_n(C)
    \\
    & {}^{\exp(S(-))}\nearrow & \downarrow
    \\
    Bord_n &\stackrel{kin}{\to}&
    Fam_n(*)
  }
$$

To illustrate this: specifically, if we consider a [[sigma-model]] [[quantum field theory]] that is induced from a **target space** geometry $X$, such that a field configuration on $\Sigma$ is a morphism $\phi : \Sigma \to X$, and with a [[gauge field|background field]] $\nabla : X \to C$, then we think of the corresponding functor

$$
  conf_X : Bord_n \to Fam_n(C)
$$

as given by homming a [[cobordism]] [[cospan]] of the form

$$
  \array{
    && \Sigma
    \\
    & \nearrow && \nwarrow
    \\
    \Sigma_{in} &&&& \Sigma_{out}
   }
$$
 

into $X$ to produce a [[span]] of path and configuration spaces

$$
  \array{
    && [\Sigma,X]
    \\
    & \swarrow && \searrow
    \\
    [\Sigma_{in},X] &&&& [\Sigma_{out},X]
   }
$$

equipped with the **transgressed background field** as the corresponding action functional

$$
  \array{
    && [\Sigma, X]
    \\
    & \swarrow && \searrow
    \\
    [\Sigma_{in},X] &&&& [\Sigma_{out},X]
    \\
    & \searrow && \swarrow
    \\
    && C
   }
   \,.
$$

With that in hand, the **[[quantization]]** of the given classical field theory $\exp(S(-)) : Bord_n \to Fam_n(C)$ is its "pushforward to the point", given by postcomposition with a functor

$$
  \int : Fam_n(C) \to C
$$

that over objects $\exp(S(-)) : P \to C$ is given by taking $n$-categorical [[colimit]]

$$
  (\exp(S(-)) : P \to C) \mapsto (\lim_\to \exp(S(-)))
$$

which in terms of [[coend]]-notation is indeed nicely suggestively written as

$$
  (\exp(S(-)) : P \to C) \mapsto (\int \exp(S(-)))
  \,.
$$

Taking such a colimit may be thought of as forming the space of [[section]]s of the action functional $n$-vector bundle $\exp(S(-)) : P \to C$. That this is the right general idea was maybe first amplified in

* [[Dan Freed]], _Higher Algebraic Structures and Quantization_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115).

A first more categorical formulation of this is in

* [[Simon Willerton]] _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv:math/0503266](http://arxiv.org/abs/math.QA/0503266))

What exactly the functor $\int : Fam_n(C) \to C$ does to [[k-morphism]]s is apparently left as an exercise for the inclined reader. it requires that in $C$ limits and colimits coincide. This is the case notably for $C = Vect$.

The authors indicate in section 8 a general recursive procedure for defining higher categories of higher vector spaces, by iterating the bimodule-style definition of [[2-vector space]]s, as described there. This yields a notion $C = n Vect$, which should be the right codomain for $n$-dimensional QFTs. So we end up with a diagram

$$
  \array{
    && Fam_n(C) &\stackrel{\int}{\to}& C
    \\
    & {}^{\exp(S(-))}\nearrow & \downarrow
    \\
    Bord_n &\stackrel{kin}{\to}&
    Fam_n(*)
  }
$$

whose left bit is the kinematical and dynamical input given by a classical field theory, and whose composition to to the right is supposed to give the corresponding quantum field theory, which by the logic motivating the [[cobordism hypothesis]] is a functor $Z : Bord_n \to n Vact$:

$$
  Z_S  = \int \exp(S(-)) : Bord_n \stackrel{\exp(S(-))}{\to}
   Fam_n(n Vect) \stackrel{\int}{\to} n Vect
   \,.
$$



## 3d Chern-Simons as a fully extended TQFT
 {#3dCSFullyExtended}

A summary of the FHLT-argument about realizing 3d [[Chern-Simons theory]] as a fully [[extended TQFT]] is given in 

* [[Konrad Waldorf]], _Chern-Simons theory and the categorified group ring_ ([[WaldorfTalbot2010.pdf:file]])


The following are some notes from a talk by [[Constantin Teleman]] on joint work with [[Dan Freed]], given at [ESI Program on K-Theory and Quantum Fields (2012)](http://maths-old.anu.edu.au/esi/2012/).

### CS as a fully extended TQFT

Goals

* i) describe [[Chern-Simons theory]] for compact Lie groups as an [[extended TQFT]], generated by some structure assigned to the point

* ii) relate to chiral [[WZW model]], also down to the point, have a formal framework for this

approach related to:

* [[Kevin Walker]]: 3d Chern-Simons theory is best understood as a boundary condition for a 4d theory.

* [[Chris Douglas]], [[Andre Henriques]]: _[[conformal nets]]_ and their relation to CS theory

construction is special case of [[Reshetikhin-Turaev construction]] which to a [[modular tensor category]] $\mathcal{B}$ assigns a 1-2-3 [[extended TQFT]] that assigns $\mathcal{B}$ to the [[circle]] $S^1$.

So the goal here is to extend this down to the point, to a 0-1-2-3 [[extended TQFT]], hence to an $(\infty,3)$-functor

$$
  Bord^{String}_{0,1,2,3} \to some\;symm\;mon.\;3\; category
$$

the standard choice on the right is a 3-category of (multi) [[fusion categories]], (see the reference by Douglas, Schommer-Pries and Snyder there) whose

* [[objects]] are [[fusion categories]];

* [[morphisms]] are bimodule categories;

* [[2-morphisms]]: bimodule homomorphism functors;

* [[n-morphisms|3-morphisms]]: [[natural transformations]] of these.

If this can be done, then 

* $CS(*) = T$;

* $CS(S^1) = $ [[Drinfeld center]] of $T$ (again an MTC)

[[Witt group]] of [[modular tensor category]]: many abelian examples of CS give nontrivial classes

**Theorem** Given a [[modular tensor category]] $A$, there exists a [[symmetric monoidal (infinity,n)-category|symmetric monoidal 3-category]] $\mathcal{C}_A$ containing the [[fusion categories]] and a [[fully dualizable object]] in $X \in \mathcal{C}_A$ which [[cobordism hypothesis|generates]] a 0-1-2-3 [[extended TQFT]] whose 1-2-3 part agrees with the [[Reshetikhin-Turaev construction]] applied to $A$. 

Here $\mathcal{C}_A$ and $X$ are formally constructed form $A$ by means of 

* $X \otimes X^\vee \simeq A$

* $\mathcal{C}_A = FusionCat[X, X^\vee]$

**Remarks**

* i) This is a theory for "[[string structure]]" manifolds in the sense that the [[first Stiefel-Whitney class]] $w_1$ and the [[first Pontryagin class]] $p_1$ are trivialized, but not necessarily $w_2$.

* ii) This is the universal extension: every other one factors through it. 

  guess: there is some kind of an "algebraic extension" of fusion categories in which the equation $X \otimes X^\vee = A$ can be solved for any MTC $A$. 

* iii) a choice of cube root wil be needed to construct the theory for a [[framed manifold|framed]] 3-manifold

  change of framing: $n \mapsto \times \exp(\frac{2 \pi i c n }{24})$ for $c$ a "[[central charge]]"

because string [[bordism ring|bordism group]] in $dim = 3$ is $\mathbb{Z}_3$, in case of [[spin structure]]

$$
  \array{
    3 & \mathbb{Z}_{24}
    \\
    2 & \mathbb{Z}_2
    \\
    1 & \mathbb{Z}_2
  }
$$

for spin theories one would need categorical representations of this 3-groupoid, but at the moment not known.

**Theorem** ([[Kevin Walker]], in [[Jacob Lurie]]'s language)

* i) $A$ generates an invertible 4d [[extended TQFT]] for [[orientation|oriented]] manifolds;

* ii) $A$ is a valid boundary condition over itself;

The 3d boundary theory in dim 1-2-3 is equivalent to $ReshTur(A)$ after a choice of "bulking manifold" 

**Comments** there is a symmetric monoidal 4-category  whose 

* objects are bimodule tensor categories

* morphisms are bialgebra categories = tensor categories $T$ with braided monoidal functors

  $(B') \otimes B^{bop} \to DZ(T)$

* 2-morphisms are bimodule categories

* 3-morphisms are functors respecting the structure;

* 4-morphisms are natural transformations between these.

Invertibility of a TQFT $Z$ $\Leftrightarrow$ invertibility of $Z(*)$.

so then $Z(S^1) \simeq 1$

**Lemma** [[modular tensor categories]] are invertible in this sense

(4d anomaly theory) + (bulking manifold) = (3d standalone theory)

**Result** Have a 3d TQFT defined on the full subcategory of $Bord^String_{0-1-2-3-4}$ of manifolds which bound.

So the final step in the construction of the full 0-1-2-3-4 theory is to extend from that to the full category of bordisms. 

### Boundary conditions: WZW theory

general metaphor:

* TQFT $\leftrightarrow$ algebra

* boundary condition $\leftrightarrow$ bimodule

other metaphor

* TQFT $Z$ determined by $Z(*)$

* boundary condition $\alpha : 1 \to Z(*)$ (left) or $\beta : Z(*) \to 1$ (right)

For the 3d RT theory this yields for boundary conditions $DZ(T)$-algebra categories.

**Theorem** ([[Graeme Segal]])

Chiral WZW model is a conformal boundary for CS theory

**Problem** make this work down to the point

## Related references

* [[Dan Freed]], _[[4-3-2 8-7-6]]_

category: reference