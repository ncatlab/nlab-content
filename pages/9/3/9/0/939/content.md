# Distributive laws

* table of contents
{:toc}

## Idea

Sometimes in [[mathematics]] we want to consider objects equipped with two different types of [[structure]] which interact in a suitable way.  For instance, a [[ring]] is a [[set]] equipped with both (1) the structure of an (additive) [[abelian group]] and (2) the structure of a (multiplicative) [[monoid]], which satisfy the distributive laws $a\cdot (b+c) = a\cdot b + a\cdot c$ and $a\cdot 0 = 0$.

Abstractly, there are two [[monads]] on the [[category]] [[Set]], one (call it $\mathbf{T}$) whose [[algebra over a monad|algebras]] are abelian groups, and one (call it $\mathbf{S}$) whose algebras are monoids, and so we might ask "can we construct, from these two monads, a third monad whose algebras are rings?"  Such a monad would assign to each set $X$ the [[free object|free]] ring on that set, which consists of formal sums of formal products of elements of $X$---in other words, it can be identified with $T(S(X))$.  Thus the question becomes "given two monads $\mathbf{T}$ and $\mathbf{S}$, what further structure is required to make the composite $T S$ into a monad?"

It is easy to give $T S$ a unit, as the composite $Id \xrightarrow{\eta^S} S \xrightarrow{\eta^T} T S$, but to give it a multiplication we need a transformation from $T S T S$ to $T S$.  We naturally want to use the multiplications $\mu^T\colon T T \to T$ and $\mu^S\colon S S \to S$, but in order to do this we first need to switch the order of $T$ and $S$.  However, if we have a transformation $\lambda\colon S T \to T S$, then we can define $\mu^{T S}$ to be the composite $T S T S \xrightarrow{\lambda} T T S S \xrightarrow{\mu^T\mu^S} T S$.

Such a transformation, satisfying suitable axioms to make $T S$ into a monad, is called a *distributive law*, because of the motivating example relating addition to multiplication in a ring.  In that case, $S T X$ is a formal product of formal sums such as $(x_1 + x_2 + x_3)\cdot (x_4 + x_5)$, and the distributive law $\lambda$ is given by multiplying out such an expression formally, resulting in a formal sum of formal products such as $x_1\cdot x_4 + x_1 \cdot x_5 + x_2 \cdot x_4 + x_2 \cdot x_5 + x_3\cdot x_4 + x_3 \cdot x_5$.


## Big picture

[[monad|Monads]] in any [[2-category]] $C$ make themselves a 2-category $\mathrm{Mnd}$ in which 1-cells are either lax or colax morphisms of monads;
by dualization the same is true for [[comonads]]. Monads internal to the 2-category of monads are called _distributive laws_. In particular, distributive laws themselves make a 2-category. There are other variants like distributive laws between a monad and an [[endofunctor]], "mixed" distributive laws between a monad and a comonad (the variants for algebras and coalgebras called [[entwining structure]]s), distributive laws between actions of two different monoidal categories on the same category, for [[PROP]]s and so on. Having a distributive law $l$ from one monad to another enables to define the composite monad $\mathbf T\circ_l\mathbf P$. This correspondence extends to a 2-functor $\mathrm{comp}:\mathrm{Mnd}(\mathrm{Mnd}(C))\to\mathrm{Mnd}(C)$. An analogue of this 2-functor in the mixed setup is a homomorphism of bicategories from the bicategory of entwinings to a bicategory of [[coring]]s.

## Explicit definition

A __distributive law__ from a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ in $A$ to an endofunctor
$P$ is a 2-cell $l : T P \Rightarrow P T$ such that
$l \circ (\eta^T)_P = P(\eta^T)$ and
$l \circ (\mu^T)_P = P(\mu^T) \circ l_T \circ T(l)$. The latter identitity is the commutativity of the pentagon
$$\array{
T T P&\stackrel{T l}\to&T P T&\stackrel{l T}\to&P T T\\
\downarrow \mu^T P&&&&\downarrow P\mu^T\\
T P &&\stackrel{l}\to && P T
}$$
Distributive laws from the monad $\mathbf{T}$ to the endofunctor $P$ are in a canonical bijection with lifts of $P$ to an endofunctor $P^{\mathbf T}$ in the [[Eilenberg-Moore category]] $A^{\mathbf T}$,
satisfying $U^{\mathbf T} P^{\mathbf T} = P U^{\mathbf T}$. Indeed, the endofunctor $P^{\mathbf T}$
is given by $(M,\nu) \mapsto (P M,P(\nu)\circ l_M)$.

