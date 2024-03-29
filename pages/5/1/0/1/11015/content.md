
This page collects links related to the article

* [[William Lawvere]]:

  \linebreak

  **Unity and Identity of Opposites in Calculus and Physics**

  \linebreak 

  Proceedings of ECCT 1994 Tours Conference, 

  Applied Categorical Structures **4** 167-174 (1996)

  Kluwer Academic Publishers

  [doi:10.1007/BF00122250](https://doi.org/10.1007/BF00122250)

  [github](https://github.com/mattearnshaw/lawvere/blob/master/pdfs/1996-unity-and-identity-of-opposites-in-calculus-and-physics.pdf)

on the formalization of [[unity of opposites]] in [[calculus]] and [[physics]]. 

{#WhatItIsAbout} Section II re-casts the statement of the *[[Hadamard lemma]]* via the three homomorphisms of [[rings]] of [[smooth functions]] on a [[smooth manifold]] $X$ and its [[product manifold]] $X \times X$ (the article generalizes this to [[fiber products]] but that's not necessary to appreciate the idea):

\begin{tikzcd}[column sep=20pt]
  C^\infty(X \times X)
  \ar[
    from=rr,
    shift left=14pt,
    "{
      \mathrm{pr}_1^\ast
    }"{description}
  ]
  \ar[
    rr,
    "{
      \mathrm{diag}^\ast
    }"{description}
  ]
  \ar[
    from=rr,
    shift right=14pt,
    "{
      \mathrm{pr}_2^\ast
    }"{description}
  ]
  &&
  C^\infty(X)
  \mathrlap{\,,}
\end{tikzcd}

where $pr_i \,\colon\, X \times X \xrightarrow{\;} X$ are the two [[projections]] out of the [[Cartesian product]] and $diag \,\colon\, X \xrightarrow{\;} X \times X$ denotes the [[diagonal map]]. So: 

* for $f \,\in\, C^\infty(X)$ we have

  $$
    pr_1^\ast(f) \,\colon\, (x_1, x_2) \,\mapsto\, f(x_1)
    ,\,
    \;\;\;\;
    pr_2^\ast(f) \,\colon\, (x_1, x_2) \,\mapsto\, f(x_2)
  $$

* for $g \,\in\, C^\infty(X \times X)$ we have

  $$
    diag^\ast(g) \,\colon\, x \,\mapsto\, g(x,x)
    \,.
  $$

These are the expressions that enter the formulation of the [[Hadamard lemma]] ([here](Hadamard+lemma#HadamardLemma)) and its corollary ([here](Hadamard+lemma#AndItsCorollary)).

Compare this to the discussion at *[[adjoint cylinder]]* and then to *[[objective and subjective logic]]* and maybe also *[[Aufhebung]]*.

### Abstract

> A significant fraction of dialectical philosophy can be modeled mathematically through the use of "[[adjoint cylinder|cylinders]]" (diagrams of shape $\Delta_1$) in a category, wherein the two identical [[subobjects]] (united by the third map in the diagram) are "opposite". In a [[bicategory]], oppositeness can be very effectively characterized in terms of [[adjunction|adjointness]], but even in an ordinary category it may sometimes be given a useful definition. For example, an effective basis for teaching calculus is a ringed category satisfying the Hadamard-Marx property. The description in engineering mechanics of continuous bodies that can undergo cracking is clarified by an example involving lattices, raising a new questions about the foundations of topology. 

> ($\Delta_1$ is the category of order-preserving maps between totally-ordered sets of one and two elements, respectively.)

category: reference