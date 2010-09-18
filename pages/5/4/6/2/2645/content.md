
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--




#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Chern-Weil theory studies the refinement of [[characteristic class]]es of [[principal bundle]]s in ordinary [[cohomology]] to [[de Rham cohomology]] and further to [[ordinary differential cohomology]]. 

The central operation that models this refinement is the construction of the [[Chern-Weil homomorphism]] from $G$-[[principal bundle]]s to [[de Rham cohomology]] by choosing a [[connection on a bundle|connection]] $\nabla$ and evaluating its [[curvature]] form $F_\nabla$ in the [[invariant polynomial]]s $\langle -\rangle$ of the [[Lie algebra]] $\mathfrak{g}$ to produce the [[curvature characteristic form]] $\langle F_\nabla \rangle$. Its de Rham cohomology class refines a corresponding [[characteristic class]] in [[integral cohomology]]. 

## Generalizations

### To principal $\infty$-bundles

The notions of [[Lie group]], [[Lie algebra]], [[principal bundle]] and all the other ingredients of ordinary Chern-Weil theory generalize to notions in [[higher category theory]] such as  [[∞-Lie group]], [[∞-Lie algebra]], [[principal ∞-bundle]] etc. The generalization of Chern-Weil theory to this context is discussed at 

* [[∞-Chern-Weil theory]].

### In noncommutative geometry

There is a [[noncommutative geometry|noncommutative]] analogue discussed in ([AlekseevMeinrenken2000](AlekseevMeinrenken)).
.

## History {#History}

> (following notes provided by [[Jim Stasheff]])

In his exposition of 1936, [[Elie Cartan]]  lists some of the general properties of Lie groups known at that time.  In particular, he lists the [[Poincare polynomial]]s for classical simple compact [[Lie group]]s and, supposing similar results will hold for the exceptional groups, points out that these polynomials are the same as those of products of odd dimensional spheres and even the homology groups are isomorphic as intersection pairing algebras.

In

* [[Heinz Hopf]],  _&#220;ber die Topologie der Gruppen-Mannigfaltigkeiten und ihre Verallgemeinerungen_  (German)  Ann. of Math. (2)  42,  (1941). 22--52.

Hopf showed that such a characterization in terms of homology groups  as intersection pairing algebras holds for any compact finite dimensional connected orientable manifold with a map $m:M\times M\to M$ such that left and right translation have non-zero degrees.

Later, with the development of [[cohomology]], especially [[de Rham cohomology]], this was stated as $H^\bullet (G)$ being isomorphic to  an [[exterior algebra]] on odd dimensional generators (Chern).

Henri Cartan in

* [[Henri Cartan]], _Notions d'alg&#233;bre diff&#233;rentielle; applications aux groupes de Lie et aux vari&#233;t&#233;s o&#249; op&#232;re un groupe de Lie_ ,  Coll. Topologie Alg&#233;brique Bruxelles (1950)
15-28

  section 7, titled _Classes caracteristiques (reelles) d'un espace fibre principal_

at the end (1951) of an era of deRham cohomology dominence (prior to Serre's thesis) abstracted the differential geometric approach of Chern-Weil and the Weil algebra to the [[dg-algebra]] context with his notion of _$\mathfrak{g}$-algebras $W$_ . This involves what is known sometimes as the [[Cartan calculus]].  In addition to the differential $d$ of differential forms on a principal bundle, Cartan abstracts the inner product aka contraction of differential forms with [[vector field]]s and the [[Lie derivative]] with respect to vector fields.  that is, he posits 3 operators on a dgca:

$d$ of degree 1, $i_X$ of degree -1 and $L_X$ of degree 0 for X in $\mathfrak{g}$
subject to the relations:

$$[i_X,i_Y] = i_{[X,Y]}$$

$$ [L_X,i_Y]= i_{[X,Y]} $$

and perhaps most useful

$$L_X = di_X + i_Xd.$$

This is what he terms a $\mathfrak{g}$-algebra.

For Cartan, an infinitesimal connection are  projectors (at each point $p$ of $E$) $\phi_p:T_p E\to T_p^{vert}.$ equivariant with repect to the $G$-action. 
This can be abstracted to an element $f$ of $Hom(\mathfrak{g}^*, A)$ of degree 1 such that

$$i_X f(h) = i_X h$$

and

$$L_X f(h) = f(L_X h)$$

for all $X\in $ and $h\in .$  this Cartan calls an _algebraic connection_ .
He then extends such an $f$ to a [[graded algebra]] morphism $\to A$.  In general, this will not be respect the differentials/not bea cochain map. In fact, the deviation gives the [[curvature]] of the connection:
the curvature tensor is the map $h\mapsto d f(h)-f(d h)$.

> HAVE TO BREAK OFF NOW - WHAT WILL COME NEXT IS the [[Weil algebra]] $W(\mathfrak{g})$ as a Cartan $\mathfrak{g}$-algebra


## Further References

Early original references are

* [[Henri Cartan]], _Notions d'alg&#233;bre diff&#233;rentielle; applications aux groupes de Lie et aux vari&#233;t&#233;s o&#249; op&#232;re un groupe de Lie_ ,  Coll. Topologie Alg&#233;brique Bruxelles (1950)
15-28

  section 7, titled _Classes caracteristiques (reelles) d'un espace fibre principal_


* [[Shiing-shen Chern]], _Differential geometry of fiber bundles_ Proceedings of the International Congress of Mathematicians, Cambridge, Mass., 1950, vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952)

An overview with a collection of references is

* _Connections on vector bundles and the Gauss-Bonnet theorem_ ([pdf](http://www.supermanifold.com/connections.pdf))

Some standard monographs are

* [[Johan Louis Dupont]], _Fibre bundles and Chern-Weil theory_, Lecture Notes Series __69__, Dept. of Math., University of Aarhus, Aarhus, 2003, 115 pp. [pdf](http://www.johno.dk/mathematics/fiberbundlestryk.pdf)

* [[Johan Louis Dupont]], _Curvature and characteristic classes_, Lecture Notes in Math. __640__, Springer-Verlag, Berlin-Heidelberg-New York, 1978. 


* [[Mikhail Postnikov|?. ?. ?????????]], _&#1051;&#1077;&#1082;&#1094;&#1080;&#1080; &#1087;&#1086; &#1075;&#1077;&#1086;&#1084;&#1077;&#1090;&#1088;&#1080;&#1080;. &#1057;&#1077;&#1084;&#1077;&#1089;&#1090;&#1088; 4, &#1044;&#1080;&#1092;&#1092;&#1077;&#1088;&#1077;&#1085;&#1094;&#1080;&#1072;&#1083;&#1100;&#1085;&#1072;&#1103; &#1075;&#1077;&#1086;&#1084;&#1077;&#1090;&#1088;&#1080;&#1103;_ &#8212; &#1052;.: &#1053;&#1072;&#1091;&#1082;&#1072;, 1988	

* [[Raoul Bott|R. Bott]], L. W. Tu, _Differential forms in algebraic topology_, Graduate Texts in Mathematics __82__, Springer 1982. xiv+331 pp.

* V. Guillemin, S. Sternberg, _Supersymmetry and equivariant de Rham theory_, Springer, 1999.

Chern-Weil theory in the context of noncommutative geometry is discussed in

* A. Alekseev, E. Meinrenken, _The non-commutative Weil algebra_, Invent. Math. __139__, n. 1, 135-172, 2000, [doi](http://dx.doi.org/10.1007/s002229900025) {#AlekseevMeinrenken}
