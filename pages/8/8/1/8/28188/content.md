\tableofcontents

## Idea

**Intersection types** are a way to add finite [[polymorphism]]
to the [[simple type|simply typed]] [[λ-calculus]].
For example, the judgment $\Gamma \vdash e : \tau \land \sigma$
means that $e$ has _both_ types $\tau$ and $\sigma$.

Intersection types (without a universal type $\omega$) capture exactly the strongly-normalizing terms
of the λ-calculus.
For example the value $\lambda x. x \, x$
can be typed using the following judgment:
$x : (\sigma \to \sigma) \land \sigma \vdash x\,x : \sigma$.
However, [[type inference]] for intersection type systems is [[undecidable]].

## Typing rules

In most intersection type systems, we can derive a rule
for function elimination similar to:
\[
  \frac{
    \Gamma \vdash f:\bigwedge_{i \in I}(A_i \to B_i)
    \qquad \Gamma \vdash x : A
  }{
    \Gamma \vdash f \, x : \bigwedge_{k \in I, A \leq A_k} B_k
  }
\]

## Non-idempotent intersection types

In the majority of intersection type systems,
$\land$ is associative, commutative and idempotent.
However, $\land$ can also be seen as the non-idempotent
[[multiplicative conjunction]] from [[linear logic]].

## Related concepts

* [[polymorphism]]
* [[union types]]

## References

* M. Coppo and M. Dezani-Ciancaglini. _A new type assignment for lambda-terms._
  Archive for Mathematical Logic, **19**:139–156, 1978.
* M. Coppo and M. Dezani-Ciancaglini.
  _An extension of the basic functionality theory for the λ-calculus._
  Notre Dame Journal of Formal Logic, **4**:685–693, 1980.

[[!redirects intersection types]]