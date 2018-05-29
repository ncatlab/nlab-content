
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The notion of a **regular semicategory** generalizes the notion of a _regular algebra_ from ring theory to (semi-)category theory. Just like regular algebras are (in general) non-unital algebras that nevertheless "behave" in many respects like unital ones, regular semicategories are semicategories on the verge of turning into categories.

## Preliminaries

Let us first recall a couple of concepts

+-- {: .num_defn #semifunctor}
###### Definition 
Let $\mathcal{G}$, $\mathcal{H}$ be [[semicategories]]. A _morphism $F:\mathcal{G}\to\mathcal{H}$ of semicategories_ assigns to all objects $X\in\mathcal{G}$ an object $F(X)\in\mathcal{H}$ and to every morphism $f:X\to Y$ in $\mathcal{G}$ a morphism $F(f):F(X)\to F(Y)$ in $\mathcal{H}$ such that $F(f\circ g)=F(f)\circ F(g)$.

A _natural transformation_ $\alpha:\mathcal{G}\Rightarrow\mathcal{H}$ consists of a family $\{\alpha_X:F(X)\to G(X)\}_{X\in|\mathcal{G}|}$ in $\mathcal{H}$ indexed by the objects of $\mathcal{G}$ such that for all $f:X\to Y$ in $\mathcal{G}$ the following diagram commutes:

$$
  \array{
     F(X)& \overset{F(f)}{\longrightarrow} & F(Y)
     \\
     {}_{\alpha_X}\downarrow & & \downarrow _{\alpha_Y}
     \\
     G(X)& \overset{G(f)}{\longrightarrow} & G(Y)
  }
$$

=--

+-- {: .num_defn #semipresheaf}
###### Definition 
A _presheaf_ on a semicategory $\mathcal{G}$ is a morphism of semicategories $F:\mathcal{G}^{op}\to Set$. The category $Prsh(\mathcal{G})$ has objects presheaves on $\mathcal{G}$ and morphisms the natural transformations and is the called _the category of presheaves of the semicategory $\mathcal{G}$_.
=--

## Definition


...

## Example


...

## Properties

...

## Related entries

* [[semicategory]]

* [[semipresheaf]]

* [[adjoint cylinder|unity-and-identity of opposites]]

* [[Yoneda lemma]]

## References

Regular semicategories were introduced in 

* {#MBB02}M.-A. Moens, U. Bernani-Canani, [[Francis Borceux|F. Borceux]], _On regular presheaves and regular semi-categories_ , Cah. Top. G&#233;om. Diff. Cat. **XLIII** no.3 (2002) pp.163-190. ([numdam](http://www.numdam.org/item?id=CTGDC_2002__43_3_163_0))

Their quantaloid-enriched theory is studied in

* {#Stubbe05}[[Isar Stubbe]], _Categorical structures enriched in a quantaloid : regular presheaves, regular semicategories_ , Cah. Top. G&#233;om. Diff. Cat. **XLVI** no.2 (2005) pp.99-121. ([numdam](http://www.numdam.org/item/CTGDC_2005__46_2_99_0))

For the origins in algebra of the concept see

* F. Grandjean, [[Enrico Vitale|E. M. Vitale]], _Morita equivalence for regular algebras_ , Cah. Top. Géom. Diff. Cat. **XXXIX** (1998) pp.137-153. ([numdam](http://www.numdam.org/item/CTGDC_1998__39_2_137_0))




[[!redirects regular semicategories]]
[[!redirects regular semi-category]]
[[!redirects regular semi-categories]]
[[!redirects regular presheaf]]
[[!redirects regular presheaves]]
