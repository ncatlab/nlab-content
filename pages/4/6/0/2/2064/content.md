
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A __fibre bundle__ or __fiber bundle__ is a [[bundle]] in which every [[fibre]] is [[isomorphism|isomorphic]], in some coherent way, to a __standard fibre__ (sometimes also called __typical fiber__). Though it is pre-dated by many examples and methods, systematic usage of locally [[trivial fibre bundles]] with structure groups in mainstream mathematics started with a famous book of Steenrod. 

One may say that 'fibre bundles are [[fibrations]]' by the [[Milnor slide trick]].


## Definitions

In the most general sense, a __bundle__ over an object $B$ in a [[category]] $C$ is a [[morphism]] $p: E \to B$ in $C$.

In appropriate contexts, a __fibre bundle__ over $B$ with standard fibre $F$ may be defined as a bundle over $B$ such that, given any [[global element]] $x: 1 \to B$, the [[pullback]] of $E$ along $x$ is isomorphic to $F$. 
Certainly this definition is appropriate whenever $C$ has a [[terminal object]] $1$ which is a [[separator]], as in a [[well-pointed category]]; even then, however, one often wants the more restrictive notion below.

One often writes a typical fibre bundle in shorthand as $F \to E \to B$ or
$$ \array {
   F & \rightarrow & E \\
     &             & \downarrow \\
     &             & B
} $$
even though there is not a single morphism $F \to E$ but instead one for each global element $x$ (and none at all if $B$ has no global elements!).

If $C$ is a [[site]], then a __locally [[trivial fibre bundle]]__ over $B$ with typical fibre $F$ is a bundle over $B$ with a [[cover]] $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, the pullback $E_\alpha$ of $E$ along $j_\alpha$ is isomorphic in the [[slice category]] $C/{U_\alpha}$ to the [[trivial bundle]] $U_\alpha \times F$ (a _[[local trivialization]]_).

One can also drop $F$ and define a slightly more general notion of __locally trivial bundle__ over $B$ as a bundle over $B$ with a cover $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, there is a fibre $F_\alpha$ and an isomorphism in $C/{U_\alpha}$ between the pullback $E_\alpha$ and the trivial bundle $U_\alpha \times F_\alpha$.  Every locally trivial fibre bundle is obviously a locally trivial bundle; the converse holds if $B$ is [[connected object|connected]].

Now suppose that $E$ is a fibre bundle over $B$ with standard fibre $F$, locally trivialised using the cover $(U_\alpha)_\alpha$.  Given an index $\alpha$ and an index $\beta$, let $U_{\alpha,\beta}$ be the [[fibred product]] (pullback) of $U_\alpha$ and $U_\beta$.  Then we have an [[automorphism]] $g_{\alpha,\beta}$ of $U_{\alpha,\beta} \times F$ in $C/{U_{\alpha,\beta}}$ as follows:
(diagram to come)
The $g_{\alpha,\beta}$ are the __transition morphisms__ of the locally trivial fibre bundle $E$.

Often one considers special kinds of bundles, by requiring structure on the standard fibre $F$ and/or conditions on the transition morphisms $g_{\alpha,\beta}$.  For example:

## Special cases 

### $G$-bundle 

If $G$ is a [[group object]] in $C$ that [[action|acts]] on $F$, then a __$G$-bundle__ (or bundle with __structure group__ $G$) over $B$ with standard fibre $F$ is a locally trivial fibre bundle over $B$ with standard fibre $F$ together with morphisms $U_{\alpha,\beta} \to G$ that, relative to the action of $G$ on $F$, give the transition maps $g_{\alpha,\beta}$.  (The morphism $U_{\alpha,\beta} \to G$ is also written $g_{\alpha,\beta}$, conflating action with application.)

### $G$-principal bundles 

More specifically, a (right or left) __[[principal bundle|principal]] $G$-bundle__ over $B$ is a $G$-bundle over $B$ with standard fibre $G$, associated with the action of $G$ on itself by (right or left) multiplication.

### Structure-preserving bundles 

If $F$ is an object of a [[concrete category]] over $C$, then we can consider locally trivial fibre bundles with standard fibre $F$ such that the transition morphisms are structure-preserving morphisms.  If the [[automorphism group]] $Aut(F)$ can be internalised in $C$, then this the same as an $Aut(F)$-bundle, but the concept makes sense in any case.

### Vector bundles 

As a fairly specific example, if $F$ is a [[topological vector space]] (and $C$ is a category with structure to support this, such as [[Top]] or [[Diff]]), then a __[[vector bundle]]__ over $B$ with standard fibre $F$ is a $GL(F)$-bundle over $B$ with standard fibre $F$, where $GL(F)$ is the [[general linear group]] with its defining action on $F$.

