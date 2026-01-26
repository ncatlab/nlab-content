
> This entry is about the concept in [[category theory]]. For (co)exponential functions in analysis see at _[[exponential map]]_ and _[[coexponential map]]_. 

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

\tableofcontents

## Idea 

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ in a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]]. 

More generally, in a category with [[finite products]], an exponential object $X^Y$ is a [[representing object]] for the functor $\hom(- \times Y, X)$. 

{#YetMoreGenerally} Yet more generally, an exponential object $X^Y$ in a [[category]] $\mathcal{C}$ is a [[representing object]] for the functor $y(X)^{y(Y)}$, where $y \,\colon\, \mathcal{C} \longrightarrow PSh(\mathcal{C})$ denotes the [[Yoneda embedding]] and the latter exponentiation takes place in the [[category of presheaves]] $PSh(\mathcal{C})$, where it always exists (see at *[[closed monoidal structure on presheaves]]).

## Definition 

The above is actually a complete definition, but here we spell it out.

Let $X$ and $Y$ be objects of a [[category]] $C$ such that all binary [[products]] with $Y$ exist.  (Usually, $C$ actually has all binary products.)  Then an __exponential object__ is an object $X^Y$ equipped with an __[[evaluation map]]__ $\mathrm{ev}\colon X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e\colon Z \times Y \to X$, there exists a unique map $u\colon Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times \mathrm{id}_Y}\to X^Y \times Y \stackrel{\mathrm{ev}}\to X $$
equals $e$.

Equivalently, this data can be repackaged as a natural isomorphism $\hom_C(-, X^Y) \cong \hom_C(- \times Y, X)$ (where $\mathrm{ev}$ is the image of the identity arrow on $X^Y$), so that exponential objects are representations of the latter as a [[representable functor]].

The map $u$ is known by various names, such as the _exponential transpose_ or *[[currying]]* of $e$.  It is sometimes denoted $\lambda(e)$ in a hat tip to the [[lambda-calculus]], since in the [[internal logic]] of a cartesian closed category this is the operation corresponding to $\lambda$-abstraction.  It is also sometimes denoted $e^\flat$ (as in music notation), being an instance of the more general notion of [[adjunct]] or [[mate]].

As with other [[universal construction]]s, an exponential object, if any exists, is [[generalized the|unique up to unique isomorphism]].  It can also be characterized as a [[distributivity pullback]].

### Without finite products

