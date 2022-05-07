
# The intermediate value theorem
* table of contents
{: toc}

## Idea

The _intermediate value theorem_ (IVT) is a fundamental principle of [[analysis]] which allows one to find a desired value by [[interpolation]].  It says that a [[continuous function]] $f \colon [0,1] \to \mathbb{R}$ from an [[interval]] to the [[real numbers]] (all with its [[Euclidean space|Euclidean]] [[topological space|topology]]) takes all values in between $f(0)$ and $f(1)$.

The IVT in its general form was not used by [[Euclid]].  Although it is hard to doubt that Euclid believed that, for any given angle, there was an angle with one-third the measure, this angle cannot be constructed by the methods available to Euclid, so he would never refer to it (see at _[[Euclidean geometry]]_).  In contrast, [[Archimedes]] made general arguments in which a quantity is approached from above and below, allowing him not only to trisect the angle but also to calculate [[pi|π]].

As normally stated, the IVT is not valid in [[constructive mathematics]], although there are constructively valid versions.

+-- {: .standout}
I\'ve decided that I don\'t really like how I\'ve been writing this, and I\'m working on a new version.  (Aside from its intrinsic interest and practical usefulness, this is such a classic example of the differences between classical and constructive analysis that I want to get it right.)  That shouldn\'t stop anybody from putting here what *they* find useful, but I thought that a warning might be in order.  ---[[Toby Bartels]]
=--


## Statements

