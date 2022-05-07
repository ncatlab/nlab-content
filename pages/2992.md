
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

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers. The positive integers are embedded into every [[commutative ring]] $R$: there is an injection $inj:\mathbb{N}^+\to\R$ such that $inj(1) = 1$ and $inj(s(n)) = inj(n) + 1$ for all $n:\mathbb{N}^+$. 

Suppose $R$ has an injection $inv:\mathbb{N}^+\to\R$ such that $inj(n) \cdot inv(n) = 1$ and $\inv(n) \cdot \inj(n) = 1$ for all $n:\mathbb{N}^+$. Then $R$ is called a __[[commutative algebra|$\mathbb{Q}$-algebra]]__, and the commutative ring of __rational numbers__ $\mathbb{Q}$ is the [[initial object|initial]] commutative $\mathbb{Q}$-algebra. 

It can then be proven from the ring axioms and the properties of the integers that every rational number apart from zero and has a multiplicative inverse, making $\mathbb{Q}$ a field.

### As an directed colimit in CRing

Let $(\mathbb{N},\leq)$ be the directed set of positive integers, and let $A:\mathbb{N}\to CRing$ be a family of [[commutative rings]] where $A_n$ is defined to be $\mathbb{Z}[1/n!]$, the [[localization of a commutative ring|localization]] of the [[integers]] $\mathbb{Z}$ [[localisation of a commutative ring away from an element|away from]] the [[factorial]] $n!$, and for $i, j:\mathbb{N}$, $i\leq j$, there is a commutative [[ring homomorphism]] from $f_{ij}:\mathbb{Z}[1/i!]\to\mathbb{Z}[1/j!]$, with $f_{ii}$ being the [[identity morphism|identity commutative ring homomorphism]] on $\mathbb{Z}[1/i!]$. Then the commutative ring of __rational numbers__ $\mathbb{Q}$ is the [[directed colimit]] $\underset{\to}\lim_i A_i$ of the system. 

### As an abelian group

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers and let $(\mathbb{Z},0,+,-,1)$ be the [[free abelian group]] on the set ${1}$.  

Let $A$ be an [[abelian group]] containing $\mathbb{Z}$ as an abelian subgroup. The positive integers are embedded into the [[function algebra|function abelian group]] $A \to A$, with $id_A:A \to A$ being the [[identity function]] on $A$; i.e. there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1) = id_A$ and $inj(s(n)) = inj(n) + id_A$ for all $n:\mathbb{N}^+$.

Suppose $A$ has an injection $inv:\mathbb{N}^+\to (A \to A)$ such that for all $n:\mathbb{N}^+$, $inj(n) \circ inv(n) = id_A$ and $inv(n) \circ inj(n) = id_A$. Then the abelian group of __rational numbers__ $\mathbb{Q}$ is the [[initial object|initial]] such abelian group. 

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

  * [[decimal rational number]]

* [[Q/Z]]
   
* [[algebraic number]]

* [[Gaussian number]]

* [[irrational number]]

* [[quadratic irrational number]]

* [[real number]]

* [[p-adic number]]

* [[rational numbers object]]

[[!redirects rational number]]
[[!redirects rational numbers]]
[[!redirects field of rational numbers]]
[[!redirects rationals]]