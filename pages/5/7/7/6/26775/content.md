
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



\tableofcontents


## Idea

For a [[pair]] of [[coprime]] [[natural numbers]] $n_+, n_- \in \mathbb{N}_{\geq 1}$, $qcd(n_+, n_-) = 1$, the *$(n_+, n_-)$-spindle* is the 2-[[dimension of a manifold|dimensional]] [[orbifold]] whose [[underlying]] coarse [[topological space]] is the [[2-sphere]]/[[Riemann sphere]] $\mathbb{C}P^1$, but where the [[poles]] $0, \infty \in \mathbb{C}P^1$ are [[cone]] tips of order $n_+, n_-$, respectively.

This is also sometimes called the *$(n_+,n_-)$-football* and is denoted "$S^2(n_+, n_-)$" or "$\Sigma(n_+, n_-)$" or sometimes just "$(n_+, n_-)$". It is the orbifold incarnation of the *weighted projective space* $\mathbb{C}P(n_+, n_-)$.

If either $n_\pm = 1$ but $n_{\mp} \gt 1$ then the spindle orbifold reduces to the orbifold known as the *teardrop*. 

If both $n_+ = n_- = 1$ then the spindle orbifold reduces is a [[smooth manifold]]: the ordinary ([[Riemann sphere|Riemann]]) [[2-sphere]] $S^2$.



