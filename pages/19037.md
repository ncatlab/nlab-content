

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

A comma double category is a generalization of a [[comma category]] to [[double categories]] and [[virtual double categories]].

There are two apparently-maximal levels of generality of this construction, which intersect nontrivially but do not coincide.  The first is an ordinary [[comma object]] in the 2-category of virtual double categories (which includes as a full sub-2-category the 2-category of pseudo double categories and *lax* functors), which produces another virtual double category.  The second is a [[colax/lax comma object]] relative to the 2-monad whose algebras are pseudo double categories.  The two constructions intersect in the case of the comma object of a pseudo double functor over a lax one, between pseudo double categories.

## Definitions

### For virtual double categories ###

For virtual double categories, the comma virtual double category has the universal property of a [[comma object]] in the 2-category of virtual double categories, functors and vertical transformations.

Explicitly, it is constructed as follows. Let $C, D, E$ be virtual double categories and $F : C \to E, G : D \to E$ be functors of virtual double categories. The comma double category $F / G$ is defined as

1. Its vertical category is the ordinary comma category $F_v/G_v$ of the vertical components of the functors. We write an object as $A : F A_C \to G A_D$.
2. A horizontal arrow $R$ from $A$ to $B$ consists of horizontal arrows $R_C : A_C \to B_C$ and $R_D : A_D \to B_D$ and a 2-cell in $E$ from $F R_C$ to $G R_D$ along $A,B$.
3. A 2-cell $\alpha$ from $R_1,\ldots,R_n$ to $S$ consists of a pair of 2-cells $\alpha_C : (R_{1C},\ldots,R_{nC}) \to S_C$ and $\alpha_D : (R_{1D},\ldots,R_{nD}) \to S_D$ such that $G(\alpha_D) \circ (R_1,\ldots,R_n) = S \circ F(\alpha_C)$.

### The oplax/lax case

Let $K = Cat^{\rightrightarrows}$ be the 2-category of [[directed graphs]] [[internalization|internal]] to [[Cat]].  There is a [[2-monad]] $T$ on $K$ whose algebras are (pseudo) double categories, and whose lax and colax morphisms are lax and colax double functors respectively.  The oplax/lax comma double category is then an [[oplax/lax comma object]] for this 2-monad.

## Structures on a virtual comma double category ##

Next, we consider what properties are required of the input data (in the virtual case) to determine that a comma virtual double category has units and composites. An analogy with the double category case gives some guidance. Since functors of virtual double categories correspond to *lax* functors of double categories, we don't have any requirements for the functor $G$ on top of $D$ having composites or units. On the other hand, for $F$ to be "oplax", we require that it be normal for units or furthermore strong for composites.

+-- {: .un_prop} 
###### Proposition

If $C$, $D$ and $E$ have units and $F$ is a normal functor, then $F / G$ has units.
=--

+-- {: .un_prop} 
###### Proposition

If $C$, $D$ and $E$ have composites and $F$ is a strong functor, then $F / G$ has composites.
=--

Next, the comma has restrictions whenever the constituent categories do and the functors preserve them.

+-- {: .un_prop} 
###### Proposition

If $C$, $D$ and $E$ have restrictions and $F,G$ preserve them, then $F / G$ has restrictions.
=--

In practice this proof burden can be reduced if we are interested in virtual equipments (i.e. having units and restrictions) because in that case restrictions are automatically preserved. We summarize this as follows:

+-- {: .un_prop} 
###### Corollary
If $C, D$ and $E$ are [[virtual equipments]] and $F$ is a normal functor, then $F/G$ is a virtual equipment.
=--

## Examples ##

1. A monad $T$ in the horizontal bicategory of a double category $C$ is equivalent to a lax functor $T : 1 \to C$ from the terminal double category. In this case we might call $Id_C / T$ the [[slice double category]].

2. [[generalized multicategories]] can be constructed using a slice category when the monad $T$ is a [[polynomial monad]].  Specifically, let $C$ be the double category of [[polynomial functors]] in some locally cartesian closed category $E$; then a polynomial monad $T$ on $E$ can be identified with a horizontal monad in $C$ on the [[terminal object]] $1$.  The slice $Id_C/T$ is then equivalent to the "horizontal Kleisli category" presented in Cruttwell-Shulman; $T$-multicategories are then monads in that comma double category.

3. The double category of [[decorated cospans]] is naturally constructed as a comma double category. Given a symmetric lax monoidal functor $F : (C,+) \to (D,\otimes)$, there is an associated lax double functor from $F' : Cospan(C) \to BD$ where $BD$ is the [[delooping]] of $D$ into a double category whose horizontal category is $D$ and vertical category is the terminal category. Then there is a colax (pseudo even) double functor $* : 1 \to BD$ that picks out the unique object of $BD$. Then the double category of decorated cospans is $*/F'$.

4. [[poset-valued sets]] given by an endofunctor $F$ on $Rel$ and a poset $P$ can be viewed as the comma double category from $F$ to $P$, since a poset is a monad in $Rel$, and $F$ is a colax endofunctor of $Rel$.  The "morphisms" of poset-valued sets are the *horizontal* morphisms in the resulting comma double category.

5. The [[Dialectica construction]] associated to an internal poset $\Omega$ in a monoidal category $C$ with pullbacks can be obtained as a comma double category.  Let $Span(C)$ be the double category whose horizontal morphisms are spans in $C$, regard $C\times C^{op}$ as a double category in the horizontal direction, and let $F: C\times C^{op} \to Span(C)$ be the colax functor defined on objects by $(A,B) \mapsto A\otimes B$ and taking the pair $(f,g) : (A_1,B_1) \to (A_2,B_2)$ (so that $f:A_1\to A_1$ and $g:B_2\to B_1$) to the span $A_1\otimes B_1 \xleftarrow{1\otimes g} A_1\otimes B_2 \xrightarrow{f\otimes 1} A_2\otimes B_2$.  The internal poset $\Omega$ is a monad in $Span(C)$, so we have a comma double category $F/\Omega$, whose horizontal category is the Dialectica construction $Dial(C,\Omega)$.

6. The [[double gluing]] construction relative to a pair of functors $L:C\to E$ and $K:C\to E^{op}$ can be phrased as a comma double category of the cospan $C \xrightarrow{(L,K)} \mathbb{C}hu(E,1) \leftarrow Chu(E,1)$, where $C$ and $Chu(E,1)$ are regarded as vertically discrete double categories and $\mathbb{C}hu(E,1)$ is the [[double Chu construction]].  To obtain the relevant monoidal structures we can consider this instead to be a comma object in [[double polycategories]].

##References

An explicit description of the comma double category from an oplax to a lax functor is given in 

* [[Kenny Courser]], _A bicategory of decorated cospans_ ([arxiv](https://arxiv.org/abs/1605.08100))




[[!redirects comma double categories]]
[[!redirects comma virtual double category]]
[[!redirects comma virtual double categories]]