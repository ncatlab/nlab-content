
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

# Distributive laws

* table of contents
{:toc}

## Idea

Sometimes in [[mathematics]] we want to consider objects equipped with two different types of [[extra structure]] which interact in a suitable way.  For instance, a [[ring]] is a [[set]] equipped with both (1) the structure of an (additive) [[abelian group]] and (2) the structure of a (multiplicative) [[monoid]], which satisfy the distributive laws $a\cdot (b+c) = a\cdot b + a\cdot c$ and $a\cdot 0 = 0$.

Abstractly, there are two [[monads]] on the [[category]] [[Set]], one (call it $\mathbf{T}$) whose [[algebra over a monad|algebras]] are abelian groups, and one (call it $\mathbf{S}$) whose algebras are monoids, and so we might ask "can we construct, from these two monads, a third monad whose algebras are rings?"  Such a monad would assign to each set $X$ the [[free object|free]] ring on that set, which consists of formal sums of formal products of elements of $X$---in other words, it can be identified with $T(S(X))$.  Thus the question becomes "given two monads $\mathbf{T}$ and $\mathbf{S}$, what further structure is required to make the composite $T S$ into a monad?"

It is easy to give $T S$ a unit, as the composite $Id \xrightarrow{\eta^S} S \xrightarrow{\eta^T S} T S$, but to give it a multiplication we need a transformation from $T S T S$ to $T S$.  We naturally want to use the multiplications $\mu^T\colon T T \to T$ and $\mu^S\colon S S \to S$, but in order to do this we first need to switch the order of $T$ and $S$.  However, if we have a transformation $\lambda\colon S T \to T S$, then we can define $\mu^{T S}$ to be the composite $T S T S \xrightarrow{\lambda} T T S S \xrightarrow{\mu^T\mu^S} T S$.

Such a transformation, satisfying suitable axioms to make $T S$ into a monad, is called a *distributive law*, because of the motivating example relating addition to multiplication in a ring.  In that case, $S T X$ is a formal product of formal sums such as $(x_1 + x_2 + x_3)\cdot (x_4 + x_5)$, and the distributive law $\lambda$ is given by multiplying out such an expression formally, resulting in a formal sum of formal products such as $x_1\cdot x_4 + x_1 \cdot x_5 + x_2 \cdot x_4 + x_2 \cdot x_5 + x_3\cdot x_4 + x_3 \cdot x_5$.


## Big picture

[[monad|Monads]] in any [[2-category]] $C$ make themselves a 2-category $\mathrm{Mnd}$ in which [[1-morphisms]] are either lax or colax [[homomorphisms]] of monads.
By [[formal duality]] the analogue is true for [[comonads]]. 

Monads [[internalization|internal]] to the 2-category of monads are called _distributive laws_. In particular, distributive laws themselves make a 2-category. There are other variants like distributive laws between a monad and an [[endofunctor]], "mixed" distributive laws between a monad and a comonad (the variants for algebras and coalgebras called [[entwining structure]]s), distributive laws between actions of two different monoidal categories on the same category, for [[PROP]]s and so on. Having a distributive law $l$ from one monad to another enables to define the composite monad $\mathbf T\circ_l\mathbf P$. This correspondence extends to a 2-functor $\mathrm{comp}:\mathrm{Mnd}(\mathrm{Mnd}(C))\to\mathrm{Mnd}(C)$. An analogue of this 2-functor in the mixed setup is a homomorphism of bicategories from the bicategory of entwinings to a bicategory of [[corings]].



## Explicit definition

### Monad distributing over monad

A __distributive law__ from a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ in $A$ to an endofunctor
$P$ is a 2-cell $l : T P \Rightarrow P T$ such that
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

Distributive laws from the monad $\mathbf{T}$ to the endofunctor $P$ are in a canonical bijection with lifts of $P$ to an endofunctor $P^{\mathbf T}$ in the [[Eilenberg-Moore category]] $A^{\mathbf T}$,
satisfying $U^{\mathbf T} P^{\mathbf T} = P U^{\mathbf T}$. Indeed, the endofunctor $P^{\mathbf T}$
is given by $(M,\nu) \mapsto (P M,P(\nu)\circ l_M)$.

