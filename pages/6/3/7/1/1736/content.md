<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A [[model category]] is a context in which we can do  [[homotopy theory]] or some generalization thereof; two model categories are 'the same' for this purpose if they are Quillen equivalent.  For example, the classic version of homotopy theory can be done using either [[topological space|topological spaces]] or [[simplicial sets]].  There is a model category of topological spaces, and a model category of simplicial sets, and they are Quillen equivalent.

In short, Quillen equivalence is the right notion of [[equivalence]] for [[model category|model categories]] --- and most importantly, this notion is weaker than [[equivalence of categories]].  The work of Dwyer--Kan, Bergner and others has shown that Quillen equivalent model categories [[presentable (infinity,1)-category|present]] equivalent [[(infinity,1)-category|(infinity,1)-categories]].

#Definition#

Let $C$ and $D$ be [[model category|model categories]] and let

$$
  D \stackrel{G}{\to} C
$$
$$
  D \stackrel{F}{\leftarrow} C
$$
be a [[Quillen adjunction]] with $F$ [[left adjoint]] to $G$.

Write $h C$ and $h D$ for the corresponding [[homotopy category|homotopy categories]].

Notice that $h C$ may be regarded as obtained by first passing to the full [[subcategory]] on cofibrant objects and then inverting weak equivalences, and $F$ (being a left Quillen adjoint) preserves weak equivalences between cofibrant objects.  Thus, $F$ induces a functor $L F : h C \to h D$ between the [[homotopy category|homotopy categories]], called its (total) left [[derived functor]].  Similarly (but dually), $G$ induces a (total) right derived functor $R G : h D \to h C$.

The Quillen adjunction $(F,G)$ is a **Quillen equivalence** if the following equivalent conditions are satisfied.

* The total left [[derived functor]] $L F : Ho(C) \to Ho(D)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* The total right [[derived functor]] $R G : Ho(D) \to Ho(C)$ is an [[equivalence of categories|equivalence]] of the [[homotopy categories]];

* For every cofibrant object $c \in C$ and every fibrant object $d \in D$, a morphism $c \to G(d)$ is a weak equivalence in $C$ precisely when the [[adjunct]] morphism $F(c) \to d$ is a weak equivalence in $D$.

* For every cofibrant object $c\in C$, the composite $c \to G(F(c)) \to G(F(c)^{fib})$ is a weak equivalence in $C$, and for every fibrant object $d\in D$, the composite $F(G(d)^{cof}) \to F(G(d)) \to d$ is a weak equivalence in $D$, where $(-)^{fib}$ and $(-)^{cof}$ denote fibrant and cofibrant replacement, respectively.

[[!redirects Quillen equivalences]]
