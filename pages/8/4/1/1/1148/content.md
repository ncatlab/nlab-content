
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

##Idea##

### General

The [[cohomology]] $H^n(X,F)$ of a [[topological space]] $X$ with values in a [[sheaf of abelian groups]] / [[abelian sheaf]] $F$ was originally defined as the value of the right [[derived functor]] of the [[global section]] functor, the [[derived direct image]] functor.

But by embedding sheaves with values in abelian groups as special cases of [[simplicial presheaf|simplicial sheaves]] into the more general context of [[(∞,1)-sheaves|∞-groupoid-valued sheaves]] via the [[Dold-Kan correspondence]] and thus the abelian sheaf cohomology into the more general context of the intrinsic [[nonabelian cohomology]] of an [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}(C)$, this definition becomes equivalent to a special case of the general notion of [[nonabelian cohomology]] defined simply as the set of homotopy classes of maps

$$
  H^n(X,F) = \pi_0 \mathbf{H}(X,\mathbf{B}^n F)
$$

from the space $X$ regarded a ("nonabelian"!) sheaf, to the [[Eilenberg-MacLane object]] in degree $n$, defined by $F$. 

The relation of this more conceptual and more general point of view on abelian sheaf cohomology to the original definition was originally clarified by [Brown 1973](#Brown1973) (whose proof is reproduced below). 

Brown constructed effectively the [[homotopy category of an (∞,1)-category|homotopy category]] of $\mathbf{H}$ using a model of a [[category of fibrant objects]] paralleling the  [[model structure on simplicial presheaves]] as a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]]. This says that ordinary abelian sheaf cohomology in fact computes the equivalence classes of the [[∞-stackification]] of a sheaf with values in [[chain complexes]] of [[abelian groups]].

The general [[(∞,1)-topos]]-theoreric perspective on cohomology is described in more detail at [[cohomology]]. The details on how to realize abelian sheaf cohomology as an example of this are discussed below.

### More details on this idea ###

Using the [[Dold-Kan correspondence]] in [[higher topos theory]], [[complex]]es of [[abelian sheaf|abelian sheaves]] can be understood as a generalization of [[topological space]]s, in a precise sense recalled below. 
This induces a notion of cohomology of [[complex]]es of [[abelian sheaf|abelian sheaves]] from the familiar notion of cohomology of spaces.

Which is a simple one: recall that the [[cohomology]] of one [[topological space]] $X$ with coefficients in another space $A$ is nothing but the space of morphisms (continuous maps) $H(X,A) := [X,A]$ from $X$ to $A$ -- or, in a more restrictive sense traditionally adopted, the set $\Pi_0[X,A]$ of connected path components of this space. 

Similarly, when considering [[chain complexes]] of [[abelian sheaves]] in their natural [[higher topos theory|higher topos theoretic]] home, the cohomology of a complex of sheaves $A$ on a space $X$ is nothing but the hom-space $H(X,A) = [X,A]$ -- where the space $X$ itself is regarded as a special case of a sheaf.

One reason this conceptually simple picture is not usually presented is that the space $X$ is typically not represented by an _abelian_ complex of sheaves, so that the full simplicity of the story becomes manifest only in general [[nonabelian cohomology]].

More precisely, via the [[Dold-Kan correspondence]] (non-negatively graded) [[complex]]es of [[abelian sheaf|abelian sheaves]] -- which are equivalently [[sheaf|sheaves]] with values in (non-negatively graded) [[category of chain complexes|categories of chain complexes]] -- can be regarded as special cases of [[simplicial presheaf|simplicial sheaves]]. But thanks to the [[model structure on simplicial presheaves|model category structure]] on the category of [[simplicial presheaf|simplicial sheaves]], this in turn is a model for the [[(infinity,1)-topos]] of  [[space and quantity|generalized spaces]] called [[infinity-stack]]s. The very point of $(\infty,1)$-[[(infinity,1)-topos|topoi]] is that they are [[(infinity,1)-category|(infintiy,1)-categories]] which behave in all structural aspects relevant for [[homotopy theory]] as the archetypical example [[Top]] does. In particular, as in [[Top]], the notion of [[cohomology]] in any [[(infinity,1)-topos]] simply coincides with that of [[hom-space]]s.

In the 1-categorical [[model category|model theoretic models]] these hom-spaces are computed technically by [[derived functor]]s. More precisely, the Hom-space $[X,A]$ for $X$ an ordinary space computes the [[global section]]s $\Gamma(X,A)$ of the complex of [[abelian sheaf|abelian sheaves]] $A$ which is computed by the right [[derived functor]] of the [[global section]] $R \Gamma(X,-)$ of the [[global section functor]] $\Gamma(X,-)$, which does exist entirely within the abelian context.

