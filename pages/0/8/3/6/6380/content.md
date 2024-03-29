
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

Every [[variety]] in [[positive characteristic]] has a [[formal group]] attached to it, called the _Artin-Mazur formal group_. This group is often related to arithmetic properties of the variety such as being ordinary or supersingular.

The Artin-Mazur formal group in dimension $n$ is a [[formal group]] version of the [[Picard infinity-group|Picard n-group]] of flat/holomorphic [[circle n-bundles]] on the given variety. Therefore for $n = 1$ one also speaks of the _[[formal Picard group]]_ and for $n = 2$ of the _[[formal Brauer group]]_.


## Definition
 {#Definition}

### Deformations of higher line bundles (of $H^n(-,\mathbb{G}_m)$-cohomology)

Let $X$ be a [[smooth scheme|smooth]] [[proper scheme|proper]] $n$ [[dimension|dimensional]] [[variety]] over an [[algebraically closed field]] $k$ of [[positive number|positive]] [[characteristic]] $p$. 

Writing $\mathbb{G}_m$ for the [[multiplicative group]] and $H_{et}^\bullet(-,-)$ for [[etale cohomology]], then $H_{et}^n(X,\mathbb{G}_m)$ classifies $\mathbb{G}_m$-[[principal infinity-bundle|principal n-bundles]] ([[line n-bundles]], [[bundle 2-gerbe|bundle (n-1)-gerbes]]) on $X$.  Notice that, by the discussion at _[Brauer group -- relation to &#233;tale cohomology](Brauer%20group#RelationToEtaleCohomology)_, for $n = 1$ this is the [[Picard group]] while for $n = 2$ this contains (as a [[torsion subgroup]]) the [[Brauer group]] of $X$.

Accordingly, for each [[Artin algebra]] regarded as an [[infinitesimally thickened point]] $S \in ArtAlg_k^{op}$ the [[cohomology group]] $H_{et}^n(X\times_{Spec(k)} S,\mathbb{G}_m)$ is that of [[equivalence classes]] of $\mathbb{G}_n$-[[principal infinity-bundle|principal n-bundles]] on a formal thickening of $X$.

The defining inclusion $\ast \to S$ of the unique global point induces a restriction map $H^n_{et}(X\times_{Spec(k)} S, \mathbb{G}_m)\to H^n_{et}(X, \mathbb{G}_m))$ which restricts an $n$-bundle on the formal thickening to just $X$ itself. The [[kernel]] of this map hence may be thought of as the group of $S$-parameterized infinitesimal [[deformations]] of the trivial $\mathbb{G}_m$-$n$-bundle on $X$. 

(For $n = 1$ this is an [[infinitesimal neighbourhood]] of the neutral element in the [[Picard scheme]] $Pic_X$, for higher $n$ one will need to genuinely speak about [[Picard stacks]] and higher stacks.)

As $S$ varies, these groups of deformations naturally form a [[presheaf]] on "[[infinitesimally thickened points]]" ([[Isbell duality|formal duals]] to [[Artin  algebras]]).

+-- {: .num_defn}
###### Definition

For $X$ an [[algebraic variety]] as above, write

$$
  \Phi_X^n \;\colon\; ArtAlg_k \to Grp 
$$

$$
  \Phi_X^n(S) \coloneqq \mathrm{ker}(H^n_{et}(X\times_{Spec(k)} S, \mathbb{G}_m)\to H^n_{et}(X, \mathbb{G}_m))
  \,.
$$ 

=--

([Artin-Mazur 77, II.1 "Main examples"](#ArtinMazur77))

The fundamental result of ([Artin-Mazur 77, II](#ArtinMazur77)) is that under the above hypotheses this presheaf is [[prorepresentable functor|pro-representable]] by a [[formal group]], which we may hence also denote by $\Phi_X^n$. This is called the **Artin-Mazur formal group** of $X$ in degree $n$.

More in detail:

+-- {: .num_prop #SufficientConditionsForRepresentability}
###### Proposition

Let $X$ be an [[algebraic variety]] [[proper morphism|proper]] over an [[algebraically closed field]] $k$ of [[positive number|positive]] [[characteristic]].

A sufficient condition for $\Phi_X^k$ to be [[prorepresentable functor|pro-representable]] by a [[formal group]] is that $\Phi_X^{k-1}$ is [[formally smooth morphism|formally smooth]].

In particular if $dim H^{k-1}(X,\mathcal{O}_X) = 0$ then $\Phi^{k-1}(X)$ vanishes, hence is trivially formally smooth, hence $\Phi^k(X)$ is representable

=--

The first statement appears as ([Artin-Mazur 77, corollary (2.12)](#ArtinMazur77)). The second as ([Artin-Mazur 77, corollary (4.2)](#ArtinMazur77)).

+-- {: .num_remark #Dimension}
###### Remark

The [[dimension]] of $\Phi^k_X$ is 

$$
  dim(\Phi^k_X) = dim H^k(X,\mathcal{O}_X)
  \,.
$$

=--

([Artin-Mazur 77, II.4](#ArtinMazur77)).


### Deformations of higher line bundles with connection (of Deligne cohomology)
 {#DeformationsOfDeligneCohomology}

In ([Artin-Mazur 77, section III](#ArtinMazur77)) is also discussed the formal [[deformation theory]] of [[line n-bundles with connection]] (classified by [[ordinary differential cohomology]], being [[hypercohomology]] with [[coefficients]] in the [[Deligne complex]]). Under suitable conditions this yields a [[formal group]], too.

Notice that by the discussion at _[intermediate Jacobian -- Characterization as Hodge-trivial Deligne cohomology](http://ncatlab.org/nlab/show/intermediate%20Jacobian#CharacterizationAsHodgeTrivialDeligneCohomology)_ the formal deformation theory of Deligne cohomology yields the formal completion of [[intermediate Jacobians]] (all in suitable degree).

## Examples

### General

+-- {: .num_remark}
###### Remark

* For a [[curve]] $X$ (i.e. $dim(X)= 1$), the Artin-Mazur group is often called the **[[formal Picard group]]** $\widehat{\mathrm{Pic}}$.

* For a [[surface]] $X$ (i.e. $dim(X) =2$), the Artin-Mazur group is called the **[[formal Brauer group]]** $\widehat{Br}$.


=--

### Of Calabi-Yau varieties
 {#OfCalabiYauVarieties}

+-- {: .num_example #AMfgOfStrictCalabiYau} 
###### Example

Let $X$ be a strict [[Calabi-Yau variety]] in [[positive characteristic]] of  [[dimension]] $n$ (strict meaning that the [[Hodge numbers]] $h^{0,r} = 0$ vanish for $0 \lt r \lt n$, i.e. over the [[complex numbers]] that the [[holonomy group]] exhausts $SU(n)$, this is for instance the case of relevance for [[supersymmetry]], see at _[[supersymmetry and Calabi-Yau manifolds]]_). 

By prop. \ref{SufficientConditionsForRepresentability} this means that
the Artin-Mazur formal group $\Phi^n_X$ exists. 
Since moreover $h^{0,n} = 1$ it follows by remark \ref{Dimension} that it is of [[dimension]] 1

=--

For discussion of $\Phi_X^n$ for [[Calabi-Yau varieties]] $X$ of [[dimension]] $n$ and in [[positive number|positive]] [[characteristic]] see ([Geer-Katsura 03](#GeerKatsura03)).


## Related concepts

* [[formal group]]

* [[height of a variety]]

[[!include moduli of higher lines -- table]]

## References

The original article is

* {#ArtinMazur77} [[Michael Artin]], [[Barry Mazur]], _Formal Groups Arising from Algebraic Varieties_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 10 no. 1 (1977), p. 87-131  ([numdam:ASENS_1977_4_10_1_87_0](http://www.numdam.org/item?id=ASENS_1977_4_10_1_87_0), [MR56:15663](http://www.ams.org/mathscinet-getitem?mr=56:15663))
 
Further developments are in 

* {#Stienstra87} [[Jan Stienstra]], _Formal group laws arising from algebraic varieties_, American Journal of Mathematics, Vol. 109, No.5 (1987), 907-925 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/stienstra1.pdf))


Lecture notes touching on the cases $n = 1$ and $n = 2$ include

* {#Liedtke14} Christian Liedtke, example 6.13 in _Lectures on Supersingular K3 Surfaces and the Crystalline Torelli Theorem_ ([arXiv.1403.2538](http://arxiv.org/abs/1403.2538))

Discussion of Artin-Mazur formal groups for all $n$ and of [[Calabi-Yau varieties]] of [[positive number|positive]] [[characteristic]] in [[dimension]] $n$ is in 

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_, Documenta Math. 8. 97-113 (2003) ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))



[[!redirects Artin-Mazur formal group]]
[[!redirects Artin-Mazur formal groups]]
[[!redirects Artin–Mazur formal group]]
[[!redirects Artin–Mazur formal groups]]
[[!redirects Artin--Mazur formal group]]
[[!redirects Artin--Mazur formal groups]]