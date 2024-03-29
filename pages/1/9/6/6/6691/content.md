
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $\Delta$ the [[simplex category]] the [[functor category]] $sSet^{\Delta}$ is that of [[cosimplicial object]]s in [[simplicial set]]s: [[cosimplicial simplicial set]]s.

There are various standard [[model category]] structures on this category. The [[Reedy model structure]] is discussed in ([BousfieldKan](#BousfieldKan)), the injective structure is discussed in ([Jardine](#Jardine)).

## Properties

+-- {: .num_remark}
###### Remark

The [[totalization]] of a cosimplicial simplicial set $X^\bullet$ coincides with the [[sSet]]-enriched [[hom-object]]

$$
  Tot(X_\bullet) = sSet^{\Delta}(\Delta, X_\bullet)
  \,,
$$

where $\Delta : [k] \mapsto \Delta[k]$ is the canonical cosimplicial simplicial set given by the [[simplex]]-assignment.

Since $\Delta$ is cofibrant in the [[Reedy model structure]] it follows that totalization of Reedy-fibrant cosimplicial simplicial sets preserves weak equivalences. The following lists situations in which totalization respects weak equivalences even without this assumption.

=--

+-- {: .num_remark}
###### Remark

Totalization is closely related to [[descent objects]]. If
$A$ is a [[simplicial presheaf]] and $Y \to X$ is a [[hypercover]], then the descent object is the [[sSet]]-[[hom object|enriched hom]]

$$
  Desc(Y,X) = sPsh(Y,A)
  \,.
$$

If we decompose 

$$
  Y = \int^{[n] \in \Delta} \Delta[n] \cdot Y_n
$$

into its cells by a [[coend]], where now each $Y_n$ is a Set-valued [[presheaf]] (see [[co-Yoneda lemma]]), then this is

$$
  \begin{aligned}
    Desc(Y,A) 
    &= 
    sPSh(\int^{n \in \Delta} \Delta[n] \cdot Y_n, A)
    \\
    & = 
    \int_{n \in \Delta} sPSh(\Delta[n] \cdot Y_n , A)
    \\
    & = \int_{n \in \Delta} sSet(\Delta[n], sPSh(Y_n,A))
   \\
    &= Tot( sPSh(Y_\bullet, A))
  \end{aligned}
  \,,
$$

where the equality signs are [[isomorphisms]] of [[simplicial sets]], the outside integral sign denotes the [[end]], and in the integrand we are using that [[simplicial presheaves]] are [[simplicially enriched category|simplicially enriched]] and [[tensoring|tensored]] over simplicial sets.

So a standard class of examples of cosimplicial simplicial sets to keep in mind are those obtained by evaluating a [[simplicial presheaf]] degreewise on the components of a [[hypercover]]. Its totalization then is the corresponding [[descent object]].

=--



+-- {: .num_prop}
###### Proposition

For $G^\bullet \to H^\bullet$ a morphism of [[cosimplicial object|cosimplicial]] [[groupoid]]s which is degreewise an [[equivalence of categories|equivalence]], also the induced morphism of [[totalization]]s

$$
  Tot(G^\bullet) \to Tot(H^\bullet)
$$

is a weak equivalence (of [[simplicial set]]s).

=--

This is ([Jardine, corollary 12](#Jardine)).

+-- {: .num_defn #RestrictedTotalization}
###### Definition 

Let $\Delta_+ \hookrightarrow \Delta$ be the [[subcategory]] of the [[simplex category]] on the co-face maps. Write $rTot$ for the corresponding [[totalization]], called the **restricted totalization**.

=--

+-- {: .num_prop}
###### Proposition

For $G^\bullet \to H^\bullet$ a degreewise weak equivalence of [[strict 2-category|strict]] [[2-groupoid]]s, the resulting morphism of connected components of [restricted totalizations](#RestrictedTotalization)

$$
  rTot(G^\bullet) \to rTot(H^\bullet)
$$

is a [[weak equivalence]].

=--

This is ([Prezma, theorem 6.1](#Prezma)).

Retsricted to $\pi_0$ this statement appeared as ([Yekutieli, theorem 2.4](#Yekutieli)). Notice  that it is indeed necessary to use the restricted totalization instead of the ordinary totalization here.


## References

The [[Reedy model structure]] on $sSet^{\Delta}$ is discussed in  Chapter X of

* [[Aldridge Bousfield]] and [[Dan Kan]], _Homotopy limits, completions and localizations_ Springer-Verlag, Berlin, 1972. Lecture Notes in Mathematics, Vol. 304.
 {#BousfieldKan}

The [[model structure on functors|injective model structure]] is discussed in

* [[Rick Jardine]], _Cosimplicial spaces and cocycles_ ([pdf](http://www.math.uwo.ca/~jardine/papers/preprints/cosimp5.pdf))
 {#Jardine}

Totalization of cosimplicial strict [[2-groupoids]] is considered in 

* [[Amnon Yekutieli]], _Combinatorial Descent Data for Gerbes_ ([arXiv:1109.1919](http://arxiv.org/abs/1109.1919))
 {#Yekutieli}

and

* [[Matan Prezma]], _Descent data of cosimplicial 2-groupoids_ ([arXiv:1112.3072](http://arxiv.org/abs/1112.3072))
 {#Prezma}
 
[[!redirects model structure on cosimplicial spaces]]