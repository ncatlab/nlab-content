
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

A _real number_ is a [[number]] that may be [[Dedekind completion|approximated]] by [[rational numbers]].  Equipped with the operations of [[addition]] and [[multiplication]] induced from the rational numbers, real numbers form a _[[field]]_, commonly denoted _$\mathbb{R}$_. The underlying set is the _[[Dedekind completion|completion]]_ of the [[ordered field]] $\mathbb{Q}$ of rational numbers: the result of adjoining to $\mathbb{Q}$ [[suprema]] for every [[inhabited set|inhabited]] [[bounded set|bounded subset]] with respect to the natural [[order|ordering]] of rational numbers.

The [[set]] of real numbers also carries naturally the [[mathematical structure|structure]] of a [[topological space]] and as such $\mathbb{R}$ is called the  _[[real line]]_ also known as _[[continuum|the continuum]]_. Equipped with both the topology and the field structure, $\mathbb{R}$ is a [[topological field]] and as such is the [[complete space|uniform completion]] of $\mathbb{Q}$ equipped with the [[absolute value]] [[metric space|metric]].

Together with its [[cartesian products]] -- the [[Cartesian spaces]] $\mathbb{R}^n$ for [[natural numbers]] $n \in \mathbb{N}$ -- the real line $\mathbb{R}$ is a standard formalization of the idea of _continuous space_.  The more general concept of ([[smooth manifold|smooth]]) _[[manifold]]_ is modeled on these Cartesian spaces. These, in turn are standard models for the notion of [[space]] in particular in [[physics]] (see _[[spacetime]]_), or at least in [[classical physics]]. See at _[[geometry of physics]]_ for more on this.


## History

The original idea of a real number came from [[geometry]]; one thinks of a real number as specifying a _point on a line_, with _[[line]]_ understood as the abstract idea of the object that a pencil and a ruler draw on a piece of paper.  (More precisely, given two distinct points on the line, called $0$ and $1$, you get a [[bijection]] between the points and the real numbers.)

[[Euclid]] (citing [[Eudoxus]]) dealt with ratios of geometric magnitudes, which give positive real numbers; an arbitrary real number is then a difference of ratios of magnitudes.  However, the Greeks did not think of such ratios as [[number]]s; that appears to have been an insight of the Arabs.  See more at [[Eudoxus real number]]. 

A big project of the 19th century (at least in hindsight) was the 'arithmetisation of analysis': showing how real numbers could be defined completely in terms of rational numbers (and the desired classes of functions on them could be defined in terms of the general point-set notion of [[function]]).  Two successful approaches were developed in 1872, [[Richard Dedekind]]\'s definition of real numbers as certain sets of rational numbers (called _[[Dedekind cuts]]_) and [[Georg Cantor]]\'s definition as certain sequences of rational numbers (called _[[Cauchy sequences]]_).

A more modern approach is instead to characterise the properties that the set of real numbers must have and to prove that this is [[generalized the|categorical]] (unique up to a unique bijection preserving those properties).  Then the important result of the 19th-century programme is simply that this is consistent (that there exists at least one such set).  One can even use [[David Hilbert|Hilbert]]\'s or [[Alfred Tarski|Tarski]]\'s axioms for geometry to do this characterisation, coming full circle back to geometry.

Exactly how to define or characterise real numbers is still important in [[constructive mathematics]] and [[topos theory]] with its [[internal logic]].  For more on this, see [[real numbers object]] and the examples below.


## Definitions and characterizations

There are two basic approaches possible: to define what a __real number__ is as a mathematical object, or to define the __real line__ as a specific object in some previously known [[category]].


### Dedekind cuts {#Dedekind}

Consider two [[inhabited set|inhabited]] subsets, $L$ and $U$, of a [[countable set|countable]] unbounded [[dense linear order]], such as $\mathbb{Q}$ (the set of [[rational numbers]]) or  $\mathbb{Z}[1/10]$ (the set of [[decimal fractions]]), such that:

*  If $a \in L$, then $b \in L$ for some $b \gt a$.
*  If $b \in U$, then $a \in U$ for some $a \lt b$.
*  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.  (\*)
*  If $a \in L$ and $b \in U$, then $a \lt b$.

We may define a __Dedekind real number__ to be such a pair, which is also called a __[[Dedekind cut]]__.

If $x \coloneqq (L,U)$ is a Dedekind cut, then we write $a \lt x$ to mean that $a \in L$ and $x \lt b$ to mean that $b \in U$.

