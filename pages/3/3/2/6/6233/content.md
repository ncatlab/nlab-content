
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $X$ a [[scheme]], analogous to how an $X$-scheme is a [[scheme]] $E \to X$ over $X$, a _$\mathcal{D}_X$-scheme_ is a scheme over the [[de Rham space]] $\mathbf{\Pi}_{inf}(X)$ of $X$.

See also [[diffiety]].

## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[scheme]], a _$\mathcal{D}_X$-scheme_ is a [[scheme]] $E \to \mathbf{\Pi}_{inf}(X)$ over the [[de Rham space]] $\mathbf{\Pi}_{inf}(X)$ of $X$.

=--

+-- {: .num_remark}
###### Remark

This definition makes sense in much greater generality: in any context of [[differential cohesion]].

=--


## Properties

### Relation to D-modules

+-- {: .num_defn}
###### Definition

In the [[sheaf topos]] over [[affine scheme]]s, an
$X$-affine $\mathcal{D}_X$-scheme is a [[commutative monoid]] object in the [[monoidal category]] of [[quasicoherent sheaves]] $QC(\mathbf{\Pi}_{inf}(X))$, which is equivalently the category of [[D-module]]s over $X$:

$$
  Aff \mathcal{D}_X Scheme \simeq CMon(\mathcal{D}Mod(X))
  \,.
$$ 

=--

This is ([BeilinsonDrinfeld, section 2.3](#BeilinsonDrinfeld)).

+-- {: .num_prop}
###### Proposition

This is indeed equivalent to the above abstract definition

=--

This appears as ([Lurie, theorem, 0.6 and below remark 0.7](#Lurie)) 

### Relation to jet schemes

The [[free functor|free]] $\mathcal{D}_X$-scheme on a given $X$-scheme $E \to X$ is the [[jet bundle]] of $E$. 

This is ([BeilinsonDrinfeld, 2.3.2](#BeilinsonDrinfeld)).

This fact makes $\mathcal{D}$-geometry a natural home for [[variational calculus]].


## Related concepts

* [[scheme]]

* [[D-module]]

* [[de Rham space]]

* [[diffiety]]

## References


The definition in terms of monoids in [[D-module]]s is in section 2.3 in

* {#BeilinsonDrinfeld} [[Alexander Beilinson]] and [[Vladimir Drinfeld]], _[[Chiral Algebras]]_
 
  _chapter 2, Geometry of D-schemes_ ([pdf](http://www.math.uchicago.edu/~mitya/langlands/chiral/cha_ch2.pdf))


The observation that this is equivalent to the abstract definition given above appears in pages 5 and 6 of

* {#LurieCrystal} [[Jacob Lurie]], *Notes on crystals and algebraic $\mathcal{D}$-modules* (2010) &lbrack;[[Lurie-NotesOnCrystals.pdf:file]]&rbrack;
 

[[!redirects D-schemes]]