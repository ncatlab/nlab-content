
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[homological algebra]], for $V_\bullet \in Ch_\bullet(\mathcal{A})$ a _[[chain complex]]_, its _chain [[homology group]]_ in degree $n$ is akin to the $n$-th [[homotopy groups]] of a topological space. It is defined to be the [[quotient]] of the $n$-[[cycles]] by the $n$-[[boundaries]] in $V_\bullet$.

[[duality|Dually]], for $V^\bullet \in Ch^\bullet(\mathcal{A})$ a [[cochain complex]], its _cochain [[cohomology group]]_ in degree $n$ is the quotient of the $n$-[[cocycles]] by the $n$-[[coboundaries]].

Basic examples are the [[singular homology]] and [[singular cohomology]] of a topological space, which are the (co)chain (co)homology of the [[singular complex]].

Chain homology and cochain cohomology constitute the basic invariants of (co)chain complexes. A [[quasi-isomorphism]] is a [[chain map]] between chain complexes that induces isomorphisms on all chain homology groups, akin to a [[weak homotopy equivalence]]. A [[category of chain complexes]] equipped with quasi-isomorphisms as [[weak equivalences]] is a presentation for the [[stable (infinity,1)-category]] of chain complexes.

## Definition

Let $\mathcal{A}$ be an [[abelian category]] such as that of $R$-[[modules]] over a [[commutative ring]] $R$. For $R = \mathbb{Z}$ the [[integers]] this is the category [[Ab]] of [[abelian groups]]. For $R = k$ a [[field]], this is the category [[Vect]] of [[vector spaces]] over $k$.

Write $Ch_\bullet(\mathcal{A})$ for the [[category of chain complexes]] in $\mathcal{A}$. Write $Ch^\bullet(\mathcal{A})$ for the [[category of cochain complexes]] in $\mathcal{A}$. 

We label [[differentials]] in a chain complex as follows:

$$
  V_\bullet
  = 
  [
   \cdots \to V_{n+1} \stackrel{\partial_n}{\to} V_n \to \cdots
  ]
$$

+-- {: .num_defn}
###### Definition

For $V_\bullet \in Ch_\bullet(\mathcal{A})$ a [[chain complex]] and $n \in \mathbb{Z}$, the **chain homology** $H_n(V)$ of $V$ in degree $n$ is the [[abelian group]]

$$
  H_n(V) \coloneqq \frac{Z_n(V)}{B_n(V)} = \frac{ker(\partial_{n-1})}{im(\partial_n)}
$$

given by the [[quotient]] ([[cokernel]]) of the group of $n$-[[cycles]] by that of $n$-[[boundaries]] in $V_\bullet$.

=--

## Properties

### Functoriality

+-- {: .num_prop}
###### Proposition

For all $n \in \mathbb{N}$ forming chain homology extends to a [[functor]]
from the [[category of chain complexes]] in $\mathcal{A}$ to $\mathcal{A}$ itself

$$
  H_n(-) : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
  \,.
$$

=--

+-- {: .proof}
###### Proof

One checks that [[chain homotopy]] (see there) respects [[cycles]] and [[boundaries]]. 

=--