+-- {: .num_theorem #classical}
###### Theorem
(classical IVT, assuming [[excluded middle]])

Let $f\colon [0,1] \to \mathbb{R}$ be a [[continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Then there exists a point $c$ in the unit interval such that $f(c) = 0$.
=--

+-- {: .proof}
###### Proof

By [this example](connected+topological+space) the interval $[0,1]$ is a [[connected topological space]] (this is where [[excluded middle]] is used).

By [this prop.](connected+topological+space) also its [[image]] $f([0,1]) \subset \mathbb{R}$ is connected. By [this example](connected+topological+space) that image is itself an interval. This implies the claim.

=--


+-- {: .num_theorem #conclusion}
###### Theorem
(constructive IVT with weakened conclusion)

Let $f\colon [0,1] \to \mathbb{R}$ be a [[uniformly continuous map|uniformly continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Then for every positive number $\epsilon$ there exists a point $c_\epsilon$ in the unit interval such that ${|f(c_\epsilon)|} \lt \epsilon$.
=--

+-- {: .num_theorem #hypothesis}
###### Theorem
(constructive IVT with strengthened hypothesis, assuming [[weak countable choice]])

Let $f\colon [0,1] \to \mathbb{R}$ be a [[uniformly continuous map|uniformly continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Suppose further that, for any points $a,b$ in the unit interval with $a \lt b$, there exists a point $c_{a,b}$ such that $a \lt c_{a,b} \lt b$ and ${|f(c_{a,b})|} \gt 0$.  (In other words, the non-[[zero set]] $\{ c : {|f(c)|} \gt 0 \}$ is [[dense subspace|dense]].)  Then there exists a point $c$ in the unit interval such that $f(c) = 0$.
=--

In the constructive versions, we have changed from a continuous function to a uniformly continuous one just to be safe; while some varieties of constructive analysis accept the theorem that any continous function on $[0,1]$ is uniformly continous, others do not, and some even refute it.  In any case, even the classical version only applies to uniformly continuous functions, even though the classical mathematician is free to leave out the word 'uniformly' and so usually does.  The more significant change is to either weaken the conclusion to an *approximate* zero, or to strengthen the hypothesis to forbid functions that 'hover' near zero on some subinterval; even interpreted classically, these are prima facie weaker results.

There are obvious generalisations in which the domain $[0,1]$ is generalised to any compact interval, in which the signs of $f(0)$ and $f(1)$ are swapped, and in which the desired value $f(c) = 0$ is generalised to any real number.  They may be proved either by modifying a proof of the main theorem or as a corollary by linearly transforming the input and output of $f$.


## Proofs

We will prove Theorem \ref{conclusion} in a constructive manner, which (besides satisfying the constructive mathematicians) demonstrates an algorithm for approximating the point $c$ as closely as desired.  Theorems \ref{classical} and \ref{hypothesis} are then easy to prove (the latter constructively, the former not) as corollaries.

+-- {: .proof}
###### Proof of Theorem \ref{conclusion}&#8288;

Since $f$ is uniformly continuous, there exists a positive number $\delta$ such that ${|f(x) - f(y)|} \lt \epsilon/2$ whenever ${|x - y|} \lt \delta$.  Since $\delta$ is positive, there exists a [[natural number]] $n$ such that $\delta \gt 2^{-n}$.  We will approximate $c_\epsilon$ in $n$ steps.

We will define finite [[sequences]] $(a_1,\ldots,a_n)$, $(b_1,\ldots,b_n)$, and $(c_1,\ldots,c_n)$ such that $a_k \lt c_k \lt b_k$ at each stage.  To begin with, let $a_1 \coloneqq 0$ and $b_1 \coloneqq 1$.  At each stage, let $c_k$ be the arithmetic mean of $a_k$ and $b_k$.  By the [[comparison]] property of the [[linear order]] $\lt$, either $f(c_k) \gt -\epsilon/2$ or $f(c_k) \lt \epsilon/2$;

*  if the former, then let $a_{k+1} \coloneqq a_k$ and $b_{k+1} \coloneqq c_k$,
*  if the latter, then let $a_{k+1} \coloneqq c_k$ and $b_{k+1} \coloneqq b_k$.

Either way, we have $a_{k+1} \lt b_{k+1}$, so we can continue.

At each stage, we have

*  $f(a_k) \lt \epsilon/2$,
*  $f(b_k) \gt - \epsilon/2$,
*  $c_k - a_k = 2^k$,
*  $b_k - c_k = 2^k$.

Therefore, $-\epsilon \lt f(b_n) - \epsilon/2 \lt f(c_n) \lt f(a_k) + \epsilon/2 \lt \epsilon$, so $c_n$ is the $c_\epsilon$ desired.
=--

This is the _bisection algorithm_ in [[numerical analysis]].  Note that this algorithm always chooses $c_\epsilon$ to be a [[dyadic rational]].  Slight variations will allow $c_\epsilon$ to be drawn from any previously chosen [[dense subspace]] of $[0,1]$ (or this can be proved as a corollary).

+-- {: .proof}
###### Proof of Theorem \ref{hypothesis}&#8288;

Suppose that $f$ satisfies the additional hypothesis (and assume [[weak countable choice]]).

...
=--

+-- {: .query}
I\'m not sure how to finish this, and maybe it\'s a mistake!  Certainly the result follows from [[countable choice]], but I had thought that it followed from *weak* countable choice.  (The proof from countable choice is to continue the bisection algorithm for infinitely many steps and take $\lim_n c_n$.)  There certainly ought to be a proof that uses only excluded middle (which implies $WCC$), since Theorem \ref{classical} needs only that.

Anonymous: Matthew Frank gave a proof of the constructive intermediate value theorem without any choice at all in this arxiv article: [arxiv:1701.02227](https://arxiv.org/abs/1701.02227). 
=--

+-- {: .proof}
###### Proof of Theorem \ref{classical}&#8288;

By way of contradiction (applying the [[double negation]] law of [[classical logic]]), suppose that ${|f(c)|} \gt 0$ for every $c$ in $[0,1]$.  Then the extra hypothesis of Theorem \ref{hypothesis} is certainly satisfied, so there exists some $c$ such that $f(c) = 0$ after all.  (Constructively, this is enough to show that the classical theorem has no counterexample.)
=--

Of course, we can also prove Theorems \ref{classical} and \ref{hypothesis} directly by modifying the proof of Theorem \ref{conclusion} appropriately.

Other ways to identify $c$ (in Theorem \ref{classical} or \ref{hypothesis}) are as the [[supremum]] of $\{x \;|\; f(x) \lt 0\}$ and as the point (guaranteed by the [[extreme value theorem]]) where the minimum of ${|f|}$ is attained.  (After accepting these non-constructive results, the proof that the value $c$ so found satisfies $f(c) = 0$, while perhaps non-trivial, is constructive without choice, given uniform continuity, or in the first case given only continuity at $c$.)


## References

* [[Peter Schuster]]; Unique existence, approximate solutions,
and countable choice; [doi](http://dx.doi.org/10.1016/S0304-3975%2802%2900707-7).

* Matt F.; answer to Approximate intermediate value theorem in pure constructive mathematics; MathOverflow; [web](http://mathoverflow.net/q/255371).

* [[Matthew Frank]], _Interpolating Between Choices for the Approximate Intermediate Value Theorem_ ([arxiv:1701.02227](https://arxiv.org/abs/1701.02227)), Logical Methods in Computer Science, July 14, 2020, Volume 16, Issue 3 - [doi:10.23638/LMCS-16(3:5)2020](https://doi.org/10.23638/LMCS-16%283:5%292020)

* [[Paul Taylor]]; The intermediate value theorem; A lambda calculus for real analysis, 14; [web](http://www.paultaylor.eu/ASD/lamcra/asdivt).


[[!redirects intermediate value theorem]]
[[!redirects intermediate value theorems]]
[[!redirects Intermediate Value Theorem]]
[[!redirects Intermediate Value Theorems]]
[[!redirects intermediate-value theorem]]
[[!redirects intermediate-value theorems]]
[[!redirects Intermediate-value Theorem]]
[[!redirects Intermediate-value Theorems]]
[[!redirects Intermediate-Value Theorem]]
[[!redirects Intermediate-Value Theorems]]
[[!redirects IVT]]
