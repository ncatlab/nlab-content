<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>



>some material that should go here is, for some reason, still to some extent at [[generalized tangle hypothesis]]. You should go there to learn more. Better yet, you go there and then come back here to create a better entry on the cobordisms hypothesis.


#Contents#

* automatic table of contents goes here
{:toc}


# Idea #

The **Cobordism Hypothesis** roughly states that

The [[n-category]] $Cob_n$ of [[extended cobordism]]s (when made precise) is the free stable $n$-category with duals on one object (the point).


In [[FQFT|extended topological quantum field theory]], which is really the [[representation theory]] of these cobordism $n$-categories, we expect:

+-- {: .un_prop}
###### Extended TQFT Hypothesis

An $n$-dimensional unitary extended TQFT is a weak $n$-[[n-functor|functor]], preserving all levels of duality, from the $n$-category $n Cob$ of cobordisms to $n Hilb$, the $n$-category of $n$-[[n-Hilbert space|Hilbert spaces]].
=--

Putting the extended TQFT hypothesis and the cobordism hypothesis together, we obtain:

+-- {: .un_prop}
###### The primacy of the point

An $n$-dimensional unitary extended TQFT is completely described by the $n$-Hilbert space it assigns to a point.
=--

#Lurie's formulation and proof of the cobordism hypothesis#

In 

* [[Jacob Lurie]] [[On the Classification of Topological Field Theories]] 

a formalization and proof of the cobordism hypothesis is indicated.

This uses the languge of [[(infinity,n)-category|(∞,n)-categories]] modeled as [[n-fold complete Segal space]]s and a concrete realization of the [[(∞,n)-category of cobordisms]] in this context.

What is not yet described in detail it what it means for an $(\infty,n)$-category to be a [[symmetric monoidal category]] but by comparison with the defintion of [[symmetric monoidal (∞,1)-category]] one can see what that would be.

The precise formulation of the cobordism hypothesis then takes the form of the following

(theorem 2.4.6 in [[On the Classification of Topological Field Theories]])

+-- {: .un_theorem }
###### Theorem (cobordism hypothesis, framed version)

Let $C$ by a [[symmetric monoidal (infinity,n)-category|symmetric monoidal]] [[(∞,n)-category]] [[(infinity,n)-category with duals|with duals]] and $Core(C)$ its [[core]] (the maximal [[∞-groupoid]] in $C$).

Let $Bord_n^{fr}$ be the [[symmetric monoidal (infinity,n)-category|symmetric monoidal]] [[(infinity,n)-category of cobordisms|(∞,n)-category of cobordisms]].

Finally let $Fun^\otimes(Bord_n^{fr} , C )$ be the [[(∞,n)-category]] of symmetric monoidal $(\infinity,n)$-functors from bordisms to $C$.

Evaluation of any such functor $F$ on the [[point]] ${*}$

$$
  F \mapsto F({*})
$$

induces an $(\infty,n)$-[[n-functor|functor]]

$$
  pt^* : Fun^\otimes(Bord_n^{fr} , C ) \to C .
$$

The statement is that

* this factors through the [[core]] of $C$;

* the map 
  $$
    pt^* : Fun^\otimes(Bord_n^{fr} , C ) \to Core(C)
  $$
  is an equivalence of [[(infinity,n)-category|(infinity,n)-categories]].

=--


+-- {: .proof}
###### Proof

The proof is based on

1. the Galatius-Madsen-Tillmann-Weiss theorem (thm 2.7.4, page 50) which characterizes the geometric realization $|Bord_n^{or}|$ in terms of the suspension of the Thom spectrum;

1. Igusas connectivity result which he uses to show that putting "framed Morse functions" on cobrdisms doesn't change their homotopy type (theorem 3.4.7, page 73)

In fact, the Galatius-Madsen-Weiss theorem is now supposed to be a corollary of Lurie's result.

=--




## Implication: morphisms of TQFTs ##

In particular this means that $Fun^\otimes(Bord_n^{fr} , C )$ is itself an $(\infinity,0)$-category, i.e. an [[∞-groupoid]].

When interpreting symmetric monoidal functors from bordisms to $C$ as [[TQFT]]s this means that TQFTs with given codomain $C$ form a [[topological space|space]], an [[∞-groupoid]]. In particular, any two of them are either equivalent or have no morphism between them.

According to [[Chris Schommer-Pries]] interesting morphisms of [[TQFT]]s arise when looking at transformations only on sub-categories on all of $Bord_n$. This is described at [[QFT with defects]] .

## Remarks ##

### invariants determined from the point ###

The theorem does say that the invariant attached by an extended TQFT to the point determines all the higher invariants &#8211; however it is important to notice that therre are strong constraints on what is assigned to the point. For an $n$-dimensional _framed_ theory one needs to assign a [[fully dualizable object]], and the meaning of the term "fully dualizable" depends on $n$, and gets increasingly hard to satisfy as n grows..

For an $n$-dimensional unoriented theory, the object assigned to the point has to be a fixed point for the $O(n)$- action on fully dualizable objects that is obtained from the framed case of the theorem. 

In the 1d case, this $O(1)$ action on dualizable objects takes every object to its dual, and an $O(1)$ fixed point is indeed a vector space with a nondegenerate symmetric inner product. 

For an _oriented_ theory $n$-dimensional theory need an $SO(n)$-fixed point, which for $n=1$ is nothing but for $n=2$ ends up meaning a [[Calabi-Yau category]] (in the case the target 2-category is that of categories).

In fact something more general is true: if one wants a theory that takes values on manifolds equipped with a $G$-structure, for $G$ any group mapping to $O(n)$ (such as for instance [[orientation]] already discussed or its higher versions [[Spin structure]] or [[String structure]] or [[Fivebrane structure]] or ...) one needs to assign to the point a $G$-fixed point in dualizable objects in your category (with $G$ acting through $O(n)$). 

This beautifully includes all the above plus for example [[manifold]]s with maps (up to [[homotopy]]) to some auxiliary (connected) space $X$ &#8211; here we take $G$ to be the [[loop space]] $\Omega X$  of $X$ (mapping trivially to $O(n)$), so that a reduction of the structure group of the manifold to $G$ involves a map to the [[delooping]] $\mathcal{B}G \simeq X$. 

Such theories are classified by $X$-families of fully dualizable objects. 

Notice that there is an important subtlety of Lurie's theorem in the case of manifolds with $G$-structure which is easy to confuse. The general version of the theorem about TFTs does not say that they are the $G$-fixed points for the $G$-action on fully dualizable objects, but rather they are the _homotopy_ fixed points. This is very important because a homotopy fixed point is not just a property. It is additional structure. Depending on $G$, this additional structure is often encoded in the higher dimensional portion of the field theory.

 One can see this in the 1 dimensional case: there is no property of vector spaces which automatically endows them with an inner product, but it is [[stuff, structure, property|extra structure]].


# References #

The original hypothesis is in 

*  [[John Baez]], [[James Dolan]], _Higher dimensional algebra and Topological Quantum Field Theory_ ([arXiv](http://arxiv.org/abs/q-alg/9503002))

The sketch of the proof is in 

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]]

Parts of the above text have been taken from blog discussion [here](http://sbseminar.wordpress.com/2009/09/24/a-hunka-hunka-burnin-knot-homology).


# Recorded lectures #

A videa of Lurie lecturing on his theorem is here:

* [[Jacob Lurie]], _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))

* The [[UC Riverside Seminar on Cobordism and Topological Field Theories]], organized by [[Julie Bergner]] in the Fall of 2009.  










