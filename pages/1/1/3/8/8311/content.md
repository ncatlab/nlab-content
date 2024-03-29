
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[tensor product]] of [[modules]].

## Definition

+-- {: .num_defn}
###### Definition

Let $R$ be a [[commutative ring]] and consider the multicategory $R$[[Mod]] of $R$-[[modules]] and $R$-[[multilinear maps]].  In this case the 
[[tensor product of modules]] $A\otimes_R B$ of $R$-[[modules]] $A$ and $B$ can be constructed as the [[quotient]] of the [[tensor product of abelian groups]] $A\otimes B$ underlying them by the [[action]] of $R$; that is,
$$ A\otimes_R B = A\otimes B / (a,r\cdot b) \sim (a\cdot r,b). $$

=--

More [[category theory|category-theoretically]]:

+-- {: .num_defn}
###### Definition

The tensor product $A \otimes_R B$
is the [[coequalizer]] of the two maps
$$ A\otimes R \otimes B \;\rightrightarrows\; A\otimes B $$
given by the action of $R$ on $A$ and on $B$.  

=--

+-- {: .num_remark}
###### Remark


If the ring $R$ happens to be a [[field]], then $R$-modules are [[vector spaces]] and the tensor product of $R$-modules becomes the [[tensor product of vector spaces]].


=--

+-- {: .num_remark}
###### Remark


This tensor product can be generalized to the case when $R$ is not commutative, as long as $A$ is a right $R$-module and $B$ is a left $R$-module.  More generally yet, if $R$ is a [[monoid]] in any [[monoidal category]] (a ring being a monoid in [[Ab]] with its tensor product), we can define the tensor product of a left and a right $R$-module in an analogous way.  If $R$ is a commutative monoid in a [[symmetric monoidal category]], so that left and right $R$-modules coincide, then $A\otimes_R B$ is again an $R$-module, while if $R$ is not commutative then $A\otimes_R B$ will no longer be an $R$-module of any sort.

=--

+-- {: .num_remark}
###### Remark

The tensor product of modules can be generalized to the [[tensor product of functors]].

=--

## Properties

