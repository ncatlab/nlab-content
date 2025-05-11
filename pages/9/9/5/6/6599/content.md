
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--



# Grothendieck duality
* table of contents
{: toc}

## Idea

Given a [[homomorphism]] $f$ of [[schemes]], one says that it satisfies
_Grothendieck duality_  if the ([[derived functor|derived]]) [[direct image]] functor $f_\ast$ on [[quasicoherent sheaves]] has a (derived) [[right adjoint]] $f^!$. This is [[Verdier duality]] in a "[[Grothendieck context]]" of [[six operations]].

Grothendieck duality is intimately connected to **dualizing complexes**. This was the original approach of Grothendieck in the book _Residues and Duality_.


## Statement


Suppose $f\colon X \to Y$ is a [[quasi-compact map|quasi-compact]] and [[quasi-separated map|quasi-separated]] [[morphism]] of [[schemes]]; then the [[triangulated functor]] $\mathbf{R}f_*\colon D_{qc}(X)\to D(Y)$ has a bounded below [[right adjoint]]. In other words, $\mathbf{R}Hom_X(\mathcal{F}, f^\times \mathcal{G})\stackrel{\sim}{\to} \mathbf{R}Hom_Y(\mathbf{R}f_*\mathcal{F}, \mathcal{G})$ is a [[natural isomorphism]].



## Dualizing Complexes

Let $X$ be a noetherian scheme. A dualizing complex on $X$ is a complex 
$\mathcal{R} \in \mathsf{D}(\mathsf{Mod} X)$ that has these three properties:

* $\mathcal{R} \in \mathsf{D}^{\mathrm{b}}_{\mathrm{c}}(\mathsf{Mod} X)$ (i.e. $\mathcal{R}$ has bounded coherent cohomology sheaves).

* $\mathcal{R}$ has finite injective dimension. 

* The canonical morphism 
$\mathcal{O}_X \to \mathrm{R} \mathcal{Hom}_{X}(\mathcal{R}, \mathcal{R})$ 
in $\mathsf{D}(\mathsf{Mod} X)$ is an isomorphism. 

The following two structures are basically equivalent to each other, for a given category of noetherian schemes $\mathsf{S}$:

* A psudofunctor $f \mapsto f^!$, called the **twisted inverse image**, 
that assigns a functor 
\[ f^! : \mathsf{D}^{+}_{\mathrm{c}}(\mathsf{Mod} Y)
\to \mathsf{D}^{+}_{\mathrm{c}}(\mathsf{Mod} X) \]
to each map of schemes $f : X \to Y$ in $\mathsf{S}$, 
and has several known properties.

* A dualizing complex $\mathcal{R}_X$ for every scheme $X$ in the category 
$\mathsf{S}$, with several known functorial properties. 

The relation between these two structures is demonstrated in the following Example. 


**Example**. 
Suppose $K$ is a regular finite dimensional noetherian ring, and let $\mathsf{S}$ be the category of finite type $K$-schemes. 
Given a twisted inverse image psudofunctor $f \mapsto f^!$, we define dualizing complexes as follows: on any $X \in \mathsf{S}$ with structural morphism 
$\pi_X : X \to \operatorname{Spec} K$, we let
$\mathcal{R}_X := \pi_X^!(K)$. 

Conversely, suppose we are given a dualizing complex $\mathcal{R}_X$ on each 
$X \in \mathsf{S}$. This gives rise to a duality (contrvariant equivalence)
$D_X$ of $\mathsf{D}^{}_{\mathrm{c}}(\mathsf{Mod} X)$,
exchanging $\mathsf{D}^{+}_{\mathrm{c}}(\mathsf{Mod} X)$ with 
$\mathsf{D}^{-}_{\mathrm{c}}(\mathsf{Mod} X)$, with formula
\[ D_X(\mathcal{M}) := \mathrm{R} \mathcal{Hom}_{X}(\mathcal{M}, \mathcal{R}_X) . \]
We then define
\[ f^!(\mathcal{M}) := D_Y( \mathrm{L} f^* ( D_X(\mathcal{M}) )) . \]


### Rigid Dualizing Complexes 

