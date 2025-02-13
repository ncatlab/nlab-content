
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


A __cogenerator__ in a [[category]] $C$ is an [[object]] $S$ such that the [[functor]] $h_S = C(-,S) : C^{\mathrm{op}} \to \mathrm{Set}$ is [[faithful functor|faithful]]. This means that for any pair $g_1,g_2\in C(X,Y)$, if they are indistinguishable by morphisms to $S$ in the sense that
$$ \forall (\theta: Y \to S),\; \theta \circ g_1 = \theta \circ g_2 ,$$
then $g_1 = g_2$.

One often extends this notion to a __cogenerating family__ of objects, which is a (usually [[small category|small]]) set $\mathcal{S} = \lbrace S_a, a\in A\rbrace$ of objects in $C$ such that the family $C(-,S_a)$ is jointly faithful. This means that for any pair $g_1,g_2\in C(X,Y)$, if they are indistinguishable by morphisms to $\mathcal{S}$ in the sense that
$$ \forall (a: A),\; \forall (\theta: Y \to S_a),\; \theta \circ g_1 = \theta \circ g_2 ,$$
then $g_1 = g_2$.



## Examples

In [[Set]], the set of [[truth value]]s is a cogenerator.  More generally, in any [[well-pointed topos]], the [[subobject classifier]] is a cogenerator. 

Much more generally, we have 

+-- {: .num_prop} 
###### Proposition 
Every [[topos]] with a [[size issues|small set]] of [[separator|generators]] (e.g., a well-pointed topos, or a Grothendieck topos), and that has [[products]] of objects indexed over sets no larger in [[cardinality]] than the generating set, admits an [[injective object|injective]] cogenerator. 
=-- 

+-- {: .proof} 
###### Proof 
Let $C$ be a set of generators for the topos; as usual, let $\Omega$ be the subobject classifier. We claim that a product 

$$\prod_{c \in C} \Omega^c$$ 

is a cogenerator. For suppose $f, g \colon X \stackrel{\to}{\to} Y$ are distinct morphisms. The contravariant power object functor $\Omega^-$ is faithful (a familiar fact, since it is [[monadic functor|monadic]]), so that $\Omega^f, \Omega^g: \Omega^Y \stackrel{\to}{\to} \Omega^X$ are distinct. Since the objects $c$ form a [[separator|generating set]], there is some $h \colon c \to \Omega^Y$ such that the composites 

$$c \stackrel{h}{\to} \Omega^Y \stackrel{\overset{\Omega^f}{\to}}{\underset{\Omega^g}{\to}} \Omega^X$$ 

are distinct. The map $h$ may be transformed to a map $\tilde{h}: Y \to \Omega^c$, and it follows that the two composites 

$$X \stackrel{\overset{f}{\to}}{\underset{g}{\to}} Y \stackrel{\tilde{h}}{\to} \Omega^c$$ 

are distinct. For any other $c' \in C$, we may uniformly define $Y \to \Omega^{c'}$ to be the map classifying the maximal [[subobject]] of $c' \times Y$, so that these maps together with $\tilde{h}$ collectively induce a map 

$$Y \to \prod_{c \in C} \Omega^c$$ 

that yields distinct results when composed with $f$ and $g$. This proves the claim. 

The object $\prod \Omega^c$ is injective because already $\Omega$ is injective (see Mac Lane-Moerdijk, IV.10), and it is a general fact that in a [[cartesian closed category]] (or more generally a [[closed monoidal category]]), an exponential (or internal Hom) $X^Y$ whose base $X$ is injective is also injective, and products of injective objects are injective. 
=-- 

Notice also that the existence of a small (co)generating family is one of the conditions in one version of the [[adjoint functor theorem]]. We may conclude, for example, that [[Grothendieck toposes]] are cototal (q.v.). 

###In topology

The existence of cogenerators is useful to produce adjoint functor theorems for certain categories of topological spaces, as well, as these are usually not locally presentable like most other typical "large" categories of mathematics. 

* In the category of all topological spaces, a single space $X$ is a cogenerator if and only if it is not $T_0,$ since $T_0$ spaces can't distinguish the points of a $T_0$ space and, conversely, any such space has the two-point indiscrete space, which cogenerates for the same reason as a two-point set, as a retract.

* In compact Hausdorff spaces, which are algebraic but not locally presentable, the interval $[0,1]$ is a cogenerator, as follows essentially from Gelfand duality. 

* Many other categories of spaces, but not all, have cogenerators; for more see the answers and references [here](https://ncatlab.org/nlab/edit/cogenerator).

##Terminology

The concept of _cogenerator_ is dual to that of [[separator]], so it can also be referred to as a _coseparator_.


## Related concepts

* [[generator]]

* [[separator]]

* **cogenerator**


[[!redirects cogenerators]]

[[!redirects cogenerating set]]
[[!redirects coseparator]]