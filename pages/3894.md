
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A **G-structure** on an $n$-[[manifold]] $M$, for a given structure group $G$, is a $G$-subbundle of the [[frame bundle]] (of the [[tangent bundle]]) of $M$. 

Equivalently, this means that a $G$-structure is a choice of [[reduction of structure groups|reduction]] of the canonical structure group [[general linear group|GL(n)]] of the [[principal bundle]] to which the [[tangent bundle]] is [[associated bundle|associated]] along the given inclusion $G \hookrightarrow GL(n)$.

More generally, one can consider the case $G$ is not a [[subgroup]] but equipped with any group homomorphism $G \to GL(n)$. If this is instead an [[epimorphism]] one speaks of a [[lift of structure groups]].

Both cases, in turn, can naturally be understood as special cases of [[twisted differential c-structures]], which is a notion that applies more generally to [[principal infinity-bundles]].

In this language, a $G$-structure is a lift _in [[classifying stacks]]_ ([[differentiable stack|differentiable]] [[delooping]] [[stacks]] $\mathbf{B}G$ of [[Lie groups]] $G$) of the classifying map of the [[tangent bundle]]

$$
  \array{
    && \mathbf{B}G
    \\
    &  
    {}^{ \mathllap{G structure} }\nearrow
    & \big\downarrow^{ str }
    \\
    X 
      &\underset{
        \vdash T X
      }{\longrightarrow}&
    \mathbf{B} GL(n)
  }
$$

Beware the distinction to _[[tangential structure]]_ on $X$, where such as lift is considered (only) at the level of underlying [[classifying spaces]].


## Definition

### General

Given a [[smooth manifold]] $X$ of [[dimension]] $n$ and given a [[Lie group|Lie]] [[subgroup]] $G \hookrightarrow GL(n)$ of the [[general linear group]], then a _$G$-structure_ on $X$ is a [[reduction of structure groups|reduction of the structure group]] of the [[frame bundle]] of $X$ to $G$.

There are many more explicit (and more abstract) equivalent ways to say this, which we discuss below. There are also many evident variants and generalizations. 

