A _symmetric monoidal category_ is a [[braided monoidal category]] for which the braiding 
$$ B_{x,y} : x \otimes y \to y \otimes x $$
satisfies an additional axiom:
$$ B_{y,x} B_{x,y} = 1_{x \otimes y}  $$
for all objects $x, y$.  Intuitively this says that switching things twice has no effect.

There is a [[strict 2-category]] SymmMonCat with:

* symmetric monoidal categories as objects,
* [[symmetric monoidal functors]] as morphisms, 
* [[symmetric monoidal natural transformations]] as 2-morphisms.

For definitions of all these concepts, see:

* John Baez, [Some definitions everyone should know](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).

For an elementary introduction to symmetric monoidal categories using string diagrams, see:

* John Baez and Mike Stay, [Physics, topology, logic and computation: a Rosetta Stone](http://math.ucr.edu/home/baez/rosetta.pdf).

Eventually we should include all these definitions and diagrams here!  I don't know a good way to do this yet.