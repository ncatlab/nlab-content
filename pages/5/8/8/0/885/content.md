
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

A __natural number__ is traditionally one of the [[numbers]] $1$, $2$, $3$, and so on.  It is now common in many fields of mathematics to include $0$ as a natural number as well.  One advantage of doing so is that a natural number can then be identified with the [[cardinal number|cardinality]] of a [[finite set]], as well as a finite [[ordinal number]].  One can distinguish these as the __nonnegative integers__ (with $0$) and the __positive integers__ (without $0$), at least until somebody uses 'positive' in the semidefinite sense.  To a [[set theory|set theorist]], a natural number is essentially the same as an __[[integer]]__, so they often use the shorter word; one can also clarify with __unsigned integer__ (but this doesn\'t help with $0$).

The set of natural numbers is often written $N$, $\mathbf{N}$, $\mathbb{N}$, $\omega$, or $\aleph_0$.  The last two notations refer to this set\'s structure as an [[ordinal number]] or [[cardinal number]] respectively, and they often (usually for $\aleph$) have a subscript $0$ allowing them to be generalised.  In the [[foundations]] of mathematics, the [[axiom of infinity]] states that this actually forms a set (rather than a proper class).  At a foundational level, it\'s completely irrelevant whether $0$ counts as a natural number or not; as [[sets]] (and even as [[natural numbers objects]]), the two options are equivalent, so we are really talking about the choice of [[rig]] structure (or [[inclusion map]] into the set of [[integers]], etc).

By default, our natural numbers always include $0$.


## Natural numbers objects

$\mathbf{N}$ is a [[natural numbers object]] in [[Set]]; indeed, it is the original example.  This consists of an initial element $0$ (or $1$ if $0$ is not used) and a successor operation $n \mapsto n + 1$ (or simply $n \mapsto n^+$; in [[computer science]], one often writes $n+$) such that, for a set $X$, an element $a: X$, and a [[function]] $s: X \to X$, there exists a unique function $f: \mathbf{N} \to X$ such that $f_0 = a$ and $f_{n+1} = s(f_n)$. This function $f$ is said to be constructed by __primitive recursion__. (Fancier forms of [[recursion]] are also possible.)  

The basic idea is that we define the values of $f$ one by one, starting with $f_0 = a$, then $f_1 = s(a)$, $f_2 = s(s(a))$, and so on.  These are all both possible and necessary individually, but something must be put in the [[foundations]] to ensure that this can go on uniquely forever.


## Properties

### Minima of subsets of natural numbers

In [[classical mathematics]], any [[inhabited set|inhabited]] subset of the natural numbers possesses a minimal element. In [[constructive mathematics]], one cannot show this:

+-- {: .num_prop}
###### Proposition 
**(a Brouwerian counterexample)**

If any inhabited subset of the natural numbers possesses a minimal element, then the [[excluded middle|law of excluded middle]] holds.
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


## Related concepts

* [[number]], [[natural number]], [[integer]], [[rational number]], [[algebraic number]], [[Gaussian number]], [[irrational number]], [[real number]], [[p-adic number]]

* [[natural numbers type]], [[natural numbers object]]

* [[carrying]]

* [[numeral]]

* [[countable ordinal]]


[[!redirects natural number]]
[[!redirects natural numbers]]

[[!redirects nonnegative integer]]
[[!redirects nonnegative integers]]
[[!redirects positive integer]]
[[!redirects positive integers]]
[[!redirects unsigned integer]]
[[!redirects unsigned integers]]
