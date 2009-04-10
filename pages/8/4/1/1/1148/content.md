#Idea#

Using the [[Dold-Kan correspondence]] in [[Higher Topos Theory|higher topos theory]], [[complex]]es of [[abelian sheaf|abelian sheaves]] can be understood as a generalization of [[topological space]]s, in a precise sense recalled below. 
This induces a notion of cohomology of [[complex]]es of [[abelian sheaf|abelian sheaves]] from the familiar notion of cohomology of spaces.

Which is a simple one: recall that the [[cohomology]] of one [[topological space]] $X$ with coefficients in another space $A$ is nothing but the space of morphisms (continuous maps) $H(X,A) := [X,A]$ from $X$ to $A$ -- or, in a more restrictive sense traditionally adopted, the set $\Pi_0[X,A]$ of connected path components of this space. 

Similarly, when considering complexes of abelian sheaves in their natural [[Higher Topos Theory|higher topos theoretic]] home, the cohomology of a complex of sheaves $A$ on a space $X$ is nothing but the hom-space $H(X,A) = [X,A]$ -- where the space $X$ itself is regarded as a special case of a sheaf.

One reason this conceptually simple picture is not usually presented is that the space $X$ is typically not represented by an _abelian_ complex of sheaves, so that the full simplicity of the story becomes manifest only in general [[nonabelian cohomology]].

More precisely, via the [[Dold-Kan correspondence]] (non-negatively graded) [[complex]]es of [[abelian sheaf|abelian sheaves]] -- which are equivalently [[sheaf|sheaves]] with values in (non-negatively graded) [[category of chain complexes|categories of chain complexes]] -- can be regarded as special cases of [[simplicial presheaf|simplicial sheaves]]. But thanks to the [[model structure on simplicial presheaves|model category structure]] on the category of [[simplicial presheaf|simplicial sheaves]], this in turn is a model for the [[(infinity,1)-topos]] of  [[space and quantity|generalized spaces]] called [[infinity-stack]]s. The very point of $(\infty,1)$-[[(infinity,1)-topos|topoi]] is that they are [[(infinity,1)-category|(infintiy,1)-categories]] which behave in all structural aspects relevant for [[homotopy theory]] as the archetypical example [[Top]] does. In particular, as in [[Top]], the notion of [[cohomology]] in any [[(infinity,1)-topos]] simply coincides with that of [[hom-space]]s.

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
[[equivalence of categories|equivalent]] to $Sh(X, Sp(Ab))$, the category
of sheaves with values in [[combinatorial spectrum|combinatorial spectra]] 
internal to abelian groups.


Let how $F \in Sh(X,Ab)$ be a [[sheaf]] on a [[site]] $X$ with vlues in the category [[Ab]] of abelian groups.

For $n \in \mathbb{N}$ write $B^n F \in Sh(X, Ch_+(Ab))$ for the [[complex]] of [[sheaf|sheaves]] with values in abelian groups which is trivial everywhere except in degree $n$, where it is given by $F$.

By the [[Dold-Kan correspondence]] we can regard $B^n F$ equivalently as a complex of sheaves of abelian groups as well as sheaf with values in [[infinity-groupoid]]s.

Write $H$ for the [[(infinity,1)-category]] of 
[[simplicial presheaf|simplicial sheaves]] on $X$ and $H_{ab}$ for the 
[[(infinity,1)-category]] of complexes of [[abelian sheaf|abelian sheaves]] on $X$. 

Write $X$ for the terminal sheaf of $X$, i.e. for the [[sheaf]] that corresponds to the space $X$ itself. 

Then

$$
  H^n(X,A) := \pi_0 H(X,\mathbf{B}^n F)
$$

is the degree $n$ [[cohomology]] class of $X$ with values in $F$, regarded as computed in [[nonabelian cohomology]].

Now write $\mathbb{Z}[X]$ for the free abelianization of the sheaf $X$. This is the sheaf constant on the abelian group $\mathbb{Z}$ of integers. Then the above cohomology set, which of course happens to be a cohomology group here, due to the abelianness of $F$, is canonically isomorphic to the cohomology set

$$
  \cdots \simeq \pi_0 H_{ab}(\mathbb{Z}[X], \mathbf{B}^n F)
$$

which can be regarded as the [[hom-set]] in the [[derived category]] of [[complex]]es of [[abelian sheaf|abelian sheaves]]. This, in turn, is the same as the traditional expression

$$
  \cdots \simeq R^n \Gamma(X,F)
$$

giving the $n$th [[derived functor]] of the [[global section functor]] of the [[abelian sheaf]] $F$. 

This, finally, is the same group as obtained by choosing any [[complex]] $I_F$ of [[abelian sheaf|abelian sheaves]] that is [[injective complex|injective]] and [[quasi-isomorphism|quasi-isomorphic]] to $F$ regarded as a complex concentrated in degree 0 and then computing the $n$ [[homology]] group of the complex $\Gamma(X,I_F)$ of global sections of $F$:

$$
  \cdots \simeq H_n(\Gamma(X,I_F))
  \,.
$$ 

Historically the development of abelian sheaf cohomology was precisely in reverse order to this derivation from the general $(\infty,1)$-[[(infinity,1)-category|categorical]] [[cohomology]].

#Examples#

...

#References#

For a discussion of that and how abelian sheaf cohomology is  embedded into [[cohomology|generalized sheaf cohomology]] and
[[nonabelian cohomology]] see 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

The reformulation of abelian sheaf cohomology in terms
of hom-spaces $H(X,A)$ is in the list of observations on p. 9, culminating in the sequence of identities of
cohomologies and hom-spaces in the proof of theorem
2 on the bottom of page 10.

In this old article Ken Brown of ccourse uses a [[model category|1-categorical model]] for the [[(infinity,1)-category|(infinity,1)-categories]] $H$ and $H_{ab}$, namely a [[category of fibrant objects]].
