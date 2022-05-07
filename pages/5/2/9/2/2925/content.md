
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# The intermediate value theorem
* table of contents
{: toc}

## Idea

The _intermediate value theorem_ (IVT) is a fundamental principle of [[analysis]] which allows one to find a desired value by [[interpolation]].  It says that a [[continuous function]] $f \colon [0,1] \to \mathbb{R}$ from an [[interval]] to the [[real numbers]] (all with its [[Euclidean space|Euclidean]] [[topological space|topology]]) takes all values in between $f(0)$ and $f(1)$.

The IVT in its general form was not used by [[Euclid]].  Although it is hard to doubt that Euclid believed that, for any given angle, there was an angle with one-third the measure, this angle cannot be constructed by the methods available to Euclid, so he would never refer to it (see at _[[Euclidean geometry]]_).  In contrast, [[Archimedes]] made general arguments in which a quantity is approached from above and below, allowing him not only to trisect the angle but also to calculate [[pi|π]].

As normally stated, the IVT is not valid in [[constructive mathematics]], although there are constructively valid versions. These versions either weaken the conclusion to an *approximate* zero, or to strengthen the hypothesis to require the functions satisfy additional properties or have other structures, such as locally nonconstancy and lifting to locators in functions in the given example below. Even interpreted classically, these are prima facie weaker results.

## Statements and Proofs

### Classical IVT

