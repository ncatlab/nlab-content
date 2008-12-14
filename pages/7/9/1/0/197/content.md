_DiGraph_ is the category of [[directed graph|directed graphs]].  We can define a directed graph to be a functor $G : X^{op} \to Set$ where $X^{op}$ is the category with an object $0$, an object $1$ and two morphisms $s,t : 1 \to 0$, along with identity morphisms.  This lets us efficiently define DiGraph as in $C$ as the category of [[presheaf|presheaves]] on $X$, where:

* objects are [[functor]]s $G: X^{op} \to C$,
* morphisms are [[natural transformation]]s between such functors.

In other words, $DiGraph$ is the [[functor category]] from this $X^{op}$ to [[Set]].

category: category