
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _singular homology_ of a [[topological space]] $X$ is the [[simplicial homology]] of its [[singular simplicial complex]]:

a **singular $n$-[[chain]]** on $X$ is a [[formal linear combination]] of [[singular simplices]] $\sigma : \Delta^n \to X$, and a singular $n$-[[cycle]] is such a chain such that its oriented [[boundary]] in $X$ vanishes. Two singular chains are **homologous** if they differ by a boundary. The **singular homology** of $X$ in degree $n$ is the group of $n$-cycles modulo those that are boundaries.

Singular homology of a topological space conincide with its [[ordinary homology]] as defined more abstractly (see at [[generalized homology theory]]).

(Here "singular" refers to the contrast with [[cellular homology]], referring to the fact that a [[simplex]] $\Delta_{top} \to X$ in the [[singular simplicial complex]] is not required to be a [[topological embedding]], but may be a "singular map", such as for instance a [[constant function]].)

## Definition
 {#Definition}


Let $X \in $ [[Top]] be [[topological space]]. 
Write $Sing X \in $ [[sSet]] for its [[singular simplicial complex]]. 

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$, a **singular $n$-chain** on $X$ is
an element in the [[free abelian group]] $\mathbb{Z}[(Sing X)_n]$:

a [[formal linear combinations]] of [[singular simplices]] in $X$.

=--

+-- {: .num_remark }
###### Remark

These are the [[chains on a simplicial set]] on $Sing X$.

=--

The groups of singular chains combine to the [[simplicial abelian group]]
$\mathbb{Z}[Sing X] \in Ab^{\Delta^{op}}$. 

+-- {: .num_defn #SingularComplex}
###### Definition

The [[alternating face map complex]] 

$$
  C_\bullet(X)
    \coloneqq 
  C_\bullet(\mathbb{Z}[Sing X]) \in Ch_\bullet
$$ 

is the **singular complex** of $X$. 

Its [[chain homology]] is the ordinary **singular homology** of $X$.

=--

One usually writes $H_n(X, \mathbb{Z})$ or just $H_n(X)$ for the singular homology of $X$ in degree $n$. See also at _[[ordinary homology]]_.

+-- {: .num_remark }
###### Remark

So we have

$$
  C_\bullet(X)
  = 
  [
    \cdots
     \stackrel{\partial_2}{\to}
    \mathbb{Z}[(Sing X)_2]
     \stackrel{\partial_1}{\to}
    \mathbb{Z}[(Sing X)_1]
     \stackrel{\partial_0}{\to}
    \mathbb{Z}[(Sing X)_0]
  ]
$$

where the differentials are defined on [[basis]] elements 
$\sigma \in (Sing X)_n$ by

$$
  \partial_n \sigma 
    = 
  -
  \sum_{i = 0}^n
    (-1)
    d_i \sigma 
$$

(with $d_i$ the $i$ [[simplicial set|simplicial face map]]) and then extended linearly. 

(One may change the global signs and obtain a [[quasi-isomorphism|quasi-isomorphic]] complex, in particular with the same homology groups.)

=--

+-- {: .num_remark }
###### Remark

This means that a [[singular chain]] is a [[cycle]] if the formal linear combination of the oriented [[boundaries]] of all its constituent [[singular simplices]] sums to 0. See the  _[basic examples](#BasicExamples)_ below

=--

More generally, for $R$ any unital [[ring]] one can form the degreewise [[free module]] $R[Sing X]$ over $R$. The corresponding homology is the _singular homology with coefficients in $R$, denoted $H_n(X,R)$.

+-- {: .num_defn }
###### Definition

Given a [[continuous map]] $f : X \to Y$ between topological spaces, 
and given $n \in \mathbb{N}$, every singular $n$-simplex $\sigma : \Delta^n \to X$ in $X$ is sent to a singular $n$-simplex 

$$
  f_* \sigma : \Delta^n \stackrel{\sigma}{\to} X \stackrel{f}{\to} Y
$$

in $Y$. This is called the **push-forward** of $\sigma$ along $f$. Accordingly there is a push-forward map on groups of singular chains

$$
  (f_*)_n : C_n(X) \to C_n(Y)
  \,. 
$$

=--

+-- {: .num_prop #PushForwardChainMap}
###### Proposition

These push-forward maps make all diagrams of the form

$$
  \array{
     C_{n+1}(X) &\stackrel{(f_*)_{n+1}}{\to}& C_{n+1}(Y)
     \\
     \downarrow^{\mathrlap{\partial^X_n}} && \downarrow^{\mathrlap{\partial^Y_n}}
     \\
     C_n(X) &\stackrel{(f_*)_n}{\to}& C_n(Y)
  }
$$

commute. In other words, push-forward along $f$ constitutes a [[chain map]]

$$
  f_* : C_\bullet(X) \to C_\bullet(Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is in fact evident that push-forward yields a functor of [[singular simplicial complexes]]

$$
 f_* : Sing X \to Sing Y
 \,.
$$

From this the statement follows since $\mathbb{Z}[-] : sSet \to sAb$ is a functor.

=--

Accordingly we have:

+-- {: .num_prop #SingularHomologyAsAFunctor}
###### Proposition

Sending a topological space to its singular chain complex $C_\bullet(X)$, def. \ref{SingularComplex}, and a continuous map to its push-forward chain map, 
prop. \ref{PushForwardChainMap}, constitutes a [[functor]]

$$
  C_\bullet(-,R) : Top \to Ch_\bullet(R Mod)
$$

from the category [[Top]] to the [[category of chain complexes]].

In particular for each $n \in \mathbb{N}$ singular homology extends to a [[functor]]

$$
  H_n(-,R) : Top \to R Mod
  \,.
$$

=--

## Examples
 
### Basic examples
 {#BasicExamples}



+-- {: .num_example }
###### Example

Let $X$ be a topological space. Let $\sigma^1 : \Delta^1 \to X$
be a singular 1-simplex, regarded as a 1-chain

$$
  \sigma^1 \in C_1(X)
  \,.
$$

Then its [[boundary]] $\partial \sigma \in H_0(X)$ is 

$$
  \partial \sigma^1 = \sigma(0)  -\sigma(1)
$$

or graphically (using notation as for [[orientals]])

$$
  \partial 
  \left(
    \sigma(0) \stackrel{\sigma}{\to} \sigma(1)
  \right)
  = 
  (\sigma(0)) - (\sigma(1))
  \,.
$$

Let $\sigma^2 : \Delta^2 \to X$ be a singular 2-chain. The boundary is

$$
  \partial
  \left(
    \array{
       && \sigma(1)
       \\
       & {}^{\mathllap{\sigma(0,1)}}\nearrow 
       & \Downarrow^{\mathrlap{\sigma}}& 
       \searrow^{\mathrlap{\sigma^{1,2}}}
       \\
       \sigma(0) &&\underset{\sigma(0,2)}{\to}&& \sigma(2)
    }
  \right)
  = 
  \left(
    \array{
       && \sigma(1)
       \\
       & {}^{\mathllap{\sigma(0,1)}}\nearrow 
       & & 
       \\
       \sigma(0) 
    }
  \right)
  -
  \left(
    \array{
       && 
       \\
       &       
       & & 
       \\
       \sigma(0) &\underset{\sigma(0,2)}{\to}& \sigma(2)
    }
  \right)
  +
  \left(
    \array{
       && \sigma(1)
       \\
       & 
       & & 
       \searrow^{\mathrlap{\sigma^{1,2}}}
       \\
       && && \sigma(2)
    }
  \right)
  \,.
$$

Hence the boundary of the boundary is

$$
  \begin{aligned}
  \partial \partial \sigma
  &= 
  \partial
  \left(
  \left(
    \array{
       && \sigma(1)
       \\
       & {}^{\mathllap{\sigma(0,1)}}\nearrow 
       & & 
       \\
       \sigma(0) 
    }
  \right)
  -
  \left(
    \array{
       && 
       \\
       &       
       & & 
       \\
       \sigma(0) &\underset{\sigma(0,2)}{\to}& \sigma(2)
    }
  \right)
  +
  \left(
    \array{
       && \sigma(1)
       \\
       & 
       & & 
       \searrow^{\mathrlap{\sigma^{1,2}}}
       \\
       && && \sigma(2)
    }
  \right)  \right)
  \\
  & = 
  \left(
    \array{
       && 
       \\
       &  
       & & 
       \\
       \sigma(0) 
    }
  \right)
  -
  \left(
    \array{
       && \sigma(1)
       \\
       &  
       & & 
       \\
       
    }
  \right)
  -
  \left(
    \array{
       && 
       \\
       &       
       & & 
       \\
       \sigma(0) && 
    }
  \right)
  +
  \left(
    \array{
       && 
       \\
       &       
       & & 
       \\
       && \sigma(2)
    }
  \right)
  +
  \left(
    \array{
       && \sigma(1)
       \\
       & 
       & & 
       \\
       && && 
    }
  \right)
  -
  \left(
    \array{
       && 
       \\
       & 
       & & 
       \\
       && && \sigma(2)
    }
  \right)
  \\
  & = 0
  \end{aligned}
$$

=--

For more illustrations see for instance ([Ghrist, (4.5)](#Ghrist)).

### Homology of cells: disks and spheres
 {#HomologyOfDisksAndSpheres}

+-- {: .num_prop }
###### Proposition

For all $n \in \mathbb{N}$ the [[reduced singular homology]] of the $n$-[[sphere]] $S^n$ is

$$
  \tilde H_k(S^n)
  = 
  \left\{
    \array{
      \mathbb{Z} & if\; k = n  
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

=--

+-- {: .proof}
###### Proof

The $n$-sphere may be realized as the [[pushout]] 

$$
  S^n \simeq D^n/S^{n-1} \coloneqq D^{n} \coprod_{S^{n-1}} *
$$

which is the $n$-[[ball]] with its [[boundary]] $(n-1)$-sphere identified with the [[point]]. The inclusion $S^{n-1} \hookrightarrow D^n$ is a "good pair" in the sense of def. \ref{GoodPair}, and so the [[long exact sequence]] from prop. \ref{RelativeHomologyLongExactSequence} yields a long exact sequence

$$
  \cdots \to \tilde H_{k+1}(S^n) \to \tilde H_k(S^{n-1}) \to \tilde H_k(D^n) \to \tilde H_k(S^n) \to \tilde H_{k-1}(S^{n-1}) \to \cdots
  \,.
$$

Since the [[disks]] are all [[contractible topological spaces]] we have $H_k(D^n) \simeq 0$ for all $k,n$ by [this example](reduced+homology#ReducedHomologyOfPoints) at _[[reduced homology]]_. This means that in the above long exact sequence all the morphisms

$$
  \tilde H_{k+1}(S^{n+1}) \to \tilde H_k(S^n)
$$

are [[isomorphisms]], for all $k \in \mathbb{N}$. Since 

$$
  \tilde H_n(S^0) \simeq 
  \left\{
    \array{
       \mathbb{Z} & if \; n = 0
       \\
       0 & otherwise
    }
  \right.
$$ 

(by [this example](reduced+homology#ReducedHomologyOf0Sphere) at _[[reduced homology]]_) the statement follows by [[induction]] on $n$.

=--

## Properties

### Homotopy invariance
 {#HomotopyInvariant}

Singular homology is _homotopy invariant_:

+-- {: .num_prop }
###### Proposition

If $f : X \to Y$ is a [[continuous map]] between [[topological spaces]] which is a [[homotopy equivalence]], then the induced morphism on singular homology groups

$$
  H_n(f) : H_n(X) \to H_n(Y)
$$

is an [[isomorphism]].

In other words: the singular chain functor of prop. \ref{SingularHomologyAsAFunctor}
sends [[weak homotopy equivalences]] to [[quasi-isomorphisms]].

=--

A proof (via [[CW approximations]]) is spelled out for instance in ([Hatcher, prop. 4.21](#Hatcher)).


### Relation to homotopy groups
 {#RelationToHomotopyGroups}

The singular [[homology groups]] of a topologial space serve to some extent as an approximation to the [[homotopy groups]] of that space.

+-- {: .num_defn #HurewiczHomomorphism}
###### Definition 
**(Hurewicz homomorphism)**

For $(X,x)$ a [[pointed object|pointed]] [[topological space]], the **Hurewicz homomorphism** is the [[function]]

$$
  \Phi : \pi_k(X,x) \to H_k(X)
$$

from the $k$th [[homotopy group]] of $(X,x)$ to the $k$th [[singular homology]] group defined by sending

$$
  \Phi : (f : S^k \to X)_{\sim} \mapsto f_*[S_k]
$$

a representative singular $k$-sphere $f$ in $X$ to the push-forward along $f$ of the [[fundamental class]] $[S_k] \in H_k(S^k) \simeq \mathbb{Z}$.


=--

+-- {: .num_prop }
###### Proposition

For $X$ a topological space the Hurewicz homomorphism in degree 0 exhibits an [[isomorphism]] between the [[free abelian group]] $\mathbb{Z}[\pi_0(X)]$ on the set of [[connected components]] of $X$ and the degree-0 singular homlogy:

$$
  \mathbb{Z}[\pi_0(X)]
   \simeq
  H_0(X)
  \,.
$$

=--


Since a [[homotopy group]] in positive degree depends on the [[homotopy type]] of the [[connected component]] of the base point, while the singular homology does not depend on a basepoint, it is interesting to compare these groups only for the case that $X$ is connected.

+-- {: .num_prop }
###### Proposition

For $X$ a [[connected topological space]] the [[Hurewicz homomorphism]]
in degree 1

$$
  \Phi : \pi_1(X,x) \to H_1(X)
$$

is [[surjection|surjective]]. Its [[kernel]] is the [[commutator subgroup]]
of $\pi_1(X,x)$. Therefore it induces an [[isomorphism]] from the [[abelianization]] $\pi_1(X,x)^{ab} \coloneqq \pi_1(X,x)/[\pi_1,\pi_1]$:


$$
  \pi_1(X,x)^{ab}
  \stackrel{\simeq}{\to}
  H_1(X)
  \,.
$$

=--

For higher connected $X$ we have the 

+-- {: .num_theorem}
###### Theorem

If $X$ is [[n-connected object in an (infinity,1)-topos|(n-1)-connected]] for $n \geq 2$ then

$$
  \Phi : \pi_n(X,x) \to H_n(X)
$$

is an [[isomorphism]].

=--

This is known as the _[[Hurewicz theorem]]_.

### Relation to relative homology
 {#RelationToRelativeHomology}

For the present purpose one makes the following definition.

+-- {: .num_defn #GoodPair}
###### Definition

A [[topological subspace]] inclusion $A \hookrightarrow X$ in [[Top]] is called a **good pair** if 

1. $A$ is [[inhabited set|inhabited]] and [[closed subset|closed]] in $X$;

1. $A$ has a [[neighbourhood]] in $X$ of which it is a [[deformation retract]].

=--

Write $X/A$ for the [[cokernel]] of the inclusion, hence for the [[pushout]]

$$
  \array{
    A &\hookrightarrow& X
    \\
    \downarrow && \downarrow
    \\
    * &\to& X/A
  }
$$

in [[Top]].

+-- {: .num_prop #RelativeHomologyLongExactSequence}
###### Proposition

If $A \hookrightarrow X$ is a good pair, def. \ref{GoodPair}, then the singular homology of $X/A$ coincides with the [[relative homology]] of $X$ relative to $A$.  In particular, therefore, it fits into a [[long exact sequence]] of the form

$$
  \cdots
  \to
  \tilde H_n(A)
  \to
  \tilde H_n(X)
  \to 
  \tilde H_n(X/A)
  \to 
  \tilde H_{n-1}(A)
  \to 
  \tilde H_{n-1}(X)
  \to 
  \tilde H_{n-1}(X/A)
  \to 
  \cdots
  \,.
$$

=--

For instance ([Hatcher, theorem 2.13](#Hatcher)).


### Relation to generalized homology

Singular homology computes the [[generalized homology]] with coefficients in the [[Eilenberg-MacLane spectrum]] $H \mathbb{Z}$ or $H R$.

## Related concepts

* The [[duality|dual]] notion is that of _[[singular cohomology]]_.

* The analogous notion in [[algebraic geometry]] is given by [[Chow groups]].

* [[Kan-Thurston theorem]]

* [[Borel-Moore homology]]

## References

### General

Original references on [[chain homology]]/[[cochain cohomology]] and [[singular homology]]/[[singular cohomology]]:

* [[Andrei Kolmogoroff]], _Über die Dualität im Aufbau der kombinatorischen Topologie_, Recueil Mathématique 1(43) (1936), 97–102.  ([mathnet](http://mi.mathnet.ru/msb5361))

* [[Andrei Kolmogoroff]], _Homologiering des Komplexes und des lokal-bicompakten Raumes_, Recueil Mathématique 1(43) (1936), 701–705.  [mathnet](http://mi.mathnet.ru/msb5475).

* [[J. W. Alexander]], _On the chains of a complex and their duals_, Proc. Nat. Acad. Sei. USA, 21(1935), 509–511 ([doi:10.1073/pnas.21.8.50](https://doi.org/10.1073/pnas.21.8.509))

* [[J. W. Alexander]], _On the ring of a compact metric space_, Proc. Nat. Acad. Sci. USA, 21(1935), 511–512 ([doi:10.1073/pnas.21.8.511](https://doi.org/10.1073/pnas.21.8.511))

* [[J. W. Alexander]], _On the connectivity ring of an abstract space_, Ann. of Math., 37 (1936), 698–708 ([doi:10.2307/1968484](https://doi.org/10.2307/1968484), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/alexcon.pdf))


Lecture notes:

* Rob Thompson, Len Evens , _[Topology notes](http://math.hunter.cuny.edu/~rthompso/topology_notes/)_ _Chapter 6, Singular homology_ ([pdf](http://math.hunter.cuny.edu/~rthompso/topology_notes/chapter%20six.pdf))

Textbook discussion in the context of [[homological algebra]] is around Application 1.1.4 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_
 {#Weibel}

and in the context of [[algebraic topology]] in chapter 2.1 of 

* {#Hatcher} [[Allen Hatcher]], _Algebraic Topology_ ([web](http://www.math.cornell.edu/~hatcher/AT/ATpage.html))
 

and [chapter 4](http://www.math.upenn.edu/~ghrist/EAT/EATchapter4.pdf) of 

* [[Robert Ghrist]], _Elementary applied topology_ ([web](http://www.math.upenn.edu/~ghrist/notes.html))
 {#Ghrist}

Discussion in the context of computing [[homotopy groups]] is in 

* [[Michael Hutchings]], _Introduction to higher homotopy groups and obstruction theory_ ([pdf](http://math.berkeley.edu/~hutching/teach/215b-2011/homotopy.pdf))
 {#Hutchings}

Lecture notes include

* [[Marco Gualtieri]], _Homology_ ([pdf](http://www.math.toronto.edu/mgualt/MAT1300/Week%206-9%20Term%202.pdf))

See also 

* Wikipedia, _[Singular homology](http://en.wikipedia.org/wiki/Singular_homology)_

### Examples and applications

* Michael  Barratt, [[John Milnor]], _An example of anomalous singular homology_, Proceedings of the American Mathematical Society
Vol. 13, No. 2 (Apr., 1962), pp. 293-297 ([JSTOR]( http://www.jstor.org/stable/2034486))

[[!redirects singular chain]] 
[[!redirects singular chains]] 

[[!redirects singular simplicial chain]] 
[[!redirects singular simplicial chains]] 


[[!redirects chain complex of singular simplices]]
[[!redirects chain complexes of singular simplices]]

[[!redirects singular chain homology]]