A __distributive law__ from a monad  $\mathbf{T} = (T, \mu^T, \eta^T)$ to a monad
$\mathbf{P} = (P, \mu^P, \eta^P)$ in $A$ 
(or _of_ $\mathbf T$ _over_ $\mathbf P$)
is a distributive law from $\mathbf T$ to the endofunctor $P$,
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

The correspondence between distributive laws and _endofunctor_ liftings extends to a correspondence between distributive laws and _monad_ liftings. That is, distributive laws $l : T P \Rightarrow P T$ from the monad $\mathbf{T}$ to the monad $\mathbf{P}$ are in a canonical bijection with lifts of the monad $\mathbf{P}$ to a monad $\mathbf{P}^{\mathbf T}$ in the [[Eilenberg-Moore category]] $A^{\mathbf T}$,
such that $U^{\mathbf T} : A^{\mathbf T}\to A$ preserves the monad structure.

Thus all together a distributive law from a monad to a monad is a 2-cell for which 2 triangles and 2 pentagons commute. In the entwining case, 
Brzezi&#324;ski and Majid combined the 4 diagrams into one picture which they call the _bow-tie diagram_. 

Similarly, there are definitions of distributive laws of a comonad over a comonad, 

### Monad distributing over comonad
 {#MonadDistributingOverComonad}

The distributivity law of 

* a monad $\mathcal{E}$ over 

* a comonad $\mathcal{C}$ 

on the same [[category]] $\mathbf{C}$

is as follows ([Brookes & Van Stone 1993 Def. 3](#BrookesVanStone93)):

A [[natural transformation]]

$$
  distr^{\mathcal{C}, \mathcal{E}}
  \;\;\colon\;\;
  \mathcal{C}
  \big(
    \mathcal{E}(D)
  \big)
  \longrightarrow
  \mathcal{E}
  \big(
    \mathcal{C}(D)
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

{#TwoSidedKleisliComposition} Given this distributivity structure, there is a two-sided ("double") [[Kleisli category]] ([Brookes & Van Stone 1993 Thm. 2](#BrookesVanStone93)) whose [[objects]] are those of $\mathbf{C}$, and whose morphisms $D_1 \to D_2$ are morphisms in $\mathbf{C}$ of the form
$$
  prog_{12}
  \;\colon\;
  \mathcal{C}(D_1) 
    \longrightarrow 
  \mathcal{E}(D_2)
$$
with two-sided Kelisli composition

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

* [[H. Applegate]], [[M. Barr]], [[J. Beck]], [[F. W. Lawvere]], [[F. E. J. Linton]], [[E. Manes]], [[M. Tierney]], [[F. Ulmer]]: *[[Seminar on Triples and Categorical Homology Theory]]*, ETH 1966/67, edited by [[Beno Eckmann]] and [[Myles Tierney]], **[[LNM 80]]**, Springer (1969), reprinted as: Reprints in Theory and Applications of Categories **18** (2008) 1-303 &lbrack;[TAC:18](http://www.tac.mta.ca/tac/reprints/articles/18/tr18abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/18/tr18.pdf)&rbrack;

* {#Street72} [[Ross Street]], §6 of: *The formal theory of monads*, Journal of Pure and Applied Algebra **2** 2 (1972) 149-168 &lbrack;<a href="https://doi.org/10.1016/0022-4049(72)90019-9">doi:10.1016/0022-4049(72)90019-9</a>&rbrack;

* [[Michael Barr]], [[Charles Wells]], *[[Toposes, Triples, and Theories]]*, Springer (1985) republished in: [[TAC reprints series|Reprints in Theory and Applications of Categories]], **12** (2005) 1-287 &lbrack;[tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html), [tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack;
 

* {#BrookesVanStone93} [[Stephen Brookes]],  [[Kathryn Van Stone]], *Monads and Comonads in Intensional Semantics* (1993) &lbrack;[dtic:ADA266522](https://apps.dtic.mil/sti/citations/ADA266522), [pdf](https://www.cs.cmu.edu/~brookes/papers/MonadsComonads.pdf), [[BrookesVanStone-CoMonads.pdf:file]]&rbrack;


* [[John Power]], [[Hiroshi Watanabe]], *Distributivity for a monad and a comonad*, Electronic Notes in Theoretical Computer Science **19** (1999) 102 &lbrack;<a href="https://doi.org/10.1016/S1571-0661(05)80271-3">doi:10.1016/S1571-0661(05)80271-3</a>&rbrack;

* [[John Power]], [[Hiroshi Watanabe]], *Combining a monad and a comonad*, Theoretical Computer Science **280** 1–2 (2002) 137-162 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(01)00024-X">doi:10.1016/S0304-3975(01)00024-X</a>&rbrack;

* [[Gabi Böhm]], _Internal bialgebroids, entwining structures and corings_, AMS Contemp. Math. **376** (2005) 207-226 &lbrack;[arXiv:math.QA/0311244](http://front.math.ucdavis.edu/math.QA/0311244)&rbrack;

* [[T. Brzeziński]], [[S. Majid]], _Coalgebra bundles_, Comm. Math. Phys.  191  (1998),  no. 2, 467--492 ([arXiv version](http://arxiv.org/abs/q-alg/9602022)).

* [[T. Brzeziński]], [[Robert Wisbauer]], _Corings and comodules_, London Math. Soc. Lec. Note Series 309, Cambridge (2003)

* Bachuki Mesablishvili, [[Robert Wisbauer]], *Bimonads and Hopf monads on categories*, Journal of K-Theory **7** 2 (2011) 349-388  &lbrack;[arXiv:0710.1163](https://arxiv.org/abs/0710.1163), [doi:10.1017/is010001014jkt105](https://doi.org/10.1017/is010001014jkt105)&rbrack;


* T. F. Fox, [[Martin Markl]], _Distributive laws, bialgebras, and cohomology_,  Operads: Proceedings of Renaissance Conferences (Hartford, CT/Luminy, 1995),   Contemp. Math. **202** AMS (1997) 167-205

* [[Steve Lack]], _Composing PROPS_, [Theory Appl. Categ.](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html) 13 (2004), No. 9, 147--163.

* [[Steve Lack]], [[Ross Street]], _The formal theory of monads II_, Special volume celebrating the 70th birthday of Professor Max Kelly, J. Pure Appl. Algebra **175** 1-3 (2002) 243-265 

* [[Martin Markl]], _Distributive laws and Koszulness_,  Ann. Inst. Fourier (Grenoble)  46  (1996),  no. 2, 307--323 ([numdam](http://www.numdam.org/numdam-bin/fitem?id=AIF_1996__46_2_307_0))


* [[Zoran Škoda]], _Distributive laws for monoidal categories_ ([arXiv:0406310](http://front.math.ucdavis.edu/math.CT/0406310)); _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_ ([arXiv:0707.1609](http://front.math.ucdavis.edu/0707.1609)); _Bicategory of entwinings_  ([arXiv:0805.4611](http://arxiv.org/abs/0805.4611))

* [[Zoran Škoda]], _Some equivariant constructions in noncommutative geometry_, Georgian Math. J. 16 (2009) 1; 183--202 ([arXiv:0811.4770](http://front.math.ucdavis.edu/0811.4770))

* R. Wisbauer, _Algebras versus coalgebras_,  Appl. Categ. Structures __16__  (2008),  no. 1-2, 255--295.

* [[Francisco Marmolejo]], Adrian Vazquez-Marquez, *No-iteration mixed distributive laws*, Mathematical Structures in Computer Science **27** 1 (2017) 1-16 &lbrack;[doi:10.1017/S0960129514000656](https://doi.org/10.1017/S0960129514000656)&rbrack;

* Enrique Ruiz Hernández, *Another characterization of no-iteration distributive laws*, [arxiv](https://arxiv.org/abs/1910.06531)

On distributive laws for [[relative monads]]:

* [[Gabriele Lobbia]], *Distributive Laws for Relative Monads*, Applied Categorical Structures **31** 19 (2023)  &lbrack;[doi:10.1007/s10485-023-09716-1](https://doi.org/10.1007/s10485-023-09716-1), [arXiv:2007.12982](https://arxiv.org/abs/2007.12982)&rbrack;


[[!redirects distributive laws]]
[[!redirects mixed distributive law]]
[[!redirects mixed distributive laws]]

[[!redirects distributivity law]]

[[!redirects distributivity]]
