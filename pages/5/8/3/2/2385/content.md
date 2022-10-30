

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

Let [[CRing]] be the [[category]] of [[commutative ring]]s. For $R \in CRing$, write $I \in R$ for the [[nilradical]] of $R$, the [[ideal]] consisting of the nilpotent elements. The canonical projection $R \to R/I$ corresponds in the [[opposite category]] $Ring^{op}$ to the inclusion

$$
  Spec R/I \to Spec R
  \,.
$$ 

+-- {: .num_defn}
###### Definition

For $X \in PSh(Ring^{op})$ a [[presheaf]] on $Ring^{op}$ (for instance a [[scheme]]), its **de Rham space** $X_{dR}$ is the presheaf defined by

$$
  X_{dR} : Spec R \mapsto X(Spec R/I)
  \,.
$$

=--

## Properties

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
     X^{inf} \stackrel{\to}{\to} X
   \right)
  \,,
$$

of the two projections out of the formal neighbourhood of the diagonal.

=--


## Related concepts 


### Crystalline site

For $X : Ring \to Set$ a [[scheme]], the [[big site]] $Ring^{op}/X_{dR}$
of $X_{dR}$, is the [[crystaline site]] of $X$.

### Grothendieck connection

Morphisms $X_{dR} \to Mod$ encode flat higher [[connection on a bundle|connections]]: [[local system]]s.

Accordingly, [[descent]] for deRham spaces -- sometimes called **deRham descent** encodes flat 1-connections. This is described at [[Grothendieck connection]], 

### D-modules

The category of [[D-module]]s on a [[space]] is equivalent to that of [[quasicoherent sheaf|quasicoherent sheaves]] on the corresponding deRham space. 

Accordingly, quasicoherent $\infty$-stacks on the full $\Pi^{inf}(X)$ encode a higher categorical version of this, as discussed at [[schreiber:∞-vector bundle]].

### Infinitesimal path $\infty$-groupoids

* [[infinitesimal path ∞-groupoid]]

## References

The term _de Rham space_ or _de Rham stack_ apparently goes back to

* [[Carlos Simpson]], _Homotopy over the complex numbers and generalized de Rham cohomology_ Moduli of VectorBundles, M. Maruyama, ed., Dekker (1996), 229-263.

A review of the constructions is on the first two pages of

* [[Jacob Lurie]], _Notes on crystals and algebraic $\mathcal{D}$-modules_ (<a href="http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19(Crystals).pdf">pdf</a>)

The deRham space construction on spaces ([[scheme]]s) is described in [section 3, p. 7](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=7)

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

which goes on to assert the existence of its [[derived functor]] on the [[homotopy category]] $Ho Sh_\infty(C)$ of [[∞-stack]]s in proposition 3.3. on the same page.

The characterization of [[formally smooth scheme]] as above is also on that page.

See also online comments by [[David Ben-Zvi]]  [here](http://golem.ph.utexas.edu/category/2009/04/journal_club_geometric_infinit.html#c023287) and [here](http://golem.ph.utexas.edu/category/2009/08/question_on_synthetic_differen.html#c026218) on the $n$Caf&eacute;. and [here](http://mathoverflow.net/questions/10556/d-modules-derham-spaces-and-microlocalization) on MO.



[[!redirects deRham space]]
[[!redirects de Rham spaces]]