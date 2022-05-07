
> This entry is about the concept in [[category theory]]. For exponential functions see at _[[exponential map]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ in a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]].


## Definition 

The above is actually a complete definition, but here we spell it out.

Let $X$ and $Y$ be objects of a [[category]] $C$ such that all binary [[products]] with $Y$ exist.  (Usually, $C$ actually has all binary products.)  Then an __exponential object__ is an object $X^Y$ equipped with an __[[evaluation map]]__ $\mathrm{ev}\colon X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e\colon Z \times Y \to X$, there exists a unique map $u\colon Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times \mathrm{id}_Y}\to X^Y \times Y \stackrel{\mathrm{ev}}\to X $$
equals $e$.

The map $u$ is known by various names, such as the _exponential transpose_ or *[[currying]]* of $e$.  It is sometimes denoted $\lambda(e)$ in a hat tip to the [[lambda-calculus]], since in the [[internal logic]] of a cartesian closed category this is the operation corresponding to $\lambda$-abstraction.  It is also sometimes denoted $e^\flat$ (as in music notation), being an instance of the more general notion of [[adjunct]] or [[mate]].

As with other [[universal construction]]s, an exponential object, if any exists, is [[generalized the|unique up to unique isomorphism]].  It can also be characterized as a [[distributivity pullback]].


## Related notions 

As before, let $C$ be a category and $X,Y\in C$.

* If $X^Y$ exists, then we say that $X$ __exponentiates__ $Y$.  As above, the existence of $X^Y$ requires that all binary products with $Y$ exist.

