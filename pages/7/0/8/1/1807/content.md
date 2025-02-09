
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

There are many related constructions of algebras, topological algebras and so on which bear the name of a _convolution algebra_. 

The basic mechanism is usually the 

* [Convolution of maps from a coalgebra to an algebra](#ConvolutionOfMapsFromACoalgebraToAnAlgebra) .

The probably most widespread example of this is the

* [Convolution algebra of a group](#OfAGroup)

This is a special case of the

* [Convolution algebra of a groupoid/category](#OfAGroupoid)

### Of maps from a coalgebra to an algebra
 {#ConvolutionOfMapsFromACoalgebraToAnAlgebra}

Let $k$ be a commutative unital [[ring]], $(C,\Delta)$ a (counital) $k$-[[coalgebra]] and $(A,m)$ an associative (unital) $k$-[[associative unital algebra|algebra]]. Then the set of linear maps
$$
\mathrm{Hom}_k(C,A)
$$
has a structure of an associative (unital) algebra, called __convolution algebra__, in which the product of two linear maps $f,g$ is given by
$$f\star g = m\circ(f\otimes g)\circ\Delta. $$

### Of maps from a comonoid to a monoid in a closed monoidal category

\begin{proposition}
Let $(\mathcal{C}, \otimes, I, \multimap)$ be a [[closed monoidal category]],  $(A,\Delta,\eta)$ a [[comonoid]] in $\mathcal{C}$ and $(B,\nabla,\epsilon)$ a [[monoid]]. Then  $A \multimap B$ is a monoid.
\end{proposition}

\begin{proposition}
Let $(\mathcal{C}, \otimes, I, \multimap)$ be a [[closed monoidal category]], $Mon(\mathcal{C})$ the [[category of monoids]] of $\mathcal{C}$ and $Comon(\mathcal{C})$ the category of comonoids of $\mathcal{C}$. We then have a functor:
$$
Comon(\mathcal{C})^{op} \times Mon(\mathcal{C}) \rightarrow Mon(\mathcal{C})
$$
which associate $A \multimap B$ to $(A,B)$
\end{proposition}

### Of a group
 {#OfAGroup}

Given a [[finite group]] $G$ and a [[ring]] $R$, the space of [[functions]] $C(G,R)$ inherits the _convolution product_ defined by

$$
  f_1 \star f_2 
    \;\;\colon\;\; 
  g 
    \;\mapsto\;
  \sum_{g_1 \cdot g_2 = g} 
    f_1(g_1) \cdot f_2(g_2)
  \,.
$$

This is the non-commutative product operation that appears in the [[Hopf algebra]] structure on $C(G,R)$.


### Of a groupoid/category
 {#OfAGroupoid}

More generally, there is convolution of functions on morphisms of a [[groupoid]]. See at _[[groupoid convolution algebra]]_ for details.


[[!redirects convolution algebras]]
