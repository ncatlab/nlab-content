
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The principle of functional extensionality states that two [[functions]] are [[equal]] if their values are equal at every argument.

## Definition

### In type theory

In [[intensional type theory|intensional]] ([[Martin-Löf type theory|Martin-Löf]]) [[dependent type theory]] the existence of [[identity types]] induces a notion on [[path space objects|paths]] between [[terms]] of a given type.

In particular for two [[terms]] $f, g \in [X,Y]$

    f g: X -> Y

of _[[function type]]_, a path/[[morphism]] $f \stackrel{p}{\to} g$

    p: f == g

between them is to be thought of as a [[homotopy]] or [[natural transformation]] (a $1$-[[transfor]]). In particular it implies, one can prove, that there are families of paths $happly_{f,g,p}$ between all the values of the functions

    happly f g p: forall x: X, f x == g x .

However, from general [[intensional type theory|intensional]] [[dependent type theory]] one cannot prove the converse: 

* the existence of paths between all pairs of values does not imply that there is a path between the functions. 

From a purely intensional point of view, this is to be expected --- two functions could be defined in different ways, and thus be intensionally different, yet produce the same values on all inputs (i.e. be extensionally the same).

However, in many contexts one wants to treat functions extensionally, such as when regarding type theory as the [[internal language]] of some [[category]].  In particular, this is the case in [[homotopy type theory]], where one wants to interpret the type theory as the [[internal language of an (∞,1)-topos]], for instance of [[Top]] $\simeq$ [[∞Grpd]].

In such an [[internal logic]] context, a _family_ of anything must always mean "continuous family", so that a family of paths between the values of two functions is a continuous homotopy between them, and hence ought to induce a path between them in the function-space.  Thus, one wants to impose the condition that from a term

    eta: forall x: X, f x == g x .

we can deduce an actual path between $f$ and $g$. 

Translating this into direct [[categorical semantics|categorical terms]], the term $\eta$ gives a map 

$$1 \to \Pi_{X \to 1} [f x = g x]$$ 

into the [[dependent product]], which (as discussed there), in turn corresponds to a [[section]] $\sigma \colon X \to [f x = g x]$ of the [[display map]] on the left side of the [[pullback]] 

$$\array{
[f x = g x] & \to & P(Y) \\
\downarrow & & \downarrow \\
X & \underset{\langle f, g \rangle}{\to} & Y \times Y
}
\,,
$$ 

where $P(Y)$ is the [[identity type]] or space of paths in $Y$. Such a section is tantamount to a lift $X \to P(Y)$ of $\langle f, g \rangle \colon X \to Y \times Y$. From this we would like to deduce an actual path $p \colon 1 \to P(Y^X)$. 

So, very simply, function extensionality means we are able to lift elements $h \colon 1 \to P(Y)^X$ through a canonical map $\phi \colon P(Y^X) \to P(Y)^X$ that is obtained from a [[dependent eliminator]]. 

Of course we are not just interested in [[global element|global elements]] here. What we really want is an actual section $P(Y)^X \to P(Y^X)$ of $\phi$ in the [[slice category|slice]] over $(Y \times Y)^X$ (although this can be derived from the global element formulation by using the [[Yoneda lemma]] together with [[currying]] and uncurrying tricks). This condition may be called "naive" or "weak" function extensionality, in view of an apparently stronger condition that this section (and therefore also $\phi$) be _equivalences_. This latter condition might be called "strong function extensionality". 

Under reasonable assumptions on the type theory, it turns out that these and other versions of function extensionality are equivalent; for now see ([Lumsdaine](#Lumsdaine)) below. In any case, if the type theory has an extra [[axiom]] that implies some such version, one says that **function extensionality** holds. 

### In category theory

Function extensionality in category theory is true in any [[concrete category]] $\mathcal{C}$. The axiom could be called "morphism extensionality"; however, in all concrete categories, the morphisms are functions between sets. 

## Properties

### Homotopy categorical semantics
 {#HomotopyCategoricalSemantics}

+-- {: .num_prop #FunExtInFibrationCat}
###### Proposition

Function extensionality holds in the [[internal language|internal]] [[type theory]] of a [[type-theoretic fibration category]] precisely if [[dependent products]] (i.e. right [[base change]]) along [[fibrations]] preserve [[acyclic fibrations]].

=--

([Shulman 12, lemma 5.9](#Shulman12))

+-- {: .num_example #EveryPresentableLocallyCartesinClosedInfinityCatInterpretsHoTTPlusFunExt}
###### Example

The condition in prop. \ref{FunExtInFibrationCat} holds in particular in [[right proper model category|right proper]] [[Cisinski model structures]], since in these right [[base change]] along fibrations is a [[right Quillen functor]] (see e.g. the proof <a href="https://ncatlab.org/nlab/show/locally+cartesian+closed+(infinity,1)-category#PresentationTheorem">here</a>). 

Notice that every [[presentable (∞,1)-category|presentable]] [[locally Cartesian closed (∞,1)-category]] (by the discussion <a href="locally+cartesian+closed+(infinity,1)-category#PresentationTheorem">there</a>) has a presentation by a [[right proper model category|right proper]] [[Cisinski model category]]. Accordingly we may say that every [[presentable (∞,1)-category|presentable]] [[locally Cartesian closed (∞,1)-category]] interprets [[HoTT]]+FunExt.

=--

### Relation to interval types

An [[interval type]] in [[homotopy type theory]] (with definitional computation rule for the endpoints) implies function extensionality; see [this blog post](http://homotopytypetheory.org/2011/04/04/an-interval-type-implies-function-extensionality/)


### Relation to the univalence axiom

The [[univalence axiom]] implies function extensionality (this is due to [[Vladimir Voevodsky]]).  See for instance ([Bauer-Lumsdaine](#BauerLumsdaine)).

## See also

* [[homotopy]]

* [[concrete category]]

* [[prefunction]]

## References

An introduction to the relevant notions and a guided walk through the formal proof that univalence implies functional extensionality is at

* {#BauerLumsdaine} [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_
  

A discussion of various flavors of function extensionality, and how to move between them, can be found in

* [[Richard Garner]], _On the strength of dependent products in the type theory of Martin-L&#246;f_

* [[Peter LeFanu Lumsdaine]], [Strong functional extensionality from weak](http://homotopytypetheory.org/2011/12/19/strong-funext-from-weak) (HoTT blog post)

Discussion of the [[categorical semantics]] in the context of [[homotopy type theory]] is in 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))



See also 

* [[Coq]] code in the [HoTT repository](https://github.com/HoTT/HoTT/blob/master/Coq/Funext.v) and [Peter Lumsdaine's fork](https://github.com/peterlefanulumsdaine/HoTT/blob/master/Coq/Funext.v) (dead link)

[[!redirects function extensionality]]
[[!redirects functional extensionality]]

[[!redirects FunExt]]

[[!redirects morphism extensionality]]
