<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

The [[cohomology]] $H^n(X,F)$ of a [[topological space]] $X$ with values in a [[sheaf]] of abelian groups $F$ was originally defined as the value of the right [[derived functor]] of the global section functor.

But by embedding sheaves with values in abelian groups as special cases of [[simplicial presheaf|simplicial presheaves]] into the more general context of [[infinity-groupoid]] valued sheaves via the [[Dold-Kan correspondence]] and thus the abelian sheaf cohomology into the more general context of [[nonabelian cohomology]], this definition becomes equivalent to a special case of the general notion of [[nonabelian cohomology]] defined simply as the set of homotopy classes of maps

$$
  H^n(X,F) = [X,\mathbf{B}^n F]
$$

from the space $X$ regarded as a ("nonabelian"!) sheaf. 

The relation of this more conceptual and more general point of view on abelian sheaf cohomology to the original definition was originally clarified in 

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

(whose proof is reproduced below). 

With the modern understanding of the [[model structure on simplicial presheaves]] as a [[presentable (infinity,1)-category|presentation]] of the [[(infinity,1)-category of (infinity,1)-sheaves]] this says that ordinary abelian sheaf cohomology in fact computes the isomorphism classes of the [[infinity-stackification]] of a sheaf with values in complexes of abelian groups.

### more details on this idea ###

Using the [[Dold-Kan correspondence]] in [[Higher Topos Theory|higher topos theory]], [[complex]]es of [[abelian sheaf|abelian sheaves]] can be understood as a generalization of [[topological space]]s, in a precise sense recalled below. 
This induces a notion of cohomology of [[complex]]es of [[abelian sheaf|abelian sheaves]] from the familiar notion of cohomology of spaces.

Which is a simple one: recall that the [[cohomology]] of one [[topological space]] $X$ with coefficients in another space $A$ is nothing but the space of morphisms (continuous maps) $H(X,A) := [X,A]$ from $X$ to $A$ -- or, in a more restrictive sense traditionally adopted, the set $\Pi_0[X,A]$ of connected path components of this space. 

Similarly, when considering complexes of abelian sheaves in their natural [[Higher Topos Theory|higher topos theoretic]] home, the cohomology of a complex of sheaves $A$ on a space $X$ is nothing but the hom-space $H(X,A) = [X,A]$ -- where the space $X$ itself is regarded as a special case of a sheaf.

One reason this conceptually simple picture is not usually presented is that the space $X$ is typically not represented by an _abelian_ complex of sheaves, so that the full simplicity of the story becomes manifest only in general [[nonabelian cohomology]].

More precisely, via the [[Dold-Kan correspondence]] (non-negatively graded) [[complex]]es of [[abelian sheaf|abelian sheaves]] -- which are equivalently [[sheaf|sheaves]] with values in (non-negatively graded) [[category of chain complexes|categories of chain complexes]] -- can be regarded as special cases of [[simplicial presheaf|simplicial sheaves]]. But thanks to the [[model structure on simplicial presheaves|model category structure]] on the category of [[simplicial presheaf|simplicial sheaves]], this in turn is a model for the [[(infinity,1)-topos]] of  [[space and quantity|generalized spaces]] called [[infinity-stack]]s. The very point of $(\infty,1)$-[[(infinity,1)-topos|topoi]] is that they are [[(infinity,1)-category|(infintiy,1)-categories]] which behave in all structural aspects relevant for [[homotopy theory]] as the archetypical example [[Top]] does. In particular, as in [[Top]], the notion of [[cohomology]] in any [[(infinity,1)-topos]] simply coincides with that of [[hom-space]]s.

In the 1-categorical [[model category|model theoretic models]] these hom-spaces are computed technically by [[derived functor]]s. More precisely, the Hom-space $[X,A]$ for $X$ an ordinary space computes the [[global section]]s $\Gamma(X,A)$ of the complex of [[abelian sheaf|abelian sheaves]] $A$ which is computed by the [[derived global section functor]] $R \Gamma(X,-)$ of the [[global section functor]] $\Gamma(X,-)$, which does exist entirely within the abelian context.

This, then, is the definition of sheaf cohomology as usually presented: the cohomology of the complex $R \Gamma(X,A)$.


##Brown's theorem: abelian sheaf cohomology as a special case of nonabelian cohomology##

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

+-- {: .un_theorem}
###### Theorem (K. Brown, 1973)

Let $X$ be a [[topological space]], $F$ a [[sheaf]] on (the [[category of open subsets]] of) $X$ with values in abelian groups, and $\mathbf{B}^n F = K(F,n)$ the image of the complex of abelian sheaves $F[n]$ ($F$ in degree $n$, trivial elsewhere) under the [[Dold-Kan correspondence]] in sheaves with values in [[Kan complex]]es
$$
  \Gamma \circ (-) : Sh(X,Ch_+(Ab)) \to Sh(X, AbSimpGrp)
$$
$$
  F[n] \mapsto K(F,n) =: \mathbf{B}^n F
  \,.
$$

Then we have the following natural isomorphism of cohomologies:

$$
  H^n(X,F) \simeq H(X, \mathbf{B}^n F)
$$

where

* on the left we have ordinary abelian sheaf cohomology defined as the right [[derived functor]] of the global sections functor
  $$
    H^n(X,F) := (R \Gamma_X)(F)
    \,;
  $$

