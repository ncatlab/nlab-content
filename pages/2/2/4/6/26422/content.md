
## Disambiguation

There are a few different types which can be called *path types* or *path space types* in [[dependent type theory]]:

* The [[identity type]] $x =_A y$ for type $A$ and elements $x:A$ and $y:A$, which is the type of paths between $x:A$ and $y:A$;

* The [[dependent sum type]] $\sum_{x:A} \sum_{y:A} x =_A y$, which is the type of all paths in $A$; reflexivity is given by the [[diagonal function]];

* The [[function type]] $\mathbb{I} \to A$ from the [[interval type]] $\mathbb{I}$ to type $A$; reflexivity is given by the [[constant functions]] in $\mathbb{I} \to A$ - this parallels the topological definition of [[path spaces]] as continuous functions out of the [[unit interval]];

* In [[cubical type theory]], the [[cubical path type]] $\mathrm{path}_A(x, y)$ for type $A$ and elements $x:A$ and $y:A$ - this is notated similarly to the identity type but also behaves as function types from the predefined interval primitive in addition to the behavior of identity types. 

The [[categorical semantics]] of path types in any of the above forms is the [[path space object]]. 

See also [[heterogeneous path type]]. 

category: disambiguation

[[!redirects path type]]
[[!redirects path types]]

[[!redirects weak path type]]
[[!redirects weak path types]]
[[!redirects strict path type]]
[[!redirects strict path types]]

[[!redirects path space type]]
[[!redirects path space types]]

[[!redirects weak path space type]]
[[!redirects weak path space types]]
[[!redirects strict path space type]]
[[!redirects strict path space types]]

[[!redirects stable path object]]
[[!redirects stable path objects]]