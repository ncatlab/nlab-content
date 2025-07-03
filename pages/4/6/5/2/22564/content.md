
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definitions

Given a [[natural number]] $n$, an __n-ary operation__ on a [[set]] $S$ is a [[function]] 

$$
  \phi
  \;\colon\;
  \big(
    \mathrm{Fin}(n) \to S
  \big) 
  \longrightarrow 
  S
$$ 

from the [[function set]] $\mathrm{Fin}(n) \to S$ to $S$ itself, where $\mathrm{Fin}(n)$ is the [[finite set]] with $n$ elements. 

The __arity__ of the operation is $n$. 

In general, if the natural number $n$ is not specified, these are called **finitary operations**. 

Sets equipped with finitary operations are also called **finitary [[magmas]]** (or "finitary groupoids" in older terminology which now clashes with another meaning of *[[groupoid]]*, see at *[[historical notes on quasigroups]]*). 

More generally, a finitary operation in a [[multicategory]] is just a [[multimorphism]]. 

### Arbitrary arity

More generally, one could use an arbitrary [[set]] instead of a [[finite set]]. However, the generalizations are only definable in [[closed monoidal category|closed]] [[multicategories]], rather than any [[multicategory]]. 

In [[dependent type theory]], one can also use an arbitrary [[type]] $I$ instead of a [[finite type]] to define functions of **arbitrary arity**:

$$\overline{x}:\prod_{x:I} A(x) \vdash f(\overline{x}):B$$

An operation of **arbitrary arity** is a function where the sources and target are the same:

$$\overline{x}:I \to A \vdash f(\overline{x}):A$$

These are important for defining [[impredicative]] structures such as [[suplattices]], [[frames]], [[complete Heyting algebras]], and [[Grothendieck topoi]]. 

Moreover, in addition to functions and operations of arbitrary arity, one also has [[type families]] and [[dependent functions]] of arbitrary arity. These are, in essence, families indexed by [[dependent product types]]:

$$\overline{x}:\prod_{x:I} A(x) \vdash B(\overline{x}) \; \mathrm{type} \qquad \overline{x}:\prod_{x:I} A(x) \vdash f(\overline{x}):B(\overline{x})$$

These are important for defining [[identity types#OfArbitraryArity|identity types]] $\mathrm{Id}_{I, A}(\overline{x})$ and [[bridge types#OfArbitraryArity|bridge types]] $\mathrm{Br}_{I, A}(\overline{x})$ of arbitrary arity, as well as expressing [[function application to identifications]] for functions of arbitrary arity. 

## Properties

Every set $S$ with an $n$-ary operation $\phi$ comes with an [[endomorphism]] called the *$n$-th [[power operation]]*

$$
  \array{
    S
    & 
    \overset{\;\;(-)^n\;\;}{\longrightarrow} 
    &
    S
    \\
    x
    &\mapsto&
    \phi \circ diag_n(x)
    \,,
  }
$$ 

where $ S \overset{diag_n}{\longrightarrow} S^n$ is the [[diagonal morphism]].

## See also

* [[magma]]

* [[monoid]]

* [[operation]]

* [[multicategory]]

* [[operad]]

### $n$-ary algebraic structures

* [[n-ary semigroup]]

* [[n-ary quasigroup]]

* [[n-ary group]]

* [[group]]

* [[commutative operation]]

## References

* Wikipedia, [n-ary group](https://en.wikipedia.org/wiki/N-ary_group)

* [[Steven Duplij]], *Polyadic Algebraic Structures*, IOP (2022) &lbrack;[ISBN:978-0-7503-2646-9](https://iopscience.iop.org/book/978-0-7503-2648-3)&rbrack; 

[[!redirects n-ary operation]]
[[!redirects n-ary operations]]

[[!redirects n-ary magma]]
[[!redirects n-ary magmas]]

[[!redirects finitary operation]]
[[!redirects finitary operations]]

[[!redirects finitary magma]]
[[!redirects finitary magmas]]

[[!redirects arbitrary arity]]
[[!redirects arbitrary arities]]