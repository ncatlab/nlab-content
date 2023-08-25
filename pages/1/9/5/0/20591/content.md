
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

* $trans \colon S \times I \to S$, a _transition function_;

* $out \colon S \times I \to O$, an _output function_

and often an [[element]]

* $q_0 \in S$, the _initial state_.

\end{definition}

\begin{remark}\label{MealyMachinesAsEffectfulMaps}
**(Mealy machines as effectful maps)**
\linebreak
More generally and concisely, a Mealy machine can be defined in any [[symmetric monoidal category]] $(\mathcal{C},\otimes,1)$ as an object of the following pullback in [[Cat]]: 
\begin{centre}
\begin{tikzcd}
Mly(I,O)\ar[r]\ar[d] & \mathcal{C}/O \ar[d, "V"]\\ 
Alg(-\otimes I) \ar[r, "U"']& \mathcal{C}
\end{tikzcd}
\end{centre}
where $Alg(-\otimes I)$ is the category of endofunctor algebras for $-\otimes I : \mathcal{C}\to\mathcal{C} : S\mapsto S\otimes I$, $U$ the forgetful functor, and $V$ the domain functor from the [[slice category]] $\mathcal{C}/O$.
\end{remark}

Then, a Mealy machine as in Def. \ref{DefinitionInComponents} consists (except for the specification of the initial state) of a span
\[ 
  E \leftarrow E\otimes I \to O
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

Discussion as [[state monad|stateful]]-maps:

* {#OliveiraMiraldo16} José Nuno Oliveira, Victor Cacciari Miraldo, *A practical approach to state-based system calculi*, Journal of Logical and Algebraic Methods in Programming **85** 4 (2016) 449-474 &lbrack;[doi:10.1016/j.jlamp.2015.11.007](https://doi.org/10.1016/j.jlamp.2015.11.007)&rbrack;

* {#PeroneKarachalias23} Marco Perone, Georgios Karachalias, *Composable Representable Executable Machines* &lbrack;[arXiv:2307.09090](https://arxiv.org/abs/2307.09090)&rbrack;


[[!redirects Mealy machines]]
