
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Let $R$ be a [[commutative ring]]. The [[category]] of [[associative algebras]] over $R$ is the category

$$
  \mathsf{Alg}_R 
  = 
  {R \downarrow \mathsf{Ring}}
$$

of [[rings]] [[undercategory|under]] $R$. If $R$ is a commutative [[rig]], we can do the same with

$$ \mathsf{Alg}_R = {R \downarrow \mathsf{Rig}} .
$$

The _tensor product of $R$-algebras_ has as [[underlying]] $R$-[[module]] just the [[tensor product of modules]] of the underlying modules, $A \otimes_R B$. On homogeneous elements $(a,b) \in A \times B \stackrel{\otimes}{\to} A \otimes_R B$ the algebra structure is given by

$$
  (a_1, b_1) \cdot (a_2, b_2) = (a_1 \cdot a_2, b_1 \cdot b_2)
  \,.
$$

We write also $A \otimes_R B$ for the tensor product of algebras.

For [[commutative algebra|commutative]] $R$-algebras, the tensor product is the [[coproduct]] in $Comm Alg_R$:

$$
  A \otimes_R B 
  \simeq 
  A \coprod B 
  \in 
  Comm Alg_R 
  = 
  Comm R \downarrow \mathsf{Rig}
  ;
$$

hence the [[pushout]] in [[CRing]]

$$
  \array{
     && R
     \\
     & \swarrow && \searrow
     \\
     A &&&& B
     \\
     & \searrow && \swarrow
     \\
     && A \otimes_R B
  }
  \,.
$$

See at _[[category of monoids#PushoutOfCommutativeMonoids|pushouts of commutative monoids]]_.

## Properties

### Relation to tensor product of categories of modules

For $A$ an associative algebra over a [[field]] $k$, write $A$[[Mod]] for its [[category of modules]] of finite [[dimension]]. Then the tensor product of algebras corresponds to the [[Deligne tensor product of abelian categories]] $\boxtimes \colon Ab \times Ab \to Ab$:

$$
  (A \otimes_k B) Mod \simeq  (A Mod) \otimes (B Mod)
  \,.
$$

See at _[[tensor product of abelian categories]]_ for more.

## Related concepts

* [[tensor product]]

* [[tensor product of abelian groups]]

* [[tensor product of modules]]

* [[tensor product of algebras over a commutative monad]]

* [[Hochschild cohomology]]


[[!redirects tensor product of algebras]]
[[!redirects tensor products of algebras]]

[[!redirects tensor product of commutative algebras]]
[[!redirects tensor products of commutative algebras]]
