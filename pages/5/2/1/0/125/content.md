
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

### In a plain category

__Composition__ is the operation that takes [[morphism|morphisms]] $f\colon  x \to y$ and $g\colon  y \to z$ in a [[category]] and produces a morphism $g \circ f\colon  x \to z$, called the __composite__ of $f$ and $g$.

Note that this composition is unique by the axioms of category theory. If we instead work in a weak [[higher category]], composition need not be unique. In this sense we may identify the composite of $f$ and $g$ with the colimit over the diagram $a\stackrel{f}{\to}b\stackrel{g}{\to}c$. This point of view is taken and generalized in [[transfinite composition]].

### In an enriched category

In [[enriched category theory]], for $V$ a [[monoidal category]] the composition operation on a $V$-[[enriched category]] $C$ is for each triple $(x,y,z)$ of [[object]]s of $C$ a [[morphism]]

$$
  \circ_{x,y,z} : C(x,y) \otimes C(y,z) \to C(x,z)
$$


in $V$.

This reduces to the above definition in the case that $V =$ [[Set]]. The composition morphism $\circ_{x,y,z}$ sends any two composable morphisms to their composite.

$$
  \circ_{x,y,z} : ((x \stackrel{f}{\to} y), (y \stackrel{g}{\to} z))
  \;\; \mapsto \;\; (x \stackrel{g\circ f}{\to} z)
  \,.
$$

### For internal homs

Let $(\mathcal{C}, \otimes)$ be a [[closed monoidal category]]. Write $[-,-] : \mathcal{C}^{op}\times \mathcal{C} \to \mathcal{C}$ for the corresponding [[internal hom]].

+-- {: .num_defn #CompositionMorphism}
###### Definition

For $X, Y, Z \in \mathcal{C}$ three [[objects]], the 
**composition morphism**

$$
  \circ_{X,Y,Z} : 
  [Y, Z]
  \times
  [X, Y]
  \to 
  [X, Z]
$$

is the $((-)\otimes X \dashv [X,-])$-[[adjunct]] of the following composite of two [[evaluation maps]], def. \ref{EvalMap}:

$$
  [Y, Z] \times [X , Y] \times X 
    \stackrel{(id_{[Y,Z]}, eval_{X,Y})}{\to}
  [Y,Z] \times Y
    \stackrel{eval_{Y,Z}}{\to}
  Z
  \,.
$$

=--


## Higher arity

Strictly speaking, composition as defined above is *binary* composition.  One can also define $n$-ary composites for any [[natural number]] $n \geq 0$: given $n + 1$ objects $x_0, \ldots, x_n$ and $n$ morphisms $f_i\colon x_{i-1} \to x_i$, we get the composite $f_n \circ \dots \circ f_1\colon x_0 \to x_n$.  Since composition in a category is associative, a definition of $n$-ary composition from binary composition via any choice of bracketing will be equal to that resulting from any other choice of bracketing.  The unary composite of $f_1\colon x_0\to x_1$ is simply $f$ itself, and the nullary composite of $x_0$ is its [[identity morphism]].

Conversely, a category can equivalently be defined as a [[quiver]] (a [[directed graph]]) equipped with an $n$-ary composition operation for every [[natural number]] $n\ge 0$, satisfying suitable associativity axioms.  This definition may be called *unbiased*, as opposed to the usual definition which is "biased" towards $0$ and $2$.

## Categorical semantics

In the context of [[formal logic]], composition is the [[categorical semantics]] for the [[cut rule]].


## Notation 
 {#Notation}

Traditionally, the composite of $f$ and $g$ as above is written $g \circ f$, following the notation introduced by the followers of Leibniz for composition of [[functions]].  This is often abbreviated as simply $g f$.  Of course, this notation preserves the order of symbols in the elementwise definition of function composition: $(g\circ f)(x) = g(f(x))$.

On the other hand, reading a diagram
$$ x \stackrel{f}\to y \stackrel{g}\to z $$
the notation $f g$ reads better.  One way to make this anti-Leibniz convention clearer is to write $f ; g$ (which is based on the interpretation of programming commands as morphisms in theoretical computer science).  Since this convention is motivated by the drawing of diagrams, it is also sometimes called **diagrammatic order**. Another way is to write $f^* g$, which interprets $g$ as pulling back along $f$ to the composite.

Therefore, the notations $g f$ and $f g$ are ambiguous, while $g \circ f$ and $f ; g$ are less so.  It seems that the notation $g f$ for $g\circ f$ is more common than $f g$ for $f ; g$, although the $f g$ notation occurs in some important older papers.

Although diagrammatic order has advantages and partisans, especially among category theorists and computer scientists, the "classical" order of composition is firmly entrenched in much of mathematics.  Many people who agree that diagrammatic order is "better" on its own merits nevertheless believe that trying to change the established "classical" order of composition creates more confusion than it removes.

In some older category theory papers, arrows were written pointing from right to left, so that the composition of arrows could be written in the "classical" style, while still preserving the diagrammatic intuition. Hom-sets were accordingly written $C(b,a)$, where $a$ is the [[source]], and $b$ is the [[target]].  This sort of convention has also been used by people working with [[string diagrams]] and [[surface diagram]]s.

## Related concepts

* [[operator product]]

* [[concatenation]]

* [[composition ring]]


[[!redirects composite]]
[[!redirects composites]]

[[!redirects composition]]
[[!redirects compositions]]
[[!redirects compose]]

[[!redirects precomposition]]
[[!redirects precompositions]]

[[!redirects postcomposition]]
[[!redirects postcompositions]]

[[!redirects diagrammatic order]]
