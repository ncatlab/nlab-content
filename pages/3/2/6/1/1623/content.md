Here are notes by [[Urs Schreiber]] for Tuesday, June 9, from [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Oberwolfach]].


## Schick: differential cohomology ##


smooth cohomology

* idea:

  * combine cohomology + differential forms
  
main diagram


$$
  \array{
    \hat H(M) &\stackrel{I}{\to}& H^\bullet(M)
    \\
    \downarrow^{R} && \downarrow
    \\
    \Omega^\bullet_{d=0}(M)
    &\stackrel{}{\to}&
    H^\bullet_{dR}(M)
    \simeq H^\bullet(M,\mathbb{R})
  }
$$

so differential cohomology $\hat H^\bullet(M)$ combines the ordinary cohomology $H^\bullet(M)$
with a differential form representative of its image in real cohomology.

* $I$ projects a differential cohomology to its underlying ordinary cohomology class;

* $R$ send the differential cohomology class to its __curvature_ differential form data

we want an exact sequence

$$
 \array{
   H^{\bullet-1}(M)
   &\stackrel{ch}{\to}&
   \Omega^{\bullet-1}(M)/{im(d)}
   &\stackrel{d}{\to}&
   \hat H(M) 
   &\stackrel{I}{\to}& 
   H^\bullet(M) \to 0
   \\
   &&&
   {}_{d}\searrow
   &
   \downarrow^R
   \\
   &&&&
   \Omega^\bullet_{d=0}(M)
 }
$$

**definition**

Given cohomology theory $E^\bullet$, a smooth refinement
$\hat E^\bullet$ is a functor $\hat E : Diff \to Grps$
with transformations $I, R$ such that 

$$
  \array{
    \hat E(M) &\stackrel{I}{\to}& E^\bullet(M)
    \\
    \downarrow^{R} && \downarrow
    \\
    \Omega^\bullet_{d=0}(M, V)
    &\stackrel{}{\to}&
    E^\bullet_{dR}(M)
    \simeq E^\bullet(M,\mathbb{R})
  }
$$

where 

$V = E^\bullet(pt)\otimes \mathbb{R}$

is the graded non-torsion cohomology of $E$ on the point. So now all the
gradings above denote total grading.

and such that there is a transformation

$$
  a : \Omega^{\bullet -1}(M)/{im(d)}
  \to
  \hat E^*(M)
$$

that gives the above kind of exact sequence


**definition**

if $E^*$ is multiplicative, we say $\hat E^*$ is multiplicative with 
product $\vee$
if $\hat E$ takes values in graded rings and the transformations are
compatible with multiplicative structure, where

$$
  a(\omega) \vee x = a(\omega \wedge R(x))
$$

**definition**

$\hat E$ has $S^1$-integration if there is a natural (in $M$) transformation

$$
  \int : \hat E^*(M \times S^1) \to \hat E^{\bullet -1}(M)
$$

compatible with $\int$ of forms  and for $E$ it is given by the suspension isomorphism

and

$$
  \int \circ p^* = 0
$$

for $p : M \times S^1 \to M$ and

$$
  \int \circ (  id \times (z \mapsto \bar z) )^* = - \int
$$


**remark** ordinary cohomology theories are supposed to be homotopy
invariant, but differential forms are not, so in general the differential
cohomology is not


**Lemma** Given $\hat E$ a smooth cohomology theory. 
The **homotopy formula**:

given $h : M \times [0,1] \stackrel{smooth}{\to} N$
a smooth homotopy we have

$$
  h^*_1(X) - h^*_0(X)
  =
  a( \int_{M \times [0,1]/M}  h^*(R(x)))
$$

**corollary** $ker(R)$ (i.e. flat cohomology) is a homotopy invariant
functor

**def** $\hat _H{flat} := ker(R)$

**proof of lemma**

suffices to show 

$$
  \iota_1^*(x) - \iota_0^*(x) = a(\int_{M\times [0,1]/M} R(x))
