\tableofcontents

\section{Introduction}

A _finite set_ is, roughly speaking, a [[set]] with only finitely many [[element|elements]]. There are a number of ways to make this precise. 

Classically, the finite sets are the [[finitely presentable object|finitely presentable objects]] in [[Set]]. Constructively, the same is true if _finitely presented_ is properly interpreted, see there for details.

The category [[FinSet]] of finite sets and functions between them is a prime example of an [[elementary topos]] which is not a [[Grothendieck topos]]. It is essentially the subject matter of [[combinatorics]]; it is fundamental in the subject of [[structure types]].

\section{Definitions}

\subsection{Standard definition}

We can for example make the following definition.

\begin{defn} A **finite set** is a [[set]] $A$ for which there exists a [[bijection]] between $A$ and the set $[n] \coloneqq \{k\in \mathbb{N} | k\lt n\}$ for some $n\in \mathbb{N}$, where $\mathbb{N}$ is the [[natural number|natural numbers]]. \end{defn}

\subsection{Finiteness constructively and internally}
{#Constructivist}

\subsubsection{Variations}

In [[constructive mathematics]], and internally to a [[topos]], a number of classically equivalent notions of finiteness become distinguishable:

* A set is **[[finite]]** (for emphasis __Bishop-finite__ or __$B$-finite__) if (as above) it admits a [[bijection]] with $[n]$ for some [[natural number]] $n$.

* A set is **[[subfinite]]** (or __$\tilde{B}$-finite__) if it admits an [[injection]] into some finite set $[n]$; that is, it is a [[subset]] of a finite set.

* A set is **finitely indexed** (or **[[Kuratowski-finite]]**, **$K$-finite**, or even sometimes, confusingly, _subfinite_) if it admits a [[surjection]] from some finite set $[n]$; that is, it is a [[quotient set]] of a finite set.

* A set is **subfinitely indexed** (or __[[Kuratowski-subfinite]]__ or **$\tilde{K}$-finite**) if it admits a surjection from a subfinite set, or equivalently admits an injection to a finitely indexed set; that is, it is a [[subquotient set]] of a finite set.

* A set $X$ is **[[Dedekind-finite]]** if it satisfies one of the following:

  * any [[injection]] $X\hookrightarrow X$ must be a [[bijection]].
  * for any function $f\colon \mathbb{N} \to X$ from the [[natural numbers]], there exist $n,m$ with $n \ne m$ such that $f(n) = f(m)$.

  In contrast to the previous three notions, Dedekind-finite [[infinite sets]] can coexist with [[excluded middle|PEM]], although [[countable choice]] suffices to banish them.  The above two versions of Dedekind-finiteness are equivalent under PEM, but constructively they may differ.

In constructive mathematics, one is usually interested in the finite sets, although the finitely indexed sets are also sometimes useful, as are the Dedekind-finite sets in the second sense.

\subsubsection{Properties and relationships}

Of course, we have

$$
\array{ & & finitely\;indexed\\
  & \neArrow & & \seArrow\\
  finite & & & & subfinitely\;indexed\\
  & \seArrow & & \neArrow\\
  & & subfinite }
$$

Moreover:

* Finite and subfinite sets have [[decidable equality]].  Conversely, any [[complement|complemented]] subset of a finite set is finite.

* Finite sets are closed under finite limits and colimits.

* A finitely indexed set with decidable equality must actually be finite.  For it is then the quotient of a decidable equivalence relation, hence a coequalizer of finite sets.  In particular, a set which is both finitely indexed and subfinite must be finite, i.e. the above "commutative square" of implications is also a "pullback".

* Finite sets are always [[projective object|projective]]; that is, the "finite [[axiom of choice]]" always holds.

* However, if a finite set with $2$ elements (or any set, finite or not, with at least $2$ distinct elements) is [[choice object|choice]], or if every finitely-indexed set (or even any $2$-indexed set) is projective, then the logic must be classical (see [[excluded middle]] for a proof).

* Finite sets are also Dedekind-finite (in either sense).

* If _[[filtered category]]_ means _admitting cocones of every Bishop-finite diagram_, then a set is Bishop-finite iff it is a [[compact object|finitely presented object]] in Set and it is Kuratowski-finite iff it is a [[finitely generated object]] in Set.

\subsubsection{Finiteness without infinity}
{#Finitist}

All of the above definitions except for Dedekind-finiteness only make sense given the set of natural numbers, i.e., given an axiom of infinity.  However, they can all be rephrased to make sense even without an axiom of infinity (and thus in a topos without a [[natural numbers object]]).  Basically, you define (for a given set $S$) the concept of 'collection of subsets of $S$ that includes all of the finite subsets' by requiring it to be closed under inductive operations appropriate for the sense of 'finite' that you want; then $S$ is finite if and only if it is an element of all such collections.  Namely, for any set $S$ we define the following subsets of the [[power set]] $P(S)$.

* $K(S)$ is the smallest subset of $P(S)$ containing the empty set and closed under the operation $A \mapsto A \cup B$ for $A$ a subset of $S$ and $B$ a [[singleton]] in $S$.  Then $S$ is finitely-indexed iff $S \in K(S)$.  Note that $K(S)$ is also the free [[semilattice]] generated by $S$.
* $\tilde{K}(S)$ is the smallest subset of $P(S)$ containing the empty set and closed under the operation $A \mapsto A \cup B$ for $A$ a subset of $S$ and $B$ a [[subsingleton]] in $S$.  Then $S$ is subfinitely-indexed iff $S \in \tilde{K}(S)$.
* $B(S)$ is the smallest subset of $P(S)$ containing the empty set and closed under the operation $A \mapsto A \cup B$ for $A$ a subset of $S$ and $B$ a singleton in $S$ [[disjoint sets|disjoint]] from $A$.  Then $S$ is finite iff $S \in B(S)$.
* $\tilde{B}(S)$ is the smallest subset of $P(S)$ containing the empty set and closed under the operation $A \mapsto A \cup B$ for $A$ a subset of $S$ and $B$ a subsingleton in $S$ disjoint from $A$.  Then $S$ is subfinite iff $S \in \tilde{B}(S)$.

\subsubsection{Challenge: Finiteness predicatively without infinity}
{#Challenge}

Can you think of a way to define these notions of finite without power objects and without a natural numbers object? More specifically (and generously), can you define them in an arbitrary [[locally cartesian closed category|locally cartesian closed]] [[pretopos]] with [[enough projectives]]?

\subsection{In a topos}
{#External}

In a topos, there are both "external" and "internal" versions of all the above notions of finiteness, depending on whether we interpret their meaning "globally" or in the [[internal logic]] of the topos.  See [[finite object]].

\section{Properties of the category of finite sets}

The [[category]] [[FinSet]] of finite sets is [[equivalence of categories|equivalent]] to that of finite [[Boolean algebras]] by the [[power set]]-[[functor]]. See at _[FinSet -- Opposite category](FinSet#OppositeCategory)_ for details and see at _[[Stone duality]]_ for more.

\section{Viewing as schemes}

Every finite set can be viewed as an [[affine scheme]]. Indeed, given a finite set $X$, view it (as one can up to isomorphism, that is, [[bijection]]) as a set of [[integer|integers]] $\left\{ x_1, \ldots, x_n \right\}$. One can view $X$ as the set of zeroes of the set of [[polynomial|polynomials]] in one variable $y$ given by $\left\{ y - x_1, \ldots, y - x_n \right\}$, or of the single polynomial given by the product of all these. 

Thus one can view $X$ as the affine scheme (over $Spec(\mathbb{Z})$) given as the [[spectrum of a commutative ring|commutative ring spectrum]] $Spec\left( k[y] / I \right)$, where $I$ is the ideal generated by the afore-mentioned polynomial(s). One can view $X$ as a 'constant scheme' over any other base scheme $Y$ by [[base change]], that is, by means of the canonical [[projection]] morphism $Y \times X \to Y$.

\section{Related concepts}

* [[hereditarily finite set]]

* [[FinSet]]

* [[finite object]]

* the [[cardinality]] of a finite set is a [[finite number]]

* [[cofinite subset]]

* [[countable ordinal]]

* [[finite-dimensional vector space]]

* [[finite homotopy type]], 

  * [[finite CW-complex]], [[finite spectrum]]

* [[profinite set]]

* [[finite cover]]

* [[finite graph]]

* [[finite category]]

* [[space of finite subsets]]

\section{References}

* [[Kazimierz Kuratowski|C. Kuratowski]], _Sur la notion d'ensemble fini_ , Fund. Math. **I** (1920) pp.130-131. ([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm1/fm1117.pdf))

For a treatment in [[homotopy type theory]] see

* Dan Frumin, Herman Geuvers, Léon Gondelman, Niels van der Weide, _Finite Sets in Homotopy Type Theory_, ([pdf](http://cs.ru.nl/~nweide/FiniteSetsInHoTT.pdf))

See also

* Wikipedia, _[Finite set](https://en.wikipedia.org/wiki/Finite_set)_


[[!redirects finite set]]
[[!redirects finite sets]]
[[!redirects Bishop-finite set]]
[[!redirects Bishop-finite sets]]
[[!redirects Bishop-finite]]
[[!redirects Bishop finite set]]
[[!redirects Bishop finite sets]]
[[!redirects Bishop finite]]
[[!redirects B-finite set]]
[[!redirects B-finite sets]]
[[!redirects F-finite set]]
[[!redirects F-finite sets]]

[[!redirects subfinite set]]
[[!redirects subfinite sets]]
[[!redirects Bishop-subfinite set]]
[[!redirects Bishop-subfinite sets]]
[[!redirects Bishop-subfinite]]
[[!redirects Bishop subfinite set]]
[[!redirects Bishop subfinite sets]]
[[!redirects Bishop subfinite]]
[[!redirects B-tilde-finite set]]
[[!redirects B-tilde-finite sets]]
[[!redirects F-tilde-finite set]]
[[!redirects F-tilde-finite sets]]

[[!redirects finitely indexed set]]
[[!redirects finitely indexed sets]]
[[!redirects finitely-indexed set]]
[[!redirects finitely-indexed sets]]
[[!redirects Kuratowski-finite set]]
[[!redirects Kuratowski-finite sets]]
[[!redirects Kuratowski-finite]]
[[!redirects Kuratowski finite set]]
[[!redirects Kuratowski finite sets]]
[[!redirects K-finite set]]
[[!redirects K-finite sets]]

[[!redirects subfinitely indexed set]]
[[!redirects subfinitely indexed sets]]
[[!redirects subfinitely-indexed set]]
[[!redirects subfinitely-indexed sets]]
[[!redirects Kuratowski-subfinite set]]
[[!redirects Kuratowski-subfinite sets]]
[[!redirects Kuratowski subfinite set]]
[[!redirects Kuratowski subfinite sets]]
[[!redirects Kuratowski subfinite]]
[[!redirects K-tilde-finite set]]
[[!redirects K-tilde-finite sets]]

[[!redirects Dedekind-finite set]]
[[!redirects Dedekind-finite sets]]
[[!redirects Dedekind finite set]]
[[!redirects Dedekind finite sets]]
[[!redirects D-finite set]]
[[!redirects D-finite sets]]