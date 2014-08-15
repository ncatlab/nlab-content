
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

In particular the [[formal completion]] or _adic completion_ of a ring $A$ at an ideal $\mathfrak{a}$ has a corresponding analog for modules. Where the adic completion $A_{\mathfrak{a}}^\wedge$ of the ring itself has the geometric interpretation of forming the [[formal neighbourhood]] $Spf(A_{\mathfrak{a}}^\wedge)$ of [[spectrum of a commutative ring|ring spectra]] $Spec(A/\mathfrak{a}) \hookrightarrow Spec(A)$, so under the interpretation (see [here](module#RelationToVectorBundlesInIntroduction)) of $A$-[[modules]] as [[bundles]] over $Spec(A)$, the $\mathfrak{a}$-adic completion $N_{\mathfrak{a}}^\wedge$ of an $A$-module $N$ has the interpretation of being the restriction of that bundle to that formal neighbourhood.



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
$$

of [[quotients]] of $N$ by the submodules induced by all powers of the ideal.

=--

There is a canonical projection map $N \longrightarrow N^\wedge_{\mathfrak{a}}$. Its [[kernel]] is sometimes called the $\mathfrak{a}$-[[adic residual]].

### For $\infty$-modules over an $E_\infty$-ring


Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 

+-- {: .num_defn #TorsionInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-torsion module_ if for all elements $n \in \pi_k N$ and all elements $a \in \mathfrak{a}$ there is $k \in \mathbb{N}$ such that $a^k n = 0$.

=--

([Lurie "Completions", def. 4.1.n3](#LurieCompletions)).

+-- {: .num_defn #LocalInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-local module_ if for every $\mathfrak{a}$-torsion module $T$ (def. \ref{TorsionInfinityModule}), the [[derived hom space]]

$$
 Hom_A(T,N) \simeq \ast
$$

is contractible.

=--

([Lurie "Completions", def. 4.1.9](#LurieCompletions)).


+-- {: .num_defn #InfinityCompletion}
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

### Monoidalness
 {#Monoidalness}

We discuss how both $\mathfrak{a}$-completion $\flat_{\mathfrak{a}}$ and $\mathfrak{a}$-[[torsion approximation]] $\Pi_{\mathfrak{a}}$ on $A Mod$ are [[monoidal (∞,1)-functors]] with respect to the [[smash product of spectra]] over $A$.

Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 


+-- {: .num_prop}
###### Proposition

The [[full sub-(∞,1)-category]] of $\mathfrak{a}$-torsion modules, def. \ref{TorsionInfinityModule}, is [[reflective sub-(∞,1)-category|co-reflective]]

$$
  A Mod_{\mathfrak{a}tor}
  \stackrel{\hookrightarrow}{\underset{\Pi_{\mathfrak{a}}}{\longleftarrow}}
  A Mod
 \,.
$$

Moreover, the coreflector $\Pi_{\mathfrak{a}}$ is "[[smashing localization|smashing]]", in that there is $V \in A Mod$ such that $\Pi_{\mathfrak{a}}(-) \simeq \wedge (-)$ is given by the [[smash product]] with $V$. If $\mathfrak{a} = (x_i)_i \Omega (A[x_i^{-1}]/A)$ then $V$ is the tensor product $V =\underset{i}{\otimes} V_i$ over all the [[homotopy fibers]]

$$
  \Omega (A[x_i^{-1}]/A) \longrightarrow A \longrightarrow A[x_i^{-1}]
  \,.
$$

=--

([Lurie "Completions", prop. 4.1.12](#LurieCompletions)).

From the general properties of [[smashing localization]] it follows that

+-- {: .num_cor}
###### Corollary

The coreflection $\Pi_{\mathfrak{a}} \colon A Mod \to A Mod$

1. preserves small [[(∞,1)-colimits]];

1. is a [[monoidal (∞,1)-functor]].

=--

See also ([Lurie "Completions", cor. 4.1.16](#LurieCompletions)).

Also

+-- {: .num_prop}
###### Proposition

The completion reflection $\flat_{\mathfrak{a}}$, def. \ref{InfinityCompletion}, is a [[monoidal (∞,1)-functor]].

=--

([Lurie "Completions", remark 4.2.6](#LurieCompletions)).


### Relation of formal completion to torsion approximation
 {#RelationToTorsionApproximation}

For suitable ideals $\mathfrak{a}\subset A$ of a commutative ring $A$ or more generally of an [[E-∞ ring]], then the [[derived functor]] of $\mathfrak{a}$-adic [[completion of a module|completion of A-modules]] forms together with $\mathfrak{a}$-[[torsion approximation]] an [[adjoint modality]] on the  
[[(∞,1)-category of modules]] over $A$. See at _[[fracture square]]_ for details.


## References

Discussion in the context of [[higher algebra]] is in

* {#LurieCompletions} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

[[!redirects completions of a module]]

[[!redirects completion of modules]]
[[!redirects completions of modules]]