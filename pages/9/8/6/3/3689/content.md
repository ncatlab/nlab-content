
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

Given a [[monoid]] $R$ in a [[monoidal category]] $(\mathcal{C}, \otimes)$, $R$[[Mod]] is the [[category]] whose [[objects]] are $R$-[[modules]] in $\mathcal{C}$ and whose morphisms are module homomorphisms.

Specifically if $(\mathcal{C}, \otimes)$ is the category [[Ab]] of [[abelian groups]] and $\otimes$ the [[tensor product of abelian groups]], then $R$ is a [[ring]]. 

We write just $Mod$ for the category whose objects are pairs $(R,N)$ consisting of a monoid $R$ and an $R$-module, and whose morphisms may also map between different monoids.



## Definition of $Mod$

We assume that the ambient [[monoidal category]] is [[Ab]] with the [[tensor product of abelian groups]]. But the definition works more generally

+-- {: .num_defn #ModSpelledOut}
###### Definition

An [[object]] in $Mod$ is a pair $(R,N)$ consisting of a commutative [[ring]] $R$ and an $R$-[[module]] $N$. 

A [[morphism]]

$$
 (\phi,\kappa) :  (R,N) \to (R',N')
$$

is a pair consisting of a ring [[homomorphism]] $\phi : R \to R'$ and a morphism $\kappa : N \to \phi^* N'$ of $R$-modules, where $\phi^* N'$ is the [[tensor product]] $\phi^* N' := R \otimes_{\phi} N$.

=--

## Properties

### $Mod$ as a bifibration
 {#ModAsBifibration}

Projecting out the first items in the pairs appearing in def. \ref{ModSpelledOut} yields a canonical functor

$$
  p :Mod \to CRing
$$

$$
  (R,N) \mapsto R
  \,.
$$

that exhibits $Mod$ as a [[bifibration]] over $R$.

The fiber of this projection over a ring $R$ is $Mod_R$, the category of $R$-modules.

In particular the fiber over the initial commutative ring $R = \mathbb{Z}$ is

$$
  Mod_{\mathbb{Z}} = Ab
$$

the category [[Ab]] of abelian groups.


### Tangents and deformation theory
 {#TangentsAndDeformationTheory}

By an old observation of Quillen -- reviewed at [[module]] -- the bifibration $Mod \to CRing$ this is [[equivalence of categories|equivalent]] to the category of fiberwise abelian [[group object]] in the [[codomain fibration]] $[I,CRing] \to CRing$:

$$
  (Mod \to CRing) \simeq Ab([I,CRing]] \to CRing)
  \,.
$$

For a fixed ring $R$, the category $Mod_R$ of $R$-modules is canonically equivalent to $Ab(CRing/R)$, the category of abelian [[group object]]s in the [[overcategory]] $CRing/R$:

$$
  Mod_R \simeq Ab(CRing/R)
  \,.
$$

This says that $Mod \to Ring$ is the [[tangent category]] of $CRing$: the above equivalence regards an $R$-module $N$ equivalently as the square-0-extension ring $R \oplus N$ (with producte $(r_1,n_1) \cdots (r_2,n_2) = (r_1 r_2, r_1 n_2 + r_2 n_1)$), which may be thought of as the ring of functions on the infinitesimal neighbourhood of the 0-section of the [[vector bundle]] (or rather [[quasicoherent sheaf]]) over $Spec R$ that is given by $N$.

There is thus another natural projection from $Mod$ to rings, namely the functor that remembers these square-0-extensions

$$
  f : Mod \to CRing
$$

$$
  (R,N) \mapsto R \oplus N
  \,.
$$

This functor has a [[left adjoint]] $\Omega : CRing \to Mod$ which is also a [[section]]: this is the functor that sends a ring to its module of [[Kähler differential]]s.

$$
  (\Omega \dashv f) :  Mod \stackrel{\overset{\Omega}{\leftarrow}}{\underset{f}{\to}}
  CRing
  \,.
$$

### $R Mod$ is an abelian category
 {#RModIsAbelian}

Let the ambient [[monoidal category]] be [[Ab]] equipped with the [[tensor product of abelian groups]].

+-- {: .num_theorem #RModIsAbelian}
###### Theorem

Let $R$ be a [[commutative ring]]. Then $R Mod$ is an [[abelian category]].

=--

We discuss now all the ingredients of this statement in detail.

Let $U : R Mod \to Set$ be the [[forgetful functor]] to the underlying sets.

+-- {: .num_prop #RModHasZeroObject}
###### Proposition

$R Mod$ has a [[zero object]], given by the 0-module, the [[trivial group]] equipped with trivial $R$-action.

=--

+-- {: .proof}
###### Proof

Clearly the 0-module $0$ is a [[terminal object]], since every morphism $N \to 0$ has to send all elements of $N$ to the unique element of $0$, and every such morphism is a [[homomorphism]].
Also, 0 is an [[initial object]] because a morphism $0 \to N$ always exists and is unique, as it has to send the unique element of 0, which is the neutral element, to the neutral element of $N$.

=--

+-- {: .num_prop #RModHasKernelsAndCokernels}
###### Proposition

1. $R Mod$ has all [[kernels]]. The kernel of a homomorphism $f : N_1 \to N_2$ is the set-theoretic [[preimage]] $U(f)^{-1}(0)$ equipped with the induced $R$-module structure.

1. $R Mod$ has all [[cokernels]]. The cokernel of a homomorphism $f : N_1 \to N_2$ is the [[quotient]] abelian group 

   $$
     coker f = \frac{N_2}{im(f)}
   $$

   of $N_2$ by the [[image]] of $f$.

=--

+-- {: .proof}
###### Proof

The defining [[universal property]] of kernel and cokernels is immediately checked.

=--

+-- {: .num_prop }
###### Proposition

$U : R Mod \to Set$ preserves and reflects [[monomorphisms]] and [[epimorphisms]]:

A homomorphism $f : N_1 \to N_2$ in $R Mod$ is a [[monomorphism]] / [[epimorphism]] precisely if $U(f)$ is an [[injection]] / [[surjection]].

=--

+-- {: .proof}
###### Proof

Suppose that $f$ is a [[monomorphism]], hence that $f : N_1 \to N_2$ is such that for all morphisms $g_1, g_2 : K \to N_1$ such that $f \circ g_1 = f \circ g_2$ already $g_1 = g_2$. Let then $g_1$ and $g_2$ be the inclusion of [[submodules]] generated by a single element $k_1 \in K$ and $k_2 \in K$, respectively. It follows that if $f(k_1) = f(k_2)$ then already $k_1 = k_2$ and so $f$ is an [[injection]].  Conversely, if $f$ is an injection then its image is a [[submodule]] and it follows directly that $f$ is a monomorphism.

Dually for epimorphisms and surjections.

=--

+-- {: .num_defn #AbelianGroupStructureOnHoms}
###### Definition

For $N_1, N_2 \in R Mod$ two modules, define on the [[hom set]] $Hom_{R Mod}(N_1,N_2)$ the structure of an [[abelian group]] whose addition is given by argumentwise addition in $N_2$: $(f_1 + f_2) : n \mapsto f_1(n) + f_2(n)$.


=--

+-- {: .num_prop #RModIsAbEnriched}
###### Proposition

With def. \ref{AbelianGroupStructureOnHoms} $R Mod$ composition of morphisms

$$
  \circ : Hom(N_1, N_2) \times Hom(N_2, N_3) \to Hom(N_1,N_3)
$$

is a [[bilinear map]], hence is equivalently a morphism

$$
  Hom(N_1, N_2) \otimes Hom(N_2,N_3) \to Hom(N_1, N_3)
$$

out of the [[tensor product of abelian groups]]. 

This makes $R Mod$ into an [[Ab-enriched category]]. 

=--

+-- {: .proof}
###### Proof

Linearity of composition in the second argument is immediate from the pointwise definition of the abelian group structure on morphisms. 
Linearity of the composition in the first argument comes down to linearity of the second module homomorphism.

=--


+-- {: .num_remark }
###### Remark

In fact $R Mod$ is even a [[closed category]], but this we don not need for showsing that it is abelian.

=--

Prop. \ref{RModHasZeroObject} and prop. \ref{RModIsAbEnriched} together say that:

+-- {: .num_cor #RModIsAdditive}
###### Corollary

$R Mod$ is an [[pre-additive category]]. 

=--

+-- {: .num_prop #RModHasProductsAndCoproducts}
###### Proposition

$R Mod$ has all [[products]] and [[coproducts]], being [[direct products]] $\prod_{i \in I} N_i$ and  [[direct sums]] $\oplus_{i \in I} N_i$. 

The products are given by [[cartesian product]] of the underlying sets with componentwise addition and $R$-action.

The direct sum is the [[submodule]] of the direct product consisting of tuples of elements such that only finitely many are non-zero.

=--

+-- {: .proof}
###### Proof

The defining [[universal properties]] are directly checked. Notice that the direct product $\prod_{i \in I} N_i$ consists of arbitrary tuples because it needs to have a projection map 

$$
  p_j : \prod_{i \in I} N_i \to N_j
$$

to each of the modules in the product, reproducing all of a possibly infinite number of non-trivial maps $\{K \to N_j\}$. On the other hand, the direct sum just needs to contain all the modules in the sum

$$
  \iota_j : N_j \to \oplus_{i \in I} N_i
$$

and since, being a module, it needs to be closed only under addition of _finitely_ many elements, so it consists only of [[linear combinations]] of the elements in the $N_j$, hence of finite formal sums of these.

=--

Together cor. \ref{RModIsAdditive} and prop. \ref{RModHasProductsAndCoproducts} say that:

+-- {: .num_cor #RModIsAdditive}
###### Corollary

$R Mod$ is an [[additive category]].

=--


+-- {: .num_prop #InRModMonosAreKernelOfTheirCokernel}
###### Proposition

In $R Mod$

* every [[monomorphism]] is the [[kernel]] of its [[cokernel]];

* every [[epimorphism]] is the [[cokernel]] of its [[kernel]].

=--

+-- {: .proof}
###### Proof

Using prop. \ref{RModHasKernelsAndCokernels} this is directly checked on the underlying sets: given a monomorphism $K \hookrightarrow N$, its cokernel is $N \to \frac{N}{K}$, The kernel of that morphism is evidently $K \hookrightarrow N$.

=--

Now cor. \ref{RModIsAdditive} and prop. \ref{InRModMonosAreKernelOfTheirCokernel} imply theorem \ref{RModIsAbelian}, by definition.


## References

Discussion of $R Mod$ in $(Ab, \otimes)$ being an [[abelian category]] is for instance in 

* Rankeya Datta, _The category of modules over a commutative ring and abelian categories_ ([pdf](http://www.math.columbia.edu/~ums/pdf/Rankeya_R-mod_and_Abelian_Categories.pdf))

A summary of the discussion in [Mod as a bifibration](#ModAsBifibration) and [Tangents and deformation theory](#TangentsAndDeformationTheory) together with their embedding into the bigger picture of [[tangent (∞,1)-category|tangent (∞,1)-categories]] is in

* [[Jacob Lurie]], _[[Deformation Theory]]_


category: category

[[!redirects Mod]]

[[!redirects RMod]]
[[!redirects R Mod]]
[[!redirects R-Mod]]
[[!redirects KMod]]
[[!redirects K Mod]]
[[!redirects K-Mod]]
[[!redirects kMod]]
[[!redirects k Mod]]
[[!redirects k-Mod]]

[[!redirects category of modules]]
[[!redirects categories of modules]]

[[!redirects module category]]