A __distributive law__ from a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ to a monad
$\mathbf{P} = (P, \mu^P, \eta^P)$ in $A$ 
(or _of_ $\mathbf T$ _over_ $\mathbf P$)
is a distributive law from $\mathbf T$ to the endofunctor $P$,
compatible with $\mu^P,\eta^P$ in the sense that
$l \circ T(\eta^P) = (\eta^P)_T$ and
$l \circ T(\mu^P) = (\mu^P)_T \circ P(l) \circ l_P$. Thus all together a distributive law from a monad to an endofunctor is a 2-cell for which 2 triangles and 2 pentagons commute. In the entwining case, 
Brzezi&#324;ski and Majid combined the 4 diagrams into one picture which they call the _bow-tie diagram_. 

##Literature##
H. Appelgate, M. Barr, J. Beck, F. W. Lawvere, F. E. J. Linton, E, Manes, M. Tierney, F. Ulmer, Seminar on triples and categorical homology theory, ETH 1966/67, edited by B. Eckmann, LNM 80, Springer 1969.
(includes article Jon Beck, Distributive laws, pages 119--140).

Michael Barr, Charles Wells, _Toposes, triples and theories_, Springer-Verlag 1985; [web remake at TAC](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html) 

G. B&#246;hm, _Internal bialgebroids, entwining structures
and corings_, AMS Contemp. Math. 376 (2005) 207--226; [arXiv:math.QA/0311244](http://front.math.ucdavis.edu/math.QA/0311244)

[[T. Brzeziński]], [[S. Majid]], _Coalgebra bundles_, Comm. Math. Phys.  191  (1998),  no. 2, 467--492 ([arXiv version](http://arxiv.org/abs/q-alg/9602022)).

T. Brzezi&#324;ski, R. Wisbauer, _Corings and comodules_, London Math. Soc. Lec. Note Series 309, Cambridge 2003.

T. F. Fox, M. Markl, _Distributive laws, bialgebras, and cohomology_,  Operads: Proceedings of Renaissance Conferences (Hartford, CT/Luminy, 1995),  167--205, 
Contemp. Math. 202, AMS 1997. 

S. Lack, _Composing PROPS_, [Theory Appl. Categ.](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html) 13 (2004), No. 9, 147--163.

S. Lack, R. Street, _The formal theory of monads II_, Special volume celebrating the 70th birthday of Professor Max Kelly.
J. Pure Appl. Algebra 175 (2002), no. 1-3, 243--265. 

M. Markl, _Distributive laws and Koszulness_,  Ann. Inst. Fourier (Grenoble)  46  (1996),  no. 2, 307--323 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=AIF_1996__46_2_307_0))

[[Ross Street|R. Street]], _The formal theory of monads_, J. Pure Appl. Alg. 2, 149--168 (1972)

[[Z. Škoda]], _Distributive laws for monoidal categories_ ([arXiv:0406310](http://front.math.ucdavis.edu/math.CT/0406310)); _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_ ([arXiv:0707.1609](http://front.math.ucdavis.edu/0707.1609)); _Bicategory of entwinings_  ([arXiv:0805.4611](http://arxiv.org/abs/0805.4611))

[[Z. Škoda]], _Some equivariant constructions in noncommutative geometry_, Georgian Math. J. 16 (2009) 1; 183--202 ([arXiv:0811.4770](http://front.math.ucdavis.edu/0811.4770))

R. Wisbauer, _Algebras versus coalgebras_,  Appl. Categ. Structures __16__  (2008),  no. 1-2, 255--295.

[[!redirects distributive laws]]
