
#Contents#
* table of contents
{:toc}

## Idea

The most basic form of the Riemann--Hilbert correspondence states that the [[category]] of [[flat connection|flat]] [[vector bundles]] on a suitable [[space]] is equivalent to the category of [[local systems]].

While [[Riemann-Hilbert problem|Hilbert's 21st problem]] has a negative solution, there is a generalized sheaf-theoretical formulation which leads to an equivalence of categories discovered by Mebkhout and a bit later also by [[Kashiwara]].

## p-torsion and p-adic Riemann-Hilbert correspondence

[[Bhargav Bhatt]] and [[Jacob Lurie]] have formulated a version of the Riemann-Hilbert correspondence for finite type schemes over a complete and algebraically closed extension of the [[p-adic numbers]]:

\begin{proposition}([Bhatt21](#Bhatt21), Theorem 5.1)

Let $C$ be a complete and algebraically closed extension of $\mathbb{Q}_{p}$ and let $X$ be of finite type over $\mathcal{O}_{C}$. Then there is a natural exact functor

$$\RH: D_{\cons}^{b}(X_{C},\mathbb{F}_{p})\to D_{\qc}^{b}(X\otimes_{\mathcal{O}_{C}} \mathcal{O}_{C}/p).$$

This functor commutes with proper pushforward, intertwines [[Verdier duality]] and [[Grothendieck duality]] in the almost category, and interacts well with the perverse [[t-structure]].
\end{proposition}

Bhatt and Lurie also have a version with p-adic, instead of p-torsion, coefficients (this time the schemes have to be smooth proper varieties over a finite extension of the p-adic numbers).

\begin{proposition}([Bhatt21](#Bhatt21), Theorem 5.4)

Let $K$ be a finite extension of $\mathbb{Q}_{p}$ and let $X$ be a smooth proper variety over $K$. Then there is a natural exact functor

$$\RH_{\mathcal{D}}: D_{wHT}^{b}(X_{C},\mathbb{Q}_{p})\to DF_{coh}(\mathcal{D}_{X})$$

where $D_{wHT}^{b}(X_{C},\mathbb{Q}_{p})$ is a full subcategory of $D_{cons}^{b}(X_{C},\mathbb{Q}_{p})$ spanned by "weakly Hodge-Tate sheaves" and $DF_{coh}(\mathcal{D}_{X})$ is a suitable derived category of [[D-modules|$\mathcal{D}_{X}$-modules]] equipped with a "good" filtration. This functor commutes with proper pushforward, intertwines [[Verdier duality]] and [[Grothendieck duality]] in the almost category, and interacts well with the perverse [[t-structure]].
\end{proposition}

## Related entries

* [[Hilbert's problems]]

* [[flat infinity-connection]]

* [[infinity-local system]]

## References

* [[Alain Connes]], [[Matilde Marcolli]] _[[Noncommutative Geometry, Quantum Fields and Motives]]_

* Wikipedia, _[Riemann-Hilbert correspondence](http://en.wikipedia.org/wiki/Riemann%E2%80%93Hilbert_correspondence)_

* Z. Mebkhout, _Le formalisme des six op&#233;rations de Grothendieck pour les $\mathcal{D}_X$-modules coh&#233;rents_, Travaux en Cours __35__. Hermann, Paris, 1989. x+254 pp. [MR90m:32026](http://www.ams.org/mathscinet-getitem?mr=1008245)

* [[Andrea D'Agnolo]], [[Masaki Kashiwara]], _Riemann-Hilbert correspondence for holonomic D-modules_, [arxiv/1311.2374](http://arxiv.org/abs/1311.2374)

> The classical Riemann-Hilbert correspondence establishes an equivalence between the triangulated category of _regular_ holonomic D-modules and that of constructible sheaves. In this paper, we prove a Riemann-Hilbert correspondence for holonomic D-modules which are not necessarily regular. The construction of our target category is based on the theory of ind-sheaves by Kashiwara-Schapira and influenced by Tamarkin's work. Among the main ingredients of our proof is the description of the structure of flat meromorphic connections due to Mochizuki and Kedlaya. 

Generalization to [[flat infinity-connections]] via the [[dg-nerve]] and [[iterated integrals]] is discussed in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_, [arXiv:0908.2843](http://arxiv.org/abs/0908.2843)

Generalization to [[p-adic geometry]] is discussed in

* [[Jacob Lurie]], _A Riemann--Hilbert Correspondence in p-adic Geometry_, [Felix Klein Lectures 2022](https://www.hcm.uni-bonn.de/events/eventpages/felix-klein-lectures/fkl-2022-lurie/).

* {#Bhatt21}[[Bhargav Bhatt]], _Algebraic Geometry in Mixed Characteristic_, preprint (2021) arXiv:[2112.12010](https://arxiv.org/abs/2112.12010)

[[!redirects Riemann-Hilbert correspondence]]
[[!redirects Riemann–Hilbert correspondence]]
[[!redirects Riemann--Hilbert correspondence]]
