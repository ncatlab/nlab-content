
# Positive cones
* table of contents
{: toc}

## Idea

Geometrically, the positive elements of a [[vector space]] with a [[partial order]] form a [[cone]], called the positive cone.  The concept makes sense even more generally but is particularly important in [[operator algebras]].


## Definition

Let $V$ be a [[partially ordered set]] and let $0$ be an [[element]] of $V$.  Then the __positive cone__ $V^+$ of the pointed poset $(V,0)$ is the [[up set]] of $0$:
$$ V^+ \coloneqq \{x\colon V \;|\; 0 \leq x\} .$$

If $V$ is an [[operator algebra]], or more generally an [[ordered group]], then we use the usual [[identity element]] $0$ here.


## Properties

Let $V$ be an [[ordered group]]; that is, $V$ is a poset (as above) and also a [[group]] (written additively but not necessarily [[abelian group|commutative]]) with this compatibility property:

*  If $a \leq b$, then $a + c \leq b + c$ and $c + a \leq c + b$.

Then the positive cone $V^+$ satisfies these properties:

*  If $a, -a \in V^+$ (where $-a$ is the [[inverse element|inverse]] of $a$), then $a = 0$;
*  Conversely, $0 \in V^+$;
*  If $a, b \in V^+$, then $a + b \in V^+$;
*  If $a \in V^+$, then $b + a - b \in V^+$ (which is trivial if $V$ is commutative).

Conversely, if $V^+$ is any subset of the group $V$ with these properties, then $V$ becomes an ordered group with either of these equivalent definitions:

*  $a \leq b$ iff $b - a \in V^+$,
*  $a \leq b$ iff $-a + b \in V^+$.

In this way, we have a [[bijection]] between ordered group structures and positive cones in a group.


## The extended positive cone

+-- {: .un_remark}
###### Motivation

The [[finite measures]] on a given [[measurable space]] form an ordered vector space $V$, and the positive cone $V^+$ consists precisely of the finite [[positive measures]].  But we often want to allow positive measures to take infinite values.  The space of (possibly infinite) positive measures is the _extended_ positive cone of $V$.
=--

I only know the general definition in some rather limited cases:

+-- {: .num_defn}
###### Definition (positive cone of a von Neumann algebra)

Let $V$ be a $W^*$-[[W-star-algebra|algebra]], and let $V_*$ be its [[predual]].  Recall that $V$ is the space of [[continuous map|continuous]] [[linear maps]] from $V_*$ to the [[base field]].  The __extended positive cone__ $\bar{V}^+$ of $V$ is the space of lower [[semicontinuous map|semicontinuous]] linear maps from the positive cone $V_*^+$ of $V_*$ to the space $\bar{\mathbb{R}}^+ = [0,\infty]$ of [[extended real number|extended]] positive [[real numbers]].
=--

The extended positive real numbers are really showing up in their guise as the nonnegative [[lower real numbers]] (the appropriate targets for a lower semicontinuous map), and the extended positive cone is really a generalisation of the nonnegative upper reals.  In particular, the extended positive cone of $\mathbb{R}$ itself is $[0,\infty]$.

This doesn\'t include the motivating example, but the following generalisation does:

+-- {: .num_defn}
###### Definition (positive cone of an ordered module over a von Neumann algebra)

Let $V$ be a [[module]] over the $W^*$-algebra $A$, and let $V$ have the structure of an ordered group such that the action of $A$ preserves order (in that a positive element acting on a positive element gives a positive element).  Then the __extended positive cone__ $\bar{V}^+$ of $V$ consists of formal infinitary $\bar{A}^+$-[[linear combination]]s of positive elements of $V$ modulo the (hopefully) obvious [[equivalence relation]].
=--

When applied to the space of finite measures on a [[localisable measurable space]] $X$ (acted on by the $W^*$-algebra $L^\infty(X)$), this should give the positive measures on $X$ (but I need to check the details).


## References

The extended positive cone of a $W^*$-algebra is Definition 4.4 of:

*  [[Masamichi Takesaki]], Theory of Operator Algebras II, Springer; [Google books](http://books.google.com/books?id=-4GyR1VlQz4C&pg=PA215&dq="extended+positive+part").


[[!redirects positive cone]]
[[!redirects positive cones]]

[[!redirects extended positive cone]]
[[!redirects extended positive cones]]
[[!redirects extended positive part]]
[[!redirects extended positive parts]]
