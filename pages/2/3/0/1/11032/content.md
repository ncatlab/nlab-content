
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The concept of _traced monoidal category_ axiomatizes the structure on a [[monoidal category]] for it to have a sensible notion of ([[partial trace|partial]]) [[trace]] the way it exists canonically in [[compact closed categories]]. Traced monoidal categories sometimes only have _right_ or _left_ traces, and are referred to as _right traced_ or _left traced_ respectively. A category with compatible right and left traces is called a planar traced category. If the right and left traces agree, then we call a planar traced category _spherical_.

Graphically, the trace of an endomorphism $f:A\to A$ is represented by the closed loop

\begin{imagefromfile}
"file_name": "trace.png",
"width": 150,
"unit": "px"
\end{imagefromfile}

The ambiguity in whether to close the loop to the right or to the left is codified in the difference between left and right traced categories. Every [[pivotal category]] can be canonically made into a planar traced category by using its implicit distinguished morphisms to close loops. Pivotal categories which induce spherical traced structures are known as [[spherical categories]]. In this way, traced monoidal categories generalize the trace operation to categories which do not necessarily have duals.

In [[denotational semantics]] of programming languages, the trace is used to model [[recursion]], though if the language is not [[substructural logic|substructural]], then this can be simplified to a [[fixed point operator]].

## Definition

