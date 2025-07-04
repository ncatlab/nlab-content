
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a sequence 

$$
  X_\bullet
  =
  \left(
  X_0 
   \overset{f_0}{\longrightarrow}
  X_1
   \overset{f_1}{\longrightarrow}
  X_2
   \overset{f_2}{\longrightarrow}
  \cdots
  \right)
$$

of ([[pointed topological space|pointed]]) [[topological spaces]], then its _mapping telescope_ is the result of forming the (reduced) [[mapping cylinder]] $Cyl(f_n)$ for each $n$ and then attaching all these cylinders to each other in the canonical way.


At least if all the $f_n$ are inclusions, this is the sequential attachment of ever "larger" cylinders, whence the name "telescope".

The mapping telescope is a representation for the [[homotopy colimit]] over $X_\bullet$. It is used for instance for discussion of [[lim^1 and Milnor sequences]] (and that's maybe the origin of the concept?).

## Definition

+-- {: .num_defn #MappingTelescope}
###### Definition

For

$$
  X_\bullet
  =
  \left(
  X_0 
   \overset{f_0}{\longrightarrow}
  X_1
   \overset{f_1}{\longrightarrow}
  X_2
   \overset{f_2}{\longrightarrow}
  \cdots
  \right)
$$

a sequence  in [[Top]], its **mapping telescope** is the [[quotient topological space]] of the [[disjoint union]] of [[product topological spaces]]

$$
  Tel(X_\bullet)
  \coloneqq
  \left(
  \underset{n \in \mathbb{N}}{\sqcup}  
  \left(
    X_n \times [n,n+1]
  \right)
  \right)/_\sim
$$

where the [[equivalence relation]] quotiented out is

$$
  (x_n, n+1) \sim (f(x_n), n+1)
$$

for all $n\in \mathbb{N}$ and $x_n \in X_n$.

Analogously for $X_\bullet$ a sequence of [[pointed topological spaces]] then use [[reduced cylinders]] to set

$$
  Tel(X_\bullet)
  \coloneqq
  \left(
  \underset{n \in \mathbb{N}}{\sqcup}  
  \left(
    X_n \wedge [n,n+1]_+
  \right)
  \right)/_\sim
  \,.
$$

=--

## Properties

### For CW-complexes

+-- {: .num_prop #TelescopeOfCWComplexEquivalentToTheOriginal}
###### Proposition

For $X_\bullet$ the sequence of stages of a ([[pointed topological space|pointed]]) [[CW-complex]] $X = \underset{\longleftarrow}{\lim}_n X_n$, then the canonical map

$$
  Tel(X_\bullet)
  \longrightarrow
  X
$$

from the [[mapping telescope]], def. \ref{MappingTelescope}, is a [[weak homotopy equivalence]].

=--


+-- {: .proof}
###### Proof

Write in the following $Tel(X)$ for $Tel(X_\bullet)$ and write $Tel(X_n)$ for the mapping telescop of the substages of the finite stage $X_n$ of $X$. It is intuitively clear that each of the projections at finite stage

$$
  Tel(X_n) \longrightarrow X_n
$$

is a [[homotopy equivalence]], hence a [[weak homotopy equivalence]]. A concrete construction of a homotopy inverse is given for instance in ([Switzer 75, proof of prop. 7.53](#Switzer75)).

Moreover, since spheres are [[compact object|compact]], so that elements of [[homotopy groups]] $\pi_q(Tel(X))$ are represented at some finite stage $\pi_q(Tel(X_n))$ it follows that 

$$
  \underset{\longrightarrow}{\lim}_n \pi_q(Tel(X_n)) 
    \overset{\simeq}{\longrightarrow} 
  \pi_q(Tel(X))
$$

are [[isomorphisms]] for all $q\in \mathbb{N}$ and all choices of basepoints (not shown). 

Together these two facts imply that in the following commuting square, three morphisms are isomorphisms, as shown.

$$
  \array{
    \underset{\longleftarrow}{\lim}_n \pi_q(Tel(X_n))
    &\overset{\simeq}{\longrightarrow}&
    \pi_q(Tel(X))
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow
    \\
    \underset{\longleftarrow}{\lim}_n \pi_q(X_n)
    &\underset{\simeq}{\longrightarrow}&
    \pi_q(X)    
  }
  \,.
$$

Therefore also the remaining morphism is an isomorphism ([[two-out-of-three]]). Since this holds for all $q$ and all basepoints, it is a weak homotopy equivalence.

=--



## Related concepts


* [[homotopy colimit]]

[[!include universal constructions of topological spaces -- table]]



## References

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

