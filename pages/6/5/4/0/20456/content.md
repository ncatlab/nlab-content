+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
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

Prismatic cohomology is a cohomology theory for p-adic [[formal schemes]] which can specialize into various $p$-adic cohomology theories, including [[étale cohomology]], [[de Rham cohomology]] and [[crystalline cohomology]], as well as the so far conjectural $q$-de Rham cohomology of [[Peter Scholze]]. It is a geometric approach to integral [[p-adic Hodge theory]].

Prismatic cohomology relies heavily on the idea of a [[Joyal delta-ring|$\delta$-ring]], introduced by [[Andre Joyal]] to formalize how a ring equipped with a [[Frobenius lift]] is analogous to ring equipped with a [[derivation]].

## Prisms

A prism is a pair $(A,I)$ where $A$ is a $\delta$-ring and $I$ is an ideal defining a Cartier divisor on $\mathrm{Spec}(A)$, such that $A$ is derived $(p,I)$-complete, and $p \in I + \phi(I)A$.

## Examples of Prisms

* $A=\mathbb{Z}_{p}[[u]]$ and $I=(u-p)$
* $A=A_{\mathrm{inf}}(R)$ and $I=\mathrm{ker}(\theta)$, where $\theta:A_{\mathrm{inf}}(R)\to R$ is the canonical surjection

## Relation to Perfectoid Rings