## Definition
 {#Definition}

### Via orbifold charts

(...)

### As a proper étale Lie groupoid
 {#DefinitionAsProperEtaleLieGroupoid}

We describe the spindle orbifold [as a proper étale Lie groupoid](orbifold#DefinitionViaProperEtaleGroupoids) (the following  description is far from unique, as far as [[Morita equivalence|Morita equivalent]] [[proper topological groupoid|proper]] [[étale Lie groupoids]] go, but it is about the simplest evident realization):

1. the [[smooth manifold]] of [[objects]] is the [[disjoint union]] of two copies of the [[plane]] $\mathbb{R}^2$ --- which for notational purposes, at least, will be useful to think of as the *[[complex line]]* $\mathbb{C}$:
  \[
    \label{ObjectSpaceForSpindleGroupoid}
    Obj\big(\mathbb{C}P(n_+, n_-)\big) 
      \;\coloneqq\; 
    \mathbb{C}_+
      \;\sqcup\;
    \mathbb{C}_-
    \mathrlap{\,,}
  \]

2. the [[smooth manifold]] of [[morphisms]] is the [[disjoint union]] of 

   1. (these) two copies of $\mathbb{C}$ [[product manifold|times]] the [[underlying set]] of the [[cyclic group]] $C_{n_{\pm}}$ of [[order of a group|order]] $n_\pm$, respectively,

   1. two copies of its [[puncture|punctured]] version $\mathbb{C}^\times \coloneqq \mathbb{C} \setminus \{0\}$ (its [[complement]] of the origin), [[product manifold|times]] the [[underlying set]] of the [[direct product group|product]] [[cyclic group]] $C_{n_{+}} \times C_{n_-}$:

  \[
    \label{MorphismSpaceForSpindleGroupoid}
    Mor\big(\mathbb{C}P(n_+, n_-)\big) 
      \;\coloneqq\; 
    \Big(
      (\mathbb{C}_+ \times C_{n_+})
        \;\sqcup\; 
      (\mathbb{C}_- \times C_{n_-})
   \Big)
      \;\sqcup\; 
    \Big(
      (\mathbb{C}_{+-}^\times \times C_{n_+} \times C_{n_-})
        \;\sqcup\; 
      (\mathbb{C}_{-+}^\times \times C_{n_-} \times C_{n_+})
    \Big)
    \mathrlap{\,,}
  \]

where the subscripts on the copies of [[complex line|$\mathbb{C}$]] only serve to [[indexed set|index]] the [[direct sum|direct summands]]. 

Here the first pair of direct summands may be referred to as the "internal" morphisms (as they will operate within either chart, implementing here the actual orbi-singularities), and the second pair of summands as the "external" or "gluing" morphisms (as they operate between charts, implementing nothing but their gluing).

Concretely, with the abbreviation

$$
  q_{\pm}
  \coloneqq
  e^{2 \pi \mathrm{i}/n_{\pm}}
  \,,
$$

the [[source]] and [[target]] [[smooth function|maps]] for the internal morphisms and for the weightless gluing morphisms are:

$$
  \begin{array}{ccc}
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    &\overset{(s,t)}{\longrightarrow}&
    Obj\big(\mathbb{C}P(n_+, n_-)\big)^2
    \\
    \big(
      (z,\pm), [k_\pm]
    \big)
      &\mapsto&
    \big(
      (z, \pm)
      ,
      (z q_{\pm}^{k_{\pm}}, \pm)
    \big)
    \\
    \\
    \big(
      (v,\pm \mp), [0], [0]
    \big)
      &\mapsto&
    \Big(
      \big( 
        v^{n_\pm}, \pm
      \big)
      ,
      \big(
        v^{-n_\mp}, \mp
      \big)
    \Big)
    \mathrlap{\,}
  \end{array}
$$

and the [[composition]] map for the "internal" morphisms is that of the [[action groupoid]] $\mathbb{C}_{\pm} \sslash C_{\pm}$:

$$
  \begin{array}{ccc}
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    {}_s \times_t
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    &\overset{(-)\circ (-)}{\longrightarrow}&
    Mor\big(\mathbb{C}P(n_+, n_-)\big)
    \\
    \Big(
     \big(
       (z q_{\pm}^{k_{\pm}} ,\pm),[k'_\pm]
     \big)
     , 
     \big(
       (z,\pm),[k_\pm]
     \big)
    \Big)
     &\mapsto&
    \big(
      (z,\pm), [k'_\pm + k_\pm]
    \big) 
    \,.
  \end{array}
$$

Finally, the general gluing morphism is the unique composite

$$
  \big(
    (v,\pm\mp), [k_\pm], [k_\mp]
  \big)
  \;\equiv\;
  \big(
    (v^{-n_\mp},\mp), [k_\mp])
  \big)
  \circ
  \big(
    (v,\pm,\mp), [0], [0]
  \big)
  \circ 
  \big(
    (v^{n_\pm} \cdot q^{-k_{\pm}}, \pm), [k_\pm]
  \big)
  \,,
$$

which defines either side by the other (meaning that the gluing morphisms are a [[groupoid torsor]] from either side over these [[action groupoids]]). Its [[source]] and [[target]] maps are

$$
  (s,t)
  \;\colon\;
  \big(
    (v,\pm\mp), [k_\pm], [k_\mp]
  \big)
  \mapsto
  \big(
    (v^{-n_{\mp}} \cdot q^{+ k_{\mp}}, \pm)
    ,
    (v^{n_{\pm}} \cdot q^{- k_{\pm}}, \mp)
  \big)
  \mathrlap{\,.}
$$


## Related entries

* [[pillowcase orbifold]]

* [[teardrop orbifold]]

* [[branched cover of the Riemann sphere]]

## Literature

### General

* {#Amenta12} Alexander Amenta, Ex. 1.2.2 in: _The Geometry of Orbifolds via Lie Groupoids_, ANU (2012) &lbrack;[arXiv:1309.6367](https://arxiv.org/abs/1309.6367)&rbrack;


* Vesta Coufal, [[Dorette Pronk]], [[Carmen Rovi]], [[Laura Scull]], Courtney Thatcher, Ex. 2.6 in: _Orbispaces and their Mapping Spaces via Groupoids: A Categorical Approach_, in: *Women in Topology: Collaborations in Homotopy Theory*, Contemporary Mathematics **641** (2015) 135-166 &lbrack;[arXiv:1401.4772](https://arxiv.org/abs/1401.4772), [doi:10.1090/conm/641](https://doi.org/10.1090/conm/641)&rbrack;



* Francisco C. Caramello Jr, Ex. 1.3.1 in: *Introduction to orbifolds* &lbrack;[arXiv:1909.08699](https://arxiv.org/abs/1909.08699)&rbrack;




### In string theory

On [[supergravity]] [[KK-compactification|KK-compactified]] (and [[branes]] [[wrapped brane|wrapped]]) on [[spindle orbifolds]]:

* [[Pietro Ferrero]], [[Jerome P. Gauntlett]], Juan Manuel Pérez Ipiña, [[Dario Martelli]], [[James Sparks]], *D3-branes wrapped on a spindle*, Phys. Rev. Lett. **126** 111601 (2021) &lbrack;[arXiv:2204.02990](https://arxiv.org/abs/2204.02990), [doi:10.1103/PhysRevLett.126.111601](https://doi.org/10.1103/PhysRevLett.126.111601)&rbrack;

* [[Pietro Ferrero]], [[Jerome P. Gauntlett]], [[Dario Martelli]], [[James Sparks]], *M5-branes wrapped on a spindle*, J. High Energ. Phys. **2021** 2 (2021)
 &lbrack;[arXiv:2105.13344](https://arxiv.org/abs/2105.13344), <a href="https://doi.org/10.1007/JHEP11(2021)002">doi:10.1007/JHEP11(2021)002</a>&rbrack;
&rbrack;


* Federico Faedo, [[Dario Martelli]], *D4-branes wrapped on a spindle*, J. High Energ. Phys. **2022** 101 (2022) &lbrack;[arXiv:2111.13660](https://arxiv.org/abs/2111.13660), <a href="https://doi.org/10.1007/JHEP02(2022)101">doi:10.1007/JHEP02(2022)10</a>&rbrack;


* Christopher Couzens, *A tale of (M)2 twists*, J. High Energ. Phys. **2022** 78 (2022) &lbrack;[arXiv:2112.04462](https://arxiv.org/abs/2112.04462), <a href="https://doi.org/10.1007/JHEP03(2022)078">doi:10.1007/JHEP03(2022)078</a>&rbrack;

* K. C. Matthew Cheung, Jacob H. T. Fry, [[Jerome P. Gauntlett]], [[James Sparks]], *M5-branes wrapped on four-dimensional orbifolds*, J. High Energ. Phys. **2022** 82 (2022) &lbrack;[arXiv:2204.02990](https://arxiv.org/abs/2204.02990), <a href="https://doi.org/10.1007/JHEP08(2022)082">doi:10.1007/JHEP08(2022)082</a>&rbrack;

[[!redirects spindle orbifolds]]


[[!redirects spindle]]
[[!redirects spindles]]

[[!redirects teardrop orbifold]]
[[!redirects teardrop orbifolds]]


[[!redirects teardrop]]
[[!redirects teardrops]]

