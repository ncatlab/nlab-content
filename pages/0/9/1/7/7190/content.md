
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _proper map of toposes_ is the generalization to [[toposes]] of the notion of [[proper map]] of [[topological spaces]].

## Definition

+-- {: .num_defn #CompactTopos}
###### Definition

A [[sheaf topos]] $\mathcal{E}$ is called a **[[compact topos]]** if the [[direct image]] of the [[global section geometric morphism]] $\Gamma : \mathcal{E} \to Set$ preserves [[directed colimit|directed]] [[joins]] of [[subterminal objects]].

A [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ is called **proper** if it exhibits $\mathcal{F}$ as a [[compact topos]] over $\mathcal{E}$.


=--

+-- {: .num_defn #StronglyCompactTopos}
###### Definition


A topos is called **strongly compact** if $\Gamma$ commutes even with all [[filtered colimits]] ([MV, p. 53](#MoerdijkVermeulen)).

A geometric morpjhism $f : \mathcal{F} \to \mathcal{E}$ is called **tidy** if it exhibits $\mathcal{F}$ as a strongly compact topos over $\mathcal{E}$.


=--



## Properties

### Compact sites
 {#CompactSites}

We discuss classes of [[sites]] such that their [[sheaf topos]] is a compact topos, def. \ref{CompactTopos} ([VM, I.5](#MoerdijkVermeulen)).

(...)

### Strongly compact sites
 {#StronglyCompactSites}

We discuss classes of [[sites]] such that their [[sheaf topos]] is a strongly compact topos, def. \ref{CompactTopos} ([VM, III.4](#MoerdijkVermeulen)).

(...)

## Examples

### Strongly compact toposes
 {#StronglyCompactToposes}

The following propositions say in summary that

1. the _[[petit topos]]_ over a [[compact topological space]] that is also [[Hausdorff topological space|Hausdorff]] is strongly compact.

1. the _[[gros topos]]_ over a [[compact object]] is strongly compact.

See also ([VM, III.1](#MoerdijkVermeulen)).

+-- {: .num_prop}
###### Proposition

Examples of strongly compact toposes $\mathcal{E}$, def. \ref{StronglyCompactTopos}, include the following.

1. Every [[coherent topos]] is strongly compact.

1. The [[sheaf topos]] over a [[compact topological space|compact]] [[Hausdorff space|Hausdorff]] [[topological space]] is strongly compact.

=--

([MV, Examples III.1.1](#MoerdijkVermeulen))


+-- {: .num_prop #SliceOverCompactIsStronglyCompact}
###### Proposition

Let $\mathbf{H}$ be a topos over [[Set]] and $X \in \mathbf{H}$ an object. If $X$ is a [[compact object]] (in the sense that the [[hom functor]] $\mathbf{H}(X,-)$ preserves [[filtered colimits]]) then the [[slice topos]] $\mathbf{H}_{/X}$ is strongly compact, def. \ref{StronglyCompactTopos}.

=--

+-- {: .proof}
###### Proof

The [[global section geometric morphism]] $\Gamma : \mathbf{H}_{/X} \to Set $ is given by the [[hom functor]] out of the [[terminal object]], which in $\mathbf{H}_{/X}$ is $id_X : X \to X$. This takes any $E \to X$ in $\mathbf{H}_{/X}$ to the set of [[sections]]

$$
  \Gamma_X([E \to X]) = \mathbf{H}(X,E) \times_{\mathbf{H}(X,X)} \{id\}
  \,.
$$

By the discussion at _[overcategory -- limits and colimits](overcategory#LimitsAndColimits)_ we have that [[colimits]] in $\mathbf{H}_{/X}$ are computed in $\mathbf{H}$. So if 
$[E \to X] \simeq \underset{\longrightarrow_i}{\lim}{[E_i \to X]}$ is a [[filtered colimit]] in $\mathbf{H}_{/X}$, then $E \simeq \underset{\longrightarrow_i}{\lim}{E_i }$ is a filtered colimit in $\mathbf{H}$. 

If now $X \in \mathbf{H}$ is a [[compact object]], then this commutes over this colimit and hence

$$
  \begin{aligned}
    \Gamma_X([E \to X]) 
    &= 
    \mathbf{H}(X,\underset{\longrightarrow_i}{\lim} E_i) \times_{\mathbf{H}(X,X)} \{id\}
    \\
    & \simeq
    (\underset{\longrightarrow_i}{\lim}\mathbf{H}(X, E_i)) \times_{\mathbf{H}(X,X)} \{id\}
    \\
    &\simeq
    \underset{\longrightarrow_i}{\lim}
    (\mathbf{H}(X, E_i) \times_{\mathbf{H}(X,X)} \{id\})
    \\
    & \simeq 
    \underset{\longrightarrow_i}{\lim}
    \Gamma_X([E_i \to X])
   \end{aligned}
  \,,
$$

where in the second but last step we used that in the [[topos]] [[Set]] [[universal colimits|colimits are preserved by pullback]]. 

This shows that $\Gamma_X(-) : \mathbf{H}_{/X} \to Set$ commutes over filtered colimits if $X$ is a [[compact object]].

=--

### Finite objects

+-- {: .num_prop}
###### Proposition

An object $X \in \mathcal{T}$ in a topos $\mathcal{T}$ is a [[Kuratowski finite object]] precisely if the [[étale geometric morphism]]

$$
  \mathcal{T}_{/X} \to \mathcal{T}
$$

out of the [[slice topos]] is a proper geometric morphism. And precisely if $X$ is even _decidable_ is this a tidy geometric morphism.

=--

([Moerdijk-Vermeulen, examples III 1.4](#MoerdijkVermeulen))



## References

* [[Ieke Moerdijk]], J. Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](http://igitur-archive.library.uu.nl/math/2001-0702-142944/1039.pdf)) and _Proper maps of toposes_ , American Mathematical Society (2000)
  {#MoerdijkVermeulen}

[[!redirects proper maps of toposes]]

[[!redirects proper geometric morphism]]
[[!redirects proper geometric morphisms]]

[[!redirects compact topos]]