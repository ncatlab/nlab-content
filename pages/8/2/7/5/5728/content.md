[[!redirects Artin ring]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A **Artinian local ring** or **local Artinian ring** or **local Artin ring** or **Artin local ring** is a [[local ring]] which is also an [[Artinian ring]]. These are also called **Artinian local algebras**, **local Artinian algebras**, **Artin local algebras**, or **local Artin algebras**, since Artinian local rings are [[commutative algebras]] over the residue field $\mathbb{K}$. 

In [[synthetic differential geometry]], these Artinian local algebras are usually known as _[[infinitesimally thickened point|Weil algebras]]_. 

## Properties

Every Artinian local $\mathbb{K}$-algebra $A$ has a [[maximal ideal]] $\mathfrak{m}_A$, whose [[residue field]] $A / \mathfrak{m}_A$ is $\mathbb{K}$ itself. As a $\mathbb{K}$ [[vector space]] one has a splitting $A=\mathbb{K}\oplus \mathfrak{m}_A$. Moreover, the descending chain condition implies that $(\mathfrak{m}_A)^n=0$ for some $n\gg 0$, a consequence of [[Nakayama lemma]]. This implies that the maximal ideal is a [[nilradical]]. 

Given a field $K$ and a Artinian local $K$-algebra $A$, let $I$ be the [[nilradical]] of $A$. There is a function $v:I \to \mathbb{N}$ which takes a [[nilpotent element]] $r \in I$ to the least natural number $n$ such that $r^{v(r) + 1} = 0$, such that given [[nilpotent elements]] $r \in I$ and $s \in I$ and non-zero scalars $a \in K$ and $b \in K$,

* $v(a r + b s) = v(r) + v(s)$
* $v(r s) = \min(v(r), v(s))$

### Spectra

Passing from commutative rings to their spectra (in the sense of algebraic geometry), Artinian local algebras correspond to infinitesimal pointed spaces. As such, they appear as bases of deformations in [[infinitesimal object|infinitesimal]] [[deformation theory]]. For instance $Spec(\mathbb{K}[\epsilon]/(\epsilon^2))$ is the base space for 1-dimensional first order deformations. Similarly, $Spec(\mathbb{K}[\epsilon]/(\epsilon^{n+1}))$ is the base space for 1-dimensional $n$-th order deformations.

An Artinian local algebra has a unique [[prime ideal]], which means that its [[spectrum]] consists of a single point, i.e., $Spec(A)$ is trivial as a topological space. It is however non-trivial as a ringed space, since its ring of functions is $A$. By this reason spectra of Artinian local algebras are occasionally called _[[infinitesimally thickened point|fat points]]_ in the literature.

## Examples

* A classical example is the ring of [[dual numbers]] $\mathbb{K}[\epsilon]/(\epsilon^2)$ over a field $\mathbb{K}$.

* Every [[prime power local ring]] is a local Artinian ring. 

## See also

* [[Artinian ring]]

## References

* [[The Stacks Project]]

  * [10.100. Flatness criteria over Artinian rings](http://stacks.math.columbia.edu/tag/051E)

Local Artinian $\infty$-algebras are discussed in

* [[Jacob Lurie]], _Formal moduli problems_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-X.pdf))

[[!redirects local Artinian ring]]
[[!redirects local Artinian rings]]
[[!redirects Artinian local ring]]
[[!redirects Artinian local rings]]

[[!redirects local Artinian algebra]]
[[!redirects local Artinian algebras]]
[[!redirects Artinian local algebra]]
[[!redirects Artinian local algebras]]

[[!redirects local Artin ring]]
[[!redirects local Artin rings]]
[[!redirects Artin local ring]]
[[!redirects Artin local rings]]

[[!redirects local Artin algebra]]
[[!redirects local Artin algebras]]
[[!redirects Artin local algebra]]
[[!redirects Artin local algebras]]
