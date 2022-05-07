
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Quasigroup is a binary algebraic structure in which every equation of the form $a\cdot x = b$ or of the form $y\cdot a = b$ has a unique solution for $x$, resp. $y$. The notion of _quasigroup_ is a generalization of the notion of _[[group]]_ without the [[associativity]] law or [[identity]] element.   A quasigroup with identity is called a _loop_ (French _la boucle_, Russian &#1083;&#1091;&#1087;&#1072;).

Note that, in the absence of associativity, it is not enough (even for a loop) to say that every element has an [[inverse element]] (on either side); instead, you must say that division is always possible.  This is because the definition $x/y = x y^{-1}$ won\'t work right without associativity.

Some consider the concept of quasigroup to be an example of [[centipede mathematics]], see more at [[historical notes on  quasigroups]]. 


## Definitions

The usual definition is this:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with a binary operation $G \times G \to G$ (which we will write with concatenation) such that:

*  for all $x$ and $y$, there exist unique $l$ and $r$ such that $l x = y$ and $x r = y$.

Then $l$ is called the __left quotient__ $y / x$ ($y$ divided by $x$, $y$ over $x$) and $r$ is called the __right quotient__ $x \backslash y$ ($x$ dividing $y$, $x$ under $y$).
=--
Note that we must specify, in the definition, that $l$ and $r$ are unique; without associativity, we cannot prove this.

As with the inverse elements of a group, we can make the quotients into operations so that all axioms are equations:
+-- {: .un_defn}
###### Definition

A __quasigroup__ is a [[set]] $G$ equipped with three binary operations (product, left quotient, and right quotient) such that these equations always hold:

*  $(x / y) y = x$,
*  $x (x \backslash y) = y$,
*  $(x y) / y = x$,
*  $x \backslash (x y) = y$.

=--

Also, without the right quotient we have left quasigroups, and without the left quotient the right quasigroups.
Thus quasigroups are described by a [[Lawvere theory]] and can therefore be [[internalization|internalized]] into any [[cartesian monoidal category]]. There are weaker structures, say left and right quasigroups in which either $\backslash$ or $/$ is well defined. 

In any case:
+-- {: .un_defn}
###### Definition

A __loop__ is a quasigroup with an [[identity element]].
=--
Loops are also described by a Lawvere theory.

Note that, even in a loop, left and right inverses need not agree.  See [the discussion on the English Wikipedia](http://secure.wikimedia.org/wikipedia/en/wiki/Quasigroup#Inverse_properties) for convenient inverse properties.

For good measure, here is another special kind of quasigroup:
+-- {: .un_defn}
###### Definition

A __[[group]]__ is an associative loop.
=--


## Examples

*  Any group is a loop, of course.
*  Any [[abelian group]] is a quasigroup in two other ways: the product switches places with one of the quotients.  (The other quotient remains a quotient.)
* [[H-space]]s are (homotopy-) loops --- this is because the [[shearing map]]s $(x,y)\mapsto (x,x y)$ and $(x,y)\mapsto (x y, y)$ are equivalences.  This generalizes the octonion examples.  Note that a [[loop space]] is always equivalent to a *group*, hence not all homotopy loops are loop spaces.  In particular ...
*  The nonzero elements of a (not necessarily associative) [[division algebra]] (such as the [[octonion]]s) form a quasigroup; this fact is basically the definition of 'division algebra'.
* [[code loop]]s are loops which are central extensions of abelian groups (actually vector spaces over the finite field $\mathbb{F}_2$) by $\mathbb{Z}_2$.

See also [[Moufang loop]] and [[associative quasigroup]]. 

## Applications

Local analytic loops have interesting induced structure on the tangent space at the identity, generalizing the Lie algebra of a group, see [[Sabinin algebra]]. Sabinin algebras are closely related to the local study of affine connections on manifolds. They include some known important classes of nonassociative algebras, namely Lie algebras, Mal'cev algebras, Lie triple systems (related to the study of [[symmetric space]]s), Bol algebras as simplest cases.

There are interesting subvarieties of quasigroups and loops (which are still not associative). Also, left [[racks]] (and quandles in particular) are precisely left distributive left quasigroups, with abundance of recent applications in the study of knots and links. Finite racks have been studied in the connection to classification of finite dimensional pointed Hopf algebras. Local augmented Lie racks appeared as integration objects in the local integration theory of [[Leibniz algebra]]s.

TS-quasigroups are related to [[Steiner triple system]]s. 

Cayley multiplication tables of finite quasigroups are [[Latin square]]s (basically the 'sudoku squares' from the quotation [[historical notes on quasigroups|here]]). 

As a sample of centipede mathematics, we have the following result on smooth quasigroups, i.e., quasigroups internal to the category of [[smooth manifolds]]: 

+-- {: .num_prop} 
###### Proposition 
The tangent bundle of a smooth quasigroup $Q$ is trivial. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose WLOG that $Q$ is inhabited by an element $x$, and let $V = T_x(Q)$ be the tangent space at $x$. Define a map 

$$\phi \colon Q \times V \to T Q: (y, v) \mapsto (d (K \circ L_y))(v)$$ 

where $L_y: Q \to Q$ is the smooth map $z \mapsto y z$ and $K: Q \to Q$ is the map $z \mapsto z/x$. The map $\phi$ commutes with the bundle projections $\pi_Q: Q \times V \to Q$, $\pi: T Q \to Q$. The map $K$ has an inverse $J: z \mapsto z x$ and each map $L_y$ has an inverse $M_y: z \mapsto y \backslash z$. We may therefore write down an inverse to $\phi$: 

$$T Q \to Q \times V: w \mapsto (\pi(w), d(M_{\pi(w)} \circ J))(w)).$$ 

This shows $T Q$ is isomorphic to the product bundle $Q \times V$. 
=--  

## Literature

* [[eom]]: [quasi-group](http://www.encyclopediaofmath.org/index.php/Quasi-group), [Webs, geometry of](http://www.encyclopediaofmath.org/index.php/Webs,_geometry_of), [Net (in differential geometry)](http://www.encyclopediaofmath.org/index.php/Net_%28in_differential_geometry%29)
* R.H. Bruck, _A survey of binary systems_, Springer-Verlag 1958
* [[Kenneth Kunen]], _Quasigroups, loops, and associative laws_, J. Algebra __185__ (1) (1996), pp. 194&#8211;204
* P&#233;ter T. Nagy, Karl Strambach, _Loops as invariant sections in groups, and their geometry_, Canad. J. Math. __46__(1994), 1027-1056 [doi](http://dx.doi.org/10.4153/CJM-1994-059-8)
* Momo Bangoura, _Big&#232;bres quasi-Lie et boucles de Lie_,  Bull. Belg. Math. Soc. Simon Stevin __16__:4 (2009), 593-616 [euclid](http://projecteuclid.org/euclid.bbms/1257776236) [arXiv:math.SG/0607662 ](http://arxiv.org/abs/math/0607662); _Quasi-big&#232;bres de Lie et cohomologie d'alg&#232;bre de Lie_, [arxiv/1006.0677](http://arxiv.org/abs/1006.0677) 
* Lev Vasil&#697;evich Sabinin, _Smooth quasigroups and loops: forty-five years of incredible growth_, Commentationes Mathematicae Universitatis Carolinae __41__ (2000), No. 2, 377--400 [cdml](http://dml.cz/dmlcz/119171) [pdf](http://dml.cz/dmlcz/119171)


[[!redirects quasigroup]]
[[!redirects quasigroups]]
[[!redirects loop (algebra)]]
[[!redirects loop(algebra)]]
