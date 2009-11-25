# The intermediate value theorem
* tic
{: toc}

## Idea

The intermediate value theorem (IVT) is a fundamental principle of analysis which allows one to find a desired value by interpolation.  Roughly speaking, it says that if Papa Bear\'s porridge is too hot and Mama Bear\'s porridge is too cold, then there must be some temperature of porridge (perhaps Baby Bear\'s) which is [just right](http://secure.wikimedia.org/wikipedia/en/wiki/The_Story_of_the_Three_Bears).

The IVT in its general form was not used by [[Euclid]].  Although it is hard to doubt that Euclid believed that, for any given angle, there was an angle with one-third the measure, this angle cannot be constructed by the methods available to Euclid, so he would never refer to it.  In contrast, [[Archimedes]] made general arguments in which a quantity is approached from above and below, allowing him not only to trisect the angle but also to calculate $\pi$.

As normally stated, the IVT is not valid in [[constructive mathematics]], although there are constructively valid versions.


## Statements

+-- {: .num_theorem #classical}
###### Theorem
(classical IVT)

Let $f\colon [0,1] \to \mathbb{R}$ be a [[continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Then there exists a point $c$ in the unit interval such that $f(c) = 0$.
=--

+-- {: .num_theorem #conclusion}
###### Theorem
(constructive IVT with weakened conclusion)

Let $f\colon [0,1] \to \mathbb{R}$ be a [[uniformly continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Then for every positive number $\epsilon$ there exists a point $c_\epsilon$ in the unit interval such that ${|f(c_\epsilon)|} \lt \epsilon$.
=--

+-- {: .num_theorem #hypothesis}
###### Theorem
(constructive IVT with strengthened hypothesis)

Let $f\colon [0,1] \to \mathbb{R}$ be a [[uniformly continuous function]] from the [[unit interval]] to the [[real line]], and suppose that $f(0) \lt 0$ while $f(1) \gt 0$.  Suppose further that, for any points $a,b$ in the unit interval with $a \lt b$, there exists a point $c_{a,b}$ such that $a \lt c_{a,b} \lt b$ and ${|f(c_{a,b})|} \gt 0$.  Then there exists a point $c$ in the unit interval such that $f(c) = 0$.
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

Suppose that $f$ satisfies the additional hypothesis.

...
=--

+-- {: .proof}
###### Proof of Theorem \ref{classical}&#8288;

By way of contradiction, suppose that ${|f(c)|} \gt 0$ for every $c$ in $[0,1]$.  Then the extra hypothesis of Theorem \ref{hypothesis} is certainly satisfied, so there exists some $c$ such that $f(c) = 0$ after all.
=--

Of course, we can also prove Theorems \ref{classical} and \ref{hypothesis} directly by modifying the proof of Theorem \ref{conclusion} appropriately.