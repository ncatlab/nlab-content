

> This entry is about domains in [[domain theory]]. For other uses, see at _[[domain]]_. 

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# DCPOs
* table of contents
{: toc}

## Idea

A *directed-complete partial order* (DCPO), is a [[poset]] with all [[directed joins]].  Often a DCPO is required to have a [[bottom element]] $\bot$; then it is called a *[[pointed object|pointed]] DCPO* or a *CPO* (but this term is ambiguous).

The [[morphisms]] between DCPOs preserve the directed joins; equivalently, they are [[Scott continuity|Scott-continuous]].  Morphisms between pointed DCPOs may or may not be required to preserve $\bot$, depending on the application.

In [[domain theory]], a DCPO $P$ is interpreted as a [[type]] (in the sense of [[programming languages]], cf. *[[data type]]*), and its [[elements]] are possible partial (in the sense of a [[partial function]]) results of a [[computation]].  The [[bottom element]] (if there is one) indicates that no result has been obtained; if $x \leq y$ in $P$, then $x$ consists of part of the information in $y$.  A [[directed set|directed subset]] $D$ of $P$ indicates a collection of partial results which are mutually consistent, since for any two results $x, y \in D$, there is a partial result that subsumes them both.  The required join of $D$ is then a partial result encoding the same information as $D$ itself.


## Definitions

Recall that a [[poset]] $P$ consists of a collection of [[elements]] equipped with a [[binary relation]] $\leq$ such that $x \leq x$ always and $x \leq z$ whenever $x \leq y$ and $y \leq z$; we also consider $x$ and $y$ to be equal whenever $x \leq y$ and $y \leq x$.

Recall that a [[subset]] $D$ of $P$ is [[directed set|semidirected]] iff, whenever $x, y \in D$, there is some $z \in D$ such that $x \leq z$ and $y \leq z$.  Then $D$ is directed iff it is semidirected and [[inhabited subset|inhabited]].

Recall that an [[upper bound]] of a subset $D$ of $P$ is an element $x$ such that $y \leq x$ whenever $y \in D$, and a [[join]] of $D$ is an upper bound $x$ such that $x \leq y$ whenever $y$ is an upper bound of $D$.  The join of $D$, if one exists, is unique, and we write it $\bigvee D$ (or even put a little arrow on the right flank of the symbol when $D$ is directed).  A [[bottom element]] is a join of the [[empty subset]].

\begin{definition}
\label{TheDefinition}
A **directed-complete partial order** (*DCPO*) or _predomain_ is a [[poset]] in which every [[directed set|directed]] [[subset]] has a [[join]].  

A _pointed DCPO_ or **complete partial order** (*CPO*) (or _inductive partial order_ (*IPO*) or _semidirected-complete partial order_ or _domain_ or *lift algebra*) is a DCPO with a [[bottom element]], equivalently a poset in which every semidirected subset has a join.
\end{definition}


## Properties

### The Scott topology

Every poset $P$ becomes a [[topological space]] under the [[Scott topology]], but this is particularly nice for DCPOs, so we review it.

A [[subset]] $A$ of a DCPO is Scott-[[open subset|open]] iff it's an [[upper subset]] and any directed subset of $P$ whose join belongs to $A$ must meet $A$; it\'s Scott-[[closed subset|closed]] iff it is a [[lower subset]] that is directed-complete in its own right.

The [[specialisation order]] of the Scott topology of a DCPO is its original order (but the Scott topology is finer than the [[specialisation topology]]).

## Related entries

* [[omega-complete poset]]

* [[domain theory]]

* [[continuous lattice]]


## References ##

See the references at *[[domain theory]]*.

See also: 

* Wikipedia, *[Scott domain](https://en.wikipedia.org/wiki/Scott_domain)*

* Wikipeida, *[Domain theory](https://en.wikipedia.org/wiki/Domain_theory)*

* D.J. Lehmann, M.B., Smyth, *Algebraic specification of data types: A synthetic approach*,  Math. Systems Theory **14** (1981) 97–139 &lbrack;[doi:10.1007/BF01752392](https://doi.org/10.1007/BF01752392)&rbrack;

Discussion in [[homotopy type theory]]/[[univalent foundations]]:

* [[Benedikt Ahrens]], [[Paige Randall North]], [[Michael Shulman]], [[Dimitris Tsementzis]], *The Univalence Principle* ([abs:2102.06275](https://arxiv.org/abs/2102.06275))

* [[Simcha van Collem]], [[Niels van der Weide]], [[Herman Geuvers]], *Initial Algebras of Domains via Quotient Inductive-Inductive Types* &lbrack;[arXiv:2509.10187](https://arxiv.org/abs/2509.10187)&rbrack;

Generalization to the context of [[quantum computation]] (via [[quantum sets]] carrying [[quantum relations]] providing [[categorical semantics]] for [[quantum programming languages]] like [[Quipper]] equipped with type recursion):

* [[Andre Kornell]], [[Bert Lindenhovius]], [[Michael Mislove]], *Quantum CPOs*, EPTCS **340** (2021) 174-187 &lbrack;[arXiv:2109.02196](https://arxiv.org/abs/2109.02196), [doi:10.4204/EPTCS.340.9](https://doi.org/10.4204/EPTCS.340.9)&rbrack;



[[!redirects dcpos]]
[[!redirects dcpo's]]

[[!redirects DCPO]]
[[!redirects DCPOs]]
[[!redirects DCPO's]]

[[!redirects directed-complete partial order]]
[[!redirects directed-complete partial orders]]
[[!redirects directed complete partial order]]
[[!redirects directed complete partial orders]]

[[!redirects directed-complete poset]]
[[!redirects directed-complete posets]]
[[!redirects directed complete poset]]
[[!redirects directed complete posetss]]

[[!redirects pointed dcpo]]
[[!redirects pointed dcpo's]]
[[!redirects pointed dcpos]]
[[!redirects pointed DCPO]]
[[!redirects pointed DCPO's]]
[[!redirects pointed DCPOs]]

[[!redirects pointed directed-complete partial order]]
[[!redirects pointed directed-complete partial orders]]
[[!redirects pointed directed complete partial order]]
[[!redirects pointed directed complete partial orders]]

[[!redirects pointed directed-complete poset]]
[[!redirects pointed directed-complete posets]]
[[!redirects pointed directed complete poset]]
[[!redirects pointed directed complete posetss]]

[[!redirects cpo]]
[[!redirects cpo's]]
[[!redirects cpos]]
[[!redirects CPO]]
[[!redirects CPO's]]
[[!redirects CPOs]]
[[!redirects complete partial order]]
[[!redirects complete partial orders]]

[[!redirects lift algebra]]
[[!redirects lift algebras]]

[[!redirects Scott domain]]
[[!redirects Scott domains]]


[[!redirects quantum CPO]]
[[!redirects quantum CPOs]]


