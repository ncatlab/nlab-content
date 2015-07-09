
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

The original definition due to ([Joyal-Street-Verity 96](#JoyalStreetVerity96)) is stated in the general setting of [[balanced monoidal categories]].  Here we give just the slightly simpler formulation for the case of symmetric monoidal categories ([Hasegawa 1997](Hasegawa97)).

A [[symmetric monoidal category]] $(C,\otimes,1,b)$ (where $b$ is the symmetry) is said to be **traced** if it is equipped with a natural family of functions

$$Tr_{A,B}^X : C(A \otimes X, B\otimes X) \to C(A,B)$$

satisfying three axioms:

* **Vanishing:** $Tr_{A,B}^1(f) = f$ (for all $f : A \to B$) and $Tr_{A,B}^{X\otimes Y} = Tr_{A,B}^X(Tr_{A\otimes X,B\otimes X}^Y(f))$ (for all $f : A \otimes X \otimes Y \to B \otimes X \otimes Y$)

* **Superposing:** $Tr_{C\otimes A,C\otimes B}^X(id_C \otimes f) = id_C \otimes Tr_{A,B}^X(f)$ (for all $f : A \otimes X \to B \otimes X$)

* **Yanking:** $Tr_{X,X}^X(b_{X,X}) = id_X$

In [[string diagrams]], the trace $Tr(f) : A \to B$ of a morphism $f : A \otimes X \to B \otimes X$ is visualized by wrapping the outgoing wire representing $X$ to the incoming wire representing $X$, thus "tying a loop" in the diagram of $f$.  The three axioms above (as well as the naturality conditions) then all have natural graphical interpretations (see [Joyal-Street-Verity 96](#JoyalStreetVerity96) or [Hasegawa 1997](Hasegawa97)).

## Properties

### Relation to compact closed categories
 {#RelationToCompactClosedCategories}

Given a traced monoidal category $\mathcal{C}$, there is a [[free construction]] completion of it to a [[compact closed category]] $Int(\mathcal{C})$ ([Joyal-Street-Verity 96](#JoyalStreetVerity96)):

the objects of $Int(\mathcal{C})$ are pairs $(A^+, A^-)$ of objects of $\mathcal{C}$, a morphism $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ is given by a morphism of the form $A^+\otimes B^- \longrightarrow A^- \otimes B^+$ in $\mathcal{C}$, and [[composition]] of two such morphisms $(A^+ , A^-) \to (B^+ , B^-)$ and $(B^+ , B^-) \to (C^+ , C^-)$ is given by [[trace|tracing out]] $B^+$ and $B^-$ in the evident way.

### In cartesian monoidal categories

For a [[cartesian monoidal category]], the existence of a trace operator is equivalent to the existence of a "parameterized" [[fixed point]] operator satisfying certain properties ([Hasegawa 1997](Hasegawa97)).

### Categorical semantics

Traced monoidal categories serve as an "operational" [[categorical semantics]] for [[linear logic]], known as _[[Geometry of Interactions]]_. See there for more.

In this context the free compact closure $Int(\mathcal{C})$ from [above](RelationToCompactClosedCategories) is sometimes called the _Geometry of Interaction construction_ and denoted $\mathcal{G}(\mathcal{C})$ ([Abramsky-Haghverdi-Scott 02, def. 2.6](AbramskyHaghverdiScott02)).

## References

The concept was introduced in 

* [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. (1996), 119, 447 ([pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf))
 {#JoyalStreetVerity96}

A characterization of trace structures on cartesian monoidal categories is given in

* [[Masahito Hasegawa]], _Recursion from Cyclic Sharing: Traced Monoidal Categories and Models of Cyclic Lambda Calculi_, Proc. 3rd International Conference on Typed Lambda Calculi and Applications (TLCA 1997). Springer LNCS1210, 1997 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.52.31))
  {#Hasegawa97}

The equivalence between traces and parameterized fixed point operators appears as Theorem 3.1 (the author notes that this theorem was also proved independently by [[Martin Hyland]]).

Comprehensive discussion as a source for [[categorical semantics]] of the [[Geometry of Interactions]] is in 

* [[Samson Abramsky]], [[Esfandir Haghverdi]],  [[Philip Scott]], _Geometry of Interaction and Linear Combinatory Algebras_. MSCS, vol. 12(5), 2002, 625-665, CUP (2002) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.24.7818))
  {#AbramskyHaghverdiScott02}


[[!redirects traced monoidal categories]]