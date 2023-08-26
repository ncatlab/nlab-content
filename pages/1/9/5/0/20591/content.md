
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

### Original definition

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
More concisely a Mealy machine as in Def. \ref{DefinitionInComponents} is (except for the specification of the initial state) just a [[map]] between [[Cartesian products]] of this form:

\[
  \label{MealyMachineAsMapBetweenProducts}
  (out, trans)
  \;\colon\; 
  I \times S \longrightarrow O \times S
\]

As such this makes sense [[internalization|in]] any [[cartesian monoidal category]] other than [[Sets]]. 

In a *[[cartesian closed monoidal category|closed]]* cartesian monoidal category (such as [[Sets]]) with [[internal hom]] $[\text{-},\text{-}]$, such a map (eq:MealyMachineAsMapBetweenProducts) is equivalent to (namely: is the "[[currying|curried]]" [[internal hom]]-[[adjunct]] of) a map of the form

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
\end{remark}


### As spans in monoidal categories
 {#AsSpans}

Instead of regarding the pair given by the transition- and output function of a Mealy machine (Def. \ref{DefinitionInComponents}) as a single map from $I \times S$ into the [[Cartesian product]] $O \times S$ (eq:MealyMachineAsMapBetweenProducts), one may, of course, regard them as a [[span]]:

\begin{tikzcd}[sep=20pt]
  & I \times S
  \ar[dl, "{ \mathrm{out} }"{sloped}]
  \ar[dr, "{ \mathrm{trans} }"{sloped}]
  \\
  O && S
  \mathrlap{\,.}
\end{tikzcd}

In this form, a [[Cartesian product]] is not needed to pair these two operations, and hence it is tempting to consider a generalized notion of Mealy machines in (not-necessarily [[cartesian monoidal category|cartesian]]) [[symmetric monoidal categories]] $(\mathcal{C}, \otimes, \mathbb{1})$, given by [[spans]] of the above form, but using the given [[monoidal product]] to pair what are now $\mathcal{C}$-objects $I$ and $S$:

\begin{tikzcd}[sep=20pt]
  & I \otimes S
  \ar[dl, "{ \mathrm{out} }"{sloped}]
  \ar[dr, "{ \mathrm{trans} }"{sloped}]
  \\
  O && S
  \mathrlap{\,.}
\end{tikzcd}

This definition is considered for instance in [BLLL23a, Def. 2.1](#BLLL23a). 

An evident notion of [[homomorphisms]] between such spans are maps $f \colon S \to S'$ such that the following [[commuting diagram|diagram commutes]] ([BLLL23a, Rem. 2.2](#BLLL23a)):

\begin{tikzcd}[sep=20pt]
  & I \otimes S
  \ar[dl, "{ \mathrm{out} }"{sloped}]
  \ar[dr, "{ \mathrm{trans} }"{sloped}]
  \ar[dd, "{ I \otimes f }"{description}]
  \\
  O 
  \ar[dd, equals]
  && 
  S
  \ar[dd, "{f}"]
  \\
  & 
  I \otimes S'
  \ar[dl, "{ \mathrm{out}' }"{sloped}]
  \ar[dr, "{ \mathrm{trans}' }"{sloped}]
  \\
  O && S'  
\end{tikzcd}

The authors of &lbrack;[BLLL23a, Prop. 3.5](#BLLL23a)&rbrack; &lbrack;[BLLL23b, Def. 2.1](#BLLL23b)&rbrack; find it useful to rephrase this as follows:

\begin{definition}
\label{FoscoDefinition}
A Mealy machine internal to a [[symmetric monoidal category]] 
$(\mathcal{C},\,\otimes,\,\mathbb{1})$ for 

* input alphabet object $I \,\in\, Ob(\mathcal{C})$ 

* output alphabet object $O \,\in\, Ob(\mathcal{C})$ 

is an object of the following [[pullback]] $Mly(I,O)$ in [[Cat]]: 

\begin{centre}
\begin{tikzcd}
  \mathrm{Mly}(I,O)
  \ar[r]
  \ar[d] 
   & 
  (-\otimes I)/O 
  \ar[d, "V"]
  \\ 
  \mathrm{Alg}(-\otimes I) 
  \ar[r, "U"']
  &
  \mathcal{C}
  \mathrlap{\,,}
\end{tikzcd}
\end{centre}

where:

* $Alg(-\otimes I)$ is the category of [[algebra over an endofunctor|algebras over]] the [[endofunctor]]

  $$
    \array{
      \mathllap{
        (\text{-})\otimes I \,\colon\;
      }        
      \mathcal{C} 
        &\longrightarrow&
      \mathcal{C} 
      \\
      S &\mapsto& S\otimes I
     }
   $$

* $U$ is the forgetful functor, 

* $(-\otimes I)/O$ is the [[comma category]] of morphisms $out \colon  X\otimes I\to O$, 

* $V$ is the forgetful functor $(X,out)\mapsto X$.

\end{definition}

\begin{remark}

If $\mathcal{C}$ has [[countable set|countable]] [[coproducts]], a semiautomaton $trans \colon S\otimes I \to S$ consists of an [[action#actions_of_a_monoid|action]] of the [[free monoid]] on $I$, $\sum_{n=0}^\infty I^{\otimes n}$; this is well-explained [[action#actions_of_a_set|_ibi_]]. 

Concisely, there is an [[equivalence of categories]]
\[
  Alg(-\otimes I) \simeq EM(I^*)
\]
between $I$-semiautomata and the [[Eilenberg-Moore category]] of the monad [[action monad|induced]] by the monoid $I^*$.
\end{remark}

Then, a Mealy machine as in Def. \ref{FoscoDefinition} consists (except for the specification of the initial state) of a [[span]]
\[ 
  S \leftarrow S\otimes I \to O
  \,.
\]



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

Discussion in symmetric monoidal categories:

* {#BLLL23a} Guido Boccali, Andrea Laretto, [[Fosco Loregian]], Stefano Luneia, *Completeness for categories of generalized automata* &lbrack;[arXiv:2303.03867](https://arxiv.org/abs/2303.03867)&rbrack;

* {#BLLL23b} Guido Boccali, Bojana Femić, Andrea Laretto, [[Fosco Loregian]], Stefano Luneia, *The semibicategory of Moore automata* &lbrack;[arXiv:2305.00272](https://arxiv.org/abs/2305.00272)&rbrack;



[[!redirects Mealy machines]]
