
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
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

### In simplicial type theory

We work in [[simplicial type theory]] with a [[directed interval]] $\mathbb{I}$. 
Let the 2-simplex type be defined as 

$$\Delta^2 \coloneqq \sum_{s:\mathbb{I}} \sum_{t:\mathbb{I}} s \leq t$$

and let the (2,1)-[[horn]] type be defined as 

$$\Lambda_1^2 \coloneqq \sum_{s:\mathbb{2}} \sum_{t:\mathbb{2}} (s =_\mathbb{I} 0) \vee (t =_\mathbb{I} 1)$$

where $P \vee Q$ is the [[disjunction]] of the types $P$ and $Q$. Since $s \leq t$ implies $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$ for all $s:\mathbb{I}$ and $t:\mathbb{I}$, we have a canonical function 

$$(\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):\Delta^2 \to \Lambda^2_1$$

which is a tuple consisting of two copies of the [[identity function]] on $\mathbb{I}$ and a [[dependent function]] $P$ that takes the witness that $s \leq t$ to a witness that $(s =_{\mathbb{I}} 0) \vee (t =_{\mathbb{I}} 1)$. By precomposition, this leads to a function 

$$\lambda u.u \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P):(\Delta^2 \to A) \to (\Lambda^2_1 \to A)$$

for all types $A$. 

Let $h_{0,2}:\mathbb{I} \to \Delta^2$ be the [[face map]] which represents the unique morphism from $0$ to $2$ in the 2-simplex. 

\begin{definition}
A morphism $f:\mathbb{I} \to A$ is the **composite** of a [[composable pair of morphisms]] $k:\Lambda^2_1 \to A$ if one can construct a [[commutative triangle]] $h:\Delta^2 \to A$ such that 

$$h \circ (\lambda t:\mathbb{I}.t, \lambda t:\mathbb{I}.t, P) = k \; \mathrm{and} \; h \circ h_{0,2} = f$$
\end{definition}

In a [[Segal type]] $A$, for all elements $x:A$, $y:A$, and $z:A$, all composites are [[unique composites]] by definition of the [[Segal condition]], and thus one can construct a [[composition]] operation on [[hom-types]] 

$$\lambda (g, f).g \circ f:\mathrm{hom}_A(y, z) \times \mathrm{hom}_A(x, y) \to \mathrm{hom}_A(x, z)$$

which by the Segal condition is automatically [[associative]] and [[unital]]. 

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

* [[composable pair]] 

* [[commutative triangle]]

* [[unique composite]]

* [[hom set]], [[hom type]]

* [[span in simplicial type theory]]

* [[cospan in simplicial type theory]]

## References

* {#RS17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* [[Emily Riehl]], *[Could $\infty$-category theory be taught to undergraduates?](https://www.ams.org/journals/notices/202305/noti2692/noti2692.html?adat=May%202023&trk=2692&galt=feature&cat=feature&pdfissue=202305&pdffile=rnoti-p727.pdf)*, Notices of the AMS (May 2023) &lbrack;[published pdf](https://www.ams.org/journals/notices/202305/rnoti-p727.pdf), [arxiv:2302.07855](https://arxiv.org/abs/2302.07855)&rbrack;

The phrase "composite" appears in:

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.5.1 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

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

[[!redirects composition of morphisms]]

[[!redirects composite of morphisms]]
[[!redirects composites of morphisms]]

[[!redirects type of composites]]
[[!redirects types of composites]]

[[!redirects type of composite of morphisms]]
[[!redirects types of composites of morphisms]]

[[!redirects composition in simplicial type theory]]

[[!redirects composition of morphisms in simplicial type theory]]

[[!redirects composite of morphisms in simplicial type theory]]
[[!redirects composites of morphisms in simplicial type theory]]

[[!redirects type of composite of morphisms in simplicial type theory]]
[[!redirects types of composites of morphisms in simplicial type theory]]