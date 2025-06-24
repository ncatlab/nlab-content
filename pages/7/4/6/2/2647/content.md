
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Some authors use "tensor category" essentially as a synonym for ([[symmetric monoidal category|symmetric]]) [[monoidal categories]] (e.g. [Davydov 1998](#Davydov98), [Kashiwara & Schapira 2006, Def. 4.2.1](#KashiwaraSchapira06)).

These days, a _tensor category_ is usually understood to be a [[monoidal category]] equipped with further "[[linear algebra|linear algebraic]]" [[properties]] and [[structure]], hence with [[monoidal category|monoidal]]-[[structure]] given by a kind of [[tensor product]] in the original sense (i.e. actually being a universal [[bilinear map]] of sorts) whence the name.

Conventions differ, but at the very least one means 

* a [[monoidal category]],

which is at times required to be

* [[symmetric monoidal category|symmetric monoidal]] 

  (e.g [Deligne 1990](#Deligne90) in (2.1.1); [Davydov 1998](#Davydov98) says "tensor category" for [[symmetric monoidal categories]] and "quasitensor category" for [[braided monoidal categories]]),

* ([[Ab]], [[tensor product of abelian groups|$\otimes$]])-[[enriched category|enriched]] or ([[Vect]],[[tensor product of vector spaces|$\otimes$]])-[[enriched category|enriched]],

  to make an [[enriched monoidal category]]  

and, in addition, often

* [[additive category|additive]] (symmetric) monoidal, so that the [[tensor product]] [[preserved limit|preserves]] [[finite product|finite]] [[direct sums]], 

* [[abelian category|abelian]] (symmetric) monoidal, in which the [[tensor product]] [[preserved colimit|preserves]] [[finite colimits]] in separate arguments, 

* with [[dual objects]], making a [[rigid monoidal category]].

## Properties 

### Tannaka theory, Deligne's theorem, super-representation theory

[[Deligne's theorem on tensor categories]] ([Deligne 02](#Deligne02)) establishes [[Tannaka duality]] between sufficiently well-behaved linear tensor categories in [[characteristic zero]] and [[supergroups]], realizing these tensor categories as [[categories of representations]] of these supergroups.

## Related concepts

* [[fusion category]]

* [[tensor triangulated category]]

* [[tensor (∞,1)-category]]

* [[2-algebraic geometry]]

* [[tensor network]]


## References

* {#Deligne90} [[Pierre Deligne]], section 2 of: _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. **87** (1990) 111-195 ([pdf](https://publications.ias.edu/sites/default/files/60_categoriestanna.pdf))

* {#Davydov98} [[Alexei Davydov]]: *Monoidal categories and functors*, Chapter 1 in: *Monoidal Categories*, J. Math. Sci.(New York) **88** (1998) 457-519 &lbrack;[doi:10.1007/BF02365309](https://doi.org/10.1007/BF02365309)&rbrack;

* [[Bojko Bakalov]], [[Alexander Kirillov]], *Lectures on tensor categories and modular functors*, University Lecture Series **21**, Amer. Math. Soc. (2001) &lbrack;[webpage](http://www.math.stonybrook.edu/~kirillov/tensor/tensor.html), [ams:ulect/21](https://bookstore.ams.org/view?ProductCode=ULECT/21), [pdf](http://math.bu.edu/people/jackwalt/research/tqft-seminar/refs/tensor_cat_mod_func.pdf)&rbrack;

  > (focus on [[Reshetikhin-Turaev construction]] of [[modular functors]] from [[modular tensor categories]])

* {#KashiwaraSchapira06} [[Masaki Kashiwara]], [[Pierre Schapira]], Section 4 of: *[[Categories and Sheaves]]*, Grundlehren der Mathematischen Wissenschaften **332**, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;

* [[Damien Calaque]], [[Pavel Etingof]], _Lectures on tensor categories_, IRMA Lectures in Mathematics and Theoretical Physics 12, 1-38 (2008) ([arXiv:math/0401246](https://arxiv.org/abs/math/0401246))

* [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], _Topics in Lie theory and Tensor categories -- 9 Tensor categories_, Lecture notes (spring 2009) ([pdf](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec09.pdf) [web](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/)) 

* {#EGNO15} [[Pavel Etingof]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *Tensor Categories*, AMS Mathematical Surveys and Monographs **205** (2015) &lbrack;[ISBN:978-1-4704-3441-0](https://bookstore.ams.org/surv-205), [pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf)&rbrack;

* [[Alexei Davydov]]: *Tensor categories*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2311.05789](https://arxiv.org/abs/2311.05789)&rbrack;

[[Deligne's theorem on tensor categories]] is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

Review in:

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

On [[quotient object|quotients]] of tensor categories:

* Zhenbang Zuo, Gongxiang Liu. *Quotient Category of a Multiring Category* (2024). ([arXiv:2403.06244](https://arxiv.org/abs/2403.06244)).

On the full dualizability of certain finite braided tensor categories:

* [[Thibault Decoppet]]. *Relative Invertibility and Full Dualizability of Finite Braided Tensor Categories* (2025). ([arXiv:2506.16241](https://arxiv.org/abs/2506.16241)).




[[!redirects quasitensor category]]

[[!redirects tensor categories]]