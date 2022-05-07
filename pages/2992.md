
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


# Rational numbers
* table of contents
{: toc}

## Definition

A _rational number_ is a [[fraction]] of two [[integer]] [[numbers]].

The [[field]] of **rational numbers**, $\mathbb{Q}$, is the [[field of fractions]] of the [[commutative ring]] of [[integers]], $\mathbb{Z}$, hence the field consisting of formal [[fractions]] ("[[ratios]]") of [[integers]].


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