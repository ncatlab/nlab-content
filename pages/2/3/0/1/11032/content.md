
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

The concept of _traced monoidal category_ axiomatizes the structure on a [[monoidal category]] for it to have a sensible notion of [[trace]] the way it exists canonically in [[compact closed categories]].

## Definition

The original definition due to ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) is stated in the general setting of [[balanced monoidal categories]].  Here we give just the slightly simpler formulation for the case of symmetric monoidal categories ([Hasegawa 1997](#Hasegawa97)).

A [[symmetric monoidal category]] $(C,\otimes,1,b)$ (where $b$ is the symmetry) is said to be **traced** if it is equipped with a natural family of functions

$$Tr_{A,B}^X : C(A \otimes X, B\otimes X) \to C(A,B)$$

satisfying three axioms:

* **Vanishing:** $Tr_{A,B}^1(f) = f$ (for all $f : A \to B$) and $Tr_{A,B}^{X\otimes Y}(f) = Tr_{A,B}^X(Tr_{A\otimes X,B\otimes X}^Y(f))$ (for all $f : A \otimes X \otimes Y \to B \otimes X \otimes Y$)

* **Superposing:** $Tr_{C\otimes A,C\otimes B}^X(id_C \otimes f) = id_C \otimes Tr_{A,B}^X(f)$ (for all $f : A \otimes X \to B \otimes X$)

* **Yanking:** $Tr_{X,X}^X(b_{X,X}) = id_X$

In [[string diagrams]], the trace $Tr(f) : A \to B$ of a morphism $f : A \otimes X \to B \otimes X$ is visualized by wrapping the outgoing wire representing $X$ to the incoming wire representing $X$, thus "tying a loop" in the diagram of $f$.  The three axioms above (as well as the naturality conditions) then all have natural graphical interpretations (see [Joyal-Street-Verity 96](#JoyalStreetVerity96) or [Hasegawa 1997](#Hasegawa97)).

## Examples

* The category of [[finite-dimensional vector spaces]] is traced monoidal. In skeletal form, the objects are natural numbers regarded as dimensions, morphisms are matrices regarded as linear maps, and tensor product is multiplication of the dimensions. The trace is a minor generalization of matrix trace:
$$ Tr_{m,n}^p((a_{(i,j),(i',j')})_{(i,j),(i',j')\in m\times p\times n\times p})_{i,i'}=
\sum_{j=1}^p a_{(i,j),(i',j)}.$$
This is an instance of a trace in a compact closed category. 

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

For a [[cartesian monoidal category]], the existence of a trace operator is equivalent to the existence of a "parameterized" [[fixed point]] operator satisfying certain properties ([Hasegawa 1997](#Hasegawa97)).

### Adding traces

Since any full monoidal subcategory of a traced monoidal category inherits a trace, not every monoidal category can be fully embedded into a traced monoidal category, and hence also not into a compact closed category.  In fact, Plotkin observed that there are monoidal categories that cannot even be *faithfully* mapped into a traced monoidal category.  This can be seen from the fact that a traced monoidal category has the "cancellation property" that if $f\otimes id_{X\otimes X} = g \otimes id_{X\otimes X}$ then $f\otimes id_X = g\otimes \id_X$ (since the latter is a trace of the former with one of the copies of $X\otimes X$ transposed), but not all monoidal categories have this property.

### Categorical semantics

Traced monoidal categories serve as an "operational" [[categorical semantics]] for [[linear logic]], known as _[[Geometry of Interactions]]_. See there for more.

In this context the free compact closure $Int(\mathcal{C})$ from [above](#RelationToCompactClosedCategories) is sometimes called the _Geometry of Interaction construction_ and denoted $\mathcal{G}(\mathcal{C})$ ([Abramsky-Haghverdi-Scott 02, def. 2.6](#AbramskyHaghverdiScott02)).

## References

The concept was introduced in

* {#JoyalStreetVerity96} [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. (1996), 119, 447 ([pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf))

A characterization of trace structures on cartesian monoidal categories is given in

* {#Hasegawa97} [[Masahito Hasegawa]], _Recursion from Cyclic Sharing: Traced Monoidal Categories and Models of Cyclic Lambda Calculi_, Proc. 3rd International Conference on Typed Lambda Calculi and Applications (TLCA 1997). Springer LNCS1210, 1997 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.31))

The equivalence between traces and parameterized fixed point operators appears as Theorem 3.1 (the author notes that this theorem was also proved independently by [[Martin Hyland]]).

Comprehensive discussion as a source for [[categorical semantics]] of the [[Geometry of Interactions]] is in 

* {#AbramskyHaghverdiScott02} [[Samson Abramsky]], [[Esfandir Haghverdi]],  [[Philip Scott]], _Geometry of Interaction and Linear Combinatory Algebras_. MSCS, vol. 12(5), 2002, 625-665, CUP (2002) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.24.7818))

The combination with [[star-autonomous category|star-autonomous]] structure was discussed in

* Tamás Hajgató and [[Masahito Hasegawa]], *Traced $\ast$-autonomous categories are compact closed*, [TAC](http://www.tac.mta.ca/tac/volumes/28/7/28-07abs.html), 2013
 {#HH13}


[[!redirects traced monoidal categories]]