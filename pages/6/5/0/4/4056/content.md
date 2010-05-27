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
See example 8.1 in the book by Parthasarathy (see references).
Our Hilbert space is $\mathbb{R}^2$. Projections $P$ on it are either identical zero, the identity, or projections on a one dimensional subspace, so that these $P$ can be written in the [[bra-ket notation]] as
$$
 P = |u \rangle \langle u|
$$
with a unit vector $u$, i.e. $u \in \mathbb{R}^2, \|u\| = 1$. In this finite dimensional case sigma-finite and finite are equivalent, and a finite probability measure is equivalent to a (complex valued) function such that
$$
f(c u) = f(u)
$$ 


$$
\sum_i f(u_i) = 1
$$ 
for every scalar $c$ of modulus one, every unit vector $u$ and every orthonormal basis $\{u_1, u_2\}$. If there is a state that extends such a measure and therefore restricts to such a measure on projections, there would be a linear operator $T$ such that
$$
f(u) = \langle u | Tu \rangle
$$
for all unit vectors $u$.

It turns out however that the conditions imposed on $f$ are not enough in two dimensions to enforce this kind of linearity of $f$. Heuristically, in three dimensions there are more rotations than in two, therefore the "rotational invariance" of (the conditions imposed on) $f$ is more restrictive in three dimensions than it is in two dimensions.

In two dimensions, choose a function $g$ on $[0, \frac{\pi}{2})$ such that $0 \le g(\theta) \le 1$ everywhere. There are no further restrictions, that is $g$ need not be continuous, for example. Now we can define a probability measure on the projections by
$$
f(u) = 
\begin{cases}

  g(\theta) \; \; \text{for} \; \; 0 \le \theta \lt \frac{\pi}{2} \\
  1 - g(\theta -  \frac{\pi}{2}) \; \; \text{for} \; \; \frac{\pi}{2} \le \theta \lt \pi \\
  f(-u) \; \; \text{as defined in the first two items, else}
\end{cases}
$$
This probability measure will in general not extend to a state.

## References ##

* Wikipedia on [Gleason's theorem] (http://en.wikipedia.org/wiki/Gleason%27s_theorem)

Gleason's original paper outlining the theorem:

* A.M. Gleason "Measures on the closed subspaces of a Hilbert space," Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050).

A monograph stating and proving both the classical theorem and extensions to von Neumann algebras is this:

* Hamhalter, Jan: "Quantum measure theory." ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1038.81003&format=complete))

The classical theorem is proved also in this monograph:

* K.R. Parthasarathy: _An Introduction to Quantum Stochastic Calculus_ ([ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0751.60046&format=complete))

[[!redirects Gleason's Theorem]]