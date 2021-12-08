
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

The **torsion subgroup** of a [[group]] $G \in $ [[Grp]] is the [[subgroup]] of all those [[elements]] $g \,\in\, G$, which have [[finite number|finite]] [[order]], i.e. those for which  some power is the [[neutral element]]
$$
  g \in G \;\text{is torsion}
  \;\;\;\;\;\;\Leftrightarrow\;\;\;\;\;\;
  \underset{n \in \mathbb{N}}{\exists}
  \;\;\;
  g^n 
  \;\coloneqq\;
  \underset{
    n\; factors
  }{
    \underbrace{
      g \cdot g \cdots g
    }
  }
  \,=\, \mathrm{e}
  \,.
$$ 


A group is 

* *pure torsion* if it coincides with its torsion subgroup, 

* *torsion-free* if its torsion subgroup is [[trivial subgroup|trivial]].

Notice that for [[abelian groups]] $A \in $ [[AbGrp]], where the group operation is traditionally written as addition $+$ and the [[neutral element]] is written as zero, this reads:

$$
  a \in A \;\text{is torsion}
  \;\;\;\;\;\Leftrightarrow\;\;\;\;\;
  \underset{n \in \mathbb{N}}{\exists}
  \;\;\;
  n \cdot a 
  \;\coloneqq\;
  \underset{
    n\; summands
  }{
    \underbrace{
      a + a \cdots + a
    }
  }
  \,=\, 0
  \,.
$$ 


Given a [[ring]] $R$, an element $m$ in an $R$-[[module]] $M$ is **torsion element** if there is a nonzero element $r$ in $R$ such that $r m=0$. A **[[torsion module]]** is a module whose elements are all torsion. A [[torsion-free module]] is a module whose elements are not torsion, other than $0$. 