$$

for all $x \in \hat E(M \times [0,1])$

observe if $x = p^* y$ the left hand side vanishes, $\int R(p^* y) = 0$

for general $x$ $\exists y \in \jhat E(M)$; $x - p^*(y) = a (\omega)$
$\omega \in \Omega(M \times [0,1])$

Stokes' theorem gives $i^*_1 \omega - i^*_0 \omega = \int_{[0,1]} d \omega$
$= \int R(a(\omega)) = \int R(x-p^* \omega) = \int R(x)$

on the other hand

$$
  i^*_1(x) - i^*_0(x) = i^*_1(a(\omega))
    - i^*_0(a(\omega))
    = a(\int R(x))
$$

a calculation: $\hat H^1_{flat}(pt) = \hat H^1(pt) = \mathbb{R}/\mathbb{Z} = \hat K^1(pt)$

**Theorem (Hopkins-Singer)**

For each generalized cohomology theory $E^*$ 
a differential version  $\hat E^*$ as in the above definition does exist

Moreover $\hat E_{flat}^* = E \mathbb{R}/\mathbb{Z}^{\bullet -1}$

**remark** it's not evident hot to obtain more structure like multiplication

**theorem** using geometric models, multiplicative smooth extensions
with $S^1$-integration are constructed for

* K-theory (Bunke-Schick)