A prism $(A,I)$ is _perfect_ if $A$ is perfect. The category of perfect prisms is equivalent to the category of _integral perfectoid rings_ which are related to, but not the same as, the perfectoid rings in [[perfectoid spaces]]. The definition of integral perfectoid ring can be found in Definition 3.5 of  [BhattScholze19](#BhattScholze19) and the relation between the two notions of perfectoid can be found in Lemma 3.20 of the same paper.

## Definition of Prismatic Cohomology

Let $(A,I)$ be a prism as defined above. Let $R$ be a formally smooth $A/I$-algebra. The _prismatic site_ $(R/A)_{\Delta}$ has objects which are prisms $(B,I B)$ over $(A,I)$ together with a map $R\to B/I B$ over $A/I$. Such an object is written $(R\to B/I B\leftarrow B)$.

We have functors $\mathcal{O}_{\Delta}$ and $\overline{\mathcal{O}}_{\Delta}$ which sends $(R\to B/I B\leftarrow B)$ to $B$ and $B/I B$ respectively. The _prismatic cohomology_ of $R$ is defined to be $\Delta_{R/A}:=R\Gamma((R/A)_{\Delta},\mathcal{O}_{\Delta})$.

## Comparison theorems

We have the following comparison theorems relating prismatic cohomology to the crystalline and étale cohomology:

\begin{theorem}
Let $A,(p)$ be a bounded prism and let $R$ be a smooth $A/p$-algebra. There exists a canonical isomorphism
$$\phi_{A}^{*}\Delta_{R/A}^{\wedge}\cong R\Gamma_{crys}(R/A)$$
in $D(A)$, compatible with the action of Frobenius on both sides.
\end{theorem}

\begin{theorem}
Let $(A,I)$ be a perfect prism and let $R$ be a $p$-complete $A/I$-algebra. For all $n\geq 1$, there exists a canonical isomorphism
$$R\Gamma_{\et}(\mathrm{Spec}(R[1/p]),\mathbb{Z}/p^{n})\cong (\Delta_{R/A}[1/d]/p^{n})^{\phi=1}$$
where $d$ is a generator of $I$.
\end{theorem}

## Absolute Prismatic Cohomology

By forgetting the choice of base prism, one obtains the absolute prismatic cohomology. Given a p-adic formal scheme $X$, its absolute prismatic site ${X}_{\Delta}$ is the category of all bounded  prisms $(B,J)$ equipped with a map $\mathrm{Spf}(B/J)\to X$, topologized with the flat topology. We have sheaves $\mathcal{O}_{\Delta}$, $I_{\Delta}$, and $\overline{\mathcal{O}}_{\Delta}$ obtained by remembering $B$, $J$, and $B/J$ respectively.

The absolute prismatic cohomology $R\Gamma(X_{\Delta},\mathcal{O}_{\Delta})$ is equipped with a filtration called the _Nygaard filtration_, playing a role analogous to that of the [[Hodge filtration]] for [[de Rham cohomology]].

## Prismatic Crystals

Let $X$ be a p-adic formal scheme and let $X_{\Delta}$ be its absolute prismatic site as above. A _prismatic crystal_ is an assignment

$$(B,J)\in X_{\Delta}\mapsto \mathcal{E}(B)\in\mathrm{Vect}_{B}$$

where $\mathrm{Vect}_{B}$ is the set of finite projective $B$-modules.

A stacky approach to the study of prismatic crystals has been developed independently by Drinfeld ([Drinfeld20](#Drinfeld20)) and Bhatt-Lurie ([BhattLurie22](#BhattLurie22)).

Given p-adic formal scheme $X$, one can attach a stack, called the _Cartier-Witt stack_ and denoted $\mathrm{WCart}_{X}$ by Bhatt-Lurie, and called the _[[prismatization]]_ of $X$ and denoted $X^{\Delta}$ by Drinfeld. When $X$ is quasi-syntomic, one can identify the $\infty$-category of crystals of $(p,I_{\Delta})$-complete complexes on $(X_{\Delta},\mathcal{O}_{\Delta})$ with the derived $\infty$-category of quasi-coherent sheaves on $\mathrm{WCart}_{X}$ ([Bhatt21](#Bhatt21), Remark 2.6).

## Applications

Prismatic cohomology can be used to obtain the following inequality for $X$ a proper smooth [[formal scheme]] over $\mathbb{C}_{p}$ (here $k$ is the residue field of $\mathcal{O}_{\mathbb{C}_{p}}$):

$$dim_{\mathbb{F}_{p}}H_{et}^{i}(X_{\mathbb{C}_{p}},\mathbb{F}_{p})\leq dim_{k}H_{dR}^{i}(X_{k})$$

Prismatic cohomology has also been used in [Bhatt20](#Bhatt20) to prove that modulo a prime power the absolute integral closure of an excellent Noetherian domain is Cohen-Macaulay. The proof also uses a p-adic version of the [[Riemann-Hilbert correspondence]] being developed in yet-unpublished work of [[Bhargav Bhatt]] and [[Jacob Lurie]].

Prismatic cohomology has also been used to construct a version of [[syntomic cohomology]], which describes the graded pieces of a "motivic" filtration on p-adic etale K-theory. This is analogous to the filtration on [[topological K-theory]] whose graded pieces are described by the shifted singular cohomology complex, and is also analogous to the filtration on [[algebraic K-theory]] by [[motivic cohomology]]. This is used by Antieau, Krause and Nikolaus in [AKN22](#AKN22) to determine the K-groups of $\mathbb{Z}/p^{n}$.

## Historical Precursors

Prismatic cohomology was developed by [[Bhargav Bhatt]] and [[Peter Scholze]] following earlier work on developing an integral version of [[p-adic Hodge theory]]. Some of this earlier work includes $A_inf$-cohomology in [BhattMorrowScholze16](#BhattMorrowScholze16) and integral p-adic Hodge theory via [[topological Hochschild homology]] in [BhattMorrowScholze16](#BhattMorrowScholze16), both of which were developed together with [[Matthew Morrow]].

## Related entries

* [[p-adic Hodge theory]]
* [[perfectoid spaces]]
* [[topological Hochschild homology]]
* [[arithmetic differential geometry]]
* [[Borger's absolute geometry]]

## References

Prismatic cohomology was introduced in

* {#BhattScholze19}[[Bhargav Bhatt]], [[Peter Scholze]], _Prisms and Prismatic Cohomology_, preprint (2019) arXiv:[1905.08229](https://arxiv.org/abs/1905.08229)

A survey of recent developments is given in

* {#Bhatt21}[[Bhargav Bhatt]], _Algebraic Geometry in Mixed Characteristic_, preprint (2021) arXiv:[2112.12010](https://arxiv.org/abs/2112.12010)

Lecture notes include

* [[Bhargav Bhatt]], _Prismatic cohomology_, course at Columbia University, 2018 [lecture notes](http://www-personal.umich.edu/~bhattb/teaching/prismatic-columbia/)

Lecture notes taken by Chao Li, from the same lectures (contains some material not included in the above)

* [[Bhargav Bhatt]], _Prismatic cohomology_, course at Columbia University, 2018 (lecture notes taken by Chao Li) [lecture notes](http://www.math.columbia.edu/~chaoli/doc/BhattEilenberg.html)

Some other lectures on prismatic cohomology:

* [[Kiran Kedlaya]], _Notes on prismatic cohomology_, 2020 [lecture notes](https://kskedlaya.org/prismatic/prismatic.html)

* [[Matthew Emerton]], _Prismatic cohomology_, lecture notes (2020) &lbrack;[webpage](http://www.math.uchicago.edu/~emerton/prismatic/prismatic.html)&rbrack;

For some introductory comments see

* [[Terence Tao]], _Prismatic cohomology_, ([blog post](https://terrytao.wordpress.com/2019/03/19/prismatic-cohomology/))

* Riccardo Pengo ([MO answer](https://mathoverflow.net/a/333062/447))

Recent developments include

* {#Drinfeld20}[[Vladimir Drinfeld]], _Prismatization_ (2020) arXiv:[2005.04746] (https://arxiv.org/abs/2005.04746)

* {#BhattLurie22}[[Bhargav Bhatt]], [[Jacob Lurie]], _Absolute Prismatic Cohomology_, preprint (2022) arXiv:[2022.06120](https://arxiv.org/abs/2201.06120)

* [[Bhargav Bhatt]], [[Jacob Lurie]], _The Prismatization of $p$-adic Formal Schemes_, preprint (2022) arXiv:[2022.06124](https://arxiv.org/abs/2201.06124)

* {#Bhatt20}[[Bhargav Bhatt]], _Cohen-Macaulayness of Absolute Integral Closures_, preprint (2020) arXiv:[2008.08070](https://arxiv.org/abs/2008.08070)

* [[Jeremy Hahn]], [[Arpon Raksit]], [[Dylan Wilson]], _A motivic filtration on the topological cyclic homology of commutative ring spectra_, preprint (2022) arXiv:[2206.11208] (https://arxiv.org/abs/2206.11208)

An application to [[algebraic K-theory]] is

* {#AKN22} [[Benjamin Antieau]], [[Achim Krause]], [[Thomas Nikolaus]], _On the K-theory of $\mathbb{Z}/p^{n}$ -- Announcement_ &lbrack;[arXiv:2204.03420](https://arxiv.org/abs/2204.03420)&rbrack;

Historical precursors of prismatic cohomology are

* {#BhattMorrowScholze16}[[Bhargav Bhatt]], [[Matthew Morrow]], [[Peter Scholze]] *Integral $p$-adic Hodge Theory* &lbrack;[arXiv:1602.03148](https://arxiv.org/abs/1602.03148)&rbrack;

* {#BhattMorrowScholze18}[[Bhargav Bhatt]], [[Matthew Morrow]], [[Peter Scholze]], *Topological Hochschild Homology and Integral $p$-adic Hodge Theory* &lbrack;[arXiv:1802.03261](https://arxiv.org/abs/1802.03261)&rbrack;
