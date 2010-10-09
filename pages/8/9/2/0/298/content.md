[[!redirects vertex operator algebras]]

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The usual definition of _vertex operator algebra_ (VOA) is long and unenlightning. But due to work by Huang and Kong it is now known that vertex operator algebras are equivalent to certain [[FQFT]]s (see also [[CFT]]):

There is a [[monoidal category]] or [[operad]] whose [[morphism|morphisms]] are conformal spheres with $n$-punctures marked as incoming and one puncture marked as outgoing (each puncture equipped with a conformally parametrized annular neighborhood). Composition of such spheres is by gluing along puctures. This can be regarded as a category $2Cob_{conf}^0$ of 2-dimensional genus-0 conformal [[cobordism|cobordisms]].

As shown by theorems by Yi-Zhi Huang and Liang Kong, a vertex operator algebra is precisely a _[[holomorphic representation]]_ of this category, or [[algebra over an operad]] for this [[operad]] i.e. an genus-0 [[conformal field theory|conformal]] [[FQFT]], hence a [[monoidal functor]]

$$
  V : 2Cob_{conf}^0 \to Vect
$$

such that its component $V_1$ is a holomorphic function on the moduli space of conformal punctured spheres.

## Examples

* [[Moonshine]]

## References

The original article with the interpretation of vertex operator algebras as holomorphic algebras over the holomorphic punctured sphere operad is

* Yi-Zhi Huang, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA __88__ (1991) pp. 9964-9968

A standard textbook summarizing these results is

* Yi-Zhi Huang, _Two-dimensional conformal geometry and vertex operator algebras_, Progr. in Math. Birkhauser 1997, [gbooks](http://books.google.hr/books?isbn=0817638296)

As mentioned in the [acknowledgements](http://books.google.com/books?id=SUUdknTpYjEC&pg=PR11&lpg=PR11&dq=%22vertex+operator+algebras%22+%22trimble%22&source=bl&ots=v3GHx_ra2M&sig=TW5MzAtDi4n_gJjvUHb6eELoAXQ&hl=en&ei=9jdnSoXqKJiCtge6xqDuDw&sa=X&oi=book_result&ct=result&resnum=4) there, [[Todd Trimble]] and [[Jim Stasheff]] had a hand in making the operadic picture manifest itself here. Other operadic approaches are known, e.g. an earlier one in 

* Bojko Bakalov, Alessandro D'Andrea, Victor G. Kac, _Theory of finite pseudoalgebras_, Adv. Math. __162__ (2001), no. 1, 1--140, [MR2003c:17020](http://www.ams.org/mathscinet-getitem?mr=2003c:17020) 

and even earlier treatments via coloured operads and [[generalized multicategories]], for references (Snydal, Soibelman, Beilinson-Drinfeld) see [[relaxed multicategory]].  

More recently Huang's student Liang Kong has been developing these results further, generalizing them to open-closed CFTs and to non-chiral, i.e. completely general CFTs. See 

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008), [math.QA/0610293](http://arxiv.org/abs/math/0610293).

See also:

* Igor Frenkel, James Lepowsky, Arne Meurman, _Vertex operator algebras and the monster_, Pure and Applied Mathematics __134__, Academic Press, New York 1998.

* Edward Frenkel, David Ben-Zvi: _Vertex algebras and algebraic curves_, Math. Surveys and Monographs __88__, AMS 2001,
xii+348 pp. (Bull. AMS. [review](http://www.ams.org/journals/bull/2002-39-04/S0273-0979-02-00955-2/S0273-0979-02-00955-2.pdf), [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1106.17035&format=complete))

* Victor Kac: _Vertex algebras for beginners_, Amer. Math. Soc.  ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0924.17023&format=complete))

An algebrogeometric version is due Beilinson and Drinfel'd and called the [[chiral algebra]].

There is an interesting theory of deformation quantization of VOAs from

* [[Pavel Etingof]], [[David Kazhdan]], _Quantization of Lie bialgebras. V. Quantum vertex operator algebras_, 
Selecta Math. (N.S.) 6 (2000), no. 1, 105--130, [MR2002i:17022](http://www.ams.org/mathscinet-getitem?mr=2002i:17022)

* E. Frenkel, N. Reshetikhin, _Towards deformed chiral algebras_, [q-alg/9706023](http://arXiv.org/abs/q-alg/9706023)

and of chiral algebras due [[Dmitry Tamarkin]].

* Ruthi Hortsch, Igor Kriz, Ales Pultr, _A universal approach to vertex algebras_, [arxiv/1006.0027](http://arxiv.org/abs/1006.0027)

Much algebraic insight to algebaric structures in CFT is in unfinished notes

* [[A. Beilinson]], [[B. Feigin]], B. Mazur, _Notes on conformal field theory_, &lt;http://www.math.sunysb.edu/~kirillov/manuscripts.html>

[[!redirects vertex algebra]]