# Idea

Grothendieck has developed a deep version of _differential calculus_, based on a linearization of $O_X$-bimodules. It is also related to the (de Rham) descent data for the stack of $O_X$-modules over the simplicial scheme resolving the diagonal of $X$. As abstract [[descent]] data correspond to the flat [[connections]] for the corresponding [[monad]], this was historically the first case in which this correspondence was noted; in positive characteristics Grothendieck called the corresponding descent data for the de Rham site "costratifications", the corresponding connection is nowdays called [[Grothendieck connection]], see [Berthelot, Ogus 1978](#BerthelotOgus) for the fundamentals and the related notion of [[crystal (algebraic geometry)]].

This corresponds to looking at a sequence of infinitesimal neighborhoods of the diagonal. This geometrical principle can be applied to other categories; it is the basis of the study of [[jet schemes]] and close in spirit to some constructions in synthetic differential geometry.

## Definitions

Given a commutative unital ring $R$, a filtration $M_n$ ($n\geq -1$) on a $R$-$R$-bimodule $M$ is a __differential filtration__ if the commutator $[r,P]$ for any $P$ in $M_n$ and $r$ in $R$ is in $M_{n-1}$, and $M_{-1} = 0$. A bimodule is differential if it has an exhaustive ($\cup_N M_n = M$) differential filtration. Every $R$-$R$-bimodule has a __differential part__, i.e. the maximal differential submodule of $M$. 

__Regular differential operators__, as defined by Grothendieck, are the elements of the differential part $Diff(R,R)$ of $Hom(R,R)$ i.e. a maximal differential subbimodule in  $Hom(R,R)$. The operators in $Diff(R,R)_n$ are called the differential operators of degree $\leq n$. 
If $R\to B$ is a ring morphism, then the differential part of $B$ via its natural $R$-$R$-bimodule structure is also an object of $R\backslash \mathrm{Ring}$; in particular $Diff(R,R)$ is a ring and $R\hookrightarrow Diff(R,R)$ is an embedding of rings.

More generally (and in the affine case equivalently), for a $S$-scheme $X$, let $P^n_{X/S}$ denote the sheaf $(O_X\otimes_{f^{-1}(O_S)} O_X)/I^{n+1}$, where $I$ is the ideal of the diagonal (this makes sense since the diagonal morphism is an immersion, cf. EGAI, 5.3.9.), and $f:X\rightarrow S$ the structure morphism. Consider $P^n_{X/S}$ as $O_X$-module via the morphism $O_X\rightarrow O_X\otimes_{f^{-1}(O_S)} O_X$, $a\mapsto a\otimes 1$.

For $O_X$-modules $E,F$,  $Diff_S(F,E)_n$ is defined to be $Hom_{O_X}(P_{X/S}^n\otimes_{O_X} F, E)$. Note that $P^n_{X/S}$ has two canonical structures as $O_X$-module given by the projections $p_i: X \times_S X\rightarrow X$. The tensor product $P_{X/S}^n \otimes_{O_X} F$ is understood to be constructed via $p_1$ and considered as an $O_X$-module via $p_0$.

## Properties

In the affine case, and in characteristics zero, the sheaf of regular differential operators is locally isomorphic to the [[Weyl algebra]]. For that simple case, a good reference is [Coutinho 1995](#Coutinho1995).

## Noncommutative analogues

Regular differential operators have been nontrivially generalized to noncommutative rings (and schemes) by V. Lunts and [[Alexander Rosenberg|A. L. Rosenberg]], as well as to the setting of [[braided monoidal categories]]. Their motivation is an analogue of a Beilinson-Bernstein localization theorem for [[quantum groups]]. The category of differential bimodules is categorically characterized in their work as the minimal [[coreflective subcategory|coreflective]] [[topologizing subcategory| topologizing]] [[monoidal category|monoidal]] subcategory of the abelian monoidal category of $R$-$R$-bimodules which is containing $R$. In the case of noncommutative rings, Lunts-Rosenberg definition of differential operators has been recovered from a different perspective in the setup of [[noncommutative algebraic geometry]] represented by monoidal categories; the emphasis is on the duality between infinitesimals and differential operators, see [Maszczyk 2006](#Maszczyk2006).

See also [[regular differential operator in noncommutative geometry]].

## References

* {#BerthelotOgus} P. Berthelot,  A. Ogus, _Notes on crystalline cohomology_, Princeton Univ.P. 1978. vi+243, ISBN0-691-08218-9
* {#Coutinho1995} S. C. Coutinho, _A primer of algebraic $D$-modules_, London Math. Soc. Stud. Texts __33__, Cambridge University Press, Cambridge, 1995. xii+207 pp.
* {#Maszczyk2006} [[Tomasz Maszczyk]], _Noncommutative geometry through monoidal categories_, [arXiv:0611806](http://arxiv.org/abs/math/0611806)

For regular differential operators in Lie theory see 

* [[I. N. Bernstein]], [[I. M. Gelfand]], [[S. I. Gelfand]], _Differential operators on the base affine space and a study of $\mathfrak{g}$-modules_, In: I. M. Gelfand, ed., Lie groups and their representations, 21--64. Adam Hilger, 1975

Lunts-Rosenberg work in noncommutative setting

* V. A. Lunts, A. L. Rosenberg, _Differential operators on noncommutative rings_, Selecta Math. (N.S.)  __3__:3  (1997) 335--359 ([doi](https://doi.org/10.1007/s000290050014))

* [[V. A. Lunts]], [[A. L. Rosenberg]], _Localization for quantum groups_, Selecta Math. (N.S.) __5__:1 (1999) 123--159 ([doi](https://doi.org/10.1007/s000290050044)).

* V. A. Lunts, A. L. Rosenberg, _Differential calculus in noncommutative algebraic geometry I. D-calculus on noncommutative rings_, MPI 1996-53 [pdf](http://www.mpim-bonn.mpg.de/preblob/3894)

* V. A. Lunts, A. L. Rosenberg, _Differential calculus in noncommutative algebraic geometry II. D-Calculus in the braided case. The localization of quantized enveloping algebras, MPI 1996-76 [pdf](http://www.mpim-bonn.mpg.de/preblob/3916)


MO questions

* MathOverflow: [Equivalence of "Weyl Algebra" and "Crystalline" definitions of rings of differential operators between modules?](http://mathoverflow.net/questions/210891/equivalence-of-weyl-algebra-and-crystalline-definitions-of-rings-of-differen), [Ring of differential operators of a quotient ring](http://mathoverflow.net/questions/194218/ring-of-differential-operators-of-a-quotient-ring)

category: algebraic geometry

[[!redirects regular differential operators]]
