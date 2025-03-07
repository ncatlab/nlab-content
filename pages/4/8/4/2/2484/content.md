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

In other words, according to viewpoint (2), a [[scheme]] may be identified with the [[sheaf]] it [[representable functor|represents]]; this sheaf is often called the _functor of points_ of the scheme.

To see this, note that by the [[Yoneda lemma]] a [[scheme]] may be identified with the [[sheaf]] it [[representable functor|represents]] on the gros [[Zariski site]] of [[schemes]]; and since any scheme admits an affine open cover, the [[comparison lemma]] says that [[sheaves]] on the [[site]] of all schemes may be identified with [[sheaves]] on the [[site]] of [[affine schemes]].

The functor of points approach has the advantage of making certain constructions much simpler (e.g. the [[fibered product]] in the category of schemes), and eliminating the need for certain constructions like the [[Zariski spectrum]]. In his famous [1973 Buffalo Colloquium talk](#Grothendieck73), [[Alexander Grothendieck]] urged that his earlier definition of scheme via [[locally ringed spaces]] should be abandoned in favour of the functorial point of view. This is recalled in [Lawvere 03](#Lawvere03):

> {#Lawvere16Quote} The 1973 Buffalo Colloquium talk by Alexander Grothendieck had as its main theme that the 1960 definition of scheme (which had required as a prerequisite the baggage of prime ideals and the spectral space, sheaves of local rings, coverings and patchings, etc.), should be abandoned AS the FUNDAMENTAL one and replaced by the simple idea of a good functor from rings to sets. The needed restrictions could be more intuitively and more geometrically stated directly in terms of the topos of such functors, and of course the ingredients from the "baggage" could be extracted when needed as auxiliary explanations of already existing objects, rather than being carried always as core elements of the very definition.

and in [Lawvere 16](#Lawvere16):

> [[Peter Gabriel]] $[$...$]$ had explained some of the same ideas at Oberwolfach in 1965-66, providing a context in which Grothendieck’s proposal seemed natural. For example, he emphasized the traditional view that the points of an algebraic space form a covariant functor on the category of field extensions of the base.

> Grothendieck’s advice in his Colloquium talk was that 1960 ingredients (like Zariski opens etc.) are easily extracted from the category of functors, when needed.

Of course, this functorial perspective generalizes to other kinds of [[geometry]] and even [[higher geometry]], the general perspective being known as _[[synthetic differential geometry]]_ or similar.  For discussion of functorial ([[higher differential geometry|higher]]) [[differential geometry]] see for instance at _[[smooth set]]_ ([[smooth ∞-groupoid]]), for discussion of functorial [[supergeometry]] see at _[[super formal smooth set]]_ ([[super formal smooth ∞-groupoid]]).

##Example

The functor from commutative rings to sets which sends a ring, $R$, to the set of simultaneous solutions in $R^n$ of a set of polynomials, $f_1, \ldots, f_k$ in $\mathbb{Z}[t_1, \ldots,t_n]$ corresponds to the affine scheme $X = Spec(\mathbb{Z}[t_1, \ldots,t_n]/(f_1, \ldots,f_k))$. These $R$-points are then equivalently the hom-space

$$
Hom_{schemes}(Spec(R), X).
$$

When $X = Spec(\mathbb{Z}[t])$, the functor of points is the [[forgetful functor]].

The functor which sends $R$ to the $R$-points of the projective space $\mathbb{P}^n$ corresponds to a non-affine scheme.

## Value added by the internal language of toposes

Typically, only field-valued points of a scheme are easy to describe. For                   instance, the functor $F$ describing projective $n$-space is given on fields by

$$
  F(K) 
  \;=\; 
  \text{the set of lines through the origin in} 
  \, K^{n+1} 
   \cong
  (K^{n+1} \setminus \{0\})/K^\times,                                                       $$  

whereas on general rings it is given by

$$
  F(R) 
  \;=\; 
  \text{the set of linear surjections}
  \, R^{n+1} 
  \twoheadrightarrow P,\text{where}
  \;P\, 
  \text{is projective, modulo isomorphism.}
$$

On the other hand, it is these more general kinds of points which impart a meaningful sense of cohesion on the field-valued points, so they can't simply be dropped from consideration.

We can resolve this tension by observing that the category of functors from rings to sets is a [[topos]] and therefore has an [[internal language]]. We can use this language to describe such functors (and later study their properties) in a naive, element-based way. For instance, the functor $F$ describing projective $n$-space can be given by either of the internal expressions
$$
  \text{the set of lines through the origin in}
  \; 
  U^{n+1}
  \quad\text{or}\quad
  (U^{n+1} \setminus \{0\})/U^\times,
$$
where $U$ is the forgetful functor (representing the [[affine line]]). Details on this approach are in Part III of [Blechschmidt 17](#Blechschmidt17).

## Related concepts

* [[gros topos]]

* [[space and quantity]]

* [[Z-functor]]

## References

The original idea is advertised in

* {#Grothendieck65} [[Alexander Grothendieck]], _Introduction au langage fonctoriel_, course in Algiers in November 1965, lecture notes by [[Max Karoubi]], ([pdf scan](http://webusers.imj-prg.fr/~leila.schneps/grothendieckcircle/GrothAlgiers.pdf), [[GrothendieckIntroductionLangageFonctoriel1965.pdf:file]])

* {#Grothendieck73} [[Alexander Grothendieck]], _Introduction to functorial algebraic geometry, part 1: affine algebraic geometry_, summer school in Buffalo, 1973, lecture notes by Federico Gaeta ([pdf scan](http://matematicas.unex.es/~navarro/res/ifag.pdf), [[GrothendieckIntrodFunctorialGeometryI1973.pdf:file]])

and has been re-emphasized in various forms in the writing of [[William Lawvere]], notably:

* {#Lawvere03} [[William Lawvere]], _Grothendieck's 1973 Buffalo Colloquium_, [Categories Mailing List](https://www.mta.ca/~cat-dist/), March 2003, ([cat-dist:03-3](https://www.mta.ca/~cat-dist/archive/2003/03-3)).

* {#Lawvere16} [[William Lawvere]], email to [[Adeel Khan]], March 2016 ([web excerpt](https://nforum.ncatlab.org/discussion/7521/functorial-geometry/?Focus=69419#Comment_69419))

For a pedagogical discussion of the advantages and disadvantages of teaching the functor of points approach, see

* Secret blogging seminar, _Algebraic geometry without prime ideals_, ([blog discussion](https://sbseminar.wordpress.com/2009/08/06/algebraic-geometry-without-prime-ideals/))

Discussion for [[supergeometry]]:

* [[Claudio Carmeli]], Lauren Caston, [[Rita Fioresi]], _Mathematical Foundations of Supersymmetry_, EMS Series of Lectures in Mathematics Volume: 15; 2011; 263 pp; ( [ISBN:978-3-03719-097-5](https://bookstore.ams.org/emsserlec-15/), [arXiv:0710.5742](https://arxiv.org/abs/0710.5742))


See also


* [[Michel Demazure]], [[Pierre Gabriel]], _Introduction to algebraic geometry and algebraic groups_, North-Holland Mathematics Studies Volume 39 (1980) ([ISBN:9780080871509](https://www.elsevier.com/books/introduction-to-algebraic-geometry-and-algebraic-groups/demazure/978-0-444-85443-8))

* [[Bertrand Toen]], _[[Master course on algebraic stacks]]_.

* {#Low16} [[Zhen Lin Low]], _Categories of spaces built from local models_, doctoral thesis (2016) ([web](https://www.repository.cam.ac.uk/handle/1810/256998),[doi.org/10.17863/CAM.384](https://doi.org/10.17863/CAM.384))

* {#Blechschmidt17}[[Ingo Blechschmidt]], _Using the internal language of toposes in algebraic geometry_, doctoral thesis (2017) ([web](https://rawgit.com/iblech/internal-methods/master/notes.pdf))

Exposition for [[differential geometry]], [[supergeometry]] and [[higher geometry]], with motivation from [[physics]]:

* [[Urs Schreiber]]: *[[schreiber:Higher Topos Theory in Physics]]*, [[Encyclopedia of Mathematical Physics 2nd ed]] **4** (2025) 62-76 \[<a href="https://doi.org/10.1016/B978-0-323-95703-8.00210-X">doi:10.1016/B978-0-323-95703-8.00210-X</a>, [arXiv:2311.11026](https://arxiv.org/abs/2311.11026)\]


[[!redirects functors of points]]

