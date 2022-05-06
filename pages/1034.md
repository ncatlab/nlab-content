
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A **universe** in a [[topos]] is a [[topos theory|topos-theoretic]] version of the notion of [[Grothendieck universe]]; see that page for general motivation and applications.

To free the notion from membership-based set theory, we must replace _sets of sets_ by _families of sets_, just as in passing from [[power set]]s to [[power object]]s we must replace sets of subsets by families of subsets.


## Definition 

A **universe** in a topos $\mathcal{E}$ is a morphism $el\colon E \to U$ satisfying the axioms to follow.  We think of $el\colon E \to U$ as an $U$-indexed family of objects/sets (fibers of $el$ being those objects), and we define a morphism $a\colon A \to I$ (regarded as an $I$-indexed family of objects) to be **$U$-small** if there exists a morphism $f\colon I \to U$ and a [[pullback]] square
$$\array{A & \to & E\\
  ^a\downarrow && \downarrow^{el}\\
  I& \underset{f}{\to} & U.}
$$

The arrow $f$ is sometimes called the **name** of $a\colon A \to I$, since in the case when $I=*$, the arrow $f:* \to U$ _points_ at the term in the universe $U$ representing the object $A$. (See also this [discussion](http://nforum.ncatlab.org/discussion/6564/elementary-formulation-of-groupautomorphism-group/?Focus=53083#Comment_53083) and references there.) 

Note that $f$ is not, in general, unique: a universe can contain many isomorphic sets.  With this definition, the pullback of a $U$-small morphism is automatically again $U$-small.  We say that an object $X$ is $U$-small if $X\to 1$ is $U$-small.

The axioms which must be satisfied are:

1. Every [[monomorphism]] is $U$-small.

2. The composite of $U$-small morphisms is $U$-small.

3. If $f\colon A \to I$ and $g\colon B \to A$ are $U$-small, then so is the [[dependent product]] $\Pi_f g$ (where $\Pi_f$ is the right adjoint to $f^*\colon \mathcal{E}/I \to \mathcal{E}/A$).

4. The [[subobject classifier]] $\Omega$ is $U$-small.

Note that since $0\to \Omega$ is a monomorphism, (1) and (4) imply that the [[initial object]] $0$ is $U$-small.  A _[[predicative mathematics|predicative]] universe_ is a morphism $el\colon E \to U$ where instead of (4) we assume merely that $0$ is $U$-small; this makes sense in any [[locally cartesian closed category]].  In a topos, the generic subobject $1\to \Omega$ is a predicative universe, and of course a morphism is $\Omega$-small if and only if it is a monomorphism.

If we assume only (1)--(3), then the identity morphism $1_0\colon 0 \to 0$ of the initial object would be a universe, for which it itself is the only $U$-small morphism.  On the other hand, if $\mathcal{E}$ has a [[natural numbers object]] $N$, we may additionally assume that $N$ is $U$-small, to ensure that all universes contain "infinite" sets.

Note that any object isomorphic to a $U$-small object is $U$-small; thus in the language of [[Grothendieck universe]]s this notion of smallness corresponds to _essential_ smallness.  Roughly, we may say that (1) corresponds to transitivity of a Grothendieck universe, (3) and (4) correspond to closure under power sets, and (2) corresponds to closure under indexed unions.


## Example: universes in $SET$

We spell out in detail some implications of these axioms for the case
that the [[topos]] in question is the Categeory of Sets according to 
[[ETCS]], to be denoted $SET$.

Write $*$ for [[generalized the|the]] 
[[terminal object]] in $SET$, the singleton set. Notice that for each
ordinary element $u \in U$, i.e. $* \stackrel{u}{\to} U$, there is the
set $E_u $ over $u$, defined as the [[pullback]] 
$$\array{
  E_u &\to& E
  \\
  \downarrow && \downarrow
  \\
  * &\stackrel{u}{\to}& U
}$$

We think of $E$ as being the disjoint union over $U$ of the $E_u$.  In the language of indexed categories, this is precisely the case: the object $E\in SET$ is the indexed coproduct of the $U$-indexed family $(E\to U) \in SET/U$.

* By the definition of $U$-smallness and the notation just introduced, 
an object $S$ in $SET$, regarded as a $*$-indexed family
$S \to *$, is $U$-small precisely if it is isomorphic to 
one of the $E_u$.

* If $S$ is a $U$-small set by the above and if 
$S_0 \hookrightarrow S$ is a [[monomorphism]] so that $S_0$
is a subset of $S$, it follows from 1) and 2) that the comoposite 
$(S_0 \hookrightarrow S \to *) = (S_0 \to *)$ is $U$-small, hence that
$S_0$ is $U$-small. So: a subset of a $U$-small set is $U$-small.

  * In particular, let $\emptyset$ be the [[initial object]], which is
  a subset $\emptyset \hookrightarrow \Omega$ of $\Omega = \mathbf{2}$. So: the 
  empty set is $U$-small.
  
