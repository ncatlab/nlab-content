
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Analytic spaces are [[spaces]] that are locally modeled on [[Isbell duality|formal duals]] of subalgebras [[associative algebra|algebras]] of [[power series]] algebras on elements with certain convergence properties. 

In complex [[analytic geometry]] analytic spaces are a vast generalization of complex analytic manifolds. There are also analytic spaces over nonarchimedean spaces, the subject introduced by Tate and called [[rigid analytic geometry]]. 
There are _rigid analytic spaces_, defined with respect to maximal spectra of these algebras, and _analytic spaces_ defined with respect to a kind of [[Gelfand spectrum]], due to [[Vladimir Berkovich]]. For the former definition see _[[rigid analytic geometry]]_. This entry is concerned with the more general notion due to Berkovich, which makes sense also over trivially [[valuation|valued]] and [[non-archimedean fields]].

For more background see _[[analytic geometry]]_.

## Definition of rigid analytic spaces

Let $k$ be a [[non-archimedean field]].

+-- {: .num_defn}
###### Definition

Given $n \in \mathbb{N}$  and positive elements $\{r_1, \cdots, r_n \in k\}$, consider the sub-[[power series]] [[associative algebra|algebra]] over $k$ defined by

$$
  \{\frac{1}{r_1} T_1 , \cdots, \frac{1}{r_n}T_n\}
  :=
  \left\{
    \sum_\nu a_\nu T^\nu | \lim_{{\vert \nu\vert} \to 0} {\vert a_\nu \vert} r^\nu = 0
  \right\}
  \,.
$$

This is a commutative [[Banach algebra]] over $k$ with [[norm]] ${\Vert f \Vert} = max {\vert a_\nu\vert} r^\nu$.

A **$k$-[[affinoid algebra]]** is a commutative Banach $k$-algebra $A$ for which there exists $n$ and $\{r_i\}$ as above and an [[epimorphism]]

$$
  \{\frac{1}{r_1} T_1 , \cdots, \frac{1}{r_n}T_n\}
  \to 
  A
$$

such that the norm on $A$ is the quotient norm.

If one can choose here $r_i = 1$ for all $i$ then $A$ is called **strictly $k$-affinoid**.

The [[category]] of **$k$-affinoid spaces** is the [[opposite category]] of the category of $k$-affinoid algebras and bounded [[homomorphisms]] between them.

=--

Via the [[analytic spectrum]] there is a [[topological space]] associated with any $k$-affinoid space.
 
+-- {: .num_defn}
###### Definition

A **$k$-analytic space** is a space obtained by gluing of $k$-affinoid spaces. 

More precisely (...)

=--

See [Berkovich 98, paragraph 2](#BerkovichReview).

## Properties

### Local contractibility
 {#LocalContractibility}

A [[complex numbers|complex]] analytic space is locally isomorphic to a [[polydisk]] and hence is trivially a [[locally contractible space]]. But over a [[non-archimedean field]] analytic spaces no longer need to be locally isomorphic to polydisks (but $p$-adic polydisks are still contractible ([Berkovich 90](#Berkovich90))). The following result establishes under mild conditions, that general analytic spaces are nevertheless locally contractible.



Assume that the [[valuation]] on the ground field $k$ is nontrivial.

+-- {: .num_defn #LocallyEmbeddableInASmoothSpace}
###### Definition

A $k$-analytic space $X$ is called _locally embeddable in a smooth space_ if each point of $X$ has an [[open neighbourhood]] [[isomorphism|isomorphic]] to a strictly $k$-analytic domain in smooth $k$-analytic space. 

=--

+-- {: .num_theorem}
###### Theorem

Every $k$-analytic space which is locally embeddable in a smooth space, def. \ref{LocallyEmbeddableInASmoothSpace}, is a [[locally contractible space]].

More precisely, every point of a locally smooth $k$-analytic space has an open neighbourhood $U$ which is contractible, and which is a union $U = \coprod_{i = 1}^\infty U_i$ of analytic domains.

=--

The local contractibility is [Berkovich (1999), theorem 9.1](#BerkovichContractible). The refinement by inductive systems on analytic domains is in [Berkovich (2004)](#BerkovichContractibleII).

## References

### Introductions and reviews

Basic notions are listed in 

* M. Temkin, _Non-archimedean analytic spaces_ ([pdf slides](http://www.math.huji.ac.il/~temkin/lectures/Non-Archimedean_Analytic_Spaces.pdf))

A review of basic definitions and facts about affinoid and rigid $k$-analytic spaces can be found in 

* Ga&#235;tan Chenevier, _lecture 5_ ([pdf](http://www.math.polytechnique.fr/~chenevier/coursIHP/chenevier_lecture5.pdf))

See also the references at [[rigid analytic geometry]].

A review of definitions and results on  $k$-analytic spaces is in 

* [[Vladimir Berkovich]], _$p$-Adic analytic spaces_, in Proceedings of the International Congress of Mathematicians, Berlin, August 1998, Doc. Math. J. DMV, Extra Volume ICM II (1998), 141-151 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/ICM98_1998.pdf)) 

A more detailed set of lecture notes along these lines is

* [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))

The Berkovich spectrum is discussed around section 2.1.4 in the course notes

* [[Frédéric Paugam]], _Global analytic geometry and the functional equation_ (2010) ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-global-analytic-geometry.pdf))


### Original articles

* [[Vladimir Berkovich]], _Spectral theory and analytic geometry over non-Archimedean fields_, Mathematical Surveys and Monographs, vol. 33, American Mathematical Society, Providence, RI, (1990) 169 pp.
  {#Berkovich90}

* [[Vladimir Berkovich]], _&#201;tale cohomology for non-Archimedean analytic spaces_, Publ. Math. IHES 78 (1993), 5-161.

Discussion of local contractibility of smooth $k$-analytic spaces is in 

* [[Vladimir Berkovich]], _Smooth $p$-adic analytic spaces are locally contractible_, Invent. Math. 137 1-84 (1999) ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Inven_1999_137_contra.pdf))
 {#BerkovichContractible}

* [[Vladimir Berkovich]], _Smooth p-adic analytic spaces are locally contractible. II_, in Geometric Aspects of Dwork Theory, Walter de Gruyter & Co., Berlin, (2004), 293-370. ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Dworkvol_2004_contraII.pdf))
 {#BerkovichContractibleII}

See also

* Hans Grauert, Reinhold Remmert, _Theory of Stein spaces_, Grundlehren der Math. Wissenschaften __236__, Springer 1979, xxi+249 pp.; _Coherent analytic sheaves_, Grundlehren der Math. Wissenschaften __265__, Springer 1984. xviii+249 pp.; _Komplexe R&#228;ume_, Math. Ann. __136__, 1958, 245&#8211;318, [DOI](http://dx.doi.org/10.1007/BF01362011)

[[!redirects analytic spaces]]

[[!redirects p-adic analytic space]]
[[!redirects p-adic analytic spaces]]