* on the right we have [[nonabelian cohomology]], namely the hom-set in the [[homotopy category]] of Kan complex valued [[model structure on simplicial presheaves|simplicial sheaves]]
  $$
    H(X, \mathbf{B}^n F) := Ho_{Sh(X,\infty Grpd)}(X,\mathbf{B}^n X)
   \,.
  $$

=--

+-- {: .proof}
###### Proof

This is the first four steps in the proof of theorem 2 in [[BrownAHT]].

The proof proceeds along the following four steps, which we describe in more detail below:

$$
  \begin{aligned}
    H^n(X,F) & \simeq
     Ho_{Sh(X,Ch(Ab))}(\mathbb{Z}, F[n])
     \\
     & \simeq
     Ho_{Sh(X,Ch_+(Ab))}(\mathbb{Z}, F[n])
     \\
     & \simeq
     Ho_{Sh(X,AbSimpGrp)}(\mathbb{Z}X, K(F,n))
     \\
     & \simeq
     Ho_{Sh(X,\infty Grpd)}(X, K(F,n))
  \end{aligned}
$$

1. By the [[derived functor]] definition of sheaf cohomology, $H^n(X,F)$ is the cohomology of any complex of sheaves $I^\bullet \in Sh(X,Ch(Ab))$ that is [[injective object|injective]] and weakly equivalent to $F[n]$, $F[n] \stackrel{\simeq}{\to} I^\bullet$:
   $$
     H^n(X,F) \simeq H^0(I^\bullet(X))
     \,.
   $$  
   On the other hand, by the general formula for hom-sets in [[homotopy category|homtotopy categories]] obtained by localizing at the [[calculus of fractions|multiplicative system]] given by [[quasi-isomorphism]]s of complexes (e.g. def. 13.1.2 in [[Categories and Sheaves|CaS]]) we have
   $$
     Ho_{Sh(X,Ch(Ab))}(\mathbb{Z}, F[n])
     \simeq
     colim_{Y^\bullet \stackrel{\simeq}{\to} \mathbb{Z}} Hom_{K(Sh(X,Ab))}(Y, I^\bullet)
     \,.
   $$
   But due to the injectiveness of $I^\bullet$, the integrand on the right is constant (lemma 14.1.5 in [[Categories and Sheaves|CaS]]) and hence the colimit is isomorphic to $\cdots \simeq Hom_{K(Sh(X,Ab))}(\mathbb{Z}, I^\bullet) \simeq H^0(I^\bullet(X))$, as desired.

1. The second step uses that the inclusion functor
   $$
     Ho_{Sh(X,Ch_+(Ab))} \hookrightarrow Ho_{Sh(X,Ch(Ab))}
   $$
   is [[full and faithful functor|full and faithful]].
   This in turn follows from 

   * first observing that the inclusion 
     $S : Sh(X,Ch_+(Ab)) \hookrightarrow Sh(X, Ch(Ab))$ of
     chain complexes concentrated in non-negative degree
     into all complexes of sheaves is 
     [[full and faithful functor|full and faithful]] and
     has the obvious [[right adjoint]] 
     $T : Sh(X,Ch(Ab)) \to Sh(X, Ch_+(Ab))$ obtained by
     **t**runcating a complex.  

    * By inspection, or else by the general properties
     of [[adjoint functor]]s (see the list of properties
     given there) this implies that $Id \to T \circ S$
     is an [[isomorphism]]. This implies that also
     $Id \to Ho T \circ Ho S$ is an [[isomorphism]]. 
    * But by the adjoint functor lemma for homotopical 
     categories, $Ho S$ is also left adjoint to $Ho T$
     (since both preserve weak equivalences). So that
     once again with the general properties of 
     [[adjoint functor]]s it follows that 
     $Ho S$ is 
     [[full and faithful functor|full and faithful]].

        

1. The third step uses that the [[normalized chain complex]] functor $Sh(X,AbSimpGrp) \to Sh(X, Ch_+(Ab))$ is an [[equivalence of categories]] that preserves the respective weak equivalences and homotopies.

1. The fourth step finally uses that the [[stuff, structure, property|forgetful functor]] $Sh(X, SimpAbGrp) \to Sh(X, \infty Grpd)$ that only remembers the [[Kan complex]] underlying a [[simplicial group]] has a [[left adjoint]], the free abelian group functor $\mathbb{Z} : Sh(X,\infty Grpd) \to Sh(X, AbSimpGrp)$ (see [[Dold-Kan correspondence]] for details), and that preserves weak equivalences (see the discussion at [[simplicial group]] for more on that). 

=--

##Examples##

...

##References##

The ordinary definition of sheaf cohomology in terms of the right derived global section functor can be found recalled for instance in these notes:

* Ch&ecirc;nevert, Kassaei, _Sheaf Cohomology_ ([pdf](http://www.math.mcgill.ca/goren/SeminarOnCohomology/Sheaf_Cohomology.pdf))

* Cibotaru, _Sheaf cohomology_ ([pdf](http://www.nd.edu/~lnicolae/sheaves_coh.pdf))

Its discussion in the more general [[nonabelian cohomology]] and [[infinity-stack]] context emphasized above is due to

* K. Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]

A discussion of the [[Cech cohomology]] description of sheaf cohomology along the above lines is in

* Tibor Beke, _Higher Cech Theory_ ([web](http://www.math.uiuc.edu/K-theory/0646/), [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))
