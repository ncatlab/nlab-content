
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
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

An __integer__ is a [[number]] that is a [[natural number]] or the [[negative number|negative]] of one.

The [[ring]] $\mathbb{Z}$ of all integers may defined as the [[free group]] on one generator or as the [[initial object|initial]] [[ring]]. 

In keeping with a historical point of view in which integers are natural numbers with a sign attached, one may write 

$$
  \mathbb{Z} = \{n, -n | n \in \mathbb{N}, 0 = -0\} = \{ \ldots, -3, -2, -1, 0, 1, 2, 3, \ldots \}
  \,.
$$

From an [[nPOV]], one may consider this as follows: $\mathbb{Z}$ is a [[filtered colimit]] of sets 

$$\mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \ldots$$ 

whereby $-n \in \mathbb{Z}$ is represented by the element $0$ in the $n^{th}$ copy of $\mathbb{N}$ appearing in this diagram (starting the count at the $0^{th}$ copy). The resulting induced map to the colimit 

$$\mathbb{N} \times \mathbb{N} \cong \sum_{m \in \mathbb{N}} \mathbb{N} \to \mathbb{Z}: (m, n) \mapsto n-m$$ 

imparts a monoid (in fact a group) structure on $\mathbb{Z}$ descended from the monoid structure on $\mathbb{N} \times \mathbb{N}$; compare double-entry bookkeeping in medieval mathematics (*[partita doppia](http://rfcwalters.blogspot.com/2011/02/mathematical-economics-double-entry.html)*). 

As a group, $\mathbb{Z}$ is [[abelian group|abelian]] and is the [[Grothendieck group]] of the [[monoid]] (or [[semigroup]]) $\mathbb{N}$ of [[natural numbers]].

The monoid of natural numbers is naturally even a [[rig]] -- in fact the [[initial object|initial]] rig -- and this multiplicative structure extends to $\mathbb{Z}$ to make it a [[ring]] -- in fact the initial ring.

## Properties ##

* The integers form a [[commutative ring]]. 

* The integers have [[decidable equality]] and [[decidable relation|decidable order]]. 

* The trivial ring is a [[tight apartness ring]] and a [[discrete ring]]. 

* The integers are a [[strictly weakly ordered ring]] and a [[lattice-ordered ring]]. 

* The integers are a [[metric space]] and a [[normed space]]. 

* The integers are a [[Euclidean domain]]

* The integers satisfy the Archimedean property, making it into an [[Archimedean integral domain]]. 

### Bijection of the integers with the natural numbers

The integers are in bijection with the natural numbers. Both the integers and the natural numbers are [[submonoids]] of the [[rational numbers]], with [[pointed set|pointed]] [[monoid]] [[monomorphisms]] 
$i_\mathbb{Z}:\mathbb{Z} \hookrightarrow \mathbb{Q}$ and $i_\mathbb{N}:\mathbb{N} \hookrightarrow \mathbb{Q}$ preserving addition, zero, and one. Let us take the relation on the rational numbers 
$$x:\mathbb{Q}, y:\mathbb{Q} \vdash \left| x + x + \frac{1}{2} \right| =_\mathbb{Q} y + \frac{1}{2}$$ 
The relation 
$$x:\mathbb{Z}, y:\mathbb{N} \vdash \left| i_\mathbb{Z}(x + x) + \frac{1}{2} \right| =_\mathbb{Q} i_\mathbb{N}(y) + \frac{1}{2}$$ 
is a [[one-to-one correspondence]], meaning that the integers are in bijection with the natural numbers. 

### Sequential Cauchy completeness

Let $x:\mathbb{N} \to \mathbb{Z}$ be a sequence of integers, and let $b:\mathbb{Z}$ be an integer. Then, there is a limit relation defined as

$$\mathrm{isLimit}(x, b) \coloneqq \forall \epsilon:\mathbb{Z}_+.\exists N:\mathbb{N}.\forall n:\mathbb{N}.(n \geq N) \to (\vert x(n) - b \vert \lt \epsilon)$$

This relation is a [[functional relation]], making the integers a [[sequentially Hausdorff space]]. 

A **modulus of Cauchy convergence** is a function $M:\mathbb{Z}_+ \to \mathbb{N}$ with a witness

$$p(M, x):\forall \epsilon:\mathbb{Z}_+.\forall m:\mathbb{N}.\forall n:\mathbb{N}.((m \geq M(\epsilon)) \wedge (n \geq M(\epsilon))) \to (\vert x(m) - x(n) \vert \lt \epsilon)$$

$\mathbb{Z}$ is [[sequentially Cauchy complete]] if every sequence with a modulus of Cauchy convergence has a unique limit. But $\mathbb{Z}$ is sequentially Cauchy complete, because the only sequences with a unique limit are those sequences for which there exists a natural number $N:\mathbb{N}$ such that for all natural numbers $m \geq N$ and $n \geq N$, $x(m) = x(n)$. The sequence $x$ has many moduli of Cauchy convergence $M$, where the natural number $N$ is given by $N = M(1)$. 

Since the integers are the [[initial object|initial]] [[Archimedean integral domain]], the integers are also the initial sequentially Cauchy complete Archimedean integral domain. Every other sequentially Cauchy complete Archimedean integral domain is provably an [[ordered field]] and has the [[HoTT book real numbers]] $\mathbb{R}$ as an integral subdomain. That means, in the context of the [[limited principle of omniscience]], the category of sequentially Cauchy complete Archimedean integral domains is equivalent to the [[walking arrow]], with objects $\mathbb{Z}$ and $\mathbb{R}$ and homomorphism $h:\mathbb{Z} \to \mathbb{R}$. 

### Cauchy completeness

Given a [[Tarski universe]] $(U, T)$ and a small type $A$ whose type reflection $T(A)$ is a [[directed set]], let $x:T(A) \to \mathbb{Z}$ be a [[net]] of integers, and let $b:\mathbb{Z}$ be an integer. Then, there is a limit relation defined as

$$\mathrm{isLimit}(x, b) \coloneqq \forall \epsilon:\mathbb{Z}_+.\exists N:T(A).\forall n:T(A).(n \geq N) \to (\vert x(n) - b \vert \lt \epsilon)$$

This relation is a [[functional relation]], making the integers a [[Hausdorff space]]. 

A **modulus of $U$-Cauchy convergence** is a function $M:\mathbb{Z}_+ \to T(A)$ with a witness

$$p(M, x):\forall \epsilon:\mathbb{Z}_+.\forall m:T(A).\forall n:T(A).((m \geq M(\epsilon)) \wedge (n \geq M(\epsilon))) \to (\vert x(m) - x(n) \vert \lt \epsilon)$$

$\mathbb{Z}$ is $U$-[[Cauchy complete]] if every net with a modulus of $U$-Cauchy convergence has a unique limit. But $\mathbb{Z}$ is $U$-Cauchy complete, because the only $U$-nets with a unique limit are those nets for which there exists an element $N:T(A)$ such that for all elements $m \geq N$ and $n \geq N$, $x(m) = x(n)$. The net $x$ has many moduli of $U$-Cauchy convergence $M$, where the element $N$ is given by $N = M(1)$. 

Since the integers are the [[initial object|initial]] [[Archimedean integral domain]], the integers are also the initial $U$-Cauchy complete Archimedean integral domain. Every other $U$-Cauchy complete Archimedean integral domain is provably an [[ordered field]] and has the $U$-[[Dedekind real numbers]] $\mathbb{R}$ as an integral subdomain. 

### Dedekind completeness

Let $\Omega$ be the [[type of all propositions]], so that the foundations is [[impredicative]]. A **Dedekind cut** is an pair $(L, U)$ of [[predicates]] such that 

* there exists an integer $a:\mathbb{Z}$ such that $L(a)$
* there exists an integer $b:\mathbb{Z}$ such that $U(b)$
* for all integers $a:\mathbb{Z}$, $L(a)$ if and only if there exists an integer $b:\mathbb{Z}$ such that $a \lt b$ and $L(b)$
* for all integers $b:\mathbb{Z}$, $U(b)$ if and only if there exists an integer $a:\mathbb{Z}$ such that $a \lt b$ and $U(a)$
* for all integers $a:\mathbb{Z}$, it is not true that $L(a)$ and $U(a)$
* for all integers $a:\mathbb{Z}$ and $b:\mathbb{Z}$, if $a \lt b$, then $L(a)$ and $U(b)$. 

There is a Dedekind cut for every integer $a:\mathbb{Z}$, given by $L_a(b) \coloneqq b \lt a$ and $U_a(b) \coloneqq a \lt b$. There are no other Dedekind cuts on the integers. Thus, the integers are Dedekind complete. 

Since the integers are the [[initial object|initial]] [[Archimedean integral domain]], the integers are also the initial Dedekind complete Archimedean integral domain. The only other Dedekind complete Archimedean integral domain is the [[Dedekind real numbers]] $\mathbb{R}$. That means, if there is a [[type of all propositions]], the category of Dedekind complete Archimedean integral domains is equivalent to the [[walking arrow]], with objects $\mathbb{Z}$ and $\mathbb{R}$ and homomorphism $h:\mathbb{Z} \to \mathbb{R}$. 

## Terminology

The underlying [[sets]] $\mathbb{Z}$ and $\mathbb{N}$ are [[isomorphic]]. Some subcultures of mathematics (and not only [[set theory|set theorists]]) use the term 'integer' synonymously for a natural number.  Computer scientists distinguish between 'unsigned integers' (natural numbers) and 'signed integers' (integers as described here).  Translations can also cause confusion with the term 'whole number'.

In [[number theory]], one generalises integers to [[algebraic integers]], an instance of the [[red herring principle]].  Accordingly, some number theorists will call the integers '[[rational integers]]' to clarify; $\mathbb{Z}$ is the [[ring of integers]] in the [[number field]] $\mathbb{Q}$ of [[rational numbers]].  (Compare, for example, [[Gaussian integers]] and [[Gaussian numbers]].)

The symbol '$\mathbb{Z}$' derives from the German word 'Zahlen', which is a generic word for 'numbers'.  (Compare [[Richard Dedekind|Dedekind]]\'s use of that word in the title of his famous book on the [[foundations]] of [[real numbers]].)

## Related concepts

* [[infinite cyclic group]]

* [[even number]], [[odd number]]

* [[natural number]], [[rational number]], [[real number]]

* [[algebraic integer]]

* [[ring of integers]]

* [[cyclotomic integer]]

* [[geometry]] modeled on the [[formal duality|formal dual]], [[Spec(Z)]], of the ring of integers is [[arithmetic geometry]]

* [[integers object]] in a [[topos]]

* [[rational zero theorem]]

* [[integers type]]

## References

The first characterization of the integers as an [[ordered integral domain]] appeared in:

* [[Hermann Grassmann]], _Lehrbuch der Arithmetik für höhere Lehranstalten_, Berlin: Enslin, 1861. ([Google Books](https://books.google.com/books?id=jdQ2AAAAMAAJ))

though the name "ordered integral domain" does not appear in the text. 

History:

* [[Leo Corry]], *A Brief History of Numbers*, Oxford University Press (2015) &lbrack;[ISBN:9780198702597](https://global.oup.com/academic/product/a-brief-history-of-numbers-9780198702597)&rbrack;

See also:

* Wikipedia, *[Integer](https://en.wikipedia.org/wiki/Integer)*

Formalization in [[univalent foundations of mathematics]] ([[homotopy type theory]] with the [[univalence axiom]]):

* {#UFP13} [[Univalent Foundations Project]], Rem. 6.10.7 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

and specifically in [[Agda]]:

* [[UniMath project]], *[agda-unimath/elementary-number-theory.integers](https://unimath.github.io/agda-unimath/elementary-number-theory.integers.html#1032)*

and specifically in [[cubical Agda]]

* [[1lab]], *[Data.Int](https://1lab.dev/Data.Int.html)*


[[!redirects integer]]
[[!redirects integers]]

[[!redirects integer number]]
[[!redirects integer numbers]]

[[!redirects additive group of integers]]
[[!redirects additive groups of integers]]

[[!redirects Z]]