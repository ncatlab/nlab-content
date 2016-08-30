+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
#### Model Theory
+-- {: .hide}
[[!include topos theory - contents]]
[[!include model theory - contents]]
=--
=--
=--


# Contents
* toc
{: toc}

## Idea

The _Deligne completeness theorem_, or **Deligne's theorem**, as it is also called, was initially proved by [[Pierre Deligne]] in an appendix of [[SGA4]][^sga] in the context of [[algebraic geometry]] as a theorem concerning the abundance of  _points_ for a [[coherent topos]].

When in the early 70s the connection between topos theory and logic became manifest [[William Lawvere]] (1975) pointed out that the theorem may be viewed as a variant of the classical **G&#246;del-Henkin completeness theorem** for [[first-order logic]]: since points of a topos $\mathcal{E}$ correspond to set-theoretic models of the theory [[classifying topos|classified]] by $\mathcal{E}$ it amounts not only to saying that a finitary [[geometric theory]] $\mathbb{T}$ has models in $Set$ but that the provability of a sequent in [[coherent logic]] relative to $\mathbb{T}$ is equivalent to its validity in all set-theoretical models of $\mathbb{T}$. 

[^sga]: [SGA 4, vol. II](#SGA4II), expos&#233; VI, p.336.

## Statement

Recall that a point of a topos $\mathcal{E}$ is simply a geometric morphism $p:Set\to\mathcal{E}$ and that $\mathcal{E}$ is said to have [[enough points]] when for any two distinct parallel $f,g:A\to B$ in $\mathcal{E}$ there is a point $p$ that separates $f$ and $g$: $p*(f)\neq p*(g)$.

+-- {: .num_theorem }
###### Theorem

A [[coherent topos]] has [[enough points]].

=--

As a corollary of the [[Deligne-Lurie completeness theorem]] this appears as ([[Spectral Schemes|Lurie SpecSchm, corollary 4.2]]).

## Remarks

Since a Grothendieck topos $\mathcal{E}$ has enough points iff it has a sufficient set of points in the sense that there is a [[surjective geometric morphism|surjection]] $Set/K\to \mathcal{E}$ with $K$ a set (cf. Johnstone [1977](#JT77), pp.224-229) and, furthermore, $Set/K\cong Sh(2^K)$,  one sees that Deligne's theorem yields a special form  $Sh(2^K)\to\mathcal{E}$ of [[Barr's theorem]].

A _general_ Grothendieck topos may fail to have enough points or even fail to have points at all, but it nevertheless has 'enough Boolean-valued points' (cf. [[Barr's theorem]]).

## Related entries

* [[Deligne-Lurie completeness theorem]]

* [[Barr's theorem]]

* [[coherent logic]]

* [[geometric theory]]

* [[coherent topos]]

* [[compactness theorem]]

## References

* M. Artin, A. Grothendieck, J. L. Verdier (eds.), _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas - SGA 4. II_ , LNM **270** Springer Heidelberg 1972.{#SGA4II}

* B. Frot, _G&#246;del's Completeness Theorem and Deligne's Theorem_ , arXiv:1309.0389 (2013). ([pdf](http://arxiv.org/pdf/1309.0389v1))

* {#JT77}P. T. Johnstone, _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). (ch. 7) {#Johnstone77b}

* F. W. Lawvere, _Continuously Variable Sets: Algebraic Geometry= Geometric Logic_ , pp.135-156 in _Proc. Logic Colloquium Bristol 1973_, North-Holland Amsterdam 1975.

* S. Mac Lane, I. Moerdijk, _Sheaves in Geometry and Logic_ , Springer Heidelberg 1994. (sec. IX.11, pp.521f)

* G. E. Reyes, _Sheaves and concepts: A model-theoretic interpretation of Grothendieck topoi_ , Cah. Top. Diff. G&#233;o. Cat. **XVIII** no.2 (1977) pp.405-437. ([numdam](http://www.numdam.org/item?id=CTGDC_1977__18_2_105_0))

