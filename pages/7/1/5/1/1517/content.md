
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A _coalgebra over an endofunctor_ is like a [[coalgebra over a comonad]], but without a notion of [[associativity]].

The concept plays a role in [[computer science]] for models of state-based [[computation]] (see also [[monad (in computer science)]]).
The concept of the [[terminal coalgebra of an endofunctor]] is a way of encoding [[coinductive types]].

## Definition

+-- {: .num_defn}
###### Definition

For a [[category]] $C$ and [[endofunctor]] $F$, a **[[coalgebra]] of** $F$ is an [[object]] $X$ in $C$ together with a [[morphism]] $\alpha: X \to F(X)$. 

Given two coalgebras $(x, \eta: x \to F x)$, $(y, \theta: y \to F y)$, a coalgebra [[homomorphism]] is a [[morphism]] $f: x \to y$ which respects the coalgebra structures: 

$$\theta \circ f = F(f) \circ \eta$$

=--

(The object $X$ is sometimes called the __carrier__ of the coalgebra.)

+-- {: .num_remark}
###### Remark

The dual concept is an [[algebra for an endofunctor]]. Both [[algebras]] and coalgebras for endofunctors on $C$ are special cases of [[algebra for a C-C bimodule|algebras for C-C bimodules]].

=--

+-- {: .num_remark}
###### Remark

If $F$ is equipped with the structure of a [[monad]], then a coalgebra for it is equivalently an [[endomorphism]] in the corresponding [[Kleisli category]]. In this case the canonical [[monoidal category]] structure on endomorphisms induces a [[tensor product]] on those coalgebras.

=--


## Examples 

### Coalgebras for endofunctors on $Set$

Each of the following examples is of the form $X\to F(X)$, (description of endofunctor $F\colon Set\to Set$) : (description of coalgebra). Where it appears, $A$ is a given fixed set.

* $X \to D(X)$, the set of [[probability distributions]] on $X$: Markov chain on $X$.
* $X \to \mathcal{P}(X)$, the [[power set]] of $X$: binary relation on $X$, and also the simplest type of [[Kripke frames]].
* $X \to X^A \times bool$, with $X^A$ the set of functions $A\to X$ and $bool = \{0,1\}$: [[deterministic automaton]].
* $X \to \mathcal{P}(X)^A\times bool$: [[nondeterministic automaton]].
* $X \to A \times X \times X$: labelled binary tree with labels from $A$.
* $X \to \mathcal{P}(A\times X)$: [[transition system|labelled transition system]] with labels from $A$.


See [[coalgebra]] for examples on categories of modules.


### The real line as a terminal coalgebra
 {#RealLine}

Let $Pos$ be the category of [[poset]]s. Consider the endofunctor

$$
  F_1 : Pos \to Pos
$$

that acts by [[ordinal product]] with $\omega$

$$
  F_1 : X \mapsto X \cdot \omega
  \,,
$$

where the right side is given the dictionary order, not the usual product order. 

+-- {: .un_prop}
###### Proposition

The terminal coalgebra of $F_1$ is order isomorphic to the non-negative [[real line]] $\mathbb{R}^+$, with its standard order.
=--

+-- {: .proof}
###### Proof
This is theorem 5.1 in

* D. Pavlovic, [[Vaughan Pratt]], _On coalgebra of real numbers_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.47.5204))
=--


+-- {: .un_prop}
###### Proposition

The real interval $[0, 1]$ may be characterized, as a [[topological space]], as the terminal coalgebra for the functor on two-[[pointed object|pointed]] topological spaces which takes a space $X$ to the space $X \vee X$. Here, $X \vee Y$, for $(X, x_-, x_+)$ and $(Y, y_-, y_+)$, is the disjoint union of $X$ and $Y$ with $x_+$ and $y_-$ identified, and $x_-$ and $y_+$ as the two base points.
=--

+-- {: .proof}
###### Proof

This is discussed in 

* [[Peter Freyd]], [cat list](http://www.mta.ca/~cat-dist/catlist/1999/realcoalg)

More information may be found at [[coalgebra of the real interval]]. 
=--


## Related concepts

* [[list of notable initial algebras and terminal coalgebras]]

* [[well-founded coalgebra]]

* [[algebra over a monad]], [[algebra over an endofunctor]], [[algebra over a profunctor]]


## References

* [[Michael Barr]], *Terminal coalgebras for endofunctors on sets*,  Theoretical Comp. Sci. **114** (1993) 299–315 &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/trmclg.pdf), [[Barr-TerminalCoalgebras.pdf:file]]&rbrack;

* {#Pattinson03} [[Dirk Pattinson]], *An Introduction to the Theory of Coalgebras* (2003) &lbrack;[pdf](https://nasslli.sitehost.iu.edu/2003/datas/DirkPattinson.pdf), [[Pattinson-Coalgebras.pdf:file]]&rbrack;

* [[Jiri Adamek]], *Introduction to coalgebras*, Theory and Applications of Categories **14** 8 (2005) 157-199 &lbrack;[tac:14-08](http://www.tac.mta.ca/tac/volumes/14/8/14-08abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/14/8/14-08.pdf)&rbrack;



There are connections between the theory of coalgebras and [[modal logic]]  for which see

* [[Bart Jacobs]], _Introduction to Coalgebra. Towards Mathematics of States and Observations_ ([book pdf](http://www.cs.ru.nl/B.Jacobs/CLG/JacobsCoalgebraIntro.pdf), [slides](http://cs.ioc.ee/ewscs/2011/jacobs/jacobs-slides.pdf))

and also 

* Corina Cırstea, Alexander Kurz, [[Dirk Pattinson]], Lutz Schroder and Yde Venema, _Modal Logics are Coalgebraic_, from the Computer Journal 2011, [here](http://users.cecs.anu.edu.au/~dpattinson/Publications/cj2011.pdf).

and with [[quantum mechanics]], for which see this and

* [[Samson Abramsky]], _Coalgebras, Chu Spaces, and Representations of Physical Systems_ ([arXiv:0910.3959](http://arxiv.org/abs/0910.3959))


Here are two blog discussions of coalgebra theory:

* [[David Corfield]], _[_Coalgebraically Thinking_](http://golem.ph.utexas.edu/category/2008/11/coalgebraically_thinking.html)_

* [[David Corfield]], _[_The Status of Coalgebra_](http://golem.ph.utexas.edu/category/2008/12/the_status_of_coalgebra.html)_


[[!redirects coalgebra of an endofunctor]]
[[!redirects coalgebras of an endofunctor]]
[[!redirects coalgebras of endofunctosr]]
[[!redirects coalgebra for an endofunctor]]
[[!redirects coalgebras for an endofunctor]]
[[!redirects coalgebras for endofunctors]]
[[!redirects coalgebra over an endofunctor]]
[[!redirects coalgebras over an endofunctor]]
[[!redirects coalgebras over endofunctors]]