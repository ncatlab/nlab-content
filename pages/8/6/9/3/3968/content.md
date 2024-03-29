
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

A **number field** is a [[finite number|finite]] [[field extension]] of the [[field]] of [[rational numbers]], $\mathbb{Q}$. 

In other words, a number field is a field $k$ of [[characteristic zero]] such that under the field [[homomorphism]] $i: \mathbb{Q} \hookrightarrow k$, the field $k$ is a [[finite number|finite]]-[[dimension|dimensional]] [[vector space]] over $\mathbb{Q}$ with respect to the scalar multiplication [[action]] of $\mathbb{Q}$

$$\mathbb{Q} \otimes k \stackrel{i \otimes 1}{\to} k \otimes k \stackrel{mult}{\to} k$$

on the underlying additive [[group]] of $k$. 

## Examples

* the [[rational numbers]] $\mathbb{Q}$;

* the [[Gaussian numbers]] $\mathbb{Q}(i)$;

* for certain $d$ the [[quadratic field]] $\mathbb{Q}(\sqrt{d})$;

* the [[cyclotomic fields]] $\mathbb{Q}(\zeta_n)$

Counterexamples:

* the [[real numbers]] $\mathbb{R}$ and [[complex numbers]] $\mathbb{C}$ are **not** number fields, since, while being [[vector spaces]] over $\mathbb{Q}$, they are not [[finite number|finite]] [[dimension|dimensional]] as $\mathbb{Q}$-vector spaces.

## Applications

Number fields are the basic objects of study in [[algebraic number theory]]. For example, one is typically interested in the arithmetic structure of $k$, including for example the structure of the ring of [[algebraic integer]]s $\mathcal{O}_k$ in $k$, the decomposition of primes in $\mathbb{Z}$ in terms of prime ideals in $\mathcal{O}_k$, the structure of the unit group of $\mathcal{O}_k$, the structure of the [[ideal class group]], the detailed study of the [[zeta function]] of $k$, and much more. 

## Properties

### As global fields

Number fields $k$ are examples of [[global field]]s, in fact they are the global fields of [[characteristic zero]]. They are often studied in terms of how they embed in their rings of [[adele ring|adeles]] $\mathbb{A}_k$, which are built from the [[local field|local completions]] of $k$. 

### Class number formula

Given a number field $K$, the [[Dedekind zeta function]] $\zeta_K$ of $K$ has a [[simple pole]] at $s = 1$. The _class number formula_ says that its [[residue]] there is proportional the product of the [[regulator of a number field|regulator]] with the [[class number]] of $K$

$$
  \underset{s\to 1}{\lim} (s-1) \zeta_K(s)
  \propto
  ClassNumber_K \cdot Regulator_K
  \,.
$$


### Function field analogy

[[!include function field analogy -- table]]

## Related concepts

* [[algebraic curve]]

* [[function field]]

## Literature

* {#NSW08} [[Jürgen Neukirch]], Alexander Schmidt, Kay Wingberg, *Cohomology of Number Fields*, Springer Grundlehren der mathematischen Wissenschaften **323**, Springer 2008 ([doi:10.1007/978-3-540-37889-1](https://link.springer.com/book/10.1007/978-3-540-37889-1), [webpage](https://www.mathi.uni-heidelberg.de/~schmidt/NSW2e/))


[[!redirects number fields]]

[[!redirects algebraic number field]]
[[!redirects algebraic number fields]]

