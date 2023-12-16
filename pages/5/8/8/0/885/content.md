
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

A __natural number__ is traditionally one of the [[numbers]] $1$, $2$, $3$, and so on.  It is now common in many fields of mathematics to include $0$ as a natural number as well.  One advantage of doing so is that a natural number can then be identified with the [[cardinal number|cardinality]] of a [[finite set]], as well as a finite [[ordinal number]].  One can distinguish these as the __nonnegative integers__ (with $0$) and the __positive integers__ (without $0$), at least until somebody uses 'positive' in the semidefinite sense.  To a [[set theory|set theorist]], a natural number is essentially the same as an __[[integer]]__, so they often use the shorter word; one can also clarify with __unsigned integer__ (but this doesn\'t help with $0$). In school mathematics, natural numbers with $0$ are called __whole numbers__. 

The set of natural numbers is often written $N$, $\mathbf{N}$, $\mathbb{N}$, $\omega$, or $\aleph_0$.  The last two notations refer to this set\'s structure as an [[ordinal number]] or [[cardinal number]] respectively, and they often (usually for $\aleph$) have a subscript $0$ allowing them to be generalised.  In the [[foundations]] of mathematics, the [[axiom of infinity]] states that this actually forms a set (rather than a proper class).  At a foundational level, it\'s completely irrelevant whether $0$ counts as a natural number or not; as [[sets]] (and even as [[natural numbers objects]]), the two options are equivalent, so we are really talking about the choice of additive [[semigroup]] structure (or [[inclusion map]] into the set of [[integers]], etc). 

By default, our natural numbers always include $0$. 

## Operations and relations

We define the standard [[arithmetic]] and [[metric]] operations and [[order]] relations of the [[natural numbers]] in [[dependent type theory]] using [[induction]] on the natural numbers. 

### Addition

Addition is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m + n:\mathbb{N}$$

$$\vdash \beta_+^{0, 0}:0 + 0 =_\mathbb{N} 0$$

$$n:\mathbb{N} \vdash \beta_+^{0, s}(n):0 + s(n) =_\mathbb{N} s(n)$$

$$n:\mathbb{N} \vdash \beta_+^{s, 0}(n):s(n) + 0 =_\mathbb{N} s(n)$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_+^{s, s}(m, n):s(m) + s(n) =_\mathbb{N} s(s(m + n))$$

### Minimum function

The minimum function is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash \min(m, n):\mathbb{N}$$

$$\vdash \beta_\min^{0, 0}:\min(0, 0) =_\mathbb{N} 0$$

$$n:\mathbb{N} \vdash \beta_\min^{0, s}(n):\min(0, s(n)) =_\mathbb{N} 0$$

$$n:\mathbb{N} \vdash \beta_\min^{s, 0}(n):\min(s(n), 0) =_\mathbb{N} 0$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\min^{s, s}(m, n):\min(s(m), s(n)) =_\mathbb{N} s(\min(m, n))$$

### Maximum function

The maximum function is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash \max(m, n):\mathbb{N}$$

$$\vdash \beta_\max^{0, 0}:\max(0, 0) =_\mathbb{N} 0$$

$$n:\mathbb{N} \vdash \beta_\max^{0, s}(n):\max(0, s(n)) =_\mathbb{N} s(n)$$

$$n:\mathbb{N} \vdash \beta_\max^{s, 0}(n):\max(s(n), 0) =_\mathbb{N} s(n)$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\max^{s, s}(m, n):\max(s(m), s(n)) =_\mathbb{N} s(\max(m, n))$$

### Distance function

The distance function is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash \rho(m, n):\mathbb{N}$$

$$\vdash \beta_\rho^{0, 0}:\rho(0, 0) =_\mathbb{N} 0$$

$$n:\mathbb{N} \vdash \beta_\rho^{0, s}(n):\rho(0, s(n)) =_\mathbb{N} s(n)$$

$$n:\mathbb{N} \vdash \beta_\rho^{s, 0}(n):\rho(s(n), 0) =_\mathbb{N} s(n)$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\rho^{s, s}(m, n):\rho(s(n), s(n)) =_\mathbb{N} \rho(n, n)$$

### Absolute value

The absolute value is defined as the distance of a natural number from zero. 

$$n:\mathbb{N} \vdash \vert n \vert:\mathbb{N}$$

$$n:\mathbb{N} \vdash \delta_{\vert-\vert}(n):\vert n \vert =_\mathbb{N} \rho(n, 0)$$

### Less than relation

The less than relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \lt n \; \mathrm{type}$$

$$\vdash \beta_\lt^{0, 0}:0 \lt 0 \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\lt^{0, s}(n):0 \lt s(n) \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\lt^{s, 0}(n):s(n) \lt 0 \simeq \mathbb{0}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\lt^{s, s}(n):s(m) \lt s(n) \simeq m \lt n$$

### Less than or equal to relation

The less than or equal to relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \leq n \; \mathrm{type}$$

$$\vdash \beta_\leq^{0, 0}:0 \leq 0 \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\leq^{0, s}(n):0 \leq s(n) \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\leq^{s, 0}(n):s(n) \leq 0 \simeq \mathbb{0}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\leq^{s, s}(n):s(m) \leq s(n) \simeq m \leq n$$

### Apart from relation

The apart from relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \# n \; \mathrm{type}$$

$$\vdash \beta_\#^{0, 0}:0 \# 0 \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\#^{0, s}(n):0 \# s(n) \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\#^{s, 0}(n):s(n) \# 0 \simeq \mathbb{1}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\#^{s, s}(n):s(m) \# s(n) \simeq m \# n$$

### Observational equality relation

The observational equality relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \doteq n \; \mathrm{type}$$

$$\vdash \beta_\doteq^{0, 0}:0 \doteq 0 \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\doteq^{0, s}(n):0 \doteq s(n) \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\doteq^{s, 0}(n):s(n) \doteq 0 \simeq \mathbb{0}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\doteq^{s, s}(n):s(m) \doteq s(n) \simeq m \doteq n$$

### Greater than relation

The greater than relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \gt n \; \mathrm{type}$$

$$\vdash \beta_\gt^{0, 0}:0 \gt 0 \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\gt^{0, s}(n):0 \gt s(n) \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\gt^{s, 0}(n):s(n) \gt 0 \simeq \mathbb{1}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\gt^{s, s}(n):s(m) \gt s(n) \simeq m \gt n$$

### Greater than or equal to relation

The greater than or equal to relation is inductively defined by double induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m \geq n \; \mathrm{type}$$

$$\vdash \beta_\geq^{0, 0}:0 \geq 0 \simeq \mathbb{1}$$

$$n:\mathbb{N} \vdash \beta_\geq^{0, s}(n):0 \geq s(n) \simeq \mathbb{0}$$

$$n:\mathbb{N} \vdash \beta_\geq^{s, 0}(n):s(n) \geq 0 \simeq \mathbb{1}$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\geq^{s, s}(n):s(m) \geq s(n) \simeq m \geq n$$

### Multiplication

Multiplication is inductively defined by induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash m + n:\mathbb{N}$$

$$n:\mathbb{N} \vdash \beta_\cdot^{0}(n):0 \cdot n =_\mathbb{N} 0$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_\cdot^{s}(m, n):s(m) \cdot n =_\mathbb{N} m \cdot n + n$$

### Exponentiation

Exponentiation is inductively defined by induction on the natural numbers

$$m:\mathbb{N}, n:\mathbb{N} \vdash n^m:\mathbb{N}$$

$$n:\mathbb{N} \vdash \beta_\cdot^{0}(n):n^0 =_\mathbb{N} 1$$

$$m:\mathbb{N}, n:\mathbb{N} \vdash \beta_{(-)^{(-)}}^{s}(m, n):n^{s(m)} =_\mathbb{N} n^m \cdot n$$

### Division and remainder

Given a natural number $n$, we define the division function $m \div n: \mathbb{N} \times \mathbb{N}_{+} \to \mathbb{N}$ such that  

* for all $m:\mathbb{N}$ and $n:\mathbb{N}_{+}$, if $m \lt n$ then $m \div n = 0$
* for all $m:\mathbb{N}$ and $n:\mathbb{N}_{+}$, $(m + n) \div n = 1 + m \div n)$

