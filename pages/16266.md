
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In elementary algebra (or more generally in a [[ring]]), [[multiplication]] distributes over [[addition]], meaning that
$$ a\cdot (b+c) = (a\cdot b) + (a\cdot c)$$
and dually.  Since multiplication and addition are a [[decategorification]] of [[products]] and [[coproducts]] in a category, we can categorify this relationship to say what it means for products to distribute over coproducts in any category.  More generally, we can talk about arbitrary [[limits]] distributing over [[colimits]].  Note that this is *not* the same as limits [[commutativity of limits and colimits|commuting]] with colimits, although in some cases they are related.

## Definitions

### Explicitly using limits and colimits

Given [[small categories]] $I$ and $K$, for any [[diagram]] $D\colon I\times K\to C$ in a [[category]] $C$ that admits all necessary [[limits]] and [[colimits]] we have a [[morphism]]
$$f\colon colim_K lim_I D \to lim_I colim_K D$$
induced using the universal property of $colim_K$ and $lim_I$ by the family of composites
$$ lim_I D(-,k) \to D(i,k) \to colim_K D(i,-) $$
of the limit projection for $i\in I$ and the colimit injection for $k\in K$.
Recall that $I$-[[limits]] are said to [[commutativity of limits and colimits|commute]] with $K$-[[colimits]] if and only if $f$ is an [[isomorphism]] for any $D$.

Now we note that $f$ factors as a [[composition]]
$$colim_K lim_I D \xrightarrow{g} colim_{K^I} lim_I D' \xrightarrow{h} lim_I colim_K D.$$
Here $K^I$ is the [[functor category]] and $D'\colon I\times K^I\to C$ is obtained from $D$ by [[precomposition]] with the functor $(\pi_1,ev) : I\times K^I \to I\times K$ that sends a pair $(i,s)$ to $(i,s(i))$.  The map $g$ is induced by the diagonal functor $K\to K^I$ sending each $k$ to the corresponding [[constant functor]], while $h$ is defined by the universal properties of $colim_{K^I}$ and $lim_I$ from the family of composites
$$ lim_I D'(-,s) \to D'(i,s) = D(i,s(i)) \to colim_K D(i,-) $$
of the limit projection for $i\in I$ and the colimit injection for $c(i)\in K$.  We say that **$I$-limits distribute over $K$-colimits** if $h$ is an isomorphism for any $D$.

More generally, we can allow $K$ to vary with $i$, becoming a functor $K\colon I\to Cat$.  Now instead of $K^I$ we use the limit category $lim_I K$, and the diagram $D$ is defined on the [[Grothendieck construction]] ([[lax colimit]]) $\int^I K$.  We recover the above definition when $K$ is a [[constant functor]].

If $\mathcal{K}$ is a class of small categories rather than a single one, we say that **$I$-limits distribute over $\mathcal{K}$-colimits** in a category $C$ if the corresponding map is an isomorphism for any $K:I\to Cat$ taking values in $\mathcal{K}$.  For instance, if $\mathcal{K}$ is the class of all [[discrete categories]], we obtain the notion of $I$-limits distributing over coproducts, and so on.  If instead $I$-limits distribute over $K$-colimits for any single $K\in \mathcal{K}$, we may say instead that "$I$-limits distribute over uniform $K$-limits."

+--{: .standout}
I don't know whether distributivity over uniform colimits is actually any weaker, but if it is, then the non-uniform version seems more correct.
=--

### For Kan extensions

Yet more generally, let $u : I\to J$ be any [[Grothendieck fibration]] and $v : K\to I$ a Grothendieck opfibration.  Since fibrations are [[exponentiable functors]], we can form the [[distributivity pullback]]
$$ \array{ X & \xrightarrow{p} & K & \xrightarrow{v} & I \\ ^q\downarrow &&&& \downarrow^u \\ Y && \xrightarrow{r} && J } $$
Thus $Y$ is the [[dependent product]] $\Pi_I K$, and $X = I\times_J \Pi_I K$, while the functor $p:X\to K$ is "evaluation".  Now in any sufficiently complete category, there is a [[Beck-Chevalley]] isomorphism
$$ r^* \circ Ran_u \cong Ran_q \circ p^* \circ v^*. $$
This is because any [[pullback]] of a fibration is an [[exact square]].  This isomorphism has a [[mate]]
$$ Lan_r \circ Ran_q \circ p^* \to Ran_u \circ Lan_v $$
and we say that **right Kan extensions along $u$ distribute over left Kan extensions along $v$** if this mate is an isomorphism.

