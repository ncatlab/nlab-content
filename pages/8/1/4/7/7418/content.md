
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

An **elegant Reedy category** is a [[Reedy category]] $R$ such that the following *equivalent* conditions hold

* For every [[monomorphism]] $A\hookrightarrow B$ of [[presheaves]] on $R$ and every $x\in R$, the induced map $A_x \amalg_{L_x A} L_x B \to B_x$ is a monomorphism.

* Every [[span]] of codegeneracy maps in $R_-$ has an [[absolute colimit|absolute]] [[pushout]] in $R_-$.

* Both the following conditions hold:

  1. For every monomorphism $A\hookrightarrow B$ of presheaves on $R$, every nondegenerate element of $A$ remains nondegenerate in $B$.

  1. Every element of a presheaf $R$ is a degeneracy of some nondegenerate element in a unique way.

=--

## Properties

The principal theorem about elegant Reedy categories is that the [[Reedy model structure]] on [[presheaves]] (i.e. contravariant diagrams) over an elegant Reedy category coincides with the [[injective model structure]].  This is not true for presheaves valued in *any* model category, only well-behaved ones.  We clarify the necessary conditions by building up to this theorem in stages, adding hypotheses on the codomain of the presheaves as necessary.

### Degeneracies are split

+-- {: .num_lemma #DegSplit}
###### Lemma
If $R$ is elegant, then every codegeneracy map (i.e. morphism in $R_-$) is a [[split epimorphism]].
=--
+-- {: .proof}
###### Proof
Let $f:x\to y$ be a codegeneracy map; then the span $y \xleftarrow{f} x \xrightarrow{f} y$ has an absolute pushout, consisting of say $g:y\to z$ and $h:y\to z$ with $g f = h f$.  This absolute pushout is preserved by $R(z,-)$, so $1_z\in R(z,z)$ must be the image under $g$ or $h$ of some map $s:z\to y$; WLOG say it is $g$, so we hav $1_z = g s$.  Now we have $s h:y\to y$ and $1_y$ such that $g s h = h = h 1_y$, and our absolute pushout is preserved by $R(y,-)$, so there must be a zigzag of elements in $R(y,z)$ relating $s h$ to $1_y$.  At one end of that zigzag, there must be a $t:y\to x$ such that $f t = 1_y$; hence $f$ is split epi.
=--

### Degeneracies in subobjects

+-- {: .num_lemma #DegSub}
###### Lemma
Let $R$ be elegant and $f:x\to y$ a codegeneracy in $R$.  Let $M$ be any category, and $\mu:A\to B$ a monomorphism in $M^{R^{\mathrm{op}}}$.  Then the following naturality square is a pullback:
$$\array{ A_y & \xrightarrow{A_f} & A_x \\
  {}^{\mu_y}\downarrow & & \downarrow^{\mu_x} \\
  B_y & \xrightarrow{B_f} & B_x  }$$
=--
+-- {: .proof}
###### Proof
This depends only on the fact that $f$ is split epi in $R$.  Let $s:y\to x$ be a section of it, and let $P$ be the pullback of $B_f$ and $\mu_x$, with projections $p:P\to A_x$ and $q:P\to B_y$ with $\mu_x p = B_f q$, and an induced map $\phi:A_y \to P$ such that $p \phi = A_f$ and $q\phi = \mu_y$.

We claim that $A_s p : P \to A_y$ is an inverse of $\phi$, making it an isomorphism.  On the one hand we have $A_s p \phi = A_s A_f = A_{f s} = 1$.  On the other, to show that $\phi A_s p = 1$ it suffices to show that $p \phi A_s p = p$ and $q \phi A_s p = q$.  For the first, since $\mu_x$ is monic, it suffices to show $\mu_x p \phi A_s p = \mu_x p$, and for that we have
$$ \mu_x p \phi A_s p = B_f q \phi A_s p = B_f \mu_y A_s p = B_f B_s \mu_x p = B_{f s} \mu_x p = \mu_x p. $$
And for the second, we have
$$q \phi A_s p = \mu_y A_s p = B_s \mu_x p = B_s B_f q = B_{f s} q = q. $$
=--

+-- {: .num_lemma #LatchSub}
###### Lemma
Let $R$ be elegant, $M$ a category with pullback-stable colimits, and $\mu:A\to B$ a monomorphism in $M^{R^{\mathrm{op}}}$.  Then for any object $x\in R$, the following square is a pullback, where $L_x$ denotes the Reedy latching object at $x$:
$$\array{ L_x A & \to & A_x \\
  {}^{L_x \mu}\downarrow & & \downarrow^{\mu_x} \\
  L_x B & \to & B_x.  }$$
=--
+-- {: .proof}
###### Proof
The map $L_x B \to B_x$ is by definition the colimit in $M/B_x$ of a diagram whose objects are morphisms of the form $B_f : B_y \to B_x$, for $f$ a codegeneracy.  By the Lemma \ref{DegSub}, each of these pulls back along $\mu_x$ to $A_f : A_y \to A_x$, forming the corresponding diagram whose colimit is $L_x A \to A_x$, and by assumption the pullback preserves the colimit.
=--

### All presheaves are "Reedy monomorphic"

+-- {: .num_lemma #ReedyCofibrant}
###### Lemma
Let $R$ be elegant and let $M$ be an [[infinitary-coherent category]].  Then for any $x\in R$ and $A\in M^{R^{\mathrm{op}}}$, the map $L_x A \to A_x$ is a monomorphism.
=--
+-- {: .proof}
###### Proof
We use the terminology from the page [[∞-ary exact category]].  Consider the [[sink]] with target $A_x$ consisting of all morphisms $A_f : A_y \to A_x$ indexed by nonidentity codegeneracies $f$ with domain $x$.  By assumption, for any two such $f:x\to y$ and $f':x\to y'$ there is an absolute pushout $g:y\to z$ and $g':y'\to z$.  By absoluteness, $A_z$ is the pullback $A_y \times_{A_x} A_y$.  Thus, the images of these absolute pushouts form the *kernel* of this sink.

Now $L_x A$ is the colimit of the diagram whose objects are $A_y$ indexed by such $f:x\to y$ and whose morphisms are $A_g: A_{y'} \to A_{y}$ for $g:y\to y'$ a codegeneracy with $g f = f'$.  In this case, by the universal property of pullback, we have a unique map from $A_{y'}$ to $A_z$, where $z$ is the absolute pushout of $f$ and $f'$.  Thus, a cocone under the above kernel is also a cocone under this diagram, and the converse is easy to see.  Hence, $L_x A$ is the quotient of the above kernel.

However, in any infinitary-regular category, the quotient of the kernel of a sink is exactly the extremal-epic / monic factorization of that sink.  Therefore, the induced map $L_x A \to A_x$ is monic.
=--

### Reedy = injective

+-- {: .num_theorem #RelativeLatching}
###### Theorem
If $R$ is elegant and $M$ is a [[Grothendieck topos]], then for any $x\in R$ and monomorphism $\mu:A\to B$ in $M^{R^{\mathrm{op}}}$, the induced map $L_x B \sqcup_{L_x A} A_x \to B_x$ is monic.
=--
+-- {: .proof}
###### Proof
Since Grothendieck toposes are infinitary-coherent, by Lemma \ref{ReedyCofibrant} $L_x B\to B_x$ is monic.  By assumption $A_x \to B_x$ is monic.  And since Grothendieck toposes have pullback-stable colimits, by Lemma \ref{LatchSub} the square
$$\array{ L_x A & \to & A_x \\
  {}^{L_x \mu}\downarrow & & \downarrow^{\mu_x} \\
  L_x B & \to & B_x.  }$$
is a pullback.  In other words, $L_x A$ is the [[intersection]] of the subobjects $L_x B$ and $A_x$ of $B_x$.  But in any [[coherent category]], the pushout of two subobjects over their intersection is their [[union]], and hence in particular a subobject of their common codomain.
=--

+-- {: .un_cor #ReedyIsInjective}
###### Corollary
If $R$ is elegant and $M$ is a [[Cisinski model category]], then the [[Reedy model structure]] on $M^{R^{\mathrm{op}}}$ coincides with the [[injective model structure]].
=--
+-- {: .proof}
###### Proof
By definition, they have the same [[weak equivalences]], so it suffices to show that their classes of cofibrations coincide.  But every Reedy cofibration in any Reedy model structure is an injective (i.e. objectwise) cofibration, and the converse is Theorem \ref{RelativeLatching}.
=--

The most common application is when $M = SSet$.  Thus, for instance, every simplicial presheaf on an elegant Reedy category is Reedy cofibrant.


## Examples

* The [[simplex category]] $\Delta$ is an elegant Reedy category.

* Joyal's [[Theta category|disk categories]] $\Theta_n$ are elegant Reedy categories.

* Every [[direct category]] is a Reedy category with no degeneracies, hence trivially an elegant one.

* If $X$ is any presheaf on an elegant Reedy category $R$, then the opposite of its [[category of elements]] $(el X)^{op}$ is again an elegant Reedy category.  This is fairly easy to see from the fact that $Set^{el X}$ is equivalent to the slice category $Set^{R^{op}}/X$.

* Every [[EZ-Reedy category]] is elegant.

Note that unlike the notion of [[Reedy category]], the notion of elegant Reedy category is not self-dual: if $R$ is elegant then $R^{op}$ will not generally be elegant.

## Related concepts

* [[generalized Reedy category]]

* [[Reedy model structure]]


## References

* [[Julie Bergner]] and [[Charles Rezk]], *Reedy categories and the $\Theta$-construction*, [arXiv:1110.1066](http://arxiv.org/abs/1110.1066)

Elegant Reedy categories are useful to model [[homotopy type theory]].

* {#Shulman12} [[Mike Shulman]], _The univalence axiom for elegant Reedy presheaves_ ([arXiv:1307.6248](http://arxiv.org/abs/1307.6248))

* {#Shulman12} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science, Volume 25, Issue 5 ( _From type theory and homotopy theory to Univalent Foundations of Mathematics_ ) June 2015 ([arXiv:1203.3253](https://arxiv.org/abs/1203.3253), [doi:/10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565))

* Benno van den Berg and Ieke Moerdijk, *W-types in homotopy type theory*, [PDF](http://www.staff.science.uu.nl/~berg0002/papers/WinHoTT.pdf)

[[!redirects elegant Reedy categories]]