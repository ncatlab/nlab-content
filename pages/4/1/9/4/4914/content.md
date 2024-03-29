
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Internal category theory
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--



# Internal diagrams
* table of contents
{: toc}

## Idea

Given a [[finitely complete category]] $E$, one can consider the [[bicategory]] $Cat(E)$ of [[internal categories]] in $E$, and thus [[internal functors]], which are the morphisms in $Cat(E)$. If $E = Set$ then one can consider not only functors among small categories but also functors of the type $F: C\to Set$ from a small category $C$ to a large category of sets. In that case one can describe $F$ as consisting of a $C_0$-indexed family of objects and an action of $C_1$ on the diagram.

Compare the ideas discussed on this page with those at [[internal profunctor]] and [[discrete fibration]].  All three notions intersect --- an internal diagram on $C$ is the same thing as an internal profunctor $C &#8696; 1$, which is the same thing as a discrete opfibration in $Cat(E)$.  The three generalize the basic idea in different ways.

## Definition

### In category theory

Given an [[internal category]] $C\in Cat(E)$, with the usual structure maps $s,t,i,c$, an **internal [[diagram]]** $F$ on $C$ (or, of type $C$) is given by

* a [[morphism]] $d : F_0\to C_0$ in $E$ together with
* a morphism $e : F_1= F_0\times_{C_0} C_1 \to F_0$

where $F_1$ is the [[pullback]]
\[
\array{
  F_0 \times_{C_0} C_1 & \to & F_0 \\
  \mathllap{s^* d} \downarrow & & \downarrow \mathrlap{d} \\
  C_1 & \underset{s}{\to} & C_0
}
\]
These data must satisfy the following conditions:

* $e$ respects the source and target maps of $C$, in that $d \circ e = t \circ s^* d$.  Equivalently, $e$ is a morphism from $s^* d$ to $t^* d$ in $E/C_1$.

* $e$ is an _action_ in the sense that $e \circ (1 \times i) = 1$ and $e(e \times 1) = e(1 \times c)$.

It is clear how to define [[homomorphisms]] of internal diagrams: a morphism $F \to G$ is given by an $E/C_0$-morphism $F_0 \to G_0$ that commutes with the actions $e$. Internal diagrams on $C$ in $E$ form a category denoted by $E^C$.

An internal diagram on $C^{op}$ is sometimes called an **[[internal presheaf]]** on $C$.

### In dependent type theory

Using the [[dependent type theory|language of]] [[dependent type|dependent types]], the map $d: F_0 \to C_0$ can be seen as the [[categorical semantics|interpretation]] of a dependent type $(X:C_0) \,\vdash\, (F(X):Type)$. The action of $C_1$ on $F_0$ can equivalently be given by the interpretation of a term in [[context]]:

$$ (X:C_0), (Y:C_0), (f:C_1(X,Y)), (a:F(X)) \;\vdash\; (p(X,Y,f,a) : F(Y)). $$

Here we consider $C_1$ to depend on $C_0 \times C_0$ by the canonical morphism $C_1 \to C_0 \times C_0$ induced by $s$ and $t$, as in the [[type-theoretic definition of category]].

If the ambient category $E$ is a [[locally cartesian closed category]], so that its internal type theory has [[dependent product types]], then this can be interpreted instead as a closed term

$$ p : \Pi_{X,Y:C_0} \Pi_{f:C_1(X,Y)} (F(X) \to F(Y)). $$

The axioms then take a particularly familiar form, also to be interpreted in the [[internal language]] of $E$:

* $(X:C_0), (a:F(X)) \;\vdash\; p(X,X,id_X,a) = a $
* $(X,Y,Z:C_0), (f:C_1(X,Y)), (g:C_1(Y,Z)), (a:F(X)) \;\vdash\; p(X,Z,g \circ f,a) = p(Y,Z,g,p(X,Y,f,a))$

## Properties

From an internal diagram $(F,C,\lambda,e)$ one can equip $F =(F_0,F_1)$ with a structure of an internal category over $C$. In other words, there is a forgetful functor $E^C\to Cat(E)/C$ (where $Cat(E)/C$ is the corresponding [[slice category]]). This functor is fully faithful and its essential image consists precisely of all objects in $Cat(E)/C$ which are [[discrete opfibrations]].  Similarly, the objects of $E^{C^{op}}$ are the [[discrete fibrations]] in $Cat(E)/C$.

There is a composite forgetful functor $U \colon E^C \to Cat(E)/C \to E/C_0$.  This functor $U$ is monadic --- its left adjoint takes $p \colon X \to C_0$ to $t \circ s^* p \colon X \times_{C_0} C_1 \to C_1 \to C_0$.

## Diagrams in an indexed category

An internal diagram as above may take values in any [[Grothendieck fibration]] over $E$.  Given a fibration in the guise of an [[indexed category]] $F : E^{op} \to Cat$, a **$C$-diagram in $F$** is given by

* an object $P \in F(C_0)$, together with
* a morphism $\phi : s^* P \to t^* P$ in $F(C_1)$

satisfying 'cocycle equations'

* $i^*\phi = 1_P$
* $c^*\phi = p_1^* \phi \circ p_2^* \phi$

modulo coherent isos, where the $p_i$ are the projections out of $C_2$.

By the [[Yoneda lemma for bicategories]], the object $P$ determines (up to canonical isomorphism) a pseudonatural $\alpha^0 : E(-,C_0) \to F_0$ in $[E^{op},Cat]$, where $E$ is considered as a locally discrete bicategory, and $F_0(X) = ob F X$ considered as a discrete category, such that $\alpha^0(f) \cong f^* P$.  Similarly, $\phi$ determines $\alpha^1 : E(-,C_1) \to F_1 = arr \circ F$, and $\alpha^1(g) \cong g^* \phi$.  It is not hard to check that the conditions above correspond to requiring that the $\alpha^i_X$ form a functor $E(X,C) \to F X$ for each $X$, and pseudonaturality then makes the $C$-diagram $(P,\phi)$ equivalent to an [[indexed functor]] $E(-,C) \to F$.  The category of $C$-diagrams in $F$ is then simply the hom-category $[E^{op},Cat](E(-,C),F)$.

### Examples

* An internal diagram on $C$ in the sense above is a $C$-diagram in the [[codomain fibration]] of $E$, that is the pseudofunctor $X \mapsto E/X$.

* If $E$ is equipped with a [[coverage]] and $C$ is the [[Cech nerve]] associated to a cover $p : U \to X$ in $E$, then the category of $C$-diagrams in $F$ is the [[descent]] category $Des_p(F)$.

## Related concepts

* [[diagram]], [[commuting diagram]], [[free diagram]]

* [[internal presheaf]], [[internal sheaf]]

* [[internal (co-)limit]]

## References

* [[P. T. Johnstone]], _Topos theory_, 1977, chapter 2 

* [[Elephant]], B2.3

[[!redirects internal diagrams]]
