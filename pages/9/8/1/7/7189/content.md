
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

The same idea applies to [[2-categories]] or [[bicategories]] more general than $Cat$: codensity monads can be defined whenever suitable right Kan extensions exist. 

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

\begin{example} 
Every monad that is induced by an adjunction $L \dashv R$ is the codensity monad of $R$. In particular, every [[enriched monad]] is a codensity monad (via its [[Kleisli category]]).
\end{example}

\begin{example}
Let $d$ be an object in a [[closed category]] $C$. Then the codensity monad of the [[constant functor]] $d : 1 \to C$ is the **double dualization monad** associated to $d$, given by $d^{d^{(-)}}$.

More conceptually, the codensity monad construction may be seen as a generalisation of the double dualisation construction analogous to the generalisation from [[algebras for a monad]] to [[modules over a monad]] (the latter is the perspective that is most natural 2-categorically).
\end{example}

\begin{example}
The [[Giry monad]] (as well as a finitely additive version) arise as codensity monads of forgetful functors from subcategories of the category of [[convex sets]] to the category of [[measurable spaces]] ([Avery 14](#Avery14)).
\end{example}

\begin{example}
The codensity monad of the inclusion [[FinSet]] $\hookrightarrow$[[Set]] is the [[ultrafilter]] monad. Its algebras are [[compact Hausdorff spaces]]. 
\end{example}

\begin{example}
The codensity monad of the inclusion $FinGrp \hookrightarrow$ [[Grp]], is the [[profinite completion of a group|profinite completion]] monad, whose algebras may be identified with [[profinite groups]] -- that is, [[topological groups]] whose underlying topological space is profinite ([Avery 17, Proposition 2.7.10](#Avery17)).
\end{example}

\begin{example}
The codensity monad of the inclusion $FinSet \to Top$
computes the [[Stone spectrum]] of the [[Boolean algebra]] of [[clopen subsets]]
of a [[topological space]].
Its algebras are precisely the [[Stone spaces]].
([Sipoș, Theorem 2](#Sipos)). 
\end{example}

\begin{example}
The codensity monad of the inclusion $N \to Top$, where
$N$ denotes the [[full subcategory]] of [[Top]] consisting
of arbitrary [[small products]] of the [[Sierpinski space|Sierpiński space]],
is the [[localic spectrum]] of the [[frame]] of opens of a [[topological space]].
Its algebras are precisely the [[sober spaces]].
([Sipoș, Theorem 6](#Sipos)) 
\end{example}

\begin{example}
The codensity monad of the inclusion of [[countable sets]] in all sets, $Ctbl \hookrightarrow Set$, assigns to each set $X$ the set of ultrafilters on $X$ closed under countable intersections. This still holds for the inclusion of the full subcategory of $Ctbl$ on the single set $\mathbb{N}$.
\end{example}

\begin{example}
More generally, the codensity monad of the inclusion of sets of cardinality less than that of fixed $Y$, $Set_{\lt Y} \hookrightarrow Set$, assigns to each set $X$ the set of $Y$-complete ultrafilters on $X$. 
\end{example}

\begin{example}
For the codensity monad induced by the inclusion of [[homotopy types with finite homotopy groups]] into all [[homotopy types]] see [there](homotopy+type+with+finite+homotopy+groups#CodensityMonadOfInclusionIntoAllHomotopyTypes).
\end{example}

\begin{example} 
The codensity monad induced by the [[Yoneda embedding]] is isomorphic to the monad induced by the [[Isbell adjunction]].
\end{example} 

\begin{example} 
In the bicategory [[Rel]], the right Kan extension of a relation $T: A \to C$ along a relation $R: B \to C$ is the relation $T/R: B \to C$ defined by the formula $\forall_{a: A}\; R(a, b) \Rightarrow T(a, c)$. The codensity monad $R/R: B \to B$, being a monad in $Rel$, is a [[preorder]]. This construction frequently recurs; see for instance [[specialization order]] for a [[topological space|topology]]. 
\end{example} 

## Properties

....


## Related entries

* [[dense]]

* [[dense functor]]

* [[shape theory]]

* [[Kan extension]]

* [[algebraic theory]]

* [[ultrafilter]]

* [[idempotent monad]]


## Link

* nCafé blog 2012: [Where do Monads come from?](https://golem.ph.utexas.edu/category/2012/09/where_do_monads_come_from.html)

## References

One of the first references is

* [[Anders Kock]], _Continuous Yoneda Representations of a Small Category_, Preprint Aarhus University (1966). ([pdf](http://home.math.au.dk/kock/CYRSC.pdf))

For the special case of double dualisation, see:

* [[Anders Kock]]. _On double dualization monads_, Mathematica Scandinavica 27.2 (1970): 151-165. ([JSTOR](https://www.jstor.org/stable/24489892))

A very nice overview is provided by

* {#Leinster13}[[Tom Leinster]], _Codensity and the Ultrafilter Monad_ , TAC **12** no.13 (2013) pp.332-370.  ([abstract](http://www.tac.mta.ca/tac/volumes/28/13/28-13abs.html))

Codensity monads arising from subcategory inclusions are studied in

* {#diLiberti19} [[Ivan Di Liberti]], _Codensity: Isbell duality, pro-objects, compactness and accessibility_, arXiv:1910.01014 (2019). ([abstract](https://arxiv.org/abs/1910.01014))

The role in shape theory is discussed in

* Armin Frei, _On categorical shape theory_ , Cah. Top. Géom. Diff. **XVII** no.3 (1976) pp.261-294. ([numdam](http://www.numdam.org/item/?id=CTGDC_1976__17_3_261_0))

* D. Bourn, J.-M. Cordier, _Distributeurs et th&#233;orie de la forme_, Cah. Top. G&#233;om. Diff. Cat. **21** no.2 (1980) pp.161-189. ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1980__21_2/CTGDC_1980__21_2_161_0/CTGDC_1980__21_2_161_0.pdf))

* J.-M. Cordier, [[Tim Porter|T. Porter]], _Shape Theory: Categorical Methods of Approximation_ , (1989), Mathematics and its Applications, Ellis Horwood. Reprinted Dover (2008).

For a description of the [[Giry monad]] and other [[probability monads]] as codensity monads, see

* {#Avery14} [[Tom Avery]], _Codensity and the Giry monad_, Journal of Pure and Applied Algebra **220** 3 (2016) 1229-1251 &lbrack;[arXiv:1410.4432](https://arxiv.org/abs/1410.4432), [doi:10.1016/j.jpaa.2015.08.017](https://doi.org/10.1016/j.jpaa.2015.08.017)&rbrack;

* Ruben Van Belle, _Probability monads as codensity monads_. Theory and Applications of Categories 38 (2022), 811–842, ([tac](http://tac.mta.ca/tac/volumes/38/21/38-21abs.html))



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