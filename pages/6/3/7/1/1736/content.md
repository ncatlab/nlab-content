
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[model category]] is a context in which we can do  [[homotopy theory]] or some generalization thereof; two model categories are 'the same' for this purpose if they are Quillen equivalent.  For example, the classic version of homotopy theory can be done using either [[topological space|topological spaces]] or [[simplicial sets]].  There is a model category of topological spaces, and a model category of simplicial sets, and they are Quillen equivalent.

In short, Quillen equivalence is the right notion of [[equivalence]] for [[model category|model categories]] --- and most importantly, this notion is weaker than [[equivalence of categories]].  The work of Dwyer--Kan, Bergner and others has shown that Quillen equivalent model categories [[presentable (infinity,1)-category|present]] equivalent [[(infinity,1)-category|(infinity,1)-categories]].


## Definition

Let $C$ and $D$ be [[model category|model categories]] and let

$$
  (L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}}
   D
$$

be a [[Quillen adjunction]] with $L$ [[left adjoint]] to $R$.

Write $h C$ and $h D$ for the corresponding [[homotopy category|homotopy categories]].

Notice that $h C$ may be regarded as obtained by first passing to the full [[subcategory]] on cofibrant objects and then inverting weak equivalences, and $F$ (being a left Quillen adjoint) preserves weak equivalences between cofibrant objects.  Thus, $L$ induces a functor $\mathbb{L} : h C \to h D$ between the [[homotopy category|homotopy categories]], called its (total) left [[derived functor]].  Similarly (but dually), $R$ induces a (total) right derived functor $\mathbb{R} : h D \to h C$.

The Quillen adjunction $(L \dashv R)$ is a **Quillen equivalence** if the following equivalent conditions are satisfied.

* The total left [[derived functor]] $\mathbb{L} : Ho(C) \to Ho(D)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* The total right [[derived functor]] $\mathbb{R} : Ho(D) \to Ho(C)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* For every cofibrant object $c \in C$ and every fibrant object $d \in D$, a morphism $c \to R(d)$ is a weak equivalence in $C$ precisely when the [[adjunct]] morphism $L(c) \to d$ is a weak equivalence in $D$.

* For every cofibrant object $c\in C$, the composite $c \to R(L(c)) \to R(L(c)^{fib})$ is a weak equivalence in $C$, and for every fibrant object $d\in D$, the composite $L(R(d)^{cof}) \to L(R(d)) \to d$ is a weak equivalence in $D$, where $(-)^{fib}$ and $(-)^{cof}$ denote fibrant and cofibrant [[resolution]]s, respectively.

## Properties

### 2-out-of-3 {#TwoOutOfThree}

Since [[equivalence of categories|equivalences of categories]] enjoy the [[category with weak equivalences|2-out-of-3-property]], so do Quillen equivalences.

### Presentation of equivalence of $(\infty,1)$-categories

[[sSet]]-[[enriched functor|enriched]] Quillen equivalences between [[combinatorial model categories]] present equivalences between the corresponding [[locally presentable (infinity,1)-categories]]. And every equivalence between these is presented by a Zig-Zag of Quillen equivalences. See there for more details.


## Related concepts

* [[Quillen adjunction]]

* [[simplicial Quillen adjunction]]

* **Quillen equivalence**

* [[monoidal Quillen adjunction]]


[[!redirects Quillen equivalences]]
