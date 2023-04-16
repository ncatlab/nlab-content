
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _locally ringed topos_ is a [[locally algebra-ed topos]] for the [[theory of local rings]].

## Definition

+-- {: .num_defn #InTermsOfStalks}
###### Definition

A [[ringed topos]] $(X, \mathcal{O}_X)$ with [[point of a topos|enough points]] (such as the [[sheaf topos]] over a [[topological space]]) is a **locally ringed topos** if all [[stalk]]s $\mathcal{O}_X(x)$ are [[local ring]]s.

=--

This is a special case of the following equivalent definitions: 

+-- {: .num_defn #InTermsOfGeometricTheory}
###### Definition 

A **locally ringed topos** is a topos equipped with a commutative ring object (see [[ringed topos]]) that in addition satisfies the axioms 

* $(0 = 1) \vdash false$ 
* $x + y = 1 \vdash \exists_z (x z = 1) \vee \exists_z (y z = 1)$ 

(note these are axioms for a [[geometric theory]], interpreted according to [[Kripke-Joyal semantics]] in a topos). 

=--

+-- {: .num_defn #InTermsOfClassifyingTopos}
###### Definition

A [[ringed topos]] $(X, \mathcal{O}_X)$ is a [[locally algebra-ed topos]] for the [[theory of local rings]]: 

* a [[topos]] $X$

* equipped with a [[geometric morphism]]

  $$
    X \stackrel{\overset{\mathcal{O}_X}{\leftarrow}}{\underset{}{\to}}
    Sh(CRing^{op}_{fp}, Z )
  $$

  into the [[Zariski topos]], the  [[classifying topos]] for the [[theory of local rings]].

=--

## Properties

+-- {: .num_prop}
###### Proposition

Definition \ref{InTermsOfStalks} is indeed a special case of def. \ref{InTermsOfClassifyingTopos}.

=--

This is for instance in [Johnstone (2002)](#Johnstone2002) and in [Lurie (2009), remark 2.5.11](#Lurie2009)


## Related concepts

* [[Cole's theory of spectrum]]

* [[ringed space]], [[locally ringed space]]

* [[ringed site]], [[locally ringed site]]

* [[ringed topos]], **locally ringed topos**

* [[locally algebra-ed topos]]

* [[locally algebra-ed (∞,1)-topos]]

## References

Original references

* [[Alexander Grothendieck]], [[Jean-Louis Verdier]], *Topos annelés, localisation dans les topos annelés*, Section 11 in Exposé iv in: [[M. Artin]] et al., *Théorie des topos et cohomologie étale des schémas. Tome 1: Théorie des topos*, Séminaire de Géométrie Algébrique du Bois-Marie 1963–1964 ([[SGA 4]]), Lecture Notes in Mathematics __269__, Springer (1972) &lbrack;[doi:10.1007/BFb0081551](https://link.springer.com/book/10.1007/BFb0081551), [pdf](http://www.cmls.polytechnique.fr/perso/laszlo/sga4/SGA4-1/sga41.pdf)&rbrack;


* [[Monique Hakim]], Chapitre III in: *Topos annelés et schémas relatifs*, Ergebnisse der Mathematik und ihrer Grenzgebiete **64**, Springer (1972) &lbrack;[doi:10.1007/978-3-662-59155-0](https://doi.org/10.1007/978-3-662-59155-0)&rbrack; 

See also:
 
* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], Section VIII.6 ofL _[[Sheaves in Geometry and Logic]]_ (1992)

* {#Johnstone2002} [[Peter Johnstone]], _[[Sketches of an Elephant]]_ (2002)
 
* {#Lurie2009} [[Jacob Lurie]], Section 2.5 of: _[[Structured Spaces]]_ (2009)
 
* {#deJong} [[Aise Johan de Jong]], Section 14.33 of: _[[The Stacks Project]]_ ([pdf](http://www.math.columbia.edu/algebraic_geometry/stacks-git/book.pdf)) ([project website](http://www.math.columbia.edu/algebraic_geometry/stacks-git/))



[[!redirects locally ringed toposes]]