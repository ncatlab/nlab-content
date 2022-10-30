+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

__Topological Hochschild__ (resp. __topological cyclic__,  survey is in ([May](#May)) __homology__ is a refinement of [[Hochschild homology]]/[[cyclic homology]] from [[commutative rings]]/algebras to the [[higher algebra]] of [[ring spectra]]/[[E-∞ rings]]/[[E-∞ algebras]]. 

In particular, given a ring $R$, then there is a natural morphism of [[spectra]] 

$$
  \array{
     && \mathbf{TC}(R)
     \\
      & {}^{\mathllap{cyclotomic \atop trace}}\nearrow & \downarrow
     \\
     \mathbf{K}(R) &\underset{}{\longrightarrow}& \mathbf{THH}(R)
  }
$$

from the [[algebraic K-theory]] spectrum to the [[topological Hochschild homology]] spectrum, the [[Dennis trace]] map. Since Hochschild homology spectra are naturally [[cyclotomic spectra]], that factors through the topological cyclic homology spectrum via a map called the _[[cyclotomic trace]]_ which much like a [[Chern character]] map for [[algebraic K-theory]].

The spectra $THH(R)$ and $TC(R)$ are typically easier to analyze than $K(R)$. Moreover, the difference between them and $K(R)$ is "locally constant" ([Dundas-Goodwillie-McCarthy13](#DundasGoodwillieMcCarthy13)) and often otherwise bounded in complexity. Accordingly, $THH$ and $TC$ are in practice computationally useful approximations to $K$.

There are various generalizations:

1. Just as for basic Hochschild homology, there is _higher topological Hochschild homology_ ([Carlsson-Douglas-Dundas 08](#CarlssonDouglasDundas08)) given not just by [[derived loop spaces]] but by derived mapping spaces out of higher dimensional [[tori]].

1. Just as algebraic K-theory generalizes from [[E-∞ rings]] to [[stable ∞-categories]], so does $TC$ and the cyclotomic trace map ([Blumberg-Gepner-Tabuada 11](#BlumbergGepnerTabuada11))

## Related concepts

* [[cyclic homology]]

* [[Chern character]]

* [[norm cofibration]]

## References

### General

The original references are

* [[Marcel Bökstedt]], _Topological Hochschild homology_, Bielefeld, 1985, 1988

* [[Marcel Bökstedt]], W.C. Hsiang, [[Ib Madsen]], _The cyclotomic trace and algebraic K-theory of spaces_, Invent. Math. __111__ (1993), 463-539, [MR94g:55011](http://www.ams.org/mathscinet-getitem?mr=1202133), [doi](http://dx.doi.org/10.1007/BF01231296)

* [[Marcel Bökstedt]], [[Ib Madsen]], _Topological cyclic homology of the integers_, $K$-theory (Strasbourg, 1992). Ast&#233;risque __226__ (1994), 7&#8211;8, 57&#8211;143.

and a further generalization is defined in 
 
* [[Bjørn Ian Dundas]], Randy McCarthy, _Topological Hochschild homology of ring functors and exact categories_, J. Pure Appl. Algebra __109__ (1996), no. 3, 231&#8211;294, [MR97i:19001](http://www.ams.org/mathscinet-getitem?mr=1388700), <a href="http://dx.doi.org/10.1016/0022-4049(95)00089-5">doi</a>

Higher topological Hochschild Homology is discussed in

* {#CarlssonDouglasDundas08} [[Gunnar Carlsson]], [[Christopher Douglas]], [[Bjørn Ian Dundas]], _Higher topological cyclic homology and the Segal conjecture for tori_, 
Adv. Math. __226__ (2011), no. 2, 1823&#8211;1874, ([arXiv:0803.2745](http://arxiv.org/abs/0803.2745), [MR2737802](http://www.ams.org/mathscinet-getitem?mr=2737802), [doi](http://dx.doi.org/10.1016/j.aim.2010.08.016))


Review and exposition includes

* {#May} [[Peter May]], _Topological Hochschild and Cyclic Homology and Algebraic K-theory_ ([pdf](http://www.math.uchicago.edu/~may/TALKS/THHTC.pdf))

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], chapter IX of _[[Rings, modules and algebras in stable homotopy theory]]_, AMS Mathematical Surveys and Monographs Volume 47 (1997) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))


* {#DundasGoodwillieMcCarthy13} [[Bjørn Dundas]], [[Thomas Goodwillie]], [[Randy McCarthy]], _The local structure of algebraic K-theory_, Springer 2013 ([pdf](http://math.mit.edu/~nrozen/juvitop/dundas.pdf))


* {#Gerhardt14} [[Teena Gerhardt]], _Computations in algebraic K-theory_, talk at [CUNY Workshop on differential cohomologies 2014](http://qcpages.qc.cuny.edu/~swilson/cunyworkshop14.html) ([video recording](http://videostreaming.gc.cuny.edu/videos/video/1800/in/channel/55/))

* Ricardo Andrade, _THH notes_, MIT juvitop seminar [pdf](http://math.mit.edu/~nrozen/juvitop/ra%20-%20juvitop.pdf), babytop seminar [pdf](http://math.mit.edu/~nrozen/juvitop/ra%20-%20babytop.pdf)

* Anatoly Preygel, _Hochschild homology notes_, juvitop seminar, [pdf](http://math.mit.edu/~nrozen/juvitop/note_hh_talk.pdf)

* Thomas Geisser, _Motivic Cohomology, K-Theory and Topological Cyclic Homology_, Handbook of K-theory II.1, [pdf](http://www.math.uiuc.edu/K-theory/handbook/1-193-234.pdf)

* Ib Madsen, _Algebraic K-theory and traces_, [pdf](http://math.mit.edu/~nrozen/juvitop/madsen.pdf)


Abstract characterization of the [[Dennis trace]] and cyclotomic trace is discussed in

* {#BlumbergGepnerTabuada11} [[Andrew Blumberg]], [[David Gepner]], [[Goncalo Tabuada]], _Uniqueness of the multiplicative cyclotomic trace_, Advances in Mathematics 260 (2014) 191-232 ([arXiv:1103.3923](http://arxiv.org/abs/1103.3923))

See also

* T. Pirashvili, F. Waldhausen, _Mac Lane homology and topological Hochschild homology_, J. Pure Appl. Algebra __82__ (1992), 81-98, [MR96d:19005](http://www.ams.org/mathscinet/search/mathscinet-getitem?mr=520492), <a href="http://dx.doi.org/10.1016/0022-4049(92)90012-5">doi</a>

* [[T. Pirashvili]], _On the topological Hochschild homology of $\mathbf{Z}/p^k\mathbf{Z}$_, Comm. Algebra __23__ (1995), no. 4, 1545&#8211;1549, [MR97h:19007](http://www.ams.org/mathscinet-getitem?mr=1317414), [doi](http://dx.doi.org/10.1080/00927879508825293)

* Z. Fiedorowicz, T. Pirashvili, R. Schw&#228;nzl, R. Vogt, F. Waldhausen, _Mac Lane homology and topological Hochschild homology_, Math. Ann. __303__ (1995), no. 1, 149&#8211;164, [MR97h:19007](http://www.ams.org/mathscinet-getitem?mr=1348360), [doi](http://dx.doi.org/10.1007/BF01460984) 

* [[Bjørn Ian Dundas]], _Relative K-theory and topological cyclic homology_, Acta Math. __179__ (1997), 223-242, ([publisher](http://link.springer.com/article/10.1007%2FBF02392744))


* Thomas Geisser, Lars Hesselhoft, _Topological cyclic homology of schemes_, in: Algebraic $K$-theory (Seattle, WA, 1997), 41&#8211;87, Proc. Sympos. Pure Math. __67__, Amer. Math. Soc. 1999, [MR2001g:19003](http://www.ams.org/mathscinet-getitem?mr=1743237); [K-theory archive](http://www.math.uiuc.edu/K-theory/0231/)

* R. McCarthy, _Relative algebraic K-theory and topological cyclic homology_, Acta Math. __179__ (1997), 197-222.


* J. McClure, R. Staffeldt, _On the topological Hochschild homology of $b u$, I_, [pdf](http://math.mit.edu/~nrozen/juvitop/mcclure.pdf)

* Daniel Joseph Vera, _Topological Hochschild homology of twisted group algebra_, MIT Ph. D. thesis 2006, [pdf](http://dspace.mit.edu/bitstream/handle/1721.1/34615/71329129.pdf?sequence=1)


* V. Angeltveit, A. Blumberg, T. Gerhardt, M. Hill, T. Lawson, M. Mandell, _Topological cyclic homology via the norm_ ([arXiv:1401.5001](http://arxiv.org/abs/1401.5001))

### Examples
 {#ReferencesExamples}

THH and TC specifically of [[KU|ku]] and [[KO|ko]] is discussed in 

* [[Christian Ausoni]], [[John Rognes]], _Algebraic K-theory of topological K-theory_, Acta Mathematica March 2002, Volume 188, Issue 1, pp 1-39 ([KTheory 0405](http://www.math.uiuc.edu/K-theory/0405/))

* [[Vigleik Angeltveit]], [[Michael Hill]], [[Tyler Lawson]], _Topological Hochschild homology of $\ell$ and $ko$_ ([arXiv:0710.4368](http://arxiv.org/abs/0710.4368))

* [[Andrew Blumberg]], [[Michael Mandell]], _Localization for $THH(ku)$ and the topological Hochschild and cyclic homology of Waldhausen categories_ ([arXiv:1111.4003](http://arxiv.org/abs/1111.4003))


and of [[tmf]] in 

* [[Bob Bruner]], [[John Rognes]], _Topological Hochschild homology of topological modular forms_ 2008 ([pdf](http://folk.uio.no/rognes/papers/ntnu08.pdf))


[[!redirects topological Hochschild homology]]

[[!redirects THH]]
[[!redirects TC]]