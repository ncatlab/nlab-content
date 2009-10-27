This page develops a theory of universes in the [[structural set theory]] called [[SEAR]], parallel to the theory of [[Grothendieck universes]] for [[ZF]] and the theory of a [[universe in a topos]].  See also [[categories in SEAR]].

+--{: .query}
[[David Roberts]]: Can we talk about Grothendieck universes or analogous size-related mechanisms? (this is a naive question, since there may be (no need for/obvious way to do) this in a structural set theory that I am unaware of.

[[Mike Shulman]]: Universes can be defined in any structural set theory in a fairly straightforward way, modulo the usual translation from "set of sets" to "family of sets."  There is some stuff from a more ETCS-like perspective at [[universe in a topos]]; I'm sure that this can be rephrased in SEAR (if you want to take a shot, feel free!).

[[David Roberts]]: I'd certainly like to, subject to real-world time constraints. It seems to me that something could be done to the axiom of collection if we had a axiom of universes (for every set there is a universe acting as a universal family for it, or similar).

[[Mike Shulman]]: I'm not sure that Collection can really be eliminated using universes, but maybe it can.
=--

## Using families

+--{: .query}
[[David Roberts]]: Some sketchy thoughts - a universe will be a relation $U \looparrowright E$ satisfying axioms analogous to those at [[universe in a topos]]. There are few points that need translating into SEAR-language first so we can define smallness of a family of sets $I \looparrowright A$

* Pullback - unless I am mistaken, the appropriate version is this: Given a function $I \to U$, the family $I \looparrowright E$ should be regarded as the \'pullback\' family. This family should be isomorphic to the family $I \looparrowright A$. This leads us to wonder how to define two families to be isomorphic.

* Dependent product - this is tricker and I'm not going to do that right now. 
=--

Fix a family of sets $U \looparrowright E$.

**Definition:** A family $a:I \looparrowright A$ is called _$U$-small_ if there is a function $f:I \to U$ such that for the composite relation $I \looparrowright E$ ...

A set $A$ is called $U$-small if the relation $\mathbf{1}\looparrowright A$, which holds of $*$ and $a$ for all elements $a$ of $A$, is a $U$-small family.

For ease of language, we define a composite of families to be the composite relation of the two relations defining the families.

**Definition:** A family of sets $U \looparrowright E$ is called a _universe_ if the following axioms are satisfied:

* The composite of two $U$-small families is $U$-small
* The relation $f^o:B\looparrowright A$ opposite to an injective function $f:A \to B$ is a $U$-small family
* $P\mathbf{1}$ is a $U$-small set
* (Something about dependent products, once these are defined)

There is an optional axiom, given the axiom of infinity from before:

* The [[natural numbers object]] is a $U$-small set

Without this axiom we do not have that universes contain infinite sets.
  
Given a universe $U \looparrowright E$, we want to define a (meta-)category $U-Set$...


## Using mere sets

+--{: .query}
[[Mike Shulman]]: The main idea of SEAR is that in a well-pointed topos, global elements suffice for everything.  In particular, we can usually dispense with families of things and consider only single ones.  So here's a formulation that I think is more in the spirit of SEAR.
=--

Given a family $E:U\looparrowright X$, recall that for $u\in U$ we let $E_u$ be a tabulation of $\{x\in X | E(u,x) \}\subseteq X$.  We say that a set $A$ is **$U$-small** (although really, it would be more appropriate to say "$E$-small") if there exists a $u\in U$ with $A\cong E_u$.  Now we say that $U$ (equipped with $E$) is a **universe** if it satisfies:

* There exists an inhabited $U$-small set.
* The tabulation of any relation between two $U$-small sets is $U$-small.
* If $A$ is $U$-small, then so is $P A$.
* (Replacement) If $f:A\to B$ is a function such that $B$ is $U$-small and for each $b\in B$, the set $f^{-1}(b)$ is $U$-small, then $A$ is $U$-small.
* (Collection) If $p:B\twoheadrightarrow A$ is a surjective function where $A$ is $U$-small, then there exists a $U$-small set $C$, a surjection $q:C\twoheadrightarrow A$ and a function $f:C\to B$ such that $q = p\circ f$.

The optional axiom is the same:

* There exists an infinite $U$-small set (in the sense of Axiom 4).

The first two properties of a universe clearly imply that the $U$-small sets satisfy Axioms 0--2 of SEAR all by themselves.  In particular, $\emptyset$ and $1$ are $U$-small, any subset of a $U$-small set is $U$-small, and if $A$ and $B$ are small then so is $A\times B$.  Thus from the additional assumption of the smallness of powersets, we can conclude that if $A$ and $B$ are small, so is the set $B^A$ of functions from $A$ to $B$.  It also follows that coproducts and quotient sets preserve smallness.  (For a notion of "predicative universe" we would replace the smallness of powersets with the smallness of function sets, and we might have to separately assume smallness of coproducts and quotients, I'm not sure.)

In order to show that the $U$-small sets model SEAR all by themselves, it remains to show:

+-- {: .num_theorem #univ-coll}
###### Theorem
The $U$-small sets for a universe $U$ satisfy the Collection axiom of SEAR.
=--
+--{: .proof}
###### Proof
Let $A$ be a $U$-small set and $P$ a property as in the Collection axiom.  Let $P'$ be a property such that $P'(a,X)$ holds iff $P(a,X)$ holds *and* $X$ is $U$-small.  By the Collection axiom for all sets applied to $P'$, there exists a set $B$, a function $p:B\to A$, and a $B$-indexed family of sets $M:B\looparrowright Y$ satisfying the desired properties: (1) for any $b\in B$, we have $P(p(b),M_b)$ *and* $M_b$ is $U$-small, and (2) for any $a\in A$, if there exists a $U$-small set $X$ with $P(a,X)$, then $a\in im(p)$.  Our goal is to replace $B$ and $Y$ by $U$-small sets $B'$ and $Y'$ with a relation $M':B'\looparrowright Y'$ maintaining the truth of these statements.

Now the induced function $\overline{p}:B\to im(p)$ is surjective, and since $im(p)$ is a subset of $A$ it is $U$-small.  Thus, by the "Collection" property of a universe, there exists a $U$-small set $C$, a surjection $q:C\twoheadrightarrow im(p)$ and a function $f:C\to B$ such that $q = \overline{p} \circ f$.  We take $B'=C$ and the composite $C \to im(p)\to A$ as the function $p'$; we claim that the composite relation $M\circ f$ still satisfies (1) and (2) above.  (We have not replaced $Y$ yet, so this is still an intermediate step.)  Property (1) follows since $p'(c) = p(f(c))$ and $(M\circ f)_c \cong M_{f(c)}$, while property (2) follows since $im(p) = im(p')$ by construction.

Now consider a tabulation $B' \overset{r}{\leftarrow} Z \overset{s}{\to} Y$ of $M\circ f$.  Note that for any $b\in B'$ we have $r^{-1}(b) \cong (M\circ f)_b$, and therefore in particular $r^{-1}(b)$ is $U$-small by (1).  Since $B'$ is also $U$-small, the "Replacement" property of a universe implies that $Z$ is also $U$-small.  But the family $r^o:B'\looparrowright Z$ is equivalent to $M\circ f$, in the sense that $(r^o)_b \cong (M\circ f)_b$ for all $b\in B'$, so it also satisfies (1) and (2); thus we can take $Y'=Z$ and $M'=r^o$.
=--

Note that both the "Replacement" and "Collection" properties of a universe are required to show the SEAR Collection axiom for $U$-small sets.  The naming of these two properties appears to be traditional, however.  See in particular the book _Algebraic Set Theory_ by Joyal and Moerdijk.

What about families and dependent products?  We define a function, considered as a family of sets, to be **$U$-small** if each of its fibers is.  Note that then we can state the Replacement property as "the composite of $U$-small functions is $U$-small."  Now for functions $g:C\to B$ and $f:B\to A$, the fiber of the dependent product $\Pi_f g$ over $a\in A$ is the subset of the function set $\Big((f g)^{-1}(a)\Big)^{f^{-1}(a)}$ consisting of functions $s: f^{-1}(a) \to (f g)^{-1}(a)$ such that $g\circ s = \id$.  Thus, if $f$ and $g$ are $U$-small, so is $f g$ (by the "Replacement" property), and thus so is this fiber.  Hence $U$-small functions are closed under dependent products.

Also of interest is the following, which should be compared to the "descent" axiom in Joyal-Moerdijk.

+-- {: .num_theorem #univ-descent}
###### Theorem
The following are equivalent for a function $f:B\to A$.
1. $f$ is $U$-small.
1. There exist a surjection $p:C\to A$ and a function $g:C\to U$ and two pullback squares
$$\array{B &\overset{q}{\leftarrow} & P & \overset{k}{\to} & {|E|}\\
  ^f\downarrow && \downarrow^j && \downarrow\\
  A &\underset{p}{\twoheadleftarrow} & C & \underset{g}{\to} & U}$$
1. (If the axiom of choice holds) There exists a function $g:A\to U$ and a pullback square
$$\array{B & \overset{}{\to} & {|E|}\\
  ^f\downarrow && \downarrow\\
  A & \underset{g}{\to} & U}$$
=--
+--{: .proof}
###### Proof
Clearly the third condition implies the second.  The second implies the first, since pullbacks have isomorphic fibers.  And in the presence of AC, the second implies the third, since the surjection $p$ has a section.  Thus the difficulty is in showing that the first implies the second.

Suppose that $f:B\to A$ is $U$-small.  This means that for any $a\in A$, there exists a $u\in U$ and a bijection $f^{-1}(a)\cong E_u$.  Let $C$ be the subset of $A\times U\times P(B\times |E|)$ consisting of those triples $(a,u,h)$ such that $h$ is a bijection $f^{-1}(a) \overset{\cong}{\to} E_{u}$, and let $p:C\to A$ and $g:C\to U$ be the projections.  Since $f$ is $U$-small, $p$ is surjective.  Define $P$ to be a pullback of $f$ along $p$, with projections $q:P\to B$ and $j:P\to C$, and define $k:P\to {|E|}$ by (informally speaking) $k(x) = h(q(x))$ where $j(x) = (a,u,h)$.  Since each $h$ is a bijection, $k$ makes $P$ a pullback of ${|E|}$.
=--
