
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Whiskering
* table of contents
{: toc}

## Idea

In a [[2-category]], the [[horizontal composition]] of a [[2-morphism]] with [[1-morphisms]] is sometimes called _whiskering_.

Whiskering from the left with an [[equivalence]] and from the right with an inverse equivalence is a [[conjugation]] [[action]] of equivalences on [[2-morphisms]].
 
## Examples

An important use of whiskering is the usual definition of [[adjoint functor]]s via the [[triangle identities]]: in [[Cat]] whiskering is the [[composition]] of a [[functor]] with a [[natural transformation]] to produce a natural transformation.


If we identify a functor or 1-morphism with its [[identity natural transformation]] or [[identity 2-morphism]], then whiskering is a special case of [[horizontal composition]], and composition of 1-morphisms is a special case of whiskering.

In detail:

* If $F,G\colon C \to D$ and $H\colon D\to E$ are functors and $\eta\colon F \to G$ is a natural transformation whose coordinate at any object $A$ of $C$ is $\eta_A$, then __whiskering__ $H$ and $\eta$ yields the natural transformation $H \circ \eta\colon (H \circ F) \to (H \circ G)$ whose coordinate at $A$ is $H(\eta_A)$.
* If $F\colon C \to D$ and $G,H\colon D \to E$ are functors and $\eta\colon G\to H$ is a natural transformation whose coordinate at $A$ is $\eta_A$, then __whiskering__ $\eta$ and $F$ yields the natural transformation $\eta \circ F\colon (G \circ F) \to (H \circ F)$ whose coordinate at $A$ is $\eta_{F(A)}$.

## In dependent type theory

In [[dependent type theory]], whiskering is the type theoretic equivalent of the principle in [[set theory]] that given sets $A$, $B$, and $C$, and functions $f:A \to B$ and $g:A \to B$, if $f(x) = g(x)$ for all elements $x \in A$, then 

* $h(f(x)) = h(g(x))$ for all functions $h:B \to C$ and elements $x \in A$ 
* $f(h(x)) = g(h(x))$ for all functions $h:C \to A$ and elements $x \in C$ 

Given types $A$, $B$, and $C$ and functions $f:A \to B$ and $g:A \to B$ there is a function

$$\mathrm{leftwhiskering}_{A, B, C}(f, g):\left(\prod_{x:A} f(x) =_B g(x)\right) \to \left(\prod_{h:B \to C} \prod_{x:A} h(f(x)) =_C h(g(x))\right)$$

called **left whiskering**, which is defined as the [[lambda abstraction]] of the composite of the [[function application to identities]] of function $h:B \to C$ with [[homotopy]] $H:\prod_{x:A} f(x) =_B g(x)$ 

$$\mathrm{leftwhiskering}_{A, B, C}(f, g)(H, h) \coloneqq \lambda x.\mathrm{ap}_h(H(x))$$

Left whiskering is frequently written simply as $h \circ H$ or $h \cdot H$.

Given types $A$, $B$, and $C$ and functions $f:A \to B$ and $g:A \to B$, there is a function

$$\mathrm{rightwhiskering}_{A, B, C}(f, g):\left(\prod_{x:A} f(x) =_B g(x)\right) \to \left(\prod_{h:C \to A} \prod_{x:C} f(h(x)) =_B g(h(x))\right)$$

called **right whiskering**, defined as the [[lambda abstraction]] of the composite of [[homotopy]] $H:\prod_{x:A} f(x) =_B g(x)$ with function $h:C \to A$ 

$$\mathrm{rightwhiskering}_{A, B, C}(f, g)(H, h) \coloneqq \lambda x.H(h(x))$$

Right whiskering is frequently written simply as $H \circ h$ or $H \cdot h$. 

## Related concepts

* [[pasting diagram]]

* [[digraph|plane digraphs]] 

## References

For whiskering in [[dependent type theory]]:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

For whiskering in [[category theory]]:

* [A MathOverflow question about whiskering](http://mathoverflow.net/questions/40813/what-is-the-name-for-the-composition-of-a-functor-with-a-natural-transformation/40814#40814)

* [[Peter Selinger]]: Introduction to categorical logic. [pdf](https://math.vanderbilt.edu/dept/conf/tacl2013/coursematerials/SelingerTACL20132.pdf), page 41


[[!redirects whiskering]]
[[!redirects whiskerings]]
[[!redirects whisker]]
[[!redirects whiskers]]
[[!redirects whiskered]]