The notion of _rigid dualizing complex_ was introduced by Van den Bergh in 1997, for a _noncommutative ring_ $A$ over a base field $K$. 

Yekutieli and Zhang have shown how to define a rigid dualizing complex $R_{A/K}$, when $K$ is a regular finite dimensional noetherian ring, and $A$ is an essentially finite type $K$-ring (both commutative). A refined variant of the rigid dualizing complex, namely the _rigid residue complex_ $\mathcal{K}_{A/K}$, was shown to exist, and to be unique (up to a unique isomorphism of complexes).  

These rigid residue complexes have all the good functorial properties alluded to above, and even more. Specifically, they are covariant for essentially etale ring homomorphisms $A \to A'$ (via the rigid localization homomorphism), and contravariant
(as graded modules) for all ring homomorphisms $A \to B$ (via the ind-rigid trace homomorphism). 

The rigid localization homomorphism permits the gluing of the rigid residue complexes 
$\mathcal{K}_{A/K}$ on affine open sets $U = \operatorname{Spec} A$ of a scheme $X$ into a rigid residue complex $\mathcal{K}_{X/K}$ on $X$. In this way one obtains a collection of dualizing complexes $\mathcal{K}_{X/K}$ on all essentially finite type $K$-schemes $X$, consisting of quasi-coherent injective sheaves. For any map of scheme $f : X \to Y$ there is the ind-rigid trace homomoprhism 
\[ \mathrm{Tr}_f : f_*(\mathcal{K}_{Y/K}) \to \mathcal{K}_{X/K} , \]
which is a homomorphism of graded quasi-coherent sheaves. 
The _Residue Theorem_ says that when $f$ is proper, 
$\mathrm{Tr}_f$ is a homomorphism of complexes. 
The _Duality Theorem_ says that when $f$ is proper, $\mathrm{Tr}_f$ induces global duality. As explained above, there is a corresponding functor $f^!$; 
and the Duality Theorem says that $\mathrm{R} f_*$ and $f^!$ are adjoint functors. 


Moreover, the rigidity method works also for finite type **Deligne-Mumford stacks** over $K$. The key observation is that the rigid residue complexes are complexes of quasi-coherent sheaves in the etale site over $K$. Details of this extension of the theory are still under preparation. 


## Noncommutative Grothendieck Duality 

(To be added later)



## Related concepts

* [[six operations]]

* [[Poincare duality]], [[Verdier duality]]

* [[Fourier-Mukai transform]]

## References

