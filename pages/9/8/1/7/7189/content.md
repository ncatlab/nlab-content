
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

A standard result in the theory of [[monad|monads]] says that every [[adjunction]] $F\dashv G:\mathcal{B}\to\mathcal{A}$ with unit $\eta$ and counit $\epsilon$ yields a monad $\langle 
G\circ F,\;\eta,\;1_G\ast\epsilon\ast 1_F\rangle$ on $\mathcal{A}$. Similarly, it is possible to attach a monad $\mathbb{T}^G$, called the **codensity monad**, to a functor $G:\mathcal{B}\to\mathcal{A}$, when the right [[Kan extension]] $Ran_G G$ of $G$ along itself exists, with both monads coinciding in case $G:\mathcal{B}\to\mathcal{A}$ has a left adjoint.

The name 'codensity monad' stems from the fact that $\mathbb{T}^G$ reduces to the identity monad iff $G:\mathcal{B}\to\mathcal{A}$ is a [[dense functor|codense functor]]. Thus, in general, the codensity monad "measures the failure of $G$ to be codense".



## Definition


+-- {: .num_defn #codensity_monad}
###### Definition 
Let $G:\mathcal{B}\to\mathcal{A}$ be a functor such that the right [[Kan extension]] $Ran_G G=(T^G,\;\alpha)$ of $G$ along itself exists with $\alpha :T^G\circ G\Rightarrow G$ the universal 2-cell of the functor $T^G:\mathcal{A}\to\mathcal{A}$. The _codensity monad_ of $G$ is given by the monad
 $$\mathbb{T}^G:=\langle T^G:\mathcal{A}\to\mathcal{A},\;\eta^G:id_\mathcal{A}\Rightarrow T^G,\;\mu^G:T^G\circ T^G\Rightarrow T^G\rangle$$
 where the unit $\eta^G:id_\mathcal{A}\Rightarrow T^G$ is the natural transformation given by the universal property of $(T^G,\;\alpha)$ with respect to the pair $(id_\mathcal{A},\;1_G)\;$, whereas the multiplication $\mu^G:T^G\circ T^G\Rightarrow T^G$ results from the universal property of $(T^G,\;\alpha)$ with respect to the pair $(T^G\circ T^G,\;\alpha\circ (1_{T^G}\ast\alpha))$.

=--

That this indeed defines a monad follows from the universal properties of the Kan extension. Concerning existence, $Ran_G G$ exists for $G:\mathcal{B}\to\mathcal{A}$ e.g. when $\mathcal{B}$ is [[small category|small]] and $\mathcal{A}$ is [[complete category|complete]].

  


## Examples


....



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

The role in shape theory is discussed in

* Armin Frei, _On categorical shape theory_ , Cah. Top. Géom. Diff. **XVII** no.3 (1976) pp.261-294. ([numdam](http://www.numdam.org/item/?id=CTGDC_1976__17_3_261_0))

* D. Bourn, J.-M. Cordier, _Distributeurs et th&#233;orie de la forme_, Cah. Top. G&#233;om. Diff. Cat. **21** no.2 (1980) pp.161-189. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1980__21_2/CTGDC_1980__21_2_161_0/CTGDC_1980__21_2_161_0.pdf))

* J.-M. Cordier, [[Tim Porter|T. Porter]], _Shape Theory: Categorical Methods of Approximation_ , (1989), Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

Other references include

* C. Casacuberta, A. Frei, _Localizations as idempotent approximations to completions_ , JPAA **142** (1999) no. 1 pp.25–33. ([draft](http://atlas.mat.ub.es/personals/casac/articles/cfre1.pdf))

* Yves Diers, _Complétion monadique_ , Cah. Top. Géom. Diff. Cat. **XVII** no.4 (1976) pp.362-379. ([numdam](http://www.numdam.org/item/?id=CTGDC_1976__17_4_363_0))

* S. Katsumata, T. Sato, [[Tarmo Uustala|T. Uustala]], _Codensity lifting of monads and its dual_ , arXiv:1810.07972 (2012). ([abstract](https://arxiv.org/abs/1810.07972))

* [[Joachim Lambek|J. Lambek]], B. A. Rattray, _Localization and Codensity Triples_ , Comm. Algebra **1** (1974) pp.145-164.


[[!redirects codensity monads]]
[[!redirects density comonad]]
[[!redirects density comonads]]
[[!redirects Codensity monad]]
[[!redirects Codensity monads]]
[[!redirects codensity triple]]