In a category without finite products, an exponential object is given by an object $X^Y$ and a universal natural transformation $C(-, X^Y) \times C(-, X) \to C(-, Y)$. See, for instance, [this](https://github.com/punkdit/categories/blob/master/www.mta.ca/cat-dist/archive/2008/08-1#L751-L782) [[categories mailing list]] post by [[Richard Garner]].


## Related notions 

As before, let $C$ be a category and $X,Y\in C$.

* If $X^Y$ exists, then we say that $X$ __exponentiates__ $Y$.

* If $Y$ is such that $X^Y$ exists for all $X$, we say that $Y$ is __exponentiable__ (or *powerful*, cf. Street-Verity [pdf](http://www.emis.de/journals/TAC/volumes/23/3/23-03.pdf)).  Then $C$ is __[[cartesian closed category|cartesian closed]]__ if it has a [[terminal object]] and every object is exponentiable (which requires that all binary products exist too).

* More generally, a morphism $f\colon Y \to A$ is [[exponentiable morphism|exponentiable]] when it is exponentiable in the [[over category]] $C/A$. See [[exponentiable morphism]] for more details.

* Conversely, if $X$ is such that $X^Y$ exists for all $Y$, we say that $X$ is __exponentiating__.  (This requires that $C$ have all binary products.)  Again, $C$ is __cartesian closed__ if it has a terminal object and every object is exponentiating.  (The reader should beware that some authors say "exponentiable" for what is here called "exponentiating.")

Dually, a __[[coexponential object]]__ in $C$ is an exponential object in the [[opposite category]] $C^{op}$.  A __[[cocartesian coclosed category]]__ has all of these (and an [[initial object]]).  Some coexponential objects occur naturally in algebraic categories (such as [[rings]] or [[frames]]) whose opposites are viewed as categories of spaces (such as [[schemes]] or [[locales]]).  Cf. also [[cocartesian closed category]].

{#WhenCIsNotCartesian} When $C$ is not cartesian but merely monoidal, then the analogous notion is that of a [[internal hom|left/right internal hom]].

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

## Properties 

As with other internal homs, the __[[currying]]__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]] of sets. This isomorphism can be internalized to an isomorphism in $C$:
$$(X^Y)^Z \cong X^{Y\times Z}$$
by the [[Yoneda lemma]], it suffices to construct a natural isomorphism between the presheaves they represent:
$$hom_C(W, (X^Y)^Z) \cong hom_C(W\times Z) , X^Y) \cong hom_C((W \times Z) \times Y , X) \cong hom_C(W\times(Y\times Z), X) \cong hom_C(W, X^{Y\times Z}).$$
In fact if we remove the final step, this argument shows that $(X^Y)^Z$ is the exponential of $X$ to the power of $Y\times Z$, showing that exponentiable objects are closed under products. A similar argument shows that $X \cong X^1$ where $1$ is a [[terminal object]]. Therefore any finite product of exponentiable objects is exponentiable.

Other natural isomorphisms that match equations from ordinary algebra include:

*  $(X \times Y)^Z \cong X^Z \times Y^Z$;
*  $1^Z \cong 1$.

Similar representability arguments show that, in a cartesian monoidal category, a product of exponentiating objects is also exponentiating.

Now suppose that $C$ is a [[distributive category]].  Then we have these isomorphisms:

*  $X^{Y + Z} \cong X^Y \times X^Z$;
*  $X^0 \cong 1$.

Here $Y + Z$ is a [[coproduct]] of $Y$ and $Z$, while $0$ is an [[initial object]]. By similar modification as above, this shows that in a distributive category, the exponentiable objects are closed under coproducts.

Note that any cartesian closed category with finite coproducts must be distributive, so all of the isomorphisms above hold in any closed [[2-rig]] (such as [[Set]], of course).

## Related concepts

* [[exponential ideal]]

* [[exponentiable topos]]

* [[reflexive object]]

## References

Discussion with focus on application to [[topological spaces]] and [[compactly generated topological spaces]]:

* {#DayKelly} [[Brian Day]], [[G. Max Kelly]], *On topological quotients preserved by pullback or products*, Mathematical Proceedings of the Cambridge Philosophical Society **67** 3 (1970) 553 - 558  ([doi:10.1017/S0305004100045850](https://doi.org/10.1017/S0305004100045850))

* [[Francis Borceux]], Section 7.1 of: *Categories and Structures*, Vol. 2 of: *[[Handbook of Categorical Algebra]]*, Encyclopedia of Mathematics and its Applications **50** Cambridge University Press (1994) ([doi:10.1017/CBO9780511525865](https://doi.org/10.1017/CBO9780511525865))


Discussion for [[locales]]:

* {#Hyland} [[Martin Hyland]], _Function Spaces in the Category of Locales._ ([doi:10.1080/00927878108822672](https://doi.org/10.1080/00927878108822672))

Discussion for [[internal groupoids]] in [[Top]] ([[topological groupoids]]):

* [[Susan B. Niefield]], [[Dorette A. Pronk]], *Internal groupoids and exponentiability*, Cahiers de topologie et géométrie différentielle catégoriques, [**LX** 4 (2019)](http://cahierstgdc.com/index.php/volume-lx/) ([pdf](http://cahierstgdc.com/wp-content/uploads/2019/10/Niefield-Pronk-LX-4.pdf))

Exponentiable [[relational structures]] are considered in

* [[Jason Parker]], *Exponentiability in categories of relational structures*  (2022) &lbrack;[arXiv:2208:07350](https://arxiv.org/abs/2208.07350)&rbrack;

[[!redirects exponential object]]
[[!redirects exponential objects]]
[[!redirects exponentiable object]]
[[!redirects exponentiable objects]]
[[!redirects powerful object]]
[[!redirects powerful objects]]

[[!redirects exponentiating object]]
[[!redirects exponentiating objects]]

