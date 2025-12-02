
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--



\tableofcontents


## Idea

The _end compactification_ &lbrack;[Freudenthal 1931](#Freudenthal31)&rbrack; of a (sufficiently well-behaved) [[topological space]] adjoins one point for each [[connected component]] of its "ends at infinity" and thereby [[compactification|compactifies]] it into a [[compact topological space]].

Starting with a non-compact space, the further [[quotient space]] of the end-compactification by the subset of ends, identifying them all with one single "[[point at infinity]]", is called the *[[one-point compactification]]*.


## Definition

The definition of end compactification was originally given only for sufficiently [[nice topological space|nice]] topological spaces (the [[hemicompact space|hemicompact]] ones).  The general definition is a bit more complicated.  We will give three versions.


### For hemicompact spaces only

Let $X$ be a [[topological space]], and suppose that $X$ is [[hemicompact space|hemicompact]]; this means that there exists an [[infinite sequence]] $n \mapsto K_n$ of [[compact subspaces]] of $X$ with $K_n \subseteq K_{n+1}$ such that every compact subspace of $X$ is contained in at least one (hence in almost all) of the $K_i$.

Consider the [[connected components]] of the [[complements]] $X \setminus K_i$.  An __end__ of $X$ is an infinite sequence that chooses one such connected component for each $i$.  Remarkably, the set of ends is independent of the sequence $K$ chosen (up to [[natural bijection]]).

The __end compactification__ of $X$ has, as its [[underlying set]], the [[disjoint union]] of the underlying set of $X$ and the set of ends.  Its [[topological structure|topology]] is generated (from a [[topological base|base]]) by the topology of $X$ and, for each end $e = (U_1,U_2,\ldots)$, the [[open sets]] $V \cup \{e\}$ whenever $V$ is open in $X$ and $U_i \subseteq V$ for some (hence almost every) $i$.


### Abstract

Let $X$ be a [[topological space]], and consider the [[poset]] $Comp(X)$ of [[compact subspaces]] of $X$, ordered by [[inclusion]].  For each compact subspace $K$, consider its [[complement]] $X \setminus K$, and consider the [[set]] $\Pi_0(X \setminus K)$ of its [[connected components]].  For each inclusion $K \hookrightarrow K'$, we have a [[function]] $\Pi_0(X \setminus K') \to \Pi_0(X \setminus K)$.  This defines a [[contravariant functor]] from $Comp(X)$ to [[Set]]; its [[limit]] is the __set of ends__ of $X$.