* MU-bordisms (unitary bordisms)  
  (Bunke-Schr&#246;der-Schick-Wiethaupts; and from there Landweber exact cohomology theories)
  

**uniqueness theorem (Bunke-Schick)** 
(Simons-Sullivan proved this for ordinary integral cohomology)

assume $E^*$ is _rationally even_, meaning that

$$
  E^k(pt)\otimes \mathbb{Q} = 0 \;\; for odd k 
$$

plus one further technical assumption

then any two smooth extensions $\hat E^*$, $\tilde E^*$ are naturally
isomorphic

such that if required to be compatible with integration the ismorphism is unique

if $\hat E, \tilde E$ are multiplicative, then this isomorphism is,
as well.

**example** if we don't require compatibility with $S^1$-integration, then there
are "exotic" abelian group structures on $\hat K^1$

## Bunke: smooth K-theory ##

(I gave up taking notes in that one, maybe somebody else
has notes?)


## Costello, part II ##

alternative to yesterday's axioms:

replace $B(M)$ by $Embeddings(\bar D^n, M)$

and replace $B_n(M)$ by

$$
  Embed(D^n, M) \times Enb(\bar D^n \coprod \cdots \coprod \bar D^n, \bar D^n)
$$

* what is the classical analog of a factorization algebra?

* and how do we get classical QFT?

**basic idea**

factorization algebras form a symmetric monoidal category

so we can look at [[algebra over an operad]] in the category of factorization
algebras

if $F, F'$ are factorization algebras, then
$$
  (F\otimes F')(B) = F(B) \otimes F'(B)
$$

**def** a **classical factorization algebra** is a commutative algebra
in the category of factorization algebras


recall, an $E_\infty$ object in $E_n$-algebras is an $E_\infty$-algebra

idea of how to associate a classical factorization algebra to a classical field
theory is as follows

suppose we have classical field theory, e.g. space of fields is
section of a vector bundle $E \to M$

$$
  S : \Gamma(M,E) \to \mathbb{R}
$$

is the classical action

$S$ is local: obtained by $int$ of a Lagrangian

if $B  \subset M$ is a ball, let

$$
  EL(B) = 
  \left\{
    \phi \in \Gamma(interior(B), E)
    such that \phi satisfies Euler-Lagrange equations
  \right\}
$$

>Freed: notice that you are doing here classical QFT in Euclidean signature
>Costello: yes

**rough idea** 

the classical factorization algebra $X_S$ associated to $S$ 
assigns to $B$, the algebra 

$$
  O(EL(B))
$$

of functions on the set of solutions to $EL$.

we want maps

$$
  X_S(B_1) \otimes \cdots \otimes X_S(B_n)
  \to
  X_S(B_{n+1})
$$

for $B_i$ in $B_{n+1}$

we have a map 

$$
  EL(B_{n+1}) \to EL(B_1)\times \cdots \times EL(B_n)
$$

this yields a map

$$
  O(EL(B_1)) \otimes \cdots \otimes O(EL(B_{n+1}))
$$

as desried

**simple example**

fields are $C^\infty$ functions on $M$

$$
  S(\phi) := \int_M \phi \Delta \phi
$$

Euler-Lagrange equation is $\Delta \phi = 0$

$$
  EL(B) = \{Harmonic functions on the interior of B\}
$$

$$
  O(EL(B)) = \prod_{n \geq 0} Hom(EL(B)^{\otimes n}, \mathbb{R})^{S_n}
$$

where Hom means continuous linear maps, and where $\otimes$ is the completed
tensor product

later, for more complex examples, what we really want to do is
to take the _derived_ space of EL solutions

**question**

Why does this classical factorization algebra want to become just a
factorization algebra?

recall that fact-algebras form a symmetric monoidal category

the $E_0$-[[operad]] is defined by 

* $E_0(n) = \emptyset$ for $n \geq 1$

* $E_0(0) = pt$

so for instance an $E_0$-algebra in $Vect$ is a vector space with an element

forgot to mention that factorization algebras need to have a unit,
a section $F$ on $B(M)$ which is a unit for the product

So: an $E_0$-algebra in factorization algebras is just a factorization algebra




$$
 \array{
     graded commutative algebra with Poisson bracket of deg +1
     &\stackrel{quantize}{\to}& 
     E_0-algebras (in co[[chain complex]]es)
     \\
     Poisson &\stackrel{quantize}{\to}& E_1-algebras
     \\
     graded comm algebra with Poisson bracket of deg -1
    &\stackrel{quantize}{\to}& 
    E_2-algebras
     \\
     graded comm algebra with Poisson bracket of deg -2
    &\stackrel{quantize}{\to}& 
    E_3-algebras
  }
$$

Beilinson and Drinfeld define an operad over (i.e. in the category of
cochain complex moudles over) the ring of formal power
series over $\hbar$
$$
  \mathbb{R}[\![\hbar]\!]
$$

as follows:

* generated by $\cdot$, a commutative product

* $\{-,-\}$ a Poisson bracket of deg +1

* with differential $d(-) = \hbar \{-,-\}$

call this the **BD operad**

$$
  BD/\hbar BD = operad of commutative algebras with \{-,-\} of deg +1
$$

$$
  H_\bullet(BD(n) \otimes_{\mathbb{R}[\![\hbar]\!]} \mathbb{R}(\hbar))  = 0
$$

so 

$$
  BD \otimes_{\mathbb{R}[\![\hbar]\!]} \mathbb{R}[\![\hbar]\!]
  \simeq E_0
$$

**rant on [[BV-theory]] termionology**

framed $E_2$, which is often called the _BV-operad_ 
has **nothing** to do with the [[BV-theory]]


instead: the BD-operad from above is the one related to [[BV-theory]]

**def** the $P_0$ (or $Poisson_0$) operad is the operad
of commutative Poisson algebras with $\{-,-\} of deg 1$

so $P_0 = BD/\hbar$

**general fact**

let $M$ be a manifold, and $f : M \to \mathbb{R}$ a function, then
$O(derived critical locus of f)$ is a $P_0$-operad

derived critical locus has as functions the [[differential graded algebra]]


$$
  \cdots 
   \Gamma(M,\Lambda^2 T M)
  \stackrel{\vee d f}{\to}
   \Gamma(M,\Lambda^ T M)
  \stackrel{\vee d f}{\to}
   O(M)
  =
  \Gamma(M, \Lambda^\bullet T M)
$$


here $\Lambda^k T M $ is in degree $-k$ with differential $\vee d f$

$$
  \Gamma(M, \Lambda^\bullet T M)
$$

has Schouten bracket, which is of degree +1

This "wants to become" $E_0$

**observation** if $M$ has a [[measure]], then 
$O(crit^n(f))$ has a canonical quantization to an 
algebra over $BD$.

then quantization is

$$
  \Gamma(M, \Lambda^\bullet T M), \vee d f + \hbar \Delta
$$


here $\Delta$ arises whenever $M$ has a measure

$$
  \Delta X = Div X
$$

$$
  X \in \Gamma(M, T M)
$$



## Costello, part III ##

so recall that the derived critical locis if a function is a $P_0$-algebra,
so it wants to quantize to $E_0$

if we have a classical field theory, the derived space of 
solutions to EL yields a $P_0$ algebra in factorizatoin algebra

so it wants to become a factorization algebra

**Example** $\phi \in C^\infty(M)$, $S(\phi) = \int \phi \Delta \phi$

derived space of solutions to EL is the complex

$$
 \array{
  C^\infty(M) &\stackrel{\Delta}{\to}&
    C^\infty(M)
  \\
    0 && 1
 }
$$

if $B \subset M$ is a ball, then

$$
  O(EL^n(B))
  =
  \Pi_{n \geq 0}(
     Hom( C^\infty(int B) \stackrel{\Delta}{\to} C^\infty(int B))^{\otimes n},
     \mathbb{R}
  )^{S_n}
$$

this is a commutative dga and defines a commutative factorizaton algebra

if we add an interaction term to the action functional

$$
  S(\phi)
  =
  \int \phi \Delta \phi + \phi^3
$$

then we get the same algebra of functions but the differential changes

in Yang-Mills theory with gauge Lie algebra $g$: 
first, we consider the derived quotient of
$\Omega^1(M)\otimes g$ by $\Omega^0(M)\otimes g$, then, take derived critical
locus of YM action

What we get, when linearized looks like

$$
  (
  \array{
     \Omega^0(M) &\to& \Omega^1(M) &\stackrel{d \star d}{\to}& \Omega^3(M)
       &\stackrel{}{\to}& \Omega^4(M)
     \\
     -1 && 0 && 1 && 2
  }) \otimes g
$$

the algebra of functions iss 
$$
  \Pi_{n \geq 0} Hom(E^{\otimes n}; \mathbb{R})^{S_n}
$$

with diffeential including YM action

**theorem**
if we take the derived space of solutions to the EL equations,
looking infinitesimally near a fixed solution, then we find
a $P_0$-algebra internal to factorization algebras on $M$

this amounts to quantizing the action $S$ into a solution
of the quantum master equation

this requires machinery of counter-terms, Wilsonian effective 
actions, to even define the quantum master equation

>see Kevin Costello's book linked to on hos website for details

**theorem** (joint with O. Gwilliam)

("wave" version)

conssider the scalar field theory, with an action of the form

$$
  S(\phi) = \int \phi (\Delta \phi + m^2 \phi)
  + arbitrary local higher terms
$$ 

use the above theorem, around the 0-solution

Let $X_S$ be the classical factorization algebra associated to it
(it is a $P_0$-algebra)

Let $Q^{(n)}(X_S)$ be the set of quantizations

= $\{lifts of $X_S$ to an algebra over BD/{\hbar^{n+1}}\}$

there is a sequence $T^{(n)} \to T^{(n-1)} \to \cdots \to T^{(1)} \to pt$

where $T^{(n)}$ maps to $Q^{(n)}(X_S)$, so that the obvious diagram commutes

where $T^{(n)} \to T^{(n-1)}$ is a torsor for the abelian group of local
functions of the field $\phi$

so $T^{(\infty)} = lim_n T^n$ then

$$
  T^{(\infty)} \simeq \{\sum_{k \geq 1} \hbar^k S^{(k)}\}
$$

$
 S^{(k)}
$ is a local function, but this is non-canonical

**more sophisticated version**

consider any reasonable classical theory, with its
classical factorization algebra $X_S$

let $Q^{(n)}(X_S) = simplicial set of possible quantizations defined mod \hbar^{n+1}$

$
  Der_{loc}(X_S)
$ 
is the cochain complex of derivations of $X_S$, preserving
$P_0$-structure (is, in fact, local functions on an extended space)

theorem

there exists a sequence of simplicial sets

$$
  T^{(n)} \to T^{(n-1)}
  \to 
  \cdots \to 
  T^{(1)}
  \to pt
$$

with maps $T^{(n)} \to Q^{(n)}(X_S)$

such that $T^{(n)}$ fits into a [[homotopy limit|homotopy fiber diagram]]

$$
  \array{
    T^{(n)}
    &\to&
    0
    \\
    \downarrow
    &&
    \downarrow
    \\
    T^{n-1} &\stackrel{obstruction}{\to}& Der_{loc}(X_S)[2]
  }
$$

so we get obstructions; for instance for $\phi^4$-theory the obstruction is
the famous $\beta$-function

**theorem**
Let $g$ be a simple Lie algebra. Then there is a
quantization of Yang-Mills theory on $\mathbb{R}^4$
which is "renormalizable"
(behaves well with respect to scaling)

the set of quantizations is 1-dimensional term by term

The set of such quantizations is $\hbar \mathbb{R}[\![\hbar]\!]$


**correlation functions**

Where do correlation functions appear?

If $F$ is a factorization algebra on $M_S$, corresponding to some
QFT, then $F(B) = \{measurements we can make on the ball B\}$

if $B_1, B_2 \subset B$  are disjoint, the maps
$$
  F(B_1)\otimes F(B_2) \to F(B)
$$

is defined by doing both observations

correlation functions should be cochain maps

$$
  \langle 
    F(B_1) \otimes \cdots \otimes F(B_n) \to \mathbb{R}
  \rangle
$$

if $B_1, \cdots, B_n$ are disjoint, if 
$
  O_i \in F(B_i)
$

then

$$
  \langle O_1, \cdots, O_n\rangle
$$
is a measurement of how to observe $O_i$ correlations

if $B_1, B_2 \subset \tilde B$ the diagram

$$
  \array{
    F(B1) \otimes \cdots \otimes F(B_n)
    &\stackrel{\langle \cdots \rangle}{\to}&
    \mathbb{R}
    \\
    \downarrow && \uparrow^{\langle \cdots \rangle}
    \\
    F(\tilde B) \otimes F(B_3) \otimes \cdots \otimes F(B_n)
  }
$$

should commute (operator product expansion)

we can consider correlation functions with coefficients in any
cochain complex, we require they must satisfy this equation

**def** (Beilinson-Drinfeld)

$$
  CH_\bullet(M,F)
  =
  homotopy universal recipient of correlation functions
$$

$$
  = colim_{B_1, \cdots B_n \subset M disjoint}
F(B_1) \otimes \cdots F(B_n) 
$$

(Kevin Walker (blob homology), Jacob Lurie (topological chiral homology))

**lemma**
for a massive scalar field,

$$
  CH_\bullet(M,F) \simeq \mathbb{R}[\![\hbar]\!]
$$

in general

$
  CH_\bullet(M,F)
$ looks like measures on the space of critical points of the classical action

if we perturb around isolated critical points, 
$
  CH_\bullet(M,F)
  =
  \mathbb{R}[\![\hbar]\!]
$ 

in this situation correlation functions exist and are unique

general program: correlation functions define a measure 
on the space of classical solutions

(Feynman graphs appear here as homotopies between operads, or something, 
see his book)

***

[[Oberwolfach Workshop, June 2009 -- Monday, June 8|Previous day]] --- [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Main workshop page]] --- [[Oberwolfach Workshop, June 2009 -- Wednesday, June 10|Next day]]