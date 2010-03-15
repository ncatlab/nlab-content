
# &#268;ech model structure on simplicial presheaves

Among the various [[model structure on simplicial presheaves|model structures on simplicial presheaves]] (see there for details, background and motivation), the _&#268;ech_ model structure is in between the [[global model structure on simplicial presheaves]] and the [[local model structure on simplicial presheaves]]. The latter is obtained by localizing the global structure at local weak equivalences -- in particular [[hypercovers]] -- , while the &#268;ech structure is obtained by localizing only at [[?ech covers]].

Accordingly, the [[(∞,1)-topos]] [[presentable (infinity,1)-category|presented]] by the &#268;ech model structure has as its [[cohomology]] theory [[?ech cohomology]].

See the further remarks at [[hypercover]].

+--{: .query}
[[Mike Shulman]]: Two questions, one (hopefully) easy and one (perhaps) hard:

1. Is there a Quillen equivalent &#268;ech model structure on simplicial *sheaves*?  Can we just lift the model structure for simplicial presheaves along the sheafification adjunction?

1. Is there a characterization of the weak equivalences in either &#268;ech model structure?

I am particularly interested in this for the following reason.  According to Beke in *Sheafifiable homotopy model categories*, the weak equivalences in the [[local model structure on simplicial sheaves]] are precisely those maps $f\colon X\to Y$ of simplicial objects in the corresponding 1-topos of sheaves of sets such that the statement "$f$ is a weak equivalence of simplicial sets" is true in the [[internal logic]] of the topos (at least, interperiting "$f$ is a weak equivalence of simplicial sets" by one particular set of geometric sentences whose interpretation in $Set$ is equivalent to saying that a simplicial map is a weak equivalence).  But if, as [[HTT]] teaches us, &#268;ech descent is often to be preferred to hyperdescent, then we should be interested in &#268;ech weak equivalences instead.  So I would really like to know what it means for a map of simplicial sheaves to be a &#268;ech weak equivalence, in the *internal logic* of the 1-topos of sheaves of sets.  If nothing else, I think such a characterization would help me understand the real meaning of [[hypercompletion]].  But any sort of characterization of them would be better than none.
=--


## References

A detailed though unfinished account of the &#268;ech model structure is given in

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

But beware of this document is unfinished. In particular there is some statement somewhere that makes it sound as if &#268;ech covers are equal to hypercovers, while the rest of the text emphasises how they are distinct.


[[!redirects ?ech model structure on simplicial presheaves]]
[[!redirects Cech model structure on simplicial presheaves]]
[[!redirects ?ech model structure on simplicial presheaves]]
