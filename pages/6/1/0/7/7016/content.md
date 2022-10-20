
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

### In set theory

In [[set theory]], function extensionality states that for all sets $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, if, for all elements $x \in A$, $f(x) = g(x)$, then $f = g$. 

There is another definition of function extensionality: for all sets $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, if, for all elements $x \in A$ and $y \in A$ such that $x = y$, $f(x) = g(y)$, then $f = g$. 

### In category theory

Since sets and functions form a [[category]], the set theory definition of function extensionality could be generalized to any [[category]] with a [[terminal object]]. Function extensionality corresponds to the fact that the [[terminal object]] is an [[extremal generator]] in [[category]], and is one of the conditions for making a [[pretopos]] a [[well-pointed pretopos]]. 

In additon, function extensionality in category theory is true in any [[concrete category]] $\mathcal{C}$. The axiom could be called "morphism extensionality"; however, in all concrete categories, the morphisms are functions between sets. 

### In type theory

In [[intensional type theory]], [[equality]] is represented by the [[identity type]], and furthermore, there might be more than one element of the identity type in intensional type theory, so a naive translation of function extensionality into intensional type theory doesn’t result in the right statement.

Instead we have the following:

For all types $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, there are two canonical functions which one could use for function extensionality

$$\mathrm{happly}(f, g):(f =_{A \to B} g) \to \prod_{x:A} f(x) =_B g(x)$$

inductively defined by 

$$\mathrm{happly}(f,f)(\mathrm{refl}_{A \to B}(f)) \equiv \lambda (x:A).\mathrm{refl}_B(f(x)):\prod_{x:A} f(x) =_B f(x)$$

and

$$\mathrm{happly}(f, g):(f =_{A \to B} g) \to \left(\prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} f(x) =_B g(y)\right)$$

inductively defined by 

$$\mathrm{happly}(f,f)(\mathrm{refl}_{A \to B}(f)) \equiv \lambda (x:A).\lambda (x:A).\lambda (\mathrm{refl}_A(x):x =_A x).\mathrm{refl}_B(f(x)):\prod_{x:A} \prod_{x:A} \prod_{\mathrm{refl}_A(x):x =_A x} f(x) =_B f(x)$$

The two definitions of $\mathrm{happly}$ become the same under [[singleton contractibility]]. This second definition behaves better with the [[action on identifications]]. 

In general, both functions $\mathrm{happly}(f, g)$ are not [[equivalences of types]] in [[intensional type theory]]: two functions could be defined in different ways, and thus be intensionally different, yet produce the same values on all inputs (i.e. be extensionally the same).

Function extensionality is then the statement that the function $\mathrm{happly}(f, g)$ is an [[equivalence of types]] for all functions $f:A \to B$ and $g:A \to B$. 

$$\mathrm{funext}(f, g):\mathrm{isEquiv}(\mathrm{happly}(f, g))$$

### Definitional function extensionality

One could replace the equivalences of types above with [[definitional equality]] of types, which results in **definitional function extensionality**. Applied to each definition, definitional function extensionality states that for all all types $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$

$$f =_{A \to B} g \equiv \prod_{x:A} f(x) =_B g(x)$$

and 

$$f =_{A \to B} g \equiv \prod_{x:A} \prod_{y:A} \prod_{p:x =_A y} f(x) =_B g(y)$$

respectively. The second version of definitional function extensionality holds in [[higher observational type theory]]

## Properties

### Categorical semantics 

Translating the type theoretic definition into its [[categorical semantics]], the term $\eta$ gives a map 

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

* [[extensionality]]

* [[homotopy]]

* [[concrete category]]

* [[prefunction]]

## References

An introduction to the relevant notions and a guided walk through the formal proof that univalence implies functional extensionality is at

* {#BauerLumsdaine} [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_
  

A discussion of various flavors of function extensionality, and how to move between them, can be found in

* [[Richard Garner]], _On the strength of dependent products in the type theory of Martin-L&#246;f_

* [[Peter LeFanu Lumsdaine]], [Strong functional extensionality from weak](http://homotopytypetheory.org/2011/12/19/strong-funext-from-weak) (HoTT blog post)

For definitional function extensionality in higher observational type theory, see

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

Discussion of the [[categorical semantics]] in the context of [[homotopy type theory]] is in 

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))



See also 

* [[Coq]] code in the [HoTT repository](https://github.com/HoTT/HoTT/blob/master/Coq/Funext.v) and [Peter Lumsdaine's fork](https://github.com/peterlefanulumsdaine/HoTT/blob/master/Coq/Funext.v) (dead link)

[[!redirects function extensionality]]
[[!redirects functional extensionality]]

[[!redirects FunExt]]

[[!redirects morphism extensionality]]
