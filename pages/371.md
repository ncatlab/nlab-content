
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+-- {: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

# Zero objects
* table of contents
{: toc}

## Definition

+-- {: .num_defn}
###### Definition

In a [[category]], an [[object]] is called 
a **zero object**, **null object**, or **biterminator** if it is both an [[initial object]] and a [[terminal object]].  

=--

A category with a zero object is sometimes called a _[[pointed category]]_.

+-- {: .num_remark}
###### Remark

This means that $0 \in \mathcal{C}$ is a zero object precisely if for every other object $A$ there is a unique [[morphism]] $A \to 0$ to the zero object as well as a unique morphism $0 \to A$ from the zero object.

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is a [[pointed category]], then an object $A$ of $\mathcal{C}$ is a zero object precisely when the only endomorphism of $A$ is the identity morphism.

=--



+-- {: .num_remark}
###### Remark

There is also a notion of **zero object** in [[algebra]] which does not always coincide with the category-theoretic terminology. For example the zero [[ring]] $\{0\}$ is not an [[initial object]] in the category of unital rings (this is instead the [[integers]] $\mathbb{Z}$); but it is the 
[[terminal object]].  However, the zero ring *is* the zero object in the category of [[nonunital ring]]s (although it happens to be unital).

=--




## Examples

+-- {: .num_prop}
###### Proposition


* The [[category of pointed sets]] has a zero object, namely any one-element set.  

* The [[trivial group]] is a zero object in the category [[Grp]] of [[groups]] and in the category [[Ab]] of [[abelian groups]].  

* For $R$ a [[ring]], the trivial $R$-[[module]] (that whose underlying abelian group is the [[trivial group]]) is the zero-object in $R$[[Mod]].

  In particular for $R = k$ a [[field]], the $k$-[[vector space]] of [[dimension]] 0 is the zero object in [[Vect]].

* However, the zero [[ring]] is not a zero object in the category of [[ring|rings]], at least as long as rings are required to have units (and ring homomorphisms to preserve them).

* For every category $C$ with a [[terminal object]] $*$ the [[under category]] $pt \downarrow C$ of [[pointed objects]] in $C$ has a zero object: the morphism $Id_{pt}$.

=--

+-- {: .num_prop #InCatsEnrichedInPointedSets}
###### Proposition

In any category $C$ [[enriched category|enriched]] over the [[category of pointed sets]] $(Set_*, \wedge)$ with [[tensor product]] the [[smash product]], any object that is either initial _or_ terminal is automatically both and hence a zero object.  

=--

+-- {: .proof}
###### Proof

Write $* \in Set_*$ for the singleton pointed set. Suppose $t$ is [[terminal object|terminal]]. Then $C(x,t) = *$ for all $x$ and so in particular $C(t,t) = *$ and hence the [[identity]] morphism on $t$ is the basepoint in the pointed [[hom-set]]. By the axioms of a [[category]], every morphism $f : t \to x$ is equal to the composite

$$
  f : t \stackrel{Id}{\to} t \stackrel{f}{\to} x
  \,.
$$

By the axioms of an $(Set_*, \wedge)$-enriched category, since $Id_{t}$ is the basepoint in $C(t,t)$, also this composite is the basepoint in $C(t,x)$ and is hence the [[zero morphism]]. So $C(t,x) = *$ for all $x$ and therefore $t$ is also an [[initial object]].

Analogously from assuming $t$ to be initial it follows that it is also terminal.

=--

+-- {: .num_remark}
###### Remark


This is a special case of an [[absolute limit]].  

=--

+-- {: .num_remark}
###### Remark

Categories enriched in $(Set_*, \wedge)$ include in particular [[Ab]]-enriched categories. So any [[additive category]], hence every [[abelian category]] has a zero object.

=--

* In the [[stable homotopy category]]: [[zero spectrum]].

## Properties

+-- {: .num_prop}
###### Proposition

A category has a zero object precisely if it has an [[initial object]] $\emptyset$ and a [[terminal object]] $*$ and the unique morphism $\emptyset \to *$ is an [[isomorphism]].

=--


+-- {: .num_remark}
###### Remark

In a category with a zero object 0, there is always a canonical morphism from any object $A$ to any other object $B$ called the _[[zero morphism]]_, given by the composite $A\to 0 \to B$. 

Thus, such a category becomes [[enriched category|enriched]] over the [[category of pointed sets]], a partial converse to prop \ref{InCatsEnrichedInPointedSets}.

=--



## Related concepts

* [[pointed category]]

  [[pointed (∞,1)-category]], [[pointed model category]]

* [[zero morphism]]

* [[zero object in a derivator]]


[[!redirects zero object]]
[[!redirects zero objects]]
[[!redirects 0 object]]
[[!redirects 0 objects]]
[[!redirects 0-object]]

[[!redirects null object]]
[[!redirects null objects]]

[[!redirects biterminator]]
[[!redirects biterminators]]
