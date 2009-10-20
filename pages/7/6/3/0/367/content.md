#Contents#
* automatic table of contents
{:toc}

#Idea#

A simplicial object $X$ in a [[category]] $C$ is a collection $\{X_n\}_{n \in \mathbb{N}}$ of [[object]]s in $C$ that behave as if $X_n$ were an $n$-dimensional [[simplex]] [[internalization|internal to]] $C$. 


#Definition#

A **simplicial object** in a category $C$ is a [[functor]] $\Delta^{op} \to C$, where $\Delta$ is the [[simplex category|simplicial indexing category]].

A **cosimplicial object** in $C$ is similarly a functor out of the [[opposite category]], $\Delta \to C$.

Accordingly, simplicial and cosimplicial objects in $C$ themselves form a [[category]] in an obvious way, namely the [[functor category]] $[\Delta^{op},C]$ and $[\Delta,C]$, respectively.

**Remark**

A **simplicial object** $X$ in $C$ is often specified by 
the objects, $X_n$, which are the images under $X$, of the objects $[n]$ of $\Delta$, together with a description of the face and degeneracy morphisms, $d_i$ and $s_j$, which must satisfy the [[simplicial identities]].

#Examples#

* A simplicial object in [[Set]] is a [[simplicial set]].

* A simplicial object in a category of [[presheaf|presheaves]] is a [[simplicial presheaf]].

* A cosimplicial object in the category of [[ring]]s ([[algebra]]s) is a [[cosimplicial ring]] ([[cosimplicial algebra]]).

* A simplicial object in the category [[Grp]] of [[group]]s is a [[simplicial group]]. See also [[Dold-Kan correspondence]].

* A simplicial object in a category of simplicial objects is a [[bisimplicial object]].

[[!redirects simplicial objects]]
[[!redirects cosimplicial object]]
[[!redirects cosimplicial objects]]