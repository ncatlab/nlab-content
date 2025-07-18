
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **topological vector space**, or **TVS** for short, is a [[vector space]] $X$ over a [[topological field]] (usually a [[local field]], more often than not the field of [[real numbers]] or the field of [[complex numbers]] with the usual topology) $k$ (called the [[ground field]]) equipped with a [[topological space|topology]] for which the addition and scalar multiplication maps 
$$+: X \times X \to X, \qquad \cdot: k \times X \to X$$ 
are [[continuous function|continuous]]. The topological vector spaces over a given field form a category [[TopVect]].

Much as a [[topological group]] is a [[group object]] in [[Top]], so a TVS is the same as a vector space [[internalization|internal to]] $Top$ ... *provided* that we use the _two-sorted_ notion of vector space $(k, X)$ so that the first sort is interpreted as the topological ground field. (More generally, there is a notion of topological module which is the internalization in $Top$ of the two-sorted notion of module involving a ring sort and a module over that ring; this notion is purely equational and thus interpretable in terms of finite products. Then a TVS is a topological module whose underlying ring is a field.) N.B.: if we internalize the one-sorted notion vector space, in which the ground field is encoded in the [[Lawvere theory]] as the set of unary operations, the continuity of the unary operations gives only a continuous map ${|k|} \times X \to X$ where we use the [[discrete topology]] on $k$ -- which is not what we want. 

Like any topological [[abelian group]], a TVS $X$ carries a [[uniform space]] structure generated by a basis of [[entourages]] (aka vicinities) that correspond to neighborhoods $U$ of $0$: 
$$\{(u, v) \in X \times X: u - v \in U\}$$ 

Thus many uniform notions (uniform continuity, completeness, etc.) carry over to the TVS context. Also from the uniformity (although it is also easy to prove directly), it follows that a TVS is completely regular, and also Hausdorff if and only if it is $T_0$ (see [[separation axiom]]). Most authors insist on the $T_0$ condition to rule out degenerate cases, but that prevents the category of TVSes from being [[topological concrete category|topological]] over [[Vect]].
If the TVS $V$ is not Hausdorff, then the subset $V_0$ defined as the intersection of all neighborhoods of zero is a vector subspace of $V$ and the [[quotient space|quotient vector space]] $V/V_0$ is Hausdorff, hence Tihonov (= completely regular Hausdorff). 

The condition that scalar multiplication is continuous puts significant constraints on the topology of $X$. For example, if we assume $k$ has a base of compact absorbing neighborhoods of $0$ and $V$ is Hausdorff, then for any non-zero $v \in X$ the function
$$- \cdot v: k \to V$$ 
maps $k$ [[homeomorphism|homeomorphically]] onto its image. It can then be shown that $X$ cannot (for instance) be [[compact space|compact]] (unless it is the zero space and so has no non-zero $v$); a classical theorem along these lines is that $V$ (over a [[local field]]) can be locally compact Hausdorff if and only if $V$ is finite-dimensional. (In the non-Hausdorff case, the theorems are that $X$ is compact if and only if its topology is indiscrete and that $X$ is locally compact if and only if it is a finitary [[direct sum]] of indiscrete spaces.) On the other hand, a nice property of even infinite-dimensional TVSes is that they are [[path-connected space|path-connected]], or at least so in the classical cases where the ground field is $\mathbb{R}$ or $\mathbb{C}$. 

More classical material should be added, particularly on [[locally convex spaces]].


### TVSes from a Hilbert space viewpoint

The theory of TVS can be understood as the quest to find the essence of many fundamental theorems of [[functional analysis]] of [[Hilbert space]]s (or [[Banach space]]s), namely to find the minimal set of assumptions that are needed for Hilbert space theorems to remain true.
Examples of these are:


* the [Hahn--Banach Theorem](http://en.wikipedia.org/wiki/Hahn%E2%80%93Banach_theorem)

* the [Open Mapping](http://en.wikipedia.org/wiki/Open_mapping_theorem_%28functional_analysis%29) and [[closed graph theorem]]s

A central r&#244;le in the whole theory plays **duality**, that is the study of [[locally convex spaces]] and their duals. A prominent example is the definition of certain concepts by duality in the theory of [[Schwartz distribution]]s.


## Important subclasses
 {#ImportantSubclasses}

Topological vector spaces come in many flavours. The following chart
provides a first overview (chart originally created and published by
[[Greg Kuperberg]] on MathOverflow
[here](http://mathoverflow.net/questions/8443/barrelled-bornological-ultrabornological-semi-reflexive-how-are-these-use),
current version generated using Graphviz from [[lctvs dot source]]):

[[!include TVS relationships]]

- [[locally convex spaces]]: where the Hahn-Banach theorem works (assuming sufficient axioms)

- [[bornological topological vector space]]s: where bounded means continuous

- [[barrelled topological vector space]]s

* [[sequence space]]

* [[stereotype space]]

## Related concepts

* [[weak topology of a topological vector space]]

* [[topology of uniform convergence]]

* [[topological vector bundle]]

* [[diffeological vector space]]

## References

* [[Nicolas Bourbaki]], *Topological Vector Spaces*, Chapters 1–5, Masson (1981), Springer (2003) &lbrack;[doi:10.1007/978-3-642-61715-7](https://doi.org/10.1007/978-3-642-61715-7)&rbrack;


* {#Treves67} [[François Trèves]], _Topological Vector Spaces, Distributions and Kernels_ (Academic Press, New York, 1967)

The following review gives lots of important examples

* Paul Garrett, _Catalogue of Useful Topological Vectorspaces_, 2011 ([pdf](http://www-users.math.umn.edu/~garrett/m/fun/catalogue_tvs.pdf))

See also 


* Wikipedia, _[Topological vector space](http://en.wikipedia.org/wiki/Topological_vector_space)_

category: analysis

[[!redirects topological vector space]]
[[!redirects topological vector spaces]]
[[!redirects TVS]]
[[!redirects TVSs]]
[[!redirects TVSes]]
