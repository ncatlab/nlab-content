# Combinatory logic

* table of contents
{: toc}

## Idea

> Combinator algebra has always struck me as a subject almost impossible to watch: it's a lousy spectator sport but has a reputation of habit-forming as a participator sport. P. Freyd ([1989](#Freyd89), p.63)

**Combinatory logic** is a rephrasing of the [[lambda calculus]] that avoids explicit mention of [[variables]] and of [[lambda abstraction]].  Instead it uses [[combinators]] -- in the most common case, they are traditionally called $S$, $K$, and $I$ -- with the only other operation being [[application]].

Since this move circumvents the necessity of variable management, combinatory logic is important for applications in [[computer science]] and [[linguistics]].

Under the [[propositions as types]] correspondence, combinatory logic corresponds to the presentation of [[logic]] using a [[Hilbert system]] (instead of [[natural deduction]] or [[sequent calculus]]).  There are versions of combinatory logic corresponding to [[linear logic]] and [[affine logic]], generally called **BCI logic** and **BCK logic** (after the combinators they use).

## Historical remarks

The 1920s gave birth to several formal systems that permitted to base mathematics on the notion of function like e.g. the lambda calculus or von Neumann 'set' theory that eventually morphed into [[NBG|Neumann-Bernays-Gödel set theory]]. Notably the first of such systems was combinatory logic which was introduced by [[Moses Schönfinkel]] in 1920 ([Sch&#246;nfinkel 1924](#Schoen24)) and developed (partly independently) by [[Haskell Curry]] by the end of the decade.

Of course, a later such function based approach to mathematics is [[category theory]] and there has been in fact some interaction between combinatory logic and category theory ([Bunder 1984](#Bunder84)). In 1972 when the connection between Cartesian closed categories and lambda calculus was an object of active research, [[Jim Lambek]] wrote:

> Sch&#246;nfinkel's original program to base all of mathematics on combinatory logic can now be said to have been carried out by Lawvere in his many articles pursuing a categorical formulation of mathematics. ([1972](#Lambek72), p.57)

## The combinators S, K, and I

The basic combinators can be defined in terms of $\lambda$-calculus as

* $S = \lambda x. \lambda y. \lambda z. (x z)(y z)$
* $K = \lambda x. \lambda y. x$
* $I = \lambda x. x$

In [[simply typed lambda-calculus]], these combinators are [[polymorphic]] with types

* $S : (A \to (B\to C)) \to ((A\to B) \to (A\to C))$
* $K : A\to (B\to A)$
* $I : A\to A$

for arbitrary types $A,B,C$.

When combinatory logic is presented on its own rather than in terms of $\lambda$-calculus, the combinators are characterized by reduction rules that mirror their definition in terms of $\lambda$-abstractions:

* $S x y z \equiv (x z)(y z)$
* $K x y \equiv x$
* $I x \equiv x$

Sometimes the combinator $I$ is omitted, as it can be defined from $S$ and $K$ as $I=S K K$.

## Encoding abstraction

The combinators $S$, $K$, and $I$ are used to encode $\lambda$-abstraction in the following way.  If $M$ is a term in combinatory logic (perhaps containing variables), we define $\lambda x.M$ by induction over the structure of the term $M$.

* If $M=x$, then $\lambda x.x = I$.
* If $M$ is a variable $y\neq x$, then $\lambda x.y = K y$.
* If $M = N P$ is an application of one term to another, then $\lambda x.M = S (\lambda x.N) (\lambda x.P)$, so we can recursively translate $\lambda x.N$ and $\lambda x.P$.

(It is common to see this described with the second case given as "$\lambda x.M = K M$ whenever $M$ does not contain $x$ as a [[free variable]]".  However, this overlaps with the third case and is not structurally recursive.  The above definition translates $\lambda x.y z$ to $S(K y)(K z)$, while the one with the free-variable-check produces $K(y z)$; both reduce to $y z$ when applied to any argument.)

Using this construction of an "abstraction operator" in the combinatory logic, we can then proceed to translate an arbitrary term of $\lambda$-calculus into combinatory logic by translating all the abstractions "from the inside out".  Formally, we crawl over the term and whenever we find an abstraction, we first recurse into its body, then we apply the above abstraction operator.

The construction of an abstraction operator in combinatory logic is analogous to a [[cut admissibility]] theorem; the resulting translation of $\lambda$-calculus into combinatory logic is then analogous to the corresponding [[cut-elimination]] theorem.

## Linear (BCI) and affine (BCK) combinatory logic 
 {#LinearAndAffine}

Versions of combinatory logic that correspond to [[linear logic]] and [[affine logic]] have been studied under the names **BCI logic** and **BCK logic**  respectively, with the letters indicating the combinators used, where

* $B = \lambda x.\lambda y.\lambda z. x(yz) : (B\to C) \to (A\to B) \to (A\to C)$
* $C = \lambda x.\lambda y.\lambda z. (xz)y : (A\to (B\to C)) \to (B \to (A\to C))$

The combinator $I$ is also definable as $CKK$, so it is also available in BCK logic (which might therefore be called BCKI logic).  Similarly, traditional combinatory logic could be called "SKI logic", or just "SK logic".

Note that $B$ has the same type as the "composition" operation in a [[closed category]], while $C$ has the type of a symmetry/exchange for a closed category.  Similarly, $K$ is a sort of [[weakening rule]] while $S$ combines composition, symmetry, and [[contraction rule|contraction]].

## Remark

A _partial combinatory algebra_ , also called a _Sch&#246;nfinkel algebra_ ,  is an algebraic structure that abstracts the structure of (partial) combinatory logic. They play an important role in the theory of [[realizability topos|realizability toposes]].

## Related pages

* [[partial combinatory algebra]]
* [[combinator]]
* [[lambda-calculus]]
* [[categorial grammar]]

## References

* {#Schoen24}[[Moses Schönfinkel]], _&#220;ber die Bausteine der mathematischen Logik_ , Math. Ann. **92** (1924) pp.305-316. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PID=GDZPPN002270110)) English translation with comments by Quine pp.355-366 in van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967. 

* {#Bunder84}M. W. Bunder, Category Theory Based on Combinatory Logic , Arch. Math. Logik **24** (1984) pp.1-15. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002045680))

* {#Freyd89}[[Peter Freyd]], _Combinators_ , Contemp. Math. **92** (1989) pp.63-66.

* R. Hindley, J. Seldin, _Introduction to Combinators and $\lambda$-Calculus_ , Cambridge UP 1986.

* {#Lambek72}[[Jim Lambek]], _Deductive systems and categories III. Cartesian closed categories, intuitionist propositional calculus, and combinatory logic_ , pp.57&#8211;82 LNM **274** Springer Heidelberg 1972.

[[!redirects combinatory logics]]
[[!redirects BCI logic]]
[[!redirects BCI-logic]]
[[!redirects BCK logic]]
[[!redirects BCK-logics]]
