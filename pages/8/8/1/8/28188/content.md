
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

**Intersection types** are a way to add finite [[polymorphism]]
to the [simply typed](lambda-calculus#SimplyTypedLambdaCalculus) [[λ-calculus]].
For example, the [[judgment]] $\Gamma \vdash e \colon \tau \land \sigma$ means that $e$ has _both_ types $\tau$ and $\sigma$.

Intersection types (without a universal type $\omega$) capture exactly the strongly-normalizing terms of the λ-calculus.
For example the value $\lambda x. x \, x$
can be typed using the following judgment:
$x : (\sigma \to \sigma) \land \sigma \vdash x\,x : \sigma$.
However, [[type inference]] for intersection type systems is [[undecidable]].

## Typing rules

In most intersection type systems, we can derive a [[inference rule|rule]] for [[function type|function]] [[term elimination|elimination]] similar to:
\[
  \frac{
    \Gamma \vdash f \colon 
    \bigwedge_{i \in I}(A_i \to B_i)
    \qquad 
    \Gamma \vdash x : A
  }{
    \Gamma \vdash f \, x \colon 
    \bigwedge_{k \in I, A \leq A_k} B_k
  }
\]

## Non-idempotent intersection types

In the majority of intersection type systems,
$\land$ is [[associativity|associative]], [[commutativity|commutative]] and [[idempotent]].
However, $\land$ can also be seen as the non-idempotent
[[multiplicative conjunction]] from [[linear logic]].

## Related concepts

* [[polymorphism]]

* [[union types]]

## References

* M. Coppo, M. Dezani-Ciancaglini: _A new type assignment for lambda-terms_, Archive for Mathematical Logic **19** (1978) 139–156 &lbrack;[doi:10.1007/BF02011875](https://doi.org/10.1007/BF02011875)&rbrack;

* M. Coppo, M. Dezani-Ciancaglini: _An extension of the basic functionality theory for the λ-calculus_, Notre Dame Journal of Formal Logic **4** (1980) 685–693 &lbrack;[doi:10.1305/ndjfl/1093883253](http://doi.org/10.1305/ndjfl/1093883253), [pdf](https://projecteuclid.org/journals/notre-dame-journal-of-formal-logic/volume-21/issue-4/An-extension-of-the-basic-functionality-theory-for-the-lambda/10.1305/ndjfl/1093883253.pdf)&rbrack;

[[!redirects intersection types]]

