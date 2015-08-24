
#Contents#
* table of contents
{:toc}

## Definition

A _simplicial sheaf_ $A$ is equivalently

* a [[simplicial object]] 

  $$
    A \in SSh(C) := [\Delta^{op}, Sh(C)]
  $$ 

  in a [[category of sheaves]] $Sh(C)$ for some [[site]] $C$;

* a [[simplicial presheaf]] 

  $$
    A \in SPSh(C) := [\Delta^{op}, PSh(C)] \simeq [\Delta^{op}, [C^{op}, Set]]
  $$

  that satisfies degreewise the [[sheaf]] condition;

* an [[SSet]]-valued [[presheaf]] 

  $$
    A \in PSh(C,SSet) := [C^{op}, SSet] \simeq [C^{op}, [\Delta^{op}, Set]]
  $$
 
  which, when regarded under the equivalence

  $$
    PSh(C,SSet) \simeq SPSh(C)
  $$

  is degreewise a [[sheaf]].

## Model structure ##

The Jardine-local [[model structure on simplicial presheaves]] restricts to the standard [[model structure on simplicial sheaves]].  This restriction is a [[Quillen equivalence]], so that equipped with this model structure $SSh(C)$ is a [[models for ∞-stack (∞,1)-toposes|model]] for the [[hypercomplete (infinity,1)-topos]] over the site $C$.

## References

A discussion of the [[homotopy theory]] of [[simplicial objects]] in [[toposes]] using [[Cisinski model structures]] is in 

* Garth Warner, _Homotopical topos theory_ ([pdf](http://www.math.washington.edu/~warner/HTT_Warner.pdf))

The last part of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

is announced to be about simplicial objects in toposes, but that part does not exist yet.

For more see at _[[simplicial presheaf]]_ and _[[model structure on simplicial presheaves]]_.


[[!redirects simplicial sheaves]]