The original definition due to ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) is stated in the setting of [[balanced monoidal categories]]. Here we present a very general formulation, as given in [Selinger's survey](#Selinger2011).


A [[monoidal category]] $\mathscr{C}$ is said to be _right traced_ if it is equipped with family of [[maps]]

$$
  \tr^X_R
  \,\colon\,
  \text{Hom}(A\otimes X,B\otimes X)
    \longrightarrow
  \text{hom}(A,B)
$$

for all $A,B,X\in \mathscr{X}$, satisfying the following four axioms:

* {#Tightening} **Tightening** (naturality in $A,B$) For all $A,B,C,D,X\in\mathscr{C}$, $h \colon A\to B$, $f \colon B\otimes X\to C\otimes X$, $g \colon C\to D$

  $$
    \tr_R^X\big(
      (g\otimes \text{id}_X) 
        \circ 
      f \circ (h\otimes \text{id}_X)
   \big)
    \;=\;
    g \circ \tr_R^X(f) \circ h
  $$

* **Sliding** (naturality in $X$) for all $A,B,X,Y\in $, $f \colon A\otimes X\to B\otimes Y$, $g \colon Y\to X$

  $$
    \tr_R^{X}\big(
      (\text{id}_B\otimes g) \circ f
    \big)
    \;=\;
    \tr_R^{Y}\big(
      f \circ (\text{id}_A\otimes g)
    \big)
  $$

* **Vanishing** For all $A, B, X, Y \in \mathscr{C}$,

  $$
    \tr^1_R(f)
      \;=\;
    f,\,\, \forall \, f\colon A\to B
  $$

  and

  $$
    \tr^{X\otimes Y}_R(f)
    \;=\;
    \tr_R^X\big( \tr_R^Y(f) \big)
  $$

  for all $f \colon A\otimes X\otimes Y\to B\otimes X\otimes Y$.

* **Strength** For all $A,B,C,D,X\in \mathscr{C}$, $f \colon C\otimes X\to D\otimes X$, $g \colon A\to B$

  $$
    \tr_R^X(g\otimes f)
    \;=\;
    g \otimes \tr_R^X(f)
  $$

Graphically, we fix the notation for right trace

\begin{imagefromfile}
"file_name": "right-trace-graphical.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

The above axioms are described with the following pictures:

\begin{imagefromfile}
"file_name": "selinger-diagram-tracing.png",
"width": 550,
"unit": "px"
\end{imagefromfile}

In the presence of a [[braided monoidal category | braiding]] (such as in a [[symmetric monoidal category]]), we additionally require a _yanking_ axioms:

* **Yanking:** $Tr^X(\beta_{X,X}) = id_X$ for all $X\in\mathscr{C}$

where $\beta:X\otimes X\to X\otimes X$ is the braiding.

A left traced category is defined similarly, with a family of morphisms

$$\tr_L^X:\text{Hom}(X\otimes A,X\otimes B)\to \text{Hom}(A,B)$$

satisfying symmetric axioms. We write the left trace graphically as

\begin{imagefromfile}
"file_name": "left-trace-graphical.png",
"width": 300,
"unit": "px"
\end{imagefromfile}

A planar traced category is a monoidal category $\mathscr{C}$ which is simultaneously left and right traced, such that the following axioms are satisfied:

* **Interchange** For all $A,B,X,Y\in \mathscr{C}$, $f:Y\otimes A\otimes X\to Y\otimes B\otimes X$

$$\tr_R^X(\tr_L^Y(f))=\tr_L^Y(\tr_R^X(f)).$$

* **Left pivoting** For all $A,B\in\mathscr{C}$, $f:1\to A\otimes B$

$$\tr_R^B(\text{id}_B\otimes f)=\tr_L^A(f\otimes \text{id}_A).$$

* **Right pivoting** For all $A,B\in\mathscr{C}$, $f:A\otimes B\to 1$

$$\tr_R^B(\text{id}_B\otimes f)=\tr_L^A(f\otimes \text{id}_A).$$

Graphically, these axioms can be stated as below:

\begin{imagefromfile}
"file_name": "pivoting-axioms.png",
"width": 500,
"unit": "px"
\end{imagefromfile}

It is from these axioms that [[pivotal categories]] get their name.

A spherical trace category is a planar traced category in which the left and right partial traces agree. That is, for any endomorphism $f:A\to A$ in $\mathscr{C}$ we have that

$$\tr_R^A(f)=\tr_L^A(f).$$

## Examples

* The category of [[finite-dimensional vector spaces]] is traced monoidal. In skeletal form, the objects are natural numbers regarded as dimensions, morphisms are matrices regarded as linear maps, and tensor product is multiplication of the dimensions. The trace is a minor generalization of matrix trace:
$$ Tr_{m,n}^p((a_{(i,k),(j,k')})_{(i,k),(j,k')\in m\times p\times n\times p})_{i,j}=
\sum_{k=1}^p a_{(i,k),(j,k)}.$$
This is an instance of a trace in a compact closed category. 

* The category of [[profunctors]] is also compact closed, hence traced monoidal (actually a bicategory, though). The trace of a profunctor $H:(B\times X)^{op} \times A\times X\to \mathbf{Set}$ is the profunctor $Tr_{A,B}^X(H):B^{op}\times A\to \mathbf{Set}$ given by the [[coend]] formula:
$$ Tr(H)(b,a)=\int^x H(b,x,a,x) .$$

* The category of sets and [[partial functions]] with the coproduct monoidal structure is traced, if we let the trace of a partial function
$f:A+X\to B+X$ be defined as follows. First, let $f_{A,B}:A\to B$, $f_{X,X}:X\to X$ and so on be the evident partial functions that come from restricting the domain and codomain of $f$. Then define
$$Tr_{A,B}^X(f)(a)=b$$
if either $f_{A,B}(a)=b$ or if there exists $n$ such that $b=f_{X,B}(f_{X,X}^n(f_{A,X}(a)))$. 
See for instance Section 5.2 of ([Abramsky, Haghverdi and Scott](#AbramskyHaghverdiScott02)). This is an example of a partially additive category.

  This is a basis for a categorical semantics of "while loops" in programming languages: we keep applying $f$ _while_ it is returning in $X$. 

* Consider the category of pointed [[cpo]]'s and continuous functions. A pointed cpo is a [[poset]] with a bottom element $\bot$ and least upper bounds of $\omega$-chains. The morphisms preserve least upper bounds of chains but are not required to preserve bottom elements. This is a [[cartesian monoidal category]], and with this structure it is traced, if we let the trace of a continuous function $f:A\times X\to B\times X$ be given as follows.
First, for fixed $a\in A$, let $x_a\in X$ be the least [[fixed point]] of 
$(\pi_2\cdot f(a,-)):X\to X$, writing $\pi_2$ for the second product projection. Here the least fixed point exists by Tarski's fixed point theorem, indeed 
$$x_a=\bigvee_n(\pi_2\cdot f(a,-))^n(\bot).$$
Then we let
$$Tr_{A,B}^X(f)(a)=\pi_1(f(a,x_a))\in B$$
In [[Haskell]] notation, where 'let' allows recursive definitions, we can more swiftly just write
$$Tr_{A,B}^X(f)(a)\ \ \ = \ \ \ let\ (b,x)=f(a,x)\ in\ b$$ 
(except that the built-in product types in Haskell are lifted products rather than categorical products: $(A,B)$ in Haskell is like $A\times B$ but with an extra bottom element added). 

  This is an example of a cartesian category with a parameterized fixed point operator ([Hasegawa 1997](#Hasegawa97)).


* Let $M$ be a [[cancellative monoid| cancellative commutative monoid]]. Write $\mid$ the divisibility relation i.e. for every $a,b \in M$, we write $a \mid b$ iff there exists $c \in M$ such that $b=ca$. Then $(M, \mid)$ is a [[preordered set]], as such it is a [[thin category]]. Moreover $(M, \mid)$ becomes a monoidal category if we define $a \otimes b = ab$ for every $a,b \in M$, with monoidal unit the unit $1$ of the monoid. Note that tensor product of morphisms is obtained via the compatibility of the multiplication with divisibility: if $a \mid b$ and $c \mid d$, then $ac \mid bd$. This monoidal category is traced since if $ac \mid bc$, then $a \mid b$. In particular if $R$ is an integral domain, then $(R \backslash \{0\}, \mid, \cdot, 1)$ is a traced (symmetric) monoidal category. Note that since $(M, \mid)$ is thin, all the coherence diagrams of the trace commute automatically. 

## Properties

### Relation to compact closed categories
 {#RelationToCompactClosedCategories}

Every [[compact closed category]] is equipped with a canonical trace defined by

$$ Tr_{A,B}^X(f) = A \overset{id\otimes \eta}{\to} A \otimes X \otimes X^* \overset{f \otimes id}{\to} B \otimes X \otimes X^* \overset{id \otimes \varepsilon'}{\to} B$$ 

where $\eta$ is a unit and $\varepsilon'$ is a counit of appropriate [[adjunctions]] (note that the symmetry makes the dual $X^*$ both a right and left adjoint of $X$: the adjunctions are ambidextrous).

Conversely, given a traced monoidal category $\mathcal{C}$, there is a [[free construction]] completion of it to a [[compact closed category]] $Int(\mathcal{C})$ ([Joyal-Street-Verity 96](#JoyalStreetVerity96)):

the objects of $Int(\mathcal{C})$ are pairs $(A^+, A^-)$ of objects of $\mathcal{C}$, a morphism $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ is given by a morphism of the form $A^+\otimes B^- \longrightarrow A^- \otimes B^+$ in $\mathcal{C}$, and [[composition]] of two such morphisms $(A^+ , A^-) \to (B^+ , B^-)$ and $(B^+ , B^-) \to (C^+ , C^-)$ is given by [[trace|tracing out]] $B^-$ from the composite
$$ A^+ \otimes B^- \otimes C^- \xrightarrow{f\otimes 1} A^- \otimes B^+ \otimes C^- \xrightarrow{1\otimes g} A^- \otimes B^- \otimes C^+. $$
Note that $\mathcal{C}$ embeds [[fully faithful functor|fully-faithfully]] in $Int(\mathcal{C})$ by sending $A$ to $(A,I)$, where $I$ is the unit object of the monoidal structure.

Furthermore, a traced monoidal category that is $\ast$-[[star-autonomous category|autonomous]] must already be compact closed; see [HH13](#HH13).

### In cartesian monoidal categories

For a [[cartesian monoidal category]], the existence of a trace operator is equivalent to the existence of a "parameterized" [[fixed point]] operator satisfying certain properties ([Hasegawa 1997](#Hasegawa97)). When the category is a [[Lawvere theory]], this is related to the notion of [[iteration theory]]. 

### Adding traces

Since any full monoidal subcategory of a traced monoidal category inherits a trace, not every monoidal category can be fully embedded into a traced monoidal category, and hence also not into a compact closed category.  In fact, Plotkin observed that there are monoidal categories that cannot even be *faithfully* mapped into a traced monoidal category.  This can be seen from the fact that a traced monoidal category has the "cancellation property" that if $f\otimes id_{X\otimes X} = g \otimes id_{X\otimes X}$ then $f\otimes id_X = g\otimes \id_X$ (since the latter is a trace of the former with one of the copies of $X\otimes X$ transposed), but not all monoidal categories have this property.


### Relation to feedback categories

[[feedback categories|Feedback categories]]$\;$[KSW02](#KatisSabadiniWalters02) are a weakening of the axioms of traced monoidal categories. Feedback categories do not satisfy the yanking axiom and they only satisfy a weaker form of naturality on the object to be traced. Examples include some categories of automata.

### Categorical semantics

Traced monoidal categories serve as an "operational" [[categorical semantics]] for [[linear logic]], known as _[[Geometry of Interactions]]_. See there for more.

In this context the free compact closure $Int(\mathcal{C})$ from [above](#RelationToCompactClosedCategories) is sometimes called the _Geometry of Interaction construction_ and denoted $\mathcal{G}(\mathcal{C})$ ([Abramsky-Haghverdi-Scott 02, def. 2.6](#AbramskyHaghverdiScott02)).


## References

The concept was introduced in

* {#JoyalStreetVerity96} [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. **119** (1996) 447-468 &lbrack;[pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf), [doi:10.1017/S0305004100074338](https://doi.org/10.1017/S0305004100074338)&rbrack;

A good exposition is found in

* {#Selinger2011} [[Peter Selinger]], _A survey of graphical languages for monoidal categories_, New structures for physics ([pdf](https://www.mscs.dal.ca/~selinger/papers/graphical-2up.pdf))

A characterization of trace structures on cartesian monoidal categories is given in

* {#Hasegawa97} [[Masahito Hasegawa]], _Recursion from Cyclic Sharing: Traced Monoidal Categories and Models of Cyclic Lambda Calculi_, Proc. 3rd International Conference on Typed Lambda Calculi and Applications (TLCA 1997). Springer LNCS1210, 1997 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.31))

The equivalence between traces and parameterized fixed point operators appears as Theorem 3.1 (the author notes that this theorem was also proved independently by [[Martin Hyland]]).

Comprehensive discussion as a source for [[categorical semantics]] of the [[Geometry of Interactions]] is in 

* {#AbramskyHaghverdiScott02} [[Samson Abramsky]], [[Esfandir Haghverdi]],  [[Philip Scott]], _Geometry of Interaction and Linear Combinatory Algebras_. MSCS, vol. 12(5), 2002, 625-665, CUP (2002) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.24.7818))

The combination with [[star-autonomous category|star-autonomous]] structure was discussed in

* Tamás Hajgató and [[Masahito Hasegawa]], *Traced $\ast$-autonomous categories are compact closed*, [TAC](http://www.tac.mta.ca/tac/volumes/28/7/28-07abs.html), 2013
 {#HH13}

Feedback categories and their connection to traced monoidal categories were discussed in

* {#KatisSabadiniWalters02} Piergiulio Katis, Nicoletta Sabadini, [[Bob Walters]].  Feedback, trace and fixed-point semantics, 2002 ([Numdam](http://www.numdam.org/item/ITA_2002__36_2_181_0/)).  


[[!redirects traced monoidal categories]]