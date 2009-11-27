
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **direction** on a set $S$ is a [[preorder]] on $S$ in which any (finite) set of elements has a common upper bound.  A **directed set** is a set equipped with a direction.

Directedness is an asymmetric condition.  Sometimes a direction as defined here is called **upward-directed**; a preorder whose [[opposite category|opposite]] is upward-directed is called **downward-directed**.  Another term for downward-directed is **codirected**.


## Definitions

### Finitely directed set 

To be explicit, a **finitely upward-directed set** (which is the default notion) is equipped with a [[preorder]] $\leq$ such that:
* there exists an element (so the set is [[inhabited set|inhabited]]); and
* given elements $x, y$, there exists an element $z$ such that $x \leq z$ and $y \leq z$.

It follows that, given any finite set $x_1, \dots, x_n$ of elements, there exists an element $z$ such that $x_i \leq z$ for all $i$. (For [[constructive mathematics|constructive]] purposes, one should interpret 'finite set' above as a [[finite set|finitely indexed set]], as shown.)

### $\kappa$-directed set

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-directed set** is equipped with a preorder $\leq$ such that, given any index set $A$ with $|A| \lt \kappa$ and function $i \mapsto x_i$ from $A$, there exists an element $z$ such that $x_i \leq z$ for all $i$. Then a finitely directed set is the same as an $\aleph_0$-directed set.  An **infinitely directed set** allows any index set $A$ whatsoever, but this reduces to the statement that the proset has a [[top]] element.


## Remarks

Directions on the real line are quite interesting; there\'s a textbook that does ordinary calculus rigorously from scratch using directions (probably _LIMITS: A New Approach to Real Analysis_), and there\'s a paper generalising interval arithmetic to arithmetic on directions.

+--{.query}
Unfortunately, I cannot find the latter now.  ---Toby
=--

As a partially ordered set is a special kind of [[category]], so a (finitely) directed set is such a category in which all finite diagrams admit a cocone.  If the category actually has finite coproducts (equivalently, all finite colimits), then it has all [[join]]s and so is a join-[[semilattice]].  (In particular, every join-semilattice is a directed set.)

Directed sets are heavily used in point-set topology and analysis, where they serve as index sets for [[net|nets]] (aka Moore--Smith sequences).  In this application, it is important that a direction need not be a partial order, since a net need not preserve the preorder in any way but by default still preserves [[equality]].  (But in principle, one could force a directed set to be a poset by allowing a net to be a [[multi-valued function]]; this has practical consequences for the meaning of [[sequence]] in the absence of [[countable choice]].)

Colimits over directed index sets also play an important role in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories; see also [[filtered category]].


[[!redirects directed set]]
[[!redirects directed poset]]
[[!redirects directed proset]]
[[!redirects codirection]]
[[!redirects codirected set]]
[[!redirects codirected poset]]
[[!redirects codirected proset]]
[[!redirects co-direction]]
[[!redirects co-directed set]]
[[!redirects co-directed poset]]
[[!redirects co-directed proset]]
[[!redirects upward direction]]
[[!redirects upward directed set]]
[[!redirects upward directed poset]]
[[!redirects upward directed proset]]
[[!redirects upward-direction]]
[[!redirects upward-directed set]]
[[!redirects upward-directed poset]]
[[!redirects upward-directed proset]]
[[!redirects downward direction]]
[[!redirects downward directed set]]
[[!redirects downward directed poset]]
[[!redirects downward directed proset]]
[[!redirects downward-direction]]
[[!redirects downward-directed set]]
[[!redirects downward-directed poset]]
[[!redirects downward-directed proset]]
[[!redirects directions]]
[[!redirects directed sets]]
[[!redirects directed posets]]
[[!redirects directed prosets]]
[[!redirects codirections]]
[[!redirects codirected sets]]
[[!redirects codirected posets]]
[[!redirects codirected prosets]]
[[!redirects co-directions]]
[[!redirects co-directed sets]]
[[!redirects co-directed posets]]
[[!redirects co-directed prosets]]
[[!redirects upward directions]]
[[!redirects upward directed sets]]
[[!redirects upward directed posets]]
[[!redirects upward directed prosets]]
[[!redirects upward-directions]]
[[!redirects upward-directed sets]]
[[!redirects upward-directed posets]]
[[!redirects upward-directed prosets]]
[[!redirects downward directions]]
[[!redirects downward directed sets]]
[[!redirects downward directed posets]]
[[!redirects downward directed prosets]]
[[!redirects downward-directions]]
[[!redirects downward-directed sets]]
[[!redirects downward-directed posets]]
[[!redirects downward-directed prosets]]
