
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _matching family_ of elements is an explicit component-wise characterizaton of a morphism from a [[sieve]] into a general [[presheaf]].

Since such morphisms govern the [[sheaf]] property and the operation of [[sheafification]], these can be discussed in terms of matching families.
As such, the set of matching families for a given [[covering]] and [[presheaf]] is the corresponding [[descent object]].


## Definition

Let $(C,\tau)$ be a [[site]] and $P:C^{\mathrm{op}}\to\mathrm{Set}$ a [[presheaf]] on $C$. Let $S\in \tau(c)$ be a [[cover]]ing [[sieve]] on [[object]] $c\in C$ (in particular a subobject of the [[representable functor|representable]] presheaf $h_c$). 

A __matching family__ for $S$ of elements in $P$ is a rule assigning to each $f:d\to c$ in $S$ an element $x_f$ of $P(d)$ such that
for all $g:e\to d$
$$ P(g)(x_f) = x_{f\circ g}. $$
Notice that $f\circ g\in S$ because $S$ is a sieve, so that the condition makes sense; furthermore the order of composition and the contravariant nature of $P$ agree. If we view the sieve $S$ as a subobject of the representable $h_c$, then a matching family $(x_f)_{f\in S}$ is precisely a [[natural transformation]] $x:S\to P$, $x: f\mapsto x_f$.

An __amalgamation__ of the matching family $(x_f)_{f\in S}$ for $S$ is an element $x\in P(c)$ such that $P(f)(x) = x_f$ for all $f\in S$.  

## Properties

### Characterization of sheaves

$P$ is a [[sheaf]] for the [[Grothendieck topology]] $\tau$ iff for all $c$, for all $S\in\tau(c)$ and every matching family $(x)_{f\in S}$ for $S$, there is a unique amalgamation. Equivalently $P$ is a sheaf if any natural transformation $x:S\to P$ has a unique extension to $h_C\to P$ (along inclusion $S\hookrightarrow h_c$); or to phrase it differently, $P$ is a sheaf (resp. [[separated presheaf]]) iff the precomposition with the inclusion $i_S : S\hookrightarrow h_C$ is an [[isomorphism]] (resp. [[monomorphism]]) $i_S:\mathrm{Nat}(h_C,P)\to \mathrm{Nat}(S,P)$. 

Suppose now that $C$ has all [[pullback]]s.  Let $R = (f_i:c_i\to c)_{i\in I}$ be any [[cover]] of $c$ (i.e., the smallest [[sieve]] containing $R$ is a [[covering]] sieve in $\tau$) and let $p_{ij}:c_i\times_c c_j\to c_i$, $q_{ij}:c_i\times_c c_j\to c_j$ be the two projections of the pullback of $f_j$ along $f_i$. A __matching family__ for $R$ of elements in a presheaf $P$ is by definition a family $(x_i)_{i\in I}$ of elements $x_i\in P(c_i)$, such that for all $i,j\in I$, $P(p_{ij})(x_i) = P(q_{ij})(x_j)$. 



### Sheafification

Let $\mathrm{Match}(R,P)$ be the set of matching families for $R$ of elements in $P$. Sieves over $c$ form a [[filtered category]], where partial ordering is by reverse inclusion ([[refinement]] of sieves).  There is an endofunctor $()^+ : PShv(C,\tau)\to PShv(C,\tau)$ given by 
$$ P^+(c) := \mathrm{colim}_{R\in\tau(C)} \mathrm{Match}(R,P)$$
In other words, elements in $P^+(c)$ are matching families $(x^R_f)_{f\in R}$ for all covering sieves modulo the equivalence given by agreement $x^R_f = x^{R'}_f$, for all $f\in R''$, where $R''\subset  R\cap R'$ is a common refinement of $R$ and $R'$. This is called the [[plus construction]].

Endofunctor $P\mapsto P^+$ extends to a presheaf on $C$ by $P^+(g:d\to c) : (x_f)_{f\in R}\mapsto (x_{g\circ h})_{h\in g^*R}$ where $g^* R = \{h:e\to d | e\in C, g\circ h\in R\}$ (recall that by the stability axiom of Grothendieck topologies, $g^*(d)\in \tau(d)$ is a covering sieve over $d$). 

The presheaf $P^+$ comes equipped with a canonical natural transformation $\eta:P\to P^+$ which to an element $x\in P(c)$ assigns the equivalence class of the matching family $(P(f)(x))_{f\in Ob(C/c)}$ where the [[maximal sieve]] $Ob(C/c)$ is the class of objects of the slice category $C/c$. 

$\eta$ is a [[monomorphism]] (resp. [[isomorphism]]) of presheaves iff the presheaf $P$ is a [[separated presheaf]] (resp. [[sheaf]]); moreover any morphism $P\to F$ of presheaves, where $F$ is a sheaf, factors uniquely through $\eta:P\to P^+$. For any presheaf $P$, $P^+$ is separated presheaf and if $P$ is already separated then $P^+$ is a sheaf. In particular, for any presheaf $P^{++}$ is a sheaf. A fortiori, $P^+(\eta)\circ\eta:P\to P^{++}$ realizes [[sheafification]]. 

### Co-representation by Čech groupoids
 {#CoRepresentationByCechGroupoid}

When [[presheaves]] of sets are regarded a [[presheaves of groupoids]], the [[Čech groupoid]] serves to co-represent matching families, hence serves as the _[[codescent object]]_ of the given covering and presheaf. See [there](Čech+groupoid#Codescent) for more.

## References

A standard reference is 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, Springer 1992. (chapter III)

[[!redirects matching families]]