### Monoidal category structure
 {#MonoidalCategoryStructure}

The category $R$[[Mod]] equipped with the tensor product of modules $\otimes_R$ becomes a [[monoidal category]], in fact a [[distributive monoidal category]].

+-- {: .num_prop}
###### Proposition

A [[monoid]] in $(R Mod, \otimes)$ is equivalently an $R$-[[associative algebra|algebra]].

=--

+-- {: .num_prop #DistributivityOverDirectSum}
###### Proposition

The tensor product of modules [[distributivity|distributes]] over the [[direct sum]] of modules: 

$$
  A \otimes \left(\oplus_{s \in S} B_s\right)
  \simeq
  \oplus_{s \in S} ( A \otimes B_c )
  \,.
$$

=--



### Characterization by exact additive functors

See _[[Eilenberg-Watts theorem]]_.

### Exactness properties
 {#ExactnessProperties}

Let $R$ be a [[commutative ring]].

+-- {: .num_prop}
###### Proposition

For $N \in R Mod$ a module, the [[functor]] of tensoring with this module

$$
  (-) \otimes_R N \colon R Mod \to R Mod
$$

is an [[additive functor|additve]] [[right exact functor]].

=--

+-- {: .proof}
###### Proof

The functor is [[additive functor|additive]] by the [[distributivity]] of tensor products over [[direct sums]], prop. \ref{DistributivityOverDirectSum}.

A [[category theory|general abstract]] way of seeing that the functor is right exact is to notice that $(-)\otimes_R N$ is a [[left adjoint]] functor, its [[right adjoint]] being the [[internal hom]] $[N,-]$ (see at [[Mod]]). By the discussion at _[[adjoint functor]]_ this means that $(-) \otimes_R N$ even preserves all [[colimits]], in particular the [[finite colimits]].

=--


+-- {: .num_remark}
###### Remark

The functor $(-)\otimes_R N$ is **not** a [[left exact functor]] (hence not an [[exact functor]]) for all choices of $R$ and $N$.

=--

+-- {: .num_example}
###### Example

Let $R \coloneqq \mathbb{Z}$, hence $R Mod \simeq$ [[Ab]] and let $N \coloneqq \mathbb{Z}/2\mathbb{Z}$ the [[cyclic group]] or [[order]] 2. 
Moreover, consider the inclusion $\mathbb{Z} \stackrel{\cdot 2}{\hookrightarrow} \mathbb{T}$ sitting in the [[short exact sequence]]

$$
  0 \to \mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z} \to \mathbb{Z}/2\mathbb{Z} \to 0
  \,.
$$

The functor $(-) \otimes \mathbb{Z}/2\mathbb{Z}$ sends this to

$$
  0 \to \mathbb{Z}/2\mathbb{Z} 
    \stackrel{0}{\to}
  \mathbb{Z}/2\mathbb{Z}
   \stackrel{id}{\to}
  \mathbb{Z}/2\mathbb{Z}
  \to 0
  \,.
$$

Here the morphism on the left is the 0-morphism: in components it is given for all $n_1, n_2 \in \mathbb{Z}$ by

$$
  \begin{aligned}
    (n_1, n_2 mod 2) 
    & \mapsto 
    (2 n_1, n_2 mod 2)
    \\
    & \simeq 2 (n_1, n_2 mod 2)
    \\
    & \simeq (n_1, 2 n_2 mod 2)
    \\
    & \simeq (n_1, 0)
    \\
    & \simeq 0
  \end{aligned} 
  \,.
$$ 

Hence this is not a [[short exact sequence]] anymore.

=--

One kind of module $N$ for which $(-)\otimes_R N$ is always exact are [[free modules]].

+-- {: .num_example}
###### Example

Let $i \colon N_1 \hookrightarrow N_2$ be an inclusion of a [[submodule]]. For $S \in $ [[Set]] write $R^{\oplus {\vert S\vert}} = R[S]$ for the [[free module]] on $S$. Then 

$$
  i \otimes_R N \colon N_1 \otimes_R R^{\oplus {\vert S\vert}} \to N_2 \otimes_R R^{\oplus {\vert S\vert}}
$$

is again a [[monomorphism]]. Indeed, due to the [[distributivity]] of the tensor product over the [[direct sum]] and using that $R \in R Mod$ is the tensor unit, this is 

$$  
  i^{\oplus {\vert S\vert}} \colon N_1^{\oplus {\vert S\vert}} \hookrightarrow N_2^{\oplus {\vert S\vert}}
  \,.
$$

=--

There are more modules $N$ than the free ones for which $(-)\otimes_R N$ is exact. One says

+-- {: .num_defn}
###### Definition

If $N \in R Mod$ is such that $(-)\otimes_R N \colon R Mod \to R Mod$ is a [[left exact functor]] (hence an [[exact functor]]), $N$ is called a **[[flat module]]**.

=--
 
+-- {: .num_remark}
###### Remark

For a general module, a measure of the failure of $(-)\otimes_R N$ to be exact is given by the [[Tor]]-functor $Tor^1(-,N)$. See there for more details.

=--

## Related concepts

* [[tensor product of abelian groups]]

* [[tensor product of bimodules]]

* [[tensor product of vector bundles]]

* [[tensor product of algebras]]

* [[tensor product of algebras over a commutative monad]]

* [[tensor product of chain complexes]]

* [[tensor product of ∞-modules]]

* [[tensor product of functors]]


## References

Textbook accounts:

* [[Frank W. Anderson]], [[Kent R. Fuller]], §19 in: _Rings and Categories of Modules_, Graduate Texts in Mathematics, **13** Springer (1992) &lbrack;[doi:10.1007/978-1-4612-4418-9](https://doi.org/10.1007/978-1-4612-4418-9)&rbrack;


* [[Paul Edwin Bland]], §2.3 in: *Rings and Their Modules*, De Gruyter (2011) &lbrack;[doi:10.1515/9783110250237](https://doi.org/10.1515/9783110250237), [pdf](http://site.iugaza.edu.ps/mashker/files/%D9%85%D8%AD%D8%A7%D8%B6%D8%B1%D8%A7%D8%AA-%D8%AC%D8%A8%D8%B1-%D8%AF%D9%83%D8%AA%D9%88%D8%B1%D8%A7%D8%A9.pdf)&rbrack;


Lecture notes:

* [[Keith Conrad]], *Tensor products* &lbrack;part I:[pdf](http://www.math.uconn.edu/~kconrad/blurbs/linmultialg/tensorprod.pdf), [[Conrad-TensorProductsI:file]]; part II: [pdf](https://kconrad.math.uconn.edu/blurbs/linmultialg/tensorprod2.pdf), [[Conrad-TensorProductsII:file]]&rbrack;

See also: 

* Wikipedia, *[Tensor product of modules](https://en.wikipedia.org/wiki/Tensor_product_of_modules)*

[[!redirects tensor products of modules]]