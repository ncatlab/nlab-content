
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Thoughout let $R$ be some [[ring]]. Write $R$[[Mod]] for the [[category]] of [[module]] over $R$. Write $U R Mod \to$ [[Set]] for the [[forgetful functor]] that sends a module to its underlying [[set]].

+-- {: .num_defn}
###### Definition

For $N \in R Mod$ a module, a **submodule** of $N$ is a [[subset]] of $U(N)$ which 

1. is a [[subgroup]] of the underlying group (closed under the addition in $N$);

1. is preserved by the $R$-[[action]].

=--

Equivalently this means:

+-- {: .num_defn}
###### Definition

A submodule of $N \in R Mod$ is a module [[homomorphism]] $i : K \to N$ whose underlying map $U(i)$ of sets is an [[injection]].

=--

And since the injections in $R$[[Mod]] are precisely the [[monomorphisms]], this means that equivalently

+-- {: .num_defn}
###### Definition

A submodule of $N \in R Mod$ is a [[monomorphism]] $i : K \hookrightarrow N$ in $R$[[Mod]]. Hence a submodule is a [[subobject]] in $R$[[Mod]].

=--

+-- {: .num_remark}
###### Remark

Given a submodule $K \hookrightarrow N$, the [[quotient module]] $\frac{N}{K}$ is the [[quotient group]] of the underlying abelian groups.

=--


## Examples


+-- {: .num_example}
###### Example

For $N = R$ regarded as a [[module]] over itself, a submodule is precisely an [[ideal]] of $R$.

=--

+-- {: .num_example #KernelAndImage}
###### Example

For $f : N_1 \to N_2$ a [[homomorphism]] of modules, 

1. the [[kernel]] $ker(f) \hookrightarrow N_1$ is a submodule of $N_1$,

1. the [[image]] $im(f) \hookrightarrow N_2$ is a submodule of $N_2$.

=--

+-- {: .num_remark}
###### Remark

In example \ref{KernelAndImage} [[quotient module]] of $N_2$ by the image is the [[cokernel]] of $f$

$$
  coker(f) \simeq \frac{N_2}{im(f)}
  \,.
$$ 

=--

## Properties

### Of free modules

Let $R$ be a [[ring]].

+-- {: .num_prop }
###### Proposition

Assuming the [[axiom of choice]], the following are equivalent

1. every submodule of a [[free module]] over $R$ is itself free;

1. every [[ideal]] in $R$ is a free $R$-module;

1. $R$ is a [[principal ideal domain]].

=--

A proof is in ([Rotman, pages 650-651](#Rotman)).

## Related concepts

* [[subgroup]], [[subring]]

## References

For instance

* Rotman _Advanced Modern Algebra_
 {#Rotman}


[[!redirects submodules]]

