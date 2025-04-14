
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

Sometimes in [[mathematics]] one considers objects equipped with two different types of [[extra structure]] which interact in a suitable way.  For instance, a [[ring]] is a [[set]] equipped with both (1) the structure of an (additive) [[abelian group]] and (2) the structure of a (multiplicative) [[monoid]], which satisfy the distributive laws $a\cdot (b+c) = a\cdot b + a\cdot c$ and $a\cdot 0 = 0$.

Abstractly, there are two [[monads]] on the [[category]] [[Set]], one (call it $T$) whose [[algebra over a monad|algebras]] are abelian groups, and one (call it $S$) whose algebras are monoids, and so we might ask "can we construct, from these two monads, a third monad whose algebras are rings?"  Such a monad would assign to each set $X$ the [[free object|free]] ring on that set, which consists of formal sums of formal products of elements of $X$---in other words, it can be identified with $T(S(X))$.  Thus the question becomes "given two monads $T$ and $S$, what further structure is required to make the composite $T S$ into a monad?"

It is easy to give $T S$ a unit, as the composite $Id \xrightarrow{\eta^S} S \xrightarrow{\eta^T S} T S$, but to give it a multiplication we need a transformation from $T S T S$ to $T S$.  We naturally want to use the multiplications $\mu^T\colon T T \to T$ and $\mu^S\colon S S \to S$, but in order to do this we first need to switch the order of $T$ and $S$.  However, if we have a transformation $\lambda\colon S T \to T S$, then we can define $\mu^{T S}$ to be the composite $T S T S \xrightarrow{\lambda} T T S S \xrightarrow{\mu^T\mu^S} T S$.

Such a transformation $\lambda\colon S T \to T S$, satisfying suitable axioms to make $T S$ into a monad, is called a *distributive law*, because of the motivating example relating addition to multiplication in a ring.  In that case, $S T X$ is a formal product of formal sums such as $(x_1 + x_2 + x_3)\cdot (x_4 + x_5)$, and the distributive law $\lambda$ is given by multiplying out such an expression formally, resulting in a formal sum of formal products such as $x_1\cdot x_4 + x_1 \cdot x_5 + x_2 \cdot x_4 + x_2 \cdot x_5 + x_3\cdot x_4 + x_3 \cdot x_5$.

Given two monads $S, T$ on a category $C$, a distributive law $S \circ T \longrightarrow T \circ S $ gives a way of lifting the monad $T$ on $C$ to a monad on the category of $S$-algebras, namely the [[Eilenberg-Moore category]] $C^S$.  In the example above, the distributive law gives a way to lift the monad $T$ for abelian groups (which is a monad on $C = Set$) to the monad for rings over $C^S = Mon$.  This is a way of making rigorous the intuition that "rings are to monoids as abelian groups are to sets".

\begin{remark}
\label{TerminologyWhatDistributesOverWhat}
**(terminology -- what distributes over what)**
\linebreak
The eponymous example of distributivity in [[arithmetic]]
$$
  a \times \sum_i b_i \;=\; \sum_i a \times b_i
$$
hence
$$
  \big( a \times (-) \big) 
  \circ 
  \big(
    \sum (-)
  \big)
  \;\;
  =
  \;\;
  \big(
    \sum (-)
  \big)
  \circ 
  \big( a \times (-) \big) 
$$
(where, of course, the [[equality]] as such works in both directions, but the *distribution* of factors over summands is the step from left to right)
suggests that a suitable transformation of (co)monads of the form
$$
  S \circ T \longrightarrow T \circ S
$$
should be referred to as *$S$ distributing over $T$* instead of the other way around. 

