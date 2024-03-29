
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

+-- {: .num_defn #TraditionalDefinition}
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

#### Torsion approximation
 {#TorsionApproximation}

+-- {: .num_defn #TorsionInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-torsion module_ if for all elements $n \in \pi_k N$ and all elements $a \in \mathfrak{a}$ there is $k \in \mathbb{N}$ such that $a^k n = 0$.

=--

([Lurie "Completions", def. 4.1.3](#LurieCompletions)).


+-- {: .num_prop #TorsionApproximation}
###### Proposition

The [[full sub-(∞,1)-category]]

$$
  A Mod_{\mathfrak{a}tor}
  \hookrightarrow
  A Mod
$$

is [[reflective sub-(∞,1)-category|co-reflective]] and the co-reflector $\Pi_{\mathfrak{a}}$ -- the _[[torsion approximation]]_ -- is [[smashing localization|smashing]].

=--

([Lurie "Completions", prop. 4.1.12](#LurieCompletions)).

+-- {: .num_prop}
###### Proposition

For $N \in A Mod_{\leq 0}$ then [[torsion approximation]], prop. \ref{TorsionApproximation}, intuced a [[monomorphism]] on $\pi_0$

$$
  \pi_0 \Pi_{\mathfrak{a}} N \hookrightarrow \pi_0 N
$$

including the $\mathfrak{a}$-nilpotent elements of $\pi_0 N$.

=--

([Lurie "Completions", prop. 4.1.18](#LurieCompletions)).

#### Localization
 {#Localization}

+-- {: .num_defn #LocalInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-local module_ if for every $\mathfrak{a}$-torsion module $T$ (def. \ref{TorsionInfinityModule}), the [[derived hom space]]

$$
 Hom_A(T,N) \simeq \ast
$$

is contractible.

=--

([Lurie "Completions", def. 4.1.9](#LurieCompletions)).

+-- {: .num_prop #LocalizationAwayByColimit}
###### Proposition

For $\mathfrak{a} = (a)$ generated from a single element, then the [localization of an (∞,1)-ring](localization+of+a+commutative+ring#ForEInfinityRings)-map $A \to A[a^{-1}]$ is given by the [[(∞,1)-colimit]] over the sequence of right-multiplication with $a$

$$
  A[a^{-1}]
  \simeq
  \underset{\rightarrow}{\lim}
  (
    A \stackrel{\cdot a}{\longrightarrow} A
    \stackrel{\cdot a}{\longrightarrow} A
    \stackrel{\cdot a}{\longrightarrow}  \cdots
  )
  \,.
$$

=--

([Lurie "Completions", remark 4.1.11](#LurieCompletions))

+-- {: .num_prop}
###### Proposition

The [[full sub-(∞,1)-category]]


$$
  A Mod_{\mathfrak{a}loc}
  \hookrightarrow
  A Mod
$$

of [[∞-modules]] [[localization of a module|local]] away from $\mathfrak{a}$ is [[reflective sub-(∞,1)-category|reflective]]. The reflector


$$
  \Pi_{\mathfrak{a}dR} \colon A Mod \longrightarrow A Mod_{\mathfrak{a}loc}
$$

is called _[[localization of a module|localization]]_.

=--

+-- {: .num_prop}
###### Proposition

There is a [[natural transformation|natural]] [[homotopy fiber sequence]]

$$
  &#643;_{\mathfrak{a}} \longrightarrow id \longrightarrow &#643;_{\mathfrak{a}dR}
$$

relating $\mathfrak{a}$-torsion approximation on the left with $\mathfrak{a}$-[[localization of a module|localization]] on the right.

=--


#### Completion

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
  \flat_{\mathfrak{a}} \colon A Mod \longrightarrow A Mod_{\mathfrak{a}comp} \hookrightarrow A Mod
$$

$$
  N \mapsto N^{\wedge}_{\mathfrak{a}}
$$

is called _$\mathfrak{a}$-completion_.

=--

([Lurie "Completions", def. 4.2.1, lemma 4.2.2](#LurieCompletions)).

Definition \ref{InfinityCompletion} relates to the traditional definition, def. \ref{TraditionalDefinition}, as follows

+-- {: .num_prop}
###### Proposition

Let $N$ a homotopically discrete [[∞-module]] over the [[E-∞ ring]] $A$ which is a [[Noetherian module]] in that all its submodules are finitely [[generators and relations|finitely generated]]. Then the $\mathfrak{a}$-completion of $N$ in the sense of def. \ref{InfinityCompletion} coincides with the traditional definition def. \ref{TraditionalDefinition}.

=--

([Lurie "Completions", prop. 4.3.6](#LurieCompletions))


## Properties

### General properties

The [[full sub-(∞,1)-category]] $A Mod_{\mathfrak{a} comp}$ is a [[locally presentable (∞,1)-category]].

([Lurie "Completions", prop. 4.1.17](#LurieCompletions))

### Monoidalness
 {#Monoidalness}

We discuss how both $\mathfrak{a}$-completion $\flat_{\mathfrak{a}}$ and $\mathfrak{a}$-[[torsion approximation]] $\Pi_{\mathfrak{a}}$ on $A Mod$ are [[monoidal (∞,1)-functors]] with respect to the [[smash product of spectra]] over $A$.

Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 


+-- {: .num_prop}
###### Proposition

The completion reflection $\flat_{\mathfrak{a}}$, def. \ref{InfinityCompletion}, is a [[monoidal (∞,1)-functor]].

=--

([Lurie "Completions", remark 4.2.6](#LurieCompletions)).


For the torsion approximation functor $\Pi_{\mathfrak{a}}$ one gets something slightly weaker, it preserves "monoids without unit":

+-- {: .num_prop}
###### Proposition

The [[full sub-(∞,1)-category]] of $\mathfrak{a}$-torsion modules, def. \ref{TorsionInfinityModule}, is [[reflective sub-(∞,1)-category|co-reflective]]

$$
  A Mod_{\mathfrak{a}tor}
  \stackrel{\hookrightarrow}{\underset{\Pi_{\mathfrak{a}}}{\longleftarrow}}
  A Mod
 \,.
$$

Moreover, the coreflector $\Pi_{\mathfrak{a}}$ is "[[smashing localization|smashing]]", in that there is $V \in A Mod$ such that $\Pi_{\mathfrak{a}}(-) \simeq V \wedge (-)$ is given by the [[smash product]] with $V$. If $\mathfrak{a} = (\{x_i\}_i) $ then $V$ is the [[tensor product]] $V =\underset{i}{\otimes} V_i$ over all the [[homotopy fibers]]

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

1. is a "[[monoidal (∞,1)-functor]]" except possibly for preservation of units.

=--

See also ([Lurie "Completions", cor. 4.1.16](#LurieCompletions)).





### Relation to localization

The [[homotopy cofiber]] of $\mathfrak{a}$-completion $\Pi_{\mathfrak{a}}$ is [[localization of a module|localization]] away from $\mathfrak{a}$, in that there is a [[homotopy fiber sequence]]

$$
  (-)_{\mathfrak{a}}^{\wedge} \to id \to (-)[\mathfrak{a}^{-1}]
$$

with the completion functor of def. \ref{InfinityCompletion} on the left and the localization functor of prop. \ref{LocalizationAwayByColimit} on the right.

([Lurie "Completions", example 4.1.14, remark 4.1.20](#LurieCompletions))

### Relation of formal completion to torsion approximation
 {#RelationToTorsionApproximation}

For suitable ideals $\mathfrak{a}\subset A$ of a commutative ring $A$ or more generally of an [[E-∞ ring]], then the [[derived functor]] of $\mathfrak{a}$-adic [[completion of a module|completion of A-modules]] forms together with $\mathfrak{a}$-[[torsion approximation]] an [[adjoint modality]] on the  
[[(∞,1)-category of modules]] over $A$. See at _[[fracture square]]_ for details.

[[!include arithmetic cohesion -- table]]


## References

Discussion in the context of [[higher algebra]] is in

* {#LurieCompletions} [[Jacob Lurie]], section 4 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

Discussion of formal completion of [[(infinity,1)-modules]] in terms of [[totalization]] of [[Amitsur complexes]] is in

* {#Carlsson07} [[Gunnar Carlsson]], _Derived completions in stable homotopy theory_, Journal of Pure and Applied Algebra Volume 212, Issue 3, March 2008, Pages 550&#8211;577 ([arXiv:0707.2585](http://arxiv.org/abs/0707.2585))


[[!redirects completions of a module]]

[[!redirects completion of modules]]
[[!redirects completions of modules]]

[[!redirects formal completion of a module]]


