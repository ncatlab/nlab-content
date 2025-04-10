
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

A _fibre bundle_ or _fiber bundle_ is a [[bundle]] in which every [[fibre]] is [[isomorphism|isomorphic]], in some coherent way, to a _standard fibre_ or _typical fiber_. Usually one also requires that it be [[locally trivial]], hence locally of the form of a [[Cartesian product]] with that typical fiber.



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

If $C$ is a [[site]], then a __[[locally trivial|locally]] [[trivial fibre bundle]]__ over $B$ with typical fibre $F$ is a bundle over $B$ with a [[cover]] $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, the pullback $E_\alpha$ of $E$ along $j_\alpha$ is isomorphic in the [[slice category]] $C/{U_\alpha}$ to the [[trivial bundle]] $U_\alpha \times F$ (a _[[local trivialization]]_).

One can also drop $F$ and define a slightly more general notion of __[[locally trivial]] bundle__ over $B$ as a bundle over $B$ with a cover $(j_\alpha: U_\alpha \to B)_\alpha$ such that, for each index $\alpha$, there is a fibre $F_\alpha$ and an isomorphism in $C/{U_\alpha}$ between the pullback $E_\alpha$ and the trivial bundle $U_\alpha \times F_\alpha$.  Every [[locally trivial]] fibre bundle is obviously a locally trivial bundle; the converse holds if $B$ is [[connected object|connected]].

+-- {: #TransitionMorphisms}
Now suppose that $E$ is a fibre bundle over $B$ with [[typical fibre]] $F$, [[local trivialization|locally trivialised]] over an ([[open cover|open]]) [[cover]] $(U_\alpha)_\alpha$ via [[isomorphisms]] $(t_\alpha \colon E_\alpha \simeq U_\alpha\times F)_\alpha$.  Given an index $\alpha$ and an index $\beta$, let $U_{\alpha,\beta}$ be the [[fibred product]] (pullback) of $U_\alpha$ and $U_\beta$. Note that we can pull back the commutative triangle formed by $t_\alpha$ along $j_\alpha^*j_\beta$ to get a new isomorphism $t_{\alpha,\beta} \colon E_{\alpha,\beta} \simeq U_{\alpha,\beta} \times F$:

\begin{centre}
\begin{tikzcd}
	{U_\alpha\times F} &&& {U_{\alpha,\beta}\times F} \\
	& \textcolor{rgb,255:red,100;green,100;blue,100}{U_\alpha} & \textcolor{rgb,255:red,100;green,100;blue,100}{U_{\alpha,\beta}} \\
	{E_\alpha} &&& {E_{\alpha,\beta}}
	\arrow["{j_\alpha^*j_\beta}", color={rgb,255:red,100;green,100;blue,100}, from=2-3, to=2-2]
	\arrow[from=3-1, to=2-2]
	\arrow[from=1-1, to=2-2]
	\arrow["\sim"{sloped}, "{t_\alpha}"', from=3-1, to=1-1]
	\arrow[from=1-4, to=2-3]
	\arrow[from=3-4, to=2-3]
	\arrow[from=1-4, to=1-1]
	\arrow["{t_{\alpha,\beta}}", "\sim"{sloped,swap}, from=3-4, to=1-4]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-90}, draw=none, from=1-4, to=2-2]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=180}, draw=none, from=3-4, to=2-2]
	\arrow[from=3-4, to=3-1]
\end{tikzcd}
\end{centre}

We can do the same on the other side, leading to the following situation:

