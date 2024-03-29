
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

A [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ is called **proper** if it exhibits $\mathcal{F}$ as a [[compact topos]] over $\mathcal{E}$. (The [[stack semantics]] of $\mathcal{E}$ can be used to formalize this.)


=--

+-- {: .num_defn #StronglyCompactTopos}
###### Definition


A topos is called **strongly compact** if $\Gamma$ commutes even with all [[filtered colimits]].

A geometric morphism $f : \mathcal{F} \to \mathcal{E}$ is called **tidy** if it exhibits $\mathcal{F}$ as a strongly compact topos over $\mathcal{E}$.

=--

([MV, p. 53](#MoerdijkVermeulen))

This are the first stages of a notion that in [[(∞,1)-topos theory]] continue as follows

+-- {: .num_defn #StronglyCompactTopos}
###### Definition

Let $\kappa$ be a [[regular cardinal]] and $ -1 \leq n \leq \infty$. Then an [[(∞,1)-topos]] is _$\kappa$-compact of height $n$_ if the [[global section geometric morphism]] preserves $\kappa$-[[filtered (∞,1)-category|filtered]] [[(∞,1)-colimits]] of [[n-truncated]] objects. 

Accordingly a geometric morphism is _$\kappa$-proper of height $n$_ if it exhibits a $\kappa$-compact of height $n$ $(\infty,1)$-topos over a [[base (∞,1)-topos]].

=--

In this terminology  

* a topos _compact of height (-1)_ is the same as a _compact topos_;

* a topos _compact of height 0_ is the same as a _strongly compact topos_;

+-- {: .num_remark }
###### Remark

An [[n-coherent (∞,1)-topos]] is compact of height $n$ in the sense of def. \ref{StronglyCompactTopos}, this is ([[Rational and p-adic Homotopy Theory|Lurie XIII, prop. 2.3.9]]).

=--


## Properties

### Stability and closure properties

+-- {: .num_prop}
###### Proposition

1. Any [[equivalence of categories|equivalence]] is proper and the class of proper maps is closed under composition.


1. If in the [[diagram]] 

   $$
     \array{
       A&\xrightarrow{p}&B
       \\
       \downarrow^f&\swarrow^g
       \\
       C
    }
   $$

   $p$ is a [[surjective geometric morphism]] and $f$ is 
   proper then so is $g$.

1. If $h$ is proper and $g$ is a [[geometric embedding]] then $p$ is proper.

1. Any [[hyperconnected geometric morphism]] is proper.

1. $f:F\to G$ is proper iff its [[localic reflection]] $Sh_G(X)\to G$ is, i.e. iff $X$ is a [[compact locale|compact]] [[internal locale]] in $G$. 

1. If in a pullback square the bottom morphism is open and surjective and the left morphism is proper then so is the right.

=--

([VM, I.1, I.2](#MoerdijkVermeulen))


+-- {: .num_prop }
###### Proposition

The [[pullback]] of a proper geometric morphism is again proper.

The pullback of a tidy geometric morphism is again tidy.

=--


([VM, theorem 5.8](#MoerdijkVermeulen))

### Properness and Beck-Chevalley conditions

A [[geometric morphism]] $f$ of toposes is said to satisfy the _stable_ (weak) Beck-Chevalley condition if any pullback of $f$ satisfies the (weak) [[Beck-Chevalley condition]] ((weak)BCC).

+-- {: .num_prop}
###### Proposition

A map satisfies the stable weak BCC iff it is proper.

=--

([MV, Corollary I.5.9](#MoerdijkVermeulen))



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

Let $\mathbf{H}$ be a [[topos]] and $X \in \mathbf{H}$ an [[object]]. If

*  $X$ is a "[[compact topological space]]-object" in that:

   for every set of morphisms $\{U_i \to X\}_{i \in I}$ such that $\coprod_{i \in I} U_i \to X$ is an [[effective epimorphism]], there is a [[finite set|finite subset]] $J \subset I$ such that $\coprod_{i \in J} U_i \to X$ is still an [[effective epimorphism]];

then

*  The [[slice topos]] $\mathbf{H}_{/X}$ is a compact topos, def. \ref{CompactTopos}. 

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

Therefore it sends all subterminal object in $\mathbf{H}_{/X}$ to the [[empty set]] except the terminal object $X$ itself, which is sent to the singleton set.

So let $X$ now be a compact-topological-space-object and $U_\bullet : I \to \mathbf{H}_{/X}$ is directed system of subterminals. 

If their union $\vee_i U_i$ does not cover $X$, then $\Gamma_X(\vee_i U_i) = \emptyset$. But then also none of the $U_i$ can be $X$ itself, and hence also $\Gamma_X(U_i) = \emptyset$ for all $i \in I$ and so $\vee_i \Gamma_X(U_i) = \emptyset$. On the other hand, if $\vee_i U_i  = X$ then the $\{U_i \to X\}_{i \in I}$ form a cover, hence then by assumption there is a finite subset $\{U_i \to X\}_{i \in J}$ which still covers. By the assumption that the system $U_\bullet$ is a [[directed set]] it also contains the union $X = \vee_{i \in J} U_i$. Therefore $\vee_{i \in I} \Gamma_X(U_i) = \Gamma_X(X) = *$ is the singleton, as is $\Gamma_X(\vee_{i \in I} U_i) = \Gamma_X(X)$. So $\Gamma_X$ preserves directed unions of subterminals and hence $\mathbf{H}_{/X}$ is a compact topos.


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

### Geometric stacks
 {#GeometricStacks}

A typical condition on a  [[geometric stack]] to qualify as an [[orbifold]]/[[Deligne-Mumford stack]] is that its [[diagonal]] be proper. This is equivalent to the corresponding map of toposes being a proper geometric morphism (e.g. [Carchedi 12, section 2](#Carchedi12), [Lurie Spectral, section 3](#LurieSpectral)). 

## Related concepts

* [[separated geometric morphism]], [[Hausdorff topos]]


## References
 {#References}

The theory of proper geometric morphisms is largly due to

* [[Ieke Moerdijk]], Jacob Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](https://dspace.library.uu.nl/handle/1874/2374)) 
  {#MoerdijkVermeulen}

* [[Ieke Moerdijk]], Jacob Vermeulen, _Proper maps of toposes_ , Memoirs of the American Mathematical Society, no. 705 (2000)

based on the [[locale|localic]] case discussed in 

* Jacob Vermeulen, _Proper maps of locales_, J. Pure Applied Alg. 92 (1994)

A textbook account is in section C3.2 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_


Discussion with relation to properness of [[geometric stacks]] includes

* {#Carchedi12} [[David Carchedi]], section 2 of _&#201;tale Stacks as Prolongations_ ([arXiv:1212.2282](http://arxiv.org/abs/1212.2282))

Discussion of higher compactness conditions in [[(∞,1)-topos theory]] is in section 3 of 

* {#LurieSpectral} [[Jacob Lurie]], _Spectral Schemes_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-VII.pdf))

and in section 2.3 of 

* [[Jacob Lurie]], _[[Rational and p-adic Homotopy Theory]]_

and for the special case of [[spectral Deligne-Mumford stacks]] in section 1.4 of

* [[Jacob Lurie]], _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_

More on proper geometric morphisms between [[(infinity,1)-toposes|$(\infty,1)$-toposes]]:

* [[Louis Martini]], [[Sebastian Wolf]], _Proper morphisms of ∞-topoi_ &lbrack;[arXiv:2311.08051](https://arxiv.org/abs/2311.08051)&rbrack;.




[[!redirects proper map of toposes]]
[[!redirects proper maps of toposes]]

[[!redirects proper geometric morphisms]]

[[!redirects compact topos]]
[[!redirects strongly compact topos]]

[[!redirects compact toposes]]
[[!redirects strongly compact toposes]]

[[!redirects compact topoi]]
[[!redirects strongly compact topoi]]