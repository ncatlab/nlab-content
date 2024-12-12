
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The concept of _isomorphism_ generalizes the concept of [[bijection]] from the category [[Set]] of [[sets]] to general [[categories]].

An _isomorphism_ is an invertible [[morphism]], hence a morphism with an [[inverse morphism]].

Two [[objects]] of a [[category]] are said to be _isomorphic_ if there exists an isomorphism between them. This means that they "are the same for all practical purposes" as long as one does not violate the [[principle of equivalence]].

But beware that two objects may be isomorphic by more than one isomorphism. In particular a single object may be isomorphic to itself by nontrivial isomorphisms other than the [[identity morphism]]. Frequently the particular choice of isomorphism matters.

Every isomorphism is in particular an [[epimorphism]] and a [[monomorphism]], but the converse need not hold.

Common jargon includes "is a mono" or "is monic" for "is a monomorphism", and "is an epi" or "is epic" for "is an epimorphism", and "is an iso" for "is an isomorphism".

[[Henri Poincaré]] wrote in [Poincaré 1908](#Poincaré1908) about isomorphisms:

> "It is scarcely credible, as Mach said, how much a well-chosen word can economize thought. I do not know whether or not I have said somewhere that mathematics is the art of giving the same name to different things. We must so understand it. It is appropriate that things different in substance, but alike in form, should be put into the same mold, so to speak. When our language is well chosen, it is astonishing to see how all the demonstrations made upon some known fact immediately become applicable to many new facts. Nothing has to be changed, not even the words, since the names are the same in the new cases. There is an example, which comes at once to my mind; it is quaternions, upon which, however, I will not dwell.

> A word well chosen very often causes the disappearance of exceptions to rules as announced in their former forms; it was for this purpose that the terms 'negative quantities', 'imaginary quantities', 'infinite points', have been invented. And let us not forget that these exceptions are pernicious, for they conceal laws. Very well then, one of those marks by which we recognize the pregnancy of a result is in that it permits a happy innovation in our language. The mere fact is oftentimes without interest; it has been noted many times, but has rendered no service to science; it becomes of value only on that day when some happily advised thinker perceives a relationship, which he indicates and symbolizes by a word.

> The physicists also do it just the same way. They invented the term 'energy', a word of very great fertility, because through the elimination of exceptions it established a law; because it gave the same name to things different in substance, but alike in form.

> Among the words which have had this happy result, I will mention the 'group' and the 'invariant'. They make us perceive the gist of many mathematical demonstrations; they make us realize how often mathematicians of the past must have run across groups without recognizing them and how, believing these groups to be isolated things, they have found them to be in close relationship without knowing why. Today we would say that they were looking right in the face of isomorphic groups. We feel now that in a group the substance interests us but very little; it is the form alone which matters, and so, when we once know well a single group, then we know through it all the isomorphic groups; thanks to the words 'groups' and 'isomorphism', which sum in a few syllables this subtle law and make it at once familiar to us all, we take our step at once and in so doing economize all effort of thought."

##Definitions

An __isomorphism__, or __iso__ for short, is an invertible [[morphism]], i.e. a [[morphism]] with a 2-sided [[inverse]].  

A morphism could be called __isic__ (following the more common 'monic' and 'epic') if it is an isomorphism, but it\'s more common to simply call it _invertible_.  Two [[objects]] $x$ and $y$ are __isomorphic__ if there exists an isomorphism from $x$ to $y$ (or equivalently, from $y$ to $x$).  An __[[automorphism]]__ is an isomorphism from one object to itself.


## Properties

It is immediate that isomorphisms satisfy the [[two-out-of-three]] property. But they also satisfy [[two-out-of-six property]] satisfied by the [[weak equivalences]] in any [[homotopical category]].

Note that the [[inverse morphism]] of an isomorphism is an isomorphism, as is any [[identity morphism]] or [[composite]] of isomorphisms.  Thus, being isomorphic is an [[equivalence relation]] on objects.  The equivalence classes form the [[fundamental 0-groupoid]] of the category in question.

Every isomorphism is both a [[split monomorphism]] (and thus about any other kind of [[monomorphism]]) and a [[split epimorphism]] (and thus about any other kind of [[epimorphism]]).  In a [[balanced category]], every morphism that is both a [[monomorphism]] and an [[epimorphism]] is invertible, but this does not hold in general.  However, any monic [[regular epimorphism]] (or dually, any epic [[regular monomorphism]]) must be an isomorphism.

A [[groupoid]] is precisely a [[category]] in which every morphism is an isomorphism.  More generally, the [[core]] of any category $C$ is the [[subcategory]] consisting of all objects but only the isomorphisms; it is a kind of underlying groupoid of $C$.  In a similar way, the automorphisms of any given object $x$ form a [[group]], the [[automorphism group]] of $x$.

In [[n-category|higher categories]], isomorphisms generalise to [[equivalence]]s, which we expect to have only [[weak inverse]]s.

In the context of [[homotopy type theory]], for every [[morphism]] $f : hom_A(a,b)$ the [[type]] "f is an isomorphism" is a [[proposition]]. Therefore, for any $a,b:A$ the type $a \cong b$ is a set.
\begin{proof}
Suppose given $g:hom_A(b,a)$ and $\eta:1_a = g \circ f$ and $\epsilon : f \circ g = 1_b$, and similarly $g',\eta'$, and $\epsilon'$. We must show $(g,\eta,\epsilon)=(g',\eta', \epsilon')$. But since all hom-sets are sets, their identity types are mere propositions, so it suffices to show $g=g'$. For this we have $ g' = 1_{a} \circ g'= (g \circ f) \circ g' = g \circ (f \circ g') = g \circ 1_{b}= g$
\end{proof}

## Examples

*  A __[[bijection]]__ is an isomorphism in [[Set]].

*  A __[[homeomorphism]]__ is an isomorphism in [[Top]].

*  A __[[diffeomorphism]]__ is an isomorphism in [[Diff]].

* Every morphism in a [[groupoid]] is an isomorphism. 
  By definition of groupoid.


## Related concepts

* [[equality]]

* **isomorphism**
  
  * [[isomorphism class]]

  * [[exceptional isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of (∞,1)-categories]]

* [[definitional isomorphism]]

* [[EI-category]]

* [[gaunt category]], where all isomorphisms are identities

* [[skeletal category]], where the only non-trivial isomorphisms are automorphisms

* [[groupoid]], where all morphisms are isomorphisms

## References

* {#Poincaré1908} [[Henri Poincaré]], *The future of mathematics*, Revue generale des Sciences pures et appliquees, Paris, 19th year, No. 23, December, 1908 ([pdf](https://sites.math.rutgers.edu/courses/535/535-f08/Poincare.pdf))

* [[Francis Borceux]], Section 1.9 in: *[[Handbook of Categorical Algebra]]* Vol. 1: *Basic Category Theory*, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511525858](https://doi.org/10.1017/CBO9780511525858)&rbrack;


[[!redirects isomorphic]]
[[!redirects isomorphisms]]
[[!redirects iso]]
[[!redirects isic]]

[[!redirects isomorphic]]