We may approximate a Dedekind cut $x$ as closely as we like by applying (\*) as often as necessary.  This will be only finitely often, for any fixed positive level of approximation, given initial upper and lower bounds (which exist since $L$ and $U$ are inhabited).

See [[Dedekind completion]] for more.


### Cauchy sequences

Classically, a real number can be given by an [[infinite sequence|infinite]] [[Cauchy sequence]] of [[decimal fractions]] $\mathbb{Z}[1/10]$, each of which is a decimal fraction that approximates the real number to a given number of decimal places. However, many real numbers have several representations, i.e. 

  $$1/10 = 0.099999... = 0.10000...$$

so we need to specify an [[equivalence relation]] on the Cauchy sequences.  Thus, $\mathbb{R}$ is constructed as a [[subquotient]] of the [[function set]] $\mathbb{Z}[1/10]^{\mathbb{N}}$.

We can generalise this to any [[Cauchy sequence]] of rational numbers, and $\mathbb{R}$ is constructed as a [[subquotient]] of the [[function set]] $\mathbb{Q}^{\mathbb{N}}$.

This construction is equivalent to the construction by Dedekind cuts, at least assuming [[weak countable choice]] (which also follows from [[excluded middle]]).  Thus it is popular in both [[classical mathematics]] and traditional [[constructive mathematics]] (which accepts [[countable choice]]).  However, in stricter forms of constructive mathematics, including those used as [[internal languages]] in [[topos theory]], the Cauchy reals and Dedekind reals are not equivalent.  (On the other hand, by generalising to Cauchy [[nets]], we recover the Dedekind reals again.)

See [[Cauchy real number]] for more.

### The complete ordered field

There is a well-known algebraic (more or less) characterisation of the real line as the 'complete ordered field', or sometimes the 'complete archimedean field'.  This can be interpreted as follows:

*  A __field__ is well known in algebra; if it matters, we mean a [[Heyting field]].
*  An __ordered field__ means a *[[linear order|linearly]]* ordered field.
*  An __archimedean field__ is an ordered field satisfying the [[archimedean property]].
*  An ordered field is __complete__ if it is [[Dedekind completion|Dedekind-complete]].
*  Alternatively, an archimedean field is __complete__ if it is [[terminal object|terminal]] in the category of archimedean fields.

We speak of [[the]] such field because it is unique up to unique [[isomorphism]].

+-- {: .un_theorem}
###### Theorem

There is an archimedean field $\mathbb{R}$ which is both Dedekind-complete and terminal among archimedean fields.  Furthermore, every Dedekind-complete ordered field is isomorphic to $\mathbb{R}$.  (By [[abstract nonsense]], we already know that every terminal archimedean field is isomorphic to $\mathbb{R}$ and that $\mathbb{R}$ has only the identity [[automorphism]], so isomorphisms to it are unique.)
=--

+-- {: .proof}
###### Proof

Construct $\mathbb{R}$ using, say, Dedekind cuts of rational numbers.  Then it is well known how to prove these facts about $\mathbb{R}$, so we omit the proof for now.
=--

However, we note that the proof is valid in weak [[foundations]], in particular internal to any [[topos]] with a [[natural numbers object]].  One can actually work in even weaker foundations than that; see the constructions at [[real numbers object]].  Even weaker foundations are possible if one allows the [[underlying set]] of $\mathbb{R}$ to be [[proper class|large]].

### The terminal archimedean group

There is a characterisation of the real line as the 'complete densely linearly ordered archimedean group'. This can be interpreted as follows:

*  An __abelian group__ is well known in algebra.
*  An __linearly ordered abelian group__ is an [[abelian group]] with a [[linear order]].
*  An __archimedean group__ is a linearly ordered abelian grouo satisfying the [[archimedean property]].
*  A __dense linear ordered archimedean group__ is an archimedean group that is also a [[dense linear order]]. 
* A densely linearly ordered archimedean group is __complete__ if it is [[Dedekind completion|Dedekind-complete]].
* Alternatively, an archimedean group is __terminal__ if it is the terminal object in the category of archimedean groups. 

Tarski's axioms for one-dimensional Euclidean geometry results in a complete densely linearly ordered archimedean group. 

### The locale of real numbers

Consider [[binary relations]] $\sim$ on a [[countable]] [[inhabited]] [[dense linear order]] without endpoints, such as the [[rational numbers]], satisfying these four properties:

