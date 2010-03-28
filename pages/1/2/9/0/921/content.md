
#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

A **real number** is something that may be approximated by [[rational numbers]].  The real numbers form the **real line** $\mathbb{R}$, also known as the **continuum**, which is the corresponding completion of the set $\mathbb{Q}$ of rational numbers.

Here we are using the usual [[order|ordering]] of rational numbers; other ordings will give the $p$-[[adic number|adic numbers]] instead.

Together with its cartesian powers -- the [[cartesian spaces]] $\mathbb{R}^n$ -- the continuum encodes one basic idea of of _continuous space_.  The notion of (especially smooth) [[manifold]] is modeled on this notion.  It provides one of the basic models of [[space]], notably the standard model for _physical space_ and _time_ (see [[spacetime]]), at least in [[classical physics]].


### History of formalisations

The original idea of a real number came from [[geometry]]; one thinks of a real number as specifying a _point on a line_ , with _line_ understood as the abstract idea of the object that a pencil and a ruler draw on a piece of paper.  

(More precisely, given two distinct points on the line, called $0$ and $1$, you get a [[bijection]] between the points and the real numbers.)  [[Euclid]] (citing [[Eudoxus]]) dealt with ratios of geometric magnitudes, which give positive real numbers; an arbitrary real number is then a difference of ratios of magnitudes.  (But the Greeks did not think of such ratios as numbers.)

A big project of the 19th century (at least in hindsight) was the 'arithmetisation of analysis': showing how real numbers could be defined completely in terms of rational numbers (and the desired classes of functions on them could be defined in terms of the general point-set notion of [[function]]).  Two successful approaches were developed in 1872, [[Richard Dedekind]]\'s definition of real numbers as certain sets of rational numbers (called _[[Dedekind cuts]]_) and [[Georg Cantor]]\'s definition as certain sequences of rational numbers (called _[[Cauchy sequences]]_).

A more modern approach is instead to characterise the properties that the set of real numbers must have and to prove that this is [[generalized the|categorical]] (unique up to a unique bijection preserving those properties).  Then the important result of the 19th century programme is simply that this is consistent (that there exists at least one such set).  One can even use Hilbert\'s or Tarski\'s axioms for geometry to do this characterisation, coming full circle back to geometry.

Exactly how to define or characterise real numbers is still important in [[constructive mathematics]] and [[topos]] theory with its [[internal logic]] of every topos. For more on this see the examples below.


## Definitions and characterizations

There are two basic approaches possible: to define what a __real number__ is, as an general object, or to define the __real line__ is as a specific object in some previously known [[category]].


### Dedekind cuts

Consider two [[inhabited set|inhabited]] subsets, $L$ and $U$, of $\mathbb{Q}$ (the set of [[rational numbers]]) such that:

*  If $b \in L$, then $a \in L$ for some $a \lt b$.
*  If $a \in U$, then $b \in U$ for some $a \lt b$.
*  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.  (\*)
*  If $a \in L$ and $b \in U$, then $a \lt b$.

We may define a __Dedekind real number__ to be such a pair, which is also called a __[[Dedekind cut]]__.

If $x \coloneqq (L,U)$ is a Dedekind cut, then we write $a \lt x$ to mean that $a \in L$ and $x \lt b$ to mean that $b \in U$.  Then we may approximate $x$ as closely as we like by applying (\*) as often as necessary (which will be only finitely often, for any fixed positive level of approximation, given initial upper and lower bounds since $L$ and $U$ are inhabited).

See [[Dedekind cut]] for more.


### Cauchy sequences

(Probably most of this should be moved to [[Cauchy real number]], with only a paragraph or so left here.)

Consider an [[infinite sequence]] of $(x_1,x_2,x_3,\ldots)$ of [[rational numbers]] such that
$$ {|x_i - x_j|} \lt 1/i + 1/j $$
always holds.  Then we may interpret each $x_i$ as a rational number within $1/i$ of the true value of some real number $x$.  Two such sequences $x,y$ are considered [[equivalence|equivalent]] if
$$ {|x_i - y_j|} \lt 1/i + 1/j $$
always holds; then they represent the same real number.  Up to this equivalence, we can demand that the denominator of $x_i$ is always $i$ (or a factor of $i$), so that $x_i$ is $x$ rounded up or down to the nearest such rational number (in the chosen direction).

