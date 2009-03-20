Let $C$ be a category. An object $x$ in $C$ is __compact__ if for every set $S$ of objects of $C$ such that the direct sum $\coprod_{s\in S} s$ exists, the canonical map
$$
\coprod_{s\in S} C(x,s)\to C(x,\coprod_{s\in S}s)
$$
is an isomorphism of sets. 

As every triangulated category is an additive category,
this notion is used in triangulated setup without change.
A triangulated category is __compactly generated__ if it is generated (see [[generator]]) by a _set_ of compact objects.

The notion can be modified to the categories enriched over a closed monoidal category (compare to the notions of finite and/or rigid objects in various contexts).

Compact objects in the derived categories of quasicoherent sheaves over a scheme are called perfect complexes. Any compact object in the category of modules over a perfect ring is finitely generated as a module. 
Lurie uses $\kappa$-compact objects in the setup of $(\infty,1)$-categories.

+--{: .query}
[[Mike Shulman|Mike]]: This may be the appropriate notion in a triangulated category, but in other contexts it is not right.  For instance, with this definition a topological space would be compact iff it is connected.  I think it is more common in non-additive situations to define compactness relative to directed unions.

[[Zoran Škoda]]: I agree. It is most standard in additive categories (including triangulated and abelian) and in few other examples. 
=--
