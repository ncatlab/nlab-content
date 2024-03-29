
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _sesquiunital sesquiagebra_ is an [[algebra object]] [[internalization|internal]] to the monoidal [[2-category]] [[2Mod]] of [[algebras]], [[bimodules]] and [[bimodule intertwiners]]. This means that it is an algebra equipped with an additional associative product and unit which are both exhibited by [[bimodules]]. If these bimodules come from algebra [[homomorphisms]] then the sesquialgebra is a [[bialgebra]].

The structure of a sesquialgebra is just so that the [[category of modules]] of the underlying algebra is itself a [[monoidal category]]. In this sense sesquialgebras are a placeholder for [[2-algebra|2-algebras]]. Moreover, in as far as these 2-algebras themselves are regarded as placeholders for _their_ [[2-category]] of [[2-modules]] a sesquialgebra presents a [[3-module]]/[[3-vector space]].

Sesquialgebras with an extra grouplike-property have been called _[[hopfish algebras]]_.


## Definition

+-- {: .num_defn}
###### Definition

A [[sesquiunital sesquialgebra]] over $R$ is an [[associative algebra]] $A$ over $R$ equipped with the structure of an [[algebra object]] internal to the [[2-category]] [[2Mod]] of [[associative algebras]], [[bimodules]] and [[bimodule intertwiners]].

This means that it is an $R$-algebra $A$ equipped with 

* a product $A \otimes_R A$-$A$-[[bimodule]] $\Delta$;

* a unit $R$-$A$-[[bimodule]] $\epsilon$

satisfying the evident [[associative law]] and [[unit law]].

=--


## Properties

### Tannaka duality and 2-rings

Precomposition with the product and unit bimodule makes the [[category of modules]] over the underlying [[associative algebra]] of a sesquialgebra itself into a [[monoidal category]].

See for instance ([Vercruysse, 5.3.3](#Vercruysse)).

In fact, regarding the [[category of modules]] $Mod_A$ as a [[2-abelian group]], the structure of a sesquialgebra on $A$ is equivalently the structure of a [[2-ring]] (see there) on $Mod_A$.

[[!include structure on algebras and their module categories - table]]


## References

* Joost Vercruysse, _Hopf algebras---Variant notions and reconstruction theorems_ ([arXiv:1202.3613](http://arxiv.org/abs/1202.3613))
 {#Vercruysse}

See also the references at _[[hopfish algebra]]_.


[[!redirects sesquialgebra]]
[[!redirects sesquialgebras]]

[[!redirects sesquiunital sesquialgebra]]
[[!redirects sesquiunital sesquialgebras]]
