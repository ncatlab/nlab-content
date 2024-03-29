

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

In a context of [[synthetic differential geometry]] or [[D-geometry]], the _de Rham space_ $dR(X)$ of a [[space]] $X$ is the [[quotient]] of $X$ that identifies [[infinitesimal object|infinitesimally close points]].

It is the [[coreduced object|coreduced reflection]] of $X$.

## Definition 

### On $Rings^{op}$

Let [[CRing]] be the [[category]] of [[commutative rings]]. For $R \in CRing$, write $I \in R$ for the [[nilradical]] of $R$, the [[ideal]] consisting of the nilpotent elements. The canonical [[projection]] $R \to R/I$ to the [[quotient]] by the ideal corresponds in the [[opposite category]] $Ring^{op}$ to the inclusion

$$
  Spec (R/I) \to Spec R
$$ 

of the [[reduced object|reduced]] part of $Spec R$.

+-- {: .num_defn}
###### Definition

For $X \in PSh(Ring^{op})$ a [[presheaf]] on $Ring^{op}$ (for instance a [[scheme]]), its **de Rham space** $X_{dR}$ is the presheaf defined by

$$
  X_{dR} : Spec R \mapsto X\left(Spec \left(R/I\right)\right)
  \,.
$$

=--

## Properties

### As a quotient

+-- {: .num_prop}
###### Proposition

If $X \in PSh(Ring^{op})$ is a [[smooth scheme]] then the canonical morphism

$$
  X \to X_{dR}
$$

is an [[epimorphism]] (hence an epimorphism over each $Spec R$) and therefore in this case $X_{dR}$ is the [[quotient]] of the relation "being infinitesimally close" between points of $X$: we have that $X_{dR}$ is the [[coequalizer]]

$$
  X_{dR} = \lim_\to 
   \left(
     X^{inf} \stackrel{\longrightarrow}{\longrightarrow} X
   \right)
  \,,
$$

of the two projections out of the [[formal neighbourhood of the diagonal]].

=--


### Relation to jet bundles

For $E \to X$ a [[bundle]] over $X$, its [[direct image]] under [[base change]] along the projection map $X \longrightarrow \Pi_{inf} X$ yields its _[[jet bundle]]_. See there for more.

+-- {: .num_remark}
###### Remark

In terms of [[differential homotopy type theory]] this means that
forming "jet types" of [[dependent types]] over $X$ is the 
[[dependent product]] operation along the unit of the [[infinitesimal shape modality]] 

$$
  jet(E) \coloneqq \underset{X \to \Pi_{inf}X}{\prod} E
  \,.
$$

=--

### Relation to formally &#233;tale morphisms of schemes

* [[formally étale morphism of schemes]]

## Related concepts 


### Crystalline site

For $X : Ring \to Set$ a [[scheme]], the [[big site]] $Ring^{op}/X_{dR}$
of $X_{dR}$, is the [[crystalline site]] of $X$.

### Grothendieck connection

Morphisms $X_{dR} \to Mod$ encode flat higher [[connection on a bundle|connections]]: [[local system]]s.

Accordingly, [[descent]] for de Rham spaces -- sometimes called **de Rham descent** encodes flat 1-connections. This is described at [[Grothendieck connection]], 

### D-modules

The category of [[D-module]]s on a [[space]] is equivalent to that of [[quasicoherent sheaf|quasicoherent sheaves]] on the corresponding de Rham space
([Lurie, above theorem  0.4](#LurieCrystal)).


### Infinitesimal path $\infty$-groupoids

* [[infinitesimal path ∞-groupoid]]

## References

The term _de Rham space_ or _de Rham stack_ apparently goes back to

* {#Simpson96} [[Carlos Simpson]], _Homotopy over the complex numbers and generalized de Rham cohomology_, Toulouse preprint no. 50, April 1995, In: M. Maruyama, (ed.) _Moduli of Vector Bundles (Taniguchi symposium December 1994)_,  Lecture notes in Pure and Applied Mathematics, Issue 189, Page 229-264, Dekker (1996), 229-263 ([web](https://www.tib.eu/en/search/id/BLCP%3ACN013382849/Homotopy-Over-the-Complex-Numbers-and-Generalized/))

But actually there it just has the notation "$X_{dR}$" and then the functor it co-represents is called the "de Rham shape" of $X$.

A review of the constructions is on the first two pages of

* {#LurieCrystal} [[Jacob Lurie]], *Notes on crystals and algebraic $\mathcal{D}$-modules* (2010) &lbrack;[[Lurie-NotesOnCrystals.pdf:file]]&rbrack;

The de Rham space construction on spaces ([[schemes]]) is described in [section 3, p. 7](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=7)

* {#SimpsonTeleman} [[Carlos Simpson]], [[Constantin Teleman]], _de Rham theorem for $\infty$-stacks_, 1997 ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf), [[SimpsonTelemanDeRhamTheoremForStacks.pdf:file]])
 
which goes on to assert the existence of its [[derived functor]] on the [[homotopy category]] $Ho Sh_\infty(C)$ of [[∞-stack]]s in proposition 3.3. on the same page.

Similar discussion in a context of [[derived algebraic geometry]] is in 

* [[Dennis Gaitsgory]], [[Nick Rozenblyum]], section 1 of _Crystals and D-modules_ ([pdf](http://www.math.harvard.edu/~gaitsgde/GL/Crystalstext.pdf))

The characterization of [[formally smooth scheme]] as above is also on that page.

See also online comments by [[David Ben-Zvi]]  [here](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023287) and [here](http://golem.ph.utexas.edu/category/2009/08/question_on_synthetic_differen.html#c026218) on the $n$Caf&eacute;. and [here](http://mathoverflow.net/questions/10556/d-modules-derham-spaces-and-microlocalization) on MO.



[[!redirects deRham space]]
[[!redirects de Rham spaces]]

[[!redirects de Rham stack]]
[[!redirects de Rham stacks]]

[[!redirects de Rham shape]]
