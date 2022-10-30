
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
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


## Logical status

In the old days, one called a closed and bounded [[interval]] in the [[real line]] 'compact'; once closedness and boundedness were generalised from intervals to arbitrary [[subsets]] (of the real line), the definition of 'compact' also generalised.  The content of Theorem \ref{classical}, then, is that this condition is equivalent to the modern definition of 'compact' using [[open covers]], and indeed the modern definition was only derived afterwards as a name for the conclusion of the theorem.

In [[constructive mathematics]], one sees several definitions of 'compact', which may make the theorem provable, refutable, or undecidable in various constructive systems.  Using the open-cover definition of 'compact', Theorems \ref{classical} and \ref{cartesian} are equivalent to the [[fan theorem]] (and so hold in [[intuitionism]]), but Theorems \ref{metric} and \ref{uniform} are stronger and [[Jan Brouwer|Brouwer]] could not prove them, leading him to *define* 'compact' (for a metric space) to mean complete and totally bounded.  In other literature, one sometimes sees the abbreviation 'CTB' used instead.  In [[Russian constructivism]], already Theorems \ref{classical} and \ref{cartesian} can be refuted using the open-cover definition, but CTB spaces are still important.

In [[locale theory]] and other approaches to [[pointless topology]], the open-cover definition of 'compact' is clearly correct, and the failure of CTB spaces to be compact (constructively) may be seen as a consequence of working with points.  Already in Bishop\'s weak system of constructivism, every CTB metric space $X$ gives rise to a compact locale, which classically (assuming [[excluded middle]] and [[dependent choice]]) is the [[locale of open subsets]] of $X$ but constructively requires a more nuanced construction; see [Vickers](#CTBlocale).


## References

[According to Wikipedia](https://en.wikipedia.org/wiki/Heine%E2%80%93Borel_theorem#History_and_motivation), the theorem was first proved by [[Pierre Cousin]] in 1895.  It is named after [[Eduard Heine]] (who used it but did not prove it) and [[Émile Borel]] (who proved a limited version of it), an instance of [[Baez's law]].

A proof is spelled out for instance at

* [ProofWiki](http://www.proofwiki.org/wiki/Main_Page),  _Heine-Borel Theorem [(General case)](http://www.proofwiki.org/wiki/Heine-Borel_Theorem_%28General_Case%29),  [(Special case)](http://www.proofwiki.org/wiki/Heine-Borel_Theorem_%28Special_Case%29)_

On constructing a compact locale from a CTB metric space:

*  [[Steve Vickers]], [Localic completion of generalized metric spaces](http://www.tac.mta.ca/tac/volumes/14/15/14-15abs.html)
   {#CTBlocale}


[[!redirects Heine-Borel theorem]]
[[!redirects Heine-Borel theorems]]
[[!redirects Heine--Borel theorem]]
[[!redirects Heine--Borel theorems]]
[[!redirects Heine–Borel theorem]]
[[!redirects Heine–Borel theorems]]
