
#Contents#

* automatic TOC goes here
{: toc}

#Definition#

## as locally presentable $\mathcal{O}_X$-modules ##

Given a [[ringed space]] $(X,O_X)$ a __quasicoherent sheaf of $O_X$-modules__ is a sheaf $\mathcal{M}$ of $O_X$-modules such that there is a cover $\{U_\alpha\}_{\alpha\in A}$ of $X$ by open sets such that for every $\alpha$ there exist $I_\alpha$ and $J_\alpha$ and an exact sequence of sheaves of $O_X$-modules of the form
$$
O_X^{I_\alpha}|_{U_\alpha}\to
O_X^{J_\alpha}|_{U_\alpha}\to
\mathcal{M}|_{U_\alpha}\to 0,
$$
which should be viewed as a local presentation of $\mathcal{M}$. If $I_\alpha, J_\alpha$ can be chosen finite one talks about __coherent sheaves__ however the latter are ill-behaved for a general ringed space, and even general scheme; they behave well on Noetherian schemes. 

Replacing covers by open sets, by covers of a terminal object in a site, the definition extends to [[ringed site]]s with a terminal object; the restrictions of $O_X$-modules should be replaced by pullbacks.
There are generalizations for [[algebraic stack]]s, ind-schemes, diagrams of schemes (for example [configuration schemes](http://arxiv.org/abs/math/0012061) of V. Lunts, obtained by gluing along closed embeddings of schemes; simplicial schemes) and so on. 

## as sheaves on $Aff/X$ ##

There is an equivalent reformulation of the above in terms of [[sheaf|sheaves]] on the [[site]] $Aff/X$ of [[affine scheme]]s over $X$.

This is the [[over category]] whose objects are morphism (of [[scheme]]s) of the form $Spec A \to X$ and whose morphisms are commuting triangles

$$
  \array{
    Spec A &&\stackrel{f}{\to}&& Spec B
    \\
    & {}_a\searrow && \swarrow_b
    \\
    && X
  }
  \,.
$$

Then: a quasicoherent sheaf on $(X, \mathcal{O}_X)$ is a [[sheaf]] of $\mathcal{O}_X$-modules on $Aff/X$  such that for each morphism $f$ as above the morphism

$$
  f^* \mathcal{M}(a) \simeq
  B \otimes_A \mathcal{M}(a)
  \to 
  \mathcal{M}(b)
$$

is an [[isomorphism]].

**Remark** This definition has a straightforward generalization to various [[higher category theory|higher categorical]] setups, such as [[derived scheme]]s and other [[generalized scheme]]s. See [[geometric infinity-function theory]] for a detailed discussion of properties of "derived quasicoherent sheaves".


# Properties #

## quasicoherent sheaves over affine schemes ##

Given an affine scheme $X=\mathrm{Spec}\,R$ (where $R$ is a commutative unital ring), the affine Serre theorem establishes the equivalence of the category $Qcoh(\mathrm{Spec}\,R)$ of quasicoherent sheaves (in Zariski topology) and the category of $R$-modules. Similarly on a projective scheme of the type $Proj(A)$ where
$A$ is a nonnegatively graded ring, the (projective) Serre theorem establishes the equivalence of $Qcoh(\mathrm{Proj}\,(A))$ and 
the localization of the category of graded $A$-modules by the subcategory of modules of finite length (and similarly, of coherent sheaves and graded $A$-modules of finite type modulo finite-length). These theorems are among basic motivating theorems for [[noncommutative algebraic geometry]]. An interesting in-depth comparison of the notions of quasi-coherent sheaves in commutative and noncommutative context are in

* D. Orlov, _Quasi-coherent sheaves in commutative and non-commutative geometry_, Izv. RAN. Ser. Mat., 2003,  Volume 67,  Issue 3, Pages 119&#8211;138 (see also preprint version [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=57), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=56))

## the category of quasicoherent sheaves ##

In the case of general (commutative) schemes, every presheaf of $O_X$-modules which is quasicoherent in the sense of having local presentation as above, is in fact a sheaf. It is known that the category of quasicoherent sheaves of $O_X$-modules over any [[quasicompact]] quasiseparated scheme is a [[Grothendieck category]] and in particular has enough [[injective object]]s.

The [[fibered category]] of $O_X$-modules can be replaced by a more general fibered category $\pi: \mathcal{F}\to\mathcal{B}$. Then the __category of quasicoherent modules in__ this __fibered category__ is the category opposite to the category of cartesian sections of $\pi$. This viewpoint is used by Rosenberg-Kontsevich in their preprint on noncommutative stacks ([dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2305), [ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2333)).

Given a category $\mathrm{Aff}$ of affine schemes (opposite to the category of rings) equipped with some [[subcanonical coverage|subcanonical pretopology]] one considers the [[stack]] of $O$-modules over $\mathrm{Aff}$: the fiber over a ring $R$, it assigns the category $Qcoh(\mathrm{Spec}\,R)$. Now given any stack on a subcanonical site, one defines the fiber over a sheaf on it so that the fiber over a representable sheaf is equivalent to the fiber over its representing object. There is a canonical way to do this (will write later about it -- Zoran); this is in particular a source of a definition $Qcoh$ on an ind-scheme. On ind-schemes Beilinson and Drinfel'd in

* A. Beilinson, V. Drinfel'd, _Quantization of Hitchin's integrable system and Hecke eigensheaves on Hitchin system_, preliminary version ([pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

consider two variants: a less important variant of quasicoherent $O_X^p$-modules (existing in bigger generality) and more delicate variant of quasicoherent $O^!_X$-modules defined for "reasonable ind-schemes"; one of the differences is which functors play the role of pullbacks.  In particular, these notions apply for a rather general variant of the category of formal schemes.

[[!redirects quasicoherent sheaves]]
[[!redirects quasicoherent module]]
[[!redirects quasicoherent modules]]