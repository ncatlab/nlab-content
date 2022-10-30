
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

For $R$ a [[ring]], the _Brauer group_ $Br(R)$ is the [[group]] of [[Morita equivalence]] classes of [[Azumaya algebras]] over $R$.

## Properties

### Relation to &#233;tale cohomology
 {#RelationToEtaleCohomology}

The Brauer group of a [[ring]] $R$ is a [[torsion]] subgroup of the second [[etale cohomology]] group of $Spec R$ with values in the [[multiplicative group]] $\mathbb{G}_m$

$$
  Br(X) \hookrightarrow H^2_{et}(X, \mathbb{G}_m)
  \,.
$$

This was first stated in ([Grothendieck 68](#Grothendieck)), a discussion is in chapter IV of ([Milne](#Milne)). A detailed discussion in the context of [[nonabelian cohomology]] is in ([Giraud](#Giraud)).

A theorem stating conditions under which the Brauer group is precisely the [[torsion]] subgroup of $H^2_{et}(X, \mathbb{G}_m)$ is due to ([Gabber](#Gabber)), see also the review in ([de Jong](#deJong)). For more details and more literature on this see ([Bertuccioni](#Bertuccioni)).


This fits into the following pattern

* $H^0_{et}(R, \mathbb{G}_m) = R^\times$ ([[group of units]])

* $H^1_{et}(R, \mathbb{G}_m) = Pic(R)$ ([[Picard group]]: iso classes of invertible $R$-modules)

* $H^2_{et}(R, \mathbb{G}_m)_{tor} = Br(R)$ ([[Brauer group]]: 
[[Morita equivalence]] classes of [[Azumaya algebras]] over $R$)




### Relation to derived &#233;tale cohomology

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

* [[group of units]]/[[multiplicative group]], [[Picard group]]

* [[Azumaya algebra]]


## References

An introduction is in

* Pete Clark, _On the Brauer group_  (2003) ([pdf](http://math.uga.edu/~pete/trivial2003.pdf))

* [[Alexandre Grothendieck]], _Le groupe de Brauer_, Dix expos&#233;s sur la cohomologie des sch&#233;mas_, Masson and North-Holland, Paris
and Amsterdam, (1968), pp. 46&#8211;66.
 {#Grothendieck}

* [[Ross Street]], _Descent_, Oberwolfach preprint (sec. 6, Brower groups) [pdf](http://www.math.mq.edu.au/~street/Descent.pdf); _Some combinatorial aspects of descent theory_, Applied categorical structures __12__ (2004) 537-576, [math.CT/0303175](http://arxiv.org/abs/math/0303175) (sec. 12, Brower groups)

The relation to [[cohomology]]/[[etale cohomology]] is discussed in

* [[James Milne]], _&#201;tale cohomology_, Princeton Mathematical Series, vol. 33, Princeton University Press, Princeton, New
Jersey (1980)
 {#Milne}

* [[Jean Giraud]], _Cohomologie non abelienne_, Die Grundlehren der mathematischen Wissenschaften, vol. 179, Springer-
Verlag, Berlin, 1971.
 {#Giraud}

* O. Gabber, _Some theorems on Azumaya algebras_, Ph. D. Thesis, Harvard University, 1978, Groupe de Brauer, Lecture
Notes in Mathematics, vol. 844, Springer-Verlag, Berlin, 1981, pp. 129&#8211;209.

* [[Aise Johan de Jong]], _A result of Gabber_ ([pdf](http://www.math.columbia.edu/~dejong/papers/2-gabber.pdf))
 {#deJong}
  
* Inta Bertuccioni, _Brauer groups and cohomology_, Archiv der Mathematik, vol. 84 Number 5 (2005)
 {#Bertuccioni}


[[!redirects Brauer groups]]
