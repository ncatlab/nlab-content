
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

An *Azumaya algebra* over a [[commutative unital ring]] $R$ is an [[associative algebra|algebra]] over $R$ that has an inverse up to [[Morita equivalence]].  That is, $A$ is an Azumaya algebra if there is an $R$-algebra $B$ such that $B \otimes_R A$ is Morita equivalent to $R$, which is the unit for the tensor product of $R$-algebras.   Thus, Morita equivalence classes of Azumaya algebras over $R$ form a group, which is called the [[Brauer group]] of $R$.

## Definition

### Traditional

In what follows, $R$ is a [[commutative unital ring]] and algebras over $R$ are assumed associative and unital but not necessarily commmutative.  An __Azumaya algebra__ over $R$ is an algebra $A$ over $R$ obeying any of the following equivalent conditions:

* There exists an $R$-algebra $B$ such that the [[tensor product]] of $R$-algebras $B \otimes_R A$ is [[Morita equivalence|Morita equivalent]] to $R$.

* The $R$-algebra $A^{\mathrm{op}} \otimes_R A$ is [[Morita equivalence|Morita equivalent]] to $R$, where $A^{\mathrm{op}}$ is the opposite algebra of $A$.

* The [[center]] of $A$ is $R$, and $A$ is a [[separable algebra]].

* As a left $R$-[[module]], $A$ finitely generated, faithful and [[projective object|projective]], and the canonical morphism $A\otimes_R A^{op}\to End_R(A)$ is an [[isomorphism]]. 

When $R$ is a field, an Azumaya algebra is the same as a [[central simple algebra]] over $R$.  

For any commutative ring $R$ there is a [[monoidal bicategory]] with

* algebras over $R$ as objects,
* bimodules as morphisms,
* bimodule homomorphisms as 2-morphisms. 

Given any monoidal bicategory we can take its [[core]]: that is, the sub-monoidal bicategory where we only keep objects invertible up to equivalence, morphisms invertible up to 2-isomorphism, and invertible 2-morphisms.  This core is a [[3-group]], sometimes called the [[Picard 3-group]], and it has [[Azumaya algebras]] over $R$ as its objects.

### Over a scheme

More generally, [[Grothendieck]] defines an __Azumaya algebra__ over a [[scheme]] $X$ as a [[sheaf]] $\mathcal{A}$ of $\mathcal{O}_X$-algebras such that for each point $x\in X$, the corresponding [[stalk]] $\mathcal{A}_x$ is an Azumaya $\mathcal{O}_{X,x}$-algebra. 

The [[Brauer group]] $Br(X)$ classifies Azumaya algebras over $X$ up to a suitably defined equivalence relation: $\mathcal{A}\sim\mathcal{B}$ if $\mathcal{A}\otimes_{\mathcal{O}_X} \mathbf{End}(\mathcal{E}) \cong \mathcal{B}\otimes_{\mathcal{O}_X}\mathbf{End}(\mathcal{F})$ for some locally free sheaves of $\mathcal{O}_X$-modules $\mathcal{E}$ and $\mathcal{F}$ of finite rank.  The group operation of $Br(X)$ is induced by the tensor product. The Brauer group can be reexpressed in terms of second [[nonabelian cohomology]]; indeed a sheaf of Azumaya algebras over $X$ determines an $\mathcal{O}_X^*$-[[gerbe]] (or $U(1)$-gerbe in the [[manifold]] context).  

[[Karoubi K-theory]] involves an element in a Brauer group and in the original Karoubi--Donovan paper is related to a twisting with a "local system" which involves Azumaya algebras.

