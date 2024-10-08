
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

The _extension of scalars_ of a [[module]] along a [[homomorphism]] of [[rings]] is the [[Isbell duality|algebraic dual]] of what geometrically is the [[pullback]] of [[bundles]] along a map of their base spaces (with respect to the discussion at _[modules - as generalized vector bundles](http://ncatlab.org/nlab/show/module#RelationToVectorBundlesInIntroduction)_).

Explicitly, extension of scalars along a [[ring]] [[homomorphism]] $f : R \to S$ is the operation on $R$-[[modules]] given by forming the [[tensor product of modules]] with $S$ regarded as an $R$-module via $f$.

There are similar functors for  [[bimodules]] and in some other categories. 


## Definition

Let $R$ and $S$ be [[commutative rings]] and let 
$f \colon R\to S$ 
be a [[homomorphism]] of [[rings]]. 

We discuss _extension of scalars_ along $f$ first [[category theory|general abstractly]] and then explicitly in components.

### General abstract

Write $R$[[Mod]] and $S$[[Mod]] for the [[categories of modules]] over $R$ and $S$, respectively. 

+-- {: .num_defn #RestrictionOfScalars}
###### Definition

Given a [[ring]] [[homomorphism]] $f : R \to S$ the **[[restriction of scalars]]** functor

$$
  f^* : S Mod \to R Mod
$$

is the [[functor]] that takes an $S$-[[module]] $N$ to the $R$-module $f^*N$ whose underlying [[abelian group]] is that of $N$ and whose $R$-[[action]] is given by

$$
  r \cdot n \coloneqq f(r)\cdot n \;\;\;\; for \; r \in R, n \in N
  \,.
$$

=--

+-- {: .num_prop #AdjointPair}
###### Proposition

The [[restriction of scalars]] functor, def. \ref{RestrictionOfScalars}, is the [[right adjoint]] in a pair of [[adjoint functors]] 

$$
  ( f_! \dashv f^* )
  \;\colon\;
  S Mod 
   \stackrel{\overset{f_!}{\longleftarrow}}
   {\underset{f^*}{\longrightarrow}}
  R Mod
  \,.
$$

=--

+-- {: .num_defn #ExtensionByAdjoint}
###### Definition

The [[left adjoint]] $f_! \colon R Mod \to S Mod$ in prop. \ref{AdjointPair} is called **extension of scalars** along $f$.

=--

+-- {: .num_remark }
###### Remark

A further [[right adjoint]] $f_*$ would be called _[[coextension of scalars]]_ along $f$.

=--

See also [[induced representation]] $\dashv$ [[restricted representation]].

### In components

+-- {: .num_prop}
###### Proposition

Given a [[ring]] [[homomorphism]] $f : R \to S$, the _extension of scalars_ [[functor]] $f_!$ of def. \ref{ExtensionByAdjoint} is the functor

$$ 
  f_! \coloneqq  S \otimes_R (-) \,:\, R Mod \to S Mod
$$ 

given by [[tensor product of modules]] with $S$ regarded as an $S$-$R$-[[bimodule]]: the left [[action]] being the canonical action of $S$ on itself, the right being the [[restriction of scalars]]-action along $f$.

Explicitly, for $N \in R Mod$ 

* the elements of $f_! N$ are [[equivalence classes]] of pairs $(s,n) \in S \times N$ under the [[equivalence relation]] $ (s \cdot f(r), n) = (s, r\cdot n) $ for all $s \in S$;

* the left $S$-[[action]] is given by $s' \cdot(s,n) = (s' \cdot s,n)$.

=--

## Properties

### Geometric interpretation

Under [[Isbell duality]] extension of scalars turns into a statement about [[geometry]].

By definition the category 

$$
  Ring^{op} \underoverset{Spec}{\colon \simeq}{\to}
  Aff
$$

of (absolute) [[affine schemes]] is the [[opposite category]] of [[Ring]].

Hence for $f : R \to S$ a [[ring]] [[homomorphism]], we have equivalently a morphism

$$
  Spec(f) : Spec(S) \to Spec(R)
$$

of affine schemes. 

An $R$-[[module]] $N$ corresponds to the collection of [[sections]] of a "generalized [[vector bundle]]" over $Spec(R)$: something that has a [[quasicoherent sheaf]] of sections. 

The [[pullback]] of this "bundle" along $Spec(f)$ has sections forming the module $f_! N$.

Generally, for any [[fibered category]] like [[Mod]]$\to Aff$ we may regard the [[inverse image functor]] as the extension of scalars. 

For that reason if there is some other fibered category $\mathcal{F}$ over the opposite of some algebraic category $\mathcal{A}$ whose objects are considered "objects of scalars" one is inclined to call the inverse image functor, the extension of scalars. 

### Frobenius extensions

Extension of scalars coincides with *[[coextension of scalars]]* (to make an [[ambidextrous adjunction]] with [[restriction of scalars]]) in the case of [[Frobenius extensions]], see there for more.

## Examples

* [[complexification]] is extension of scalars along the inclusion $\mathbb{R} \hookrightarrow \mathbb{C}$ of the [[real numbers]] into the [[complex numbers]].

* [[localization of a module]]

## Related concepts

* **extension of scalars** $\dashv$ [[restriction of scalars]] $\dashv$ [[coextension of scalars]]

* [[extension (double category theory)]]