However, already the original reference [Beck 1969 §1](#Beck69) uses the opposite terminology.

Authors sticking to this original but arguably reverse terminological convention include [Brookes & Van Stone 1993](#BrookesVanStone93), while other authors tacitly switch to the other terminological convention (eg. [Barr & Wells 1985 §9 2.1](#BarrWells85), [Power & Watanabe 2002 p. 138](#PowerWatanabe02)).
\end{remark}


## Big picture
 {#BigPicture}

[[monad|Monads]] in any [[2-category]] $C$ make themselves a 2-category $\mathrm{Mnd}$ in which [[1-morphisms]] are either lax or colax [[homomorphisms]] of monads (cf. *[[monad transformations]]*). By [[formal duality]] the analogue is true for [[comonads]]. 

Distributivity laws may be understood as 
monads [[internalization|internal]] to this 2-category of monads.

In particular, distributive laws themselves make a 2-category. 

There are other variants like distributive laws between a monad and an [[endofunctor]], **mixed distributive laws** between a monad and a comonad (the variants for algebras and coalgebras called [[entwining structures]]), distributive laws between actions of two different monoidal categories on the same category, for [[PROP]]s and so on. 

Having a distributive law $l$ from one monad to another enables to define the composite monad $\mathbf T\circ_l\mathbf P$. This correspondence extends to a 2-functor $\mathrm{comp} \,\colon\, \mathrm{Mnd}(\mathrm{Mnd}(C))\to\mathrm{Mnd}(C)$. An analogue of this 2-functor in the mixed setup is a [[2-functor]] from the bicategory of entwinings to a bicategory of [[corings]].


## Explicit definition

### Monad distributing over monad

\begin{definition}
A __distributive law__ for a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ in $A$ over an endofunctor
$P$ is a [[2-morphism]] $l : T P \Rightarrow P T$ such that
$l \circ (\eta^T)_P = P(\eta^T)$ and
$l \circ (\mu^T)_P = P(\mu^T) \circ l_T \circ T(l)$. In diagrams:

\begin{tikzcd}
& P \ar{dl}[swap]{\eta^T P} \ar{dr}{P \eta^T} \\
T P \ar{rr}{l} && P T
\end{tikzcd}
\begin{tikzcd}
T T P \ar{d}{\mu^T P} \ar{r}{T l} & T P T \ar{r}{l T} & P T T \ar{d}{P \mu^T} \\
T P \ar{rr}{l} && P T
\end{tikzcd}

\end{definition}

Distributive laws for the monad $\mathbf{T}$ over the endofunctor $P$ are in a canonical bijection with lifts of $P$ to an [[endofunctor]] $P^{\mathbf T}$ in the [[Eilenberg-Moore category]] $A^{\mathbf T}$,
satisfying $U^{\mathbf T} P^{\mathbf T} = P U^{\mathbf T}$. Indeed, the endofunctor $P^{\mathbf T}$
is given by $(M,\nu) \mapsto (P M,P(\nu)\circ l_M)$.

\begin{definition}
A __distributive law__ for a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ over a monad
$\mathbf{P} = (P, \mu^P, \eta^P)$ in $A$ 
is a distributive law for $\mathbf T$ over the endofunctor $P$,
compatible with $\mu^P,\eta^P$ in the sense that
$l \circ T(\eta^P) = (\eta^P)_T$ and
$l \circ T(\mu^P) = (\mu^P)_T \circ P(l) \circ l_P$. In diagrams:

\begin{tikzcd}
& T \ar{dl}[swap]{T \eta^P} \ar{dr}{\eta^P T} \\
T P \ar{rr}{l} && P T
\end{tikzcd}

\begin{tikzcd}
T P P \ar{d}{T \mu^P} \ar{r}{l P} & P T P \ar{r}{P l} & P P T \ar{d}{\mu^P T} \\
T P \ar{rr}{l} && P T
\end{tikzcd}

\end{definition}
(due to [Beck 1969](#Beck69), review includes [Barr & Wells 1985 §9 2.1](#BarrWells85))

The correspondence between distributive laws and _endofunctor_ liftings extends to a correspondence between distributive laws and _monad_ liftings. That is, distributive laws $l \colon T P \Rightarrow P T$ from the monad $\mathbf{T}$ to the monad $\mathbf{P}$ are in a canonical bijection with lifts of the monad $\mathbf{P}$ to a monad $\mathbf{P}^{\mathbf T}$ in the [[Eilenberg-Moore category]] $A^{\mathbf T}$,
such that $U^{\mathbf T} \colon A^{\mathbf T}\to A$ preserves the monad structure.

Thus all together a distributive law for a monad over a monad is a 2-cell for which 2 triangles and 2 pentagons commute. In the entwining case, 
Brzezi&#324;ski and Majid combined the 4 diagrams into one picture which they call the _bow-tie diagram_. 


\begin{remark}\label{DistributivityAsMonadsInMonads}
**(distributivity as monads in monads)**
\linebreak
As mentioned earlier, one can understand a distributivity law of a monad $(a,s)$ over another monad $(a,t)$ as displaying $s \colon a \to a$ as a monad on $(a,t)$ [[internalization|in]] the [[2-category]] $\mathbf{Mnd}(A)$ of monads in a 2-category $A$.

Specifically, a monad in $\mathbf{Mnd}(A)$ over $(a,t)$ (which is a monad in $A$!) is comprised of the following data:

1. A [[1-morphism]] $s \colon a \to a$ in $A$, together with an intertwiner $\lambda \colon t s \to s t$ satisfying the equations [[monad#BicategoryOfMonads|here]]

2. Two [[2-morphisms]] (in $\mathbf{Mnd}(A)$) $\sigma \colon 1 \Rightarrow (s,\lambda)$ and $\nu \colon (s,\lambda)(s,\lambda) \Rightarrow (s,\lambda)$ which correspond to two 2-morpisms in $A$ $\sigma \colon 1 \Rightarrow s$, $\nu \colon s s \Rightarrow s$ commuting with the intertwiners of $1$, $s$ and $ss$.

Then $\lambda$ is the distributive law sought, and the laws $\lambda$, $\sigma$ and $\nu$ satisfy correspond to those of a distributive law.
\end{remark}


### Monad distributing over a comonad 

[van Osdol 1973 p. 456](#vanOsdol73) 

(...)


### Comonad distributing over monad
 {#ComonadDistributingOverMonad}

The distributivity law of 

* a comonad $\mathcal{C}$ over 

* a monad $\mathcal{E}$  

on the same [[category]] $\mathbf{C}$

is as follows ([Brookes & Van Stone 1993 Def. 3](#BrookesVanStone93), [Power & Watanabe 2002](#PowerWatanabe02)):

A [[natural transformation]]

$$
  distr^{\mathcal{C}, \mathcal{E}}_{(\text{-})}
  \;\;\colon\;\;
  \mathcal{C}
  \big(
    \mathcal{E}(-)
  \big)
  \longrightarrow
  \mathcal{E}
  \big(
    \mathcal{C}(-)
  \big)
$$

such that the following [[commuting diagram|diagrams commute]] for all objects $D$:


\begin{imagefromfile}
    "file_name": "MixedCoMonadDistributivity-230929.jpg",
    "width": 540,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

{#TwoSidedKleisliComposition} Given this distributivity structure, there is a two-sided ("double") [[Kleisli category]] ([Brookes & Van Stone 1993 Thm. 2](#BrookesVanStone93), [Power & Watanabe 2002, Prop. 7.4](#PowerWatanabe02)) whose [[objects]] are those of $\mathbf{C}$, and whose morphisms $D_1 \to D_2$ are morphisms in $\mathbf{C}$ of the form
$$
  prog_{12}
  \;\colon\;
  \mathcal{C}(D_1) 
    \longrightarrow 
  \mathcal{E}(D_2)
$$
with two-sided Kleisli composition

$$
  prog_{12} \text{>=>} prog_{23}
  \;\;
  \colon
  \;\;
  \mathcal{C}(D_1)
  \longrightarrow
  \mathcal{E}(D_3)
$$

given by the (co-)[[Kleisli extension|bind-operation]] on the factors connected by the distributivity transformation:

\begin{imagefromfile}
    "file_name": "CoMonKleisliComposition-230930b.pdf",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

## Algebras for a distributive law

Given a composite monad $T S$ arising from a distributive law $l : S T \Rightarrow T S$, an algebra for $T S$ comprises an object $A$ with both $S$- and $T$-algebra structures $s : SA \to A$ and $t : TA \to A$ satisfying the following compatibility law.
\begin{tikzcd}
	STA && TSA \\
	SA && TA \\
	& A
	\arrow["{l_A}", from=1-1, to=1-3]
	\arrow["St"', from=1-1, to=2-1]
	\arrow["Ts", from=1-3, to=2-3]
	\arrow["s"', from=2-1, to=3-2]
	\arrow["t", from=2-3, to=3-2]
\end{tikzcd}
The category of $T S$-algebras therefore forms a full subcategory of the category of $(S + T)$-algebras.

##Examples##

### Products distributing over coproducts

In a _[[distributive category]]_ [[products]] distribute over [[coproducts]].

### In Cat

* There is a distributive law of the monad (on [[Set]]) for [[monoids]] over the monad for [[abelian groups]], whose composite is the monad for [[rings]].  This is the canonical example which gives the name to the whole concept.


#### Tensor products distributing over direct sums

For many standard choices of [[tensor products]] in the presence of [[direct sums]] the former distribute over the latter. See at _[[tensor product of abelian groups]]_ and _[[tensor product of modules]]_. 


### In other 2-categories

* [[strict factorization systems]] can be identified with distributive laws between categories regarded as monads in [[span|Span(Set)]].

* More generally, [[factorization systems over a subcategory]] can be identified with distributive laws in [[Prof]].  Ordinary [[orthogonal factorization systems]] are a special case.  The latter can also be obtained by other weakenings; see for instance [this discussion](http://golem.ph.utexas.edu/category/2010/07/ternary_factorization_systems.html).

## Related concepts

* [[weak distributive law]]

* [[iterated distributive law]]

* [[wreath]]

* [[distributivity for monoidal structures]]

* [[monad transformer]]

* [[pseudo-distributive law]]


## Literature
 {#Literature}

* {#Beck69} [[Jon Beck]], *Distributive Laws*, in: *[[Seminar on Triples and Categorical Homology Theory]]*, ETH 1966/67, Lecture Notes in Mathemativs, Springer (1969), Reprints in Theory and Applications of Categories **18** (2008) 1-303 &lbrack;[TAC:18](http://www.tac.mta.ca/tac/reprints/articles/18/tr18abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/18/tr18.pdf#page=95)&rbrack;

* {#vanOsdol73} [[Donovan van Osdol]], *Bicohomology Theory*, Transactions of the American Mathematical Society **183** (1973) 449-476 &lbrack;[jstor:1996479](https://www.jstor.org/stable/1996479)&rbrack;

* {#Street72} [[Ross Street]], §6 of: *The formal theory of monads*, Journal of Pure and Applied Algebra **2** 2 (1972) 149-168 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90019-9">doi:10.1016/0022-4049(72)90019-9</a>&rbrack;

* {#BarrWells85} [[Michael Barr]], [[Charles Wells]], *[[Toposes, Triples, and Theories]]*, Springer (1985) republished in: [[TAC reprints series|Reprints in Theory and Applications of Categories]], **12** (2005) 1-287 &lbrack;[tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html), [tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack;
 
* {#BrookesVanStone93} [[Stephen Brookes]],  [[Kathryn Van Stone]], *Monads and Comonads in Intensional Semantics* (1993) &lbrack;[dtic:ADA266522](https://apps.dtic.mil/sti/citations/ADA266522), [pdf](https://www.cs.cmu.edu/~brookes/papers/MonadsComonads.pdf), [[BrookesVanStone-CoMonads.pdf:file]]&rbrack;


* [[Martin Markl]], _Distributive laws and Koszulness_,  Ann. Inst. Fourier (Grenoble)  46  (1996),  no. 2, 307--323 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=AIF_1996__46_2_307_0))

* T. F. Fox, [[Martin Markl]], _Distributive laws, bialgebras, and cohomology_,  Operads: Proceedings of Renaissance Conferences (Hartford, CT/Luminy, 1995),   Contemp. Math. **202** AMS (1997) 167-205

* [[T. Brzeziński]], [[S. Majid]], _Coalgebra bundles_, Comm. Math. Phys.  **191** 2  (1998) 467--492 &lbrack;[arXiv:q-alg/9602022](http://arxiv.org/abs/q-alg/9602022)&rbrack;

For a study of distributive laws between monads and (pointed) endofunctors, see:

* Marina Lenisa, John Power, and Hiroshi Watanabe, _Distributivity for endofunctors, pointed and co-pointed endofunctors, monads and comonads_, Electronic Notes in Theoretical Computer Science 33 (2000): 230-260.

For a thorough study of mixed distributive laws, see:

* {#PowerWatanabe99} [[John Power]], [[Hiroshi Watanabe]], *Distributivity for a monad and a comonad*, Electronic Notes in Theoretical Computer Science **19** (1999) 102 &lbrack;<a href="https://doi.org/10.1016/S1571-0661(05)80271-3">doi:10.1016/S1571-0661(05)80271-3</a>, [[PowerWatanabe-Distributivity.pdf:file]]&rbrack;


* [[Steve Lack]], _Composing PROPS_, [Theory Appl. Categ.](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html) 13 (2004), No. 9, 147--163.

* [[Steve Lack]], [[Ross Street]], _The formal theory of monads II_, Special volume celebrating the 70th birthday of Professor Max Kelly, J. Pure Appl. Algebra **175** 1-3 (2002) 243-265 


* {#PowerWatanabe02} [[John Power]], [[Hiroshi Watanabe]], *Combining a monad and a comonad*, Theoretical Computer Science **280** 1–2 (2002) 137-162 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(01)00024-X">doi:10.1016/S0304-3975(01)00024-X</a>&rbrack;

* [[T. Brzeziński]], [[Robert Wisbauer]], _Corings and comodules_, London Math. Soc. Lec. Note Series 309, Cambridge (2003)


* [[Gabi Böhm]], _Internal bialgebroids, entwining structures and corings_, AMS Contemp. Math. **376** (2005) 207-226 &lbrack;[arXiv:math.QA/0311244](http://front.math.ucdavis.edu/math.QA/0311244)&rbrack;

* [[Ernie Manes]], [[Philip Mulry]]: *Monad compositions I: general constructions and recursive distributive laws*, Theory and Applications of Categories **18** 7 (2007) 172-208 &lbrack;[tac:18-07](http://www.tac.mta.ca/tac/volumes/18/7/18-07abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/18/7/18-07.pdf)&rbrack;

* [[Zoran Škoda]], _Distributive laws for monoidal categories_ ([arXiv:0406310](http://front.math.ucdavis.edu/math.CT/0406310)); _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_ ([arXiv:0707.1609](http://front.math.ucdavis.edu/0707.1609)); _Bicategory of entwinings_  ([arXiv:0805.4611](http://arxiv.org/abs/0805.4611))

* R. Wisbauer, _Algebras versus coalgebras_,  Appl. Categ. Structures __16__  1-2 (2008) 255--295 &lbrack;[doi:10.1007/s10485-007-9076-5](https://doi.org/10.1007/s10485-007-9076-5)&rbrack;

* [[Zoran Škoda]], _Some equivariant constructions in noncommutative geometry_, Georgian Math. J. 16 (2009) 1; 183--202 ([arXiv:0811.4770](http://front.math.ucdavis.edu/0811.4770))

* Bachuki Mesablishvili, [[Robert Wisbauer]], *Bimonads and Hopf monads on categories*, Journal of K-Theory **7** 2 (2011) 349-388  &lbrack;[arXiv:0710.1163](https://arxiv.org/abs/0710.1163), [doi:10.1017/is010001014jkt105](https://doi.org/10.1017/is010001014jkt105)&rbrack;

* [[Francisco Marmolejo]], Adrian Vazquez-Marquez, *No-iteration mixed distributive laws*, Mathematical Structures in Computer Science **27** 1 (2017) 1-16 &lbrack;[doi:10.1017/S0960129514000656](https://doi.org/10.1017/S0960129514000656)&rbrack;

* Liang Ze Wong, _Distributive laws_, post at $n$-[cafe](https://golem.ph.utexas.edu/category/2017/02/distributive_laws.html), Feb 2017

* Enrique Ruiz Hernández, *Another characterization of no-iteration distributive laws*, [arxiv](https://arxiv.org/abs/1910.06531)

* Werner Struckmann and Dietmar Wätjen, _A note on the number of distributive laws_, Algebra universalis 21 (1985): 305-306.

On distributive laws for [[relative monads]]:

* [[Gabriele Lobbia]], *Distributive Laws for Relative Monads*, Applied Categorical Structures **31** 19 (2023)  &lbrack;[doi:10.1007/s10485-023-09716-1](https://doi.org/10.1007/s10485-023-09716-1), [arXiv:2007.12982](https://arxiv.org/abs/2007.12982)&rbrack;

Invertible distributive laws are considered in Lemma 4.12 of:

* [[Bob Rosebrugh]], [[Richard J. Wood]], *Distributive Adjoint Strings*, Theory and Applications of Categories, **1** 6 (1995) 119-145 &lbrack;[tac:1-06](http://www.tac.mta.ca/tac/volumes/1995/n6/1-06abs.html)&rbrack;

* Stefano Kasangian, [[Stephen Lack]], and [[Enrico Vitale]]. _Coalgebras, braidings, and distributive laws_, Theory and Applications of Categories 13.8 (2004): 129-146. ([html](https://www.emis.de/journals/TAC/volumes/13/8/13-08abs.html))

* Alain Bruguieres and Alexis Virelizier, _Quantum double of Hopf monads and categorical centers_, Transactions of the American Mathematical Society 364.3 (2012): 1225-1279.

[[!redirects distributive laws]]
[[!redirects mixed distributive law]]
[[!redirects mixed distributive laws]]

[[!redirects distributivity law]]

[[!redirects distributivity]]
