
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

__Motivic integration__ attaches to certain subsets of [[arc scheme]]s of varieties an element in a [[Grothendieck ring of varieties]] in a manner close in spirit to [[Euler characteristics]]. Technically it may be viewed as one of generalizations of [[p-adic integration]] to a geometric integration theory obtained by replacing the [[p-adic integers]] by a more broad class of rings. Some examples include [[formal power series ring]] over the [[complex numbers]], and more generally any henselian discretely valued fields of residual characteristic zero. [Recently](#References), these cases have been generalized to the case of any complete [[discrete valuation ring]] (whose [[residue field]] is [[perfect field|perfect]] in the [[mixed characteristic]] case).

In all of the described cases, the idea is to construct a suitable [[scheme]] over the residue field, called the [[arc space|arc scheme]] which serves as a suitable [[measure space]] on which functions are integrated; however, the value of integrals are not [[real number|real numbers]], but instead they are valued in the [[Grothendieck ring]] of varieties. In this sense, the value of a "motivic" integral is often regarded as a _geometric object_, rather than a numerical value.

The notion of arc scheme has a further generalization, known as a [[Greenberg scheme]].

## History

Motivic integration was introduced in the talk of [[Maxim Kontsevich]] at Orsay in 1995 in order to prove that [[Hodge numbers]] of [[Calabi-Yau manifolds]] are [[birational map|birational]] invariants. This talk also dealt with [[orbifold cohomology]] as well as 2 related papers of  [[Lev Borisov]]. The orbifold cohomology has been continued by Weimin Chen, [[Yongbin Ruan]] and collaborators, and later also by algebraic geometers Abramovich, Vistoli, and others. Batyrev is another contributor to both subjects in the context of physics.

Later, a more general framework of motivic integration in model theory has been put forward by Denef and Loeser, partly based on Denef's work on $p$-adic integration. More recent work using a model-theoretic approach is by Hrushovski and Kazhdan. 

## Related concepts

* [[p-adic integration]]

* [[motivic cohomology]]

* [[arc space]]

* [[Greenberg scheme]]

## References
 {#References}

A textbook account is in

*  {#CNS18} Antoine Chambert-Loir, Johannes Nicaise, Julien Sebag, _Motivic integration_, Progress in Mathematics 325 Birkhaeuser 2018 ([doi:10.1007/978-1-4939-7887-8](https://doi.org/10.1007/978-1-4939-7887-8))


See also

* Wikipedia _[Motivic integration](https://en.wikipedia.org/wiki/Motivic_integration)_

Lectures include

* Karen Smith, _Motivic integration_, ([pdf](http://www.msri.org/ext/shortermotivic2.pdf))
* Manuel Blickle, _A short course on geometric motivic integration_, [math.AG/0507404](http://arxiv.org/abs/math/0507404)
* [[Raf Cluckers]], _Motivic integration for dummies_, [pdf](http://wis.kuleuven.be/algebra/Raf/MForD.pdf), A course on motivic integration [I](http://wis.kuleuven.be/algebra/Raf/LaRoche3Cluckers.pdf), [II](http://wis.kuleuven.be/algebra/Raf/LaRoche3Cluckers.pdf), [III](http://wis.kuleuven.be/algebra/Raf/LaRoche3Cluckers.pdf)
* Julia Gordon, Yoav Yaffe, _An overview of arithmetic motivic integration_, [arxiv/0811.2160](http://arxiv.org/abs/0811.2160)
* [[Lou van den Dries]], _Lectures on motivic integration_ , Ms. University of Illinois at Urbana-Champaign. ([dvi](http://www.math.uiuc.edu/~vddries/mo.dvi))
* Thomas C. Hales, _What is motivic measure?_, [math.LO/0312229](https://arxiv.org/abs/math/0312229)

The concept originates from

* [[M. Kontsevich]], lecture on motivic integration, Orsay, December 7, 1995.

Original articles include the following:

* Jan Denef, [[François  Loeser]], _Definable sets, motives and $p$-adic integrals_,  J. Amer. Math. Soc. __14__ (2001),  no. 2, 429--469, [doi](http://dx.doi.org/10.1090/S0894-0347-00-00360-X)

* Jan Denef, Fran&#231;ois  Loeser, _Motivic integration and the Grothendieck group of pseudo-finite fields_ Proc. ICM, Vol. II (Beijing, 2002), 13--23, Higher Ed. Press, Beijing, 2002. 

* R. Cluckers, F. Loeser, _Constructible motivic functions and motivic integration_, Invent. Math. __173__ (2008), 23--121 [math.AG/0410203](http://arxiv.org/abs/math/0410203)

* Jan Denef, Fran&#231;ois  Loeser, _Germs of arcs on singular algebraic varieties and motivic integration_,  Invent. Math. __135__  (1999),  no. 1, 201--232.

* D. Abramovich, M. Mari&#241;o, M. Thaddeus, R. Vakil, _Enumerative invariants in algebraic geometry and string theory_, Lectures from the C.I.M.E. Summer School, Cetraro, June 6--11, 2005. Edited by Kai Behrend and Marco Manetti. LNIM 1947, Springer 2008. x+201 pp.

Hrushovski and Kazhdan studied motivic integration from [[model theory]] point of view:

* [[Ehud Hrushovski]], [[David Kazhdan]], _Motivic Poisson summation_, [arxiv/0902.0845](http://arxiv.org/abs/0902.0845)

* [[Ehud Hrushovski]], [[David Kazhdan]], _The value ring of geometric motivic integration and the Iwahori Hecke algebra of $SL_2$_, [math.LO/0609115](http://arxiv.org/abs/math/0609115); _Integration in valued fields_, in Algebraic geometry and number theory, 261&#8211;405, Progress. Math. __253__, Birkh&#228;user Boston, [pdf](http://math.huji.ac.il/~ehud/papers/intv-060428.pd

* [[David Kazhdan]], _Lecture notes in motivic integration_, with intro to logic and model theory, [pdf](http://www.ma.huji.ac.il/~kazhdan/Notes/motivic/b.pdf)
* R. Cluckers, J. Nicaise, J. Sebag (Editors), _Motivic Integration and its Interactions with Model Theory and Non-Archimedean Geometry_, 2 vols.
London Mathematical Society Lecture Note Series __383__, __384__ 
* Raf Cluckers, Julia Gordon, Immanuel Halupczok, _Motivic functions, integrability, and uniform in p bounds for orbital integrals_, [arxiv:1309.0594](https://arxiv.org/abs/1309.0594)

* Julien Sebag, _Int&#233;gration motivique sur les sch&#233;mas formels_,  Bull. Soc. Math. France __132__:1 (2004) 1--54, [MR2005e:14017](https://mathscinet.ams.org/mathscinet-getitem?mr=2075915) 

* Takehiko Yasuda, _Motivic integration over Deligne-Mumford stacks_ (2004) arXiv:[math/0312115](https://arxiv.org/abs/math/0312115)

* [[Michael Larsen]], [[Valery Lunts]], _Motivic measures and stable birational geometry_, Mosc. Math. J. 3 (2003), no. 1, 85--95, 259, [math.AG/0110255](http://arxiv.org/abs/math/0110255), [MR2005a:14026](http://www.ams.org/mathscinet-getitem?mr=1996804), [journal](http://www.ams.org/distribution/mmj/vol3-1-2003/abst3-1-2003.html#larsen-lunts_abstract); _Rationality criteria for motivic zeta functions_, Compos. Math. __140__ (2004), no. 6, 1537--1560, [math.AG/0212158](https://arxiv.org/abs/math/0212158)
* [[Alexei Bondal]], [[Michael Larsen]], [[Valery Lunts]], _Grothendieck ring of pretriangulated categories_, Int. Math. Res. Not. 2004, no. 29, 1461--1495, [math.AG/0401009](https://arxiv.org/abs/math/0401009)

* Emmanuel Bultot, _Motivic integration and logarithmic geometry_, PhD thesis [arxiv/1505.05688](https://arxiv.org/abs/1505.05688)

 
[[!redirects motivic measure]]