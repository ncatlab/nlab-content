
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _Mealy machine_ (named after [Mealy 1955](#Mealy55)) -- traditionally understood as a particular type of [[finite state automaton]] -- is a [[map]] (traditionally thought of as a [[pair]] of maps, see Def. \ref{DefinitionInComponents} below) which takes input data *and* a given "state" to output data *and* an update of that "state". In modern language of [[monadic computational effects]] this just means that a Mealy machine is a *[[state monad|stateful]]-map*, namely a [[Kleisli morphisms]] for a [[state monad]] (see Rem. \ref{MealyMachinesAsEffectfulMaps}  below).

## Definition

\begin{definition}
\label{DefinitionInComponents}
**(traditional component definition)**
\linebreak
A finite _Mealy machine_, $\mathbf{A}$, consists of [[finite sets]]

* $S$, of _states_;

* $I$, the _input alphabet_;

* $O$, the _output alphabet_;

and [[functions]]

* $trans \colon S \times I \to S$, a _transition function_ (the pair $(S,trans)$ is sometimes called a ($I$-)_semiautomaton_, cf. [Kilp et al](#KilpKnauerMikhal));

* $out \colon S \times I \to O$, an _output function_

and often an [[element]]

* $q_0 \in S$, the _initial state_.

\end{definition}

\begin{remark}\label{MealyMachinesAsEffectfulMaps}
**(Mealy machines as effectful maps)**
\linebreak
More generally and concisely, a Mealy machine with (finite or infinite) input alphabet $I$ and output alphabet $O$ can be defined in any [[symmetric monoidal category]] $(\mathcal{C},\otimes,1)$ as an object of the following pullback $Mly(I,O)$ in [[Cat]]: 
\begin{centre}
\begin{tikzcd}
Mly(I,O)\ar[r]\ar[d] & (-\otimes I)/O \ar[d, "V"]\\ 
Alg(-\otimes I) \ar[r, "U"']& \mathcal{C}
\end{tikzcd}
\end{centre}
Here, $Alg(-\otimes I)$ is the category of endofunctor algebras for $-\otimes I : \mathcal{C}\to\mathcal{C} : S\mapsto S\otimes I$, $U$ the forgetful functor, and similarly, $(-\otimes I)/O$ is the [[comma category]] of morphisms $out : X\otimes I\to O$, and $V$ the forgetful functor $(X,out)\mapsto X$.
\end{remark}
\begin{remark}
If $\mathcal{C}$ has countable [[coproduct|coproducts]], a semiautomaton $trans : S\otimes I \to S$ consists of an [[action#actions_of_a_monoid|action]] of the free monoid on $I$, $\sum_{n=0}^\infty I^{\otimes n}$; this is well-explained [[action#actions_of_a_set|_ibi_]]. 

Concisely, there is an equivalence of categories
\[
  Alg(-\otimes I) \simeq EM(I^*)
\]
between $I$-semiautomata and the [[Eilenberg-Moore category]] of the monad [[action monad|induced]] by the monoid $I^*$.
\end{remark}

Then, a Mealy machine as in Def. \ref{DefinitionInComponents} consists (except for the specification of the initial state) of a span
\[ 
  S \leftarrow S\otimes I \to O
\]
Unwinding this definition in the case of the category of [[Set|sets]], a Mealy machine consists of a [[map]] between [[Cartesian products]] of this form:
\[
  \label{MealyMachineAsMapBetweenProducts}
  (out, trans)
  \;\colon\; 
  I \times S \longrightarrow O \times S
\]

Mealy machines in a *[[cartesian closed monoidal category|closed]]* cartesian monoidal category (such as [[Sets]]) with [[internal hom]] $[\text{-},\text{-}]$, are a particularly well-behaved structure for a variety of reasons: for starters, a map like the one in (eq:MealyMachineAsMapBetweenProducts) is equivalent to (namely: is the "[[currying|curried]]" [[internal hom]]-[[adjunct]] of) a map of the form

$$
  S \longrightarrow \big[I,\, O \times S\big]
  \,.
$$

In this form Mealy machines are discussed as [[coalgebras of an endofunctor]], for instance in &lbrack;[Pattinson 2003, 1.1.3](#Pattinson03)&rbrack;, &lbrack;[Bonsangue, Rutten & Silva 2008, p. 1](BonsangueRuttenSilva08)&rbrack;, &lbrack;[Ghica, Kaye & Sprunger 2022, Def. 25](#GhicaKayeSprunger22)&rbrack;.

But of course, by the same token  (eq:MealyMachineAsMapBetweenProducts) is also [[adjunct]] to a map of the form

\[
  \label{MealyMachineAsStateEffectufulFunction}
  I \longrightarrow \big[S ,\, S \times O \big]
\]

which makes more manifest how a Mealy machine is a map sending input $i \in I$ to output $o \in O$ after also reading out a stated $s \in S$ and then also updating that state.

In fact, in this form (eq:MealyMachineAsStateEffectufulFunction) Mealy machines are exactly the *$S$-effectful maps* in these sense of [[monadic computational effects]], namely the [[Kleisli morphisms]] for the $S$-[[state monad]] (mentioned as such for instance in [Oliveira & Miraldo 2016, p. 462](#OliveiraMiraldo16)).

For discussion of this perspective in [[Haskell]]: &lbrack;[github.com/orakaro/MonadicMealyMachine](https://github.com/orakaro/MonadicMealyMachine)&rbrack;, &lbrack;[Perone & Karachalias 2023, p. 3](#PeroneKarachalias23)&rbrack;.

Second, Mealy machines in the category of sets organize in a bicategory, in the sense that the categories $Mly(I,O)$ in \ref{MealyMachinesAsEffectfulMaps} happen to be the hom-categories of a [[bicategory]]; specifically, it is possible to define [[bifunctor|bifunctors]]
\[
  \odot \colon  
  Mly(Y,Z)\times Mly(X,Y) \to Mly(X,Z)
\]
for a bicategory $\mathcal{M}ly$ whose objects are sets. 

This is the subject of &lbrack;[Katis, Sabadini, Walters 1997](#Katis1)&rbrack; and &lbrack;[Katis, Sabadini, Walters 2002](#Katis2)&rbrack;


## Related entries

* [[state monad]]

* [[Moore machine]]

* [[automata]]

* [[Mealy morphism]]

## References

The notion is due to:

* {#Mealy55} [[George H. Mealy]], *A Method for Synthesizing Sequential Circuits*, Bell System Technical Journal **34** 5 (1955) 1045-1079 &lbrack;[doi:10.1002/j.1538-7305.1955.tb03788.x](https://doi.org/10.1002/j.1538-7305.1955.tb03788.x)&rbrack;



* [[Mark V. Lawson]], *Finite automata*, CRC Press (2003) &lbrack;[webpage](http://www.ma.hw.ac.uk/~markl/books.html), course notes:[pdf](http://www.ma.hw.ac.uk/~markl/teaching/AUTOMATA/kleene.pdf)&rbrack;

Discussion via [[category theory]] and as [[coalgebras of an endofunctor]]

* {#Pattinson03} [[Dirk Pattinson]], Section 1.1.3 in: _An Introduction to the Theory of Coalgebras_ (2003) &lbrack;[pdf](https://nasslli.sitehost.iu.edu/2003/datas/DirkPattinson.pdf), [[Pattinson-Coalgebras.pdf:file]]&rbrack;

* {#BonsangueRuttenSilva08} M. M. Bonsangue, Jan Rutten & Alexandra Silva , *Coalgebraic Logic and Synthesis of Mealy Machines*,  in: *Foundations of Software Science and Computational Structures. FoSSaCS 2008*, Lecture Notes in Computer Science, **4962** (2008) &lbrack;[doi:10.1007/978-3-540-78499-9_17](https://doi.org/10.1007/978-3-540-78499-9_17)&rbrack;

* H. Hansen, Jan Rutten, *Symbolic synthesis of Mealy machines from arithmetic bitstream functions*, Scientific Annals of Computer Science **20** (2010) 97–130 &lbrack;[pub:16639](https://ir.cwi.nl/pub/16639), [pdf](https://core.ac.uk/download/pdf/301659512.pdf)&rbrack;

* {#GhicaKayeSprunger22} [[Dan R. Ghica]], George Kaye, David Sprunger, Def. 25 in: *A compositional theory of digital circuits* &lbrack;[arXiv:2201.10456](https://arxiv.org/abs/2201.10456)&rbrack;

* {#KilpKnauerMikhal} Kilp, Mati, Knauer, Ulrich and Mikhalev, Alexander V. *Monoids, Acts and Categories: With Applications to Wreath Products and Graphs. A Handbook for Students and Researchers*, Berlin, New York: De Gruyter, 2000. &lbrack;[https://doi.org/10.1515/9783110812909](https://doi.org/10.1515/9783110812909)&rbrack;

The bicategory of Mealy machines is discussed in:

* {#Katis1} P. Katis a, N. Sabadini b, R.F.C. Walters, _Bicategories of processes_, Journal of Pure and Applied Algebra, Volume 115, Issue 2, 28 February 1997, Pages 141-178. [doi:10.1016/S0022-4049(96)00012-6](https://doi.org/10.1016/S0022-4049(96)00012-6)

* {#Katis2} Katis, P.; Sabadini, Nicoletta; Walters, Robert F. C. _Feedback, trace and fixed-point semantics
_. RAIRO - Theoretical Informatics and Applications - Informatique Théorique et Applications, Volume 36 (2002) no. 2, pp. 181-194. [doi:10.1051/ita:2002009](https://doi.org/10.1051/ita:2002009)

Discussion as [[state monad|stateful]]-maps:

* {#OliveiraMiraldo16} José Nuno Oliveira, Victor Cacciari Miraldo, *A practical approach to state-based system calculi*, Journal of Logical and Algebraic Methods in Programming **85** 4 (2016) 449-474 &lbrack;[doi:10.1016/j.jlamp.2015.11.007](https://doi.org/10.1016/j.jlamp.2015.11.007)&rbrack;

* {#PeroneKarachalias23} Marco Perone, Georgios Karachalias, *Composable Representable Executable Machines* &lbrack;[arXiv:2307.09090](https://arxiv.org/abs/2307.09090)&rbrack;


[[!redirects Mealy machines]]
