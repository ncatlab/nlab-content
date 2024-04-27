
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


> In the wake of the movement of ideas which followed the [[general relativity|general theory of relativity]], I was led to introduce the notion of new geometries, more general than [[Riemannian geometry]], and playing with respect to the different [[Klein geometries]] the same role as the [[Riemannian geometries]] play with respect to [[Euclidean space]]. The vast synthesis that I realized in this way depends  of course on the ideas of [[Felix Klein|Klein]] formulated in his celebrated [[Erlangen program|Erlangen programme]] while at the same time going far beyond it since it includes [[Riemannian geometry]], which had formed a completely isolated branch of geometry, within the compass of a very general scheme in which the notion of [[group]] still plays a fundamental role. 

> &lbrack;[[Élie Cartan]] 1939, as quoted in [Sharpe 1997, p. 171](#Sharpe97)&rbrack;


## Idea

**Cartan geometry** is [[geometry]] of [[spaces]] that are locally (infinitesimally, tangentially) like [[coset spaces]] $G/H$, i.e. like [[Klein geometries]].  Intuitively, Cartan geometry studies the geometry of a [[manifold]] by 'rolling without sliding' the 'model geometry' $G/H$ along it. Hence Cartan geometry may be thought of as the globalization of the program of [[Klein geometry]] initiated in the [[Erlangen program]].


Cartan geometry subsumes many types of geometry, such as notably [[Riemannian geometry]], [[conformal geometry]], [[parabolic geometry]] and many more. As a Cartan geometry is defined by [[principal connection]] data (hence by [[cocycles]] in [[nonabelian cohomology|nonabelian]] [[differential cohomology]]) this means that it serves to express all these kinds of geometries in connection data. 

This is used notably in the [[first order formulation of gravity]], which was the motivating example in the original text ([Cartan 22](#Cartan23)). The [[physics]] literature tends to use the term "Cartan moving frame method" instead of "Cartan geometry".



## Definition

A _Cartan geometry_ is a space equipped with a _[[Cartan connection]]_. See there for more.

## Examples


\begin{example}\label{RiemannCartanGeometryOfS3}
**(Riemann-Cartan geometry of $S^3$)**
We discuss the [[Riemannian geometry]] of the [[round sphere|round]] [[3-sphere]] $S^3$ as a [[Cartan geometry]], hence via [[frame field]] and [[spin connection]] with vanishing [[torsion]] tensor. 

Among all spheres, this is particularly easy for the $S^3$, since its [[underlying]] [[smooth manifold]] [[diffeomorphism|is]] that of the [[Lie group]] [[SU(2)|$SU(2)$]]. This means that the [[frame field]]  can be chosen to be globally defined 

$$
  \big(
    e^i
  \big)_{i = 1}
  \,\in\,
  \Omega^1_{dR}\big(
    S^3
    ;\,
    \mathbb{R}^3
  \big)
$$

and to be given by [[left-invariant differential forms]] that satisfy the [[Maurer-Cartan equation]]

$$
  \mathrm{d}
  e^i
  \;=\;
  \epsilon^{i j k }
  \,
  e_j \, e_k
  \,,
$$

where $\epsilon^{i j k}$ is the [[Levi-Civita symbol]] in 3 dimensions, and we use the [[Einstein summation convention]] throughout.

In next defining the "[[spin connection]]" form

$$
  \big(
    \omega^{i j}
    =
    - \omega^{j i}
  \big)_{i,j = 1}^3
  \,\in\,  
  \Omega^1_{dR}\big(S^3;\, \mathfrak{so}(3)\big)
$$

we shall use the convention where the [[torsion]]-[[tensor]] $\big(T^i\big)_{i = 1}^3$ and [[curvature]]-[[tensor]] $\big(R^{i j}\big)_{i,j=1}^3$ are formed with a relative minus sign as

\begin{equation}
  \label{TorsionAndCurvatureInCartanGeometryOfS3}
  \begin{aligned}
    T^i & 
      \coloneqq\; 
        \mathrm{d} \, e^i - \omega^{i j} \, e_j
    \,,
    \\
    R^{i j} & 
      \coloneqq\; 
        \mathrm{d}\, \omega^{i j} 
          - \omega^{i k}\, \omega_k{}^j
    \,.
  \end{aligned}
\end{equation}

This implies that the unique [[torsion]]-free [[spin connection]] is given by

$$
  \omega^{i j}
  \;\equiv\;
  -
  \epsilon^{i j k} 
  e_k
  \,,
$$

since, by the above:

$$
  \begin{array}{l}
    \mathrm{d}
    e^i
    -
    \omega^{i j} e_j
    \\
    \;=\;
    \epsilon^{i j k }
    e_j e_k
    +
    \epsilon^{i j k} 
    e_k\, e_j
    \\
    \;=\;
    0
    \,.
  \end{array}
$$

To find the [[curvature]] of this connection we compute

$$
  \begin{array}{l}
    \mathrm{d} 
    \omega^{i j}
    \\
    \;=\;
    -
    \epsilon^{i j k}
    \epsilon_{k l m} e^l \, e^m
    \\
    \;=\;
    -2 \delta^{ i j }_{l m}
    e^{l}\, e^m
    \\
    \;=\;
    -2 e^{i}\, e^{j}
    \,,
  \end{array}
$$

where we take the multi-[[Kronecker symbol]] is normalized as

$$
  \delta^{i j}_{k l}
  \;\coloneqq\;
  \delta^{[i j]}_{[k l]}
  \;=\;
  \delta^{[i j]}_{k l}
  \;=\;
  \tfrac{1}{2}
  \Big(
    \delta^i_k\, \delta^j_l
    -
    \delta^j_k\, \delta^i_l
  \Big)
  \,,
$$

and

$$
  \begin{array}{l}
    \omega^{i k} \, \omega_{k}{}^j
    \\
    \;=\;
    \epsilon^{i k l}
    \epsilon_{k j m}
    e_l
    \, e^m
    \\
    \;=\;
    -2\delta^{i l}_{j m}
    e_l \, e^m
    \\
    \;=\;
    -
    e^i \, e^j
  \end{array}
$$

to obtain:

$$
  \begin{array}{l}
    R^{i j}
    \\
    \;=\;
    \mathrm{d}\omega^{i j} - \omega^{i k}\, \omega_k{}^j
    \\
    \;=\;
    -2 e^{i}\, e^{j}
    +
    e^i \, e^j
    \\
    \;=\;
    - e^{i}\, e^{j}
    \,,
  \end{array}
$$

hence

$$
  R^{i j}{}_{k l}
  \;=\;
  - \delta^{i j}_{k l}
  \,.
$$

Notice that, therefore, with the conventions (eq:TorsionAndCurvatureInCartanGeometryOfS3) the [[scalar curvature]] $\mathrm{R}$ of the $S^3$ comes out with a *negative* sign, since the [[Ricci tensor]] of $S^3$ is
$$
  Ric_{i j}
  \;\equiv\;
  R^{i k}{}_{j k}
  \;=\;
  - \delta_{i j}
$$
so that
$$
  \mathrm{R}
  \;\equiv\;
  Ric^i{}_i
  \;=\;
  - 3
  \,.
$$

This may seem undesirable, but it is a common choice in practice (cf. e.g. [Freund & Rubin 1980, below (4b)](Freund-Rubin+compactification#FreundRubin80)).
\end{example}


\linebreak


[[!include local and global geometry - table]]


## Related entries

* [[super-Cartan geometry]]

* [[Cartan geometry, Supergravity and Branes]]

* [[G-structure]], [[homothety]]

* [[first-order formulation of gravity]]

* [[torsion constraints in supergravity]]

* [[parabolic geometry]]

* [[tractor bundle]]

* [[higher Cartan geometry]]


## References

The original articles:

* {#Cartan22} [[Élie Cartan]], *Sur une généralisation de la notion de courbure de Riemann et les espaces á torsion*, C. R. Acad. Sci. **174** (1922) 593-595 .

* [[Élie Cartan]], Comptes rendus hebdomadaires des s&#233;ances de l&#8217;Acad&#233;mie des sciences, 174, 437-439, 593-595, 734-737, 857-860, 1104-1107 (January 1922).

* {#Cartan23} [[Élie Cartan]], *Sur les variétés à connexion affine et la théorie de la relativité généralisée (première partie)*, Annales scientifiques de l’École Normale Supérieure, Sér. 3, **40** (1923) 325-412 \[<a href="http://www.numdam.org/item?id=ASENS_1923_3_40__325_0">doi:ASENS_1923_3_40__325_0</a>\]

Historical review:

* [[Erhard Scholz]], *E. Cartan’s attempt at bridge-building between Einstein and the Cosserats – or how translational curvature became to be known as "torsion"*, The European Physics Journal H **44** (2019) 47-75 \[<a href="https://doi.org/10.1140/epjh/e2018-90059-x">doi:10.1140/epjh/e2018-90059-x</a>\]


Introductions:

* [[Richard W. Sharpe]], *An introduction to Cartan Geometries*, Proceedings of the 21st Winter School "Geometry and Physics", Circolo Matematico di Palermo (2002) 61-75 &lbrack;[eudml:220395](https://eudml.org/doc/220395), [dml:701688](http://dml.cz/dmlcz/701688)&rbrack;

* [[Benjamin McKay]], *An introduction to Cartan geometries*, Proceedings of the 21st Winter School "Geometry and Physics", Palermo (2002) &lbrack;[arXiv:2302.14457](https://arxiv.org/abs/2302.14457), [eudml:220395](https://eudml.org/doc/220395)&rbrack;


Monographs:

* {#Sharpe97} [[Richard W. Sharpe]], *Differential geometry -- Cartan's generalization of Klein's Erlagen program*, Graduate Texts in Mathematics **166**, Springer (1997) &lbrack;[ISBN:9780387947327](https://link.springer.com/book/9780387947327)&rbrack;

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], Chapter I.3.7 in: *[[Supergravity and Superstrings - A Geometric Perspective]]*, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), toc: [[CDF91-TOC.pdf:file]], ch I.3: [[CastellaniDAuriaFre-ChI3.pdf:file]]&rbrack;

  > (these authors refer to Cartan geometries as "soft group manifolds")

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]], chapter 1 of: _Parabolic Geometries I -- Background and General Theory_, AMS (2009) &lbrack;[ISBN:978-1-4704-1381-1](http://bookstore.ams.org/surv-154)&rbrack;

* [ps](http://www.math.muni.cz/~slovak/Vyuka/gs2.ps)

For more see at _[Cartan connection -- References](Cartan+connection#References)_.

Discussion in [[modal homotopy type theory]] is in

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017

* {#Wellen18} [[Felix Wellen]], _Cartan Geometry in Modal Homotopy Type Theory_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))


See also

* wikipedia: [Cartan connection](http://en.wikipedia.org/wiki/Cartan_connection)

* The blog [discussion](http://golem.ph.utexas.edu/category/2007/07/derek_wise_on_cartan_geometry.html) of [[Derek Wise]], [MacDowell-Mansouri gravity and Cartan geometry](http://arxiv.org/abs/gr-qc/0611154).

[[!redirects Cartan geometries]]