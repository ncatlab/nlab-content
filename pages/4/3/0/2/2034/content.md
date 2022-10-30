
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

## Definition

### Traditional

Given a [[commutative unital ring]] $R$, an __Azumaya $R$-algebra__ is a (noncommutative in general) $R$-[[associative algebra|algebra]] $A$ which is finitely generated faithful [[projective object|projective]] as an $R$-[[module]] and the canonical morphism $A\otimes_R A^{op}\to End_R(A)$ is an [[isomorphism]]. This definition extends the notion of a [[central simple algebra]] over a [[field]]. 

More generally, [[Grothendieck]] defines an __Azumaya algebra__ over a [[scheme]] $X$ as a [[sheaf]] $\mathcal{A}$ of $\mathcal{O}_X$-algebras such that for each point $x\in X$, the corresponding [[stalk]] $\mathcal{A}_x$ is an Azumaya $\mathcal{O}_{X,x}$-algebra. 

The [[Brauer group]] $Br(X)$ classifies Azumaya algebras over $X$ up to a suitably defined equivalence relation: $\mathcal{A}\sim\mathcal{B}$ if $\mathcal{A}\otimes_{\mathcal{O}_X} \mathbf{End}(\mathcal{E}) \cong \mathcal{A}\otimes_{\mathcal{O}_X}\mathbf{End}(\mathcal{F})$ for some locally free sheaves of $\mathcal{O}_X$-modules $\mathcal{E}$ and $\mathcal{F}$ of finite rank.  The group operation of $Br(X)$ is induced by the tensor product. The Brauer group can be reexpressed in terms of second [[nonabelian cohomology]]; indeed a sheaf of Azumaya algebras over $X$ determines an $\mathcal{O}_X^*$-[[gerbe]] (or $U(1)$-gerbe in the [[manifold]] context).  

Brauer groups and Azumaya algebras are closely related to [[Morita theory]] and they make sense in the context of algebras and bimodules in the context of [[braided monoidal category|braided monoidal categories]]. [[Karoubi K-theory]] involves an element in a Brauer group and in the original Karoubi--Donovan paper is related to a twisting with a "local system" which involves Azumaya algebras.


### In terms of (derived) &#233;tale cohomology
 {#InTermsOfEtaleCohomology}

For $R$ a [[ring]] and $H^n_{et}(-,-)$ the [[etale cohomology]], $\mathbb{G}_m$ the [[multiplicative group]] of the [[affine line]]; then

* $H^0_{et}(R, \mathbb{G}_m) = R^\times$ ([[group of units]])

* $H^1_{et}(R, \mathbb{G}_m) = Pic(R)$ ([[Picard group]]: iso classes of invertible $R$-modules)

* $H^2_{et}(R, \mathbb{G}_m)_{tor} = Br(R)$ ([[Brauer group]] Morita classes of Azumaya $R$-algebras)

More generally, this works for $R$ a (connective) [[E-infinity ring]] 
(the following is due to [[David Gepner]]). 

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

One shows (Gepner) that this is exactly the Azumaya $R$-algebras modulo Morita equivalence.

**Theorem** (B. Antreau, D. Gepner) 

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

hence for $R \to S$ e&#233;tale

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


## Related concepts

* [[group of units]], [[Picard group]], [[Brauer group]]

## References 


* [G. Corti&#241;as](http://mate.dm.uba.ar/~gcorti), [[Charles Weibel]], _Homology of Azumaya algebras_, Proc. AMS __121__, 1, pp. 1994 ([jstor](http://www.jstor.org/stable/2160364))

* [[John Duskin]], _The Azumaya complex of a commutative ring_, in Categorical Algebra and its Appl., Lec. Notes in Math. 1348 (1988) [doi:10.1007/BFb0081352](http://dx.doi.org/10.1007/BFb0081352)

* [[Alexander Grothendieck]], _Le groupe de Brauer I, II, III_, in Dix exposes sur la cohomologie des schemas (I: Alg&#232;bres d'Azumaya et interpr&#233;tations diverses) North-Holland Pub. Co., Amsterdam (1969)

* [[Max Karoubi]], [[Peter Donovan]], _Graded Brauer groups and $K$-theory with local coefficients_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1970__38_/PMIHES_1970__38__5_0/PMIHES_1970__38__5_0.pdf))

* M-A. Knus, M. Ojanguren, _Th&#233;orie de la descente et alg&#232;bres d'Azumaya_, Lec. Notes in Math. __389__, Springer 1974, [doi:10.1007/BFb0057799](http://dx.doi.org/doi:10.1007/BFb0057799), MR0417149

* J. Milne, _&#201;tale cohomology_, Princeton Univ. Press

* [[Ross Street]], _Descent_, Oberwolfach preprint (sec. 6, Brower groups) [pdf](http://www.math.mq.edu.au/~street/Descent.pdf); _Some combinatorial aspects of descent theory_, Applied categorical structures __12__ (2004) 537-576, [math.CT/0303175](http://arxiv.org/abs/math/0303175) (sec. 12, Brower groups)

* [[Enrico Vitale]], _A Picard-Brauer exact sequence of categorical groups_, [pdf](http://www.math.ucl.ac.be/membres/vitale/cat-gruppi2.pdf)

See also

* [wikipedia page](http://en.wikipedia.org/wiki/Azumaya_algebra)

* Category Cafe 2006: [Picard and Brauer 2-groups](http://golem.ph.utexas.edu/string/archives/000786.html)


[[!redirects Azumaya algebras]]