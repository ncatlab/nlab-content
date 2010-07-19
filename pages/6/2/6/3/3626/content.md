# Frobenius algebra
* table of contents
{: toc}


## Definition

+-- {: .num_defn}
###### Definition
A Frobenius algebra in a [[monoidal category]] is a quadruple $(A, \delta, \epsilon, \mu, \eta)$ such that

1. $(A, \mu, \eta)$ is a [[monoid]],
1. $(A, \delta, \epsilon)$ is a [[comonoid]], and
1. $(1 \otimes \mu) \circ (\delta \otimes 1) = \delta \circ \mu = (\mu \otimes 1) \circ (1 \otimes \delta)$.
=--

Frobenius algebras were originally formulated in the category of vector spaces with the following equivalent definition:

+-- {: .num_defn}
###### Definition
A **Frobenius algebra** is a unital, associative algebra $(A, \mu, \eta)$ equipped with a linear form $\epsilon : A \rightarrow k$ such that $\epsilon\mu$ is a non-degenerate pairing. I.e. the induced map

\[  u \mapsto \epsilon\mu(1 \otimes u) \]

is an isomorphism of $V$ with its dual space $V^*$. In such a case, $\epsilon$ is called a **Frobenius form**.
=--

From this definition it is easy to see that every Frobenius algebra in [[Vect]] is necessarily finite-dimensional.

There are about a dozen equivalent definitions of a Frobenius algebra. [Ross Street (2004)](#Street2004) lists most of them.

## Types of Frobenius algebras

### Commutative Frobenius algebras ###

We can define 'commutative' Frobenius algebras in any [[symmetric monoidal category]].  Namely, a Frobenius algebra is **commutative** if its associated monoid is commutative --- or equivalently, if its associated comonoid is cocommutative.  

### Symmetric Frobenius algebras ###

We can define 'commutative' or 'symmetric' Frobenius algebras in any [[symmetric monoidal category]].  A Frobenius algebra $A$ is **symmetric** if 
$$\epsilon S_{A,A} = \epsilon \, $$
where $S_{A,A} : A \otimes A \to A \otimes A$ is the symmetry.  Any commutative Frobenius algebra is symmetric, but not conversely: for example the algebra of $n \times n$ matrices with entries in a field, with its usual trace as $\epsilon$, is symmetric but not commutative when $n \gt 1$.  

A theorem of Eilenberg and Nakayama says that in the category of vector spaces over a field $k$, an algebra $A$ can be equipped with the structure of a symmetric Frobenius algebra if (but not only if) it is **separable**, meaning that for any field $K$ extending $k$, $A \otimes_k K$ is a [[semisimple algebra|semisimple]] algebra over $K$.   

### Special Frobenius algebras ###

If $\mu \circ \delta = 1$, a Frobenius algebra is said to be **special**.   In the category of vector spaces, any element $a$ of an associative unital algebra gives a left multiplication map 
$$ \array{ 
L_a : &A &\to& A \\
      &b &\mapsto& a b 
}
$$
which in turn gives a bilinear pairing $g: A \times A \to k$ defined by
$$ g(a,b) = tr(L_a L_b) $$
One can show that the algebra $A$ can be equipped with the structure of a special Frobenius algebra if and only if $g$
is nondegenerate, i.e., if there is an isomorphism $A \to A^*$ given by
$$ a \mapsto g(a, -)  $$
In this case, there is just one way to make $A$ into a special Frobenius algebra, namely by taking the counit to be 
$$ \epsilon(a) = tr(L_a) $$
(In any Frobenius algebra, the unit, multiplication and counit determine the comultiplication.)  

In fact, all the results of the previous paragraph generalize to Frobenius algebras in any symmetric monoidal category, since the proofs can be done using string diagrams.  

An associative unital algebra for which the bilinear pairing $g$ is nondegenerate is called **strongly separable**.  So, any strongly separable algebra becomes a special Frobenius algebra in a unique way.  For more details, see [[separable algebra]] and [Aguiar (2000)](#Aguiar2000).

We should warn the reader that [Rosebrugh et al (2005)](#Rosebrugh2005) call a special Frobenius algebra 'separable'. This usage conflicts with the standard definition of a [[separable algebra]] in the category of vector spaces over a field, so we suggest avoiding it.

### &#8224;-Frobenius algebras ###

If a Frobenius algebra lives in a monoidal [[†-category]], $(\delta)^\dagger = \mu$ and $(\epsilon)^\dagger = \eta$, then it is said to be a **&#8224;-Frobenius algebra**. These crop up in the theory of 2d [[TQFTs]], and also in the foundations of [[quantum mechanics in terms of dagger-compact categories|quantum theory]].

## PROPs for Frobenius algebras ##

Certain kinds of Frobenius algebras have nice [[PROPs]] or [[PRO|PROs]].  The PRO for Frobenius algebras is the monoidal category of planar thick tangles, as noted by Aaron Lauda.  The PROP for commutative Frobenius algebras is [[2Cob]], as noted by many people and formally proved by Lowell Abrams; see [Kock (2006)](#Kock2006).
   
The PROP for special commutative Frobenius algebras is Span(FinSet), as proved by Rosebrugh, Sabadini and Walters. This is worth comparing to the PROP for commutative [[bialgebra|bialgebras]], which is Cospan(FinSet).  For details, see [Rosebrugh et al (2005)](#Rosebrugh2005), and also [Lack (2004)](#Lack2004).


## References ##

* Lowell Abrams, 1996, Two-dimensional topological quantum field theories and Frobenius algebra, _Jour. Knot. Theory and its Ramifications_ **5** (1996), 569--587. 
{#Abrams1996}

* Marcelo Aguiar, 2000, A note on strongly separable algebras, Bolet&#237;n de la Academia Nacional de Ciencias (C&#243;rdoba, Argentina), special issue in honor of Orlando Villamayor, 65 (2000) 51--60.  ([gzipped postscript](http://www.math.tamu.edu/~maguiar/strongly.ps.gz))
{#Aguiar2000}

* John Baez, This Week's Finds in Mathematical Physics, [week268](http://math.ucr.edu/home/baez/week268.html) and [week299](http://math.ucr.edu/home/baez/week299.html).
{#BaezTWF}

* Samuel Eilenberg and Tadasi Nakayama, 1955, On the dimension of modules and algebras. II. Frobenius algebras and quasi-Frobenius rings, _Nagoya Math. J._ **9** (1955), 1--16. ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.nmj/1118799677))
{#Eilenberg1955}

* Joachim Kock, 2004, _Frobenius Algebras and 2d Topological Quantum Field Theories_, Cambridge U. Press, Cambridge, 2004.
{#Kock2004}

* Joachim Kock, 2006, Remarks on the history of the Frobenius equation.  ([web](http://mat.uab.es/~kock/TQFT.html#history))
{#Kock2006}

* Stephen Lack, 2004, Composing PROPs, Theory and Applications of Categories 13 (2004), 147--163.  ([web](http://www.tac.mta.ca/tac/volumes/13/9/13-09abs.html))
{#Lack2004}

* R. Rosebrugh, N. Sabadini and R.F.C. Walters, 2005, Generic commutative separable algebras and cospans of graphs, Theory and Applications of Categories 15 (Proceedings of CT2004), 164--177.  ([web](http://www.tac.mta.ca/tac/volumes/15/6/15-06abs.html))
{#Rosebrugh2005}

* R. Street, 2004, Frobenius monads and pseudomonoids, _J. Math. Phys._ **45** (2004).  ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.91.2686))
{#Street2004}


[[!redirects Frobenius algebra]]
[[!redirects Frobenius algebras]]
