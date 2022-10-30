
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

The notion of _compact topos_ is the generalization from [[topology]] to [[topos theory]] of the notion of _[[compact topological space]]_.

More generally, over a general [[base topos]], the notion of _proper geometric morphism_ is the generalization to morphisms between toposes of the notion of _[[proper map]]_ between [[topological spaces]].

## Definition
 {#Definition}

+-- {: .num_defn #CompactTopos}
###### Definition

A [[sheaf topos]] $\mathcal{E}$ is called a **[[compact topos]]** if the [[direct image]] of the [[global section geometric morphism]] $\Gamma : \mathcal{E} \to Set$ preserves [[directed colimit|directed]] [[joins]] of [[subterminal objects]].

A [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ is called **proper** if it exhibits $\mathcal{F}$ as a [[compact topos]] over $\mathcal{E}$.


=--

+-- {: .num_defn #StronglyCompactTopos}
###### Definition


A topos is called **strongly compact** if $\Gamma$ commutes even with all [[filtered colimits]].

A geometric morpjhism $f : \mathcal{F} \to \mathcal{E}$ is called **tidy** if it exhibits $\mathcal{F}$ as a strongly compact topos over $\mathcal{E}$.

=--

([MV, p. 53](#MoerdijkVermeulen))

This are the first stages of a notion that in [[(∞,1)-topos theory]] continue as follows

+-- {: .num_defn #StronglyCompactTopos}
###### Definition

Let $\kappa$ be a [[regular cardinal]] and $ -1 \leq n \leq \infty$. Then an [[(∞,1)-topos]] is _$\kappa$-compact of height $n$_ if the [[global section geometric morphism]] preserves $\kappa$-[[filtered (∞,1)-category|filtered]] [[(∞,1)-colimits]] of [[n-truncated]] objects. 

Accordingly a geometric morphism is _$\kappa$-proper of height $n$_ if it exhibits $\kappa$-compact of height $n$ $(\infty,1)$-topos over a [[base (∞,1)-topos]].

=--

In this terminology  

* a topos _compact of height (-1)_ is the same as a _compact topos_;

* a topos _compact of height 0_ is the same as a _strongly compact topos_;



## Properties

### Stability and closure properties

+-- {: .num_prop }
###### Proposition

The [[pullback]] of a proper geometric morphism is again proper.

The pullback of a tidy geometric morphism is again tidy.

=--

([VM, theorem 5.8](#MoerdijkVermeulen))


### Compact sites
 {#CompactSites}

We discuss classes of [[sites]] such that their [[sheaf topos]] is a compact topos, def. \ref{CompactTopos} ([VM, I.5](#MoerdijkVermeulen)).

(...)

### Strongly compact sites
 {#StronglyCompactSites}

We discuss classes of [[sites]] such that their [[sheaf topos]] is a strongly compact topos, def. \ref{CompactTopos} ([VM, III.4](#MoerdijkVermeulen)).

(...)

## Examples

### Compact toposes

+-- {: .num_prop}
###### Proposition

Let $\mathbf{H}$ be a [[topos]] and $X \in \mathbf{H}$ an [[object]]. Then the following are equivalent

1. $X$ is a "[[compact topological space]]-object" in that:

   for every set of morphisms $\{U_i \to X\}_{i \in I}$ such that $\coprod_{i \in I} U_i \to X$ is an epimorphism, there is a [[finite set|finite subset]] $J \subset I$ such that $\coprod_{i \in J} U_i \to X$ is still an epimorphism;

1. The [[slice topos]] $\mathbf{H}_{/X}$ is a compact topos, def. \ref{CompactTopos}. 

=--

+-- {: .num_remark}
###### Remark

Beware that $X$ being a "compact topological space-object" is different from it being a [[compact object]] (the difference being that between compactness of height (-1) and height 0). For the latter case see prop. \ref{SliceOverCompactIsStronglyCompact} below.

=--

+-- {: .proof}
###### Proof

The [[terminal object]] of $\mathbf{H}_{/X}$ is the [[identity]] $id_X : X \to X$ in $\mathbf{H}$. A [[subterminal object]] of $\mathbf{H}_{/X}$ is a [[monomorphism]] $U \hookrightarrow X$ in $\mathbf{H}$.

The [[global section geometric morphism]] $\Gamma_X : \mathbf{H}_{/X} \to Set$ sends an object $[E \to X]$ to its set of [[sections]]

$$
  \Gamma_X([E \to X]) = \mathbf{H}(X, E) \times_{\mathbf{H}(X,X)} \{id_X\}
  \,.
$$

Therefore (...)
=--

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

Let $\mathbf{H}$ be a topos over [[Set]] and $X \in \mathbf{H}$ an object. Then the following are equivalent

1. $X$ is a [[compact object]] (in the sense that the [[hom functor]] $\mathbf{H}(X,-)$ preserves [[filtered colimits]]) 

1. the [[slice topos]] $\mathbf{H}_{/X}$ is strongly compact, def. \ref{StronglyCompactTopos}.

=--

+-- {: .proof}
###### Proof

The [[direct image]] $\Gamma_X$ of the [[global section geometric morphism]] 

$$
  ((-) \times X \dashv  \Gamma_X) : \mathbf{H}_{/X} 
    \stackrel{\overset{(-) \times X}{\leftarrow}}{\underset{\mathbf{\Gamma}_X}{\to}} 
  \mathbf{H}
   \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\mathbf{H}(*,-)}{\to}}
  Set 
$$ 

is given by the [[hom functor]] out of the [[terminal object]]. The terminal object in $\mathbf{H}_{/X}$ is the [[identity]] [[morphism]] $id_X : X \to X$. So the terminal geometric morphism  takes any $[E \to X]$ in $\mathbf{H}_{/X}$ to the set of [[sections]], given by the [[pullback]] of the [[hom set]] along the inclusion of the [[identity]]

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

Conversely, assume that $\Gamma_X(-)$ commutes over all filtered colimits. For every ([[filtered category|filtered]]) [[diagram]] $F_\bullet : I \to \mathbf{H}$ there is the corresponding filtered diagram $X \times F_\bullet : I \to \mathbf{H}_{/X}$, where $[X \times F_i \to X]$ is the projection. As before, the product with $X$ preserves forming colimits 

$$
  \underset{\longrightarrow_i}{\lim} ([X \times F_i \to X])
  \simeq
  [X \times  (\underset{\longrightarrow_i}{\lim} F_i) \to X]
  \,.
$$

Moreover, sections of a trivial [[bundle]] are maps into the fiber

$$
  \Gamma_X([X \times F_i \to X]) \simeq \mathbf{H}(X,F_i)
  \,.
$$

So it follows that $X$ is a compact object:

$$
  \begin{aligned}
    \mathbf{H}(X, \underset{\longrightarrow_i}{\lim} F_i)
    & 
   \simeq 
   \Gamma_X( [X \times (\underset{\longrightarrow_i}{\lim} F_i) \to X])
    \\
    & \simeq 
   \Gamma_X(\underset{\longrightarrow_i}{\lim} [X \times  F_i \to X])
   \\
   & \simeq
   \underset{\longrightarrow_i}{\lim}
   \Gamma_X( [X \times  F_i \to X])   
   \\
   & \simeq
   \underset{\longrightarrow_i}{\lim}
   \mathbf{H}(X,F_i)     
  \end{aligned}
  \,.
$$

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

## Related concepts

* [[separated geometric morphism]], [[Hausdorff topos]]


## References

* [[Ieke Moerdijk]], Jacob Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](http://igitur-archive.library.uu.nl/math/2001-0702-142944/1039.pdf)) and _Proper maps of toposes_ , American Mathematical Society (2000)
  {#MoerdijkVermeulen}

[[!redirects proper map of toposes]]
[[!redirects proper maps of toposes]]

[[!redirects proper geometric morphisms]]

[[!redirects compact topos]]
[[!redirects strongly compact topos]]

[[!redirects compact toposes]]
[[!redirects strongly compact toposes]]

[[!redirects compact topoi]]
[[!redirects strongly compact topoi]]