and the remainder function 

$$m\ \%\ n \coloneqq m - (m \div n) \cdot n$$

## Natural numbers objects

$\mathbf{N}$ is a [[natural numbers object]] in [[Set]]; indeed, it is the original example.  This consists of an initial element $0$ (or $1$ if $0$ is not used) and a successor operation $n \mapsto n + 1$ (or simply $n \mapsto n^+$; in [[computer science]], one often writes $n+$) such that, for a set $X$, an element $a: X$, and a [[function]] $s: X \to X$, there exists a unique function $f: \mathbf{N} \to X$ such that $f_0 = a$ and $f_{n+1} = s(f_n)$. This function $f$ is said to be constructed by __primitive recursion__. (Fancier forms of [[recursion]] are also possible.)  

The basic idea is that we define the values of $f$ one by one, starting with $f_0 = a$, then $f_1 = s(a)$, $f_2 = s(s(a))$, and so on.  These are all both possible and necessary individually, but something must be put in the [[foundations]] to ensure that this can go on uniquely forever.


## Properties

### Minima of subsets of natural numbers

In [[classical mathematics]], any [[inhabited set|inhabited]] subset of the natural numbers possesses a minimal element. In [[constructive mathematics]], one cannot show this:

+-- {: .num_prop #BrouwerianCounterexample}
###### Proposition 
**(a [[Brouwerian counterexample]])**

If every inhabited subset of the natural numbers possesses a minimal element, then the [[excluded middle|law of excluded middle]] holds.
=--

+-- {: .proof}
###### Proof

Let $\varphi$ be an arbitrary arithmetical formula. Then the subset
$$ U := \{ n \in \mathbb{N} \,|\, n = 1 \vee \varphi \} \subseteq \mathbb{N} $$
is inhabited. By assumption, it possesses a minimal element $n_0$. By discreteness of the natural numbers, either $n_0 = 0$ or $n_0 \gt 0$. In the first case, $\varphi$ holds. In the second case, $\neg\varphi$ holds.
=--

In this sense, the natural numbers are not complete, and it's fruitful to study their completion: For instance, the global sections of the completed natural numbers object in the [[category of sheaves|sheaf topos]] on a topological space $X$ are in one-to-one correspondence with upper semicontinuous functions $X \to \mathbb{N}$ (details at _[[one-sided real number]]_).

We can salvage the minimum principle in two ways:

+-- {: .num_prop}
###### Proposition

Any **[[decidable subset|detachable]]** inhabited subset of the natural numbers possesses a minimal element.
=--

+-- {: .num_prop}
###### Proposition

Any inhabited subset of the natural numbers does **not not** possess a minimal element.
=--

For instance, any finitely generated vector space over a [[field|residue field]] does _not not_ possess a finite basis (pick a minimal generating set, guaranteed to _not not_ exist). Interpreting this in the [[internal language]] of the sheaf topos of a [[reduced scheme]] $X$, one obtains the well-known fact that any $\mathcal{O}_X$-module locally of finite type over $X$ is locally free on a dense open subset.


### Decreasing sequences of natural numbers

Classically, any *weakly* decreasing sequence of natural numbers $(a_n)_n$ is eventually constant, i.e. admits an index $N$ such that $a_N = a_{N+1} = a_{N+2} = \cdots$. Constructively, one can only prove for each $M$ that there exists an index $N$ such that $a_N = a_{N+1} = \cdots = a_{N+M}$.  (One may prove this by induction on $a_0$; indeed, you can always find $N$ so that $N \leq a_0 M$.)  The classical principle is equivalent to the [[limited principle of omniscience]] for $\mathbb{N}$ (which follows already when $a_0 = 1$).

On the other hand, there can be no *strictly* decreasing sequence of natural numbers.  This is constuctively valid (proved by contradiction and induction on $a_0$).

This is relevant to [[constructive algebra]], as this shows that formulating chain conditions needs some care.  (It is easier to say 'weakly' than 'strictly' in the hypothesis, but then it\'s unclear how to state the conclusion.)

## Examples
 {#Examples}

* [[0]]

* [[1]]

* [[24]]

## Related concepts

* [[number]], [[natural number]], [[integer]], [[rational number]], [[algebraic number]], [[Gaussian number]], [[irrational number]], [[real number]], [[p-adic number]]

* [[natural numbers type]], [[natural numbers object]]

* [[decimal numeral representation of the natural numbers]]

* [[conatural number]]

* [[carrying]]

* [[currying]]

* [[numeral]]

* [[countable ordinal]]

## References

Origin of the [[Dedekind-Peano axioms]] for the [[natural numbers]]:

* [[Richard Dedekind]], *Was sind und was sollen die Zahlen?* (1888) &lbrack;scan: [pdf](https://rcin.org.pl/Content/37485/WA35_52499_2264brosz_Was-sind.pdf), [doi:10.1007/978-3-663-02788-1](https://doi.org/10.1007/978-3-663-02788-1)&rbrack;

* [[Richard Dedekind]] (transl. by W. Beman), _The nature and meaning of numbers_, Chapter II in: *Essays on the Theory of Numbers*, Chicago (1901) &lbrack;[Project Gutenberg](http://www.gutenberg.org/ebooks/21016), [pdf](https://www.gutenberg.org/files/21016/21016-pdf.pdf)&rbrack;

* [[Giuseppe Peano]], *Arithmetices principia, nova methodo exposita*, &lbrack;[Wikipedia](https://en.wikipedia.org/wiki/Arithmetices_principia,_nova_methodo_exposita)&rbrack;

Review:

* [[David E. Joyce]], *The Dedekind/Peano Axioms* (2005) &lbrack;[pdf](http://aleph0.clarku.edu/~djoyce/numbers/peano.pdf)&rbrack;

Broader historical review:

* [[Leo Corry]], *A Brief History of Numbers*, Oxford University Press (2015) &lbrack;[ISBN:9780198702597](https://global.oup.com/academic/product/a-brief-history-of-numbers-9780198702597)&rbrack;

[[!redirects whole number]]
[[!redirects whole numbers]]

[[!redirects natural number]]
[[!redirects natural numbers]]

[[!redirects nonnegative integer]]
[[!redirects nonnegative integers]]
[[!redirects positive integer]]
[[!redirects positive integers]]
[[!redirects unsigned integer]]
[[!redirects unsigned integers]]