+-- {: .num_theorem #classical}
###### Theorem
(classical IVT, assuming [[excluded middle]])

Let $f\colon [a,b] \to \mathbb{R}$ be a [[continuous function]] from a [[compact space|compact]] [[closed interval]] to the [[real line]], and suppose that $f(a) \lt 0$ while $f(b) \gt 0$. Then there exists a point $c$ in the unit interval such that $f(c) = 0$.
=--

+-- {: .proof}
###### Proof

Let $g:\mathbb{R} \to \mathbb{R}$ be defined as $g(x) \coloneqq (b - a) x + a$. Then there exists a function $h:[1,0] \to \mathbb{R}$ such that $f = g \circ h$. 

By [this example](connected+topological+space) the interval $[0,1]$ is a [[connected topological space]] (this is where [[excluded middle]] is used).

By [this prop.](connected+topological+space) also its [[image]] $f([0,1]) \subset \mathbb{R}$ is connected. By [this example](connected+topological+space) that image is itself an interval. This implies the claim is true for $h$. Since linear functions preserve the properties of an interval being compact and closed, if the claim is true for $h$, it is true for $f$. 

=--

### Constructive IVT with weakened conclusion

+-- {: .num_theorem #conclusion}
###### Theorem
(constructive IVT with weakened conclusion)

For real numbers $a$ and $b$, let $f\colon [a,b] \to \mathbb{R}$ be a [[pointwise continuous function]] from the [[closed interval]] $[a, b]$ to the [[real line]], and supposed that $f(a) \lt 0$ and $f(b) \gt 0$. Then for every positive number $\epsilon$ there exists a point $c_\epsilon$ in the unit interval such that ${|f(c_\epsilon)|} \lt \epsilon$.
=--


+-- {: .proof}
###### Proof of Theorem \ref{conclusion}&#8288;

This proof originally appeared in [Frank 2020](#Frank20). 

Let us inductively define the following [[sequences]]:

$$a_0 \coloneqq a$$ 
$$b_0 \coloneqq b$$ 
$$c_n \coloneqq \frac{a_n + b_n}{2}$$
$$d_n \coloneqq \max\left(0, \min\left(\frac{1}{2} + \frac{f(c_\epsilon)}{\epsilon}, 1\right)\right)$$
$$a_{n + 1} = c_n - \frac{d_n (b - a)}{2^{n + 1}}$$
$$a_{n + 1} = b_n - \frac{d_n (b - a)}{2^{n + 1}}$$

Then 
$$b_n - a_n = \frac{b - a}{2^n}$$

and the sequence $c_n$ is a [[Cauchy sequence]], because for [[natural numbers]] $m \lt n$, 

$$\vert c_m - c_n \vert \leq \frac{b - a}{2^m}$$

Lemma: For every natural number $m$, either 1. there exists a $j \leq m$ such that $\vert f(c_j) \lt \epsilon$, or 2. $f(a_m) \lt 0$ and $f(b_m) \gt 0$. This could be proved by induction on natural numbers: 

When $m = 0$, $f(a_0) = f(a) \lt 0$ and $f(b_0) = f(b) \gt 0$. 

Now, assume that the above lemma is true for a particular $m$. If there exists a $j \leq m$ such that $\vert f(c_j) \lt \epsilon$, then there exists a $j \leq m + 1$ such that $\vert f(c_j) \lt \epsilon$. Otherwise, either $2 f(c_m) \lt -\epsilon$, $2 f(c_m) \gt \epsilon$, or $\vert f(c_m) \vert \gt \epsilon$. 

* If $2 f(c_m) \lt -\epsilon$, then we define 
$$d_m \coloneqq 1$$
$$a_{m + 1} \coloneqq a_m$$
$$b_{m + 1} \coloneqq c_m$$
so that $a_{m + 1} \lt 0$ and $b_{m + 1} \gt 0$. 

* If $2 f(c_m) \gt \epsilon$, then we define 
$$d_m \coloneqq 1$$
$$a_{m + 1} \coloneqq c_m$$
$$b_{m + 1} \coloneqq b_m$$
so that $a_{m + 1} \lt 0$ and $b_{m + 1} \gt 0$. 

* If $\vert f(c_m) \vert \gt \epsilon$, then there exists a $j \leq m + 1$ such that $\vert f(c_j) \lt \epsilon$. 

Thus, the above lemma is true. 

Now, by pointwise continuity at $c$, let $\delta$ be such that $\vert x - y \vert \lt \delta$ implies $\vert f(x) - f(y)\vert  \lt \epsilon$. Choose a natural number $m$ such that 

$$\vert c - c_m \vert \lt \frac{\delta}{2}$$ 
$$\frac{\vert b - a \vert}{2^{m + 1}} \lt \frac{\delta}{2}$$ 

If there exists a $j \leq m$ such that $\vert f(c_j) \lt \epsilon$, then the intermediate value is true. Otherwise, $f(a_m) \lt 0$ and $f(b_m) \gt 0$, and so

$$\vert c - c_m \vert \lt \vert c - c_m \vert + \vert c_m - a_m \vert \lt \delta$$
$$\vert c - c_m \vert \lt \vert c - c_m \vert + \vert c_m - b_m \vert \lt \delta$$

and so that means that 

$$\vert f(c) - f(a_m) \vert \lt \epsilon$$
$$\vert f(c) - f(b_m) \vert \lt \epsilon$$

which means that $\vert f(c) \vert \lt \epsilon$. 

=--

If [[excluded middle]] is true, then the classical IVT follows from the above theorem:

+-- {: .proof}
###### Proof of Theorem \ref{classical}&#8288;

By way of contradiction (applying the [[double negation]] law of [[classical logic]]), suppose that ${|f(c)|} \gt 0$ for every $c$ in $[0,1]$.  Then the extra hypothesis of Theorem \ref{hypothesis} is certainly satisfied, so there exists some $c$ such that $f(c) = 0$ after all.  (Constructively, this is enough to show that the classical theorem has no counterexample.)
=--

### Constructive IVT with strengthened hypothesis

+-- {: .num_theorem #hypothesis}
###### Theorem
(constructive IVT with strengthened hypothesis)

For real numbers $a$ and $b$ with [[locators]], let $f\colon [a,b] \to \mathbb{R}$ be a [[pointwise continuous function]] from the [[closed interval]] $[a, b]$ to the [[real line]] that is a [[locally nonconstant function]] and that [[lifts to locators]], and supposed that $f(a) \leq 0$ and $f(b) \geq 0$. Then, there exists a point $c$ in $[a, b]$ with a locator such that $f(c) = 0$. 
=--


+-- {: .proof}
###### Proof of Theorem \ref{hypothesis}&#8288;

This proof originally appeared in [Booij 2018](#Booij18)

... 

=--

## See also

* [[extreme value theorem]]
* [[fundamental theorem of algebra]]

## References

* [[Peter Schuster]]; Unique existence, approximate solutions,
and countable choice; [doi](http://dx.doi.org/10.1016/S0304-3975%2802%2900707-7).

* Matt F.; answer to Approximate intermediate value theorem in pure constructive mathematics; MathOverflow; [web](http://mathoverflow.net/q/255371).

* {#Frank20} [[Matthew Frank]], _Interpolating Between Choices for the Approximate Intermediate Value Theorem_ ([arxiv:1701.02227](https://arxiv.org/abs/1701.02227)), Logical Methods in Computer Science, July 14, 2020, Volume 16, Issue 3 - [doi:10.23638/LMCS-16(3:5)2020](https://doi.org/10.23638/LMCS-16%283:5%292020)

* [[Paul Taylor]]; The intermediate value theorem; A lambda calculus for real analysis, 14; [web](http://www.paultaylor.eu/ASD/lamcra/asdivt).

* {#Booij18} Auke Booij, *Extensional constructive real analysis via locators*, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

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
