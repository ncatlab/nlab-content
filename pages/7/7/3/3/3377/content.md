
#Contents#
* table of contents
{:toc}

## Idea

A _Higgs bundle_ is a [[holomorphic bundle|holomorphic]] [[vector bundle]] $E$ together with a [[differential form|1-form]] $\Phi$ with values in the [[endomorphisms]] of (the [[fibers]] of) $E$, such that $\Phi \wedge \Phi = 0$.

The term was introduced by [[Nigel Hitchin]] as a reference to roughly analogous structures in the [[standard model of particle physics]] related to the _[[Higgs field]]_.

Higgs bundles play a central role in [[nonabelian Hodge theory]].

## Definition

Let $\mathcal{E}$ be a [[sheaf]] of [[section]]s of a holomorphic [[bundle]] $E$ on [[complex manifold]] $M$ with [[structure sheaf]] $\mathcal{O}_M$ and [[module]] of [[Kähler differential]]s $\Omega^1_M$. 

A **Higgs field** on $\mathcal{E}$ is an $\mathcal{O}_M$-linear map

$$
  \Phi : \mathcal{E}\to \Omega^1_M\otimes_{\mathcal{O}_M}\mathcal{E}
$$

satisfying the integrability condition $\Phi\wedge\Phi = 0$. The pair of data $(E,\Phi)$ is then called a **Higgs bundle**. 

Higgs bundle can be considered as a limiting case of a [[curvature|flat]] [[connection on a bundle|connection]] in the limit in which its exterior differential tends to zero, be obtained by rescaling. So the equation $d u/dz = A(z)u$ where $A(z)$ is a matrix of connection can be rescaled by putting a small parameter in front of $d u/dz$. 

## Properties

### Stability

For a Higgs bundle to admit a harmonic metric (...) it needs to be _stable_ (...).

### In nonabelian Hodge theory

In [[nonabelian Hodge theory]] the [[moduli space]] of stable Higgs bundles overa [[Riemann surface]] $X$ is identified with that of  [[special linear group]] $SL(n,\mathbb{C})$ [[irreducible representations]] of its [[fundamental group]] $\pi_1(X)$.

## Examples

### Rank 1

In the special case that $E$ has [[rank]] 1, hence is a [[line bundle]], the form $\Phi$ is simply any holomorphic 1-form. This case is also called that of an **abelian Higgs bundle**.

## References

The [[moduli space]] of Higgs bundles over an [[algebraic curve]] is one of the principal topics in works of [[Nigel Hitchin]] and [[Carlos Simpson]] in late 1980-s and 1990-s (and later Ron Donagi, Tony Pantev...).  

* [[Nigel Hitchin|N.J. Hitchin]], _Stable bundles and integrable systems_,  Duke Math. J. , 54  (1987)  pp. 91&#8211;114 [MR89a:32021](http://www.ams.org/mathscinet-getitem?mr=89a:32021) [doi](http://dx.doi.org/10.1215/S0012-7094-87-05408-1) [euclid](http://projecteuclid.org/euclid.dmj/1077305506); _The self-duality equations on a Riemann surface_, Proc. London Math. Soc. (3) 55 (1987), no. 1, 59&#8211;126, [MR887284](http://www.ams.org/mathscinet-getitem?mr=887284) [doi](http://dx.doi.org/10.1112/plms/s3-55.1.59); _Flat connections and geometric quantization_, Comm. Math. Phys. __131__, n 2 (1990), 347-380, [euclid](http://projecteuclid.org/euclid.cmp/1104200841)
* [[Carlos Simpson]], _Higgs bundles and local systems_, Publ. Math&#233;matiques de l'IH&#201;S __75__ (1992), p. 5-95, [numdam](http://www.numdam.org/item?id=PMIHES_1992__75__5_0), [MR94d:32027](http://www.ams.org/mathscinet-getitem?mr=94d:32027)
* [[Ludmil Katzarkov]], [[Dmitri Orlov]], [[Tony Pantev]], _Notes on Higgs bundles and D-branes_, (delivered as a lecture by Tony Pantev at winter school at Guanajuato 2013 [link](http://www.cimat.mx/Eventos/moduli_spaces2013)) draft [pdf](http://www.cimat.mx/Eventos/moduli_spaces2013/img/tony_pantev.pdf)
* S. B. Bradlow, O. Garc&#237;a-Prada, P. B. Gothen, _WHAT IS...a Higgs Bundle?_, Notices AMS, [pdf](http://www.ams.org/notices/200708/tx070800980p.pdf)
* [[Michael Murray]], [[Danny Stevenson]], _Higgs fields, bundle gerbes and string structures_, [arxiv/math.DG/0106179](http://arxiv.org/abs/math.DG/0106179)
* David Baraglia, _Cyclic Higgs bundles and the affine Toda equations_, [arxiv/1011.6421](http://arxiv.org/abs/1011.6421)

Around lemma 6.4.1 in 

* [[Kevin Costello]], _Notes on supersymmetric and holomorphic field theories in dimension 2 and 4_ ([pdf](http://www.math.northwestern.edu/~costello/sullivan.pdf))

See also 

* Donu Arapura, _[MO comment on Higgs bundles](http://mathoverflow.net/questions/101326/what-is-the-current-state-of-the-mathematics-of-higgs-fields/101347#101347)_

[[!redirects Higgs bundles]]