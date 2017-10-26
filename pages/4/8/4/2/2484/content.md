[[!redirects functor of points]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[algebraic geometry]], there are two equivalent ways of looking at a [[scheme]]: it may be viewed 

1. as a [[petit topos]] with a [[structure sheaf]] of [[commutative rings]], hence as a [[locally ringed space]], 

1. as an object of the [[gros topos]] of [[sheaves]] on the [[site]] of [[commutative rings]] (with [[étale topology]] or [[Zariski topology]]) satisfying the condition that it is covered by [[representable functor|representables]] via [[open maps]].

In other words, a [[scheme]] may be identified with the [[sheaf]] it [[representable functor|represents]]; this sheaf is often called the _functor of points_ of the scheme.

To see this, note that by the [[Yoneda lemma]] a [[scheme]] may be identified with the [[sheaf]] it [[representable functor|represents]] on the gros [[Zariski site]] of [[schemes]]; and since any scheme admits an affine open cover, the [[comparison lemma]] says that [[sheaves]] on the [[site]] of all schemes may be identified with [[sheaves]] on the [[site]] of [[affine schemes]].

The functor of points approach has the advantage of making certain constructions much simpler (e.g. the [[fibered product]] in the category of schemes), and eliminating the need for certain constructions like the [[Zariski spectrum]]. In his famous [1973 Buffalo Colloquium talk](#Grothendieck73), [[Alexander Grothendieck]] urged that his earlier definition of scheme via [[locally ringed spaces]] should be abandoned in favour of the functorial point of view.

Of course, the above discussion generalizes to other types of [[geometry]] and even [[higher geometry]], the general perspective being known as _[[synthetic differential geometry]]_ or similar.  For discussion of functorial ([[higher differential geometry|higher]]) [[differential geometry]] see for instance at _[[smooth set]]_ ([[smooth ∞-groupoid]]), for discussion of functorial [[supergeometry]] see at _[[super formal smooth set]]_ ([[super formal smooth ∞-groupoid]]).

##Example

The functor from commutative rings to sets which sends a ring, $R$, to the set of simultaneous solutions in $R^n$ of a set of polynomials, $f_1, \ldots, f_k$ in $\mathbb{Z}[t_1, \ldots,t_n]$ corresponds to the affine scheme $X = Spec(\mathbb{Z}[t_1, \ldots,t_n]/(f_1, \ldots,f_k))$. These $R$-points are then equivalently the hom-space

$$
Hom_{schemes}(Spec(R), X).
$$

The functor which sends $R$ to the points of the projective space $\mathbb{P}^n_R$ corresponds to a non-affine scheme.

## Related concepts

* [[gros topos]]

## References

* {#Grothendieck65} [[Alexander Grothendieck]], _Introduction au langage fonctoriel_, course in Algiers in November 1965, lecture notes by [[Max Karoubi]], ([pdf scan](http://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/GrothAlgiers.pdf))

* {#Grothendieck73} [[Alexander Grothendieck]], _Introduction to functorial algebraic geometry, part 1: affine algebraic geometry_, summer school in Buffalo, 1973, lecture notes by Federico Gaeta, [pdf scan](http://matematicas.unex.es/~navarro/res/ifag.pdf).


* {#Lawvere73} [[William Lawvere]], _Grothendieck's 1973 Buffalo Colloquium_, posting to the mailing list _categories@mta.ca_, [gmane archive](http://permalink.gmane.org/gmane.science.mathematics.categories/2228).

* [[Michel Demazure]], [[Pierre Gabriel]], _Introduction to algebraic geometry and algebraic groups_, North-Holland Mathematics Studies
Volume 39 (1980).

* [[Bertrand Toen]], _[[Master course on algebraic stacks]]_.

* {#Low16} [[Zhen Lin Low]], _Categories of spaces built from local models_, doctoral thesis (2016) ([web](https://www.repository.cam.ac.uk/handle/1810/256998),[doi.org/10.17863/CAM.384](https://doi.org/10.17863/CAM.384))

[[!redirects functors of points]]