*  If $a \geq b$, then $a \sim b$.
*  If $a \geq b \sim c \geq d$, then $a \sim d$.
*  If $a \sim b \gt c \sim d$, then $a \sim d$.
*  If $b \sim c$ whenever $a \lt b$ and $c \lt d$, then $a \sim d$.

The collection of all such relations form a [[frame]], which we may interpret (by definition) as the __[[locale of real numbers]]__.  It can also be defined as the [[localic completion]] of the rational numbers.

We may then define a __localic real number__ to be a [[point of a locale|point]] of this locale.

This agrees with the notion of Dedekind real number, even in very weak ([[predicative mathematics|predicative]] and [[constructive mathematics|constructive]]) [[foundations]].

See [[locale of real numbers]] for more.

### Unit intervals

The [[coalgebra of the real interval|unit interval]] of the real numbers $[0,1]$ could be constructed as a [[terminal coalgebra of an endofunctor]] in the [[category]] of [[intervals]]. Let $(\mathbb{R},0,+,-,1,\lt)$ be a [[linear order|linearly ordered]] [[abelian group]] where $0 \lt 1$, with a [[monotone]] $f:[0,1]\to \mathbb{R}$ such that $f(0) = 0$ and $f(1) = 1$. The set $\mathbb{R}$ of real numbers is the initial such ordered group. 

### $\mathbb{R}^+$ as a terminal coalgebra

The positive real line $\mathbb{R}^+$ may be characterized as the [[terminal object|terminal]] [[coalgebra for an endofunctor]]

Let [[Pos]] be the [[category]] of [[poset]]s with a [[forgetful functor]]

$$ 
  U\colon Pos \to Set
$$

Consider the endofunctor

$$
  F_1\colon Pos \to Pos
$$

defined as the [[ordinal product]]

$$
  F_1\colon X \mapsto \omega \cdot X,
$$ 
for $\omega \in Pos$, where $\omega \cdot X$ is the [[cartesian product]] $U(\omega) \times U(X)$ with the [[lexicographic order]]. 

+-- {: .un_prop}
###### Proposition

The terminal coalgebra of $F_1$ is order isomorphic to the non-negative real line $\mathbb{R}^+$, with its standard order.
=--

+-- {: .proof}
###### Proof

