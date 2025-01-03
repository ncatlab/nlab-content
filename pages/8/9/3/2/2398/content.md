
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

### On cohomology

The **de Rham theorem** (named after [[Georges de Rham]]) asserts that the [[de Rham cohomology]] $H^n_{dR}(X)$ of a smooth [[manifold]] $X$ (without boundary) is [[isomorphism|isomorphic]] to the [[real cohomology]] $H^n(X, \mathbb{R})$, hence its [[ordinary cohomology]] with [[real number]] [[coefficients]], as computed for instance by the [[singular cohomology|singular]] or [[Čech cohomology]] with real coefficients. 

The theorem has several dozens of different proofs. For example in the &#268;ech approach one can make a double complex whose first row is the &#268;ech complex of a covering and first column is the de Rham complex and other entries are mixed and use spectral sequence argument (cf. [Bott & Tu 1982](#BottTu82), [Postnikov 1989](#Postnikov89)). 
 
This is maybe best formulated, understood and proven in the context of [[abelian sheaf cohomology]]:

Write $\mathbb{R}_c$ for 

* the abelian group $\mathbb{R}$ 

* regarded not as a [[Lie group]] with the standard [[manifold]] structure on $\mathbb{R}$ but as a topologically discrete group on the underlying set of $\mathbb{R}$

* and then regarded as a [[sheaf]] on $X$: the [[constant sheaf]] that sends connected $U \subset X$ to the set of _constant_ maps $U \to \mathbb{R}$.

Write $\mathbf{B}^n \mathbb{R}_c$ for the corresponding [[Eilenberg-MacLane object]] in [[chain complex]]es of sheaves of abelian groups: this is the complex of sheaves with $\mathbb{R}_c$ in degree $n$:

$$
  \mathbf{B}^n \mathbb{R}_c
  = 
  (\cdots \to 0 \to \mathbb{R}_c \to 0 \to \cdots \to 0) 
  \,.
$$ 

Next, write $\bar \mathbf{B}^n \mathbb{R}$ (without the subscript $c$!) for the [[Deligne cohomology|Deligne complex]] for $\mathbb{R}$

$$
  \bar \mathbf{B}^n \mathbb{R}
  = 
  (C^\infty(-,\mathbb{R}) \stackrel{d_{dR}}{\to}
    \Omega^1(-) \stackrel{d_{dR}}{\to}
    \Omega^2(-) \stackrel{d_{dR}}{\to} \cdots \stackrel{d_{dR}}{\to} \Omega^n_{closed}(-)) 
  \,.
$$ 

(The notation here is borrowed from that used at [[motivation for sheaves, cohomology and higher stacks]]: we can think of $\bar \mathbf{B}^n \mathbb{R}$ as a differential refinement of the object $\mathbf{B}^n \mathbb{R}_c$).

Then we have:

* "ordinary" $\mathbb{R}$-valued cohomology of $X$ is the [[abelian sheaf cohomology]] with coefficients in $\mathbf{B}^n \mathbb{R}_c$.

* [[de Rham cohomology]] of $X$ is the [[abelian sheaf cohomology]] with coefficients in $\bar \mathbf{B}^n \mathbb{R}$ (this is semi-obvious, requires a bit more discussion).

* the [[Poincare lemma]] says that every closed [[differential form]] is locally exact, and hence there is a [[quasi-isomorphism]] of chain complexes of sheaves

  $$
    \mathbf{B}^n \mathbb{R}_c \stackrel{\simeq}{\to}
    \bar \mathbf{B}^n \mathbb{R}
  $$

  given by injecting for each $U \subset X$ the set $\mathbb{R}$ as the constant functions into $C^\infty(U,\mathbb{R})$.

It is this quasi-isomorphism of coefficient objects that induces the de Rham isomorphism of [[abelian sheaf cohomology|abelian sheaf]] [[cohomology group]]s, which is ordinarily written as

$$
  H^n(X,\mathbb{R}) \simeq 
  H^n_{dR}(X)
  \,.
$$

...

