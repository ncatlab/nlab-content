
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _weak model categories_ is a relaxation of that of [[model categories]], even weaker than the concept of [[semimodel categories]], but such that it still allows for a rich theory largely analogous to that of actual [[model categories]]: 

The weak analogue of the construction of the [[homotopy category of a model category]] still exists, as do notions of [[Quillen adjunction]] and [[Quillen equivalence]].

Also, for example, an analogue of left or right _[[Bousfield localization of model categories]]_ still makes sense for weak model categories; and, as a bonus in contrast to the usual case, it does not require the assumption of left or right [[proper model category|properness]].

## Definition

A __weak model category__ is a [[premodel category]] that satisfies the following two [[axioms]]:

1. __Cylinder axiom__: Every [[cofibration]] $A\to X$ from a [[cofibrant object]] to a [[fibrant object]] admits a __relative strong cylinder object__ 
$$X\sqcup_A X\to I_A X\to X,$$ 
where the left map is a [[cofibration]] and its first component $X\to I_A X$
is an [[acyclic cofibration]].

1. __Path object axiom__: Every [[fibration]] $A\to X$ from a [[cofibrant object]] to a [[fibrant object]] admits a __relative strong path object__
$$A\to P_X A\to A\times_X A,$$
where the right map is a [[fibration]] and its first component $P_X A\to A$ is an [[acyclic fibration]].

## Properties

### Relation to premodel categories

A [[premodel category]] can be upgraded to a weak model category
as follows.

\begin{theorem}
If a [[premodel category]] admits a weak Quillen cylinder,
then it is a weak model category.
\end{theorem}

\begin{definition}
A __weak Quillen cylinder__ on a [[premodel category]] $C$
is a pair of [[left adjoint functors]] $I,D\colon C\to C$
together with the following commutative square of
[[natural transformations]] of [[functors]] $C\to C$:
$$\begin{matrix}
id_C\sqcup \id_C&\mathop{\longrightarrow}\limits^i&I\cr
\downarrow\nabla&&\downarrow e\cr
id_C&\mathop{\longrightarrow}\limits_j&D,\cr
\end{matrix}$$
where $\nabla$ is the [[codiagonal]],
$i$ is a [[cofibration]],
$j$ is a [[trivial cofibration]],
and the first component of $i$ is a [[trivial cofibration]].
\end{definition}

Here a [[natural transformation]] $\lambda\colon F\to G$
of [[functors]] $C\to C$ is a cofibration
if for any (trivial) cofibration $X\to Y$
the map $F(Y)\sqcup_{F(X)}G(X)\to G(Y)$ is a (trivial) cofibration.
Likewise, $\lambda$ is a trivial cofibration
if for any cofibration $X\to Y$ the above map is a trivial cofibration.

Reference: [Henry 20, Section 6](#Henry20).

This is essentially a reformulation of [[Cisinski-Olschok theory]].



### Relation to model categories

[[model category|Model categories]] can be singled out from weak model categories
by adding the following properties:

1.  Every [[fibrant object]] 
admits a strong path object and every [[cofibrant object]] admits a strong [[cylinder object]].

1.  All [[acyclic cofibrations]] are [[trivial cofibrations]]
and all [[acyclic fibrations]] are [[trivial fibrations]].
(Trivial maps are given as data for a [[premodel category]],
whereas acyclic (co)fibrations are defined as (co)fibrations
that satisfy a right (left) lifting property with respect to the class of cofibrations with cofibrant source (respectively fibrations with fibrant target.)

1.  The two classes of [[weak equivalence]] corresponding
to the left and right induced [[semimodel structures]] coincide.


### Relation to combinatorial model categories


Every [[combinatorial]] weak model category can
be connected to a [[combinatorial model category]]
by a zigzag of [[Quillen equivalences]].

## Examples

\begin{example}\label{WeakModelStructureOnSemiSimplicialSets}
**([[weak model structure on semi-simplicial sets]])** \linebreak
There is a weak model structure on [[semi-simplicial sets]] which is [[Quillen equivalence|Quillen equivalen]] to [[classical model structure on simplicial sets|that on simplicial sets]]. ([Henry 18, Thm. 5.5.6](#Henry18)).
\end{example}

## Related concepts

* [[model category]]

* [[premodel category]]


## References

* {#Henry18} [[Simon Henry]], _Weak model categories in classical and constructive mathematics_, Theory and Applications of Categories, Vol. 35, 2020, No. 24, pp 875-958.  ([arXiv:1807.02650](https://arxiv.org/abs/1807.02650), [tac:35-24](http://www.tac.mta.ca/tac/volumes/35/24/35-24abs.html))

* {#Henry20} [[Simon Henry]], _Combinatorial and accessible weak model categories_ ([arXiv:2005.02360](https://arxiv.org/abs/2005.02360))

[[!redirects weak model categories]]
[[!redirects weak model structure]]
[[!redirects weak model structures]]

