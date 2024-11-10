
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Topological spaces
* table of contents
{: toc}

## Idea
 {#Idea}

The notion of _topological space_ aims to axiomatize the idea of a _[[space]]_ as a collection of [[points]] that hang together ("[[cohesive topos|cohere]]") in a _[[continuous function|continuous]]_ way. Roughly speaking, a *topology* on a [[set]] "of points" prescribes which [[subsets]] are to be considered "[[neighborhoods]]" of the points they contain. Various conditions or [[axioms]] must be satisfied in order for such neighborhood systems to form a topology, but one of the most important is that for any two neighborhoods of a point, their [[intersection]] must also be a neighborhood of that point. 

Many notions of [[spaces]] used in [[mathematics]] have [[underlying topological spaces]], such as: [[manifolds]], [[schemes]], [[probability spaces]], etc.

The concept of a topology, gradually refined over the latter half of the 19th century and the first two decades of the 20th, was developed to capture what it means abstractly for a mapping between sets of points to be "[[continuous function|continuous]]". Intuitively, the idea of *bending*, *twisting* or *crumpling* a continuous body applies to continuous mappings, because they preserve neighborhood relations (in a suitable sense), but *tearing*, for instance, does not. 

For example, the surface of a [[torus]] or doughnut is topologically equivalent to the surface of a mug: the surface of the mug can be deformed _continuously_ into the surface of a torus. Abstractly speaking: the continuous [[cohesion]] among the collections of points of the two surfaces is the same. Similarly, a [[circle]] and a [[square]] are considered equivalent from the standpoint of their topologies. 

Some one-dimensional shapes with different topologies: the Mercedes-Benz symbol, a line, a circle, a complete graph with 5 nodes, the skeleton of a cube, and an asterisk (or, if you'll permit the one-dimensional approximation, a starfish). On the other hand, a circle has the same topology as a line segment with a wormhole at its finish which teleports you to its start; or more prosaically: The [[circle]] is [[homeomorphism|homeomorphic]] to the [[closed interval]] with *endpoints identified*.

There is a generalization of the notion of topological spaces to that of _[[locales]]_, which consists of dropping the assumption that all [[neighbourhoods]] are explicitly or even necessarily supported by points. For this reason, the theory of locales is sometimes called "pointless topology". In this form, the definition turns out to be quite fundamental and can be naturally motivated from just pure [[logic]] -- as the formal dual of _[[frames]]_ --  as well as, and [[duality|dually]], from [[category theory]] in its variant as [[topos theory]] -- by the notion of _[[(0,1)-toposes]]_. 

Topological spaces are the objects studied in _[[topology]]_. But types of topological spaces exist in such great and wild profusion that in practice it is often more convenient to replace strict topological equivalence by a notion of [[weak equivalence]], namely of [[weak homotopy equivalence]]. From this point of view, topological spaces  support also _[[homotopy theory]]_. 

Topological spaces equipped with extra [[property|properties]] and [[structure]] form the fundament of much of [[geometry]]. For instance a topological space locally isomorphic to a [[Cartesian space]] is a _[[manifold]]_. A topological space equipped with a notion of [[smooth functions]] into it is a [[diffeological space]]. The intersection of these two notions is that of a _[[smooth manifold]]_ on which [[differential geometry]] is based. And so on.


## Definitions
 {#Definitions}

We present first the

* [standard definition](#StandardDefinition)

and then a list of different

* [equivalent definitions](#AlternateDefinitions).

Finally we mention genuine

* [variants of the notion](#Variants).

### Standard definition
 {#StandardDefinition}


\begin{definition}\label{TheStandardDefinition}
A **topological space** is a [[set]] $X$ equipped with a set of [[subsets]] 
$U \subset X$, called the **[[open sets]]**, which are closed under 

1. finite [[intersections]],

1. arbitrary [[unions]].  

\end{definition}

+-- {: .num_remark}
###### Remark

The word 'topology' sometimes means the [[topology|study of topological spaces]] but here it means the collection of open sets in a topological space. In particular, if someone says 'Let $T$ be a topology on $X$', then they mean 'Let $X$ be equipped with the structure of a topological space, and let $T$ be the collection of open sets in this space'.

=--


+-- {: .num_remark}
###### Remark

Since $X$ itself is the intersection of zero subsets, it is open, and since the [[empty set]] $\emptyset$ is the union of zero subsets, it is also open. Moreover, every open subset $U$ of $X$ contains the empty set and is contained in $X$

$$
  \emptyset \subset U \subset X
  \,,
$$

so that the topology of $X$ is determined by a [[poset of open subsets]] $Op(X)$ with [[bottom]] element $\bot = \emptyset$ and [[top]] element $\top = X$. 

Since by definition the elements in this [[poset]] are closed under finite [[meets]] (intersection) and arbitrary [[joins]] (unions), this poset of open subsets defining a topology is a _[[frame]]_, the _[[frame of opens]]_ of $X$.

=--

+-- {: .num_defn}
###### Definition

A [[homomorphism]] between topological spaces $f : X \to Y$ is a **[[continuous function]]**: 

a [[function]] $f:X\to Y$ of the underlying [[sets]] such that the [[preimage]] of every open set of $Y$ is an open set of $X$.

=--

Topological spaces with continuous maps between them form a [[category]], usually denoted _[[Top]]_.

+-- {: .num_remark}
###### Remark

The definition of [[continuous function]] $f : X \to Y$ is such that it induces a homomorphism of the corresponding [[frames of opens]] the other way around

$$
  Op(X) \leftarrow Op(Y) : f^{-1}
  \,.
$$

And this is not just a morphism of [[posets]] but even of [[frames]].
For more on this see at _[[locale]]_.

=--

### Alternate equivalent definitions
 {#AlternateDefinitions}

There are many equivalent ways to define a topological space.  A non-exhaustive list follows:

* A set $X$ with a [[frame]] of open sets (the standard definition, given above), called a *topology* on $X$.

* A set $X$ with a co-frame of [[closed sets]] (the complements of the open sets), satisfying dual axioms: closure under finite unions and arbitrary intersections. This is sometimes called a co-topology on $X$. 

* A pair $(X, int)$, where $int\colon P(X) \to P(X)$ is a [[lex functor|left exact]] [[comonad]] on the [[power set]] of $X$ (the "[[interior]] operator"). In more nuts-and-bolts terms, this means for all subsets $A, B$ of $X$ we have 
$$A \subseteq B \Rightarrow int(A) \subseteq int(B), \;\;\; int(A) \subseteq A, \;\;\; int(A) \subseteq int(int(A)), \;\;\; int(A \cap B) = int(A) \cap int(B), \;\;\; int(X) = X.$$
The open sets are exactly the fixed points of $int$. The first three of these conditions say $int$ is a [[closure operator|coclosure operator]]. 

* A pair $(X, cl)$ where $cl$ is a [[rex functor|right exact]] [[Moore closure]] operator satisfying axioms dual to those of $int$.  The closed sets are the fixed points of $cl$. Such an operator is sometimes called a *Kuratowski closure operator* (compare Kuratowski's closure-complement problem at [[closed subspace]]). 

* A set $X$ together with, for each $x \in X$, a [[filter]] $N_x$ on $X$, i.e., a collection of inhabited subsets of $X$ closed under finite intersections and also upward-closed ($U \in N_x$ and $U \subseteq V$ together imply $V \subseteq N_x$). If $U \in N_x$, we call $U$ a *neighborhood* of $x$. The remaining conditions on these neighborhood systems are that $x \in U$ for every $U \in N_x$, and that for every $U \in N_x$, there exists $V \in N_x$ such that $V \subseteq U$ and $V$ is a neighborhood of each point it contains. In this formulation, a subset $U \subseteq X$ is *open* if it is a neighborhood of every point it contains. 

The next two definitions of topological space are at a higher level of abstraction, but the underlying idea that connects them with the neighborhood system formulation is that we say a filter $F$ on $X$ *converges* to a point $x \in X$ if $N_x \subseteq F$. The point then is to characterize properties of convergence abstractly. 

* A [[relational beta-module]]; that is, a [[lax algebra]] of the [[monad]] $\beta$ of [[ultrafilters]] on the [[(1,2)-category]] [[Rel]] of sets and [[binary relations]].  More explicitly, this means a set $X$ together with a relation called "[[convergence]]" between ultrafilters and points satisfying certain axioms.  This exhibits it as a special sort of [[generalized multicategory]], and also as a special sort of [[pseudotopological space]]. However, the equivalence of this definition to the traditional definition of a topological space requires the [[ultrafilter principle]] to be true. 

* A set with a [[convergence relation]] between [[nets]] or [[filters]] (not just ultrafilters) and points, or even between transfinite [[sequences]] and points, satisfying appropriate axioms. 

The following are not definitions, but they provide alternative ways to present a topological space. 

* A [[topological base|(topological) base]] on a set $X$ is a collection $\mathcal{B}$ of subsets of $X$ whose union is all of $X$, and such that whenever $B, C \in \mathcal{B}$ and $x \in B \cap C$, there exists $D \in \mathcal{B}$ such that $D \subseteq B \cap C$ and $x \in D$. 

If $\mathcal{B}$ is a base on $X$, then it is easily shown that the collection of all unions of subcollections of $\mathcal{B}$ is a topology on $X$. 

* A set $X$ with any collection of subsets whatsoever, to be thought of as a [[subbase]] for a topology. 

From the fact that the intersection of any collection of topologies is also a topology, there is a smallest topology that contains a given subbase $\mathcal{S}$. It consists of all possible unions of all possible finite intersections of members of $\mathcal{S}$. This is called the *topology generated by* the subbase. 


### Variations
 {#Variants}

Historically, the notion of topological space (see the historical references given [there](topology#ReferencesHistoricalOrigins)) involving [[neighbourhoods]] was first developed by [[Felix Hausdorff]] in 1914 in his seminal text on [[set theory]] and [[topology]], *Fundamentals of Set Theory* (*[[Grundzüge der Mengenlehre]]*). Hausdorff's definition originally contained the $T_2$-[[separation axiom]] (now known as the definition of *[[Hausdorff spaces]]*). This axiom was in effect removed by [[Kazimierz Kuratowski]] in 1922, who defined general topological spaces in terms of [[closure operators]] that preserve finite [[unions]]. The usual [[open set]] formulation was widely popularized by Bourbaki in their 1940 treatise (without identifying a single author behind this notion). 

However, in more modern treatments that emphasize [[category theory|category theoretic]] methods, particularly to address needs of [[homotopy theory]], it becomes important to consider not just the category [[Top]] of all topological spaces, but [[convenient categories of topological spaces]] that are better behaved, especially with regard to function spaces and [[cartesian closed category|cartesian closure]]. Thus many texts work with [[nice topological spaces]] (such as [[sequential topological spaces]]) and/or a [[nice category of spaces|nice-]] or [[convenient category of topological spaces]]  (such as [[compactly generated spaces]]), or indeed to directly use a model of $\infty$-[[infinity-groupoid|groupoids]] (such as [[simplicial sets]]).

On the other hand, when doing [[topos theory]] or working in [[constructive mathematics]], it is often more appropriate to use [[locales]] than topological spaces.

Some applications to [[analysis]] require more general [[convergence spaces]] or other generalisations.

There are also [[unified topological spaces]] which contains notions of apartness and nearness in addition to the usual notion of neighbourhood in a topological space. 

In [[dependent type theory]], one could also have a [[topological space]] be a general [[type]] instead of an [[h-set]]. For most kinds of topological spaces in dependent type theory, the [[T0-space|$T_0$]]-[[separation axiom]] forces the type to be an h-set. 

### In dependent type theory
 {#DependentTypeTheory}

In [[dependent type theory]], given a type $X$, the type of all [[subtypes]] of $X$, the [[powerset]] of $X$, is defined as the [[function type]] 
$$\mathcal{P}(X) \coloneqq X \to \Omega$$ 
where $\Omega$ is the [[type of all propositions]] with the type reflector type family $P:\Omega \vdash \mathrm{El}_\Omega(P) \; \mathrm{type}$. In the [[inference rules]] for the [[type of all propositions]], one has an operation $(-)_\Omega$ which takes a proposition $P$ and turns it into an element of the [[type of all propositions]] $P_\Omega:\Omega$. 


The **local membership relation** $x \in_A B$ between elements $x:A$ and material subtypes $B:\mathcal{P}(A)$ is defined as 
$$x \in_A B \coloneqq \mathrm{El}_\Omega(B(x))$$

Arbitrary unions and intersections of subtypes could be defined in [[dependent type theory]]: 

* Given a type $A$ and a type $I$, there is an function $\bigcap:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the $I$-indexed [[intersection]], such that for all families of subtypes $B:I \to \mathcal{P}(A)$, $\bigcap_{i:I} B(i)$ is defined as
$$\left(\bigcap_{i:I} B(i)\right)(x) \coloneqq (\forall i:I.x \in_A B(i))_\Omega$$
for all $x:A$, where 
$$\forall x:A.B(x) \coloneqq \left[\prod_{x:A} B(x)\right]$$ 
is the [[universal quantification]] of a [[type family]] and $[T]$ is the propositional truncation of $T$. 

* Given a type $A$ and a type $I$, there is an function $\bigcup:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the $I$-indexed [[union]], such that for all families of subtypes $B:I \to \mathcal{P}(A)$, $\bigcup_{i:I} B(i)$ is defined as
$$\left(\bigcup_{i:I} B(i)\right)(x) \coloneqq (\exists i:I.x \in_A B(i))_\Omega$$
for all $x:A$, where 
$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$ 
is the [[existential quantification]] of a [[type family]] and $[T]$ is the propositional truncation of $T$. 

In [[dependent type theory]], however, one cannot quantify over arbitrary types, since one could only quantify over elements of a type. Instead, one has to use a [[Tarski universe]] $(U, \mathrm{El}_U)$, where the elements of $U$ represent $U$-[[small types]], and then quantify over $U$. In the case of topological spaces, instead of the [[open sets]] being closed under arbitrary unions, the open sets are only closed under all $U$-small unions $\bigcup_{i:\mathrm{El}_U(I)} B(i)$ for $I:U$. 

\begin{definition}
Given a [[Tarski universe]] $(U, \mathrm{El}_U)$, a **[[topological space]]** is a type $X$ with a **$U$-small topology**, a type of subtypes $O(X)$ with canonical [[embedding]] $i_O:O(X) \hookrightarrow \mathcal{P}(X)$, called the open sets of $X$, which are closed under [[finite type|finite]] [[intersections]] and $U$-[[small type|small]] unions. 
\end{definition}

Given a topological space $(X, O(X))$, we define the membership [[relation]] between elements $x:X$ and open sets $V:O(X)$:

$$x:X, V:O(X) \vdash x \in V \; \mathrm{type}$$ 

by 

$$x \in V \coloneqq \mathrm{El}_\Omega((i_O(V))(x))$$

By definition of the type of all propositions and its type reflector, $x \in V$ is always a [[h-proposition]] for all $x:X$ and $V:O(X)$. 

## Examples

### Special cases

* [[finite topological space]]

* [[discrete topological space]]

* [[codiscrete topological space]]

* [[cofinite topology]]

* [[order topology]] [[specialization topology]], [[Scott topology]]

* [[compact topological space]]

* [[paracompact topological space]], [[sigma-compact topological space]], [[Lindelöf topological space]]

* [[spectral topological space]]

* [[CW-complex]]

* [[manifold]]

...


### Specific examples

* [[empty space]]

* [[point space]]

* [[Sierpinski space]]

* [[simplex]]

* [[circle]]

* [[Cantor space]]

* [[long line]], [[line with two origins]]

* [[K-topology]]

* [[projective space]], [[real projective space]], [[complex projective space]]

* [[classifying space]]

...

+-- {: .num_example}
###### Example

The [[Cartesian space]] $\mathbb{R}^n$ with its standard notion of open subsets [[topological base|generated from]]: [[unions]] of [[open balls]] $D^n \subset \mathbb{R}^n$.

=--


## Related concepts

* [[separation axioms]]

* [[finer topology]], [[coarser topology]]

* [[first countable topological space]], [[second countable topological space]], [[separable topological space]], [[Hausdorff topological space]], [[topological manifold]]

* [[sigma-topological space|$\sigma$-topological space]]

* [[unified topological space]]

* [[topological property]]

* [[locale]], [[topos]]

* [[ionad]]

* [[proximity space]], [[uniform space]], [[syntopogenous space]]

* [[quotient topology]], [[quotient topological space]]

* [[subspace topology]], [[topological subspace]]

* [[product topological space]]

* [[effective topological space]], [[equilogical space]]

* [[topological G-space]]

* [[filter space]]

* [[connected topological spaces]], [[simply connected topological space]]

* [[nilpotent topological space]]

* [[fractal]]

* [[sheaf on a topological space]]

* [[pretopological space]]

[[!include topology -- references]] 



[[!redirects topological space]]
[[!redirects topological spaces]]
[[!redirects topological structure]]
[[!redirects topological structures]]

[[!redirects small topology]]
[[!redirects small topologies]]

[[!redirects small topological structure]]
[[!redirects small topological structures]]