* If $Y$ is such that $X^Y$ exists for all $X$, we say that $Y$ is __exponentiable__ (or *powerful*, cf. Street-Verity [pdf](http://www.emis.de/journals/TAC/volumes/23/3/23-03.pdf)).  Then $C$ is __[[cartesian closed category|cartesian closed]]__ if it has a [[terminal object]] and every object is exponentiable (which requires that all binary products exist too).

* More generally, a morphism $f\colon Y \to A$ is __exponentiable__ (or *powerful*) when it is exponentiable in the [[over category]] $C/A$.  This is equivalent to saying that all pullbacks along $f$ exist and that the resulting [[base change]] functor $f^* : C/A \to C/Y$ has a [[right adjoint]], usually denoted $\Pi_f$ and called a [[dependent product]].  In particular, $C$ is __[[locally cartesian closed category|locally cartesian closed]]__ iff every morphism is exponentiable, iff all pullback functors have right adjoints.  (Sometimes locally cartesian closed categories are also required to have a terminal object, and hence to also be cartesian closed.)

* Conversely, if $X$ is such that $X^Y$ exists for all $Y$, we say that $X$ is __exponentiating__.  (This requires that $C$ have all binary products.)  Again, $C$ is __cartesian closed__ if it has a terminal object and every object is exponentiating.  (The reader should beware that some authors say "exponentiable" for what is here called "exponentiating.")

Dually, a __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^{op}$.  A __[[cocartesian coclosed category]]__ has all of these (and an [[initial object]]).  Some coexponential objects occur naturally in algebraic categories (such as [[rings]] or [[frames]]) whose opposites are viewed as categories of spaces (such as [[schemes]] or [[locales]]).  Cf. also [[cocartesian closed category]].

When $C$ is not cartesian but merely monoidal, then the analogous notion is that of a [[residual|left/right residual]].

## Properties

* If $C$ has equalizers of coreflexive pairs, then any pullback of an exponentiable morphism is exponentiable.  This follows from the [[adjoint triangle theorem]], since the left adjoint $\Sigma_f$ of pullback is [[comonadic functor|comonadic]].

## Examples 

Of course, in any cartesian closed category every object is exponentiable and exponentiating.  In general, exponentiable objects are more common and important than exponentiating ones, since the existence of $X^Y$ is usually more related to properties of $Y$ than properties of $X$.


### Exponentiation of sets and of numbers

In the cartesian closed category [[Set]] of [[set]]s, for $X,S \in Set$ to sets, their exponentiation $X^S$ is the set of [[function]]s $S\to X$.

Restricted to [[finite set]]s and under the [[cardinality]] operation $|-| : FinSet \to \mathbb{N}$ this induces an exponentiation operation on [[natural number]]s

$$
  \left|X^S\right| = |X|^{|S|}
  \,.
$$

This exponentiation operation on numbers $(-)^{(-)} : \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ is therefore the [[decategorification]] of the canonically defined [[internal hom]] of sets. It sends numbers $a,b \in \mathbb{N}$ to the product

$$
  a^b = a \times a \times \cdots \times a \;\; (b \; \text{factors})
  \,.
$$

If $b = 0$ is [[zero]], the expression on the right is 1, reflecting the fact that $0$ is the [[cardinality]] of the [[empty set]], which is the [[initial object]] in [[Set]].

When the natural numbers are embedded into larger [[rig]]s or [[ring]]s, the operation of exponentiation may extend to these larger context. It yields for instance an exponentiation operation on the [[positive real numbers]].


### More examples

* In [[Top]] (the category of _all_ topological spaces), the exponentiable spaces are precisely the [[core-compact spaces]] (see [Day and Kelly](#DayKelly)).  In particular, this includes [[locally compact Hausdorff space]]s.  However, most [[nice category of spaces|nice categories of spaces]] are cartesian closed, so that all objects are exponentiable; note that usually the cartesian product in such categories has a slightly different topology than it does in $Top$.

The condition that a topological space be core-compact (i.e. exponentiable) is in fact a condition on its underlying locale. More precisely, a topological space is core-compact if and only if its underlying locale is a [[continuous poset]]. In fact, a topological space is exponentiable if and only if its underlying locale is exponentiable:

* A [[locale]] is exponentiable if and only if it is a [[continuous poset]] (see [Hyland](#Hyland)) -- this is sometimes taken as the _definition_ of a [[locally compact locale]]). The notion of continuous poset generalizes straightforward to that of [[continuous category]] and [[continuous ∞-category]]. Using these notions, one has analogous characterization of those [[toposes]] and [[(∞,1)-toposes]] which are exponentiable (see [[metastably locally compact locale]] and [[continuous category]] as well as [[exponentiable topos]]).

* In [[algebraic set theory]] (see [[category with class structure]] for one example) one often assumes that only small objects (and morphisms) are exponentiable. analogous to how in material [[set theory]] one can talk about the class of functions $Y\to X$ when $Y$ is a set and $X$ a class, but not the other way round.

* In a [[type theory]] with [[dependent product]]s, every display morphism is exponentiable in the category of [[context]]s ---even in a type theory without identity types, so that not every morphism is display and the relevant slice category need not have all products.

* In a [[functor category]] $D^C$, a [[natural transformation]] $\alpha:F\to G$ is exponentiable if it is [[cartesian natural transformation|cartesian]] and each component $\alpha_c:F c \to G c$ is exponentiable in $D$.  Given $H\to F$, we define $\Pi_\alpha(H)(c) = \Pi_{\alpha_c}(H c)$; then for $u:c\to c'$ to obtain a map $\Pi_{\alpha_c}(H c) \to \Pi_{\alpha_{c'}}(H c')$ we need a map $\alpha_{c'}^*(\Pi_{\alpha_c}(H c)) \to H c'$.  But since $\alpha$ is cartesian, $\alpha_{c'}^*(\Pi_{\alpha_c}(H c)) \cong \alpha_c^* (\Pi_{\alpha_c}(H c))$, so we have the counit $\alpha_c^* (\Pi_{\alpha_c}(H c)) \to H c$ that we can compose with $H u$.  (This is certainly not an if-and-only-if, however: for instance, if $C$ is small, then all morphisms of $Set^C$ are exponentiable, whether or not they are cartesian.)

However, exponentiating objects do matter sometimes.

* In [Abstract Stone Duality](http://www.paultaylor.eu/ASD/), [[Sierpinski space]] is exponentiating.

* [[Toby Bartels]] has [argued](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023187) that [[predicative mathematics]] can have a set of [[truth value]]s as long as this set is not exponentiating (or even exponentiates only [[finite set]]s).

* A [[dialogue category]] is a [[symmetric monoidal category]] equipped with the non-cartesian monoidal analogue of an exponentiating object.

### Relative Examples

Let $\mathcal{C}$ be a category with finite limits and $f: C \to D$ a morphism in $\mathcal{C}$. Then $f$ is exponentiable as an object of the slice category $\mathcal{C}\downarrow D$ if and only if the [[base change]] functor $f^\ast: \mathcal{C} \downarrow D \to \mathcal{C} \downarrow C$ has a right adjoint. In this case, we say that $f$ is an [[exponentiable morphism]] in $\mathcal{C}$.

* The exponentiable morphisms in $Top$ were characterized by [Niefield](#Niefield82). In particular, a subspace inclusion $C \to D$ is exponentiable if and only if it is [[locally closed]].

* The exponentiable morphisms in $Locale$ and $Topos$ which are embeddings were also characterized by [Niefield](#Niefield81). It seems(?) that no complete characterization of exponentiable morphisms in $Locale$ or $Topos$ appears in the literature.

* The exponentiable morphisms in $Cat$ are the [[Conduché functors]].

## Properties 

As with other internal homs, the __[[currying]]__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]] of sets.  By the usual [[Yoneda lemma|Yoneda]] arguments, this isomorphism can be internalized to an isomorphism in $C$:
$$ (X^Y)^Z \cong X^{Y\times Z}. $$
Similarly, $X \cong X^1$, where $1$ is a [[terminal object]].  Thus, a product of exponentiable objects is exponentiable.

Other natural isomorphisms that match equations from ordinary algebra include:

*  $(X \times Y)^Z = X^Z \times Y^Z$;
*  $1^Z \cong 1$.

These show that, in a cartesian monoidal category, a product of exponentiating objects is also exponentiating.

Now suppose that $C$ is a [[distributive category]].  Then we have these isomorphisms:

*  $X^{Y + Z} \cong X^Y \times X^Z$;
*  $X^0 \cong 1$.

Here $Y + Z$ is a [[coproduct]] of $Y$ and $Z$, while $0$ is an [[initial object]].  Thus in a distributive category, the exponentiable objects are closed under coproducts.

Note that any cartesian closed category with finite coproducts must be distributive, so all of the isomorphisms above hold in any closed [[2-rig]] (such as [[Set]], of course).


## Related concepts

* [[exponential ideal]]

* [[exponentiable topos]]

* [[reflexive object]]

## References

  * {#Niefield82} [[Susan Niefield]], _Cartesianness: topological spaces, uniform spaces, and affine schemes._, Journal of Pure and Applied Algebra, 23.2, 1982, pp. 147-167.(<a href="https://doi.org/10.1016/0022-4049(82)90004-4">doi</a>)

  * {#Niefield81} [[Susan Niefield]], _Cartesian inclusion: locales and toposes._, Communications in Algebra, 9.16, 1981, pp. 1639-1671.  [doi](https://doi.org/10.1080/00927878108822672)

  * {#Hyland} [[Martin Hyland]], _Function Spaces in the Category of Locales._, [available from Hyland's website](https://doi.org/10.1080/00927878108822672)

 * {#DayKelly} [[Brian Day]] and [[G. Max Kelly]], _On topological quotients preserved by pullback or
products_, [doi](https://doi.org/10.1017/S0305004100045850)

[[!redirects exponential object]]
[[!redirects exponential objects]]
[[!redirects exponentiable object]]
[[!redirects exponentiable objects]]
[[!redirects exponentiable morphism]]
[[!redirects exponentiable morphisms]]
[[!redirects powerful morphism]]
[[!redirects powerful morphisms]]
[[!redirects powerful object]]
[[!redirects powerful objects]]

[[!redirects exponentiating object]]
[[!redirects exponentiating objects]]