Notably one may consider reductions of the frames in the $k$th order [[jet bundle]]. (e. g. [Alekseevskii](#Alekseevskii)) This yields order $k$ $G$-structure and the ordinary $G$-structures above are then first order.

Moreover, the definition makes sense for generalized [[manifolds]] modeled on other base spaces than just [[Cartesian spaces]]. In particular there are evident generalizations to [[supermanifolds]] and to [[complex manifolds]].




### In terms of subbundles of the frame bundle
 {#InTermsOfSubbundlesOfTheFrameBundle}

+-- {: .num_defn}
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$ with [[frame bundle]] $Fr(X)$, and given a [[Lie group]] [[monomorphism]]

$$
  G \longrightarrow GL(\mathbb{R}^n)
$$

into the [[general linear group]], then a _$G$-structure_ on $X$ is an $G$-[[principal bundle]] $P \to X$ equipped with an inclusion of [[fiber bundles]]

$$
  \array{
    P &&\hookrightarrow&& Fr(X)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
$$

which is $G$-equivariant. 

=--

([Sternberg 64, section VII, def. 2.1](#Sternberg64)).


+-- {: .num_remark}
###### Remark

From this perspective, a $G$-structure consists of the collection of all $G$-[[frame field|frames]] on a manifold. For instance for an [[orthogonal structure]] it consists of all those frames which are pointwise an [[orthonormal basis]] of the [[tangent bundle]] (with respect to the [[Riemannian metric]] which is defined by the orthonormal structure).

=--

Accordingly: 

+-- {: .num_defn #GStructureGeneratedByFrameField}
###### Definition

Given $G \hookrightarrow GL(n)$ and given any one [[frame field]] $\sigma \colon X \to Fr(X)$ over a [[manifold]] $X$, then acting with $G$ on $\sigma$ at each point produces a $G$-subbundle. This is called the $G$-structure _generated_ by the frame field $\sigma$.

=-- 



### In terms of Cartan connections

A $G$-structure equipped with compatible [[connection on a bundle|connection]] data is equivalently a [[Cartan connection]] for the inclusion $(G \hookrightarrow \mathbb{R}^n \rtimes G)$. 

See at _[Cartan connection -- Examples -- G-structures](Cartan+connection#ExampleGStructures)_

### In higher differential geometry

#### $G$-structure on a $K$-principal bundle

We give an equivalent definition of $G$-structures in terms of [[higher differential geometry]] ("from the [[nPOV]]"). This serves to clarify the slightly subtle but important difference between existence and choice of $G$-structure, and seamlessly embeds the notion into the more general context of [[twisted differential c-structures]].

+-- {: .num_defn}
###### Definition

Let $G \to K$ be a [[homomorphism]] of [[Lie groups]]. Write 

$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}K
$$

for the morphism of [[delooping]] [[Lie groupoids]] ( the [[smooth infinity-groupoid|smooth]] [[moduli stacks]] of smooth $K$- and $G$-[[principal bundles]], respectively).

For $X$ a [[smooth manifold]] (or generally an [[orbifold]] or [[Lie groupoid]], etc.) Let $P \to X$ be a $K$-[[principal bundle]] and let 

$$
  k \colon X \longrightarrow \mathbf{B}K
$$ 

be any choice of morphism [[modulating morphism|modulating]] it.

Write $\mathbf{H}(X, \mathbf{B}G)$ etc. for the [[derived hom space|hom-groupoid]] of [[smooth infinity-groupoid|smooth groupoids]] / smooth stacks . This is equivalently the groupoid of $G$-principal bundles over $X$ and smooth [[gauge transformations]] between them.

Then the **groupoid of $G$-structure on $P$** (with respect to the given morphism $G \to K$) is the [[homotopy pullback]]

$$
  \mathbf{c}Struc_{[P]}(X)
  :=
  \mathbf{H}(X, \mathbf{B}G)
   \times_{\mathbf{H}(X, \mathbf{B}K)}
  \{k\}
  \,.
$$

$$
  \array{
    \mathbf{c}Struc_{[P]}(X)
    &\longrightarrow&
    \ast
    \\
    \downarrow & \swArrow_\simeq& \downarrow^{\mathrlap{k}}
    \\
    \mathbf{H}(X, \mathbf{B}G)
     &\stackrel{\mathbf{H}(X, \mathbf{c})}{\longrightarrow}&
    \mathbf{H}(X, \mathbf{B}K)
  }
$$

(the groupoid of _[[twisted differential c-structure|twisted c-structures]]_).


=--

+-- {: .num_remark}
###### Remark

If here $k$ is trivial in that it factors through the point, $k \colon X \to \ast \to \mathbf{B}K$ then this homotopy fiber product is $\mathbf{H}(X,K/G)$, where $K/G$ is the [[coset space]] ([[Klein geometry]]) which itself sits in the [[homotopy fiber sequence]]

$$
   K/G \to \mathbf{B}G \to \mathbf{B}K
  \,.
$$

=--

+-- {: .num_example}
###### Example

Specifically, when $X$ is a [[smooth manifold]] of [[dimension]] $n$, the [[frame bundle]] $Fr(X)$ is [[modulating moprhism|modulated]] by a morphism $\tau_X \colon X \to \mathbf{B} GL(n)$ into the [[moduli stack]] for the [[general linear group]] $K := GL(n)$. Then for any group homomorphism $G \to GL(n)$, a **$G$-structure** on $X$ is a $G$-structure on $Fr(X)$, as above.

=--

#### $G$-Structure on an etale $\infty$-groupoid

We discuss the concept in the generality of [[higher differential geometry]], formalized in [[differential cohesion]].

See at _[differential cohesion -- G-Structure](differential+cohesive+%28infinity%2C1%29-topos#structures)_



## Properties

### Integrability of $G$-structure

+-- {: .num_defn #Integrability}
###### Definition

A $G$-structure on a [[manifold]] $X$ is called _locally flat_ ([Sternberg 64, section VII, def. 24](#Sternberg64)) or _integrable_ (e.g. [Alekseevskii](#Alekseevskii)) if it is locally equivalent to the _standard flat $G$-structure_, def. \ref{StandardFlatGStructure}. 

This means that there is an [[open cover]] $\{U_i \to X\}$ by [[open subsets]] of the [[Cartesian space]] $\mathbb{R}^n$ such that the restriction of the $G$-structure to each of these is equivalent to the standard flat $G$-structure.

=--


See at _[[integrability of G-structures]]_ for more on this

The [[obstruction]] to integrability of $G$-structure is the _[[torsion of a G-structure]]_. See there for more.


### Relation to special holonomy

The existence of $G$-structures on tangent bundles of [[Riemannian manifolds]] is closely related to these having [[special holonomy]].

+-- {: .num_theorem}
###### Theorem

Let $(X,g)$ be a [[connected topological space|connected]] [[Riemannian manifold]]
of [[dimension]] $n$ with [[holonomy group]]  $Hol(g) \subset O(n)$.

For $G \subset O(n)$ some other [[subgroup]], $(X,g)$ admits a torsion-free 
G-structure precisely if $Hol(g)$ is [[adjoint action|conjugate]] to 
a [[subgroup]] of $G$.

Moreover, the space of such $G$-structures is the [[coset]] $G/L$,
where $L$ is the group of elements suchthat conjugating $Hol(g)$ with them
lands in $G$.

=--

This appears as ([Joyce prop. 3.1.8](#Joyce))


## Examples

### Canonical G-structures

+-- {: .num_defn #StandardFlatGStructure}
###### Definition

For $G \hookrightarrow GL(n)$ a subgroup, the _standard flat $G$-structure_ on the [[Cartesian space]] $\mathbb{R}^n$ is the $G$-structure which is generated, via def. \ref{GStructureGeneratedByFrameField}, from the canonical [[frame field]] on $\mathbb{R}^n$ (the one which is the identity at each point, under the defining identifications).

=--

\begin{example}
  \label{CanonicalHStructureOnFModH}
  For $H \subset G$ any [[Lie group|Lie]] [[subgroup]]-inclusion, the canonical [[quotient space]] [[coprojection]] $G \to G/H$ to the [[coset space]] is an $H$-[[principal bundle]] that exhibits $H$-structure on $G/H$.
\end{example}
 
(e.g. [Čap-Slovak 09, p. 53](#CapSlovak09))






### Reduction of tangent bundle structure

* For the [[subgroup]] of $GL(n, \mathbb{R})$ of matrices of positive determinant, a $GL(n, \mathbb{R})^+$-structure defines an [[orientation]].

* For the [[orthogonal group]], an $O(n)$-structure defines a [[Riemannian metric]]. (See the discussion at [[vielbein]] and at

* For the [[special linear group]], an $SL(n,R)$-structure defines a [[volume form]]. 

* For the trivial group, an $\{e\}$-structure consists of an [[absolute parallelism]] of the manifold.

* For $n = 2 m$ even, a $GL(m, \mathbb{C})$-structure defines an [[almost complex structure]] on the manifold. It must satisfy an integrability condition to be a [[complex structure]].

### Lift of tangent bundle structure

An example for a lift of structure groups is

* for the [[spin group]]  $spin(n)$, a $G$-structure is a [[spin structure]].

This continues with lifts to the 

* [[string group]] giving [[string structure]];

* [[fivebrane group]] giving [[fivebrane structure]].

### Reduction of more general bundle structure
 {#ExamplesOfReductionsOfNonTangentBundles}

* For general $G \to K$, the corresponding notion of [[Cartan geometry]] involves $G$-structure on $K$-principal bundles (not necessarily underlying a tangent bundle).

* A $U(n,n) \hookrightarrow O(2n,2n)$-structure is a [[generalized complex structure]];

* For $H_n \to E_{n(n)}$ the inclusion of the [[maximal compact subgroup]] into the [[split real form]] of an [[exceptional Lie group]], the corresponding structure is an [[exceptional generalized geometry]].

### Complex geometric examples

* The choice of $SO(n, \mathbb{C})$ as subgroup of $GL(n, \mathbb{C})$, determines a complex Riemannian structure;

* $CO(n, \mathbb{C}) \hookrightarrow GL(n, \mathbb{C})$, a complex conformal structure;

* $Sp(2n, \mathbb{C})\hookrightarrow GL(2n, \mathbb{C})$, an almost symplectic structure;

* $GL(2, \mathbb{C}) GL(n, \mathbb{C}) \hookrightarrow GL(2n, \mathbb{C}), n \geq 3$,  determines an almost quaternionic structure;

* more generally a $GL(m, \mathbb{C}) GL(n, \mathbb{C})$-structure on a $m n$-dimensional manifold is locally identical to a Grassmannian spinor structure.

### Special holonomy examples

[[!include normed division algebra Riemannian geometry -- table]]

### $G$-Structures on 8-manifolds

For discussion of [[G-structures]] on [[closed manifold|closed]] [[8-manifolds]] see [there](8-manifold#GStructuresOn8Manifolds).

### Higher geometric examples

See the list at [[twisted differential c-structure]].

\linebreak

## Related concepts

* [[special holonomy]]

* [[integrability of G-structures]]

* [[homothety]]


## References

### Traditional
 
The concept originates around the work of [[Eli Cartan]] ([[Cartan geometry]]) and

* [[Shiing-Shen Chern]], _The geometry of G-structures_, Bull. Amer. Math. Soc. 72(2): 167&#8211;219. 1966 ([pdf](http://www.ams.org/journals/bull/1966-72-02/S0002-9904-1966-11473-8/S0002-9904-1966-11473-8.pdf), [Euclid](http://projecteuclid.org/euclid.bams/1183527777))

Textbook accounts:

* {#Sternberg64} [[Shlomo Sternberg]], chapter VII of: _Lectures on differential geometry_, Prentice-Hall 1964, 

  2nd edition AMS 1983 ([ISBN:978-0-8218-1385-0](https://bookstore.ams.org/chel-316))

* [[Shoshichi Kobayashi]], _Transformation Groups in Differential Geometry_ 1972, reprinted as: Classics in Mathematics Vol. 70, Springer 1995 ([doi:10.1007/978-3-642-61981-6](https://link.springer.com/book/10.1007/978-3-642-61981-6))

* [[Pierre Molino]], _Theorie des G-Structures: Le Probleme d'Equivalence_, Lecture Notes in Mathematics, Springer (1977) ([ISBN:978-3-540-37360-5](https://www.springer.com/de/book/9783540082460))

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]], Chapter 1 of: _Parabolic Geometries I -- Background and General Theory_, AMS 2009 ([ISBN:978-1-4704-1381-1](http://bookstore.ams.org/surv-154))


See also:

* [[Pierre Molino]], _Sur quelques propriétés des G-structures_, J. Differential Geom. Volume 7, Number 3-4 (1972), 489-518 ([euclid:jdg/1214431168](https://projecteuclid.org/euclid.jdg/1214431168))


Lecture notes:

* [[Marius Crainic]], Chapters 3 and 4 of: _[Differential geometry course](https://webspace.science.uu.nl/~crain101/DG-2015/)_, 2015 ([pdf](https://webspace.science.uu.nl/~crain101/DG-2015/main10.pdf), [[CrainicDifferentialGeometry15.pdf:file]])

* {#Pasquotto} [[Federica Pasquotto]], _Linear $G$-structures by examples_ ([pdf](http://www.few.vu.nl/~pasquott/course16.pdf), [[PasquottoGStructures.pdf:file]])


Surveys include

* {#Alekseevskii} [[Dmitry Vladimirovich Alekseevsky]], _$G$-structure on a manifold_ in M. Hazewinkel (ed.) _Encyclopedia of Mathematics, Volume 4_ ([eom:G-structure](https://encyclopediaofmath.org/wiki/G-structure))

See also

* Wikipedia, _[G-structure](http://en.wikipedia.org/wiki/G-structure)_

Discussion with an eye towards [[special holonomy]] is in 

* {#Joyce} [[Dominic Joyce]], section 2.6 of _Compact manifolds with special holonomy_ , Oxford Mathematical Monogrophs (200)

Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

Discussion of G-structures more generally on [[orbifolds]]:

* A. V. Bagaev, N. I. Zhukova, _The Automorphism Groups of Finite Type $G$-Structures on Orbifolds_, Siberian Mathematical Journal 44, 213–224 (2003) ([doi:10.1023/A:1022920417785](https://doi.org/10.1023/A:1022920417785))

* [[Robert Wolak]], _Orbifolds, geometric structures and foliations. Applications to harmonic maps_, Rendiconti del seminario matematico - Universita politecnico di Torino vol. 73/1 , 3-4 (2016), 173-187 ([arXiv:1605.04190](https://arxiv.org/abs/1605.04190))



### In supergeometry

Discussion of $G$-structures in [[supergeometry]] includes

* [[Dmitri Alekseevsky]], [[Vicente Cortés]], [[Chandrashekar Devchand]], [[Uwe Semmelmann]], _Killing spinors are Killing vector fields in Riemannian Supergeometry_ ([arXiv:dg-ga/9704002](http://arxiv.org/abs/dg-ga/9704002))

  (on [[Killing spinors]] as super-[[Killing vectors]])

### In supergravity 
 {#ReferencesInSupergravity}

Discussion of [[G-structures]] in [[supergravity]] and [[superstring theory]]:

In relation to [[torsion constraints in supergravity]]:

* {#Lott90} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_, Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

As a way of speaking about [[Calabi-Yau structure]] and [[generalized Calabi-Yau structure]]:

* {#Prins16} [[Daniël Prins]], _On flux vacua, $SU(n)$-structures and generalised complex geometry_, Université Claude Bernard -- Lyon I, 2015.  ([arXiv:1602.05415](https://arxiv.org/abs/1602.05415), [tel:01280717](https://tel.archives-ouvertes.fr/tel-01280717))


In relation to [[BPS states]]/partial reduction of [[number of supersymmetries]] under [[KK-compactification]]:

* [[Paul Koerber]], _Lectures on Generalized Complex Geometry for Physicists_, Fortsch. Phys. 59: 169-242, 2011 ([arXiv:1006.1536](https://arxiv.org/abs/1006.1536))

  (with application to [[generalized complex geometry]])


* [[Jerome Gauntlett]], Dario Martelli, Stathis Pakis, [[Daniel Waldram]], _G-Structures and Wrapped NS5-branes_, Commun.Math.Phys. 247 (2004) 421-445 ([arxiv:hep-th/0205050](https://arxiv.org/abs/hep-th/0205050))

  (application to [[flux compactifications]])

* [[Jérôme Gaillard]], _On $G$-structures in gauge/string duality_, 2011 ([cronfa:42569](https://cronfa.swan.ac.uk/Record/cronfa42569) [spire:1340775](http://inspirehep.net/record/1340775), [[GaillardGStructure.pdf:file]])

  (with application to [[holographic QCD]])

* [[Ulf Danielsson]], [[Giuseppe Dibitetto]], Adolfo Guarino, _KK-monopoles and $G$-structures in M-theory/type IIA reductions_, JHEP 1502 (2015) 096 ([arXiv:1411.0575](https://arxiv.org/abs/1411.0575))

  (with application to [[D6-branes]]/[[KK-monopoles]] in [[M-theory]])

and specifically so for [[M-theory on 8-manifolds]]:

* {#IshamPope88} [[Chris Isham]], [[Christopher Pope]], _Nowhere Vanishing Spinors and Topological Obstructions to the Equivalence of the NSR and GS Superstrings_, Class. Quant. Grav. 5 (1988) 257 ([spire:251240](http://inspirehep.net/record/251240), [doi:10.1088/0264-9381/5/2/006](https://doi.org/10.1088/0264-9381/5/2/006))

  (focus on [[Spin(7)-structure]])

* {#IshamPopeWarner88} [[Chris Isham]], [[Christopher Pope]], [[Nicholas Warner]], _Nowhere-vanishing spinors and triality rotations in 8-manifolds_,  Classical and Quantum Gravity, Volume 5, Number 10, 1988 ([cds:185144](http://cds.cern.ch/record/185144), [doi:10.1088/0264-9381/5/10/009](https://iopscience.iop.org/article/10.1088/0264-9381/5/10/009))

  (focus on [[Spin(7)-structure]])


* Cezar Condeescu, [[Andrei Micu]], [[Eran Palti]], _M-theory Compactifications to Three Dimensions with M2-brane Potentials_, JHEP 04 (2014) 026 ([arxiv:1311.5901](https://arxiv.org/abs/1311.5901))

* [[Daniël Prins]], [[Dimitrios Tsimpis]], _IIA supergravity and M-theory on manifolds with $SU(4)$ structure_, Phys. Rev. D 89.064030 ([arXiv:1312.1692](https://arxiv.org/abs/1312.1692))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Singular foliations for M-theory compactification_, JHEP 03 (2015) 116 ([arXiv:1411.3497](https://arxiv.org/abs/1411.3497))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Foliated eight-manifolds for M-theory compactification_, JHEP 01 (2015) 140 ([arXiv:1411.3148](https://arxiv.org/abs/1411.3148))

* C. S. Shahbazi, _M-theory on non-Kähler manifolds_, JHEP 09 (2015) 178 ([arXiv:1503.00733](https://arxiv.org/abs/1503.00733))

* [[Elena Babalic]], [[Calin Lazaroiu]], _The landscape of $G$-structures in eight-manifold compactifications of M-theory_, JHEP 11 (2015) 007 ([arXiv:1505.02270](https://arxiv.org/abs/1505.02270))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Internal circle uplifts, transversality and stratified $G$-structures_, JHEP 11 (2015) 174 ([arXiv:1505.05238](https://arxiv.org/abs/1505.05238))


See also

* Johannes Held, Section 3 of: _Non-SupersymmetricFlux Compactifications of Heterotic String- and M-theory_ ([pdf](https://edoc.ub.uni-muenchen.de/14341/1/Held_Johannes.pdf))

* {#Papadopoulos18} [[George Papadopoulos]], _Geometry and symmetries of null $G$-structures_ ([arXiv:1811.03500](https://arxiv.org/abs/1811.03500))


### In complex geometry

* Sergey Merkulov, _On group theoretic aspects of the non-linear twistor transform_, ([pdf](http://people.maths.ox.ac.uk/lmason/Tn/40/TN40-07.pdf))

and his chapter A in

* [[Yuri Manin]], _Gauge Field Theory and Complex Geometry_, Springer.

* Norman Wildberger, _On the complexication of the classical geometries and exceptional numbers_, ([pdf](http://web.maths.unsw.edu.au/~norman/papers/L.pdf))

* Jun-Muk Hwang, _Rational curves and prolongations of G-structures_,[arXiv:1703.03160](https://arxiv.org/abs/1703.03160)

### In higher geometry

Some discussion in [[higher differential geometry]] is in section 4.4.2 of

* _[[schreiber:differential cohomology in a cohesive topos]]_

Formalization in [[modal type theory|modal]] [[homotopy type theory]] is in 

* {#Wellen17} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_, 2017

* {#Wellen18} [[Felix Wellen]], _[[schreiber:Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))


[[!redirects G-structures]]

