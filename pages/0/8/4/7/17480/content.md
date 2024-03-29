
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
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

A _symmetric ring spectrum_ is a [[ring spectrum]] modeled as a [[symmetric spectrum]]. Equivalently this is a [[monoid object]] with respect to the [[symmetric monoidal smash product of spectra]], for symmetric spectra.
Morever, if we regard symmetric spectra as $\mathbb{S}_{sym}$-[[modules]], as discussed at _[[Model categories of diagram spectra]]_, then this, in turn, is equivalent to a $\mathbb{S}_{sym}$-algebra, where $\mathbb{S}_{sym}$ is the standard model of the [[sphere spectrum]] as a symmetric spectrum.

There is a [[model structure for ring spectra|model structure for symmetric ring spectra]] ([MMSS 00](#MandellMaySchwedeShipley01)) under which symmetric ring spectra represent genuine [[A-infinity rings]], and commutative symmetric ring spectra represent genuine [[E-infinity rings]]. This fact is one of the key motivation for passing from [[sequential spectra]] to the richer model of [[symmetric spectra]] (and possibly further to other [[highly structured spectra]] such as [[orthogonal spectra]] and [[excisive functors]]).

Despite all this, the component expression of the structure in a symmetric ring spectrum, in the fashion of _[[functors with smash product]]_, is rather straightforward, and directly analogous to the structure in a [[dg-algebra]]: essentially there is for all pairs of indices $n_1, n_2$ a pairing between the component spaces of the spectrum in these degrees

$$
  E_{n_1}\wedge E_{n_2}\longrightarrow E_{n_1 + n_2}
$$

such that this respects the given action of the [[symmetric groups]] and of [[suspensions]], and such that it is is [[associativity|associative]] and [[unitality|unital]] in the evident way.

## Definition

Write $Top_{cg}^{\ast}$ for the [[category]] of [[pointed topological space|pointed]] [[compactly generated topological spaces]].

One minimal way to state the definition is as follows. We follow conventions as used at _[[model structure on orthogonal spectra]]_.

+-- {: .num_defn #RingSpectrumInSymmetricAndOrthogonalSpectra}
###### Definition

A **commutative symmetric ring spectrum** $E$ is 

1. a sequence of component spaces $E_n \in Top^{\ast/}_{cg}$ for $n \in \mathbb{N}$;

1. a basepoint preserving continuous left [[action]] of the [[symmetric group]] $\Sigma(n)$ on $E_n$;

1. for all $n_1,n_2\in \mathbb{N}$ a _multiplication map_

   $$
     \mu_{n_1,n_2}
       \;\colon\;
      E_{n_1} \wedge E_{n_2} \longrightarrow E_{n_1 + n_2}
   $$

   (a morphism in $Top^{\ast/}_{cg}$)

1. two _unit maps_

   $$
     \iota_0 \;\colon\; S^0 \longrightarrow E_0
   $$

   $$
     \iota_1 \;\colon\; S^1 \longrightarrow E_1
   $$

such that

1. $\mu_{n_1,n_2}$ [[intertwiner|intertwines]] the $\Sigma(n_1) \times \Sigma(n_2)$-action;

1. (associativity) for all $n_1, n_2, n_3 \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]] (where we are notationally suppressing the [[associators]] of $(Top^{\ast/}_{cg}, \wedge, S^0)$)

   $$
     \array{
       E_{n_1} \wedge E_{n_2} \wedge E_{n_3}
         &\overset{id \wedge \mu_{n_2,n_3}}{\longrightarrow}&
       E_{n_1} \wedge E_{n_2 + n_3}
       \\
       {}^{\mathllap{\mu_{n_1,n_2}\wedge id }}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{n_1, n_2 + n_3}}}
       \\
       E_{n_1 + n_2} \wedge E_{n_3}
         &\underset{\mu_{n_1 + n_2, n_3}}{\longrightarrow}&
       E_{n_1 + n_2 + n_3}
     }
     \,;
   $$

1. (unitality) for all $n \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       S^0 \wedge E_n 
         &\overset{\iota_0 \wedge id}{\longrightarrow}&
       E_0 \wedge E_n
       \\
       &{}_{\mathllap{\ell^{Top^{\ast/}_{cg}}_{E_n}}}\searrow& \downarrow^{\mathrlap{\mu_{0,n}}}
       \\
       && E_n
     }
   $$

   and

   $$
     \array{
       E_n \wedge S^0 
         &\overset{id \wedge \iota_0 }{\longrightarrow}&
       E_n \wedge E_0
       \\
       &{}_{\mathllap{r^{Top^{\ast/}_{cg}}_{E_n}}}\searrow& \downarrow^{\mathrlap{\mu_{n,0}}}
       \\
       && E_n
     }
   $$

1. (commutativity) for all $n_1, n_2 \in \mathbb{N}$ the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       E_{n_1} \wedge E_{n_2}
         &\overset{\tau^{Top^{\ast/}_{cg}}_{E_{n_1}, E_{n_2}}}{\longrightarrow}&
       E_{n_2} \wedge E_{n_1}
       \\
       {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow
         &&
       \downarrow^{\mathrlap{\mu_{n_2,n_1}}}
       \\
       E_{n_1 + n_2}
         &\underset{\chi_{n_1,n_2}}{\longrightarrow}&
       E_{n_2 + n_1}
     }
     \,,
   $$

where $\chi_{n_1,n_2} \in \Sigma(n_1 + n_2)$ denotes the [[permutation]] which [[shuffle|shuffles]] the first $n_1$ elements past the last $n_2$ elements.

A [[homomorphism]] of symmetric commutative ring spectra $f \colon E \longrightarrow E'$ is a sequence $f_n \;\colon\; E_n \longrightarrow E'_n$ of $\Sigma(n)$-equivariant pointed continuous functions such that the following [[commuting diagram|diagrams commute]] for all $n_1, n_2 \in \mathbb{N}$

$$
  \array{
    E_{n_1} \wedge E_{n_2}
     &\overset{f_{n_1} \wedge f_{n_2}}{\longrightarrow}&
    E'_{n_1} \wedge E'_{n_2}
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow 
      &&
    \downarrow^{\mu_{n_2,n_1}}
    \\
    E_{n_1 + n_2}
     &\underset{\chi_{n_1, n_2}}{\longrightarrow}&
    E_{n_2 + n_1}
  }
$$

and $f_0 \circ \iota_0 = \iota_0$ and $f_1\circ \iota_1 = \iota_1$.

Write

$$
  CRing(SymSpec(Top_{cg}))
$$

for the resulting [[category]] of symmetric [[commutative ring spectra]].

There is an analogous definition of **[[orthogonal ring spectrum]]** and we write

$$
  CRing(OrthSpec(Top_{cg}))
$$

for the category that these form.

=--

([Schwede 12, def. 1.3](#Schwede12))

## Related concepts

* [[orthogonal ring spectrum]]


## References

* {#MandellMaySchwedeShipley01} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

The structure of a [[symmetric ring spectrum]] on [[KO]] is discussed in

* {#Joachim01} [[Michael Joachim]], _A symmetric ring spectrum representing
$KO$-theory_, Topology 40 (2001) 299-308

[[!redirects symmetric ring spectra]]
