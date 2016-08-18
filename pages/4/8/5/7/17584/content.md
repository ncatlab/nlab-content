**Affine logic** is a [[substructural logic]] which omits the [[contraction rule]] but not the [[weakening rule]].

Categorically, affine logic is modeled by (symmetric) [[monoidal categories]] whose tensorial unit $I$ is [[terminal object|terminal]], also known as [[semicartesian monoidal categories]], an example of which is the category of [[affine spaces]], giving rise to the name of the logic.

A more general notion of model would be given by monoidal categories equipped with a natural (in $A$) family $A\to I$ of arrows implementing "weakening" at each object. However, such an interpretation is in general badly behaved, unless we additionally require the natural transformation given by the maps $A\to I$ to be *monoidal*, and it can be shown that this additional requirement already forces the tensorial unit to be terminal (specifically, this follows from the component at $I$ being the identity).

An example of the badly behaved case -- where the transformation is not monoidal, and the tensorial unit is not terminal -- is given by the category [[Rel]] of relations, with cartesian product as tensor product (i.e., with $Rel$ as [[cartesian bicategory]]). Here a natural family of relations $A\to I$ is given by picking empty relations everywhere.  In the corresponding interpretation of affine logic, any weakening yields an empty relation, which contradicts intuitive principles like for example that "adding a dummy variable to a proof and then substituting a closed term" should not change the semantics.

###Related concept

* Affine **BCK** [[combinatory logic]] 