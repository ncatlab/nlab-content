
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

## Joyal model structure ##

The Jardine local [[model structure on simplicial presheaves]] restricts to the standard [[model structure on simplicial sheaves]].  This restriction is a [[Quillen equivalence]], so that equipped with this model structure $SSh(C)$ is a [[models for ∞-stack (∞,1)-toposes|model]] for the [[hypercomplete (infinity,1)-topos]] over the site $C$.

Historically, [[Joyal]] constructed his model structure on simplicial sheaves first and [[Jardine]] later constructed his model structure on [[simplicial presheaves]].

## Local projective model structure

Blander proved that the category of simplicial sheaves
admits a model structure whose weak equivalences are the same as in the Joyal model structure and acyclic fibrations are the projective (i.e., degreewise) acyclic fibrations.

## Related concepts

* [[simplicial presheaf]]

* [[model structures on simplicial presheaves]]

## References

The original construction due to [[Joyal]] in 1984 is in

* [[André Joyal]], _Lettre d’André Joyal à Alexandre Grothendieck_, April 11, 1984, [PDF](https://webusers.imj-prg.fr/~georges.maltsiniotis/ps/lettreJoyal.pdf).

Discussion of the [[homotopy theory]] of [[simplicial objects]] in [[toposes]] using [[Cisinski model structures]]:

* [[Garth Warner]], *Homotopical Topos Theory* (2012) &lbrack;[pdf](https://sites.math.washington.edu//~warner/HTT_Warner.pdf), [[Waner-HomotopicalTopos.pdf:file]]&rbrack;

The last part of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

is announced to be about simplicial objects in toposes, but that part does not exist yet.

For more see at _[[simplicial presheaf]]_ and _[[model structure on simplicial presheaves]]_.


[[!redirects simplicial sheaves]]
