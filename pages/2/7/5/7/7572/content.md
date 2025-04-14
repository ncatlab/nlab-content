
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The classical _Heine--Borel theorem_ identifies those [[topological subspaces]] of [[Cartesian spaces]] ($\mathbb{R}^n$s) that are [[compact space|compact]] in terms of simpler properties.  A generalisation applies to all [[metric spaces]] and even to [[uniform spaces]].


## Versions

This is the classical theorem:

+-- {: .num_theorem #classical}
###### Theorem

Let $S$ be a [[topological subspace]] of a [[Cartesian space]] ($S \subset \mathbb{R}^n$).  Then $S$ is a [[compact topological space]] (with the [[induced topology]]) precisely if it is [[closed subset|closed]] and [[bounded subset|bounded]] in $\mathbb{R}^n$.
=--

It\'s easy to prove that $S$ is closed precisely if it is a [[complete metric space]] as with the induced [[metric]], and similarly $S$ is bounded precisely if it is [[totally bounded metric space|totally bounded]].  This gives the next version:

+-- {: .num_theorem #cartesian}
###### Theorem

Let $S$ be a [[topological subspace]] of a [[Cartesian space]] ($S \subset \mathbb{R}^n$).  Then $S$ is a [[compact topological space]] (with the [[induced topology]]) precisely if it is [[complete space|complete]] and [[totally bounded space|totally bounded]] (with the [[induced metric]]).
=--

This refers entirely to $S$ as a metric space in its own right.  In fact it holds much more generally than for subspaces of a cartesian space:

+-- {: .num_theorem #metric}
###### Theorem

Let $S$ be a [[metric space]].  Then $S$ is [[compact space|compact]] precisely if it is [[complete space|complete]] and [[totally bounded space|totally bounded]].
=--

This theorem refers only to uniform properties of $S$, and in fact a further generalistion is true:

+-- {: .num_theorem #uniform}
###### Theorem

Let $S$ be a [[uniform space]].  Then $S$ is [[compact space|compact]] precisely if it is [[complete space|complete]] and [[totally bounded space|totally bounded]].
=--

The hard part is proving that a complete totally bounded space is compact; the converse is easy.

We could also try to generalise Theorem \ref{classical} to subspaces of other metric spaces, but this fails: every compact subspace of a metric space is closed and bounded (which is the easy direction), but not conversely.

Another variant of these statements is:

* _[[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]_


## Logical status

In the old days, one called a closed and bounded [[interval]] in the [[real line]] 'compact'; once closedness and boundedness were generalised from intervals to arbitrary [[subsets]] (of the real line), the definition of 'compact' also generalised.  The content of Theorem \ref{classical}, then, is that this condition is equivalent to the modern definition of 'compact' using [[open covers]], and indeed the modern definition was only derived afterwards as a name for the conclusion of the theorem.

In [[constructive mathematics]], one sees several definitions of 'compact', which may make the theorem provable, refutable, or undecidable in various constructive systems.  Using the open-cover definition of 'compact', Theorems \ref{classical} and \ref{cartesian} are equivalent to the [[fan theorem]] (and so hold in [[intuitionism]]), but Theorems \ref{metric} and \ref{uniform} are stronger and [[Jan Brouwer|Brouwer]] could not prove them, leading him to *define* 'compact' (for a metric space) to mean complete and totally bounded.  In other literature, one sometimes sees the abbreviation 'CTB' used instead.  In [[Russian constructivism]], already Theorems \ref{classical} and \ref{cartesian} can be refuted using the open-cover definition, but CTB spaces are still important.

In [[locale theory]] and other approaches to [[pointless topology]], the open-cover definition of 'compact' is clearly correct, and the failure of CTB spaces to be compact (constructively) may be seen as a consequence of working with points.  Already in Bishop\'s weak system of constructivism, every CTB metric space $X$ gives rise to a compact locale, which classically (assuming [[excluded middle]] and [[dependent choice]]) is the [[locale of open subsets]] of $X$ but constructively requires a more nuanced construction; see [Vickers](#CTBlocale).

{#InDTT} In [[dependent type theory]], the open-cover definition of 'compact' holds as well, but one has to use the [[higher inductive type|higher]] [[inductive family]] of [[inductive covers]] instead of the usual pointwise definitions of covers ([UFP13, §11.5](#UFP13)). 



## Proofs
 {#Proofs}

For definiteness, we restate the versions which we prove:

+-- {: .num_lemma #CompactClosedInterval}
###### Lemma
**(closed interval is compact)**

In [[classical mathematics]]:

For any $a \lt b \in \mathbb{R}$ the [[closed interval]]

$$
  [a,b] \subset \mathbb{R}
$$

regarded with its [[topological subspace|subspace topology]] is a [[compact topological space]].

=--

+-- {: .proof}
###### Proof

Since all the closed intervals are [[homeomorphism|homeomorphic]]
it is sufficient to show the statement for $[0,1]$. Hence let $\{U_i \subset [0,1]\}_{i \in I}$ be an 
open cover. We need to show that it has an open subcover.

Say that an element $x \in [0,1]$ is _admissible_ if the closed sub-interval $[0,x]$ is covered by 
finitely many of the $U_i$. In this terminlogy, what we need to show is that $1$ is admissible.

Observe from the definition that 

1. 0 is admissible,

1. if $y \lt x \in [0,1]$ and $x$ is admissible, then also $y$ is admissible.

This means that the set of admissible $x$ forms either an [[open interval]] $[0,g)$ or a [[closed interval]]
$[0,g]$, for some $g \in [0,1]$. We need to show that the latter is true, and for $g = 1$. 
We do so by observing that the alternatives lead to contradictions:

1. Assume that the set of admissible values were an open interval $[0,g)$. By assumption there would be 
   a finite subset $J \subset I$ such that $\{U_i \subset [0,1] \}_{i \in J \subset I}$ were a finite 
   open cover of $[0,g)$. Accordingly, since there is some $i_g \in I$ such that $g \in U_{i_g}$, the union
   $\{U_i\}_{i \in J } \sqcup \{U_{i_g}\}$ were a finite cover of the closed interval $[0,g]$, 
   contradicting the assumption that $g$ itself is not admissible (since it is not contained in $[0,g)$).
   
1. Assume that the set of admissible values were a closed interval $[0,g]$ for $g \lt 1$. 
   By assumption there would then be a finite set $J \subset I$ such that $\{U_i \subset [0,1]\}_{i \in J \subset I}$
   were a finite cover of $[0,g]$. Hence there would be an index $i_g \in J$ such that $g \in U_{i_g}$.
   But then by the nature of open subsets in the Euclidean space $\mathbb{R}$, this $U_{i_g}$ would also 
   contain an open ball $B^\circ_g(\epsilon) = (g-\epsilon, g + \epsilon)$. This would mean that 
   the set of admissible values includes the open interval $[0,g+ \epsilon)$, contradicting the assumption.
   
This gives a [[proof by contradiction]].

=--


+-- {: .num_prop #BorelHeine}
###### Proposition
**([[Heine-Borel theorem]] classically)**

For $n \in \mathbb{N}$, regard $\mathbb{R}^n$ as the $n$-dimensional [[Euclidean space]],
regarded as a [[topological space]] via its [[metric topology]].

Then in [[classical mathematics]] for a [[topological subspace]] $S \subset \mathbb{R}^n$ the following are equivalent:

1. $S$ is  [[compact topological space|compact]],

1. $S$ is [[closed subset|closed]] and [[bounded subset|bounded]].

=--

+-- {: .proof #BorelHeineProof}
###### Proof

First consider a [[subset]] $S \subset \mathbb{R}^n$ which is closed and bounded. We need to show that
regarded as a [[topological subspace]] it is [[compact topological space|compact]].

The assumption that $S$ is bounded by (hence contained in) some [[open ball]] $B^\circ_x(\epsilon)$ in $\mathbb{R}^n$ 
implies that it is contained in $\{ (x_i)_{i = 1}^n \in \mathbb{R}^n \,\vert\, -\epsilon \leq x_i \leq \epsilon \}$.
This topological subspace is homeomorphic to the $n$-cube
$[-\epsilon, \epsilon]^n$. Since the closed interval $[-\epsilon, \epsilon]$
is compact by lemma \ref{CompactClosedInterval}, the [[Tychonoff theorem]]
implies that this $n$-cube is compact. 

Since [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]] the closed subset $S \subset \mathbb{R}^n$ is still closed as a subset $S \subset [-\epsilon, \epsilon]^n$.
Since [[closed subspaces of compact spaces are compact]] this implies that $S$ is compact.

Conversely, assume that $S \subset \mathbb{R}^n$ is a compact subspace. We need to show that it is closed and bounded.

The first statement follows since 
the [[Euclidean space]] $\mathbb{R}^n$ is [[Hausdorff topological space|Hausdorff]]
and since [[compact subspaces of Hausdorff spaces are closed]].

Hence what remains is to show that $S$ is bounded.

To that end, choose any [[positive number|positive]] [[real number]] $\epsilon \in \mathbb{R}_{\gt 0}$
and consider the [[open cover]] of all of $\mathbb{R}^n$ by the open [[n-cubes]] 

$$
  (k_1-\epsilon, k_1+1+\epsilon) 
    \times 
  (k_2-\epsilon, k_2+1+\epsilon)
    \times  
      \cdots
    \times
  (k_n-\epsilon, k_n+1+\epsilon)
$$

for [[n-tuples]] of [[integers]] $(k_1, k_2 , \cdots, k_n ) \in \mathbb{Z}^n$.
The restrictions of these to $S$ hence form an open cover of the subspace $S$. By the assumption that 
$S$ is compact, there is then a finite subset of $n$-tuples of integers such that the 
corresponding $n$-cubes still cover $S$. But the union of any finite number of bounded closed $n$-cubes
in $\mathbb{R}^n$ is clearly a bounded subset, and hence so is $S$.

=--




## Related theorem

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[Tietze extension theorem]]

* [[Tychonoff theorem]]

* [[topological invariance of dimension]]

* [[Brouwer's fixed point theorem]]

* [[Jordan curve theorem]]

* [[Heine-Cantor theorem]]

* [[fan theorem]] (The [[locale]] of [[Cantor space]] is a [[spatial locale]].)

* [[monotone bar induction]] (The [[locale]] of the [[Baire space of sequences]] is a [[spatial locale]].)

* [[principle of enough functions]] (The [[locale]] of the [[function space]] $\mathbb{R}^\mathbb{R}$ is a [[spatial locale]].)

## References

[According to Wikipedia](https://en.wikipedia.org/wiki/Heine%E2%80%93Borel_theorem#History_and_motivation), the theorem was first proved by [[Pierre Cousin]] in 1895.  It is named after [[Eduard Heine]] (who used it but did not prove it) and [[Émile Borel]] (who proved a limited version of it), an instance of [[Stigler's law of eponymy]].

A proof is spelled out for instance at

* [ProofWiki](http://www.proofwiki.org/wiki/Main_Page),  _Heine-Borel Theorem [(General case)](http://www.proofwiki.org/wiki/Heine-Borel_Theorem_%28General_Case%29),  [(Special case)](http://www.proofwiki.org/wiki/Heine-Borel_Theorem_%28Special_Case%29)_

On the [[Heine-Borel theorem]] not implying the [[fan theorem]] in the absence of [[countable choice]]:

* [[Ieke Moerdijk]], *Heine-Borel Does Not Imply the Fan Theorem*, Journal of Symbolic Logic, vol. 49, no. 2, 1984, pp. 514–519. ([doi:10.2307/2274182](https://doi.org/10.2307/2274182))

On constructing a compact locale from a CTB metric space:

*  {#CTBlocale} [[Steve Vickers]], [Localic completion of generalized metric spaces](http://www.tac.mta.ca/tac/volumes/14/15/14-15abs.html)
   
On the Heine-Borel theorem in [[dependent type theory]] using [[inductive covers]], see section 11.5 of:

* {#UFP13} [[Univalent Foundations Project]]: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]*, The Institute for Advanced Study (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

[[!redirects Heine-Borel theorem]]
[[!redirects Heine-Borel theorems]]
[[!redirects Heine--Borel theorem]]
[[!redirects Heine--Borel theorems]]
[[!redirects Heine–Borel theorem]]
[[!redirects Heine–Borel theorems]]
