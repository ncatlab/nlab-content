
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Final and initial lifts
* table of contents
{: toc}

## Definition

Let $U\colon C\to D$ be a [[functor]].

+-- {: .un_defn}
###### Definition
A **$U$-structured sink** is a [[sink]] of the form $\{f_i \colon U(A_i) \to Y\}$ in $D$.
=--

Note that like all sinks, a $U$-structured sink is not necessarily assumed to be [[small category|small]].

A **lift** of $Y$ along a $U$-structured sink $\{f_i\colon U(A_i)\to Y\}$ is an object $B$ of $C$, equipped with a sink $\{\phi_i\colon A_i \to B\}$ in $C$ and a morphism $h\colon Y\to U(B)$ in $D$, such that $U(\phi_i) = h \circ f_i$ for each $i$. A **morphism of lifts** is, of course, a morphism $\xi\colon B\to B'$ of $C$ such that the sink $\{\phi'_i\colon A_i\to B'\}$ factors through the sink $\{\phi_i\colon A_i\to B\}$ as $\phi_i'=\xi\circ\phi_i$, and such that the morphism $h'\colon Y\to U(B')$ factors through the morphism $h\colon Y\to U(B)$ as $h'=p(\xi)\circ h$.

Note that if $U$ is faithful, then it suffices to demand merely that the sink $\{\phi_i\colon A_i \to B\}$ exists, rather than giving it as part of the structure.

+-- {: .un_defn}
###### Definition
A **semi-final lift** of $\{f_i \colon U(X_i) \to Y\}$ is a lift $B$ of $Y$ admitting a unique morphism of lifts to any other lift of $Y$.  If the morphism $h\colon Y\to U(B)$ is an isomorphism, then the semi-final lift is called a **final lift**.  If $h$ is an identity, we call $B$ a **strictly final lift**.
=--

If objects of $C$ are regarded as objects of $D$ equipped with [[stuff, structure, property|structure]], for a (strictly) final lift we say that $B$ is the **final structure** or **strong structure** on $Y$ induced by the sink.  Note that if $U$ is an [[isofibration]], then any final lift may be made into a strictly final one.

The dual concept, which applies to cosinks ("sources"), is called a (perhaps semi- or strictly) **initial lift**, an **initial structure** or a **weak structure**.


## Examples

* If $D$ is the [[terminal category]], then a $U$-structured sink is simply a family of objects $A_i$ of $C$, a lift is just a cocone $A_i\to B$, a morphism of lifts is a morphism of cocones, hence a semi-final lift is simply a [[colimit]] in $C$.

* An empty $U$-structured sink is just an object $Y$ of $D$, a lift of it is a morphism $Y\to U(B)$, and a morphism of lifts is a morphism $B\to B'$ so that $Y\to U(B')$ factors as $Y\to U(B)\to U(B')$. Hence, a semi-final lift of such a sink is a [[free object]] with unit morphism $h\colon Y\to U(B)$ of $D$.  Thus $U$ admits semi-final lifts of empty sinks precisely when it has a [[left adjoint]].  Similarly, it admits final lifts of empty sinks precisely when it has a [[fully faithful functor|fully faithful]] left adjoint (i.e. if it admits [[discrete objects]]).

* A singleton $U$-structured sink is just a morphism of the form $f\colon U(X) \to Y$.  A strictly final lift of such a sink is precisely an [[opcartesian arrow]] lying over $f$.  Thus $U$ admits strictly final lifts of singleton structured sinks precisely when it is a [[Grothendieck opfibration]] (and final lifts of such sinks precisely when it is a [[Street opfibration]]).

* A [[topological concrete category]] is a functor that admits final lifts of *all* (not necessarily small) structured sinks.  This turns out to be equivalent to admitting initial lifts of all structured cosinks.  The most famous example is then [[initial topology|initial topologies]] and [[final topology|final topologies]] for $U\colon Top \to Set$.

* More generally, a [[solid functor]] is one that admits *semi-final* lifts of all structured sinks.

* If $U$ has both a left and right adjoint, of which one (and hence also the other) is fully faithful, and $C$ is cocomplete, then $U$ admits final lifts of all *small* structured sinks.  See [[adjoint triple]] for a proof.  Dually, if $C$ is complete in this situation, then $U$ admits initial lifts of all small structured cosinks.

## Remarks

* (Semi-)final lifts can be generalized to *(semi-)final extensions*, which are to (semi-)final lifts as [[Kan extensions]] are to [[colimits]].

* In [[Higher Topos Theory]] (section 4.3.1) the corresponding notion of (strictly) *final lift* for [[(∞,1)-categories]] is called a *$U$-colimit*.

[[!redirects final lift]]
[[!redirects final lifts]]
[[!redirects semi-final lift]]
[[!redirects semi-final lifts]]
[[!redirects semifinal lift]]
[[!redirects semifinal lifts]]
[[!redirects strictly final lift]]
[[!redirects strictly final lifts]]
[[!redirects final structure]]
[[!redirects final structures]]
[[!redirects strong structure]]
[[!redirects strong structures]]

[[!redirects initial lift]]
[[!redirects initial lifts]]
[[!redirects semi-initial lift]]
[[!redirects semi-initial lifts]]
[[!redirects semiinitial lift]]
[[!redirects semiinitial lifts]]
[[!redirects strictly initial lift]]
[[!redirects strictly initial lifts]]
[[!redirects initial structure]]
[[!redirects initial structures]]
[[!redirects weak structure]]
[[!redirects weak structures]]
