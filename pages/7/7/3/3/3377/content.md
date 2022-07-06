
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Higgs bundle_ is a [[holomorphic vector bundle]] $E$ together with a [[differential form|1-form]] $\Phi$ with values in the [[endomorphisms]] of (the [[fibers]] of) $E$, such that $\Phi \wedge \Phi = 0$.

Higgs bundles play a central role in [[nonabelian Hodge theory]].


## Terminology
 {#Terminology}

The term was introduced by [[Nigel Hitchin]] as a reference to roughly analogous structures in the [[standard model of particle physics]] related to the _[[Higgs field]]_.

> ([Witten 08, remark 2.1](#Witten08)): As an aside, one may ask how closely related $\phi$, known in the present context as the Higgs field, is to the Higgs fields of [[standard model of particle physics|particle physics]]. Thus, to what extent is the terminology that was introduced in Hitchin (1987a) actually justified? The main difference is that [[Higgs fields]] in particle physics are [[scalar fields]], while $\phi$ is a [[differential 1-form|one-form]] on $C$ (valued in each case in some [[representation]] of the [[gauge group]]). However, although Hitchin's equations were first written down and studied directly, they can be obtained from [[N=4 D=4 super Yang-Mills theory|N = 4 supersymmetric gauge theory]] via a sort of twisting procedure (similar to the procedure that leads from N = 2 supersymmetric gauge theory to Donaldson theory). In this twisting procedure, some of the Higgs-like scalar fields of $N = 4$ super Yang-Mills theory are indeed converted into the Higgs field that enters in Hitchin's equations. $[$ [Kapustin-Witten 06](#KapustinWitten06) $]$ This gives a reasonable justification for the terminology.

## Definition

### In components

Let $\mathcal{E}$ be a [[sheaf]] of [[section]]s of a [[holomorphic vector bundle]] $E$ on [[complex manifold]] $M$ with [[structure sheaf]] $\mathcal{O}_M$ and [[module]] of [[Kähler differential]]s $\Omega^1_M$. 

A **Higgs field** on $\mathcal{E}$ is an $\mathcal{O}_M$-linear map

$$

  \Phi : \mathcal{E}\to \Omega^1_M\otimes_{\mathcal{O}_M}\mathcal{E}
$$

satisfying the integrability condition $\Phi\wedge\Phi = 0$. The pair of data $(E,\Phi)$ is then called a **Higgs bundle**. 

(Notice that this is similar to but crucially different the definition of a [[flat connection]] on a [[vector bundle]]. For that the map $\Phi$ is just $\mathbb{C}$-linear and the integrability condition is $\mathbf{d}\phi + \Phi\wedge\Phi = 0$.)

Higgs bundles can be considered as a limiting case of a [[curvature|flat]] [[connection on a bundle|connection]] in the limit in which its exterior differential tends to zero, be obtained by rescaling. So the equation $d u/dz = A(z)u$ where $A(z)$ is a matrix of connection can be rescaled by putting a small parameter in front of $d u/dz$. 

### Formulation in D-geometry

Analogous to how the [[de Rham stack]] $\int_{inf} X = X_{dR}$ of $X$ is the ([[homotopy quotient|homotopy]]) [[quotient]] of $X$ by the first order [[infinitesimal neighbourhood]] of the [[diagonal]] in $X \times X$, so there is a space ([[stack]]) $X_{Dol}$ which is the [[formal completion]] of the 0-section of the [[tangent bundle]] of $X$ ([Simpson 96](#Simpson96)).

Now a [[flat vector bundle]] on $X$ is essentially just a [[vector bundle]] on the [[de Rham stack]] $X_{dR}$, and a [[Higgs bundle]] is essentially just a [[vector bundle]] on $X_{Dol}$. Therefore in this language the nonabelian Hodge theorem reads (for $G$ a linear [[algebraic group]] over $\mathbb{C}$)

$$
  \mathbf{H}(X_{dR}, \mathbf{B}G)
  \simeq
  \mathbf{H}(X_{Dol}, \mathbf{B}G)^{ss,0}
  \,,
$$

where the superscript on the right denotes restriction to semistable Higgs bundles with vanishing [[first Chern class]] (see [Raboso 14, theorem 4.2](#Raboso14)). 


## Properties

### Stability

For a Higgs bundle to admit a harmonic metric (...) it needs to be _stable_ (...).

Stability is defined similarly to stability for holomorphic vector bundles except that instead of quantifying over all proper non-zero sub-bundles, one only considers proper $\Phi$ invariant sub-bundles. So in particular for $\Phi=0$, this is stability of the underlying vector bundle.

### In nonabelian Hodge theory

In [[nonabelian Hodge theory]] the [[moduli space]] of stable Higgs bundles over a [[Riemann surface]] $X$ is identified with that of  [[special linear group]] $SL(n,\mathbb{C})$ [[irreducible representations]] of its [[fundamental group]] $\pi_1(X)$.

## Examples

### Rank 1

In the special case that $E$ has [[rank]] 1, hence is a [[line bundle]], the form $\Phi$ is simply any holomorphic 1-form. This case is also called that of an **abelian Higgs bundle**.

### Bundles of holomorphic forms

Let $X$ be a [[complex manifold]] and $\omega \in \Omega^{k,0}(X)$ for odd $k$. Then $\Omega^{\bullet,0}(X)$ becomes a Higgs bundle when equipped with the endomorphis-valued 1-form which sends a holomorphic vector $v$ to the wedge product operation with the contraction of $\omega$ with $v$.

This is discussed in ([Seaman 98](#Seaman98))

## Related concepts

* [[Hitchin system]]

* [[nonabelian Hodge theory]]

* [[topological recursion]]

## References

### General

The [[moduli space]] of Higgs bundles over an [[algebraic curve]] is one of the principal topics in works of [[Nigel Hitchin]] and [[Carlos Simpson]] in late 1980-s and 1990-s (and later Ron Donagi, Tony Pantev, etc....).  

* [[Nigel Hitchin|N.J. Hitchin]], _Stable bundles and integrable systems_,  Duke Math. J. , 54  (1987)  pp. 91&#8211;114 [MR89a:32021](http://www.ams.org/mathscinet-getitem?mr=89a:32021) [doi](http://dx.doi.org/10.1215/S0012-7094-87-05408-1) [euclid](http://projecteuclid.org/euclid.dmj/1077305506); _The self-duality equations on a Riemann surface_, Proc. London Math. Soc. (3) 55 (1987), no. 1, 59&#8211;126, [MR887284](http://www.ams.org/mathscinet-getitem?mr=887284) [doi](http://dx.doi.org/10.1112/plms/s3-55.1.59); _Flat connections and geometric quantization_, Comm. Math. Phys. __131__, n 2 (1990), 347-380, [euclid](http://projecteuclid.org/euclid.cmp/1104200841)


* [[Carlos Simpson]], _Higgs bundles and local systems_, Publ. Math&#233;matiques de l'IH&#201;S __75__ (1992), p. 5-95, [numdam](http://www.numdam.org/item?id=PMIHES_1992__75__5_0), [MR94d:32027](http://www.ams.org/mathscinet-getitem?mr=94d:32027)

* [[Ludmil Katzarkov]], [[Dmitri Orlov]], [[Tony Pantev]], _Notes on Higgs bundles and D-branes_, (delivered as a lecture by Tony Pantev at winter school at Guanajuato 2013 [link](http://www.cimat.mx/Eventos/moduli_spaces2013)) draft [pdf](http://www.cimat.mx/Eventos/moduli_spaces2013/img/tony_pantev.pdf)

* S. B. Bradlow, O. Garc&#237;a-Prada, P. B. Gothen, _WHAT IS...a Higgs Bundle?_, Notices AMS, [pdf](http://www.ams.org/notices/200708/tx070800980p.pdf)

* [[Michael Murray]], [[Danny Stevenson]], _Higgs fields, bundle gerbes and string structures_, [arxiv/math.DG/0106179](http://arxiv.org/abs/math.DG/0106179)

* [[David Baraglia]], _Cyclic Higgs bundles and the affine Toda equations_, [arxiv/1011.6421](http://arxiv.org/abs/1011.6421)

Around lemma 6.4.1 in 

* [[Kevin Costello]], _Notes on supersymmetric and holomorphic field theories in dimension 2 and 4_ ([pdf](http://www.math.northwestern.edu/~costello/sullivan.pdf))

See also 

* Donu Arapura, _[MO comment on Higgs bundles](http://mathoverflow.net/questions/101326/what-is-the-current-state-of-the-mathematics-of-higgs-fields/101347#101347)_

Discussion of the topology of the moduli space of Higgs bundles is in

* {#Rayan18} [[Steven Rayan]], _Aspects of the topology and combinatorics of Higgs bundle moduli spaces_, SIGMA 14 (2018) 129, 18 pages ([arXiv:1809.05732](https://arxiv.org/abs/1809.05732))

Discussion in terms of $X_{Dol}$ is in 

* {#Simpson96} [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_, Santa Cruz 1995, Proc. Sympos. Pure Math., vol. 62, Amer. Math. Soc., Providence, RI, 1997, pp. 217{281. MR
1492538 (99g:14028) ([arXiv:9604005](http://arxiv.org/abs/alg-geom/9604005))

* {#Raboso14} [[Alberto García Raboso]], _A twisted nonabelian Hodge correspondence_, PhD thesis 2014 ([pdf slides](http://www.math.toronto.edu/agraboso/files/TwistedNAHT_Talk_Handout.pdf))

Discussion of the example of homolorphic forms is in 

* {#Seaman98} Walter Seaman, _Higgs Bundles and Holomorphic Forms_ ([arXiv:9811097](http://arxiv.org/abs/math/9811097))

Discussion in the context of [[geometric Langlands duality]] includes

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_, Communications in Number Theory and Physics Volume 1 (2007) Number 1 ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))



* {#Witten08} [[Edward Witten]], _Mirror Symmetry, Hitchin's Equations, And Langlands Duality_ ([arXiv:0802.0999](http://arxiv.org/abs/0802.0999))

### Relation to $Spin(7)$-manifolds

Relating [[M-theory on Spin(7)-manifolds]] with [[F-theory on Spin(7)-manifolds]] via [[Higgs bundles]]:

* {#CHRTZ20} [[Mirjam Cvetic]], [[Jonathan Heckman]], Thomas B. Rochais, Ethan Torres, [[Gianluca Zoccarato]], _Geometric Unification of Higgs Bundle Vacua_ ([arXiv:2003.13682](https://arxiv.org/abs/2003.13682))



[[!redirects Higgs bundles]]