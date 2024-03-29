
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

### General

The classical _Gleason theorem_ says that a [[state on a star-algebra|state]] on the [[C*-algebra]] $\mathcal{B}(\mathcal{H})$ of all [[bounded operators]] on a [[Hilbert space]] is uniquely described by the values it takes on the orthogonal [[projections]] $\mathcal{P}$, if the dimension of the [[Hilbert space]] $\mathcal{H}$ is not 2.

In other words: every [[quasi-state]] is already a state if  $dim(H) \gt 2$.

It is possible to extend the theorem to certain types of [[von Neumann algebras]] (e.g. obviously [[von Neumann algebra factor|factors]] of type $I_2$ have to be excluded).

Gleason's theorem is also valid for real and quaternionic Hilbert spaces as proved by Varadarajan in 1968. A gap of that proof has been fixed in 2018 by V.Moretti and M.Oppio. 


### Implications for Quantum Logic

Roughly, Gleason's theorem says that "a quantum state is completely determined by only knowing the answers to all of the possible yes/no questions".



## Definitions

+-- {: .num_defn}
###### Definition
Let $\rho: \mathcal{P} \to [0, 1]$ such that for every finite family $\{ P_1, ..., P_n: P_i \in \mathcal{P} \}$ of pairwise orthogonal projections we have $\rho(\sum_{i=1}^n P_i) = \sum_{i=1}^n \rho(P_i) $, then $\rho$ is a **finitely additive measure** on $\mathcal{P}$.

If the family is not finite, but countable, then $\rho$ is a **sigma-finite measure**.
=--


## The Theorem

### Classical Gleason's Theorem

+-- {: .num_theorem}
###### Theorem
If $dim(\mathcal{H}) \neq 2$ then each finitely additive measure on $\mathcal{P}$ can be uniquely extended to a state on $\mathcal{B}(\mathcal{H})$. Conversly the restriction of every state to $\mathcal{P}$ is a finitley additive measure on $\mathcal{P}$.

The same holds for sigma-finite measures and [[normal state|normal states]]: Every sigma-finite measure can be extended to a normal state and every normal state restricts to a sigma-finite measure.
=--


### Extension to Certain Types of von Neumann Algebras

...


### Gleason\'s Theorem for POVMs

In [[quantum information theory]], one often considers positive operator-valued measures ([[POVM]]s) instead of [[Hermitian operators]] as [[observables]].  While a Hermitian operator is given by a family of [[projection operator]]s $P_i$ such that $\sum_i P_i = 1$, a POVM is given more generally by any family of positive-semidefinite operators $E_i$ such that $\sum_i E_i = 1$.

In the analog of Gleason's Theorem for POVMs, therefore, we start with $\rho\colon \mathcal{E} \to [0,1]$, where $\mathcal{E}$ is the space of all positive-semidefinite operators.  Then if $\sum_i \rho(E_i) = 1$ whenever $\rho(\sum_i E_i) = 1$, the theorem states that $\rho$ has a unique extension to a mixed [[quantum state]].

As a theorem, Gleason\'s Theorem for POVMs is much weaker than the classical Gleason\'s Theorem, since we must begin with $\rho$ defined on a much larger space of operators.  However, some content does remain, since we have not assumed any continuity properties of $\rho$.  Also, Gleason\'s Theorem for POVMs has a much simpler proof, which works regardless of the dimension.


## Examples

### Counterexample For Dimension Two

See example 8.1 in the book by Parthasarathy (see references).
Our Hilbert space is $\mathbb{R}^2$. Projections $P$ on it are either identical zero, the identity, or projections on a one dimensional subspace, so that these $P$ can be written in the [[bra-ket notation]] as
$$
 P = {|u \rangle} {\langle u|}
$$
with a unit vector $u$, i.e. $u \in \mathbb{R}^2, {\|u\|} = 1$. In this finite dimensional case sigma-finite and finite are equivalent, and a finite probability measure is equivalent to a (complex valued) function such that
$$
f(c u) = f(u)
$$ 


$$
\sum_i f(u_i) = 1
$$ 
for every scalar $c$ of modulus one, every unit vector $u$ and every orthonormal basis $\{u_1, u_2\}$. If there is a state that extends such a measure and therefore restricts to such a measure on projections, there would be a linear operator $T$ such that
$$
f(u) = {\langle u | T u \rangle}
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

## Related theorems

Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]


## References

Gleason's original paper outlining the theorem:

* {#Gleason57} [[Andrew Gleason]], _Measures on the closed subspaces of a Hilbert space_, Journal of Mathematics and Mechanics,  Indiana Univ. Math. J. **6** 4 (1957), 885-893 &lbrack;[IUMJ:56050](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050), [pdf](http://www.iumj.indiana.edu/IUMJ/FTDLOAD/1957/6/56050/pdf)&rbrack;
 

Textbook accounts:

* [[Huzihiro Araki]], Theorem 2.3 (without proof) in: _[[Mathematical Theory of Quantum Fields]]_ ,


* [[Roland Omnès]], §3 of: *[[The Interpretation of Quantum Mechanics]]*, Princeton University Press (1994) &lbrack;[ISBN:9780691036694](http://press.princeton.edu/titles/5525.html)&rbrack;

A monograph stating and proving both the classical theorem and extensions to [[von Neumann algebras]]:

* Jan Hamhalter, _Quantum measure theory_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1038.81003&format=complete))

The classical theorem is proved also in this monograph:

* K. R. Parthasarathy, _An Introduction to Quantum Stochastic Calculus_ ([ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0751.60046&format=complete))

Gleason\'s Theorem for POVMs is proved here:

* Paul Busch, _Quantum states and generalized observables: a simple proof of Gleason's theorem_; (1999) ([arXiv](http://arxiv.org/abs/quant-ph/9909073)) 

The failure of Gleason's theorem for _classical_ states (on [[Poisson algebra]]s) is discussed in

* Michael Entov, Leonid Polterovich, _Symplectic quasi-states and semi-simplicity of quantum homology_ ([arXiv](http://arxiv.org/abs/0705.3735)).

Gleason\'s Theorem proved for real, complex and quaternionic Hilbert spaces using the notion of real trace. 

* [[Valter Moretti]], Marco Oppio, _The correct formulation of Gleason's theorem in quaternionic  Hilbert spaces_, Ann. Henri Poincaré 19 (2018), 3321-3355  ([arXiv:1803.06882](http://arxiv.org/abs/1803.06882))


See also

* Wikipedia on [Gleason's theorem] (http://en.wikipedia.org/wiki/Gleason%27s_theorem)


[[!redirects Gleason's theorem]]
[[!redirects Gleason's theorem]]
[[!redirects Gleason theorem]]
[[!redirects Gleason's Theorem]]
[[!redirects Gleason's Theorem]]
[[!redirects Gleason Theorem]]