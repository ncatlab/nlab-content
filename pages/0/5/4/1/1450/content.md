#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

In _synthetic differential geometry_ one formulates [[differential geometry]] axiomatically in [[topos]]es -- called [[smooth topos]]es --  of [[generalized smooh space]]s. 

The main point of the axioms is to ensure that a well defined notion of [[infinitesimal space]]s exist in the topos, whose existence concretely and usefully formalizes the wide-spread but often vague intuition about te role of infinitesimals in [[differential geometry]].

In particular, in such toposes $T$ there exists an [[infinitesimal space]] $D$ that behaves like the [[infinitesimal object|infinitesimal interval]] in such a way that for any space $X \in T$ the [[tangent bundle]] of $X$, is, again as an object of the topos, just the [[internal hom]] $T X \;\text{:=}\; X^T$ (using the notation of [[exponential object]]s in the [[cartesian closed category]] $T$). So a tangent vector in this context literally is an _infinitesimal path_ in $X$.

This way, in [[smooth topos]]es it is possible to give precise well-defined meaning to many of the familiar computations -- wide-spread in particular in the [[physics]] literature -- that compute with supposedly "infinitesimal" quantities.

As quoted by Anders Kock in his book (see below), Sophus Lie once said that he found his main theorems in [[Lie theory]] using "synthetic reasoning", but had to write them up in non-synthetic style (see [[analytic versus synthetic]]) through lack of a formalized language.  Synthetic differential geometry does provides this formalized language.


## axiomatics ## 

The axioms of synthetic differential geometry demand that the [[topos]] $T$ of smooth spaces is 

* a [[smooth topos]] (see there for details)

in which in particular 

* [[infinitesimal space]]s exists and

* satisfy the [[Kock-Lawvere axiom]].

