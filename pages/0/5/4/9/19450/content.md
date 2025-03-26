# The category of PERs

* table of contents
{: toc}

## Idea

The **category of PERs** over a [[partial combinatory algebra]] $A$ is a particularly concrete and simple subcategory of its [[realizability topos]], which is especially well-suited to modelling "computable" objects relative to $A$.

It is based on the idea that a "computable set" $X$ relative to $A$ is specified by saying which elements of $A$ are "codes" representing which elements of $X$, such that no element of $A$ can code for more than one element of $X$ (but not all elements of $A$ need to code for any element of $X$).  Thus this sort of "computable set" (sometimes called a **modest set**) is equivalently a partition of a subset of $A$, i.e. a [[partial equivalence relation]] on $A$.

## Definition

Let $A$ be a [[partial combinatory algebra]].  If $E$ is a [[partial equivalence relation]] on $A$, we write $A/E$ for its set of equivalence classes.  Now the [[category]] $PER(A)$ has:

* as objects, the [[partial equivalence relations]] on $A$.

* as morphisms $E\to E'$, for PERs $E$ and $E'$, the set-theoretic functions $\phi:A/E \to A/E'$ with the [[property]] of being "tracked", i.e. such that there exists an element $f\in A$ such that whenever $(a,a)\in E$ we have $\phi([a]) = [f\cdot a]$ (hence in particular $(f\cdot a,f\cdot a)\in E'$).  Equivalently, it is the quotient of the set of elements $f\in A$ such that $(a,b)\in E$ implies $(f\cdot a,f\cdot b)\in E'$ by the relation $f\sim g$ meaning that $(f\cdot a,g\cdot a)\in E'$ whenever $(a,a)\in E$.

## Properties

* $PER(A)$ is a [[locally cartesian closed category]] and a [[Heyting category]].

* $PER(A)$ is a full subcategory of the category of [[assemblies]] over $A$, which is in turn a full subcategory of the [[realizability topos]] over $A$.

## In first-order logic

Given a theory in first-order logic with equality (categorically, this can be taken as a [[first-order hyperdoctrine]]), its category of partial equivalence relations represents all the [[subquotient]]s the theory can "see" of its given sorts and all the functions the theory can "see" between them.

Specifically, the objects of this category are pairs $(X, R)$ where $X$ is a sort in the first-order theory and $R$ is a binary predicate which the theory proves to be a [[partial equivalence relation]] on $X$. A morphism between objects $(X, R)$ and $(Y, S)$ can be taken to be a binary predicate $F \in P(X \times Y)$ such that the theory proves $F$ is essentially the graph of a function between the specified subquotients (In detail: ...). Composition is given in the obvious way (In detail: ...).

In the case where the original hyperdoctrine was in fact a [[tripos]], the resulting category of PERs will be a [[topos]] (while the converse isn't quite true, the condition of being a tripos is just slightly stronger than necessary for this to happen).

## Relationship with exact completions

The construction of partial equivalence relations is part of the [[tripos]] to [[topos]] construction. The following universal property is noted by Maietti and Rosolini (2012). 

Let $\mathbf{Ex}$ be the (bi-)category of [[exact categories]] and [[regular functors]] between them. There is also a $\mathbf{EED}$ of elementary existential doctrines (aka [[regular hyperdoctrines]]). There is a forgetful functor  $\mathbf{Ex} \to \mathbf{EED}$, mapping an exact category to its doctrine of [[subobjects]]. The construction of PERs forms a left adjoint to this functor. 

## References

* [[Maria Maietti]] and [[Giuseppe Rosolini]], Unifying exact completions. Applied Categorical Structures, 2012. arxiv:[1212.0966 ](https://arxiv.org/abs/1212.0966)

[[!redirects categories of PERs]]
[[!redirects category of partial equivalence relations]]
[[!redirects categories of partial equivalence relations]]
[[!redirects modest set]]
[[!redirects modest sets]]
