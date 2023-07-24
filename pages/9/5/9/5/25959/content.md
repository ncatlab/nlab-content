
\tableofcontents

## Idea

MV-algebras are the algebraic semantics for [[propositional logic|propositional]] [[Łukasiewicz logic]]. 

## Definition

An **MV-algebra** is a [[commutative monoid]] $(S, 0, \oplus)$ with an [[involution]] $x \mapsto \neg x:S \to S$ such that for all $x \in S$ and $y \in S$, $x \oplus \neg 0 = \neg 0$ and $\neg (\neg x \oplus y) \oplus y = \neg (\neg y \oplus x) \oplus x$. 

An MV-algebra [[homomorphism]] between MV-algebras $A$ and $B$ is a [[function]] $f:A \to B$ such that $f(0) = 0$, for all $x \in A$, $\neg f(x) = f(\neg x)$, and for all $x \in A$ and $y \in A$, $f(x) \oplus f(y) = f(x \oplus y)$. 

## Examples

* The [[unit interval]] $[0, 1]$ is an MV-algebra where $x \oplus y$ is defined as $\max(x + y, 1)$ and $\neg x$ is defined as $1 - x$. 

* Every [[Boolean algebra]] is a MV-algebra whose monoid operation is idempotent. 

* Any [[singleton]] $1$ is a trivial MV-algebra where $x \oplus y$ is defined as the unique [[binary function]] on $1$ and $\neg x$ defined as the unique unary function on $1$, the [[identity function]] on $1$. It is also the [[terminal object|terminal]] MV-algebra in the category of MV-algebras and MV-algebra homomorphisms. 

## Related concepts

* [[Łukasiewicz logic]]

## References

* Wikipedia, [MV-algebra](https://en.wikipedia.org/wiki/MV-algebra)