\begin{centre}
\begin{tikzcd}
	&&& {U_{\alpha,\beta}\times F} \\
	&&& {E_{\alpha,\beta}} \\
	&&& \textcolor{rgb,255:red,100;green,100;blue,100}{U_{\alpha,\beta}} \\
	{U_\alpha\times F} & {E_\alpha} & \textcolor{rgb,255:red,100;green,100;blue,100}{U_\alpha} && \textcolor{rgb,255:red,100;green,100;blue,100}{U_\beta} & {E_\beta} & {U_\beta\times F} \\
	&&& \textcolor{rgb,255:red,100;green,100;blue,100}{B} \\
	&&& E \\
	&&& {B \times F}
	\arrow["{j_{\alpha}}", color={rgb,255:red,100;green,100;blue,100}, from=4-3, to=5-4]
	\arrow["{j_{\beta}}"', color={rgb,255:red,100;green,100;blue,100}, from=4-5, to=5-4]
	\arrow["{j_\alpha^*j_\beta}", color={rgb,255:red,100;green,100;blue,100}, from=3-4, to=4-3]
	\arrow["{j_\beta^*j_\alpha}"', color={rgb,255:red,100;green,100;blue,100}, from=3-4, to=4-5]
	\arrow[from=2-4, to=3-4]
	\arrow[from=4-6, to=4-5]
	\arrow[from=6-4, to=5-4]
	\arrow[from=4-2, to=4-3]
	\arrow[from=4-2, to=6-4]
	\arrow[from=4-6, to=6-4]
	\arrow[from=2-4, to=4-2]
	\arrow[from=2-4, to=4-6]
	\arrow[from=4-1, to=7-4]
	\arrow[from=4-7, to=7-4]
	\arrow[from=1-4, to=4-1]
	\arrow[from=1-4, to=4-7]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-90}, draw=none, from=2-4, to=4-3]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=2-4, to=4-5]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=4-2, to=5-4]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-90}, draw=none, from=4-6, to=5-4]
	\arrow["{t_\alpha}"', "\sim"{sloped,swap}, from=4-2, to=4-1]
	\arrow["{t_\beta}", "\sim"{sloped,swap}, from=4-6, to=4-7]
	\arrow["{t_{\beta,\alpha}}"'{pos=0.4}, bend right=30, "\sim"{sloped}, from=2-4, to=1-4]
	\arrow["{t_{\alpha,\beta}}"{pos=0.4}, bend left=30, "\sim"{sloped}', from=2-4, to=1-4]
	\arrow["\lrcorner"{anchor=center, pos=0.125, rotate=-45}, color={rgb,255:red,100;green,100;blue,100}, draw=none, from=3-4, to=5-4]
\end{tikzcd}
\end{centre}

Then we have an [[automorphism]] $g_{\alpha,\beta}$ of $U_{\alpha,\beta} \times F$ in $C/{U_{\alpha,\beta}}$ given by $g_{\alpha,\beta} = t_{\beta,\alpha} \circ t_{\alpha,\beta}^{-1}$. The $g_{\alpha,\beta}$ are the __[[transition morphisms]]__ of the locally trivial fibre bundle $E$.

If $E$ in fact admits a *global* [[trivial fiber bundle|trivialisation]] $t \colon E \simeq B \times F$, then one can see that the two isomorphisms $t_{\alpha,\beta}$ and $t_{\beta,\alpha}$ are equal to the pullback of (the commutative triangle formed by) $t$ along $j_{\alpha,\beta} : U_{\alpha,\beta} \to B$, so that the [[transition morphisms]] $g_{\alpha,\beta}$ are all [[identity morphism|identities]].
=--

Often one considers special kinds of bundles, by requiring structure on the standard fibre $F$ and/or conditions on the [[transition morphisms]] $g_{\alpha,\beta}$.  For example:

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

## Properties

### Relation to fibrations
 {#RelationToFibrations}

\begin{prop}

Every [[locally trivial]] topological fiber bundle projection is a [[Serre fibration]], and a [[Hurewicz fibration]] if it is also a [[numerable bundle]].

\end{prop}

\begin{proof}
  It is clear that the [[projection]] out of a [[Cartesian product]] is a [[Serre fibration]]. With this, the statement follows from [[local triviality]] and the local recognition of Serre fibrations ([this Prop](Serre+fibration#MapIsSerreFibrationIfLocallySo)) and of [[Hurewicz fibrations]] ([this Prop.](Hurewicz+fibration#MapIsHurewiczFibrationIfPullbackToNumerableCoverIsSo)), respectively.
\end{proof}

\begin{remark}
  Beware that the converse statement is far from being true.
\end{remark}


## Related concepts

* [[bundle]]

* [[Ehresmann's theorem]]

* **fiber bundle** / [[fiber ∞-bundle]]

  * [[associated bundle]]

  * [[vector bundle]]

  * [[sphere fiber bundle]], [[spherical fibration]]

  * [[empty bundle]]

  * [[equivariant bundle]]

  * [[fiber bundles in physics]]

  * [[Leray-Hirsch theorem]]

* [[principal bundle]] / [[torsor]] / **associated bundle**

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / [[associated ∞-bundle]]

* [[(∞,1)-vector bundle]] / [[(∞,n)-vector bundle]]

## References

Fiber bundles (then spelled fibre-bundles) were originally defined in:

* [[Hassler Whitney]], *On the theory of sphere-bundles*, Proceedings of the National Academy of Sciences **26** 2 (1940) 148-153 &lbrack;[doi:10.1073/pnas.26.2.148](https://doi.org/10.1073/pnas.26.2.148)&rbrack;

  > (with focus on [[sphere bundles]])

Other sources:

* [[Norman Steenrod]], Section I.7 of _The topology of fibre bundles_, Princeton Mathematical Series **14**, Princeton Univ. Press (1951) &lbrack;[jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5)&rbrack;

* [[Alexander Grothendieck]], *A General Theory of Fibre Spaces With Structure Sheaf*, University of Kansas, Report No. 4 (1955, 1958) &lbrack;[pdf](https://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/Kansasnotes.pdf), [[Grothendieck-FibreSpaces.pdf:file]]&rbrack;

  > (in relation to [[nonabelian cohomology|nonabelian]] [[Čech cohomology]])

* [[Jean Frenkel]], *Cohomologie non abélienne et espaces fibrés*, Bulletin de la Société Mathématique de France, **85** (1957) 135-220 &lbrack;[numdam:BSMF_1957__85__135_0](http://www.numdam.org/item/BSMF_1957__85__135_0)&rbrack;


* [[Glen Bredon]], Section II.1 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN:9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))

* [[Dale Husemöller]]: _Fibre bundles_, Springer (1966, 1975 , 1994) &lbrack;[doi:10.1007/978-1-4757-2261-1](https://doi.org/10.1007/978-1-4757-2261-1), [pdf](https://link.springer.com/content/pdf/10.1007/978-1-4757-4008-0.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/husemoller), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/husemoller.pdf)&rbrack;

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, 
Lecture Notes in Physics, Springer 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

* [[Ralph Cohen]], _The Topology of Fiber Bundles_, Stanford University (2017) ([pdf](http://math.stanford.edu/~ralph/fiber.pdf), [OMN:201707.110706](https://www.ams.org/open-math-notes/omn-view-listing?listingId=110706))

* [[Dai Tamaki]], *Fiber Bundles and Homotopy*, World Scientific 2021 ([doi:10.1142/12308](https://doi.org/10.1142/12308))

  > (in the context of [[homotopy theory]])

With an eye towards application in [[mathematical physics]]:

* [[Mikio Nakahara]], Chapter 9 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)

* [[Gerd Rudolph]], [[Matthias Schmidt]], Chapter 1 of: *Differential Geometry and Mathematical Physics Part II. Fibre Bundles, Topology and Gauge Fields*, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))

Discussion of fiber bundles [[internalization|internal]] to [[finitely complete categories]]:

* [[Anders Kock]], *Fibre bundles in general categories*, Journal of Pure and Applied Algebra **56** 3 (1989) 233-245 &lbrack;<a href="https://doi.org/10.1016/0022-4049(89)90059-5">doi:10.1016/0022-4049(89)90059-5</a>&rbrack;

* [[Anders Kock]], *Generalized fibre bundles*, in: Categorical Algebra and its Applications, Lecture Notes in Mathematics **1348** (2006) 194-207 &lbrack;[doi:10.1007/BFb0081359](https://doi.org/10.1007/BFb0081359)&rbrack;


[[!redirects fiber bundles]]


[[!redirects fibre bundle]]
[[!redirects fibre bundles]]



[[!redirects standard fiber]]
[[!redirects standard fibre]]

[[!redirects typical fiber]]
[[!redirects typical fibre]]

[[!redirects locally trivial fiber bundle]]
[[!redirects locally trivial fiber bundles]]

[[!redirects locally trivial fibre bundle]]
[[!redirects locally trivial fibre bundles]]

[[!redirects locally trivial bundle]]
[[!redirects locally trivial bundles]]


[[!redirects G-bundle]]
[[!redirects G-bundles]]

[[!redirects bundle with structure group]]
[[!redirects bundle with structure groups]]
[[!redirects bundles with structure groups]]

[[!redirects standard fiber]]
[[!redirects standard fibres]]

[[!redirects typical fiber]]
[[!redirects typical fibres]]


[[!redirects transition function]]
[[!redirects transition functions]]

[[!redirects transition map]]
[[!redirects transition maps]]

[[!redirects transition morphism]]
[[!redirects transition morphisms]]



