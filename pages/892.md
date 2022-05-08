
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

# Power sets
* table of contents
{: toc}

## Definition

Given a [[set]] $S$, the __power set__ of $S$ is the set $\mathcal{P}S$ of all [[subsets]] of $S$.  Equivalently, it is 

* the set $\TV^S$ of all [[functions]] from $S$ to the set $\TV$ of [[truth values]].  This is often written $2^S$, since there are (at least in [[classical logic]]) exactly $2$ truth values;

* the collection of [[subobjects]] of $X$ in the [[topos]] [[Set]].

* the [[slice category]] $Inj/S$, where [[Inj]] is the [[wide subcategory]] of [[Set]] with morphisms restricted to [[injection|injections]]. This is similar to the subobject definition but is more unpacked. $Inj/S$ has objects that are injections to $S$ and morphisms that are commuting triangles of injections.


## Foundational status

One generally needs a specific axiom in the [[foundations of mathematics]] to ensure the existence of power sets.  In [[material set theory]], this can be phrased as follows:

+-- {: .un_defn}
###### Axiom (power sets)

If $S$ is a set, then there exists a set $\mathcal{P}$ such that $A \in \mathcal{P}$ if $A \subseteq S$.
=--

One can then use the [[axiom of separation]] ([[bounded separation]] is enough) to prove that $\mathcal{P}$ may be chosen so that the subsets of $A$ are the *only* members of $\mathcal{P}$; the [[axiom of extensionality]] proves that this $\mathcal{P}$ is unique.

In [[structural set theory]], we state rather that there exists a set $\mathcal{P}$ which indexes the subsets of $A$ and prove uniqueness [[generalised the|up to unique isomorphism]].

In [[predicative mathematics]], the existence of power sets (along with other "impredicative" axioms) is not accepted.  However we can still speak of a power set as a [[proper class]], sometimes called a __power class__.

One can use power sets to construct [[function sets]]; the converse also works using [[excluded middle]] (or anything else that will guarantee the existence of the set of truth values).  In particular, power sets exist in any theory containing excluded middle and function sets; thus predicative theories which include function sets must also be [[constructive mathematics|constructive]].


## Properties

### General

* The power set $\mathcal{P}S$ is a [[partial order|poset]] ordered by containment: $A$ precedes $B$ means that $A$ is a [[subset]] of $B$ ($A \subseteq B$).


* [[Cantor's theorem]] states that there exists no [[surjection]] from $S$ to $\mathcal{P}S$; as there does exist such an [[injection]], one concludes that
$$ {|S|} \lt {|\mathcal{P}S|} $$
in the usual arithmetic of [[cardinal numbers]].

* Power sets live in the category [[Set]].  Given an object $S$ of any [[category]], one can similarly form a poset of [[subobjects]] of $S$; the category is called [[well-powered category|well-powered]] when this poset is [[small category|small]].  One also has an internal notion of power set (a [[power object]]) in a [[topos]].

* The power set construction constitutes an [[equivalence of categories]] between the [[opposite category]] [[Set]]$^{op}$ and that of [[complete atomic Boolean algebras]]. See at _[Set -- Properties -- Opposite category and Boolean algebras](Set#OppositeCategory)_. Restricted to [[finite sets]], the power set construction constitutes an [[equivalence of categories]] between the [[opposite category]] of [[FinSet]] and that of finite [[Boolean algebras]]. See at _[FinSet -- Opposite category](FinSet#OppositeCategory)_.

### Power set functor

The power set construction gives rise to two functors, the contravariant power set functor $Set^op \to Set$ and the covariant power set functor $Set \to Set$. The first sends a function $f\colon S\to T$ to the _preimage_ function $f^*\colon P(T) \to P(S)$, whereas the second sends $f$ to the _image_ function $f_*\colon P(S) \to P(T)$.


## Related concepts

* A [[closure operator]] on a power set is a _[[Moore closure]]_.

* [[power object]]

* [[poly-morphism]]


category: foundational axiom

[[!redirects power set]]
[[!redirects power sets]]
[[!redirects power-set]]
[[!redirects power-sets]]
[[!redirects powerset]]
[[!redirects powersets]]

[[!redirects power class]]
[[!redirects power classes]]
[[!redirects power type]]
[[!redirects power types]]

[[!redirects axiom of power set]]
[[!redirects axiom of power sets]]
[[!redirects power set axiom]]
[[!redirects powerset axiom]]

[[!redirects power set functor]]
[[!redirects power set functors]]
[[!redirects covariant power set functor]]
[[!redirects covariant power set functors]]
[[!redirects contravariant power set functor]]
[[!redirects contravariant power set functors]]

[[!redirects powerset functor]]
[[!redirects powerset functors]]
[[!redirects covariant powerset functor]]
[[!redirects covariant powerset functors]]
[[!redirects contravariant powerset functor]]
[[!redirects contravariant powerset functors]]