Similarly, consider an infinite sequence $(x_0,x_1,x_2,\ldots)$ of rational numbers such that
$$ {|x_i - x_j|} \lt 1/2^i + 1/2^j $$
always holds.  Then we may interpret each $x_i$ as a rational number within $1/10^i$ of the true value of some real number $x$.  Two such sequences $x,y$ are considered equivalent if
$$ {|x_i - y_j|} \lt 1/2^i + 1/2^j $$
always holds.  Up to this equivalence, we can demand that the denominator of $x_i$ is always $10^i$ (or a factor of $10^i$), so that $x_i$ is $x$ rounded up or down to the nearest such rational number (in the chosen direction), that is the nearest rational number with $i$ decimal digits (at most) after the decimal point.

More generally (or a priori more generally), given any __modulus__ $(\alpha_0,\alpha_1,\alpha_2,\ldots)$, which is an infinite sequence of positive rational numbers that diverges to infinity, a __regular Cauchy equivalence__ with modulus $\alpha$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ such that
$$ {|x_i - x_j|} \lt 1/\alpha_i + 1/\alpha_j $$
always holds.  Two such sequences $x,y$ are __regular equivalent__ with modulus $\alpha$ if
$$ {|x_i - y_j|} \lt 1/\alpha_i + 1/\alpha_j $$
always holds.  The previous examples are simply regular Cauchy sequences with modulus $(1,2,3,\ldots)$ or $(1,2,4,\ldots)$, with the appropriate notion of equivalence.

More generally still, given any modulus as above, a __modulated Cauchy sequence__ with modulus $\alpha$ is an infinite sequence $(x_0,x_1,x_2,\ldots)$ such that
$$ {|x_i - x_j|} \lt 1/\alpha_{\min(i,j)} $$
always holds.  Two such sequences $x,y$ are __modulated equivalent__ with modulus $\alpha$ if
$$ {|x_i - y_j|} \lt 2/\alpha_{\min(i,j)} $$
always holds.  Every regular Cauchy sequence with a given modulus is a modulated Cauchy sequence with the same modulus.

Instead of fixing a modulus and considering all infinite sequences satisfying this condition for that modulus, we might consider all moduli at once.  Two modulated Cauchy sequences (possibly with different moduli) will now be considered equivalent in that equivalence is given by *any* modulus.

Most generally of all, we need not specify the modulus as an actual function from $\mathbb{N}$ to $\mathbb{Q}$ but instead demand that, for each positive rational number $N$ (no matter how large), there exists a [[natural number]] $k$ such that
$$ {|x_i - x_j|} \lt 1/N $$
whenever $i,j \geq k$.  In other words, we consider a __[[Cauchy sequence]]__ of rational numbers.  Similarly, we consider two such sequences __equivalent__ if, for each $N$, there exists $k$ such that
$$ {|x_i - y_i|} \lt 1/N $$
whenever $i \geq k$.

In weak [[foundations]] (including internally to a [[topos]], or even a $\Pi$-[[Pi-pretopos|pretopos]], with [[natural numbers object]]), we can fix any modulus $\alpha$ and then prove that every modulated Cauchy sequence is equivalent to a regular Cauchy sequence with modulus $\alpha$, and also prove that any two modulated Cauchy sequences with given modulus are modulated equivalent if they are equivalent by any modulus (and regualar equivalent if they are also regular).  Thus all the constructions of real numbers in this vein are equivalent if they involve moduli at all.

We would also like to prove that every Cauchy sequence is equivalent to a modulated one, that any two equivalent Cauchy sequences are modulated equivalent, and that any Dedekind real number is represented by a Cauchy sequence.  Each of these results is equivalent to a weak form of [[countable choice]] that also follows from [[excluded middle]].  Thus, almost any foundation used in practice proves these results, but they fail in many [[sheaf topos|sheaf topoi]].  When a distinction must be made, the real numbers represented by modulated Cauchy sequences are called __[[Cauchy real number|Cauchy reals]]__.