* Let $S$, $T$ and $K$ be objects of $SET$, regarded as $*$-indexed families
$f\colon S \to *$, $T \to *$ and $K \to *$. Notice that 
$(SET\downarrow S)(f^* K, f^* T) \simeq (SET\downarrow S)(\array{K \times S \\ \downarrow^{p_2} \\ S}, \array{T \times S \\ \downarrow^{p_2} \\ S})$
is canonically isomorphic to $SET(K \times S, T)$. Since $\Pi_f$ is 
defined to be the [[right adjoint]] to $f^*\colon SET \to SET \downarrow S$
it follows that $\Pi_f f^* T \simeq T^S$  is the function set of functions
from $S$ to $T$. By 3), if $S$, $T$ are $U$-small then so is 
the function set $T^S$.

  * Since by 4) $\Omega = \mathbf{2}$ is $U$-small and for every $S$ the function
  set $\mathbf{2}^S \simeq P(S)$ is the power set of $S$, it follows that
  the power set of a $U$-small set is $U$-small.
  
 
* Let $I$ be a $U$-small set, in that $I \to *$ is $U$-small, and let 
$S \to I$ be $U$-small, to be thought of as an $I$-indexed family of
$U$-small sets $S_i$, where $S_i$ is the [[pullback]] $\array{
  S_i &\to& S
  \\
  \downarrow && \downarrow
  \\
  * &\stackrel{i}{\to}& I
}$, so that $S$ is the disjoint union of the $S_i$: $S = \bigsqcup_{i \in I} S_i$.
By axiom 2) the composite morphism $(S \to I \to *) = (S \to *)$ is $U$-small,
hence $S$ is a $U$-small set, hence the $I$-indexed union of $U$-small sets
$\bigsqcup_{i \in I} S_i$ is $U$-small.

By standard constructions in [[set theory]] from these
properties the following further closure properties of the universe $U$
follow.

* For $I$ a $U$-small set and $S \to I$ an $I$-indexed family of
$U$-small sets $S_i$, the cartesian product $\prod_{i \in I} S_i$
is $U$-small, as it is a subset of $P(I \times S)$.


In **summary**

* the sets $\emptyset, *, \mathbf{2}$ are $U$-small;

* a subset of a $U$-small set is $U$-small;

* the power set $P(S)$ of any $U$-small set is $U$-small;

* the function set $T^S$ for any two $U$-small sets is $U$-small;

* the [[coproduct|union]] of a $U$-small family of $U$-small sets is $U$-small.

* the [[product|product]] of a $U$-small family of $U$-small sets is $U$-small.


## Axioms of universes 

Just as [[ZFC]] and other material [[set theory|set theories]] may be augmented with axioms guaranteeing the existence of [[Grothendieck universe]]s, so may [[ETCS]] and other structural set theories be augmented with axioms guaranteeing the existence of universes in the above sense.  For example, the counterpart of Grothendieck's axiom

* For every set $s$ there exists a universe $U$ containing $s$, i.e. $s\in U$

would be

* For every morphism $a\colon A \to I$ in $\mathcal{E}$, there exists a universe $el\colon E \to U$ such that $a$ is $U$-small.


## Consequences 

One can show, from the above axioms, that the $U$-small morphisms are closed under finite [[coproduct]]s and under [[quotient object]]s.  See the reference below.


## In terms of indexed categories 

Recall that an $\mathcal{E}$-[[indexed category]] is a [[pseudofunctor]] $\mathcal{E}^{op}\to \Cat$.  The fundamental $\mathcal{E}$-indexed category is the _self-indexing_ $\mathbb{E}$ of $\mathcal{E}$, which takes $I\in \mathcal{E}$ to the [[over category|slice category]] $\mathbb{E}^I = \mathcal{E}/I$ and $x\colon I \to J$ to the [[base change]] functor $x^*$.