With that little bit of axiomatics alone, a large amount of [[differential geometry]] may be formulated. This has been carried through quite comprehensively by [[Anders Kock]], see the [reference](#References) below. 

In his work he particularly makes use of the fact that as sophisticated as a [[smooth topos]] may be when explicitly constructed (see the section on [models](#models)), being a [[topos]] means that one can reason inside it almost literally as in [[Set]]. Using this Kock's work gives descriptions of synthetic differential geometry which are entirely intuitive and have no esoteric topos-theoretic flavor. All he needs is the assumption that the [[Kock-Lawvere axiom]] is satisfied for "numbers". Here "numbers" is really to be interpreted in the topos, but if one just accepts that they satisfy the KL axiom, one may work with infinitesimals in this context in essentially precisely the naive way, with the topos theory in the background just ensuring that everything makes good sense.

## models ##

Being exiomatic, reasoning in synthetic differential geometry applies in every **model** for the axioms, i.e. in every concrete choice of [[smooth topos]] $T$.

Models of [[smooth topos]]es tend to be inspired, but more general than, constructions familiar from [[algebraic geometry]]. In particular the old insight promoted by [[Grothendieck]] in his work, that nilpotent ideals in [[ring]]s are formal duals of spaces with infinitesimal extension is typically used to model [[infinitesimal space]]s in synthetic differential geometry.

The main difference between models for [[smooth topos]]es  and  [[algebraic geometry]] from this perspective is that models for [[smooth topos]] tend to employ test spaces that are _richer_ than plain formal duals to commutative [[ring]]s or algebras, as in [[algebraic geometry]]: typical models for synthetic differential geometry use test spaces given by formal duals of [[generalized smooth algebras]] that remember "smooth structure" in the usual sense of [[differential geometry]] (and different from, though not entirely unrelated, to the notion of [[smooth scheme]] in algebraic geometry). This is in particular true for the [well adapted models](#well adapted models).

However, with a a sufficiently general perspective on [[higher geometry]] one finds that algebraic geometry and  synthetic differential geometry are both special cases of a more general notion of theories of generalized spaces. For more on this see [[generalized scheme]].

## well adapted models ##

A [[topos]] $T$ modelling the axioms of synthetic differential geometry is called **(well) adapted** if the ordinary [[differential geometry]] of [[manifolds]] embeds into it, in particular if there is a [[full and faithful functor]] [[Diff]] $\to T$ from the category of ordinary smooth [[manifold]]s into $T$. 

A standard model for well adapted synthetic toposes is obtained in terms of sheaves on duals of "germ determined" $C^\infty$-rings. This is described in great detail in the textbook _[[Models for Smooth Infinitesimal Analysis]]_. 

The conception and discussion of these well adapted toposes goes back to E. Dubuc, who studied them in a long series of articles. He <a href="http://north.ecc.edu/alsani/ct99-00(8-12)/msg00218.html">asks</a> people to refer it this topos as the **[[Dubuc topos]]**. 

This theory of well-adapted models was later summarized and extended in the standard textbook

* [[Ieke Moerdijk]] [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ 



# Variations #

## higher categorical versions ##

* Synthetic differential geometry may be thought of as embedded in the general theory of [[derived smooth manifolds]] and, generally, that of [[generalized schemes]].

## supergeometry  versions ##

The notion of synthetic differential geometry extends to the context of [[supergeometry - contents|supergeometry]]. See

* [[synthetic differential supergeometry]].


# Related entries #

* [[infinitesimal singular simplicial complex]]

  * [[differential forms in synthetic differential geometry]]

  * [[Chevalley-Eilenberg algebra in synthetic differential geomet|Chevalley-Eilenberg algebra in synthetic differential geometry]]

# References #

The idea of axiomaizing [[differential geometry]] using [[topos]] theory originates in 

* [[Bill Lawvere]], _Categorical dynamics_, lecture (1967)

The first model for the axioms presented there served to demonstrate that the theory is non-empty, but was hard to work with. Much of the later work was concerned with refining the model-building. For instance

* E. Dubuc, _Sur la mod&egrave;le de la g&eacute;ometrie diff&eacute;rrentielle synth&eacute;tique_, Cahier Top et G&eacute;om. Diff. XX-3 (1979)

## Books ##

The textbooks by [[Anders Kock]]

*  [[Anders Kock]], _Synthetic Differential Geometry_, ([pdf])

*  [[Anders Kock]], _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

develop in great detail the theory of [[differential geometry]] using using the axioms of synthetic differential geometry. The main goal in these books is to demonstrate how these axioms lead to a very elegant, very intuitive and very comoprehensive conception of differential geometry. Accordingly, concrete models (whose explicit description is typically much more evolved than the nice axiomatics that holds once they have been constructed) play a minor role in these books.

Somewat complementary to that, the book

* [Ieke Moerdijk]], [[Gonzalo Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ 

focuses on concrete constructions of well-adapted models using the technology of [[generalized smooth algebra]]s ($C^\infty$-rings). 

Another testbook is

* R. Lavendhomme, _Basic concepts of synthetic differential geometry_, Kluwer, Dordrecht (1996)

## Expositions ##

Two useful introductory expositions of basic ideas of synthetic differential geometry are

*  [Mike Shulman], __Chicago Pizza-Seminar: Synthetic Differential Geometry ([pdf](http://www.math.uchicago.edu/~shulman/exposition/sdg/pizza-seminar.pdf))

*  [John Bell], _An invitation to smooth infinitesimal analysis_ ([pdf](http://publish.uwo.ca/~jbell/invitation%20to%20SIA.pdf))

# Discussion #

+-- {: .query}

[[Eric]]: Mike, have you ever looked into [stochastic calculus](http://en.wikipedia.org/wiki/It%C5%8D%27s_lemma)? I was looking at your "pizza seminar" and was left with the thought that stochastic calculus might also be presented in terms of synthetic differential geometry. To do so, you need a slightly different class of elements $\delta$ such that that $\delta^2\in D$ and $d\delta = 0$. Then the 2-dimensional Taylor expansion becomes the [Ito lemma](http://en.wikipedia.org/wiki/It%C5%8D%27s_lemma):

$$f(t+d,w+\delta) =  f(t,w) + \left(\frac{\partial f}{\partial t} + \frac{1}{2}\frac{\partial^2 f}{\partial w^2}\right) d + \frac{\partial f}{\partial w} \delta.$$

Just curious...

[[Eric]]: On second thought, $d\delta = 0$ is probably too strong. You could probably get away with $d\delta = -\delta d$.

[[Mike Shulman]]: No, I haven't looked into stochastic calculus; that's an interesting idea.  But I don't know what $d\delta$ means.

[[David Roberts]]: the product, presumably. So Eric seems to be proposing a second lot of infinitesimals $D'$ such that the product of two things in $D'$ are in $D$ and (in the first version) the product of something in $D$ and something in $D'$ vanishes, or in the second version that the product $D\times D' \to R$ is antisymmetric.

[[Mike Shulman]]: Sorry, I guess I wasn't quite awake enough to guess that Eric meant "for any $d\in D$."  The usual models of SDG do contain pretty much any sort of infinitesimal you want; you can make that precise by talking about polynomial rings of nilpotents.

[[Eric]]: Thanks for clarifying that David. So I think we can define a "synthetic stochastic calculus". We need a set of elements $D'$ that are like "square roots of infinitesimals" in the sense that they square to infinitesimals, i.e. for any $\delta\in D'$, we have $\delta^2\in D$. To get the synthetic stochastic calculus, we need elements in $D$ and $D'$ to anti-commute. Hmm... this makes me wonder if there is a synthetic differential graded algebra where you have differentials of different (possibly fractional) degrees.

=--
