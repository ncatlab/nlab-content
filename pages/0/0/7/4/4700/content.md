
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}



## Graph complex
 {#GraphComplex}

### Via grafting of graphs

Consider the [[complex vector space]] $\mathcal{G}$ [[linear span|spanned]] by the [[isomorphism classes]] of [[orientation|oriented]] [[ribbon graphs]] [[quotient|modulo]] the [[relation]] $(\Gamma,-\sigma) = - (\Gamma, \sigma)$ where $\sigma$ is an [[orientation]] on the [[graph]] $\Gamma$. 

A [[differential]] on this vector space is given by

$$
  \partial(\Gamma) 
    \coloneqq 
  \sum_{e\in E(\Gamma)\backslash Loop(\Gamma)} \Gamma/e
  \,,
$$

where the [[sum]] is over [[edges]] $e$ which are not [[loops]] (have distinct [[source]] and [[target]]) and $\Gamma/e$ is obtained from $\Gamma$ by contraction at edge $e$ (cf. [[ribbon graph]]). 

This function $\partial$ is indeed a differential, in that it satisfies $\partial^2 = 0$, because two contractions in different order produce a different orientation. 

The resulting [[chain complex]] $(\mathcal{G}_\bullet, \partial)$ is called the _graph complex_. Its [[chain homology]] $H_\bullet(\mathcal{G}, \partial)$ is called _graph homology_.

([Kontsevich 94, pages 11-12](#Kontsevich94))

### Via Poincaré duality pairing  
 {#ViaPoincareDualityPairing}

+-- {: .num_defn #GraphComplexOfCartesianSpace}
###### Definition
**(graph complex via Poincaré pairing)**

For $n, N, D \geq 1  \in \mathbb{N}$, let 

* $V$ be a [[finite-dimensional vector space|finite-dimensional]] [[real vector space|real]] [[graded vector space]] of [[dimension]] $N$;

* equipped with a non-degenerate [[inner product]]

  $$
    g \;\colon\; V \otimes V \longrightarrow \mathbb{R}
  $$

  of degree $-D$

* equipped with an "[[augmentation]]" [[linear map]]

  $$
    \epsilon \;\colon\; V \longrightarrow \mathbb{R}
  $$

  whose [[kernel]] is to be denoted

  $$
    \overline{V} \;\coloneqq\; ker(\epsilon)
    \,.
  $$

Choose a [[linear basis]]  $\{e_i\}_{i \in \{1, 2, \cdots, N\}}$ of $V$ such that $\{e_2, \cdots, e_N\}$ is a linear basis for $\overline{V}$. Write $\{g^{\alpha \beta}\}$ for the components of the inner product in this basis

$$
  g^{\alpha \beta} 
    \;\coloneqq\;
  g(e_\alpha, e_\beta)
  \,.
$$

On the [[graded-commutative algebra]] 

$$
  \mathbb{R}\left[
     \{e_i\},
     \{s^{i j}\}
  \right]
$$

[[generators and relations|generated]] by 

1. generators $e^i_\alpha$ for $\alpha \in \{1, \cdots N\}$, $i \in \{1, \cdots, N\}$ of degree that of the respective basis element $e_\alpha$ as above,

1. generators $s^{i j}$ for $1 \leq i, j \leq n$, of degree $D - 1$, subject to 

   $$
     s^{i j} \;=\; (-1)^D s^{j i}
   $$

define a [[differential]] (a graded [[derivation]] of degree 1 with $d \circ d = 0$)

$$
  d 
  \;\colon\;
  \mathbb{R}\left[
     \{e_i\},
     \{s^{i j}\}
  \right]
  \longrightarrow
  \mathbb{R}\left[
     \{e_i\},
     \{s^{i j}\}
  \right]
$$

by

$$
  \begin{aligned}
    d e^j_\alpha  
      & \coloneqq 0
    \\
    d s^{i j} 
      & \coloneqq 
      \underset{\alpha, \beta}{\sum} g^{\alpha \beta} e^i_\alpha e^j_\beta
  \end{aligned}
  \,.
$$

This defines a [[differential graded-commutative algebra]]. 
Its [[quotient]] algebra, 
which identifies the generators not in $\overline{V}$ with the [[unit]],

\[
  \label{GraphComplexOfPoincareDualityVectorSpace}
  {}^\ast Gra_{(V,g)}(n)
  \;\coloneqq\;
  \left( 
  \mathbb{R}\left[
     \{e_i\},
     \{s^{i j}\}
  \right]
  ,\, d
  \right)/( e^j_1 - 1 )
\]

is the _pre-graph complex_ of $(V, g)$. (This is independent, up to [[isomorphism]] of the choice of linear basis used in this presentation of the algebra.)

We may identify a homogeneous element 

$$
  e^1_\alpha e^1_\beta s^{1 2} e^2_{\gamma} \cdots e^n_\delta
  \;\in\;
  {}^\ast Gra_{(V,g)}
$$

with a [[graph]] with $n$ [[vertices]], whose 1st [[vertex]] carries the labels $\alpha$ and $\beta$, the second carries the label $\gamma$, etc. and with an [[edge]] for the $i$th vertex to the $j$th vertex for every factor $s^{i j}$.

In terms of this identification of homogeneous elements in ${}^\ast Gra_{(V,g)}(n)$ with graphs, the [[differential]] $d$ is the [[linear dual]] of a map $\Delta$ on the vector space spanned by graphs which acts by 

1. picking a [[pairs]] $(\omega,\nu)$ of labels of vertices,

1. removing these labels, replacing them with an edge between the corresponding vertices, and weihting the result by the pairing of the two labels

1. summing up the resulting over all choice of pairs.

<center>
<img src="https://ncatlab.org/nlab/files/GraphComplex1.jpg" width="400">   
</center>

Now for $X$ a [[closed manifold]] of [[dimension]] $D$, set

1. $V \coloneqq H^\bullet(X,\mathbb{R}) \simeq  H^\bullet_{dR}(X)$ its [[ordinary cohomology]] with [[coefficients]] in the [[real numbers]] (equivalently, by the [[de Rham theorem]], the [[de Rham cohomology]] of $X$);

1. $\epsilon \;\colon\; H^\bullet(X,\mathbb{R}) \longrightarrow H^0(X,\mathbb{R}) \simeq \mathbb{R}$ the [[projection]] onto the cohomology in degree 0 (the [[constant functions]] on $X$);

1. $g \coloneqq Poin \;\colon\; H^\bullet(X, \mathbb{R}) \otimes H^\bullet(X, \mathbb{R}) \longrightarrow \mathbb{R}$  the [[Poincaré duality]]-pairing.

Then the _graph complex of the closed manifold $X$_ is the graph complex (eq:GraphComplexOfPoincareDualityVectorSpace) of the cohomology of $X$ equipped with the [[Poincaré duality]]-pairing

$$
  {}^\ast Gra_X
  \;\coloneqq\;
  {}^\ast Gra_{(H^\bullet(X,\mathbb{R}), Poin)}
  \,.

$$

Next, define ${}^\ast TwGra_X$ roughly (...) as above, but with some of the vertices declared "internal" and made indistinguishable (no labels), and equipped with the above differential plus a differential which comes from a linear dual of the map that 

1. picks a vertex $v$

1. adds a new internal vertex and an edge from it to $v$

1. reconnects the original edges coincident to $v$ in all possible ways with either $v$ or the new internal vertex

1. sums over all ways of doing this.


<center>
<img src="https://ncatlab.org/nlab/files/GraphComplex2.jpg" width="280">   
</center>


Finally, the actual graph complex ${}^{\ast}Graph_X$ is the quotient of that which identifies all [[vacuum diagrams]] $\mathcal{G}$ (i.e. those with only internal vertices) with their with their partition function $Z_X(\mathcal{G})$:

$$
  {}^\ast Graphs_X 
  \;\coloneqq\;
  \mathbb{R} \otimes_{{}Z_X} {}^\ast TwGra_X
  \,.
$$


=--

This definition is due to [Campos-Willwacher 16, section 3](#CamposWillwacher16) using constructions from [Willwacher 10, appendix](#Willwacher10), following [Kontsevich 99b, around Def. 15 and Lemma 3](#Kontsevich99b).




## Properties

### General properties

There is a canonical [[graded object|bigrading]] on the graph complex, where $\mathcal{G}_{i j}$ is generated by those graphs which have $i$ [[vertices]] and $j$ [[edges]]; the differential has bidegree $(-1,-1)$; each $\mathcal{G}_{i j}$ is finite-dimensional, while the whole complex is infinite-dimensional. 

The graph complex splits into a [[direct sum]] of subcomplexes labelled by the  [[Euler characteristics]] of the underlying graph. 

The structure of a graph complex reflects a structure in the [[Chevalley-Eilenberg complex]] of a certain [[Lie algebra]]; and the graph homology to the relative Lie homology of that Lie algebra as shown by Kontsevich. 


### $L_\infty$-algebra structure

The Graph complex carries the structure of a [[dg-Lie algebra]] ([[L-infinity algebra]]) which acts on the space of choices of [[formal deformation quantization]] of [[Poisson manifolds]]. Its degree-0 [[chain homology]] is the [[Lie algebra]] of the [[Grothendieck-Teichmüller group]]. 

The homology in negative degree vanishes and that in positive degree is still unknown, but computer experiements show that at least the third cohomology contains nontrivial elements.

The degree-0 homology is also isomorphic, up to one "scaling class", to the 0th cohomology of the [[derivations]] of the [[Ek-operad|E2 operad]].

([Willwacher 10](#Willwacher10))

### Relation to Grothendieck-Teichm&#252;ller group and deformation quantization

See at _[deformation quantization -- Motivic Galois group action on the space of quantizations](deformation+quantization#MotivicGaloisGroup)_.

See at _[Grothendieck-Teichm&#252;ller group -- relation to the graph complex](Grothendieck-Teichm%C3%BCller+tower#RelationToTheGraphComplex)_.


### Relation to configuration spaces
 {#RelationToConfigurationSpaces}

The system of graph complexes is [[quasi-isomorphism|quasi-isomorphic]] to the [[ordinary cohomology|real cohomology]] of [[configuration spaces of points]] ([Campos-Willwacher 16, theorem 1](#CamposWillwacher16)).

## Examples 

* Graph complexes may be obtained from the [[Feynman transform]] of a [[modular operad]].


## Further applications

...moduli spaces

...deformation theory

...Rozansky-Witten theory

...Vassiliev invariants

...description of the classifying space $BOut(F_n)$ of the group of outer automorphisms of a free group with $n$ generators

Graph complex controls the universal $L_\infty$-deformations of the space of polyvector fields. 

## Generalizations

There are generalizations for $d$-algebras (algebras over little disc operad in higher dimension). The cohomological graph complex is then the case for $d=2$. There is also a "directed" version. On the other hand, graph complex 

## Related concepts

* [[Kontsevich formality]]

* [[Rozansky-Witten theory]]

* [[formal noncommutative symplectic geometry]] 

* [[Fulton-MacPherson operad]]


## References

Various versions of the definition of the graph complex were introduced in

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121, [pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf)

* {#Kontsevich99b} [[Maxim Kontsevich]], around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))


See also

* {#Kontsevich99a} [[Maxim Kontsevich]], _Rozansky&#8211;Witten invariants via formal geometry_, Compositio Mathematica __115__: 115&#8211;127, 1999, [doi](http://dx.doi.org/10.1023/A:1000619911308), [arXiv:dg-ga/9704009](http://arxiv.org/abs/dg-ga/9704009)


* {#MarklShniderStasheff02} [[Martin Markl]], [[Steve Shnider]], [[James Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.

* [[Andrey Lazarev]], _Operads and topological conformal field theories_, [pdf](http://www.maths.lancs.ac.uk/~lazarev/1-10.pdf); and older versio: _Graduate lectures on operads and topological field theories_, zip file with 11 pdfs, [over 5 Mb](http://www2.le.ac.uk/departments/mathematics/extranet/staff-material/staff-profiles/al179/New%20Folder.zip)

* [[Alastair Hamilton]], _A super-analogue of Kontsevich's theorem on graph homology_, Lett. Math. Phys. __76__ (2006), no. 1, 37--55, [math.QA/0510390](http://arxiv.org/abs/math/0510390)

* A. Lazarev, [[Alexander Voronov]], _Graph homology: Koszul and Verdier duality_ ([math.QA/0702313](http://arxiv.org/abs/math/0702313))

* [[Mikhail Movshev]], _A definition of graph homology and graph K-theory of algebras_ ([math.KT/9911111](http://arxiv.org/abs/math/9911111))

* [[Alberto S. Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Algebraic structures on graph cohomology_, Journal of Knot Theory and Its Ramifications, Vol. 14, No. 5 (2005) 627-640 ([doi:10.1142/S0218216505004019](http://dx.doi.org/10.1142/S0218216505004019), [math.GT/0307218](http://arxiv.org/abs/math/0307218), [MR2006g:58021](http://www.ams.org/mathscinet-getitem?mr=2006g:58021))

* [[Kiyoshi Igusa]], _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)

* {#Willwacher10} [[Thomas Willwacher]], _M. Kontsevich's graph complex and the Grothendieck-Teichmueller Lie algebra_ ([arxiv/1009.1654](http://arxiv.org/abs/1009.1654))


* [[Vasily Dolgushev]], [[Christopher Rogers]], [[Thomas Willwacher]], _Kontsevich's graph complex, GRT, and the deformation complex of the sheaf of polyvector fields_ ([arxiv/1211.4230](http://arxiv.org/abs/1211.4230))

* [[Damien Calaque]], Carlo A. Rossi, _Lectures on [[Duflo isomorphism]]s in Lie algebra and complex geometry_, European Math. Soc. 2011

* [[Sergei Merkulov]], _Graph complexes with loops and wheels_, in (Manin's Festschrift:) Algebra, Arithmetic, and Geometry, Progress in Mathematics __270__ (2009) 311-354, [doi](http://dx,doi.org/10.1007/978-0-8176-4747-6_10), [pdf](http://www2.math.su.se/~sm/Papers/graph_complexes.pdf)


* [[Martin Markl]], [[Sergei Merkulov]], S. Shadrin, _Wheeled PROPs, graph complexes and the master equation_, J. Pure Appl. Algebra, 213(4):496–535, 2009, [math.AT/0610683](https://arxiv.org/abs/math/0610683)

The following survey has discussion of context between the graph complex and [[Batalin-Vilkovisky formalism]]:

* Jian Qiu, Maxim Zabzine, _Introduction to graded geometry, Batalin-Vilkovisky formalism and their applications_, [arxiv/1105.2680](http://arxiv.org/abs/1105.2680) 
* Jian Qiu, Maxim Zabzine, _Knot weight systems from graded symplectic geometry_, [arxiv/1110.5234](http://arxiv.org/abs/1110.5234) 

* [[Alastair Hamilton]], [[Andrey Lazarev]], _Graph cohomology classes in the [[BV-BRST formalism|Batalin-Vilkovisky formalism]]_, J.Geom.Phys. __59__:555-575, 2009, [arxiv/0701825](http://arxiv.org/abs/math/0701825)

Relation to [[configuration space (mathematics)|configuration spaces]]:

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))



[[!redirects graph complexes]]

[[!redirects graph homology]]
[[!redirects graph homology group]]
[[!redirects graph homology groups]]

[[!redirects graph cohomology]]
[[!redirects graph cohomology group]]
[[!redirects graph cohomology groups]]