### Associated bundles 

Given a right [[principal bundle|principal]] $G$-bundle $\pi: P\to X$ and a left $G$-space $F$, all in a sufficiently strong category $C$ (such as [[Top]]), one can form the [[quotient object]] $P\times_G F = (P\times F)/{\sim}$, where $P \times F$ is a [[product]] and $\sim$ is the smallest [[congruence]] such that (using [[generalized element]]s) $(p g,f)\sim (p,g f)$; there is a canonical projection $P\times_G F\to X$ where the class of $(p,f)$ is mapped to $\pi(p)\in X$, hence making $P\times_G F\to X$ into a fibre bundle with typical fiber $F$, and the transition functions belonging to the action of $G$ on $F$. We say that  $P\times_G F\to X$ is the __[[associated bundle]]__ to $P\to X$ with fiber $F$. 

## Generalizations

### In higher category theory

In [[higher category theory]] the notion of fiber bundle generalizes. See

* [[associated ∞-bundle]].

### In commutative algebra

Under the interpretation of [modules as generalized vector bundles](http://ncatlab.org/nlab/show/module#RelationToVectorBundlesInIntroduction), locally trivial fiber bundles correspond to _[[locally free modules]]_. See there for more.

### In noncommutative geometry 

In [[noncommutative geometry]] both principal and associated bundles have analogues. The principal bundles over noncommutative spaces typically have structure group replaced by a [[Hopf algebra]]; the most well-known class whose base is described by a single algebra are [[Hopf--Galois extensions]]; the global sections of the associated bundle are formed using cotensor product. Transition functions can be to some extent emulated using noncommutative localizations, which yield nonaffine generalizations of Hopf--Galois extensions. Another generalization is when Hopf--Galois extensions in the sense of comodule algebras are replaced by entwining structures with analogous Galois condition. 


## Related concepts

* [[bundle]]

* **fiber bundle** / [[fiber ∞-bundle]]

  * [[associated bundle]]

  * [[vector bundle]]

  * [[sphere fiber bundle]], [[spherical fibration]]

  * [[equivariant bundle]]

  * [[fiber bundles in physics]]

  * [[Leray-Hirsch theorem]]

* [[principal bundle]] / [[torsor]] / **associated bundle**

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

## References

Fiber bundles (then spelled fibre-bundles) were defined by [[Hassler Whitney]] in

* [[Hassler Whitney]], _On the theory of sphere-bundles_, Proceedings of the National Academy of Sciences 26:2 (1940), 148-153.  [doi](https://doi.org/10.1073/pnas.26.2.148).

Other sources include

* [[Norman Steenrod]], section I.7 of _The topology of fibre bundles_, Princeton Mathematical Series 14, Princeton Univ. Press, 1951 ([jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5))


* [[Dale Husemöller]], _Fibre bundles_, McGraw-Hill 1966 (300 p.); Springer Graduate Texts in Math. __20__, 2nd ed. 1975 (327 p.), 3rd. ed. 1994 (353 p.) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/husemoller)) 

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, 
Lecture Notes in Physics, Springer 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

* [[Ralph Cohen]], _The Topology of Fiber Bundles_, Stanford University (2017) ([pdf](http://math.stanford.edu/~ralph/fiber.pdf), [OMN:201707.110706](https://www.ams.org/open-math-notes/omn-view-listing?listingId=110706))


With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Chapter 9 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)



[[!redirects fibre bundle]]
[[!redirects standard fiber]]
[[!redirects standard fibre]]
[[!redirects typical fiber]]
[[!redirects typical fibre]]
[[!redirects locally trivial fiber bundle]]
[[!redirects locally trivial fibre bundle]]
[[!redirects locally trivial bundle]]
[[!redirects transition morphism]]
[[!redirects transition map]]
[[!redirects transition function]]
[[!redirects G-bundle]]
[[!redirects bundle with structure group]]
[[!redirects fiber bundles]]
[[!redirects fibre bundles]]
[[!redirects standard fibers]]
[[!redirects standard fibres]]
[[!redirects typical fibers]]
[[!redirects typical fibres]]
[[!redirects locally trivial fiber bundles]]
[[!redirects locally trivial fibre bundles]]
[[!redirects locally trivial bundles]]
[[!redirects transition morphisms]]
[[!redirects transition maps]]
[[!redirects transition functions]]
[[!redirects G-bundles]]
[[!redirects bundles with structure group]]
[[!redirects bundles with structure groups]]

[[!redirects locally trivial bundle]]
[[!redirects locally trivial bundles]]
[[!redirects locally trivial fiber bundle]]
[[!redirects locally trivial fiber bundles]]