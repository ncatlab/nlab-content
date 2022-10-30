
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

### General

What is known as _(Grothendieck's) six operations_ is a formalization of structure that 

* assigns to every [[morphism]] $f$ of suitable [[spaces]] a ([[derived direct image|derived]])[[direct image]]/([[derived inverse image|derived]])[[inverse image]] [[adjunction]] $(f^\ast \dashv f_*)$;

* assigns to every [[separated morphism]] a [[direct image with compact support]]/[[Verdier duality|Verdier dual]] [[adjunction]] $(f_! \dashv f^!)$.

These are _four operations_ and together with

* a [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]] [[tensor product]]/[[internal hom]] [[adjunction]] $((-)\otimes X \dashv [X,-])$ 

form _six operations_. 

(All this is usually interpreted as [[derived functors]]/[[(infinity,1)-functors]] so that for instance in the usual application to [[derived categories]] of [[abelian sheaves]] the last two operations are really [[Tor]] and [[Ext]].) 

With a list of compatibility conditions between these (for instance ([Cisinski-D&#233;glise 09, p. x](#CisinskiDeglise09)) this is a structure of _Grothendieck's six operations_.


These consistency conditions include the following:

1. The adjunctions are functorial, hence form [[2-functors]] $f \mapsto f_*$, $f \mapsto f_!$:

1. There is a [[natural transformation]]  $f_! \to f_*$ which is a [[natural equivalence]] when $f$ is a [[proper map]]. 

1. [[Beck-Chevalley condition]] (base change formulas): given a ([[homotopy pullback|homotopy]]) [[pullback]] [[diagram]]

   $$
     \array{
       && Q_1 \underset{X}{\times} Q_2
       \\
       & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
       \\
       Q_1 && && Q_2
       \\
       & {}_{\mathllap{f}}\searrow && \swarrow_{\mathrlap{g}}
       \\
       && X
     }
   $$

   such that $f$ is a [[separated morphism]], then there are [[natural equivalences]]

   $$
     g^\ast \circ f_! \simeq (p_2)_! \circ (p_1)^\ast
   $$

   $$
     f^! \circ g_\ast \simeq (p_1)_\ast\circ (p_2)^!
     \,. 
   $$

1. ...

([Cisinski-D&#233;glise 09, p. x](#CisinskiDeglise09))

Morover one imposes a formalization of [[Verdier duality]] with [[dualizing object]]...

([Cisinski-D&#233;glise 09, p. xi](#CisinskiDeglise09))


### Specializations

Often specializations of the general concept play a role:

* [[Wirthmüller context]]: $f^! \simeq f^\ast$ and $f^\ast$ is a strong [[closed monoidal functor]] (hence the [[projection formula]] for $f_!$ holds);

  * [[transfer context]]: in addition the [[projection formula]] for $f_\ast$ holds;

* [[Verdier-Grothendieck context]]: the "projection formula" $Y \otimes f_! X \simeq f_!(f^\ast Y \otimes X)$ holds naturally in $X,Y$:

* [[Grothendieck context]]: $f_! \simeq f_\ast$ and the projection formula holds $Y \otimes f_! X \simeq f_!(f^\ast Y \otimes X)$.


## Properties

### Relation to motivic homotopy theory

The [[initial object]] in the [[(infinity,2)-category]] of functors to [[stable (infinity,1)-categories]] which satisfy the _six  operations_ formalism (and a bit more, such that [[motivic homotopy theory|A1-homotopy invariance]]) is _[[stable motivic homotopy theory]]_. See there for more.


## Related concepts

* [[Grothendieck duality]], [[Verdier duality]]

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]

## References

General abstract discussion is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_, Theory and Applications of Categories , Vol. 11, 2003, No. 4, pp 107-131. ([TAC](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))

* [[Roy Joshua]], _Grothendieck-Verdier duality in enriched symmetric monoidal $t$-categories_ ([[JoshuaDuality.pdf:file]])

* [[Paul Balmer]], [[Ivo Dell'Ambrogio]], [[Beren Sanders]], _Grothendieck-Neeman duality and the Wirthm&#252;ller isomorphism_, [arXiv:1501.01999](http://arxiv.org/abs/1501.01999).

An approach to six functor formalism as a bifibered multicategory (multiderivator, when appropriate) over correspondences is in 

* Fritz H&#246;rmann, _Fibered derivators, (co)homological descent, and Grothendieck's six functors_ [pdf](http://home.mathematik.uni-freiburg.de/hoermann/overview6fu.pdf); _Fibered Multiderivators and (co)homological descent_, [arxiv./1505.00974](http://arxiv.org/abs/1505.00974)

The traditional applications ([[quasicoherent sheaves of modules]]) are discussed in

* [[Joseph Lipman]], _Notes on derived functors and Grothendieck duality_, in _Foundations of Grothendieck Duality for Diagrams of Schemes_,
Lecture Notes in Math., no. 1960, Springer-Verlag, New York, 2009, 1&#8211;259. ([pdf](http://www.math.purdue.edu/~lipman/Duality.pdf))


* Yves Laszlo, Martin Olsson, _The six operations for sheaves on Artin stacks I: Finite Coefficients_ ([arXiv:math/0512097](http://arxiv.org/abs/math/0512097))

An [[enhanced triangulated category|enhanced]] version of the six operations formalism for [[etale cohomology]] of [[Artin stacks]] (and [[higher Artin stacks]]), using the language of [[stable (infinity,1)-categories]] is developed in

* Yifeng Liu, Weizhe Zheng, _Enhanced six operations and base change theorem for Artin stacks_, [arXiv](http://arxiv.org/abs/1211.5948).

The six functor formalism for [[motivic homotopy theory]] was developed in

* [[Joseph Ayoub]], _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescants dans le monde motivique_ PhD thesis, Paris ([pdf](http://www.math.uiuc.edu/K-theory/0761/THESE.pdf))

Discussion for pull-push of ([[holonomic D-module|holonomic]]) [[D-modules]] is in

* [[Joseph Bernstein]], around p. 18 of _Algebraic theory of D-modules_ ([[BernsteinDModule.pdf:file]], [ps](http://www.math.uchicago.edu/~mitya/langlands/Bernstein/Bernstein-dmod.ps), [dvi](http://www.math.uchicago.edu/~mitya/langlands/Bernstein/Bernstein-dmod.dvi))

reviewed for instance in

* [[Pavel Etingof]], _Formalism of six functors on all (coherent) D-modules_ ([pdf](http://www-math.mit.edu/~etingof/dmodfactsheet.pdf))

* [[David Ben-Zvi]], [[David Nadler]], section 3 of _The Character Theory of a Complex Group_ ([arXiv:0904.1247](http://arxiv.org/abs/0904.1247))

A quick list of the axioms with a  Grothendieck's six operations with an eye towards the definition of [[motives]] is in section A.5 of 

* [[Denis-Charles Cisinski]], Fr&#233;d&#233;ric D&#233;glise, _Triangulated categories of mixed motives_ ([arXiv:0912.2110](http://arxiv.org/abs/0912.2110))
 {#CisinskiDeglise09}

The six operations for [[derived categories]] of [[quasi-coherent sheaves]], [[ind-coherent sheaves]], and [[D-modules]] on [[derived stacks]] are developed in

* [[Dennis Gaitsgory]], [[Notes on geometric Langlands]], [web](http://www.math.harvard.edu/~gaitsgde/GL/).

Six operations in the setup of [[o-minimal structure]]s is discussed in 

* Mario J. Edmundo, Luca Prelli, _The six Grothendieck operations on o-minimal sheaves_, [arxiv/1401.0846](http://arxiv.org/abs/1401.0846)
 
Grothendieck six operations formalism using diagrams of topoi

* Alexey Kalugin, _On categorical approach to Verdier duality_, [arxiv/1505.06922](http://arxiv.org/abs/1505.06922)
 

[[!redirects six operations]]
[[!redirects Grothendieck's six operations]]
[[!redirects Grothendieck\'s six operations]]
[[!redirects Grothendieck's six operations]]
[[!redirects Grothendieck six operations]]
[[!redirects yoga of six functors]]
[[!redirects yoga of six operations]]

[[!redirects six operation yoga]]
[[!redirects six operations yoga]]