* [[Robin Hartshorne]], _Residues and duality_ (Lecture notes of a seminar on the work of A. Grothendieck, given at Harvard 1963/64. With an appendix by P. Deligne.) Springer LNM 20, 1966 [MR222093](http://www.ams.org/mathscinet-getitem?mr=222093)
* Domingo Toledo, Yue Lin L. Tong,  _Duality and intersection theory in complex manifolds. I._, Math. Ann. __237__ (1978), no. 1, 41&#8211;77, [MR80d:32008](http://www.ams.org/mathscinet-getitem?mr=506654), [doi](http://dx.doi.org/10.1007/BF01351557)
* Mitya Boyarchenko, [[Vladimir Drinfeld]], _A duality formalism in the spirit of Grothendieck and Verdier_, [arxiv/1108.6020](http://arxiv.org/abs/1108.6020)
* Z. Mebkhout, _Le formalisme des six op&#233;rations de Grothendieck pour les $\mathcal{D}_X$-modules coh&#233;rents_, Travaux en Cours __35__. Hermann, Paris, 1989. x+254 pp. [MR90m:32026](http://www.ams.org/mathscinet-getitem?mr=1008245)
* [[Amnon Neeman]], _Derived categories and Grothendieck duality_, in:  Triangulated categories, 290&#8211;350, London Math. Soc. Lecture Note Ser. __375__, Cambridge Univ. Press 2010
* Amnon Neeman, _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, J. Amer. Math. Soc. __9__ (1996), no. 1, 205&#8211;236, [MR96c:18006](http://www.ams.org/mathscinet-getitem?mr=1308405), [doi](http://dx.doi.org/10.1090/S0894-0347-96-00174-9)

* [[Brian Conrad]]: *Grothendieck duality and base change*, Lec. Notes Math. __1750__, Springer (2000) &lbrack;[doi:10.1007/b75857](https://doi.org/10.1007/b75857), [errata](https://math.stanford.edu/~conrad/papers/dualitycorrections.pdf)&rbrack;

* [[Joseph Lipman]], _Notes on derived functors and Grothendieck duality_, in: Foundations of Grothendieck duality for diagrams of schemes, 1&#8211;259, Lecture Notes in Math. __1960__, Springer 2009, [doi](http://dx.doi.org/10.1007/978-3-540-85420-3), [draft pdf](http://www.math.purdue.edu/~lipman/Duality.pdf)

* J. Lipman, _Grothendieck operations and coherence in categories_, conference slides, 2009, [pdf](http://www.math.purdue.edu/~lipman/Madrid.pdf)
* Alonso Tarr&#237;o, Leovigildo; Jerem&#237;as L&#243;pez, Ana; Joseph Lipman, _Studies in duality on Noetherian formal schemes and non-Noetherian ordinary schemes_, Contemporary Mathematics __244__ Amer. Math. Soc. 1999. x+126L. [MR2000h:14017](http://www.ams.org/mathscinet-getitem?mr=1716706); _Duality and flat base change on formal schemes_, Contemporary Math. __244__ (1999), pp. 3&#8211;90.
* J. Ayoub, _Les six op&#233;rations de Grothendieck et le formalisme des cycles &#233;vanescents dans le monde motivique. I._, Ast&#233;risque No. 314 (2007), x+466 pp. (2008) [MR2009h:14032](http://www.ams.org/mathscinet-getitem?mr=2423375); _II._ Ast&#233;risque No. 315 (2007), vi+364 pp. (2008) [MR2009m:14007](http://www.ams.org/mathscinet-getitem?mr=2438151); 
also a file at K-theory archive [THESE.pdf](http://www.math.uiuc.edu/K-theory/0761/THESE.pdf)

* [[Amnon Yekutieli]], James Zhang,
Rings with Auslander Dualizing Complexes, J. Algebra 213 (1999), 1-51;
_Rigid dualizing complexes over commutative rings_, Algebr. Represent. Theory __12__ (2009), no. 1, 19&#8211;52, [doi](http://dx.doi.org/10.1007/s10468-008-9102-9);
Dualizing Complexes and Perverse Sheaves on Noncommutative Ringed Schemes,
Selecta Math. 12 (2006), 137-177;
Dualizing Complexes and Perverse Modules over Differential Algebras,
Compositio Mathematica 141 (2005), 620-654.

* [[Amnon Yekutieli]], 
An Explicit Construction of the Grothendieck Residue Complex, Ast&#233;risque **208** (1992);
The residue complex of a noncommutative graded algebra, J. Algebra __186__ (1996), no. 2, 522&#8211;543; _Smooth formal embeddings and the residue complex_, Canad. J. Math. __50__ (1998), no. 4, 863&#8211;896, [MR99i:14004](http://www.ams.org/mathscinet-getitem?mr=1638635); _Rigid dualizing complexes via differential graded algebras (survey)_, in: Triangulated categories, 452&#8211;463, London Math. Soc. Lecture Note Ser. __375__, Cambridge Univ. Press 2010, [MR2011h:18015](http://www.ams.org/mathscinet-getitem?mr=2681716);
 Residues and Differential Operators on Schemes,
Duke Math. J. 95 (1998), 305-341;
Duality and Tilting for Commutative DG Rings, [arXiv:1312.6411](http://arxiv.org/abs/1312.6411);
Residues and Duality for Schemes and Stacks 
([lecture notes](http://www.math.bgu.ac.il/~amyekut/lectures/resid-stacks/handout.pdf)).

* [[Roy Joshua]], _Grothendieck-Verdier duality in enriched symmetric monoidal $t$-categories_ ([[JoshuaDuality.pdf:file]])

* {#Belmans} [[Pieter Belmans]], section 2.2 of _Grothendieck duality: lecture 3_, 2014 ([[BelmansDuality.pdf:file]])

* [[Amnon Neeman]], _An improvement on the base-change theorem and the functor $f^!$_, [arXiv](http://arxiv.org/abs/1406.7599).