This, then, is the definition of sheaf cohomology as usually presented: the cohomology of the complex $R \Gamma(X,A)$.

## Properties

### As intrinsic (∞,1)-topos cohomology 
 {#AsIntrinsicInfinityToposCohomology}


Under the ([[stable Dold-Kan correspondence|stable]]) [[Dold-Kan correspondence]] we have the following identification of sheaves taking values in [[chain complexes]] with sheaves taking values in [[infinity-groupoids]] and [[spectrum|spectra]], crucial for a conceptual understanding of abelian sheaf cohomology.

Let $X$ be a [[site]].

* The category $Sh(X, Ch_+(Ab))$ of non-negatively graded [[chain complex]]es of [[abelian sheaf|abelian sheaves]] is [[homotopical functor|homotopically]] [[equivalence|equivalent]] to the category $Sh(X, sAb)$ of [[sheaf|sheaves]] with values in simplicial abelian groups (i.e. [[Kan complex]]es with strict abelian group structure);

* The category $Sh(X, Ch(Ab))$ of unbounded [[chain complex]]es of [[abelian sheaf|abelian sheaves]] is [[equivalence of categories|equivalent]] to $Sh(X, Sp(Ab))$, the category of sheaves with values in [[combinatorial spectrum|combinatorial spectra]] internal to abelian groups.


Let how $F \in Sh(X,Ab)$ be a [[sheaf]] on a [[site]] $X$ with values in the category [[Ab]] of abelian groups.

For $n \in \mathbb{N}$ write $B^n F \in Sh(X, Ch_+(Ab))$ for the [[complex]] of [[sheaf|sheaves]] with values in abelian groups which is trivial everywhere except in degree $n$, where it is given by $F$.

By the [[Dold-Kan correspondence]] we can regard $B^n F$ equivalently as a complex of sheaves of abelian groups as well as sheaf with values in [[infinity-groupoid]]s.

Write $H$ for the [[(infinity,1)-category]] of 
[[simplicial presheaf|simplicial sheaves]] on $X$ and $H_{ab}$ for the 
[[(infinity,1)-category]] of complexes of [[abelian sheaf|abelian sheaves]] on $X$. 

Write $X$ for the terminal sheaf of $X$, i.e. for the [[sheaf]] that corresponds to the space $X$ itself. 

Then

$$
  H^n(X,A) \coloneqq \pi_0 H(X,\mathbf{B}^n F)
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

\begin{theorem}
**([Brown 1973](#Brown1973))**
\linebreak
Let $X$ be a [[topological space]], $F$ a [[sheaf]] on (the [[category of open subsets]] of) $X$ with values in abelian groups, and $\mathbf{B}^n F = K(F,n)$ the image of the complex of abelian sheaves $F[n]$ ($F$ in degree $n$, trivial elsewhere) under the [[Dold-Kan correspondence]] in sheaves with values in [[Kan complex]]es
$$
  \Gamma \circ (-) 
    \colon 
   Sh(X,Ch_+(Ab)) \to Sh(X, AbSimpGrp)
$$
$$
  F[n] \mapsto K(F,n) \eqqcolon \mathbf{B}^n F
  \,.
$$

Then we have the following [[natural isomorphism]] of cohomologies:

$$
  H^n(X,F) \simeq H(X, \mathbf{B}^n F)
  \,,
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

\end{theorem}
\begin{proof}
This is the first four steps in the proof of theorem 2 in [Brown 1973](#Brown1973).

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

\end{proof}

### Relation to derived direct images


+-- {: .num_prop}
###### Proposition

Let $f^{-1} \colon Y \to X$ be a [[morphism of sites]].
Then the $q$th [[derived functor]] $R^q f_\ast$ of the induced [[direct image]] functor sends $\mathcal{F} \in Ab(Sh(X_{et}))$ to the [[sheafification]] of the [[presheaf]]

$$
  U_Y
  \mapsto
  H^q(f^{-1}(U_Y), \mathcal{F})
  \,,
$$

where on the right we have the degree $q$ [[abelian sheaf cohomology]] [[cohomology group|group]] with [[coefficients]] in the given $\mathcal{F}$.


=--

(e.g. [Tamme, I (3.7.1), II (1.3.4)](#Tamme), [Milne, 12.1](#Milne)).

+-- {: .proof}
###### Proof

We have a [[commuting diagram]]

$$
  \array{
    Ab(PSh(X)) &\stackrel{(-)\circ f^{-1}}{\longrightarrow}& Ab(PSh(Y))
    \\
    \uparrow^{\mathrlap{inc}} && \downarrow^{L}
    \\
    Ab(Sh(X)) &\stackrel{f_\ast}{\longrightarrow}& Ab(Sh(Y))
  }
  \,,
$$

where the right vertical morphism is [[sheafification]]. Because $(-) \circ f^{-1}$ and $L$ are both [[exact functors]] it follows that for $I^\bullet \to \mathcal{F}$ an [[injective resolution]] that

$$
  \begin{aligned}
     R^p f_\ast(\mathcal{F})
     & :\simeq
     H^p( f_\ast I)
     \\
     & = H^p(L I^\bullet(f^{-1}(-)))
     \\
     & = L (H^p(I^\bullet)(f^{-1}(-)))
  \end{aligned}
$$

=--

## Examples

* [[de Rham cohomology]]

* [[Dolbeault cohomology]]

* [[Spencer cohomology]]

* [[Deligne cohomology]]

* [[etale cohomology]]

* [[crystalline cohomology]]

* [[syntomic cohomology]]

## Related concepts

* [[sheaf]], [[cohomology]]

* **abelian sheaf cohomology**

  * [[model structure on chain complexes]]

  * [[resolutions]]: [[soft sheaf]], [[fine sheaf]], [[flabby sheaf]]

  * [[triangulated category of sheaves]]

  * [[Verdier duality]]



## References 

Original texts:

* {#Godement58} [[Roger Godement]], *Topologie algébrique et theorie des faisceaux*, Hermann, Paris (1958) &lbrack;[webpage](https://www.editions-hermann.fr/livre/topologie-algebrique-et-theorie-des-faisceaux-roger-godement), [[Godement-TopologieAlgebrique.pdf:file]]&rbrack;

Monographs:

* [[Ugo Bruzzo]]: _Derived Functors and Sheaf Cohomology_, Contemporary Mathematics and Its Applications: Monographs, Expositions and Lecture Notes: **2**, World Scientific (2020) &lbrack;[doi:10.1142/11473](https://doi.org/10.1142/11473)&rbrack;

* [[Jean Gallier]], [[Jocelyn Quaintance]]: *Homology, Cohomology, and Sheaf Cohomology for Algebraic Topology, Algebraic Geometry, and Differential Geometry*, World Scientific (2022) &lbrack;[doi:10.1142/12495](https://doi.org/10.1142/12495), [webpage](https://www.cis.upenn.edu/~jean/gbooks/sheaf-coho.html)&rbrack;


Lecture notes:

* Gabriel Ch&#234;nevert, Payman Kassaei: _Sheaf Cohomology_ (2003) &lbrack;[pdf](http://www.math.mcgill.ca/goren/SeminarOnCohomology/Sheaf_Cohomology.pdf)&rbrack;

* Daniel Cibotaru: _Sheaf cohomology_ (2005) &lbrack;[pdf](http://www.nd.edu/~lnicolae/sheaves_coh.pdf)&rbrack;

* [[Ieke Moerdijk]]: *Sheaf Cohomology for Locally Compact Spaces*, Lecture notes, Sheffield (2025) &lbrack;[[Moerdijk-SheafCohomology.pdf:file]]&rbrack;
 

Discussion in the more general context of [[nonabelian cohomology]] and [[infinity-stacks]] is due to:

* {#Brown1973} [[Kenneth Brown]]: _[[BrownAHT|Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_,  Transactions of the American Mathematical Society **186** (1973) 419-458 &lbrack;[jstor:1996573](http://www.jstor.org/stable/1996573)&rbrack;

This uses homotopical structures of a [[category of fibrant objects]] on complexes of abelian sheaves. Discussion of actual [[model structure on chain complexes]] of abelian sheaves is in 

* [[Mark Hovey]], _Model category structures on chain complexes of sheaves_, Trans. Amer. Math. Soc. 353, 6 ([pdf](http://www.mathaware.org/tran/2001-353-06/S0002-9947-01-02721-0/S0002-9947-01-02721-0.pdf))

A discussion of the [[Čech cohomology]] description of sheaf cohomology along the above lines is in

* [[Tibor Beke]], _Higher &#268;ech Theory_ ([web](http://www.math.uiuc.edu/K-theory/0646/), [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))


See also:

* {#Duskin79} [[John Duskin]], _Higher-dimensional torsors and the cohomology of topoi: the abelian theory_, p. 255-279 in: _Applications of sheaves_,  Lecture Notes in Mathematics **753**, Springer (1979) &lbrack;[doi:10.1007/BFb0061822](https://doi.org/10.1007/BFb0061822)&rbrack; 


* {#Tamme} [[Günter Tamme]], section II 1 of _[[Introduction to Étale Cohomology]]_
 

* {#Milne} [[James Milne]], section 7 of _[[Lectures on Étale Cohomology]]_
 


[[!redirects chain complex of sheaves]]
[[!redirects chain complexes of sheaves]]

[[!redirects sheaf of chain complexes]]
[[!redirects sheaves of chain complexes]]

[[!redirects abelian presheaf]]
[[!redirects abelian presheaves]]