
# Racks
* table of contents
{: toc}

## Idea

A rack is a set equipped with a binary operation satisfying axioms analogous to the second and third [[Reidemeister moves]] in knot theory.  The most commonly appearing racks in nature are [[quandle|quandles]], which satisfy an additional axiom analogous to the first Reidemeister move.

While mainly used to obtain invariants of framed knots, racks are interesting algebraic structures in their own right: they capture the idea of an algebraic structure where every element acts as an automorphism of that structure.


## Definition

A **rack** may be defined as a set $R$ with a binary operation $\triangleright$ such that
for every $a, b, c \in R$ the **[[self-distributive law]]** holds:

$$a \triangleright (b \triangleright c) = (a  \triangleright b)\triangleright (a \triangleright  c)$$

and for every $a,b \in R$ there exists a unique
$c \in R$ such that 

$$a \triangleright c = b$$

This definition, while terse and commonly used, is suboptimal for certain purposes because it contains an [[existential quantifier]] which is not really necessary. To avoid this,  we may write the unique $c \in R$ such that $a \triangleright c = b$ as $b \triangleleft a$.  We then have

$$ a \triangleright c = b \iff  c = b \triangleleft a $$

and thus 

$$ a \triangleright (b \triangleleft a) = b$$ 

and

$$(a \triangleright b) \triangleleft a = b$$

Using this idea, a rack may be equivalently defined as a set $R$ with two binary operations $\triangleright$ and $\triangleleft$ such that for all $a, b, c \in R$:

\[ a \triangleright (b \triangleright c) = (a \triangleright b)\triangleright (a \triangleright  c)   \]

\[ (c \triangleleft b) \triangleleft a = (c \triangleleft a)\triangleleft (b \triangleleft a)  \]

\[ (a \triangleright b)\triangleleft a = b \]

\[ a \triangleright (b \triangleleft a) = a \]

It is convenient to say that the element $a \in R$ is **acting from the left** in the expression $a \triangleright b$, and **acting from the right** in the expression $b \triangleleft a$.  The third and fourth rack axioms then say that these left and right actions are inverses of each other.  Using this, we can eliminate either one of these actions from the definition of rack.  If we eliminate the right action and keep the left one, we obtain the terse definition given initially.   However, the longer definition makes it clear that racks are algebras of [[Lawvere theory]].


## Notations and Conventions

Many different conventions are used in the literature on racks and quandles.  For example, many authors prefer to work with just the _right_ action.  Furthermore, the use of the symbols $\triangleright$ and $\triangleleft$ is by no means universal: many authors use exponential notation 

$$ a \triangleright b = {}^a b $$

and

$$ b \triangleleft a = b^{a} $$

while many others write

$$ b \triangleleft a = b \star a $$

We may equivalently define a rack in the following more conceptual manner: it is a set where each element acts on the left and right as [[automorphism|automorphisms]] of the rack, with the left action being the inverse of the right one.  In this definition, the fact that each element acts as automorphism encodes the left and right self-distributivity laws, and also these laws:

$$ a \triangleright (b \triangleleft c) = (a \triangleright b)\triangleleft (a \triangleright  c)$$ 

$$(c \triangleright b) \triangleleft a = (c \triangleleft a)\triangleright (b \triangleleft a)$$

which are consequences of the definition(s) given earlier.

## Shelves 

Even simpler than a rack is a [[shelf]].  Briefly, a set with a binary operation $\triangleright$ obeying the left self-distributive law

$$ a \triangleright (b \triangleright c) = (a \triangleright b)\triangleright (a \triangleright  c)   $$

is called a **left shelf**, and similarly a set with a binary operation $\triangleleft$ obeying the right self-distributive law is called a **right shelf**. 

See [[shelf]] for more details. 

## Related entries

* [[quandle]]

* [[shelf]]

## Links

* Gavin Wraith, [A personal story about knots](http://www.wra1th.plus.com/gcw/math/Rack.html).

* Wikipedia, [Racks and quandles](http://en.wikipedia.org/wiki/Racks_and_quandles).

* Sam Nelson, [Quandle theory](http://www.esotericka.org/cmc/quandles.html).

## References

* Nicol&#225;s Andruskiewitsch, Mati&#225;s Gra&#241;ab, _From racks to pointed Hopf algebras_, Adv. Math. __178__(2):177--243 (2003, [arxiv:math/0202084](https://arxiv.org/abs/math/0202084) (<a href="https://doi.org/10.1016/S0001-8708(02)00071-3">doi</a>)

* J. Scott Carter, _A survey of quandle ideas_, [arXiv](http://arxiv.org/abs/1002.4429).

The next reference makes it clear that racks are algebras of a [[Lawvere theory]], so that racks may be defined in any [[cartesian monoidal category]] (a category with finite [[products]]).

* Alissa Crans, _Shelves, racks, spindles and quandles_, [arXiv:math/0409602](https://arxiv.org/math/abs/pdf/0409602), in _Lie 2-Algebras_, p. 56.

* Roger Fenn, Colin Rourke, Brian Sanderson, _Trunks and classifying spaces_, Appl. Categ. Structures __3__ (1995), no. 4, 321--356 [MR1364012](https://www.ams.org/mathscinet-getitem?mr=1364012)[doi](https://doi.org/10.1007/BF00872903); _The rack space_, Trans. Amer. Math. Soc. __359__ (2007), no. 2, 701--740 [MR2255194](http://www.ams.org/mathscinet-getitem?mr=2255194)

* Colin Rourke, Roger Fenn, (1992). _Racks and links in codimension 2_. J. Knot Theory and Its Ramifications 1 (4): 343--406. 

* Seiichi Kamada, _Knot invariants derived from quandles and racks_, [arXiv:math/0211096](https://arxiv.org/abs/math/0211096).

* Markus Szymik, _Permutations, power operations, and the center of the category of racks_, Comm. Algebra 46 (2018) 230--240 [arXiv:1609.08687](https://arXiv.org/abs/1609.08687)

A generalization of [[Lie integration]] to conjectural Leibniz groups has been conjectured by [[J-L. Loday]]. A local version via local Lie racks has been proposed in

* Simon Covez, _The local integration of Leibniz algebras_, [arXiv:1011.4112](https://arxiv.org/abs/1011.4112); _On the conjectural cohomology for groups_, [arXiv:1202.2269](https://arxiv.org/abs/1202.2269); _L'int&#233;gration locale des alg&#232;bres de Leibniz_, Thesis (2010), [pdf](http://tel.archives-ouvertes.fr/docs/00/49/54/69/PDF/THESE_Simon_Covez.pdf)

There are also crossed modules for racks:

* Alissa S. Crans, Friedrich Wagemann, _Crossed modules of racks_, [arXiv:1310.4705](https://arxiv.org/abs/1310.4705)

[[!redirects rack]]
[[!redirects racks]]