
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The classical _Brown representability theorem_ ([Brown 62](#Brown62)) says that certain contravariant [[functors]] on the [[homotopy category]] are [[representable functor|representable]].  This is used, for instance, to show that any [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]] is representable by a [[spectrum]].

There are various generalizations, such as to homotopy categories of other [[model category|model categories]] ([Brown 65](#Brown65)) and to [[triangulated category|triangulated categories]].  Note, however, that all of these generalizations require either

* [[group]] structure on the values of the functor, as is the case for an (abelian) cohomology theory, and as would be the case for a represented functor in any [[additive category]], OR

* the existence of a [[strong generator]] in the homotopy category in question.

In particular, there is no Brown representability theorem for functors from the homotopy category of pointed not-necessarily-connected spaces to pointed sets, or for functors from the homotopy category of unpointed spaces to sets.  In fact, there are counterexamples in these two cases.


## Classical Brown representability

Let $Ho(Top_*^c)$ denote the homotopy category of pointed, connected, [[topological spaces]] under [[weak homotopy equivalence]] --- or equivalently the homotopy category of pointed connected [[CW complexes]] under homotopy equivalence.  Then $Ho(Top_*^c)$ has [[coproducts]] (given by wedge sums) and also [[weak limit|weak pushouts]] (namely, [[homotopy pushouts]]).

+-- {: .num_theorem #Classical}
###### Theorem
**(Brown)**
If a functor $F:Ho(Top_*^c)^{op} \to Set_*$ [[preserved limit|takes]] coproducts to products, and weak pushouts to weak pullbacks, then it is [[representable functor|representable]].  That is, there is a pointed connected CW-complex $(Y,y_0)$ and a universal element $u\in F(Y,y_0)$ such that $T_u:[-,(Y,y_0)]\to F$ is a natural isomorphism.
=--

Note that it is immediate that every representable functor has the given properties; the nontrivial statement is that these properties already characterize representable functors.

When the theorem is stated in terms of CW complexes, the second property (taking weak pushouts to weak pullbacks) is often phrased equivalently as:

* The **Mayer-Vietoris axiom**: For every [[CW triad|triad]] $(X; A_1, A_2)$ of CW-spaces (with $A_1\cup A_2 = X$) and any elements $x_1\in F(A_1)$, $x_2\in F(A_2)$ such that $x_1|A_1\cap A_2 = x_2|A_1\cap A_2$, there exists $y\in F(X)$ such that $y|A_1 = x_1$ and $y|A_2 = x_2$.

## Generalizations

### For $RO(G)$-graded equivariant cohomology
 {#ForEquivariantCohomology}

The generalization of the Brown representability theorem to [[equivariant cohomology]] says that [[RO(G)-grading|RO(G)-graded]] equivariant cohomology is represented by [[genuine G-spectra]] (e.g. [May 96, chapter XIII.3](#May96)).

### Categorical Brown representability
 {#CategoricalBrownRepresentability}


Let $C$ be a [[category]] and $C_0$ an [[essentially small category|essentially small]] [[full subcategory]] such that

* $C$ has coproducts, and $C_0$ is closed under finite coproducts.
* $C$ and $C_0$ have weak pushouts and the inclusion preserves them.
* $C$ has weak colimits of sequences $X_0 \to X_1 \to X_2 \to\dots$, which are taken to actual colimits by $C(Z,-)$ for any $Z\in C_0$ (that is, the objects of $C_0$ are [[compact object|compact]] in some weak sense).

For example, $C$ could be the homotopy category $Ho(Top_*)$ of pointed spaces (under weak homotopy equivalence), with $C_0$ the full subcategory of (spaces of the homotopy type of) finite [[CW complexes]].  Motivated by this example, we write $[-,-]$ for hom-sets in $C$.

Let $\bar{C_0}\subseteq C$ denote the full subcategory of those $Y\in C$ such that for any $f:Y\to Y'$, if the induced map $[X,Y] \to [X,Y']$ is bijective for all $X\in C_0$, then $f$ is an isomorphism.  If $C=Ho(Top_*)$ as above, then $\bar{C_0}$ is the category of pointed *connected* spaces.

+-- {: .num_theorem #Categorical}
###### Theorem
**(Brown)**
With $(C,C_0$ as above, let $F:C^{op}\to Set$ be a functor which takes coproducts to products and weak pushouts to weak pullbacks.  Then there exists $Y\in C$ and a natural transformation $T:[-,Y] \to F$ such that
* $T_X$ is an isomorphism for all $X\in C_0$.
* If $Y\in \bar{C_0}$, then $T_X$ is an isomorphism for all $X$.
=--

### For model categories 
 {#VersionForModelCategories}

Let $C$ be a [[simplicial model category]] with a [[zero object]] and such that there is a set $S$ of [[cofibrant object|cofibrant]] [[compact objects]] such that the [[weak equivalences]] in $C$ are precisely the $S$-[[local equivalence]]s.

+-- {: .num_theorem}
###### Theorem
**(Jardine)**
Let $F : C^{op} \to Set_{*}$ be a [[homotopical functor]] to the category of pointed sets on $C^{op}$ such that

1. $F$ preserves small [[coproduct]]s of cofibrant objects (including preserving the zero object).

1. **(Mayer-Vietoris property)** $F$ takes any [[pushout]] diagram

   $$
     \array{
       A &\to& X
       \\
       \downarrow^i && \downarrow 
       \\
       B &\to& B \coprod_A X,
     }
   $$  

   with all objects cofibrant and $i$ a cofibration, to a weak pullback.

Then $F$ is [[representable functor|representable]].
=--

This follows essentially immediately from Theorem \ref{Categorical} applied to $Ho(C)$.  Jardine also proves a more refined version (see references).

## Counterexamples

In some places, one can find the classical Brown representability stated without the restricted to *connected* pointed spaces.  However, this version is false, as is the analogous statement for unpointed spaces.

In the paper of Freyd-Heller cited below, it is show that if $G$ is [[Thompson's group F]], with $g:G\to G$ its canonical endomorphism, then $g$ does not [[split idempotent|split]] in the quotient of [[Grp]] by conjugacy.  Since the quotient of [[Grp]] by conjugacy embeds as the full subcategory of the unpointed homotopy category $Ho(Top)$ on connected [[homotopy 1-types]], we have an endomorphism $B g:B G \to B G$ of the [[classifying space]] of $G$ which does not split in $Ho(Top)$.

Thus, if $F:Ho(Top)^{op} \to Set$ splits the idempotent $[-,B g]$ of $[-,B G]$, then $F$ satisfies the hypotheses of the Brown representability theorem (being a [[retract]] of a representable functor), but is not representable.  A similar argument using $B G_+$ applies to $Ho(Top_*)$.

There is also another example due to Heller, which fais to be representable for cardinality reasons.

* MO questions [non-connected spaces](http://mathoverflow.net/questions/104866/brown-representability-for-non-connected-spaces), [unpointed spaces](http://mathoverflow.net/questions/11456/unpointed-brown-representability-theorem)
* [blog post](http://golem.ph.utexas.edu/category/2012/08/brown_representability.html)


## Related concepts

* [[Landweber exact functor theorem]]

## References

The original theorem was proven in

* {#Brown62} [[Edgar Brown]], _Cohomology theories_, Annals of Mathematics, Second Series 75: 467&#8211;484 (1962)

The categorical generalization was proven in

* {#Brown65} [[Edgar Brown]], _Abstract homotopy theory_, Trans. AMS 119 no. 1 (1965)

The model-categorical version, with applications to [[∞-stacks]] -- or rather to the standard  [[models for ∞-stack (∞,1)-toposes]] in terms of the standard [[model structure on simplicial presheaves]] -- is given in

* [[Rick Jardine]], _[[JardineBrownrep.pdf:file]]_ 

Warning: this is probably implicitly about [[reduced cohomology theory]], as the functors considered always assign the trivial result to the [[terminal object]] (the [[point]] in the usual examples).

The case of [[RO(G)-grading|RO(G)-graded]] [[equivariant cohomology]] theory is discussed for instance in

* {#May96} [[Peter May]], chapter XIII.3 of _Equivariant homotopy and cohomology theory_, CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. ([pdf](http://www.math.uchicago.edu/~may/BOOKS/alaska.pdf))


The counterexamples to nonconnected and unpointed Brown representability are from

* [[Peter Freyd]] and [[Alex Heller]], _Splitting homotopy idempotents. II._ J. Pure Appl. Algebra 89 (1993), no. 1-2, 93&#8211;106.

A review in the context of [[chromatic homotopy theory]] is in 

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010, Lecture 17 _Phantom maps_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture17.pdf)) 
 {#Lurie}

The relation to [[Grothendieck context|Grothendieck contexts]] ([[six operations]]) is highlighted in 

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc. 9 (1996), 205-236 ([web](http://www.ams.org/journals/jams/1996-9-01/S0894-0347-96-00174-9/))
 {#Neeman96}



[[!redirects Brown representability]]

[[!redirects Brown's representability theorem]]