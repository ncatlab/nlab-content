
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
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

## Definition

## Via embedding 

A full [[additive category|additive]] [[subcategory]] $A$ of an [[abelian category]] $B$ is called **Quillen exact category** if it is closed under [[extensions]] (if in extension $0\to X\stackrel{j}\to Y\stackrel{p}\to Z\to 0$, $X$ and $Z$ are in $A$ then $Y$ is in $A$). It is viewed as a pair $(A,E)$ where $E$ is the class of all short exact sequences in $A$ which are [[exact sequence|exact]] in $B$.

All $j$ which appear as $j$ in an exact sequence as above are called __inflation__s or __admissible monomorphism__s. All $p$ which appear in an exact sequence as above are called __deflation__s or __admissible epimorphism__s. 

## Via exact structure

A **Quillen exact category** is a pair $(A,E)$ of an [[additive category]] $A$ and a class of sequences $E$ called 'exact'.
The following axioms are required for $(A,E)$:

(QE1) The class of 'exact' sequences is closed under [[isomorphism]]s and it contains all split extensions.
For any 'exact' sequence the deflation is the [[cokernel]] of inflation and the inflation is the [[kernel]] of the deflation.

(QE2) The class of deflations is closed under [[composition]] and [[base change]] by arbitrary maps. The class of inflations is closed under compositions and [[cobase change]] by arbitrary maps. 

(QE3) If a morphism $M\to M'$ having a [[kernel]] can factor a deflation $N\to M'$ as $N\to M\to M'$ then it is a deflation. If a morphism $I\to I'$ having a cokernel can factor an inflation $I\to J$ as $I\to I'\to J$ then it is also an inflation. 

## Properties

### Quillen-Gabriel embedding theorem

For every small exact category in the sense of a pair $(A,E)$, there is an embedding $A\hookrightarrow B$ into an [[abelian category]] such that $E$ is a class of all sequences which are (short) exact in $B$.

### Relation to Waldhausen categories and algebraic K-theory

Every Quillen exact category can be made into a [[Waldhausen category]]. However some information is lost in the process. Moreover, not every Waldhausen category comes from a Quillen exact category. Both Quillen exact categories and Waldhausen categories are devised in order to do [[algebraic K-theory]]. The K-theory spectrum based on [[Quillen's Q-construction]] and an exact category agrees with the K-theory spectrum based on the [[Waldhausen S-construction]] of the K-theory spectrum from its associated [[Waldhausen category]]. 

## References
 
Quillen introduced exact categories in above sense in the article 

* [[Daniel Quillen]], "Higher algebraic K-theory", in Higher K-theories, pp. 85--147, Proc. Seattle 1972, Lec. Notes Math. 341, Springer  1973.

A nonadditive generalization of exact categories has been introduced by Dyckerhoff and Kapranov and named a [[proto-exact category]].

[[Alexander Rosenberg]]  <a href="http://www.mpim-bonn.mpg.de/preprints/send?bid=3623">introduced</a> one sided generalizations of Quillen exact categories: right 'exact' categories involving deflations, and left 'exact' categories involving inflations. One of the motivations an alternative definition of higher K-theory of (right exact) categories not involving spectra. In this setup the K-theory is an example of a derived functor in nonabelian homological algebra utilizing roughly the left 'exact' structure on the category of essentially small right 'exact' categories. It is not known if this K-theory when restricted to the category of essentially small Quillen exact categories agrees with Quillen K-theory. But it has the standard properties of Quillen K-theory (devissage, exactness and so on).
The one-sided generalization inspired by ideas introduced by Keller and Vossieck in the build up of the theory of [[suspended category|suspended categories]]. 

A right 'exact' category is a category with an initial object and a Grothendieck pretopology consisting of single maps which are [[strict epimorphism]]s. The distinguished class of strict epimorphisms is called a right 'exact' structure, or the class of _deflations_. The construction of derived functors in this generality involves a version of [[satellite|satellites]].

* Dmitry Kaledin, Wendy Lowen, _Cohomology of exact categories and (non-)additive sheaves_, Adv. Math. __272__ (2015) 652--698 [arXiv:1102.5756](https://arxiv.org/abs/1102.5756)

[[!redirects Quillen exact categories]]
[[!redirects Quillen-exact category]]
[[!redirects Quillen exactness]]
[[!redirects Quillen-Gabriel embedding theorem]]