
> This entry is about the concept in [[order theory]]. For the concept in [[analytic geometry]] see at *[[direction of a vector]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea and terminology

A **direction** on a set $S$ is a [[preorder]] on $S$ in which any finite subset has an [[upper bound]].  A **directed set** is a [[set]] equipped with a direction.  A **directed poset** is a directed set whose preorder is a [[partial order]] (so _directed proset_ might be a better term than _directed set_). Note that many authors by directed set mean directed poset.

Directedness is an asymmetric condition.  Sometimes a direction as defined here is called **upward-directed**; a preorder whose [[opposite category|opposite]] is upward-directed is called **downward-directed** or **codirected**.

A [[subset]] of a poset (or proset) which is a directed set (when regarded as a poset in its own right) is a **directed subset**, and dually.  More generally, a [[diagram]] in a [[category]] whose domain is a directed set (when regarded as a [[thin category]]) is called a **directed diagram**, and dually.


## Definitions

### Finitely directed set 

+-- {: .num_defn}
###### Definition

A **finitely upward-directed set** (which is the default notion) is a [[set]] with a [[preorder]] $\leq$ such that:

1. there exists an element (so the set is [[inhabited set|inhabited]]); and

2. given elements $x, y$, there exists an element $z$ such that $x \leq z$ and $y \leq z$.

=--

It follows that, given any [[finite set]] $x_1, \dots, x_n$ of elements, there exists an element $z$ such that $x_i \leq z$ for all $i$. 

(For [[constructive mathematics|constructive]] purposes, one should interpret 'finite set' above as a [[finite set|finitely indexed set]], as shown.)

Equivalently, this says: 

+-- {: .num_defn}
###### Definition

A directed set is a [[proset]] which is a [[filtered category]]: a **filtered [[(0,1)-category]].

=--


In analogy with the definition there, we can provide an [[biased definition|unbiased definition]] that is also commonly used in the literature:

+-- {: .num_defn}
###### Definition

A directed set is a [[proset]] in which every finite subset has an upper bound.

=--

### Higher cardinality

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-directed set** is equipped with a preorder $\leq$ such that, given any index set $A$ with $|A| \lt \kappa$ and function $i \mapsto x_i$ from $A$, there exists an element $z$ such that $x_i \leq z$ for all $i$. Then a finitely directed set is the same as an $\aleph_0$-directed set.  An **infinitely directed set** allows any index set $A$ whatsoever, but this reduces to the statement that the proset has a [[top]] element.


## Remarks

Directions on the [[real line]] are quite interesting: 

[Beardon 1997](#Beardon97) develops [[infinitesimal calculus|ordinary calculus]] rigorously from scratch using directions, and [Markov 1996](#Markov96) generalizes interval arithmetic to arithmetic on directions.

As a partially ordered set is a special kind of [[category]], so a (finitely) directed set is such a category in which all (finite) diagrams admit a [[cocone]].  If the category actually has finite coproducts (equivalently, all finite colimits), then it has all [[joins]] and so is a join-[[semilattice]].  (In particular, every join-semilattice is a directed set.)

Directed sets are heavily used in point-set [[topology]] and [[analysis]], where they serve as index sets for [[nets]] (aka Moore--Smith sequences).  In this application, it is important that a direction need not be a partial order, since a net need not preserve the preorder in any way but by default still preserves [[equality]].  (But in principle, one could force a directed set to be a poset by allowing a net to be a [[multi-valued function]]; this has practical consequences for the meaning of [[sequence]] in the absence of [[countable choice]].)

[[join|Joins]] over directed index sets are [[directed joins]]; [[colimits]] over directed index sets are [[directed colimits]].  These play an important role in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories; see also [[filtered category]].

## References

* {#Beardon97}  Alan F. Beardon: *Limits -- A New Approach to Real Analysis*, Springer (1997) &lbrack;[doi:10.1007/978-1-4612-0697-2](https://doi.org/10.1007/978-1-4612-0697-2)&rbrack;

* {#Markov96} Svetoslav Markov: *On directed interval arithmetic and its applications*, in: *J.UCS The Journal of Universal Computer Science*, Springer (1996) 514-526 &lbrack;[doi:10.1007/978-3-642-80350-5_43](https://doi.org/10.1007/978-3-642-80350-5_43)&rbrack;




[[!redirects direction]]
[[!redirects directions]]

[[!redirects directed set]]
[[!redirects directed sets]]
[[!redirects directed poset]]
[[!redirects directed posets]]
[[!redirects directed proset]]
[[!redirects directed prosets]]

[[!redirects directed subset]]
[[!redirects directed subsets]]
[[!redirects directed diagram]]
[[!redirects directed diagrams]]

[[!redirects codirection]]
[[!redirects codirections]]
[[!redirects co-direction]]
[[!redirects co-directions]]
[[!redirects codirected set]]
[[!redirects codirected sets]]
[[!redirects co-directed set]]
[[!redirects co-directed sets]]
[[!redirects codirected poset]]
[[!redirects codirected posets]]
[[!redirects co-directed poset]]
[[!redirects co-directed posets]]
[[!redirects codirected proset]]
[[!redirects codirected prosets]]
[[!redirects co-directed proset]]
[[!redirects co-directed prosets]]
[[!redirects codirected subset]]
[[!redirects codirected subsets]]
[[!redirects co-directed subset]]
[[!redirects co-directed subsets]]
[[!redirects codirected diagram]]
[[!redirects codirected diagrams]]
[[!redirects co-directed diagram]]
[[!redirects co-directed diagrams]]

[[!redirects upward direction]]
[[!redirects upward directions]]
[[!redirects upward-direction]]
[[!redirects upward-directions]]
[[!redirects upward directed]]
[[!redirects upward-directed]]
[[!redirects upward directed set]]
[[!redirects upward directed sets]]
[[!redirects upward-directed set]]
[[!redirects upward-directed sets]]
[[!redirects upward directed poset]]
[[!redirects upward directed posets]]
[[!redirects upward-directed poset]]
[[!redirects upward-directed posets]]
[[!redirects upward directed proset]]
[[!redirects upward directed prosets]]
[[!redirects upward-directed proset]]
[[!redirects upward-directed prosets]]
[[!redirects upward directed subset]]
[[!redirects upward directed subsets]]
[[!redirects upward-directed subset]]
[[!redirects upward-directed subsets]]
[[!redirects upward directed diagram]]
[[!redirects upward directed diagrams]]
[[!redirects upward-directed diagram]]
[[!redirects upward-directed diagrams]]

[[!redirects downward direction]]
[[!redirects downward directions]]
[[!redirects downward-direction]]
[[!redirects downward-directions]]
[[!redirects downward directed]]
[[!redirects downward-directed]]
[[!redirects downward directed set]]
[[!redirects downward directed sets]]
[[!redirects downward-directed set]]
[[!redirects downward-directed sets]]
[[!redirects downward directed poset]]
[[!redirects downward directed posets]]
[[!redirects downward-directed poset]]
[[!redirects downward-directed posets]]
[[!redirects downward directed proset]]
[[!redirects downward directed prosets]]
[[!redirects downward-directed proset]]
[[!redirects downward-directed prosets]]
[[!redirects downward directed subset]]
[[!redirects downward directed subsets]]
[[!redirects downward-directed subset]]
[[!redirects downward-directed subsets]]
[[!redirects downward directed diagram]]
[[!redirects downward directed diagrams]]
[[!redirects downward-directed diagram]]
[[!redirects downward-directed diagrams]]