+-- {: .num_prop #ChainHomologyRespectsDirectProduct}
###### Proposition

Chain homology commutes with [[direct product]] of chain complexes:

$$
  H_n(\prod_i C^{(i)})
  \simeq
  \prod_i H_n(C^{(i)})
  \,.
$$

Similarly for [[direct sum]].

=--

### Respect for direct sums and filtered colimits
 {#RespectForDirectSum}

+-- {: .num_prop }
###### Proposition

The chain homology functor preserves [[direct sums]]:

for $A,B \in Ch_\bullet$ and $n \in \mathbb{Z}$, the canonical morphism

$$
  H_n(A \oplus B) \to H_n(A) \oplus H_n(B)
$$

is an [[isomorphism]].

=--

+-- {: .num_prop }
###### Proposition

The chain homology functor preserves [[filtered colimits]]:

for $A \colon I \to Ch_\bullet$ a [[filtered category|filtered]] [[diagram]] and $n \in \mathbb{Z}$, the canonical morphism

$$
  H_n(\underset{\to_i}{\lim} A_i) \to \underset{\to_i}{\lim} H_n(A_i)
$$

is an [[isomorphism]].

=--

This is spelled out for instance as ([Hopkins-Mathew , prop. 23.1](#HopkinsMathew)).


## Examples

* For $X$ a [[topological space]] and $Sing X$ its [[singular simplicial complex]], write $N \mathbb{Z}[Sing X]$ for the [[normalized chain complex]] of the [[simplicial abelian group]] that is degreewise the [[free abelian group]] on $Sing X$. The resulting chain homology is the _[[singular homology]]_ of $X$

  $$
    H_\bullet( N \mathbb{Z}[Sing X]) \simeq H_\bullet(X, \mathbb{Z})
    \,.
  $$

* [[Koszul homology]]

* [[Ext]], [[Tor]]


## In the context of homotopy theory
 {#InTheContextOfHomotopyTheory}

We discuss here the notion of (co)homology of a [[chain complex]] from a more abstract point of view of [[homotopy theory]], using the [[nPOV]] on _[[cohomology]]_ as discussed there.

A [[chain complex]] in non-negative degree is, under the [[Dold-Kan correspondence]] a [[homological algebra]] model for a particularly nice [[topological space]] or [[∞-groupoid]]: namely one with an abelian group structure on it, a [[simplicial abelian group]].
Accordingly, an unbounded (arbitrary) [[chain complex]] is a model for a [[spectrum]] with abelian group structure. 

One consequence of this embedding

$$
  N : Ch_+ \to \infty Grpd
$$

induced by the Dold-Kan [[nerve]] is that it allows to think of [[chain complexes]] as objects in the [[(∞,1)-topos]] [[∞Grpd]] or equivalently [[Top]]. Every [[(∞,1)-topos]] comes with a notion of [[homotopy]] and [[cohomology]] and so such abstract notions get induced on chain complexes.

Of course there is an independent, age-old definition of [[homology]] of chain complexes and, by dualization, of cohomology of cochain complexes. 

This entry describes how these standard definition of chain homology and cohomology follow from the general [[(∞,1)-topos]] nonsense described at [[cohomology]] and [[homotopy]]. 

The main statement is that

* the na&#239;ve [[homology]] groups of a [[chain complex]] are really its [[homotopy groups]], in the abstract sense (i.e. with the chain complex regarded as a model for a space/$\infty$-groupoid);

* the na&#239;ve cohomology groups of a cochain complex are really the abstract [[cohomology groups]] of the dual [[chain complex]].

### Preliminaries 

Before discussing chain homology and cohomology, we fix some terms and notation.

#### Eilenberg-MacLane objects 

In a given [[(∞,1)-topos]] there is a notion of [[homotopy]] and [[cohomology]] for every (co-)coefficient object $A$ ($B$).

The particular case of [[chain complex]] [[homology]] is only the special case induced from coefficients given by the corresponding [[Eilenberg-MacLane objects]].

Assume for simplicity here and in the following that we are talking about non-negatively graded chain complexes of vector spaces over some field $k$. Then for every $n \in \mathbb{N}$ write

$$
  \begin{aligned}
    \mathbf{B}^n k &:=
    ( 
      \cdots
      \to 
      \mathbf{B}^n k_n
      \to  
      \cdots 
       \to \stackrel{\partial}{\to} \mathbf{B}^n k_1 
      \stackrel{\partial}{\to} \mathbf{B}^n k_0)
    \\
    &=
    (  \cdots \to k \to \cdots \to 0 \to 0 )
  \end{aligned}
$$

for the $n$th [[Eilenberg-MacLane object]]. 

Notice that this is often also denoted $k[n]$ or $k[-n]$ or $K(k,n)$.


#### Homotopy and cohomology 

With the [[Dold-Kan correspondence]] understood, embedding
chain complexes into [[∞-groupoids]], for any chain complexes $X_\bullet$, $A_\bullet$ and $B_\bullet$ we obtain 

* the $\infty$-groupoid

  $$
    \mathbf{H}_{\infty Grpd}(X_\bullet, A_\bullet)
  $$

  whose 
  * objects are the $A$-valued [[cocycle]]s on $X$;
  * morphisms are the coboundaries between these [[cocycle]]s;
  * 2-morphisms are the coboundaries between coboundaries
  * etc.
  and where the elements of $\pi_0 \mathbf{H}(X_\bullet,A_\bullet)$ are the cohomology classes

* the $\infty$-groupoids

  $$
    \mathbf{H}_{\infty Grpd}(B_\bullet, X_\bullet)
  $$

  whose 
  * objects are the $B$-co-valued cycles on $X$;
  * morphisms are the boundaries between these cycles;
  * 2-morphisms are the boundaries between boundaries
  * etc.
  and where the elements of $\pi_0 \mathbf{H}(B_\bullet,X_\bullet)$ are the homotopy classes


### Chain homology as homotopy 

For $X_\bullet := V_\bullet$ any [[chain complex]] 
and $H_n(V_\bullet)$ its ordinary chain [[homology]] in degree $n$, we have

$$
  H_n(V_\bullet) \simeq 
  \pi_0 \mathbf{H}(\mathbf{B}^n k_\bullet, V_\bullet)
  \,.
$$

A cycle $c : \mathbf{B}^n k_\bullet \to V_\bullet$ 
is a chain map

$$
  \array{
    \cdots 
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    k
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    \cdots
    \\
    && \downarrow
    && \downarrow^{c_n}
    && \downarrow
    \\
    \cdots 
    &\stackrel{\partial}{\to}&
    V_{n+1}
    &\stackrel{\partial}{\to}&
    V_n
    &\stackrel{\partial}{\to}&
    V_{n-1}
    &\stackrel{\partial}{\to}&
    \cdots        
  }
$$

Such chain maps are clearly in bijection with those elements $c_n \in V_n$ that are in the kernel of
$V_n \stackrel{\partial}{\to} V_{n-1}$
in that $\partial c_n = 0$.

A boundary $\lambda : c \to C'$ is a chain homotopy

$$
  \array{
    \cdots 
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    k
    &\stackrel{\partial}{\to}&
    0
    &\stackrel{\partial}{\to}&
    \cdots
    \\
    && &
    {}^{\lambda_n}\swarrow
    \\
    \cdots 
    &\stackrel{\partial}{\to}&
    V_{n+1}
    &\stackrel{\partial}{\to}&
    V_n
    &\stackrel{\partial}{\to}&
    V_{n-1}
    &\stackrel{\partial}{\to}&
    \cdots        
  }
$$

such that $c' = c + \partial \lambda$.

(...)


### Cohomology of cochain complexes 

The ordinary notion of cohomology of a [[chain complex|cochain complex]]
is the special case of cohomology in the 
[[stable (∞,1)-category|stable (∞,1)-]] [[category of chain complexes]].

For $V^\bullet$ a cochain complex let 

$$
  \begin{aligned}
      X &:= V_\bullet = (V^\bullet)^*
      \\
      &=
      (\cdots \to X_{n+1} \stackrel{\partial}{\to}
      X_n \stackrel{\partial}{\to} X_{n-1} \to \cdots)
      \\
      & :=
      (\cdots \to V_{n+1} \stackrel{\partial}{\to}
      V_n \stackrel{\partial}{\to} V_{n-1} \to \cdots)
  \end{aligned}
$$

be the corresponding dual [[chain complex]]. Let

$$
  \begin{aligned}
     A  &:=  \mathbf{B}^n I 
     \\
     &=
     (\cdots \to A_{n+1}  \to A_n \to A_{n-1} \to \cdots )
     \\
      & =
     (\cdots \to 0  \to I \to 0 \to \cdots )
  \end{aligned}
$$ 

be the [[chain complex]] with the 
tensor unit (the [[ground field]], say) in degree $n$ and
trivial elsewhere. Then 
$$
  \begin{aligned}
    \mathbf{H}(X,A)
    &=
    Ch(V_\bullet, \mathbf{B}^n I)
  \end{aligned}
$$

has 

* as objects chain morphisms 
  $c : V_\bullet \to \mathbf{B}^n I$
  $$
    \array{
      \cdots &\to& V_{n+1} &\stackrel{\partial}{\to}& 
      V_{n} 
      &\stackrel{\partial}{\to}& V_{n-1} 
      &\to& 
      \cdots
      \\
      &&  \downarrow^{c_{n+1}}
      && \downarrow^{c_{n}}
      && \downarrow^{c_{n-1}}
      \\
      \cdots &\to& 0 &\stackrel{\partial}{\to}& 
      I 
      &\stackrel{\partial}{\to}& 0 
      &\to& 
      \cdots  
    }
    \,.
  $$
  These are in canonical bijection with 
  the elements in the kernel of $d_{n}$ of the dual
  cochain complex $V^\bullet = [V_\bullet,I]$.

* as morphism chain homotopies $\lambda : c \to c'$

  $$
    \array{
      \cdots &\to& V_{n+1} &\stackrel{\partial}{\to}& 
      V_{n} 
      &\stackrel{\partial}{\to}& V_{n-1} 
      &\to& 
      \cdots
      \\
      && 
      && 
      &{}^{\lambda}\swarrow& 
      \\
      \cdots &\to& 0 &\stackrel{\partial}{\to}& 
      I 
      &\stackrel{\partial}{\to}& 0 
      &\to& 
      \cdots  
    }
    \,.
  $$

Comparing with the general definition of cocycles and coboudnaries from above, one confirms that

* the **cocycles** are the chain maps
  $$
    V_\bullet \to I[n]_\bullet
  $$

* the **coboundaries** are the chain homotopies between these chain maps.

* the **coboundaries of coboundaries** are the second order chain homotopies between these chain homotopies.

* etc.

## References 



[[!include cohomology -- early references]]


Review of basi

* [[Charles Weibel]], Section 1.1: _[[An Introduction to Homological Algebra]]_

* {#HopkinsMathew} [[Michael Hopkins]] (notes by [[Akhil Mathew]]), _algebraic topology -- Lectures_ ([pdf](http://people.fas.harvard.edu/~amathew/ATnotes.pdf))
 

[[!redirects chain homology]]
[[!redirects cochain homology]]
[[!redirects chain cohomology]]
[[!redirects cochain cohomology]]


[[!redirects chain homology group]]
[[!redirects chain homology groups]]
