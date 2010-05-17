#Contents#
* the following line creates the automatic table of contents
{:toc}


## Idea ##
The classical Gleanson's theorem says that a state of the [[C-star algebra]] $\mathcal{B}(\mathcal{H})$ of all [[bounded operators]] on a [[Hilbert space]] is uniquely described by the values it takes on the orthogonal projections $\mathcal{P}$, if the dimension of the [[Hilbert space]] $\mathcal{H}$ is not 2.

It is possible to extend the theorem to certain types of [[von Neumann algebras]] (e.g. obviously factors of type $I_2$ have to be excluded).

### Implications for Quantum Logic
Roughly, Gleason's theorem says that "a quantum state is completly determined by only knowing the answers to all of the possible yes/no questions".

## Abstract ##
...

## Definitions ##

+-- {: .un_def}
###### Definition
Let $\rho: \mathcal{P} \to [0, 1]$ such that for every finite family $\{ P_1, ..., P_n: P_i \in \mathcal{P} \}$ of pairwise orthogonal projections we have $\rho(\sum_{i=1}^n P_i) = \sum_{i=1}^n \rho(P_i) $, then $\rho$ is a **finitely additive measure** on $\mathcal{P}$.

If the family is not finite, but countable, then $\rho$ is a **sigma-finite measure**.
=--

## The Theorem ##

### classical Gleason's theorem

+-- {: .un_theorem}
###### Theorem
If $dim(\mathcal{H}) \neq 2$ then each finitley additive measure on $\mathcal{P}$ can be uniquely extended to a state on $\mathcal{B}(\mathcal{H})$. Conversly the restriction of every state to $\mathcal{P}$ is a finitley additive measure on $\mathcal{P}$.

The same holds for sigma-finite measures and [[normal states]]: Every sigma-finite measure can be extended to a normal state and every normal state restricts to a sigma-finite measure.
=--

### Extension to Certain Types of von Neumann Algebras
...


## Examples ##

### Counterexample For Dimension Two ###
The counterexample is from the book by Parthasarathy (see references), which uses a different terminology from what we did, so we will have to introduce some new concepts: 

+-- {: .un_def}
###### Definition
A sigma-finite measure with $\rho(\mathbb{1}) = 1$ is called a (quantum) **probability distribution**.
=-- 

...

## References ##

* Wikipedia on [Gleason's theorem] (http://en.wikipedia.org/wiki/Gleason%27s_theorem)

A monograph stating and proving both the classical theorem and extensions to von Neumann algebras is this:

* Hamhalter, Jan: "Quantum measure theory." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1038.81003&format=complete))

The classical theorem is proved also in this monograph:

* K.R. Parthasarathy: _An Introduction to Quantum Stochastic Calculus_ ([ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0751.60046&format=complete))
