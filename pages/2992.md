
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Rational numbers
* table of contents
{: toc}

## Definition

A _rational number_ is a [[fraction]] of two [[integer]] [[numbers]].

### As a field

The [[field]] of **rational numbers**, $\mathbb{Q}$, is the [[field of fractions]] of the [[commutative ring]] of [[integers]], $\mathbb{Z}$, hence the field consisting of formal [[fractions]] ("[[ratios]]") of [[integers]].

### As a commutative ring

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers. Then there exist [[commutative rings]] $R$ with injections $inj,inv:\mathbb{N}^+\to\R$ satisfying the following axioms:

* $inj(1) = 1$
* $inj(s(n)) = inj(n) + 1$ for all $n:\mathbb{N}^+$
* $inj(n) \cdot inv(n) = 1$ for all $n:\mathbb{N}^+$. 

The first two axioms state that there is an embedding of the positive integers in $R$, amd the third axiom states that every positive integer has a multiplicative inverse. The commutative ring of rational numbers $\mathbb{Q}$ is the [[initial object|initial]] such commutative ring, and general commutative rings satisfying the axioms above are called [[commutative algebra|commutative $\mathbb{Q}$-algebras]]. 

It can then be proven from the commutative ring axioms that every rational number apart from zero has a multiplicative inverse, making $\mathbb{Q}$ a field.

### As an abelian group

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers and let $(\mathbb{Z},0,+,-,1)$ be the [[free abelian group]] on the set ${1}$.  

Let $A$ be an [[abelian group]] containing $\mathbb{Z}$ as an abelian subgroup. There are injections $inj,inv:\mathbb{N}^+\to (A \to A)$ satisfying the following axioms for all $a:A$:

* $inj(1)(a) = a$
* $inj(s(n))(a) = inj(n)(a) + a$ for all $n:\mathbb{N}^+$
* $inj(n)(inv(n)(a)) = a$ and $inv(n)(inj(n)(a)) = a$ for all $n:\mathbb{N}^+$. 

The abelian group of rational numbers $\mathbb{Q}$ is the [[initial object|initial]] abelian group satisfying the above axioms. 

## Properties

### Algebraic closure

The [[algebraic closure]] $\overline{\mathbb{Q}}$ of the rational numbers is called the [[field]] of _[[algebraic numbers]]_. The [[absolute Galois group]] $Gal(\overline{\mathbb{Q}}\vert \mathbb{Q})$ has some curious properties, see [there](absolute+Galois+group#OfTheRationalNumbers).

### Topologies

There are several interesting [[topological space|topologies]] on $\mathbb{Q}$ that make $\mathbb{Q}$ into a [[topological group]] under addition, allowing us to define interesting fields by taking the [[complete space|completion]] with respect to this topology:

1.  The _[[discrete topology]]_ is the most obvious, which is already complete.

2.  The _absolute-value topology_ is defined by the [[metric space|metric]] $d(x,y) \coloneqq {|x - y|}$; the completion is the field of [[real numbers]]. 

    (This topology is [[totally disconnected space|totally disconnected]] ([this exmpl.](totally+disconnected+space#RationalNumbersAreTotallyDisconnected)))

3.  Fixing a [[prime number]] $p$, the _$p$-adic topology_ is defined by the [[ultrametric]] $d(x,y) \coloneqq 1/n$ where $n$ is the highest exponent on $p$ in the [[prime factorization]] of ${|x - y|}$; the completion is the field of $p$-[[adic number|adic numbers]].

According to [[Ostrowski's theorem]] this are the only possibilities.

Interestingly, (2) cannot be interpreted as a [[locale|localic]] group, although the completion $\mathbb{R}$ can.  (Probably the same holds for (3); I need to check.)


## Related concepts

* [[natural number]]

* [[integer]]

* **rational number**

  * a finite [[field extension]] of $\mathbb{Q}$ is called a _[[number field]]_

  * [[dyadic rational number]]

* [[Q/Z]]

* [[quadratic number]]
   
* [[algebraic number]]

* [[Gaussian number]]

* [[irrational number]]

* [[real number]]

* [[p-adic number]]

* [[rational numbers object]]

[[!redirects rational number]]
[[!redirects rational numbers]]
[[!redirects field of rational numbers]]
[[!redirects rationals]]