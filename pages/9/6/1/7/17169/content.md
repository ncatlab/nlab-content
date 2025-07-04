
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Stable homotopy groups are [[homotopy groups]] as seen in [[stable homotopy theory]].

A [[morphism]] inducing an [[isomorphism]] on all stable homotopy groups is called a [[stable weak homotopy equivalence]].

## Definition

### For pointed topological spaces

Given a [[pointed topological space]] $X$, its _stable homotopy groups_ are the [[colimit]] of ordinary [[homotopy groups]] of its [[reduced suspensions]]

$$
  \pi_n^S(X) \coloneqq \underset{\longrightarrow}{\lim}_k \pi_{n+k}(\Sigma^k X)
  \,.
$$

### For sequential spectra

\begin{definition}
  \label{StableHomotopyGroupsOfSequentialSpectrum}

Given a  [[sequential spectrum]] $E$, in the form of a sequence of component spaces $E_n$ with structure maps $\Sigma E_n \to E_{n+1}$, then for $n \in \mathbb{Z}$ the $n$th _homotopy group_ of $E$ is the [[colimit]]

$$
  \begin{aligned}
  \pi_n(E) 
    & \coloneqq 
  \underset{\longrightarrow}{\lim}_k
  \pi_{n+k}(E_k)
  \\
  & \coloneqq
  \underset{\longrightarrow}{\lim}
  \left(
    \cdots
      \to
    \pi_{n+k}(E_k)
       \stackrel{\Sigma}{\longrightarrow}
    \pi_{n+k+1}(\Sigma E_k)
       \stackrel{\pi_{n+k+1}(\sigma_k^E)}{\longrightarrow}
    \pi_{n+k+1}(E_{k+1})
       \to
    \cdots
  \right)
  \end{aligned}
$$

over the [[homotopy groups]] of the component spaces. 

\end{definition}

For sequential spectra in [[simplicial sets]], the same formula applies for the [[geometric realization]] of the component simplicial sets.

(For details see [this definition](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroups).)


\begin{remark}
  \label{StableHomotopyGroupsOfOmegaSpectrum}

If a [[sequential spectrum]] $X$ is an [[Omega-spectrum]], then its colimiting stable homotopy groups according to Def. \ref{StableHomotopyGroupsOfSequentialSpectrum} reduce to the actual [[homotopy groups]] of the component spaces $X_n \coloneqq \Omega^\infty \Sigma^n X$, in that:

$$
  X \; \text{is Omega-spectrum}
  \;\;\;\;\;
   \Rightarrow
  \;\;\;\;\;
  \pi_k(X)
    \simeq
  \left\{
    \array{
      \pi_{k+n}\big( X_n \big)
      &\vert& 
      k + n \geq 0
      \\
      \pi_k\big(X_0\big)
      &\vert& 
      k \geq 0
      \\
      \pi_0 X_{\vert k \vert}  
      &\vert&  
      k \lt 0
      \\
    }
  \right.
  \,.
$$

\end{remark}

(For details see [this example](Introduction+to+Stable+homotopy+theory+--+1-1#StableHomotopyGroupsOfOmegaSpectrum).)


## Properties

### Suspension isomorphism

Let 

$$
  \Sigma
  \;\colon\;
  SeqSpec
  \longrightarrow
  SeqSpec
$$

be the operation of forming degreewise the [[smash product]] with the circle, the (un-derived, [[reduced suspension|reduced]]) [[suspension]] of $X$.

+-- {: .num_prop #SuspensionIsomorphismOfStableHomotopyGroups}
###### Proposition

For $X$ a [[sequential spectrum]], smashing with $S^1$ constitutes [[natural isomorphisms]] of stable homotopy groups of $X$ with the stable homotopy groups in one degree higher of the suspension spectrum of $X$

$$ 
  S^1 \wedge (-)
    \;\colon\; 
  \pi_\bullet(X)
    \stackrel{\simeq}{\longrightarrow}
  \pi_{\bullet+1}(\Sigma X)
  \,.
$$

=--

(e.g. [Schwede 12, part I, prop. 2.6](#Schwede12))

### For suspension spectra

For $E = \Sigma^\infty X$ the [[suspension spectrum]] of a [[pointed topological space]], we have

$$
  \pi_n^S(X) \simeq \pi_n(\Sigma^\infty X)
  \,.
$$


### As a homology theory

The assignment of [[stable homotopy groups]] to [[topological spaces]] $X$ ([[CW-complexes]])

$$
  X \mapsto \pi_\bullet^{st}(X) \coloneqq \pi_\bullet(\Sigma^\infty X)
$$

satisfies the [[axioms]] of a [[generalized homology theory]]. As such this is also called _[[stable homotopy homology theory]]_.



## Examples

* [[stable homotopy groups of spheres]]

* [[Thom's theorem]]

## Related concepts

* [[homotopy group]]

* [[free infinite loop space]]

* [[equivariant homotopy group]]


## Examples

* The homotopy groups of a [[suspension spectrum]] $\Sigma^\infty X$ of a [[pointed topological space]] $X$ are the _[[stable homotopy groups]]_ of $X$.

* In particular the homotopy groups of the [[sphere spectrum]] are the _[[stable homotopy groups of spheres]]_.

* [[Thom's theorem]] says that the homotopy groups of the [[Thom spectrum]] $M O$ form the (unoriented) [[cobordism ring]].

## References

* [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_ (2012)

[[!redirects homotopy groups of a spectrum]]

[[!redirects homotopy groups of spectra]]

[[!redirects stable homotopy group]]
[[!redirects stable homotopy groups]]

