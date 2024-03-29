
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _functional calculus_ or _function calculus_ are operations by which for $f$ a [[function]] (on the [[complex number]]s , for instance) and $a$ a suitable [[linear operator]] (on a [[Hilbert space]], for instance) one makes sense of the expression $f(a)$ as a new operator. Usually one requires that the assignment $f \mapsto f(a)$ is an algebra [[homomorphism]], but not always, namely in some contexts as [[quantization]] the ordering effects may not respect the homomorphism property, see [[Weyl functional calculus]]. 

## Statements

Let $A$ be a [[C-star algebra]] (possibly non-commutative) and $a \in A$ a [[normal operator]]. With $sp(a)$ the [[operator spectrum]] of $a$ write $C(sp(a))$ for the commutative $C^\ast$-algebra of continuous complex-valued functions on $sp(a)$. Finally write $\iota : \in C(sp(A))$ for the function $\iota : x \mapsto x$.


+-- {: .num_theorem}
###### Theorem

There is a unique [[star-algebra]] [[homomorphism]]

$$
  \phi_a : C(sp(a)) \to A
$$

such that $\phi(\iota) = a$. 

For all $f \in C(sp(a))$ we have that $\phi(f) \in A$ is a [[normal operator]].

=--

This appears for instance as ([KadisonRingrose, theorem 4.4.5](#KadisonRingrose)).

+-- {: .proof}
###### Proof

Let $\langle a \rangle \subset A$ be the $C^\ast$-algebra generated by $a$, or in fact any commutative $C^\ast$-subalgebra of $A$ containing $a$.

Then by [[Gelfand duality]] there is a [[compact topological space]] $X$ and an [[isomorphism]] $\psi : \langle a \rangle \stackrel{\simeq}{\to} C(X)$. 

Define a morphism

$$
  (-) \circ \psi(a) :  C(sp(a)) \to C(X)
$$

by $f \mapsto f \circ \psi(a)$. This is a [[continuous map|continuous]] $\ast$-algebra homomorphism. Therefore so is the composite

$$
  \phi
   :
  C(sp(a)) \stackrel{(-)\circ \psi(a)}{\to}
  C(X)
  \stackrel{\psi^{-1}}{\to}
  \langle a\rangle
  \hookrightarrow
  A
  \,.
$$

And this satisfies $\phi(\iota) = \psi^{-1}(\iota \circ \psi(a)) = \psi^{-1}\psi (a) = a$.

This establishes the existence of $\phi$. To see uniqueness, notice that any other morphism with these properties coincides with $\phi$ on all [[polynomial]]s in $\iota$ and $\bar \iota$. By the [[Stone-Weierstrass theorem]] such polynomials form an everywhere-[[dense subset]] of $C(sp(a))$. Since moreover one can see that the two morphisms must be isometric (...) it follows that they in fact agree.
 
=--


## References

A standard textbook is for instance

* Richard Kadison, John Ringrose, _Fundamentals of the theory of operator algebra_ , Academic Press (1983)
 {#KadisonRingrose}

See also

* [[eom]], _[Functional calculus](http://eom.springer.de/F/f042030.htm)_

* [[Planet Math]], _[Borel functional calculus](http://planetmath.org/encyclopedia/BorelFunctionalCalculus.html)_