Torsion and torsion-free classes of objects in an [[abelian category]] were introduced axiomatically as a [[torsion theory]] (or torsion pair) in ([Dickson 1963](#Dickson63)).

Beware that there are other, completely independent, concepts referred to as _[[torsion]]_. See there for more.

## Properties

### Relation to the $Tor$-functor

+-- {: .num_prop}
###### Proposition

For $A$ an [[abelian group]], its torsion subgroup is isomorphic to the value of the degree-1 [[Tor|Tor functor]] $Tor^\mathbb{Z}_1(\mathbb{Q}/\mathbb{Z}, A)$. 

=--

See at _[Tor - relation to torsion subgroups](Tor#RelationToTorsionGroups)_ for more.

### Relation to flatness

+-- {: .num_prop}
###### Proposition

An [[abelian group]] is torsion-free precisely if regarded as a $\mathbb{Z}$-[[module]] it is a [[flat module]].

=--

This is a special case of a [more general result](http://ncatlab.org/nlab/show/principal+ideal+domain#flat) for modules over a principal ideal domain. See also _[flat module - Examples](flat+module#Examles)_ for more.


## Examples and applications  
 {#ExamplesAndApplications}

\begin{example}\label{FiniteGroupsArePureTorsion}
**(finite groups are pure torsion)**
\linebreak
Every [[finite group]] is pure torsion, hence is its own maximal torsion subgroup. 
\end{example}

\begin{example}
**(tensoring with the rational numbers removes torsion subgroups)**
\linebreak
Given an [[abelian group]] $A$ which is pure torsion (e.g. a [[finite abelian group]], by Ex. \ref{FiniteGroupsArePureTorsion}), its [[tensor product of abelian groups|tensor product]] with the additive group of [[rational numbers]] is the [[trivial group|trivial]] abelian group:

$$
  A \,\text{torsion}
  \;\;\;
  \Rightarrow
  \;\;\;
  A \otimes_{\mathbb{Z}} \mathbb{Q}
  \;\simeq\;
  0
  \;\;\;
  \in
  \;
  AbGrp
  \,.
$$

Because, for $a \in A$ with
$\underset{ n\;summands }{\underbrace{a + a + \cdots + a}} =  0$ and for
$p,q \in \mathbb{Z} \subset \mathbb{Q}$ with $q \neq 0$ we have, by the definition of [[tensor product of abelian groups]]:

$$
  \begin{aligned}
    a \otimes \frac{p}{q}
    & \;=\; 
    a \otimes 
    \underset{n\; summands}{
    \underbrace{
      \Big(
       \frac{p}{n \cdot q} 
         + \frac{p}{n \cdot q} 
         + \cdot  +
          \frac{p}{n \cdot q} 
      \Big)
    }}
    \\
    & \;=\;
    \underset{n\;summands}{
    \underbrace{
      \Big(a \otimes \frac{p}{n \cdot q}\Big) 
      + \cdots + 
      \Big(a \otimes \frac{p}{n \cdot q}\Big) 
    }}
    \\
    & \;=\;
     \underset{
       n \; summands
     }{
     \underbrace{
       ( a + \cdots + a )
     }}
     \otimes 
     \frac{p}{n \cdot q}
    \\
    & \;=\;
    0 \otimes \frac{p}{n \cdot q}
    \\
    & \;=\; 0  
    \,.
  \end{aligned}
$$

In [[rational homotopy theory]] one considers the higher [[homotopy groups]] $\pi_n(X)$ of [[topological spaces]] $X$ tensored over [[rational numbers|$\mathbb{Q}$]]: the resulting groups $\pi_n(X) \otimes_{\mathbb{Z}} \mathbb{Q}$ are then necessarily torsion-free -- in this sense [[rational homotopy theory]] studies spaces "up to torsion".
\end{example}

\begin{example}
**(torsion homotopy groups of spheres)**
\linebreak
  By the [[Serre finiteness theorem]], the [[homotopy groups of spheres]] are [[finite groups]], and hence pure torsion by Ex. \ref{FiniteGroupsArePureTorsion}, except in the degree of the dimension of the sphere and, for even-dimensional spheres, twice its dimension minus one:

  $$
    \pi_k\big( S^n \big)
    \;\;
    \simeq
    \;
    \left\{
    \begin{array}{ll}
      \mathbb{Z} & k = n
      \\
      \mathbb{Z} \oplus \text{torsion} & 
      k = 2n-1  \;\text{and}\; n\;\text{even} 
      \\
      \text{torsion} & \text{otherwise}
    \end{array}
    \right.
  $$
\end{example}

\begin{example}
**(torsion in elliptic curves)**
\linebreak
The torsion elements of an [[elliptic curve]] as a group are important in [[number theory]] and [[arithmetic geometry]]. See [[torsion points of an elliptic curve]].
\end{example}

## Related concepts

* [[torsion-free module]]

* [[p-torsion]]

* [[torsion approximation]]

* [[Pontryagin duality for torsion abelian groups]]

* [[Bockstein homomorphism]]

## References

On axiomatization of [[torsion theory]] in [[abelian categories]]:

* {#Dickson63} [[Spencer Ernst Dickson]], _Torsion theories for abelian categories_, Thesis, New Mexico State University (1963) ([ProQuest](https://www.proquest.com/openview/0c7793e99ae9368bd940699a03d70132/1))
 
* {#Dickson66} [[Spencer Ernst Dickson]], *A Torsion Theory for Abelian Categories*, Transactions of the American Mathematical Society **121** 1 (1966) 223-235 ([doi:10.2307/1994341](https://doi.org/10.2307/1994341), [jstor:1994341](https://www.jstor.org/stable/1994341))


[[!redirects torsion subgroup]]
[[!redirects torsion subgroups]]

[[!redirects torsion group]]
[[!redirects torsion groups]]
[[!redirects torsion element]]
[[!redirects torsion elements]]


[[!redirects torsion-free group]]
[[!redirects torsion-free abelian group]]
[[!redirects torsion-free groups]]
[[!redirects torsion-free abelian groups]]