This is theorem 5.1 in ([Pavlovic–Pratt 1999](#PavlovicPratt)).

There are many ways of setting up this description of $\mathbb{R}^+$, depending on the coalgebra structure $\mathbb{R}^+ \to \omega \cdot \mathbb{R}^+$ chosen. Here is one: there are evident poset isomorphisms $\mathbb{R}^+ \cong [1, \infty)$ and $\omega \cong \mathbb{N}_{\geq 2} = \{n \in \mathbb{N}: n \geq 2\}$. Define a map 

$$(\alpha, \beta): [1, \infty) \to \mathbb{N}_{\geq 2} \cdot [1, \infty)$$ 

where $\alpha(x)$ is the smallest integer strictly greater than $x$, and $\beta(x) = 1/(\alpha(x) - x)$. The stream of integers $a_n = \alpha(\beta^n(x))$ gives a [[continued fraction]] representation of $x$ in the form

$$x = a_0 - \frac1{a_1 - \frac1{a_2 - \ldots}},$$ 

and the resulting bijection $[1, \infty) \to \mathbb{N}_{\geq 2} \times \mathbb{N}_{\geq 2} \times \ldots$, sending $x$ to $(a_0, a_1, \ldots)$, is in fact a poset isomorphism if we endow the right-hand side with the lexicographic order. 
=-- 

Another way, which circumvents the use of isomorphisms $\mathbb{R}^+ \cong [1, \infty)$ and $\omega \cong \mathbb{N}_{\geq 2}$, is to define 

$$(\alpha, \beta): \mathbb{R}^+ \to \omega \cdot \mathbb{R}^+$$ 

where $\alpha(x)$ is the floor of $x$, and $\beta(x) = 1/(1 - x + \alpha(x)) - 1$. Then $a_n = \alpha(\beta^n(x))$ gives a [[continued fraction]] representation of $x$ in the form 

$$x = a_0 + \frac1{1 + \frac1{a_1 + \frac1{1 + \frac1{a_2 + \ldots}}}},$$ 
and the resulting [[bijection]] $\mathbb{R}_+ \to \omega \times \omega \times \ldots$, sending $x$ to $(a_0, a_1, \ldots)$, is again a poset isomorphism if we endow the right-hand side with the lexicographic order.

There are more and similar characterizations along these lines. 

## Topologies
{#Topologies}

There are alternative topologies on $\mathbb{R}$ sometimes considered:

* the [[discrete topology]] (not very interesting),
* the [[order topology]] or [[absolute-value topology]] (the usual topology of a [[Euclidean space|Euclidean]] [[metric space]]),
* the [[upper-interval topology]] or the [[lower-interval topology]],
* the [[lower semicontinuous topology]] or the [[upper semicontinuous topology]],
* the [[K-topology]].

Another variant of $\mathbb{R}$ as a topological space is the

* [[long line]].


## Generalisations

The term 'real number' was originally introduced to indicate that one is *not* considering the generalistion to [[complex numbers]] or other kinds of [[hypercomplex numbers]].  Accordingly, that term 'real' may sometimes be used for another generalisation of real numbers to indicate again that one is not considering a complexification.

The [[extended real number]]s include $\pm\infty$ as well as the real numbers; one may speak of _finite numbers_ or _bounded numbers_ to indicate that one is not considering this extension.  [[lower real|Lower reals]], [[upper reals]], and [[MacNeille real number|MacNeille reals]] are related generalisations studied in [[constructive mathematics]], although with [[excluded middle]] they are (at least if bounded) the same as ordinary real numbers; one may speak of _located numbers_ to indicate that one is not considering such extensions.

[[surreal number|Surreal numbers]] and the [[hyperreal number]]s of [[nonstandard analysis]] are two ways to include [[infinite number|infinite]] and [[infinitesimal number|infinitesimal]] versions of real numbers (besides the trivial case of $\pm\infty$); one may speak of _standard numbers_ to indicate that one is not considering such extensions (although the precise meaning of 'standard' depends on the [[universe]] that one is working in).

In [[descriptive set theory]], one often says 'real number' for an element of [[Baire space of irrational numbers|Baire space]] $\mathbb{N}^{\mathbb{N}}$.  This is not really a generalisation; by the [[Schroeder-Bernstein theorem]], the underlying sets of $\mathbb{R}$ and $\mathbb{N}^{\mathbb{N}}$ are [[bijection|isomorphic]].  Constructively, $\mathbb{N}^{\mathbb{N}}$ can still be thought of as the set of [[irrational numbers]], so this use of the term may actually be a *restriction*.

[[floating-point number|Floating-point numbers]] are often used in computer programming to represent real numbers, but they do not behave very well; one may speak of _infinite-precision numbers_ to indicate that one\'s programming environment models '[*real* real numbers](http://math.fau.edu/richman/html/mm2.htm)'.

As mentioned above, the $p$-[[adic number|adic numbers]] for various [[prime numbers]] $p$ are variations on the theme of real numbers; real numbers may be thought of as _$0$-adic numbers_.  Similarly, the real numbers are _characteristic-$0$ numbers_ since they are based on the [[prime field]] $\mathbb{Q}$; one could also start the construction with a different [[characteristic]] (although it makes more sense to get analogues of complex numbers than of real numbers).

Finally, one can consider points on a [[noncommutative geometry|noncommutative]] line instead of the usual _commutative numbers_.

So in summary, this page is about the _real, finite, located, standard, analytic, infinite-precision, $0$-adic, characteristic-$0$, commutative numbers_.

## Related concepts

* [[real numbers object]]

* [[computable real number]]

* [[p-adic numbers]]

* in [[constructive analysis]] one may use the [[completion monad]] for dealing with real numbers

* [[exact real computer arithmetic]]

[[!include exceptional spinors and division algebras -- table]]


## References

A formalization of the real numbers in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], chapter 11 of _[[Homotopy Type Theory – Univalent Foundations of Mathematics]]_

* Ga&#235;tan Gilbert, _Formalising Real Numbers in Homotopy Type Theory_ ([arXiv:1610.05072](https://arxiv.org/abs/1610.05072))

For more see the references at _[[analysis]]_.

* {#PavlovicPratt} [[Dusko Pavlovic]], [[Vaughan Pratt]], _On coalgebra of real numbers_, Electronic Notes in Theoretical Computer Science **19** (1999) 103-117, doi:[10.1016/S1571-0661(05)80272-5](https://doi.org/10.1016/S1571-0661%2805%2980272-5), [CiteSeerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204)
 
[[!redirects real number]]
[[!redirects real numbers]]

[[!redirects real line]]
[[!redirects real number line]]
[[!redirects the continuum]]

[[!redirects located real number]]
[[!redirects located real numbers]]
[[!redirects located Dedekind real number]]
[[!redirects located Dedekind real numbers]]
