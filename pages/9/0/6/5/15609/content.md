
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Formal geometry
+-- {: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Directly analogous to the concept of [[completion of a ring]] is the _completion of a module_ over that ring.

## Definition

### For modules over a commutative ring

+-- {: .num_defn}
###### Definition

For $A$ a [[commutative ring]], $\mathfrak{a} \subset A$ an ideal in $A$ and for $N$ an $A$-[[module]], then the _$\mathfrak{a}$-adic completion_ or _formal completion at $\mathfrak{a}$_ of $N$ is the [[filtered limit]]

$$
  N^{\wedge}_{\mathfrak{a}}
  \coloneqq
  \underset{\leftarrow}{\lim}_n
  N/(\mathfrak{a}^n N)
  \,.
$$

=--

### For $\infty$-modules over an $E_\infty$-ring


Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 

+-- {: .num_defn #TorsionInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-torsion module_ if for all elements $n \in \pi_k N$ and all elements $a \in \mathfrak{a}$ there is $k \in \mathbb{N}$ such that $a^k n = 0$.

=--

([Lurie "Completions", def. 4.1,3](#LurieCompletions)).

+-- {: .num_defn #LocalInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-local module_ if for every $\mathfrak{a}$-torsion module $T$ (def. \ref{TorsionInfinityModule}), the [[derived hom space]]

$$
 Hom_A(T,N) \simeq \ast
$$

is contractible.

=--

([Lurie "Completions", def. 4.1.9](#LurieCompletions)).


+-- {: .num_defn}
###### Definition/Proposition

An [[∞-module]] $N$ over $A$ is _$\mathfrak{a}$-complete_ if for all $\mathfrak{a}$-local $\infty$-modules $L$ (def. \ref{LocalInfinityModule}) then $Hom_A(L,N) \simeq \ast$.

The [[full sub-(∞,1)-category]]

$$
  A Mod_{\mathfrak{a}comp}
  \hookrightarrow
  A Mod
$$

of the [[(∞,1)-category of ∞-modules]] on the $\mathbb{a}$-complete ones is a [[reflective sub-(∞,1)-category]]. The reflector

$$
  \flat_{\mathfrak{a}} \colon A Mod \longrightarrow A Mod_{\mathfrak{a}compl} \hookrightarrow A Mod
$$

$$
  N \mapsto N^{\wedge}_{\mathfrak{a}}
$$

is called _$\mathfrak{a}$-completion_.

=--

([Lurie "Completions", def. 4.2.1, lemma 4.2.2](#LurieCompletions)).



## Properties

### Relation of formal completion to torsion approximation
 {#RelationToTorsionApproximation}

For suitable ideals $\mathfrak{a}\subset A$ of a commutative ring $A$, then the [[derived functor]] of $\mathfrak{a}$-adic [[completion of a module|completion of A-modules]] forms together with $\mathfrak{a}$-[[torsion approximation]] an [[adjoint modality]] on the  
[[(∞,1)-category of modules]] over $A$. See at _[arithmetic fracturing for chain complexes](fracture+theorem#CompletionAndTorsionOnDerivedCategories)_ for details.


## References

Discussion in the context of [[higher algebra]] is in

* {#LurieCompletions} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

[[!redirects completions of a module]]

[[!redirects completion of modules]]
[[!redirects completions of modules]]