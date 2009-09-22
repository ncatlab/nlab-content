<div class="rightHandSide toc">

[[!include functorial quantum field theory - contents]]

</div>



The material that should go here is, for some reason, still to some extent at [[generalized tangle hypothesis]]. You should go there to learn more. Better yet, you go there and then come back here to create a decent entry on the cobordisms hypothesis.

+-- {: .un_prop}
###### [[cobordism hypothesis|Cobordism Hypothesis]]

The $n$-category $n Cob$ of cobordisms is the free stable $n$-category with duals on one object (the point).
=--

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

It seems that Lurie's proof uses at least the following two non-trivial ingredients:

a formalization and proof of the cobordism hypothesis is indicated.

This uses the languge of [[(infinity,n)-category|(infinity,n)-categories]] modeled as [[n-fold complete Segal space]]s and a cocrete realization of the [[(infinity,n)-category of cobordisms]] in this context.

What is not yet described in detail it what it means for an $(\inftty,n)$-category to be a [[symmetric monoidal category]] but by comparison with the defintion of [[symmetric monoidal (infinity,1)-category]] one can see what that would be.

The precise formulation of the cobordism hypothesis then takes the form of the following

(theorem 2.4.6 in [[On the Classification of Topological Field Theories]])

+-- {: .num_theorem #Lagrange}
###### Theorem (cobordism hypothesis, framed version)

Let $C$ by a [[symmetric monoidal (infinity,n)-category|symmetric monoidal]] [[(infinity,n)-category]] [[(infinity,n)-category with duals|with duals]] and $Core(C)$ its [[core]] (the maximal [[infinity-groupoid]] in $C$).

Let $Bord_n^{fr}$ be the [[symmetric monoidal (infinity,n)-category|symmetric monoidal]] [[(infinity,n)-category of cobordisms|(infinity,n)-category of cobordisms]].

Finally let $Fun^\otimes(Bord_n^{fr} , C )$ be the [[(infinity,n)-category]] of symmetric monoidal $(\infinity,n)$-functors from bordisms to $C$.

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

The proof is base on

a) the Galatius-Madsen-Tillmann-Weiss theorem (thm 2.7.4, page 50) which characterizes the geometric realization &#8739;Bord n or&#8739; in terms of the suspension of the Thom spectrum;


b) Igusas connectivity result which he uses to show that putting "framed Morse functions" on cobrdisms doesn't change their homotopy type (theorem 3.4.7, page 73)

In fact, the Galatius-Madsen-Weiss theorem is now supposed to be a corollary of Lurie's result.

=--

## Implication: morphisms of [[TQFT]]s ##

In particular this means that $Fun^\otimes(Bord_n^{fr} , C )$ is itself an $(\infinity,0)$-category, i.e. an [[infinity-groupoid]].

When interpreting symmetric monoidal functors from bordisms to $C$ as [[TQFT]]s this means that TQFTs with given codomain $C$ form a [[topological space|space]], an [[infinity-groupoid]]. In particular, any two of them are either equivalent or have no morphism between them.

According to [[Chris Schommer-Pries]] interesting morphisms of [[TQFT]]s arise when looking at transformations only on sub-categories on all of $Bord_n$. This is described at [[QFT with defects]] .




#Further resources#

* [[Jacob Lurie]], _TQFT and the Cobordism Hypothesis_ ([video](http://www.ma.utexas.edu/video/dafr/lurie/), [notes](http://www.ma.utexas.edu/users/plowrey/dev/rtg/notes/perspectives_TQFT_notes.html))


##Discussion##

* [Caf&eacute;](http://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006381)




