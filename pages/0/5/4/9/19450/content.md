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

[[!redirects categories of PERs]]
[[!redirects modest set]]
[[!redirects modest sets]]
