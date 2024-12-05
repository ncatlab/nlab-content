
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Gopakumar-Vafa invariants are supposed to count the number of [[pseudoholomorphic curves]] and represent the number of [[BPS states]] on a three-dimensional projective [[Calabi-Yau manifold]], hence are of interest in [[string theory]].

[[Rajesh Gopakumar]] and [[Cumrun Vafa]] first described the invariant in ([GV 98a](#GopakumarVafa98a), [GV 98b](#GopakumarVafa98b), [GV 98c](#GopakumarVafa98c), [GV 99](#GopakumarVafa99)). Instead of directly defining the invariant, they instead described properties and connections to other invariants. [[Gromov-Witten invariants]] and Pandharipande-Thomas invariants also count the numbers of holomorphic curves, so equivalences between the three invariants known as _GW/PT/GV correspondence_ are conjectured. But all of them use additional data: [[Gromov-Witten invariants]] additionally use maps into the manifold, Pandharipande-Thomas invariants additionally use points on the curve (D0-D2-D6 
bound states) and [[Gopakumar-Vafa invariants]] additionally use [[vector bundles]] on the curve (D2-branes). As a result, the Gromov-Witten invariant is [[rational number|rational]], hence not really counting a number of curves. On the other hand, Pandharipande-Thomas invariants and Gopakumar-Vafa invariants are [[integers]].

## GW/PT/GV correspondence

Let $M$ be a three-dimensional [[Calabi-Yau manifold]], $\beta\in H_2(M,\mathbb{Z})$ the homology class and $g$ the [[genus]] of a [[pseudoholomorphic curve]]. Let $\operatorname{GW}(g,\beta)\in\mathbb{Q}$ be the [[Gromov-Witten invariant]], $\operatorname{PT}(g,\beta)\in\mathbb{Z}$ be the Pandharipande-Thomas invariant and $\operatorname{GV}(n,\beta)\in\mathbb{Z}$ be the [[Gopakumar-Vafa invariant]], then:
$$
\sum_{g=0}^\infty\sum_{\beta\in H_2(M,\mathbb{Z})}\operatorname{GW}(g,\beta)q^{\beta}\lambda^{2g-2}
=\sum_{k=1}^\infty\sum_{g=0}^\infty\sum_{\beta\in H_2(M,\mathbb{Z})}\frac{\operatorname{GV}(g,\beta)}{k}\left(2\sin\left(\frac{k\lambda}{2}\right)\right)^{2g-2}q^{k\beta};
$$
$$
\ln\left(
1+\sum_{n=-\infty}^\infty\sum_{\beta\in H_2(M,\mathbb{Z})}\text{PT}(n,\beta)q^\beta\lambda^n
\right)
=\sum_{k=1}^\infty\sum_{n=-\infty}^\infty\sum_{\beta\in H_2(M,\mathbb{Z})}\frac{\operatorname{GV}(g,\beta)}{k}(-1)^{g-1}\left(
(-\lambda)^{\frac{k}{2}}-(-\lambda)^{\frac{k}{2}}
\right)^{2g-2}q^{k\beta}.
$$

([Ionel & Parker 99, Eq. (0.1)](#IonelParker99), [Toda 21, Eq. (7.2) & Thrm. 7.1](#Toda21))

## Related entries

* [[topological string]]

* [[black holes in string theory]]

## Related concepts

* [[Gopakumar-Vafa duality]]

## References

Original introduction:

* {#GopakumarVafa98a} [[Rajesh Gopakumar]], [[Cumrun Vafa]], _M-Theory and Topological Strings--I_ (1998), ([arXiv:hep-th/9809187](https://arxiv.org/abs/hep-th/9809187), [bibcode:1998hep.th....9187G](https://ui.adsabs.harvard.edu/abs/1998hep.th....9187G))

* {#GopakumarVafa98b} [[Rajesh Gopakumar]], [[Cumrun Vafa]], _M-Theory and Topological Strings--II_ (1998), ([arXiv:hep-th/9812127](https://arxiv.org/abs/hep-th/9812127), [bibcode:1998hep.th...12127G](https://ui.adsabs.harvard.edu/abs/1998hep.th...12127G))

* {#GopakumarVafa98c} [[Rajesh Gopakumar]], [[Cumrun Vafa]], _Topological Gravity as Large N Topological Gauge Theory_ (1998), _Advances in Theoretical and Mathematical Physics_ **2** (2), pp. 413–442, [doi:10.4310/ATMP.1998.v2.n2.a8](https://doi.org/10.4310/ATMP.1998.v2.n2.a8), [arxiv:hep-th/9802016](https://arxiv.org/abs/hep-th/9802016), [bibcode:1998hep.th....2016G](https://ui.adsabs.harvard.edu/abs/1998hep.th....2016G)

* {#GopakumarVafa99} [[Rajesh Gopakumar]], [[Cumrun Vafa]], _On the Gauge Theory/Geometry Correspondence_ (1999), _Advances in Theoretical and Mathematical Physics_ **3** (5), pp. 1415–1443, [doi:10.4310/ATMP.1999.v3.n5.a5](https://link.intlpress.com/JDetail/1805563068753059842), [arxiv:hep-th/9811131](https://arxiv.org/abs/hep-th/9811131), [bibcode:1998hep.th...11131G](https://ui.adsabs.harvard.edu/abs/1998hep.th...11131G)

Further references:

* {#IonelParker99} Eleny-Nicoleta Ionel und Thomas H. Parker, _The Gopakumar–Vafa formula for symplectic manifolds_ (1999), _Annals of Mathematics, Second Edition_ **187** (1), pp. 1–64, [doi:10.4007/annals.2018.187.1.1](https://annals.math.princeton.edu/2018/187-1/p01), [arxiv:1306.1516](https://arxiv.org/abs/1306.1516), [bibcode:1998hep.th...11131G](https://ui.adsabs.harvard.edu/abs/1998hep.th...11131G)

* {#Toda21} Yukinobu Toda, _Recent Progress on the Donaldson–Thomas Theory: Wall-Crossing and Refined Invariants_ (2021.12.15) , [doi:10.1007/978-981-16-7838-7](https://link.springer.com/book/10.1007/978-981-16-7838-7)

* Yukinobu Toda, _A mathematical definition of Gopakumar-Vafa invariants_, [pdf](https://indico.ipmu.jp/event/134/contributions/573/attachments/457/507/18_03_toda.pdf)

See also:

* Wikipedia, _[Gopakumar-Vafa invariant](https://en.wikipedia.org/wiki/Gopakumar%E2%80%93Vafa_invariant)_

[[!redirects Gopakumar-Vafa invariants]]
[[!redirects GW/PT/GV correspondence]]