### On cochains
 {#OnCochains}

The equivalence on cohomology asserted by the de Rham theorem is but a [[decategorification]] of a more refined statement: a [[quasi-isomorphism]] of [[cochain complex]]es. This even respects the product structure:

for $X$ a [[smooth manifold]] there is an [[equivalence in an (infinity,1)-category|equivalence]] of [[A-infinity algebra]]s

$$
  (\Omega^\bullet(X), d_{dR})
  \stackrel{\simeq}{\to}
  (C(X), \cup)
$$

between the [[de Rham complex]] and the collection of [[singular cohomology|singular cochain]]s equipped with the [[cup product]].

This is due to ([Gugenheim, 1977](#Gugenheim)).

Furthermore, the [[E-infinity algebra]] structure on [[differential forms]]
(trivially induced by the [[commutative dga]] structure)
and [[singular cochains]] (as witnessed by the action of
the [[sequence operad]] of McClure and Smith on [[singular cochains]])
is also preserved.

### Synthetic version
 {#SyntheticVersion}

The de Rham theorem also holds internally in the context of suitable [[smooth topos]]es $\mathcal{T}$ modelling the axioms of [[synthetic differential geometry]].

Specifically 

* the internal [[singular cohomology|singular chain complex]] in $\mathcal{T}$ is given as the $R$-linear dual of the free internal $R$-module on the [[internal hom]] objects $[\Delta^n,X]$, where $R$ is the internal incarnation of the real numbers;

* the de Rham complex is given by [[differential forms in synthetic differential geometry]].

The de Rham theorem in $\mathcal{T}$ then asserts that for $X$ a manifold regarded as an object in the well-adapted smooth topos $\mathcal{T}$ the morphism

$$
  \textstyle{\int} \;\colon\; H^p(X) \to H_p(X,R)^*
$$

in $\mathcal{T}$ is an [[isomorphism]] for all $p \in \mathbb{N}$. This implies the standard (external) de Rham theorem.

This is discussed in chapter IV of

* [[Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ for the toposes $\mathcal{T} = \mathcal{G}, \mathcal{F}$ (see [models](http://ncatlab.org/nlab/show/Models+for+Smooth+Infinitesimal+Analysis#Models)).

Discussion for [[diffeological spaces]]:

* [[Patrick Iglesias-Zemmour]], _De Rham calculus_ ([pdf](http://math.huji.ac.il/~piz/documents/D6.pdf))

## Related concepts

* [[PL de Rham theorem]]

* [[equivariant de Rham theorem]]

* [[equivariant PL de Rham theorem]]

* [[Poincaré lemma]]

* [[Stokes theorem]]

* **de Rham theorem**

  * [[kernel of integration is the exact differential forms]]

* [[Dolbeault theorem]]

* [[Hodge theorem]]


## References

### On cohomology

Textbook accounts:

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Thm. 8.9 & Prop. 10.6 of: *[[Differential Forms in Algebraic Topology]]*, Springer (1982) &lbrack;[doi:10.1007/978-1-4757-3951-0](https://link.springer.com/book/10.1007/978-1-4757-3951-0)&rbrack;

* {#Postnikov89} [[M M Postnikov]], *Differentiable manifolds*, vol. III of: *Lectures on geometry* (1989) &lbrack;[ark:/13960/s2ccbwqpt99](https://archive.org/details/postnikov-lectures-in-geometry-semester-3-smooth-manifolds-mir-1989/page/7/mode/2up)&rbrack; 


* [[Jean Gallier]], [[Jocelyn Quaintance]], Ch. 9 in: *Homology, Cohomology, and Sheaf Cohomology for Algebraic Topology, Algebraic Geometry, and Differential Geometry*, World Scientific (2022) &lbrack;[doi:10.1142/12495](https://doi.org/10.1142/12495), [webpage](https://www.cis.upenn.edu/~jean/gbooks/sheaf-coho.html)&rbrack;

Exposition:

* Arne Lorenz, _Abstract de Rham theorem_, [pdf slides](http://wwwb.math.rwth-aachen.de/~arne/Talks/deRham.pdf) 

In the context of [[rational homotopy theory]]:

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Theorem 10.15 in: _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

In [[analytic geometry]]:

* M. E. Herrera, _De Rham theorems on semianalytic sets_, Bull. Amer. Math. Soc. __7__ 3 (1967) 414&#8211;418, [doi](http://dx.doi.org/10.1090/S0002-9904-1967-11772-5), [MR214094](http://www.ams.org/mathscinet-getitem?mr=214094)

In the generality of [[diffeological spaces]]:

* [[Patrick Iglesias-Zemmour]], *Une cohomologie de Čech pour les espaces differentiables et sa relation a la cohomologie de De Rham* (1988) &lbrack;[pdf](https://math.huji.ac.il/~piz/documents/UCDCPLEDESRALCDDR.pdf), [[IglesiasZemmour-CechDeRham.pdf:file]]&rbrack;

* [[Patrick Iglesias-Zemmour]], *Čech–De Rham bicomplex in diffeology*, Israel Journal of Mathematics (2023) 1–38 &lbrack;[doi:10.1007/s11856-023-2486-8](https://doi.org/10.1007/s11856-023-2486-8)&rbrack;

* [[Emilio Minichiello]], *The Diffeological Čech-de Rham Obstruction* &lbrack;[arXiv:2401.09400](https://arxiv.org/abs/2401.09400)&rbrack;


### On cocycles
 {#ReferencesdeRhamTheoremOnCocycles}

The refinement of the de Rham theorem from an [[isomorphism]] of [[cohomology group]]s to an [[equivalence]] of  [[A-∞ algebras]] of cochains and forms was first stated in 

* [[Victor Gugenheim]], _On Chen's iterated integrals_ , Illinois J. Math. Volume 21, Issue 3 (1977), 703-715.
 {#Gugenheim}

proven using Chen's [[iterated integral]]s.

A review is in section 3 of

* [[Camilo Arias Abad]], [[Florian Schätz]], _The $A_\infty$ de Rham theorem and integration of representations up to homotopy_ ([arXiv:1011.4693](http://arxiv.org/abs/1011.4693))


[[!redirects deRham theorem]]

[[!redirects de Rham isomorphism]]
[[!redirects de Rham isomorphisms]]

