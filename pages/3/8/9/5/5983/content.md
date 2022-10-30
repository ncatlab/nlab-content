
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _differential function complex_ ([HopkinsSinger](#HopkinsSinger)) is a [[Kan complex]] of [[cocycle]] s for _generalized_ [[differential cohomology]], hence for differential refinements of [[generalized (Eilenberg-Steenrod) cohomology]] theories:

roughly, given a [[spectrum]] $E$ [[Brown representability|representing]] a given [[cohomology theory]], its _differential function complex_ over any given [[smooth manifold]] $U$ is the [[simplicial set]] whose $k$-[[simplices]] are triples consisting of

* a [[continuous function]] $f : U \times \Delta^k \to E_{n}$;

* a smooth [[differential form]] $\omega$ on $U \times \Delta^k$ whose corresponding real cohomology class (under the [[de Rham theorem]]) is that of the pullback of the real cohomology classes of $E$ along $f$;

* an explict [[coboundary]] in real cohomology exhibiting this fact.

(More precisely, in order for this construction to yield not just a single [[simplicial set]] (which will be a [[Kan complex]]) but a suitable [[spectrum]] object, there are conditons on the dependency of $\omega$ on the [[tangent vector]]s to the [[simplex]].)

When applied to the [[Eilenberg-MacLane spectrum]] $K\mathbb{Z}$ this construction reproduces, on cohomology classes, [[ordinary differential cohomology]]. Applied to the [[classifying space]] $B U$ of [[topological K-theory]] it gives [[differential K-theory]]. 


## Definitions

### Cocycles with values in graded vector spaces

For the present purposes it will be convenient to collect [[cocycle]]s of various degrees together to a single cocycle. For that purpose we make the following simple definition.

+-- {: .num_defn }
###### Definition

For $V = V^\bullet$ a [[graded vector space]] over the [[real number]]s set

* for $E$ a [[topological space]]:

  $$
    C^\bullet(E, V)^n := \oplus_{i + j = n} C^i(E, V^j)
  $$

* and so on

=--

(...)


### Differential functions


+-- {: .num_defn #DifferentialFunctions}
###### Definition

For 

* $E$ a [[topological space]];

* $\iota \in Z^n(E,\mathbb{R})$ a [[cocycle]] on $E$ for real-valued [[singular cohomology]] on $E$,

a **differential function** on a smooth [[manifold]] $U$ with values in $(E,\iota)$ is a triple $(c,h,\omega)$ with

* $c : U \to E$ a continuous map;

* $\omega \in \Omega^n(S)$ a smooth [[differential form]] on $S$;

* $h \in C^{n-1}(U,\mathbb{R})$ a cochain in real cohomology on (the topological space underlying) $U$;

such that in the [[abelian group]] $Z^n(S,\mathbb{R})$ of singular cochains the equation

$$
  \omega = c^*\iota + \delta h
$$

holds, where 

* $\omega$ is here regarded  as a singular cochain (that sends a chain to the integral of $\omega$ over it, as discussed at [[de Rham theorem]]), 

* $\delta$ denotes the coboundary operator,(the [[Moore complex]] differential of the [[singular simplicial complex]]).

=--

This is ([HopkinsSinger, def.4.1](#HopkinsSinger)).

In words this is: a continuous map to the topological space together with a _smooth_ refinement of the pullback of the chosen singular cochain.

### Differential function complexes

+-- {: .num_defn #DifferentialFunctionComplex}
###### Definition

For 

* $E$ be a [[topological space]] and 

* $\iota \in Z^n(E,\mathbb{R})$ a [[cocycle]] on $E$ for real-valued [[singular cohomology]] on $X$,

* $U$ a [[smooth manifold]],

the **differential function complex** 

$$
  (E,\iota)^U
$$ 

of all differential functions $S \to (X,\iota)$ is the [[simplicial set]] whose $k$-[[simplices]] are differential functions, def, \ref{DifferentialFunctions}

$$
  U \times \Delta^k_{Top} \to (E,\iota)
  \,.
$$

=--


For applications one needs certain sub-complex of this, filtered by the number of legs that $\omega$ has along the 
simplices.

+-- {: .num_defn }
###### Definition

For $s \in \mathbb{N}$ write

* $filt_s \Omega^\bullet(U \times \Delta^k)$

  for the sub-simplicial set of differential forms that vanish when evaluated on more than $s$ [[vector field]]s tangent to the [[simplex]];

* $filt_s (X,\iota)^S \subset (X,\iota)^S$

  for the sub-simplicial set of those differential functions whose differential form component is in $filt_s \Omega^\bullet(U \times \Delta^k)$.


=--

This is ([HopkinsSinger, def. 4.5](#HopkinsSinger)).

+-- {: .num_prop }
###### Proposition

The complex $filt_s (E,\iota)^U$ is (up to [[weak homotopy equivalence|equivalence]], of course) the [[homotopy pullback]]

$$
  \array{
    filt_s (E,\iota)^U &\to& 
      filt_s \Omega^n_{cl}(U \times \Delta^\bullet, \mathcal{V})
    \\
    \downarrow && \downarrow
    \\
    Sing E^U &\to& Z^\bullet(U \times \Delta^\bullet, \mathcal{V})
  }
$$

in [[sSet]] (regarded as equipped with its standard [[model structure on simplicial sets]]).

=--

Here $E^U$ is the [[internal hom]] in [[Top]] and $Sing(-)$ denotes the [[singular simplicial complex]].

The following proposition gives the [[simplicial homotopy groups]] of these differential function complexes in dependence of the parameter $s$.

+-- {: .num_prop #HomotopyGroupsOfDiffFunctionComplex}
###### Proposition

We have generally

$$
  \pi_k Z(S \times \Delta^\bullet_{Diff}, \mathcal{V}) = 
   H^{n-m}(S; \mathcal{V})
$$

(for instance by the [[Dold-Kan correspondence]]).

The [[simplicial homotopy group]]s of $filt_s \Omega^n_{cl}(S \times \Delta^\bullet_{Diff})$ are 

$$
  \pi_k filt_s \Omega^n_{cl}(S \times \Delta^\bullet_{Diff})
  =
  \left\{
    \array{
       H_{dR}^{n-k}(S, \mathcal{V}) & | k \lt s
       \\
       \Omega_{cl}(S; \mathcal{V})^{n-s} & | k = s
       \\
       0 & | k \gt s
    }
  \right\}
  \,.
$$

This implies [[isomorphism]]s

$$
  \pi_k filt_s(X; \iota)^S 
   \stackrel{\simeq}{\to}
  \left\{
    \array{
       \pi_k X^S & | k \lt s
       \\
       H^{n-k-1}(S; \mathcal{V})/ \pi_{k+1} X^S
       |
       k \gt s
    }
  \right.
  \,.
$$

=--

This appears as [HopkinsSinger, p. 36 and corollary D15](#HopkinsSinger).


### Differential $E$-cohomology

Let $E_\bullet$ be an [[Omega-spectrum]]. Let $\iota_\bullet$ be the canonical [[Chern character]] class (...).

+-- {: .num_prop}
###### Proposition/Definition

For $S$ a [[smooth manifold]], and $s \in \mathbb{N}$, the sequence of differential function complexes, def. \ref{DifferentialFunctionComplex},

$$
  filt_{s + n}(E_n; \iota_n)^S
   \stackrel{\simeq}{\to}
  \Omega  filt_{s + (n + 1)}(E_{n+1}; \iota_{n+1})^S
$$

forms an [[Omega-spectrum]].

This is the **differential function spectrum** for $E$, $S$, $s$.

=--

This is ([HopkinsSinger, section 4.6]).

+-- {: .num_defn}
###### Definition

The **differential $E$-cohomology group** of the smooth manifold $S$ in degree $n$ is

$$
  H_{diff}^n(S,E) :=
  \pi_0
  filt_0(E_n \iota_n)^S
$$

=--

This is ([HopkinsSinger, def. 4.34](#HopkinsSinger)).


## Properties

### Relation to differential cohomology in cohesive $(\infty,1)$-toposes

The following is a simple corollary or slight rephrasing of some of the above constructions, which may serve to show how differential function complexes present differential cohomology in the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoid]]s.

+-- {: .num_prop}
###### Proposition

For $E_\bullet$ a spectrum as above,  
we have an [[(∞,1)-pullback]] square

$$
  \array{  
    filt_0 (E_n; \iota_n)^{(-)} &\to& \prod_i \Omega^{n_i}_{cl}(-)
    \\
    \downarrow && \downarrow
    \\
    Disc E_n
    & 
     \stackrel{}{\to}
    &
    \prod_i \mathbf{B}^{n_i} \mathbb{R}_{disc}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{HomotopyGroupsOfDiffFunctionComplex} we have that

* $filt_\infty (E; \iota_n)^S \simeq Sing X^S$;

* $filt_0 \Omega_{cl}(S \times \Delta^\bullet) \simeq \Omega_{cl}(S)$.

The statement then follows with the [[pasting law]] for [[homotopy pullback]]s

$$
  \array{
     filt_0 (E_n; \iota_n)^S &\to&  \Omega^n_{cl}(S; \mathcal{V})
     \\
     \downarrow && \downarrow     
     \\  
     filt_\infty (E_n; \iota_n)^S &\to&  filt_\infty \Omega_{cl}(S \times \Delta^\bullet; \mathcal{V})
     \\
     \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
     \\
     Sing X^S &\to& Z(S \times \Delta^\bullet; \mathcal{V})
  }
  \,.
$$

(...)

=--


## Examples

### Line bundles with connection


Let $X = \mathcal{B} U(1) \simeq K(\mathbb{Z},2)$ be the [[Eilenberg-MacLane space]] that is the [[classifying space]] for $U(1)$-[[principal bundle]]s. It carries the canonical [[cocycle]] $\iota := Id : \mathcal{B}U(1) \to \mathcal{B}U(1) \simeq K(\mathbb{Z},2)$ representing in $H^2(X,\mathbb{Z})$ the class of the universal complex [[line bundle]] $L \to X$ on $X$.

Accordingly, for $c : S\to \mathcal{B}U(1)$ a continuous map, we have the corresponding line bundle $c^* L$ on $S$. 

One checks (...details...Example 2.7 in HopSin) that a refinement of $c$ to a differential function $(c,\omega,h)$ corresponds to equipping $c^* L$ with a [[connection on a bundle|smooth connection]].

Now consider $((c,\omega,h) \to (c',\omega', h')) \in filt_0  (\mathcal{B}U(1),Id)^S$ a morphism between two such $(\mathcal{B}U(1),Id)$-differential functions. By definition this is now a $U(1)$-principal bundle $\hat L$ with connection on $S \times \Delta^i_{Diff}$, whose curvature form $\hat \omega \in \Omega^2(S \times \Delta^1_{Diff})$ is of the form $g \cdot \tilde \omega$, where $\tilde \omega$ is a 2-form on $S$ and $g$ is a smooth function on $\Delta^1_{Diff}$, both pulled back to $S \times \Delta^1_{Diff}$ and multiplied there.

But since $\hat \omega$ is necessarily _closed_ it follows with $d (g \wedge \tilde \omega) = d t \frac{\partial g}{\partial t} \wedge \tilde \omega + g \wedge d_{S} \tilde \omega$ that $g$ is actually constant. 

This means that that the parallel transoport of the connection $\hat \nabla$ on $S \times \Delta^1_{Diff}$ induces a insomorphism between the two line bundles on $S$ over the endpoints of $S \times \Delta^1_{Diff}$ that respects the connections. 

...

### Differential K-cocycles

(...)

## References

Differential function complexes were introduced and studied in

* [[Mike Hopkins]], I. Singer, _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
 {#HopkinsSinger}

For further references see [[differential cohomology]].

[[!redirects differential function complexes]]
