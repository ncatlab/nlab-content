
> This entry is about loops in [[algebra]]. For loops in [[topology]] see *[[loop (topology)]]*.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebra]] a *loop* is a [[quasigroup]] with (two-sided) [[identity element]].

## Definition

A __left loop__ is a [[unital magma]] $(G, (-)\cdot(-):G\times G\to G,1:G)$ equipped with a __left division__ $(-)\backslash(-):G \times G \to G$  such that $x \cdot (x \backslash y) = y$ and $x \backslash (x \cdot y) = y$. A __right loop__ is a [[unital magma]] $(G, (-)\cdot(-):G\times G\to G,1:G)$ equipped with a __right division__ $(-)/(-):G \times G \to G$ such that $(x / y) \cdot y = x$ and $(x \cdot y) / y = x$. A __two-sided loop__ or just a __loop__ is a unital magma that is both a left loop and a right loop. 

There is another definition of a loop using only division: 

A __left loop__ is a [[pointed]] [[magma]] $(G,\backslash,1)$ such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=1$
  * For all $a$ in $G$, $(a\backslash 1)\backslash 1=a$

A __right loop__ is a [[pointed]] [[magma]] $(G,/)$ such that:

  * For all $a$ and $b$ in $G$, $a/a=1$
  * For all $a$ in $G$, $1/(1/a)=a$

A __loop__ is a left and right loop as defined above $(G,\backslash,/,1)$ such that $a/(1/b) = (a\backslash 1)\backslash b$ for all $a$ and $b$ in $G$.

Loops are described by a Lawvere theory.

Note that, even in a loop, left and right inverses need not agree.  See [the discussion on the English Wikipedia](http://secure.wikimedia.org/wikipedia/en/wiki/Quasigroup#Inverse_properties) for convenient inverse properties.

## Examples

*  Any [[group]] is a loop.

*  The nonzero elements of a (not necessarily associative) unital [[division algebra]] (such as the [[octonion]]s) form a quasigroup; this fact is basically the definition of 'division algebra'.
* [[code loop]]s are loops which are central extensions of abelian groups (actually vector spaces over the finite field $\mathbb{F}_2$) by $\mathbb{Z}_2$.

* A [[Moufang loop]] is a loop. 

## Applications

Local analytic loops have interesting induced structure on the tangent space at the identity, generalizing the Lie algebra of a group, see [[Sabinin algebra]]. Sabinin algebras are closely related to the local study of affine connections on manifolds. They include some known important classes of nonassociative algebras, namely Lie algebras, Mal'cev algebras, Lie triple systems (related to the study of [[symmetric space]]s), Bol algebras as simplest cases.

## Related concepts

* [[Moufang loop]]

* [[possibly empty loop]]

[[!include oidification - table]]

## Literature

* [[Kenneth Kunen]], _Quasigroups, loops, and associative laws_, J. Algebra __185__ (1) (1996), pp. 194&#8211;204

* P&#233;ter T. Nagy, Karl Strambach, _Loops as invariant sections in groups, and their geometry_, Canad. J. Math. __46__(1994), 1027-1056 [doi](http://dx.doi.org/10.4153/CJM-1994-059-8)

* Lev Vasil&#697;evich Sabinin, _Smooth quasigroups and loops: forty-five years of incredible growth_, Commentationes Mathematicae Universitatis Carolinae __41__ (2000), No. 2, 377--400 [cdml](http://dml.cz/dmlcz/119171) [pdf](http://dml.cz/dmlcz/119171)

See also:

* Wikipedia, *[Loops](https://en.wikipedia.org/wiki/Quasigroup#Loops)*