If $J=1$ then this reduces to the above non-uniform notion, where $K\to I$ is the [[Grothendieck construction]] of a functor $I\to Cat$.  Moreover, since isomorphisms of $J$-diagrams are pointwise, right and left Kan extensions along fibrations and opfibrations respectively are given by fiberwise limits and colimits respectively, and dependent exponentials are preserved by pullback (the Beck-Chevalley condition), we can say that right Kan extensions along $u$ distribute over left Kan extensions along $v$ if and only if the above non-uniform distributivity condition holds for the fibers of $v$ over each object of $J$.

The formulation in terms of Kan extensions generalizes naturally to [[derivators]], and can also be [[internalization|internalized]] to [[internal categories]] and [[fibrations]] in any [[locally cartesian closed category]].

### For sound doctrines

(See Section 6 in [ABLR](#ABLR).)

Given a [[sound doctrine]] $D$ of limits,
we have the associated notions of $D$-limits,
$D$-filtered colimits,
and
$D$-filtered cocompletion $D-Ind(C)$ of a category $C$
together with the associated colimit functor $colim\colon D-Ind(C)\to C$.

We say that some class of limits _distributes over $D$-filtered colimits_ if the functor colim preserves these limits.

See Appendix A in [AR](#AR) for a comparison of this definition to the above explicit definition in the special case of distributivity of [[filtered colimits]]
over [[small limits]] in [[locally finitely presentable categories]]
and distributivity of [[sifted colimits]] over [[small limits]]
in [[varieties of algebras]].

## Relation to commutativity of limits and colimits

Observe that distributivity is asymmetric with respect to limits and colimits, whereas [[commutativity of limits and colimits]] is a symmetric notion.  In some cases, however, distributivity and commutativity are equivalent.  This happens exactly when the above functor $g$ is an isomorphism, which is to say that the [[diagonal]] map $K\to K^I$ is a [[final functor]].

Thus, for instance, finite limits distribute over (uniform) filtered colimits if and only if finite limits commute with filtered colimits.  The same is true for finite products and sifted colimits.


## Examples

### Finite products

The distributivity of [[finite products]] over arbitrary [[coproducts]] is the most classical version.  See [[distributivity for monoidal structures]] for various generalizations.

More generally, finite products distribute over arbitrary colimits in any [[cartesian closed category]], such as [[Set]].


### Filtered colimits

If $D$ is the doctrine of finite limits,
then $D$-filtered colimits are precisely filtered colimits
and the $D$-filtered cocompletion of $C$ is $Ind(C)$,
the category of [[Ind-objects]] in $C$.

According to Definition 5.11 in [ALR](#ALR),
a category is _precontinuous_
if it admits small limits and filtered colimits,
and the functor $colim: Ind(C)\to C$ is continuous.

According to Theorem 2.1 in \cite{ARVloc},
a category is precontinuous if and only if it has small [[limits]]
and [[filtered colimits]], [[filtered colimits]] commute with finite [[limits]],
and small [[products]] distribute over [[filtered colimits]].

In particular, any [[locally finitely presentable category]], equivalently the category of algebras
over some finitary [[essentially algebraic theory]],
is precontinuous.
See Theorem 5.13 and Lemma 5.14 in [ALR](#ALR).

In fact, as shown in [ALR](#ALR), precontinuous categories with continuous functors that preserve filtered colimits
form the accessible [[equational hull]] of the bicategory
of [[locally finitely presentable categories]] and continuous functors
that preserve filtered colimits.

### Sifted colimits

If $D$ is the doctrine of finite products,
then $D$-filtered colimits are precisely [[sifted colimits]]
and the $D$-filtered cocompletion of $C$ is $Sind(C)$,
the [[nonabelian derived category]] of $C$.

According to Definition 4.5 in [ALRalg](#ALRalg),
a category is _algebraically exact_
if it admits small limits and sifted colimits,
and the functor $colim: Sind(C)\to C$ is continuous.
In particular (Example 5.3 in [ALRalg](#ALRalg)),
any [[variety of algebras]]
is an algebraically exact category.
In particular, this includes [[Set]].

In fact, as shown in [ALRalg](#ALRalg), algebraically exact
categories with continuous functors that preserve sifted colimits
form the accessible [[equational hull]] of the bicategory
of [[varieties of algebras]] and continuous functors
that preserve sifted colimits.

### Indexed products and coproducts

When the definition for Kan extensions is internalized to internal categories and fibrations, and then specialized to the case of discrete categories, the notion of distributivity of dependent products over dependent sums encoded by a [[distributivity pullback]] becomes the statement that in the [[codomain fibration]], [[indexed products]] distribute over [[indexed coproducts]] in this sense.

### Pullback-stable colimits
 {#PullbackStableColimits}

As a nontrivial example of the $K\colon I\to Cat$ case, let $I$ be the [[walking structure|walking]] [[cospan]] $0 \to 1 \leftarrow 2$, and let $K(0) = J$ for some category $J$ while $K(1)=K(2)=\ast$, the [[terminal category]].  Then $\int^I K$ is $J$ together with a new terminal object $1$ and a new object $2$ having only a map to $1$, and so a diagram $D: \int^I K \to C$ consists of a $J$-diagram $D_0$ in a slice category $C/Z$ over some object $Z$ along with a morphism $f:Z\to Y$.  The limit category $\lim_I K$ is isomorphic to $J$, and the functor $D'\colon I\times \lim_I K\to C$ has $D'(0,j) = D_0(j)$, with $D'(1,j) =Z$ and $D'(2,j)=Y$.  Therefore, $\colim_{\lim_I K} \lim_I D'$ is the $J$-colimit of the pullback of $D_0$ along $f$, while $\lim_{i\in I} \colim_{K(i)} D$ is the pullback along $f$ of the colimit of $D_0$.  Thus, the distributivity condition for this $K$ holds if and only if $J$-colimits are [[universal colimit|universal]] (stable under pullback).


## Related entries

* [[commutativity of limits and colimits]]
* [[distributivity pullback]]
* [[distributive law]]
* [[distributivity for monoidal structures]]
* [[universal colimit]]

## References

The original definition is due to [[Jan-Erik Roos]], see Definition 1 in

* {#Roos64} [[Jan-Erik Roos]], *Introduction à l'étude de la distributivité des foncteurs lim par rapport aux lim dans les catégories des faisceaux (topos)*, Comptes Rendus Hebdomadaires des Séances de l'Académie des Sciences 259 (1964), 969–972 ([[roos-distributivity.pdf:file]])

Additional references:

* {#ARV} [[Jiří Adámek]], [[Jiří Rosický]], [[Enrico Vitale]], _Algebraic theories.  A categorical introduction to general algebra_ CUP 2011.

* {#ALR} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], [_Continuous Categories Revisited_](http://www.tac.mta.ca/tac/volumes/11/11/11-11abs.html) TAC 11, 2003.

* {#ALRalg} [[Jiří Adámek]], [[William Lawvere]], [[Jiří Rosický]], [_How algebraic is algebra_](http://www.tac.mta.ca/tac/volumes/8/n9/8-09abs.html) TAC 8, 2001.

* {#ABLR} [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiří Rosický]], [_A classification of accessible categories_](http://www.sciencedirect.com/science/article/pii/S0022404902001263) JPAA 175, 2002.

* {#AR} [[Jiří Adámek]], [[Jiří Rosický]], [_Algebra and local presentability: how algebraic are they? (A survey)_](https://doi.org/10.1515/tmj-2017-0113).

* {#ARVloc} [[Jiří Adámek]], [[Jiří Rosický]], [[Enrico Vitale]],
[_On Algebraically Exact Categories and Essential Localizations of Varieties_](https://doi.org/10.1006/jabr.2000.8577)

\bibitem{Garner.2011}

[[!redirects distributivity of limits and colimits]]
[[!redirects distributivity of colimits over limits]]
[[!redirects distributivity of colimits and limits]]
[[!redirects distributivity of products over colimits]]
[[!redirects distributivity of products and colimits]]
[[!redirects products distribute over colimits]]
[[!redirects limits distributive over colimits]]
[[!redirects precontinuous category]]
[[!redirects precontinuous categories]]
[[!redirects algebraically exact category]]
[[!redirects algebraically exact categories]]