An **internal full subcategory** of $\mathcal{E}$ is a full sub-indexed category $\mathbb{F}$ of $\mathbb{E}$ (that is, a collection of full subcategories $\mathbb{F}^I\subset \mathbb{E}^I$ closed under reindexing) such that there exists a generic $\mathbb{F}$-morphism, i.e. a morphism $el\colon E \to U$ in $\mathbb{F}^U$ such that for any $a\colon A \to I$ in $\mathbb{F}^I$, we have $a \cong f^*(el)$ for some $f\colon I \to U$.  In this case (since $\mathcal{E}$ is [[locally cartesian closed category|locally cartesian closed]]) there exists an [[internal category]] $U_1 \;\rightrightarrows\; U$ in $\mathcal{E}$ such that $\mathbb{F}$ is equivalent, as an indexed category, to the indexed category represented by $U_1 \;\rightrightarrows\; U$.

An internal full subcategory is an **internal full subtopos** if each $\mathbb{F}$ is a [[logical functor|logical]] subtopos of $\mathbb{E}$ (closed under finite limits, exponentials, and containing the subobject classifier).  A universe in $\mathcal{E}$, as defined above, can then be identified with an internal full subtopos satisfying the additional axiom that $U$-small morphisms are closed under composition.


## In the internal logic 

In a topos with a universe, we can talk about small objects in the [[internal logic]] by instead talking about elements of $U$.  We can then rephrase the axioms of a universe in the internal logic to look more like the usual axioms for a Grothendieck universe, with the morphism $el\colon E \to U$ interpreted as a "family of objects"  $(S_u)_{u\colon U}$:

1. for all $u$ in $U$, if $X$ is a [[subset]] of $S_u$ (in the sense that there exists an [[injection]] $X \embedsin S_u$), then there is a $v$ in $U$ such that $X \cong S_v$;
2. for all $u$ in $U$, there is a $v$ in $U$ such that the [[power set]] $P(S_u) \cong S_v$;
3. there is a $v$ in $U$ such that $S_v$ is [[empty set|empty]];
4. for all $u$ in $U$ and all functions $f\colon S_u \to U$, there is a $v$ in $U$ such that the [[disjoint union]] $\biguplus_{i\colon S_u} S_{f(i)} \cong S_v$.

In a [[well-pointed topos]], such as a model of [[ETCS]], these "internal" axioms are equivalent to their "external" versions that refer to [[global element]]s of $U$.

+-- {: .query}
[[Mike Shulman|Mike]]: I haven't actually checked anything in this section, but it seems probable.
=--

## Related concepts

* [[type universe]]

* [[object classifier in an (infinity,1)-topos]]

* [[Grothendieck universe]]

## References 

The construction of universes in presheaf toposes was first discussed in the following short note which might serve as a concise introduction to the more general reference that follows:

* [[Martin Hofmann]], [[Thomas Streicher]], _Lifting Grothendieck Universes_ , ms. University of Darmstadt (unpublished). ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/NOTES/lift.pdf)) 

The general case is considered here:

* [[Thomas Streicher]], _Universes in Toposes_ , pp.78-90 in L. Crosilla, P. Schuster (eds.), _From Sets and Types to Topology and Analysis: Towards Practicable Foundations for Constructive Mathematics_ , Oxford UP 2005. ([ps](http://www.mathematik.tu-darmstadt.de/~streicher/NOTES/UniTop.ps.gz),[pdf](http://www.mathematik.tu-darmstadt.de/~streicher/NOTES/UniTop.pdf))

See also

* Christian Maurer, _Universes in Topoi_ , pp.285-296 in F. W. Lawvere, C. Maurer, G. C. Wraith (eds.), _Model Theory and Topoi_ , LNM **445** Springer Heidelberg 1975.


[[!redirects universe in a topos]]
[[!redirects universes in a topos]]
[[!redirects universes in toposes]]
[[!redirects universe in the topos]]
[[!redirects universes in the topos]]
[[!redirects universes in the toposes]]
[[!redirects internal full subcategory]]
[[!redirects internal full subcategories]]
[[!redirects internal full subtopos]]
[[!redirects internal full subtoposes]]
[[!redirects internal full subtopoi]]