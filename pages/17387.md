
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# The Quintet Construction
* table of contents
{:toc}

## Idea

A *quintet construction* is an operation that takes a "globular" categorical structure and produces a "cubical" one (see [[geometric shape for higher structures]]) in which the squares

$$ \array{ A & \overset{f}{\to} & B \\
^g\downarrow  & \swArrow & \downarrow^h\\
C & \underset{k}{\to} & D }$$

are morphisms between composites $\alpha:h\circ f \to k\circ g$.  The name arises because a square in the resulting cubical structure is formally a quintet $(f,g,h,k,\alpha)$ (since just knowing the globular cell $\alpha$ does not determine the decomposition of its domain and codomain as composites).

Hence given a [[2-category]] $\mathcal{C}$, it induces a [[double category]] $Sq(\mathcal{C})$ whose

* [[objects]] are the objects of $\mathcal{C}$;

* [[horizontal morphisms]] are the [[1-morphisms]] of $\mathcal{C}$;

* [[vertical morphisms]] are also the [[1-morphisms]] of $\mathcal{C}$;

* [[2-morphisms]] are the [[2-morphisms]] of $\mathcal{C}$ between the [[compositions]] of the [[1-morphisms]]. 


## Examples

* Quintets in a [[strict 2-category]] form a [[strict double category]].

* Quintets in a [[bicategory]] form a [[double bicategory]].

* Quintets in a [[Gray-category]] form an [[intercategory]].

* By a certain stretch of terminology, the singular [[cubical set]] of a [[topological space]] might be called a quintet construction.


## Applications

A quintet construction is a [[left adjoint]] to a functor that picks out the [[companion pairs]] in a cubical structure (see Theorem 1.7 in [Grandis and Paré](#GrandisPare04)).  Thus, functors *out* of quintet constructions are nothing new; but some interesting applications involve functors *into* quintet constructions from other cubical structures.  For instance:

* The assignment of [[homotopy categories]] and [[derived functors]] to [[model categories]] can be made into a [[double pseudofunctor]] from the [[double category of model categories]] to the double category of quintets in [[Cat]] ([this Prop.](double+category+of+model+categories#HomotopyDoublePseudofunctor)).  This implies that [[mates]] are preserved even when they relate composites of left and right [[Quillen functors]].

## References

The concept is due to 

* [[Charles Ehresmann]], _Catégorie double des quintettes; applications covariantes, C. R. A. S. Paris 256 (1963), 1891-1894._ and in [volume III](http://ehres.pagesperso-orange.fr/C.E.WORKS_fichiers/Ehresmann_C.-Oeuvres_III_1.pdf) in his collected works.

It appears spelled out also in

* {#BastianiEhresmann74} A. Bastiani, [[Charles Ehresmann]], pages 272-273 of  _Multiple functors. I. Limits relative to double categories_, Cah. Top. G&#233;om. Diff&#233;r. Cat&#233;g. 15 (1974) 215&#8211;292

* {#GrandisPare04} Grandis, Marco, and Robert Paré. "Adjoint for double categories." Cahiers de topologie et géométrie différentielle catégoriques 45.3 (2004): 193-240. [link](http://www.numdam.org/item/CTGDC_2004__45_3_193_0/)

[[!redirects quintet]]
[[!redirects quintets]]
[[!redirects quintet constructions]]
[[!redirects quintets in a 2-category]]
[[!redirects double category of quintets]]

[[!redirects double category of squares]]
[[!redirects double categories of squares]]
