
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In the context of [[homological algebra]], the _$Tor$-functor_ is the [[derived tensor product]]: the [[left derived functor]] of the [[tensor product of modules|tensor product of]] $R$-[[modules]], for $R$ a [[commutative ring]].

Together with the [[Ext-functor]] it constitutes one of the central operations of interest in [[homological algebra]].

## Definition

Given a [[ring]] $R$ the [[bifunctor]] $\otimes_R : Mod_{R} \times {}_{R}Mod\to Ab$
from two copies of $R$-[[Mod]] to [[Ab]] is a [[right exact functor]]. Its 
[[left derived functors]] are the **Tor-functors

$$
  Tor(-,B)
  : 
  Mod_R \to Ab
$$ 

and 

$$
  Tor(A,-)
  : 
  {}_{R}Mod \to Ab
$$ 

with respect to one argument with fixed another, if they exist, are parts of a bifunctor 

$$
  Tor : Mod_{R}\times {}_{R}Mod\to Ab
  \,.
$$ 

## Properties

### Existence and balancing
 {#ExistenceAndBalancing}

Given a right $R$-module

$$
  A \in Mod_R
$$

and a left $R$-module

$$
  B \in {}_R Mod
$$

there are in principle three different ways to compute their derived tensor product $Tor_\bullet(A,B)$:

1. keeping $B$ fixed and deriving the functor

   $$
     (-) \otimes_R B : Mod_R \to Ab 
   $$

1. keeping $A$ fixed and deriving the functor

   $$
     A \otimes_R (-) : {}_R Mod \to Ab
   $$

1. deriving the functor 

   $$
     (-) \otimes_R (-) : Mod_R \times {}_R Mod \to Ab
   $$

   in both arguments

+-- {: .num_theorem}
###### Theorem

If both $Mod_{R}$ and $_{R}Mod$ have [[projective object|enough projectives]], then all these three derived functors exist and all give the same result.
=--


+-- {: .proof}
###### Proof

Existence is clear from the very definition of [[derived functor in homological algebra]]. So we show that deriving in the left argument gives the same result as deriving in the right argument.

Let $Q^A_\bullet \stackrel{\simeq_{qi}}{\to} A$ and $Q^B_\bullet \stackrel{\simeq_{qi}}{\to} B$ be [[projective resolutions]] of $A$ and $B$, respectively. The corresponding [[tensor product of chain complexes]] 
$Tot (Q^A_\bullet\otimes Q^B_\bullet)$, hence the [[total complex]] of the degreewise [[tensor product of modules]] [[double complex]] carries the [[filtered chain complex|filtration]] by horizontal degree as well as that by vertical degree.

Accordingly there are the corresponding two [[spectral sequences of a double complex]], to be denoted here $\{{}^{A}E^r_{p,q}\}_{r,p,q}$ (for the filtering by $A$-degree) and $\{{}^{B}E^r_{p,q}\}_{r,p,q}$ (for the filtering by $B$-degree). By the discussion there, both converge to the chain homology of the total complex. 

We find the value of both spectral sequences on low degree pages according to the general discussion at _[spectral sequence of a double complex - low degree pages](spectral+sequence+of+a+double%20complex#LowDegreePages)_. 

The 0th page for both is

$$
  {}^A E^0_{p,q} = {}^B E^0_{p,q} \coloneqq Q^A_p \otimes_R Q^B_q  
  \,.
$$

For the first page we have

$$  
  \begin{aligned}
    {}^A E^1_{p,q} 
    & \simeq H_q(C_{p,\bullet}) 
    \\
    & \simeq  H_q( Q^A_p \otimes Q^B_\bullet )
  \end{aligned}
$$

and

$$  
  \begin{aligned}
    {}^B E^1_{p,q} 
    & \simeq H_q(C_{\bullet,p}) 
    \\
    & \simeq  H_q( Q^A_\bullet \otimes Q^B_p )
  \end{aligned}
  \,.
$$

Now using the [[universal coefficient theorem]] [in homology](universal%20coefficient%20theorem#InHomology) and the fact that $Q^A_\bullet$ and $Q^B_\bullet$ is a [[resolution]] by [[projective objects]], by construction, hence of tensor [[acyclic objects]] for which all [[Tor]]-modules vanish, this simplifies to

$$
  \begin{aligned}
     {}^A E^1_{p,q} 
     & \simeq Q^A_p \otimes H_q(Q^B_\bullet)
     \\
     & \simeq \left\{
       \array{
           Q^A_p \otimes_R B & if\; q = 0
           \\
           0 & otherwise
       }
     \right.
  \end{aligned}
$$

and similarly

$$
  \begin{aligned}
     {}^B E^1_{p,q} 
     & \simeq H_q(Q^A_\bullet) \otimes_R Q^B_p
     \\
     & \simeq \left\{
       \array{
           A \otimes_R Q^B_p & if\; q = 0
           \\
           0 & otherwise
       }
     \right.
  \end{aligned}
  \,.
$$

It follows for the second pages that

$$
  \begin{aligned}
    {}^A E^2_{p,q} 
    & \simeq
    H_p(H^{vert}_q(Q^A_\bullet \otimes Q^B_\bullet))
    \\
   & \simeq 
   \left\{
     \array{
     (L_p( (-)\otimes_R B ))(A) & if \; q = 0
     \\
     0 & otherwise    
     }
  \right.
  \end{aligned}
$$

and

$$
  \begin{aligned}
    {}^B E^2_{p,q} & \simeq
    H_p(H^{hor}_q(Q^A_\bullet \otimes Q^B_\bullet))
    \\
   & \simeq 
   \left\{
     \array{
       (L_p ( A \otimes_R (-) ))(B) & if \; q = 0
       \\
       0 \; otherwise
     }
   \right.
  \end{aligned}
  \,.
$$

Now both of these second pages are concentrated in a single row and hence have converged on that page already. Therefore, since they both converge to the same value:

$$
  L_p((-)\otimes_R B)(A)
  \simeq
  {}^A E^2_{p,0}
  \simeq
  {}^A E^\infty_{p,0}
  \simeq
  {}^B E^2_{p,0}
  \simeq
  L_p(A \otimes_R (-))(B)
  \,.
$$

=--


### Respect for direct sums and filtered colimits
 {#RespectForDirectSumsAndFilteredColimits}

+-- {: .num_prop #Tor1RespectsDirectSum}
###### Proposition

Each $Tor_n^R(-,N)$ respects [[direct sums]].


=--

+-- {: .proof}
###### Proof

Let $S \in$ [[Set]] and let $\{N_s\}_{s \in S}$ be an $S$-family of $R$-[[modules]]. Observe that 

1. if $\{(F_s)_\bullet\}_{s \in S}$ is an family of [[projective resolutions]], then their degreewise [[direct sum]] $(\oplus_{s \in S} F)_\bullet$ is a projective resolution of $\oplus_{s \in S} N_s$. 

1. the tensor product functor distributes over direct sums (this is discussed at _[tensor product of modules -- monoidal category structure](module#MonoidalCategoryStructure)_)

1. the [[chain homology]] functor preserves direct sums (this is discussed at _[chain homology - respect for direct sums](http://ncatlab.org/nlab/show/chain+homology+and+cohomology#RespectForDirectSum)_).

Using this we have

$$
  \begin{aligned}
    Tor_n^R(\oplus_{s \in S} N_s, N)
    & \simeq
    H_n\left( \left(\oplus_{s \in S} F\right) \otimes  N  \right)
    \\
    & \simeq
    H_n\left( \oplus_{s \in S} \left(F_s \otimes N \right)  \right)
    \\
    & \simeq \oplus_{s \in S} H_n( F_s \otimes N )
    \\
    & \simeq \oplus_{s \in S} Tor_n(N_s, N)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #TorPreservesFilteredColimits}
###### Proposition

Each $Tor_n^R(-,N)$ respects [[filtered colimits]].

=--

+-- {: .proof}
###### Proof

Let hence $A \colon I \to R Mod$ be a [[filtered category|filtered]] [[diagram]] of modules. For each $A_i$, $i \in I$ we may find a [[nLab:projective resolution]] and in fact a [[nLab:free resolution]] $(Y_i)_\bullet \stackrel{\simeq_{qi}}{\to} A$. Since [[chain homology]] commutes with filtered colimits (this is discussed at _[chain homology - respect for filtered colimits](http://ncatlab.org/nlab/show/chain+homology+and+cohomology#RespectForDirectSum)_), this means that 

$$
  (\underset{\to_i}{\lim} Y_i)_\bullet \to A
$$

is still a [[quasi-isomorphism]]. Moreover, by [[Lazard's criterion]] the degreewise filtered colimits of [[free modules]] $\underset{\to_i}{\lim} (Y_i)_n$ for each $n \in \mathbb{N}$ are [[flat modules]]. This means that $\underset{\to_i}{\lim} (Y_i)_\bullet \to A$ is [[flat resolution]] of $A$. By the very definition or else by the basic properties of [[flat modules]], this means that it is a $(-)\otimes N$-[[acyclic resolution]]. By the discussion there it follows that 

$$
  Tor_n^\mathbb{Z}(A,N)
  \simeq
  H_n( (\underset{\to_i}{\lim} Y_i) \otimes N )
  \,.
$$

Now the [[tensor product of modules]] is a [[left adjoint]] [[functor]] (the [[right adjoint]] being the [[internal hom]] of modules) and so it commutes over the filtered colimit to yield, using again that [[chain homology]] commutes with filtered colimits,

$$
  \begin{aligned}
  \cdots 
    & 
    \simeq 
    H_n( \underset{\to_i}{\lim} (Y_i \otimes N) )
    \\
    & \simeq
   \underset{\to_i}{\lim} H_n( Y_i \otimes N )   
    \\
    & \simeq
    \underset{\to_i}{\lim} Tor_n( A_i, N)
 \end{aligned}
  \,.
$$

=--



### Symmetry in the two arguments
 {#SymmetryInTheTwoArguments}

+-- {: .num_prop}
###### Proposition

For $N_1, N_2 \in R Mod$ and $n \in \mathbb{N}$ there is a [[natural isomorphism]]

$$
  Tor_n(A,B) \simeq Tor_n(B,A)
  \,.
$$

=--

We first give a proof for $R$ a [[principal ideal domain]] such as $\mathbb{Z}$.

+-- {: .proof}
###### Proof

Let $R$ be a [[principal ideal domain]] such as $\mathbb{Z}$ (in the latter case $R$[[Mod]]$\simeq$ [[Ab]]). Then by the discussion at _[projective resolution -- length-1 resolutions](projective+resolution#Lenght1ResolutionsOfAbelianGroups)_ there is always a [[short exact sequence]]

$$
  0 \to F_1 \to F_0 \to N \to 0
$$

exhibiting a [[projective resolution]] of any module $N$. It follows that $Tor_{n \geq 2}(-,-) = 0$.

Let then $0 \to F_1 \to F_2 \to N_2 \to 0$ be such a short resolution for $N_2$. Then by the [long exact sequence of a derived functor](derived+functor+in+homological+algebra#LongExactSequence) this induces an [[exact sequence]] of the form

$$
  0 \to Tor_1(N_1, F_1) \to Tor_1(N_1, F_0) \to Tor_1(N_1, N_2) \to N_1 \otimes F_1 \to N_1 \otimes F_0 \to N_1 \otimes N_2 \to 0
  \,.
$$

Since by construction $F_0$ and $F_1$ are already [[projective modules]] themselves this collapses to an exact sequence

$$
  0 \to Tor_1(N_1, N_2) \hookrightarrow N_1 \otimes F_1 \to N_1 \otimes F_0 \to N_1 \otimes N_2 \to 0
  \,.
$$

To the last three terms we apply the natural [[braided monoidal category|symmetric braiding]] [[isomorphism]] in $(R Mod, \otimes_R)$  to get 

$$
  \array{
    0 &\to& Tor_1(N_1, N_2) &\hookrightarrow& N_1 \otimes F_1 &\to& N_1 \otimes F_0 &\to& N_1 \otimes N_2 &\to& 0
    \\
    && \downarrow && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}} 
  && 
    \\ 
    0 &\to& Tor_1(N_2, N_1) &\hookrightarrow& F_1 \otimes N_1 &\to& F_0 \otimes N_1 &\to& N_2 \otimes N_1 &\to& 0
  }
  \,.
$$

This exhibits a morphism $Tor_1(N_1,N_2) \to Tor_1(N_2, N_1)$ as the morphism induced on [[kernels]] from an isomorphism between two morphisms. Hence this is itself an isomorphism. (This is just by the [[universal property]] of the [[kernel]], but one may also think of it as a simple application of the the [[four lemma]]/[[five lemma]].)

=--


### Localization
 {#Localization}

(...)

For instance ([Weibel, cor. 3.2.13](#Weibel)).

## Explicit computations for $Tor_1$

Over a commutative ring $R$, the computation of the Tor functor can be
reduced to the computation of each $Tor(M, R/I)$ where $I$ is a finitely generated ideal of $R$.

### $Tor_1$ and the torsion modules
{#RelationToTorsionGroups}

We shall start looking at the case where $I$ is a principal ideal generated by a [[regular element]] $r \in R$.

\begin{definition}
For $M$ and $R$-module and $r$ a [[regular element]] of $R$, we write

$$
  {}_r M \coloneqq \{ x \in M | r \cdot x = 0 \}
$$ 

for the **$r$-[[torsion submodule]]**.
\end{definition}

The following proposition explains why Tor functors are called this way.

\begin{proposition}
\label{TorOutOfCyclicGroup}
Let $R$ be a commutative ring, let $M$ be an $R$-module and let $r \in R$ be a [[regular element]] of $R$, then
$$
  Tor_1^R(R/(r), M)
  =
  {}_r M
$$
\end{proposition}

\begin{proof}
Since $r$ is regular, one has a short exact sequence
$$
  0 \to R \stackrel{\cdot r}{\to} R \stackrel{mod\, r}{\to}
  R/(r) \to 0
$$
which once tensored with $M$ gives us the long exact sequence
$$
  0 \to Tor_1(R/(r), M) \to M \stackrel{\cdot r}{\to} M \to M/rM \to 0
$$ 
One can then identify $Tor_1(R/(r), M)$ with the kernel of the map $x \mapsto rx$, that is ${}_r M$.
\end{proof}

This is no longer the case when $r$ is not regular.

\begin{proposition}
Let $\pi$ be an idempotent element of $R$, then the $R$-module $R/(\pi)$ is flat, that is
$$
  Tor_1^R(R/(\pi), X) = 0
$$
for every $R$-module $X$.
\end{proposition}

\begin{proof}
Since $\pi$ is idempotent, $R/(\pi)$ can be identified with the direct summand $(1-\pi)R$ of $R$. It is then a projective $R$-module and is then flat.
\end{proof}

### The case of abelian groups

For $n \in \mathbb{N}$ with $n \geq 1$, write $\mathbb{Z}_n = \mathbb{Z}/n\mathbb{Z}$ for the [[cyclic group]] of [[order]] $n$, as usual.

In the ring $\mathbb{Z}$ all non-zero elements are regular, we have thus
that for any abelian group $A$
$$
  Tor_1^\mathbb{Z}(\mathbb{Z}_n, A)
  \simeq
  {}_n A
$$
for every $n \neq 0$.

One can now leverage the knowledge of the structure of finite abelian groups to deduce the following proposition.

+-- {: .num_prop }
###### Proposition

Let $A$ be a [[finite abelian group]] and $B$ any abelian group. Then
$Tor_1(A,B)$ is a [[torsion group]].
Specifically, $Tor_1(A,B)$ is a [[direct sum]] of [[torsion subgroups]] of $B$.

=--

+-- {: .proof}
###### Proof

By a fundamental fact about [[finite abelian groups]] (see _[this theorem](finite+abelian+group#FiniteAbelianGroupIsDirectSumOfCyclics)_), $A$ is a [[direct sum of abelian groups|direct sum]] of [[cyclic group]] $A \simeq \oplus_k \mathbb{Z}_{p_k}$. By prop. \ref{Tor1RespectsDirectSum} $Tor_1$ respects this direct sum, so that

$$
  Tor_1(A,B) \simeq \oplus_k Tor_1(\mathbb{Z}_{p_k}, B)
  \,.
$$

By prop. \ref{TorOutOfCyclicGroup} every direct summand on the right is a torsion group and hence so is the whole direct sum.

=--


More generally we have:

+-- {: .num_prop}
###### Proposition

Let $A$ and $B$ be [[abelian groups]]. Write $Tor^\mathbb{Z}$ for the [[left derived functor]] of tensoring over $R = \mathbb{Z}$.  Then

1. $Tor^\mathbb{Z}_1(A,B)$ is a [[torsion group]]. Specifically it is a [[filtered colimit]] of torsion subgroups of $B$.

1. $Tor^{\mathbb{Z}}_1(\mathbb{Q}/\mathbb{Z}, A)$ is the [[torsion subgroup]] of $A$.

1. $A$ is a [[torsion subgroup|torsion-free group]] precisely if $Tor^\mathbb{Z}_1(A,-) = 0$, equivalently if $Tor^\mathbb{Z}_1(-,A) = 0$.

=--

For instance ([Weibel, prop. 3.1.2, prop. 3.1.3, cor. 3.1.5](#Weibel)).

+-- {: .proof}
###### Proof

The group $A$ may be expressed as a [[filtered colimit]] 

$$
  A \simeq \underset{\to_i}{\lim} A_i
$$

of finitely generated [[subgroups]] (this is discussed at _[Mod - Limits and colimits](http://ncatlab.org/nlab/show/Mod#LimitsAndColimits)_). Each of these is a [[direct sum]] of [[cyclic groups]]. 

By prop. \ref{TorPreservesFilteredColimits} $Tor_1^\mathbb{Z}(-,B)$ preserves these colimits. By prop. \ref{TorOutOfCyclicGroup} every cyclic group is sent to a torsion group (of either $A$ or $B$).  Therefore by prop. \ref{TorOutOfCyclicGroup} $Tor_1(A,B)$ is a filtered colimit of direct sums of torsion groups. This is itself a torsion group.

=--


+-- {: .num_remark}
###### Remark

Analogous results fail, in general, for $\mathbb{Z}$ replaced by another ring $R$.

=--

+-- {: .num_cor}
###### Corollary

An [[abelian group]] is [[torsion subgroup|torsion free]] precisely if regarded as a $\mathbb{Z}$-[[module]] it is a [[flat module]].

=--

See at _[flat module - Examples](flat+module#Examles)_ for more.

### $Tor_1$ of two cyclic modules

\begin{proposition}
Let $R$ be a commutative ring and let $I \subset R$ and $J \subset R$ be two ideals. Then
$$
Tor^R_1(R/I, R/J) \simeq (I \cap J) /IJ
$$
\end{proposition}

\begin{proof}
One has a short exact sequence $0 \to I \to R \to R/I \to 0$. Tensoring it
with $R/J$, one gets the long exact sequence
$$
0 \to Tor_1(R/I, R/J) \to I \otimes R/J \to R/J \to R/I \otimes R/J \to 0
$$
Hence $Tor_1(R/I, R/J)$ can be identified with the kernel of the map
$I \otimes R/J \to R/J$ which is isomorphic to $(I \cap J)/IJ$.
\end{proof}

## Related concepts

* [[Ext]]

* [[Cotor]]

* [[flat resolution lemma]]

* [[universal coefficient theorem]]

## References

Standard textbook accounts include the following:

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_,  Cambridge Studies in Adv. Math. 38, CUP 1994
 {#Weibel}

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton Univ. Press 1956.

* M. Kashiwara and P. Schapira, _[[Categories and Sheaves]]_, Springer (2000)

* S. I . Gelfand, Yu. I. Manin, _Methods of homological algebra_

Lecture notes include

* Daniel Murfet, _Tor_  ([pdf](http://therisingsea.org/notes/Tor.pdf))

section 3 of 

* [[Peter May]], _Notes on Tor and Ext_ ([pdf](http://www.math.uchicago.edu/~may/MISC/TorExt.pdf))
 {#May}

and specifically for [[symmetric smash product of spectra|symmetric]] [[model categories of spectra]]

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], section 7 of _[[Modern foundations for stable homotopy theory]]_ ([pdf](https://www.math.uchicago.edu/~may/PAPERS/Newfirst.pdf))


Original articles include

* Patrick Keef, _On the Tor functor and some classes of abelian groups_,  Pacific J. Math. Volume 132, Number 1 (1988), 63-84. ([Euclid](http://projecteuclid.org/euclid.pjm/1102689795))



[[!redirects Tor-functor]]
[[!redirects Tor functor]]
[[!redirects Tor-functors]]
[[!redirects Tor functors]]