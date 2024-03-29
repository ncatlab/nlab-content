
#Contents#
* table of contents
{:toc}

## Definition

A [[field]] (in the sense of [[commutative algebra]]) $F$ is **perfect** if every [[algebraic extension]] of $F$ is [[separable extension|separable]]. In that case, every [[splitting field|splitting field extension]] of $F$ is a [[Galois extension]]. 

An extension $E/F$ is separable iff every element $\alpha \in E$ is separable, meaning that its irreducible polynomial $f \in F[x]$ (a monic generator of the kernel of $F[x] \to E: x \mapsto \alpha$) has no multiple roots. Of course $f$ has a multiple root only if its [[derivative]] satisfies $f'(\alpha) = 0$, which means $f' \in (f)$: by degree considerations this can happen only if $f'$ is the zero polynomial. Notice this cannot happen in characteristic zero.

A field, $F$, of characteristic $p$ is perfect if every element of $F$ is a $p$th power. This property is used in the generalization to [[perfect rings]].

## Examples 

All fields of [[characteristic]] zero are perfect, as are all [[finite fields]], all [[algebraically closed fields]], and all algebraic extensions of perfect fields. 

An example of a field that isn't perfect is the field of rational functions over a finite field.

## Related entry

* [[perfect ring]]
* [[perfectoid field]]

[[!redirects perfect fields]]
