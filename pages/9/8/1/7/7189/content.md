
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}


## Idea

Every [[adjunction|right adjoint functor]] $F\dashv G:\mathcal{B}\to\mathcal{A}$ yields by a classical result a [[monad]] on $\mathcal{A}$ with endofunctor $G\circ F$. The **codensity monad** $\mathbb{T}^G$ is a generalization of this monad to functors $G:\mathcal{B}\to\mathcal{A}$ merely admitting a right [[Kan extension]] $Ran_G G$ of $G$ along itself, with both monads coinciding in case $G:\mathcal{B}\to\mathcal{A}$ is a right adjoint.

The name 'codensity monad' stems from the fact that $\mathbb{T}^G$ reduces to the identity monad iff $G:\mathcal{B}\to\mathcal{A}$ is a [[codense functor]]. Thus, in general, the codensity monad "measures the failure of $G$ to be codense".



## Definition


+-- {: .num_defn #codensity_monad}
###### Definition 
Let $G:\mathcal{B}\to\mathcal{A}$ be a functor such that the right [[Kan extension]] $Ran_G G=(T^G,\;\alpha)$ of $G$ along itself exists with $\alpha :T^G\circ G\Rightarrow G$ the universal 2-cell of the functor $T^G:\mathcal{A}\to\mathcal{A}$. The _codensity monad_ of $G$ is given by the monad
 $$\mathbb{T}^G:=\langle T^G:\mathcal{A}\to\mathcal{A},\;\eta^G:id_\mathcal{A}\Rightarrow T^G,\;\mu^G:T^G\circ T^G\Rightarrow T^G\rangle$$
 where the unit $\eta^G:id_\mathcal{A}\Rightarrow T^G$ is the natural transformation given by the universal property of $(T^G,\;\alpha)$ with respect to the pair $(id_\mathcal{A},\;1_G)\;$, whereas the multiplication $\mu^G:T^G\circ T^G\Rightarrow T^G$ results from the universal property of $(T^G,\;\alpha)$ with respect to the pair $(T^G\circ T^G,\;\alpha\circ (1_{T^G}\ast\alpha))$.

=--

That this indeed defines a monad follows from the universal properties of the Kan extension. Concerning existence, $Ran_G G$ exists for $G:\mathcal{B}\to\mathcal{A}$ e.g. when $\mathcal{B}$ is [[small category|small]] and $\mathcal{A}$ is [[complete category|complete]].

In this circumstance, when $\mathcal{B}$ is small and $\mathcal{A}$ is complete, then the codensity monad is equivalently the one that arises from the adjunction 
$$
  \mathcal{A}
  \underoverset
    {\underset{}{\longleftarrow}}
    {\overset{hom(-,G)}{\longrightarrow}}
    {\bot}
  [\mathcal{B},Set]^{op}
$$
where the left adjoint 
$hom(-,G):\mathcal{A}\to [\mathcal{B},Set]^{op}$ 
takes an object $a$ to the functor $hom(a,G-):\mathcal{B}\to Set$. 
The right adjoint $[\mathcal{B},Set]^{op}\to \mathcal{A}$ is the canonical functor from the [[free completion]] of $\mathcal{B}$ to the category $\mathcal{A}$ which has limits. $G$ is codense if and only if the left adjoint is [[full and faithful]].
 

## Examples

* The [[Giry monad]] (as well as a finitely additive version) arise as codensity monads of forgetful functors from subcategories of the category of [[convex sets]] to the category of [[measurable spaces]] ([Avery 14](#Avery14)).

* The codensity monad of the inclusion [[FinSet]] $\hookrightarrow$[[Set]] is the [[ultrafilter]] monad. Its algebras are [[compact Hausdorff spaces]]. 

* The codensity monad of the inclusion $FinGrp \hookrightarrow$ [[Grp]], is the [[profinite completion of a group|profinite completion]] monad, whose algebras may be identified with [[profinite groups]] -- that is, [[topological groups]] whose underlying topological space is profinite ([Avery 17, Proposition 2.7.10](#Avery17)).

* The codensity monad of the inclusion $FinSet \to Top$
computes the [[Stone spectrum]] of the [[Boolean algebra]] of [[clopen subsets]]
of a [[topological space]].
Its algebras are precisely the [[Stone spaces]].
([Sipoș, Theorem 2](#Sipos)).


* The codensity monad of the inclusion $N \to Top$, where
$N$ denotes the [[full subcategory]] of [[Top]] consisting
of arbitrary [[small products]] of the [[Sierpinski space|Sierpiński space]],
is the [[localic spectrum]] of the [[frame]] of opens of a [[topological space]].
Its algebras are precisely the [[sober spaces]].
([Sipoș, Theorem 6](#Sipos))

* For the codensity monad induced by the inclusion of [[homotopy types with finite homotopy groups]] into all [[homotopy types]] see [there](homotopy+type+with+finite+homotopy+groups#CodensityMonadOfInclusionIntoAllHomotopyTypes).

## Properties

....


## Related entries

* [[dense functor]]

* [[shape theory]]

* [[Kan extension]]

* [[algebraic theory]]

* [[ultrafilter]]

* [[idempotent monad]]


## Link

* nCafé blog 2012: [Where do Monads come from?](https://golem.ph.utexas.edu/category/2012/09/where_do_monads_come_from.html)

## References

A very nice overview is provided by

* {#Leinster13}[[Tom Leinster]], _Codensity and the Ultrafilter Monad_ , TAC **12** no.13 (2013) pp.332-370.  ([abstract](http://www.tac.mta.ca/tac/volumes/28/13/28-13abs.html))

Codensity monads arising from subcategory inclusions are studied in

* {#diLiberti19} [[Ivan Di Liberti]], _Codensity: Isbell duality, pro-objects, compactness and accessibility_, arXiv:1910.01014 (2019). ([abstract](https://arxiv.org/abs/1910.01014))

The role in shape theory is discussed in

* Armin Frei, _On categorical shape theory_ , Cah. Top. Géom. Diff. **XVII** no.3 (1976) pp.261-294. ([numdam](http://www.numdam.org/item/?id=CTGDC_1976__17_3_261_0))

* D. Bourn, J.-M. Cordier, _Distributeurs et th&#233;orie de la forme_, Cah. Top. G&#233;om. Diff. Cat. **21** no.2 (1980) pp.161-189. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1980__21_2/CTGDC_1980__21_2_161_0/CTGDC_1980__21_2_161_0.pdf))

* J.-M. Cordier, [[Tim Porter|T. Porter]], _Shape Theory: Categorical Methods of Approximation_ , (1989), Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

For a description of the [[Giry monad]] as a codensity monad, see

* {#Avery14} [[Tom Avery]], _Codensity and the Giry monad_, ([arXiv:1410.4432](https://arxiv.org/abs/1410.4432))



Other references include

* {#Avery17} [[Tom Avery]], _Structure and Semantics_, ([arXiv:1708.01050](https://arxiv.org/abs/1708.01050))

* C. Casacuberta, A. Frei, _Localizations as idempotent approximations to completions_ , JPAA **142** (1999) no. 1 pp.25–33. ([draft](http://atlas.mat.ub.es/personals/casac/articles/cfre1.pdf))

* Yves Diers, _Complétion monadique_ , Cah. Top. Géom. Diff. Cat. **XVII** no.4 (1976) pp.362-379. ([numdam](http://www.numdam.org/item/?id=CTGDC_1976__17_4_363_0))

* S. Katsumata, T. Sato, [[Tarmo Uustalu|T. Uustalu]], _Codensity lifting of monads and its dual_ , arXiv:1810.07972 (2012). ([abstract](https://arxiv.org/abs/1810.07972))

* [[Joachim Lambek|J. Lambek]], B. A. Rattray, _Localization and Codensity Triples_ , Comm. Algebra **1** (1974) pp.145-164.

* [[Jiří Adámek]], [[Lurdes Sousa]], _D-Ultrafilters and their Monads_, ([arXiv:1909.04950](https://arxiv.org/abs/1909.04950))

* {#Sipos} [[Andrei Sipos]], _Codensity and Stone spaces_, ([arXiv:1409.1370](https://arxiv.org/abs/1409.1370))

[[!redirects codensity monads]]
[[!redirects density comonad]]
[[!redirects density comonads]]
[[!redirects Codensity monad]]
[[!redirects Codensity monads]]
[[!redirects codensity triple]]