#Idea#

Using the [[Dold-Kan correspondence]] in [[Higher Topos Theory|higher topos theory]], [[complex]]es of [[abelian sheaf|abelian sheaves]] can be understood as a generalization of [[topological space]]s, in a precise sense recalled below. 
This induces a notion of cohomology of [[complex]]es of [[abelian sheaf|abelian sheaves]] from the familiar notion of cohomology of spaces.

Which is a simple one: recall that the [[cohomology]] of one [[topological space]] $X$ with coefficients in another space $A$ is nothing but the space of morphisms (continuous maps) $H(X,A) := [X,A]$ from $X$ to $A$ -- or, in a more restrictive sense traditiuonally adopted, the set $\pi_0[X,A]$ of connected path components of this space. 

Similarly, when considering complexes of abelian sheaves in their natural [[Higher Topos Theory|higher topos theoretic]] home, the cohomology of a complex of sheaves $A$ on a space $X$ is nothing but the hom-space $H(X,A) = [X,A]$ -- where the space $X$ itself is regarded as a special case of a sheaf.

One reason this conceptually simple picture is not usually presented is that the space $X$ is typically not represented by an _abelian_ complex of sheaves, so that the full simplicity of the story becomes manifest only in general [[nonabelian cohomology]].

More precisely, via the [[Dold-Kan correspondence]] (non-negatively graded) [[complex]]es of [[abelian sheaf|abelian sheaves]] -- which are equivalently [[sheaf|sheaves]] with values in (non-negatively graded) [[category of chain complexes|categories of chain complexes]] -- can be regarded as special cases of [[simplicial sheaf|simplicial sheaves]]. But thanks to the [[model structure on simplicial presheaves|model category structure]] on the category of [[simplicial presheaf|simplicial sheaves]], this in turn is a model for the [[(infinity,1)-topos]] of  [[space and quantity|generalized spaces]] called [[infinity-stack]]s. The very point of [[(infinity,1)-topos|(\infty,1)-topoi]] is that they are [[(infinity,1)-category|(infintiy,1)-categories]] which behave in all structural aspects relevant for [[homotopy theory]] as the archetypical example [[Top]] does. In particular, as in [[Top]], the notion of [[cohomology]] in any [[(infinity,1)-topos]] simply coincides with that of [[hom-spaces]].

In the 1-categorical [[model category|model theoretic models]] these hom-spaces are computed technically by [[derived functor]]s. More precisely, the Hom-space $[X,A]$ for $X$ an ordinary space computes the [[global section]]s $\Gamma(X,A)$ of the complex of [[abelian sheaf|abelian sheaves]] $A$ which is computed by the [[derived global section functor]] $R \Gamma(X,-)$ of the [[global section functor]] $\Gamma(X,-)$, which does exist entirely within the abelian context.

This, then, is the definition of sheaf cohomology as usually presented: the cohomology of the complex $R \Gamma(X,A)$.


#Details#

Under the [[Dold-Kan correspondence]] we have the following
identification of sheaves taking values in [[chain complex]]es
with sheaves taking values in [[infinity-groupoid]]s and
[[spectrum|spectra]], crucial for a conceptual understanding of
abelian sheaf cohomology:

let $X$ be a [[site]]

* the category $Sh(X, Ch_+(Ab))$ of non-negatively graded
[[chain complex]]es of [[abelian sheaf|abelian sheaves]] is
[[homotopical functor|homotopically]] [[equivalence|equivalent]]
to the category $Sh(X, sAb)$ of [[sheaf|sheaves]] with values in 
simplicial abelian groups (i.e. [[Kan complex]]es with strict abelian group structure);

* the category $Sh(X, Ch(Ab))$ of unbounded 
[[chain complex]]es of [[abelian sheaf|abelian sheaves]] is 
[[equivalence|equivalent]] to $Sh(X, Sp(Ab))$, the category
of sheaves with values in [[combinatorial spectrum|combinatorial spectra]] 
internal to abelian groups.


(...)


$$
  \begin{aligned}
    H^q(X,F)
    & \simeq
    [X, \mathbf{B}^q F]
  \end{aligned}
$$

#Examples#

...

#References#

For a discussion of that and how abelian sheaf cohomology is 
embedded into [[generalized sheaf cohomology]] and
[[nonabelian cohomology]] see 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

The reformulation of abelian sheaf cohomology in terms
of hom-spaces $[X,A]$ is in the list of observations on p. 9,
culminating in the sequence of identities of
cohomologies and hom-spaces in the proof of theorem
2 on the bottom of page 10.