We can also use [[nets]] instead of sequences.  In that case, we have that every Dedekind real may be represented by a Cauchy net that is modulated by a net, and that this is unique up to an equivalence modulated by a net, even in weak foundations (in particular, in any $\Pi$-pretopos).  This still will not allow us to fix a modulus in advance, however.


### The complete ordered field

There is a well-known algebraic (more or less) characterisation of the real line as the 'complete ordered field', or sometimes the 'complete archimedean field'.  This can be interpreted as follows:

*  A __field__ is well known in algebra; if it matters, we mean a [[Heyting field]].
*  An __ordered field__ means a *[[linear order|linearly]]* ordered field.
*  An __archimedean field__ is an ordered field in which every element is bounded above by a [[natural number]], so it has no [[infinite number|infinite]] elements and no non-zero [[infinitesimal number|infinitesimal]] elements.
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

However, we note that the proof is valid in weak [[foundations]], in particular internal to any [[topos]] with a [[natural numbers object]].  One can actually work in even weaker foundations than that, especially if one allows the [[underlying set]] of $\mathbb{R}$ to be [[proper class|large]].


### The locale of real numbers

Consider a [[binary relation]] $\sim$ on [[rational numbers]] satisfying these three properties:

*  If $a \geq b$ are rational numbers, then $a \sim b$.
*  If $a \geq b \sim c \geq d$, then $a \sim d$.
*  If $a \sim b \gt c \sim d$, then $a \sim d$.

These relations form a [[frame]], which we may interpret (by definition) as the __[[locale of real numbers]]__.

We may then define a __localic real number__ to be a [[point of a locale|point]] of this locale.

This agrees with the notion of Dedekind real number, even in very weak ([[predicative mathematics|predicative]] and [[constructive mathematics|constructive]]) [[foundations]].

See [[locale of real numbers]] for more.


### $\mathbb{R}$ as a terminal coalgebra

The real line $\mathbb{R}$, or at least the positive real line $\mathbb{R}^+$, may be characterized as the [[terminal object|terminal]] [[coalgebra for an endofunctor]]

Let [[Pos]] be the [[category]] of [[poset]]s. Consider the endofunctor

$$
  F_1 : Pos \to Pos
$$

that acts by [[ordinal product]] with $\omega$

$$
  F_1 : X \mapsto X \cdot \omega
  \,.
$$

+-- {: .un_prop}
###### Proposition

The terminal coalgebra of $F_1$ is order isomorphic to the non-negative real line $\mathbb{R}^+$, with its standard order.
=--

+-- {: .proof}
###### Proof

This is theorem 5.1 in

* D. Pavlovic, [[Vaughan Pratt]], _On coalgebra of real numbers_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204))
=--

> There are more and similar characterizations along these lines. Hopefully we can eventually fill them in here.


## Generalisations

Of course, one can generalise real numbers to [[complex number]]s and other kinds of [[hypercomplex number]]s.

The [[extended real number]]s include $\pm\infty$ as well as the ordinary (or _bounded_) real numbers.  [[lower real|Lower reals]], [[upper reals]], and [[MacNeille real number|MacNeille reals]] are important variations in [[constructive mathematics]], although with [[excluded middle]] they are (at least if bounded) the same as ordinary real numbers.

[[surreal number|Surreal numbers]] and the [[hyperreal number]]s of [[nonstandard analysis]] are two ways to include [[infinite number|infinite]] and [[infinitesimal number|infinitesimal]] versions of real numbers.

In [[descriptive set theory]], one often says 'real number' for an element of [[Baire space]] $\mathbb{B}$.  By the [[Schroeder-Bernstein theorem]], the sets $\mathbb{R}$ and $\mathbb{B}$ are [[bijection|isomorphic]].  Constructively, $\mathbb{B}$ can still be thought of as the set of [[irrational number]]s.


[[!redirects real number]]
[[!redirects real numbers]]
[[!redirects real line]]
[[!redirects real number line]]
[[!redirects continuum]]
