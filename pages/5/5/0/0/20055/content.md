
# Semi-left-exact left Bousfield localizations

* table of contents
{: toc}

## Idea

When constructing a general [[left Bousfield localization]] of a [[cofibrantly generated model category]] $C$ at a set of maps $S$, it is fairly straightforward to construct a localization functor, i.e. a fibrant replacement functor for the putative localized model category $L_S C$, by a small object argument.  We represent the maps in $S$ by cofibrations between cofibrant objects, take their pushout products with all boundary inclusions $\partial \Delta^n \hookrightarrow \Delta^n$ (assuming for simplicity that $C$ is a [[simplicial model category]]), and add all the generating acyclic cofibrations of $C$.  Then an object $Z$ has the right lifting property with respect to this set if and only if it is fibrant in $C$ (because we added the generating acyclic cofibrations of $C$) and for all $f:A\to B$ in $S$ the induced map $Map(B,Z) \to Map(A,Z)$ of simplicial mapping spaces (which is a fibration since $f$ is a cofibration and $Z$ is fibrant) is an acyclic fibration, i.e. $Z$ is $S$-local.  However, it is much harder to construct a factorization of an *arbitrary* map as an $S$-acyclic cofibration followed by an $S$-fibration --- one has to use a cardinality argument to obtain a set of generating $S$-acyclic cofibrations --- and accordingly the $S$-fibrations have no explicit description.

This can be seen as a homotopy-theoretic analogue of the construction of a [[reflective factorization system]].  The localization functor exhibits the $S$-local objects as a reflective subcategory, while the $S$-acyclic cofibrations and $S$-fibrations are a model-categorical representation of the corresponding reflective factorization system, whose left class consists of the morphisms inverted by the reflector (here, the $S$-local equivalences) and whose right class is defined by orthogonality to these.  Even in 1-category theory, constructing reflective factorizations requires finicky cardinality or size-based arguments as well.  However, there are some reflections, such as the [[semi-left-exact reflections]], for which the reflective factorization system can be constructed by a direct argument in one step.  The homotopy-theoretic analogue of these is a **semi-left-exact left Bousfield localization**.


## Construction

The following is Theorems 9.3 and 9.7 from [Bousfield 2001](#Bousfield01).

\begin{theorem}
  Let $C$ be a [[proper model category]] and $Q:C\to C$ a functor equipped with a natural transformation $\alpha:Id\to Q$ such that

  1. $Q$ is a [[homotopical functor]], i.e. preserves weak equivalences.
  2. For each $X\in C$, the maps $\alpha_{Q X}$ and $Q \alpha_X$ are weak equivalences $Q X \to Q Q X$.
  3. Define an object $X$ to be $Q$-local if $X\to Q X$ is a weak equivalence, and define a morphism $f$ to be a $Q$-equivalence if $Q f$ is a weak equivalence.  Then pullback along fibrations between $Q$-local fibrant objects preserves $Q$-equivalences.

  Then there is a new model structure $C^Q$ on $C$ whose cofibrations are those of $C$, whose weak equivalences are the $Q$-equivalences, and whose fibrations are the maps whose $\alpha$-naturality-square is a [[homotopy pullback]].  Moreover, $C^Q$ is also proper, and simplicial if $C$ is.
\end{theorem}

The first two conditions say essentially that $Q$ is a homotopical reflection into some subcategory (namely the $Q$-local objects).  The third condition says that it is semi-left-exact (a 1-categorical reflection of $C$ into $B\subseteq C$ is semi-left-exact if and only if pullback along morphisms in $B$ preserves morphisms that are inverted by the reflector).

For details of the proof, see [Bousfield 2001](#Bousfield01), and [Bousfield-Friedlander 78](#BousfieldFriedlander78) which proved a less powerful version.  The central point is the construction of the factorization into an $S$-acyclic cofibration and an $S$-fibration, which proceeds by first applying $Q$ along with fibrant replacement, then taking a homotopy pullback: the same way that a [[reflective factorization system]] is constructed from a [[semi-left-exact reflection]] in 1-category theory.


## Remarks

* Right properness of semi-left-exact left Bousfield localizations was also shown in [Gepner-Kock, Prop. 7.8](#GK), with special attention paid to [[type-theoretic model categories]].

* Nullification, i.e. localization at a family of maps $A\to \ast$, is always semi-left-exact.  (Indeed, nullification is what in [[homotopy type theory]] is called a [[higher modality]], and has [[stable units|reflection with stable units]], a stronger condition.)

* [[left-exact reflection|Left exact]] reflections are always semi-left exact.  In particular, the left-exact localizations that present [[Grothendieck (∞,1)-toposes]] can be constructed in this way.


## References

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], def. 1.1.6 in _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf))

* {#Bousfield01} [[Aldridge Bousfield]], *On the telescopic homotopy theory of spaces*, Trans. Amer. Math. Soc. 353 (2001), 2391-2426, [web with fulltext](https://www.ams.org/journals/tran/2001-353-06/S0002-9947-00-02649-0/)

* {#Hirschhorn} [[Philip Hirschhorn]], chapter 13 of _Model Categories and Their Localizations_, 2003 ([AMS](http://www.ams.org/bookstore?fn=20&arg1=whatsnew&item=SURV-99), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))
 
* {#CHK} Cassidy and H&#233;bert and [[Max Kelly|Kelly]], "Reflective subcategories, localizations, and factorization systems".  *J. Austral. Math Soc. (Series A)* 38 (1985), 287--329 ([pdf](http://journals.cambridge.org/download.php?file=%2FJAZ%2FJAZ1_38_03%2FS1446788700023624a.pdf&code=5796045be8904c5183c2e95bce65491e))

* {#GK} [[David Gepner]] and [[Joachim Kock]], *Univalence in locally cartesian closed categories*, [arxiv:1208.1749](https://arxiv.org/abs/1208.1749)


[[!redirects semi-left-exact left Bousfield localization]]
[[!redirects semi-left-exact left Bousfield localizations]]
[[!redirects semi-left-exact Bousfield localization]]
[[!redirects semi-left-exact Bousfield localizations]]

[[!redirects locally cartesian left Bousfield localization]]
[[!redirects locally cartesian left Bousfield localizations]]
[[!redirects locally cartesian Bousfield localization]]
[[!redirects locally cartesian Bousfield localizations]]
