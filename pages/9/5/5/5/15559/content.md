
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Dedekind zeta function_ is a generalization of the [[Riemann zeta function]] from the [[rational numbers]]/[[integers]] to [[number fields]]/their [[rings of integers]].

The analog for [[function fields]] is the [[Weil zeta function]], while the generalization to [[higher dimensional arithmetic geometry]] are the [[arithmetic zeta functions]].

## Properties

### Special values

For $K$ a [[number field]] then all [[special values of L-functions|special values]] of the Dedekind zeta function $\zeta_K(n)$ for integer $n$ happen to be [[periods]] ([MO comment](http://mathoverflow.net/a/54244/381)).

Based on this ([Deligne 79](#Deligne79)) identified _critical values_ of $L$-functions (at certain integers) and conjectured that these are all these are algebraic multiples of [[determinants]] of [[matrices]] whose entries are [[periods]]. For more on this see at _[[special values of L-functions]]_.

### Adelic integral expression

The Dedekind zeta function has an [[adelic integral]] expression in direct analogy to that of the [[Riemann zeta function]]. This is due to ([Tate 50](#Tate50)), highlighted by [[Ivan Fesenko]] in ([Goldfeld-Hundley 11, Interlude remark (1)](#GoldfeldHundley11)).

### Functional equation

The [[functional equation]] of the Dedekind zeta function follows from its [[adelic integral]] representation in direct analogy to how this works for the [[Riemann zeta function]]. This is due to ([Tate 50](#Tate50)), highlighted by [[Ivan Fesenko]] in ([Goldfeld-Hundley 11, Interlude remark (1)](#GoldfeldHundley11)).

### The pole and the class number formula

The Dedekind zeta function $\zeta_K$ of $K$ has a [[simple pole]] at $s = 1$. The _[[class number formula]]_ says that its [[residue]] there is proportional the the product of the [[regulator of a number field|regulator]] of $K$ with the [[class number]] of $K$

$$
  \underset{s\to 1}{\lim} (s-1) \zeta_K(s)
  \propto
  ClassNumber_K \cdot Regulator_K
  \,.
$$


### Relation to Hecke theta functions
 {#RelationToThetaFunctions}

The Dedekind zeta function has an expression as an integral over a kernel given by a [[Hecke theta function]] ([Kowalski (2.3) (2.4)](#Kowalski)).

### Relation to Hasse-Weil zeta function

The Dedekind zeta function of $K$ is equivalently the [[Hasse-Weil zeta function]] of $Spec(\mathcal{O}_K)$.

### Analogs over complex curves

The [[function field analogy]] in view of the discussion at _[[zeta function of an elliptic differential operator]]_ says that the Dedekind zeta function is [[analogy|analogous]] to the regulated [[functional determinant|functional trace]] of a would-be "[[Dirac operator]] on [[Spec(Z)]]".

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

Other identifications/analogies of the Riemann zeta function (and more generally the [[Dedekind zeta-function]]) with [[partition functions]] in [[physics]] have been proposed, in particular the _[[Bost-Connes system]]_.


[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]


### Function field analogy

[[!include function field analogy -- table]]

## References

* {#Tate50} [[John Tate]], _Fourier analysis in number fields, and Hecke's zeta-functions_, Algebraic Number Theory (Proc. Instructional Conf., Brighton, 1965), Thompson, Washington, D.C., pp. 305&#8211;34 1950


* Wikipedia, _[Dedekind zeta function](http://en.wikipedia.org/wiki/Dedekind_zeta_function)_

* E. Kowalski, section 1.4 of _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))


[[!redirects Dedekind zeta functions]]

[[!redirects Dedekind zeta-function]]
[[!redirects Dedekind zeta-functions]]