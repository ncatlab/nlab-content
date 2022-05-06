
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement

### For horizontal weight systems

+-- {: .num_prop}
###### Proposition

For $D, n \in \mathbb{N}$, the [[ordinary homology]], with [[coefficients]] in some [[ground field]] $\mathbb{F}$, of the [[based loop space]] of the [[ordered configuration space of points]] in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^D$ is [[isomorphism|isomorphic]] to the [[universal enveloping algebra]] $(\mathcal{A}^{pb})^\bullet$ of the [[Lie algebra]] given by the [[infinitesimal braid relations]]:

$$
  H_\bullet
  \big(
    \Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}
    ;
    \mathbb{F}
  \big)
  \;\simeq\;
  (\mathcal{A}^{pb})^\bullet
  \,.
$$

Here $\mathcal{A}^{pb}$ is equivalently the [[associative algebra]] of [[horizontal chord diagrams]] [[quotient vector space|modulo]] the [[2T relations]] and [[4T relations]].

=--

+-- {: .num_prop}
###### Proposition
**(integral [[horizontal weight systems]] are [[integral cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground ring]] $R = \mathbb{Z}$ the [[integers]], there is, for each [[natural number]] $n$, a canonical [[isomorphism]] of [[graded abelian groups]] between 

1. the integral [[weight systems]]

   $$
     \mathcal{W}_{pb}
     \;\coloneqq\;
     Hom_{\mathbb{Z} Mod}
     \big(
       \underset{
         \mathcal{A}^{pb}
       }{
         \underbrace{
           \mathbb{Z}
           \langle 
             \mathcal{D}^{pb}
           \rangle
           /(2T,4T)
         } 
       }
       ,
       \mathbb{Z}
     \big)
   $$

   on [[horizontal chord diagrams]] of $n$ strands (elements of the set $\mathcal{D}^{pb}$)

1. the [[integral cohomology]] of the [[based loop space]] of the [[ordered configuration space of n points]] in 3d [[Euclidean space]]:

$$
  H \mathbb{Z}^\bullet
  \big(
    \Omega 
    \underset{
      {}^{\{1,\cdots,n\}}
    }{Conf}
    (\mathbb{R}^3)
  \big)
  \;\simeq\;
  \mathcal{W}_{pb}^\bullet
  \;\simeq\;
  Gr^\bullet( \mathcal{V}_{pb} )
  \,.
$$

(the second equivalence on the right is the fact that [[weight systems are associated graded of Vassiliev invariants]]).

=--

This is stated as [Kohno 02, Theorem 4.1](#Kohno02)



### For weight systems (circular)

+-- {: .num_prop}
###### Proposition
**([[weight systems]] are inside [[real cohomology]] of [[based loop space]] of [[ordered configuration space of points]] in [[Euclidean space]])**

For [[ground field]] $k = \mathbb{R}$ the [[real numbers]], 
there is a canonical [[injection]] of the [[real vector space]] $\mathcal{W}$ of [[framed weight systems]] ([here](weight+system#eq:SpaceOfWeightSystemsAsLinearDual)) into the [[real cohomology]] of the [[based loop spaces]] of the ordered [[configuration spaces of points]] in 3-[[dimension|dimensional]] [[Euclidean space]]:

$$
  \mathcal{W}
  \;\overset{\;\;\;\;}{\hookrightarrow}\;
  H\mathbb{R}^\bullet
  \Big(
    \underset{n \in \mathbb{N}}{\sqcup}
    \Omega 
    \underset{{}^{\{1,\cdots,n\}}}{Conf}
    \big(
      \mathbb{R}^3 
    \big)
  \Big)
$$

=--

This is stated as [Kohno 02, Theorem 4.2](#Kohno02)

## Related theorems

* [[weight systems are associated graded of Vassiliev invariants]]

* [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]

## Related concepts

[[!include chord diagrams and weight systems -- table]]

## References

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori and [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))

* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* [[Fred Cohen]], [[Samuel Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))

[[!redirects horizontal weight systems are cohomology of loop space of configuration space]]