For the [[topological structure|topology]], each compact subspace $K$ defines a topological space $K \uplus \Pi_0(X \setminus K)$; here, the points of $\Pi_0(X \setminus K)$ are all [[isolated point|isolated]].  For each inclusion $K \hookrightarrow K'$, we have a [[continuous map]] $K' \uplus \Pi_0(X \setminus K') \to K \uplus \Pi_0(X \setminus K)$; it sends $x$ to itself if $x \in K$, and $x$ to the connected component $[x] \in \Pi_0(X \setminus K)$ if $x \in K' \setminus K$.  This defines a [[contravariant functor]] from $Comp(X)$ to [[Top]]; its [[limit]] is the __end compactification__ of $X$.


### Concrete

Let $X$ be a [[topological space]].  An __end__ of $X$ assigns, to each [[compact subspace]] $K$ of $X$, a [[connected component]] $e_K$ of its [[complement]] $X \setminus K$, in such a way that $e_{K'} \subseteq e_K$ whenever $K \subseteq K'$.  The __end compactification__ of $X$ has, as its [[underlying set]], the [[disjoint union]] of the underlying set of $X$ and the set of ends.  Its [[topological structure|topology]] is generated (from a [[topological base|base]]) by the topology of $X$ and, for each end $e\colon K \mapsto e_K$, the [[open sets]] $V \cup \{e\}$ whenever $V$ is open in $X$ and $e_K \subseteq V$ for some compact subspace $K$.


## Examples

\begin{example}
A [[compact space]] has no ends, hence is its own end compactification.  The converse (that a space with no ends must be compact) seems to require the [[axiom of choice]] (although [[excluded middle]] and [[dependent choice]] suffice for hemicompact spaces).
\end{example}

\begin{example}
The end compactification of the [[real line]], whose ends are $\pm \infty$, is the [[extended real number]], [[homeomorphism|homeomorphic]] to the [[closed interval]] $[-1,+1]$. 
\end{example}

\begin{example}
But the [[complex plane]] has only one end; its end compactification is the [[Riemann sphere]] (the same as its [[one-point compactification]]).
\end{example}


## Applications

Ends are important in [[proper homotopy theory]]. 

According to [Peschke 1990](#Peschke90), [Freudenthal 1931](#Freudenthal31) was led to his theory of ends by the following observation. For a space $X$, consider a path-connected family $F \subseteq Homeo(X)$ containing the identity $1_X$. Let $K \subseteq X$ be compact, and let $U$ be a connected component of $X \setminus K$. Then for all $f \in F$, it may be shown $f(U) \setminus U$ is contained in a compact subset of $X$. The upshot is that $f$ extends to a homeomorphism on the end compactification that is *pointwise fixed* on the ends. If in addition for each pair $(x, y) \in X^2$ there is $f \in F$ with $f(x) = y$, then there is a severe constraint on the ends; in particular Freudenthal showed the following. 

\begin{proposition}

A path-connected topological group has at most two ends. 

\end{proposition}

For example, it follows that the space obtained by removing two points from $\mathbb{R}^3$ cannot be given a topological group structure. 

## Related concepts

* [[compactification]]

  * [[One-point compactification]]

  * [[Stone–Cech compactification]]

  * [[Bohr compactification]]


## References

The original articles:

* {#Freudenthal31} [[Hans Freudenthal]], _Über die Enden topologischer Räume und Gruppen_, Mathematische Zeitschrift **33** (1931) 692-713 &lbrack;[doi:10.1007/BF01174375](https://doi.org/10.1007/BF01174375), [pdf](http://dspace.library.uu.nl/bitstream/handle/1874/7437/1930-freudenthal-dissertatie.pdf?sequence=1)&rbrack;

* [[Hans Freudenthal]], *Neuaufbau der Endentheorie*, Annals of Mathematics Second Series **43** 2 (1942) 261-279 &lbrack;[doi:10.2307/1968869](https://doi.org/10.2307/1968869), [jstor:1968869](https://www.jstor.org/stable/1968869)&rbrack;

* [[Hans Freudenthal]], *Über die Enden diskreter Räume und Gruppen*, Commentarii Mathematici Helvetici **17** (1944) 1–38 &lbrack;[doi:10.1007/BF02566233](https://doi.org/10.1007/BF02566233)&rbrack;


Review:

* {#Peschke90}  [[Georg Peschke]]: _The Theory of Ends_, Nieuw Archief voor Wiskunde **8** (1990) 1-12 &lbrack;[pdf](https://www.ualberta.ca/~gepe/pdf/Peschke_TheoryOfEnds.pdf), [[Peschke-Ends.pdf:file]]&rbrack; 

* Steve Alpern, V. S. Prasad: *Noncompact Manifolds and Ends*, chapter 14 in: *Typical Dynamics of Volume Preserving Homeomorphisms*, Cambridge University Press (2011) &lbrack;[ISBN:9780521172431](https://www.cambridge.org/ae/universitypress/subjects/mathematics/differential-and-integral-equations-dynamical-systems-and-co/typical-dynamics-volume-preserving-homeomorphisms?format=PB&isbn=9780521172431), [[AlpernPrasad-Ends.pdf:file]]&rbrack;

* William G. Bass, Jack S. Calcut: *Ends and end cohomology*, Expositiones Mathematicae **43** 5 (2025) 125692 &lbrack;[doi:10.1016/j.exmath.2025.125692](https://doi.org/10.1016/j.exmath.2025.125692), [pdf](https://isis2.cc.oberlin.edu/faculty/jcalcut/rec.pdf)&rbrack;

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/End_(topology)">End (topology)</a>*

Via [[nonstandard analysis]]:

* Matt Insall, Peter Loeb: *End Compactifications and General Compactifications*, Journal of Logic & Analysis **6** 7 (2014) 1–16 &lbrack;[jla:231/99](http://www.logicandanalysis.com/index.php/jla/article/view/231/99), [pdf](http://www.logicandanalysis.com/index.php/jla/article/download/231/99)&rbrack;

See also:
 
* *Isotopic homeomorphisms of surface induces same map on the space of ends* &lbrack;[MO:q/423463](https://mathoverflow.net/q/423463/381)&rbrack;

* {#Rashed2022} Hussain S. Rashed: *A Coarse Approach to the Freudenthal Compactification and Ends of Groups*, PhD thesis, Univerity of Tennessee (2022) &lbrack;[utk_graddiss:7138](https://trace.tennessee.edu/utk_graddiss/7138)&rbrack;


[[!redirects end compactification]]
[[!redirects end compactifications]]

[[!redirects topological end]]
[[!redirects topological ends]]

[[!redirects end of a topological space]]
[[!redirects ends of a topological space]]
[[!redirects ends of topological spaces]]
