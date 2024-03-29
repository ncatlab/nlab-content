
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
{:toc}

## Idea

The axioms of a [[category]] ensure that every _finite_ number of composable morphisms has a (unique) [[composite]].

_Transfinite composition_ is a means to talk about morphisms in a category that behave as if they were the result of composing infinitely many morphisms. 



## Definition

Transfinite composition is indexed by [[ordinals]]. For convenience we first recall the definition of these assuming [[excluded middle]] in the ambient [[set theory]] (for definitions not assuming this see at _[[ordinal]]_ and pointers given there):

+-- {: .num_defn #PosetsWosetTosetsAndOrdinals}
###### Definition

A _[[partial order]]_ is a [[set]] $S$ equipped with a [[relation]] $\leq$ such that for all elements $a,b,c \in S$

1) ([[reflexive relation|reflexivity]]) $a \leq a$;

2) ([[transitive relation|transitivity]]) if $a \leq b$ and $b \leq c$ then $a \leq c$;

3) ([[antisymmetric relation|antisymmetry]]) if a $a\leq b$ and $\b \leq a$ then $a = b$. 

This we may and will equivalently think of as a [[category]] with [[objects]] the elements of $S$ and a unique morphism $a \to b$ precisely if $a\leq b$. In particular an order-preserving function between partially ordered sets is equivalently a [[functor]] between their corresponding categories.

A _[[bottom element]]_ $\bot$ in a partial order is one such that $\bot \leq a$ for all a. A _[[top element]]_ $\top$ is one for wich $a \leq \top$.

A partial order is a _[[total order]]_ if in addition

4) ([[total relation|totality]]) either $a\leq b$ or $b \leq a$.

A total order is a _[[well order]]_ if in addition

5) ([[well-founded relation|well-foundedness]]) every non-empty subset has a least element.

An _[[ordinal]]_ is the [[equivalence class]] of a well-order. 

The _[[successor]]_ of an ordinal is the class of the well-order with a [[top element]] freely adjoined.

A _[[limit ordinal]]_ is one that is not a successor.

=--

+-- {: .num_example}
###### Examples

The finite ordinals are labeled by $n \in \mathbb{N}$, corresponding to the well-orders $\{0 \leq 1 \leq 2 \cdots \leq n-1\}$. Here $(n+1)$ is the successor of $n$. The first non-empty limit ordinal is $\omega = [(\mathbb{N}, \leq)]$.


=--

+-- {: .num_defn #TransfiniteComposition}
###### Definition


Let $\mathcal{C}$ be a [[category]], and let $I \subset Mor(\mathcal{C})$ be a [[class]] of its morphisms. 

For $\alpha$ an [[ordinal]] (regarded as a [[category]]), an $\alpha$-indexed _transfinite sequence_ of elements in $I$ is a [[diagram]]

$$
  X_\bullet 
    \;\colon\; 
  \alpha \longrightarrow \mathcal{C}
$$

such that 

1. $X_\bullet$ takes all [[successor]] morphisms $\beta \stackrel{\leq}{\to} \beta + 1$ in $\alpha$ to elements in $I$

   $$
     X_{\beta,\beta + 1} \in I
   $$

1. $X_\bullet$ is _continuous_ in that for every nonzero [[limit ordinal]] $\beta \lt \alpha$, $X_\bullet$ restricted to the [[full subcategory|full-subdiagram]] $\{\gamma \;|\; \gamma \leq \beta\}$ is a [[colimit|colimiting cocone]] in $\mathcal{C}$ for $X_\bullet$ restricted to $\{\gamma \;|\; \gamma \lt \beta\}$:

   $$
     X_\beta \simeq \underset{\longrightarrow}{\lim}_{\gamma \lt \beta} X_\gamma
     \,. 
   $$

The corresponding **transfinite composition** is the induced morphism

$$
  X_0 \longrightarrow X_\alpha \coloneqq \underset{\longrightarrow}{\lim}X_\bullet
$$

into the [[colimit]] of the diagram, schematically:

$$
  \array{
    X_0 &\stackrel{X_{0,1}}{\to}& X_1
    &\stackrel{X_{1,2}}{\to}& X_2
    &\to& \cdots
    \\
    & \searrow & \downarrow & \swarrow & \cdots 
    \\
    &&
    X_\alpha
  }  
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For purposes of [[constructive mathematics]], the continuity condition should be stated as follows:

* For *every* ordinal $\beta \lt \alpha$, $X_\bullet$ restricted to $\{\gamma \;|\; \gamma \leq \beta\}$ is a colimiting cone in $\mathcal{C}$ for the disjoint union of $\{X_0\}$ and the restriction of $X_{\bullet}$ to $\{\gamma + 1 \;|\; \gamma \lt \beta\}$.

This actually includes $F(0) = X$ as a special case but says nothing when $\beta$ is a successor (so the successor clause is still required).

=--

## Applications

Transfinite composition plays a role in

* the [[small object argument]];

* [[cofibrantly generated model category|cofibrantly generated model categories]].

* the [[transfinite construction of free algebras]]


## Related concepts

* [[transfinite induction]]

## References

For instance 

* [[Tibor Beke]], page 6  of _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))


[[!redirects transfinite composite]]
[[!redirects transfinite composites]]
[[!redirects transfinite composition]]
[[!redirects transfinite compositions]]