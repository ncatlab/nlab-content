
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

At certain [[integers]] $s = n$ the values $L(s)$ of  [[L-functions]] $L$ are typically of special interest, these are known as the "special values of L-functions".

For instance some of special values of the [[Riemann zeta function]] found (for the non-trivial region of non-positive integers) by [[Leonhard Euler]] in 1734 and 1749 are

| n | -5 | -3 | -1 |  0 | 2 | 4 | 6 | 8 |
|---|----|----|----|----|---|---|---|---|
| $\zeta(n)$ | $-\frac{1}{252}$ |  $\frac{1}{120}$ | $-\frac{1}{12}$ | $-\frac{1}{2}$ | $\frac{\pi^2}{6}$ | $\frac{\pi^4}{90}$ | $\frac{\pi^6}{945}$ | $\frac{\pi^8}{9450}$

where for instance the value $\zeta(-1) = -\frac{1}{12}$ turns out to be the [Euler characteristic of the moduli stack of complex elliptic curves](moduli+stack+of+elliptic+curves#EulerCharacteristic) and as such controls much of [[string theory]] (notably the critical dimension).

### Periods and Deligne's conjecture

More generally, it is known that for $K$ a [[number field]] and $\zeta_K$ its [[Dedekind zeta function]], then all values $\zeta_K(n)$ for integer $n$ happen to be [[periods]] ([MO comment](http://mathoverflow.net/a/54244/381)).

Based on this ([Deligne 79](#Deligne79)) identified _critical values_ of $L$-functions (at certain integers) and [[conjecture|conjectured]] that these all are algebraic multiples of [[determinants]] of [[matrices]] whose entries are [[periods]]. Review of this relation to periods in in ([Konsevich Zagier, section 3](#KonsevichZagier)).

Notice that under the [[function field analogy]] these arithmetic $L$-functions are supposed to be analogous to [[eta functions]] and [[zeta functions of elliptic differential operators]], which, when regarding these operators as [[Dirac operators]]/[[Hamiltonians]] encode [[partition functions]] and [[path integrals]] of [[quantum mechanical systems]], and that [[periods]] naturally appear as [[expectation values]] in [[quantum field theory]] (highlighted in [Kontsevich 99](deformation%20quantization#Kontsevich99)).


### Regulators and Beilinson's conjectures

Another kind of special value is given by the classical [[class number formula]] which says that the [[residue]] of the [[Dedekind zeta function]] $\zeta_K$ of a [[number field]] $K$ at $n = 1$ is proportional to the [[regulator of a number field|regulator of the number field]].

Also the [[Birch and Swinnerton-Dyer conjecture]] expresses the first non-vanishing [[derivative]] of the $L$-series of an [[elliptic curve]] over $\mathbb{Q}$ at $s= 1$ in terms of the [[regulator of a number field|regulator]].

Motivated by this ([Beilinson 85](#Beilinson85)) generalized both Deligne's conjecture and the statements about regulators by defining [[higher regulators]] ("Beilinson regulators") and conjecturing a general statement that expresses special values of $L$-function in terms of these, now known as _[[Beilinson's conjectures]]_.

### Periods and Scholl's conjecture

However ([Scholl 91](#Scholl91)) observed that also these [[Beilinson regulators]] have an expression in terms of [[periods]] and ([Konsevich Zagier, section 3.2 and 3.5](#KonsevichZagier)) advertises the 

**Deligne-Beilinson-Scholl conjecture**: _For $r$ the order of vanishing of a motivic $L$-function at some integer $n$, then the $r$th [[derivative]] of the function at that point is a [[period]]._

### Relative Langlands and boundary conditions in topological quantum field theory

Ongoing by work by [[David Ben-Zvi]], [[Yiannis Sakellaridis]], and [[Akshay Venkatesh]] relate special values of L-functions and periods to boundary conditions in a  [[topological quantum field theory]] approach to the [[Langlands program]] (see [BenZvi](#BenZvi)).

## Related concepts

* [[Beilinson conjectures]]


[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

Original article on the main conjectures are

* {#Deligne79} [[Pierre Deligne]], _Valeurs de fonctions $L$ et p&#233;riodes d'int&#233;grales_, in  _Automorphic forms, Representations, and $L$-functions_, Proc. Symp. Pure Math. 33, AMS (1979) pages 313-346

* {#Beilinson85} [[Alexander Beilinson]], _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070 ([web (Russian original)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng))

* {#Scholl91} [[Anthony Scholl]], _Remarks on special values of L-functions_, in J. Coates, M. Taylor (eds.) _$L$-Functins and Arithmetic_, London Math. Soc.  Lecture Notes 153, Cambridge University Press 1991, pages 373-392 ([pdf](https://www.dpmms.cam.ac.uk/~ajs1005/preprints/remarks.pdf))


Review and further developments:


* [[Michael Rapoport]], [[Norbert Schappacher]], [[Peter Schneider]] (eds.), _[[Beilinson's Conjectures on Special Values of L-Functions]]_  Perspectives in Mathematics, Volume 4, Academic Press, Inc. 1988 (ISBN:978-0-12-581120-0)

* {#KonsevichZagier} [[Maxim Kontsevich]], [[Don Zagier]], section 3 of _Periods_ ([pdf](http://www.ihes.fr/~maxim/TEXTS/Periods.pdf))


* {#Flach} [[Matthias Flach]], _The equivariant Tamagawa Number Conjecture: A survey_ ([pdf](http://www.math.caltech.edu/papers/baltimore-final.pdf))

* [[Bruno Kahn]], _Fonctions z&#234;ta et $L$ de vari&#233;t&#233;s et de motifs_, [arXiv:1512.09250](http://arxiv.org/abs/1512.09250v1).

* {#BenZvi} [[David Ben-Zvi]], _Relative Langlands_, MSRI lectures (notes taken by Jackson van Dyke) [pdf](https://www.msri.org/workshops/918/schedules/28233/documents/50487/assets/88599)

[[!redirects special value of an L-function]]