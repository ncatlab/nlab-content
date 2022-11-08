

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A **2-plethory** ([Baez-Moeller-Trimble](#BMT21)) is a categorification of a rig-[[plethory]]. Just as a rig-plethory is defined as a monoid in $(\mathsf{Birig}, \odot)$, a 2-plethory is a [[pseudomonoid]] in $(2\mathsf{Birig}, \odot)$.

The property that polynomials in $\mathbb{N}[x]$ can be composed is a consequence of the fact that  $\mathbb{N}[x]$ is the free rig in one generator, and hence represents the identity functor $\mathsf{Rig}\to \mathsf{Rig}$. Similarly, the category of [[Schur functor]]s $\mathsf{Schur}$ can be seen as a 2-rig (in the sense below) representing the identity 2-functor $2\mathsf{Rig}\to 2\mathsf{Rig}$. As a consequence, $\mathsf{Schur}$ has the structure of a 2-plethory. Taking isomorphism classes, one recovers the rig-[[plethory]] structure on the positive [[symmetric function]]s, justifying the term "categorified [[plethysm]]".

## Definitions
Let $k$ be a field of characteristic zero, and let $\mathsf{Rig}$ be the category of [[rig]]s and rig morphisms.
Let $U:\mathsf{Rig} \to \mathsf{Set}$ be  the [[forgetful functor]].

A birig is equivalently defined as:

* A rig object in $\mathsf{Rig}^\text{op}$.

* A rig $B$ and a lift of the representable functor $\mathsf{Rig}(B,-):\mathsf{Rig}\to \mathsf{Set}$ to a functor $\Phi_B:\mathsf{Rig}\to \mathsf{Rig}$ such that $U \circ \Phi_B=\mathsf{Rig}(B,-)$. Observe that any two representable 2-functors $\Phi_B$, $\Phi_B'$ can be composed. Denote the resulting object by $B\odot B'$, so that $\Phi_B \circ \Phi_B'=\Phi_{B' \circ B}$.

* A functor $\Phi:\mathsf{Rig}\to \mathsf{Rig}$ that is a right adjoint.

Denote by $(\mathsf{Birig}, \odot)$ the monoidal category of birigs, viewed as a [[full subcategory]] of $\mathsf Rig$.

A rig-[[plethory]] is equivalently defined as:

* A monoid in $(\mathsf{Birig}, \odot)$.

* A birig $B$ such that $\Phi_B$ is a comonad.

The categorified versions of the definitions above are as follows.

The category $2\mathsf{Rig}$ has:

* Objects: [[symmetric monoidal]] $k$-linear categories for which the tensor product is bilinear on hom-spaces and which are [[Cauchy complete]].

* 1-morphisms: [[symmetric monoidal]] [[linear functor]]s.

* 2-morphisms: [[symmetric monoidal]] linear natural transformations.

Let $\mathsf{U}:\mathsf{2Rig} \to \mathsf{Cat}$ be  the forgetful [[2-functor]].

A **2-birig** is a 2-rig $\mathsf B$ and a lift of the 2-functor $\mathsf{2Rig}(B,-):\mathsf{2Rig}\to \mathsf{Cat}$ to a 2-functor $\Phi_\mathsf{B}:\mathsf{2Rig}\to \mathsf{2Rig}$ such that $\mathsf U \circ \Phi_\mathsf{B}=\mathsf{2Rig}(\mathsf{B},-)$. Again, any two representable 2-functors $\Phi_\mathsf{B}$, $\Phi_\mathsf{B'}$ can be composed. Denote the resulting object by $\mathsf{B}\odot \mathsf{B'}$, so that $\Phi_\mathsf{B} \circ \Phi_\mathsf{B'}=\Phi_{\mathsf{B'}\odot \mathsf{B}}$.

Denote by $(\mathsf{2Birig}, \odot)$ the [[monoidal 2-category]] of 2-birigs, viewed as a full [[sub-2-category]] of $\mathsf{2Rig}$.

A **2-plethory** can be equivalently defined as

* A [[pseudomonoid]] in $(2\mathsf{Birig}, \odot)$.

* A 2-comonad $\Phi:\mathsf{2Rig}  \to  \mathsf{2Rig}$ whose underlying 2-functor is a right 2-adjoint.


## Example: Schur functors
For any 2-plethory $\Phi$ with left 2-adjoint $\Psi$, the composition $\mathsf{U}\Phi$ is representable, with representing object $\Psi(\overline{k\mathsf{S}})$, where $\overline{k\mathsf{S}}$ is the [[Cauchy completion]] of the $k$-linearization of the [[permutation groupoid]] $\mathsf{S}$. In turn, the 2-rig $\overline{k\mathsf{S}}$ is equivalent to $\mathsf{Schur}$ made into a 2-rig with the pointwise tensor product.

In particular, the identity $1: \mathsf{2Rig} \to \mathsf{2Rig}$ is a 2-plethory with underlying 2-rig $\overline{k\mathsf{S}}$. The set isomorphism classes $J(\overline{k\mathsf{S}})$ has a commutative monoid structure coming from the decategorifications of $\oplus$ and $\otimes$. Then, $J(\overline{k\mathsf{S}})$ is isomorphic to the monoid of positive [[symmetric functions]] $\Lambda_+$. The 2-plethory structure induces the well-known rig-plethory structure on $\Lambda_+$. In turn, the [[Grothendieck group]] of $\mathsf{Schur}$ is $K(\overline{k\mathsf{S}})=\mathbb{Z}\otimes_\mathbb{N} J(\overline{k\mathsf{S}})$, and the rig-plethory  structure on $J(\overline{k\mathsf{S}})$ extends to a ring-plethory structure on $K(\overline{k\mathsf{S}})$.
 

## Related concepts

* [[biring]]

* [[plethory]]

* [[plethysm]]

* [[Schur functor]]

##References

* {#TW70} D. Tall and [[Gavin Wraith|G. Wraith]], Representable functors and operations on rings, _Proc. London Math. Soc._ **3** (1970), 619--643.

* {#BW05} [[James Borger]], [[Ben Wieland]],  Plethystic algebra, _Advances in Mathematics_ **194** (2005), 246--283.  ([web](http://wwwmaths.anu.edu.au/~borger/papers/03/paper03.html))

* {#BMT21} [[John Baez]], [[Joe Moeller]], [[Todd Trimble]], Schur functors and categorified plethysm, [arXiv:2106.00190](https://arxiv.org/abs/2106.00190)