### In terms of (derived) &#233;tale cohomology
 {#InTermsOfEtaleCohomology}

For $R$ a [[ring]] and $H^n_{et}(-,-)$ the [[etale cohomology]], $\mathbb{G}_m$ the [[multiplicative group]] of the [[affine line]]; then

* $H^0_{et}(R, \mathbb{G}_m) = R^\times$ ([[group of units]])

* $H^1_{et}(R, \mathbb{G}_m) = Pic(R)$ ([[Picard group]]: iso classes of invertible $R$-modules)

* $H^2_{et}(R, \mathbb{G}_m)_{tor} = Br(R)$ ([[Brauer group]] Morita classes of Azumaya $R$-algebras)

More generally, this works for $R$ a (connective) [[E-infinity ring]] 
(the following is due to [[Benjamin Antieau]] and [[David Gepner]]). 

Let $GL_1(R)$ be its [[infinity-group of units]]. 
If $R$ is [[connective spectrum|connective]], then the first [[Postnikov tower|Postikov stage]] of the [[Picard group|Picard]] [[infinity-groupoid]]

$$
  Pic(R) \coloneqq Mod(R)^\times
$$

is
 
$$
  \array{
   \mathbf{B}_{et} GL_1(-) &\to& Pic(-)
   \\
   && \downarrow
   \\
   && \mathbb{Z}
  }
  \,,
$$

where the top morphism is the inclusion of locally free $R$-modules.

so $H^1_{et}(R, GL_1)$ is not equal to $\pi_0 Pic(R)$, but it is off only by $H^0_{et}(R, \mathbb{Z}) = \prod_{components of R} \mathbb{Z}$.

Let $Mod_R$ be the [[(infinity,1)-category]] of $R$-[[module spectra|modules]].

There is a notion of $Mod_R$-[[enriched (infinity,1)-category]], of "$R$-linear $(\infty,1)$-categories".

$Cat_R \coloneqq Mod_R$-modiles in [[presentable (infinity,1)-categories]].

Forming module $(\infty,1)$-categories is then an [[(infinity,1)-functor]]

$$
  Alg_R \stackrel{Mod}{\to} Cat_R
$$

Write $Cat'_R \hookrightarrow Car_R$ for the image of $Mod$.  Then define the [[Brauer group|Brauer]] [[infinity-group]] to be

$$
  Br(R) \coloneqq (Cat'_R)^\times
$$

One shows (Antieau-Gepner) that this is exactly the Azumaya $R$-algebras modulo Morita equivalence.

**Theorem** (B. Antieau, D. Gepner) 

1. For $R$ a connective $E_\infty$ ring, any Azumaya $R$-algebra $A$ is &#233;tale locally trivial: there is an [[etale topology|etale cover]] $R \to S$ such that $A \wedge_R S \stackrel{Morita \simeq}{\to} S$.

   (Think of this as saying that an Azumaya $R$-algebra is &#233;tale-locally a Matric algebra, hence Morita-trivial: a "bundle of compact operators" presenting a (torsion) $GL_1(R)$-2-bundle).

1. $Br : CAlg_R^{\geq 0} \to Gpd_\infty$ is a sheaf for the [[etale cohomology]].

**Corollary** 

1. $Br$ is [[connected object in an (infinity,1)-topos|connected]]. Hence $Br \simeq \mathbf{B}_{et} \Omega Br $.

1. $\Omega Br \simeq Pic$, hence $Br \simeq \mathbf{B}_{et} Pic$

  
[[Postnikov tower]] for $GL_1(R)$:

$$
  for\; n \gt 0: \pi_n GL_1(S) \simeq \pi_n 
$$

hence for $R \to S$ &#233;tale

$$
  \pi_n S \simeq \pi_n R \otimes_{\pi_0 R} \pi_0 S
$$

This is a [[quasi-coherent sheaf]] on $\pi_0 R$ of the form $\tilde N$ (quasicoherent sheaf associated with a module), for $N$ an $\pi_0 R$-module. By vanishing theorem of higher cohomology for quasicoherent sheaves

$$
  H_{et}^1(\pi_0 R, \tilde N) = 0; for p \gt 0
$$

For every [[(infinity,1)-sheaf]] $G$ of [[infinity-groups]], there is a [[spectral sequence]]

$$
  H_{et}^p(\pi_0 R; \tilde \pi_q G) \Rightarrow \pi_{q-p} G(R)
$$

(the second argument on the left denotes the $qth$ Postnikov stage). From this one gets the following.

* $\tilde \pi_0 Br \simeq *$

* $\tilde \pi_1 Br \simeq \mathbb{Z}$;

* $\tilde \pi_2 Br \simeq \tilde \pi_1 Pic \simeq \pi_0 GL_1 \simeq \mathbb{G}_m$

* $\tilde \pi_n Br$ is quasicoherent for $n \gt 2$.

there is an [[exact sequence]]

$$
  0 \to 
  H_{et}^2(\pi_0 R, \mathbb{G}_m)
  \to \pi_0 Br(R)
  \to H_{et}^1(\pi_0 R, \mathbb{Z})
  \to 0
$$

(notice the inclusion $Br(\pi_0 R) \hookrightarrow H_{et}^2(\pi_0 R, \mathbb{G}_m)$)

this is [[split exact sequence|split exact]] and so computes $\pi_0 Br(R)$ for connective $R$.

Now some more on the case that $R$ is not connective. 

Suppose there exists $R \stackrel{\phi}{\to} S$ which is a faithful 
[[Galois extension]] for $G$ a [[finite group]].

**Examples** 

1. (real into complex [[K-theory spectrum]]) $KO \to KU$ (this is $\mathbb{Z}_2$) 

1. [[tmf]] $\to tmf(3)$

Give $R \to S$, have a [[fiber sequence]]

$$
  Gl_1(R/S) \stackrel{fib}{\to} GL_1(R) \to GL_1(S)
  \to 
  Pic(R/S) \stackrel{fib}{\to} Pic(R) \to Pic(S)
  \to
  Br(R/S) \stackrel{fib}{\to} Br(R) \to Br(S) \to \cdots
$$

**Theorem** (descent theorems) (Tyler Lawson, David Gepner) Given $G$-Galois extension $R \stackrel{\simeq}{\to} S^{hG}$ ([[homotopy fixed points]])

1. $Mod_R \stackrel{\simeq}{\to} Mod_S^{hG}$

1. $Alg_R \stackrel{\simeq}{\to} Alg_S^{hG}$

it follows that there is a homotopy fixed points spectral sequence

$$
  H^p(G, \pi_\bullet \Sigma^n GL_1(S))
  \Rightarrow
  \pi_{-n} GL_1(S)
$$


**Conjecture** The spectral sequence gives an Azumaya $KO$-algebra $Q$ which is a nontrivial element in $Br(KO)$ but becomes trivial in $Br(KU)$.

### Azumaya categories

Borceux and Vitale have noted that the [[monoidal bicategory]] of  $R$-algebras, bimodules and bimodule morphisms can be generalized in the context of [[enriched category]] theory, leading to a concept of "Azumaya category".  An Azumaya algebra over the commutative ring $R$ is then a one-object Azumaya category enriched over $R Mod$.

More precisely, they consider an arbitrary [[Benabou cosmos]] $V$, meaning a [[complete]] and [[cocomplete]] [[symmetric monoidal]] [[closed category|closed]] category.   This gives a monoidal bicategory $V Mod$ with 

* $V$-enriched categories as objects,
* $V$-enriched [[profunctors]] as morphisms, and
* $V$-natural transformations between $V$-enriched profunctors as 2-morphisms.

The [[core]] of this monoidal bicategory is a 3-group, and they call the objects of the core **Azumaya categories**.

* [[Francis Borceux]] and [[Enrico Vitale]], Azumaya categories, *Applied Categorical Structures* **10** (2002), 449-467. ([pdf](https://link.springer.com/content/pdf/10.1023/A:1020570213428.pdf))

## Related concepts

* [[group of units]], [[Picard group]], [[Brauer group]], [[Picard 3-group]]

## References 


* [G. Corti&#241;as](http://mate.dm.uba.ar/~gcorti), [[Charles Weibel]], _Homology of Azumaya algebras_, Proc. AMS __121__, 1, pp. 1994 ([jstor](http://www.jstor.org/stable/2160364))

* [[John Duskin]], _The Azumaya complex of a commutative ring_, in Categorical Algebra and its Appl., Lec. Notes in Math. 1348 (1988) [doi:10.1007/BFb0081352](http://dx.doi.org/10.1007/BFb0081352)

* {#GrothendieckBrauer} [[Alexander Grothendieck]], _Le groupe de Brauer I, II, III_, in Dix exposes sur la cohomologie des schemas (I: Alg&#232;bres d'Azumaya et interpr&#233;tations diverses) North-Holland Pub. Co., Amsterdam (1969)

* [[Max Karoubi]], [[Peter Donovan]], _Graded Brauer groups and $K$-theory with local coefficients_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1970__38_/PMIHES_1970__38__5_0/PMIHES_1970__38__5_0.pdf))

* M-A. Knus, M. Ojanguren, _Th&#233;orie de la descente et alg&#232;bres d'Azumaya_, Lec. Notes in Math. __389__, Springer 1974, [doi:10.1007/BFb0057799](http://dx.doi.org/doi:10.1007/BFb0057799), MR0417149

* J. Milne, _&#201;tale cohomology_, Princeton Univ. Press

* [[Ross Street]], _Descent_, Oberwolfach preprint (sec. 6, Brower groups) [pdf](http://www.math.mq.edu.au/~street/Descent.pdf); _Some combinatorial aspects of descent theory_, Applied categorical structures __12__ (2004) 537-576, [math.CT/0303175](http://arxiv.org/abs/math/0303175) (sec. 12, Brower groups)

* [[Enrico Vitale]], _A Picard-Brauer exact sequence of categorical groups_, [pdf](http://www.math.ucl.ac.be/membres/vitale/cat-gruppi2.pdf)

* Ana-L. Agore, [[Stefan Caenepeel]], Gigel Militaru,  _Braidings on the category of bimodules, Azumaya algebras and epimorphisms of rings_, Appl. Categor. Struct. 22, 29--42 (2014) [doi](https://doi.org/10.1007/s10485-012-9294-3)

The observation that passing to [[derived algebraic geometry]] makes also the non-torsion elements in the "[[bigger Brauer group]]" $H^2_{et}(-,\mathbb{G}_m)$ be represented by (derived) Azumaya algebras is due to

* {#Toen10} [[Bertrand Toën]], _Derived Azumaya algebras and generators for twisted derived categories_ ([arXiv:1002.2599](http://arxiv.org/abs/1002.2599))

The comparison of the Artin's theorem on characterization of Azumaya algebras
and Tomiyama-Takesaki's theorem on $n$-[[homogeneous C*-algebra]]s is in chapter 9 of

* Edward Formanek, _Noncommutative invariant theory_, in: Group actions on rings (Brunswick, Maine, 1984), 87&#8211;119, Contemp. Math. 43, Amer. Math. Soc. 1985 [doi](http://dx.doi.org/10.1090/conm/043)


See also

* Wikipedia, [Azumaya algebra](http://en.wikipedia.org/wiki/Azumaya_algebra)

* Urs Schreiber, [Picard and Brauer 2-groups](http://golem.ph.utexas.edu/string/archives/000786.html), String Theory Coffee Table, 2006.

* John Baez, [The Brauer 3-group](https://golem.ph.utexas.edu/category/2020/05/the_brauer_3group.html), $n$-Category Caf&eacute;, 2020.


[[!redirects Azumaya algebras]]
[[!redirects central separable algebra]]