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

Prismatic cohomology is a cohomology theory which can specialize into various $p$-adic cohomology theories, including [[étale cohomology]], [[de Rham cohomology]] and [[crystalline cohomology]], as well as the so far conjectural $q$-de Rham cohomology of [[Peter Scholze]]. It is a geometric approach to integral [[p-adic Hodge theory]].

## Prisms

A prism is a pair $(A,I)$ where $A$ is a $\delta$-ring and $I$ is an ideal defining a Cartier divisor on $\mathrm{Spec}(A)$, such that such that $A$ is derived $(p,I)$-complete, and $p \in I + \phi(I)A$.

## Examples of Prisms

* $A=\mathbb{Z}_{p}[[u]]$ and $I=(u-p)$
* $A=A_{\mathrm{inf}}(R)$ and $I=\mathrm{ker}(\theta)$, where $\theta:A_{\mathrm{inf}}(R)\to R$ is the canonical surjection

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

## Applications

Prismatic cohomology can be used to obtain the following inequality for $X$ a proper smooth [[formal scheme]] over $\mathbb{C}_{p}$ (here $k$ is the residue field of $\mathcal{O}_{\mathbb{C}_{p}}$):

$$dim_{\mathbb{F}_{p}}H_{et}^{i}(X_{\mathbb{C}_{p}},\mathbb{F}_{p})\leq dim_{k}H_{dR}^{i}(X_{k})$$

Prismatic cohomology has also been used in [Bhatt20](#Bhatt20) to prove that modulo a prime power the absolute integral closure of an excellent Noetherian domain is Cohen-Macaulay. The proof also uses a p-adic version of the [[Riemann-Hilbert correspondence]] being developed in yet-unpublished work of [[Bhargav Bhatt]] and [[Jacob Lurie]].

Prismatic cohomology has also been used to construct a version of [[syntomic cohomology]], which describes the graded pieces of a "motivic" filtration on p-adic etale K-theory. This is analogous to the filtration on [[topological K-theory]] whose graded pieces are described by the shifted singular cohomology complex, and is also analogous to the filtration on [[algebraic K-theory]] by [[motivic cohomology]].

## Historical Precursors

Prismatic cohomology was developed by [[Bhargav Bhatt]] and [[Peter Scholze]] following earlier work on developing an integral version of [[p-adic Hodge theory]]. Some of this earlier work includes $A_inf$-cohomology in [BhattMorrowScholze16](#BhattMorrowScholze16) and integral p-adic Hodge theory via topological [[Hochschild homology]] in [BhattMorrowScholze16](#BhattMorrowScholze16), both of which were developed together with [[Matthew Morrow]].

## Related entries

* [[arithmetic differential geometry]]
* [[Borger's absolute geometry]]
* [[p-adic Hodge theory]]

## References

Prismatic cohomology was introduced in

* [[Bhargav Bhatt]], [[Peter Scholze]], _Prisms and Prismatic Cohomology_, preprint (2019) arXiv:[1905.08229](https://arxiv.org/abs/1905.08229)

A survey of recent developments is given in

* [[Bhargav Bhatt]], _Algebraic Geometry in Mixed Characteristic_, preprint (2021) arXiv:[2112.12010](https://arxiv.org/abs/2112.12010)

Lecture notes include

* [[Bhargav Bhatt]], _Prismatic cohomology_, course at Columbia University, 2018 [lecture notes](http://www-personal.umich.edu/~bhattb/teaching/prismatic-columbia/)

Lecture notes taken by Chao Li, from the same lectures (contains some material not included in the above)

* [[Bhargav Bhatt]], _Prismatic cohomology_, course at Columbia University, 2018 (lecture notes taken by Chao Li) [lecture notes](http://www.math.columbia.edu/~chaoli/doc/BhattEilenberg.html)

Some other lectures on prismatic cohomology:

* [[Kiran Kedlaya]], _Notes on prismatic cohomology_, 2020 [lecture notes](https://kskedlaya.org/prismatic/prismatic.html)

* [[Matthew Emerton]], _Prismatic cohomology_, 2020 [lecture notes](http://www.math.uchicago.edu/~emerton/prismatic/prismatic.html)

For some introductory comments see

* [[Terence Tao]], _Prismatic cohomology_, ([blog post](https://terrytao.wordpress.com/2019/03/19/prismatic-cohomology/))

* Riccardo Pengo ([MO answer](https://mathoverflow.net/a/333062/447))

Recent developments include

* [[Vladimir Drinfeld]], _Prismatization_ (2020) arXiv:[2005.04746] (https://arxiv.org/abs/2005.04746)

* [[Bhargav Bhatt]], [[Jacob Lurie]], _Absolute Prismatic Cohomology_, preprint (2022) arXiv:[2022.06120](https://arxiv.org/abs/2201.06120)

* [[Bhargav Bhatt]], [[Jacob Lurie]], _The Prismatization of $p$-adic Formal Schemes_, preprint (2022) arXiv:[2022.06124](https://arxiv.org/abs/2201.06124)

* {#Bhatt20}[[Bhargav Bhatt]], _Cohen-Macaulayness of Absolute Integral Closures_, preprint (2020) arXiv:[2008.08070](https://arxiv.org/abs/2008.08070)

* [[Jeremy Hahn]], [[Arpon Raksit]], [[Dylan Wilson]], _A motivic filtration on the topological cyclic homology of commutative ring spectra_, preprint (2022) arXiv:[2206.11208] (https://arxiv.org/abs/2206.11208)

Historical precursors of prismatic cohomology are

* {#BhattMorrowScholze16}[[Bhargav Bhatt]], [[Matthew Morrow]], and [[Peter Scholze]] _Integral $p$-adic Hodge Theory_, arXiv:[1602.03148](https://arxiv.org/abs/1602.03148)

* {#BhattMorrowScholze18}[[Bhargav Bhatt]], [[Matthew Morrow]], and [[Peter Scholze]] _Topological Hochschild Homology and Integral $p$-adic Hodge Theory_, arXiv:[1802.03261](https://arxiv.org/abs/1802.03261)
