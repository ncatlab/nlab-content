<div class="rightHandSide toc">
[[!include homotopy - contents]]
***
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

In $C$ a [[category with weak equivalences]] and with [[products]] a **path space object** (often just called a **path object**) for an [[object]] $X$ is a factorization of the diagonal morphism $X \stackrel{(Id, Id)}{\to} X \times X$ into the [[product]] as

$$
  X \stackrel{s}{\to} X^I \stackrel{(d_0, d_1)}{\to} X \times X
$$

such that $s$ is a weak equivalence.


**Notice.** Here $C^I$ is a primitive symbol. $I$ is _not_ assumed to be an object and $C^I$ is not assumed to be an [[closed category|internal hom]]. This is standard but somewhat abusive notation. It is supposed to remind us of the "nice" situation where the path object _is_ co-represented after all. See [[interval object]].

If the category in question also has a notion of [[fibration]]s, such as in a [[category of fibrant objects]] or in a [[model category]], the morphism 
$C^I \stackrel{(d_0, d_1)}{\to} C \times C$ in the definition of a path object is required to be a fibration.

Path space objects are in particular guaranteed to exist in any [[model category]].

## Examples

### In model categories

If $C$ is a [[model category]] then the factorization axiom ensures that for every object $X \in C$ there is a factorization of the diagonal 

$$
  X \stackrel{\simeq}{\to} X^I \stackrel{(d_0, d_1)}{\to} X \times X
$$

with the additional property that $X^I \to X \times X$ is a fibration.

If $X$ itself is fibrant, then the projections $X \times X \to X$ are fibrations and moreover by 2-out-of-3 applied to the diagram

$$
  \array{
    && X^I
    \\
    & {}^{\mathllap{s}}\nearrow && \searrow^{\mathrlap{d_i}}
    \\
    X &&\stackrel{Id}{\to}&& X
  }
$$

are themselves weak equivalences $X^I \stackrel{\simeq}{\to} X$. This is a key property that implies the [[category of fibrant objects|factorization lemma]].

If moreover the [[small object argument]] applies in the model catgeory $C$, then such factorizations, and hence path objects, may be chosen fonctorially: such that for each morphism $X \to Y$ the factorizations fit into a [[commuting diagram]]

$$
  \array{
     X &\stackrel{\simeq}{\to} &X^I &\to & X \times X  
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Y & \stackrel{\simeq}{\to} & Y^I &\to & Y \times Y  
  }
$$

### In simplicial model categories

If $C$ is a [[simplicial model category]], then the [[power]]ing over [[sSet]] can be used to explicitly construct functorial path objects for fibrant objcts $X$: define $X \to X^I \to X \times X$ to be the [[power]]ing of $X$ by the morphisms

$$
  \Delta[0] \coprod \Delta[0]
  \stackrel{d_0, d_1}{\hookrightarrow} \Delta[1]
  \stackrel{\simeq}{\to} 
  \Delta[0]
$$

in $sSet_{Quillen}$. Notice that the first morphism is a cofibration and the second a weak equivalence in the standard [[model structure on simplicial sets]] and that all objects are cofibrant.

Since by the axioms of an [[enriched model category]] the [[power]]in functor

$$
  (-)^{(-)} : sSet^{op} \times C \to C
$$

sends cofibrations and acyclic cofibrations in the first argument to fibratoins and acyclic fibrations inif the second argument is fibrant, and since this implies by the [[category of fibrant objects|factorization lemma]] that it then also preserves weak equivalences between cofibrant objects, it follows that $X^{\Delta[1]}$ is indeed a path object with the extra property that also the two morphisms $X^{\Delta[1]} \to X$ are acyclic fibratios.





## Related notions

### Right homotopies

Path objects are used to define a notion of [[right homotopy]] between morphisms in a category. Thus they capture aspects of [[higher category theory]] in a 1-categorical context.

### Loop space objects 

From a path space object may be derived [[loop space object]]s.




##Discussion

Originally the remark on abusive notation was missing and Toby asked:

What is $I$ here? Is it something that any category with weak equivalences must have (although I don\'t see how offhand), or is part of the data of the path object? (Indeed, it seems to be the only actual *object* in that data!) And then what are $d_0$ and $d_1$ exactly; maps $C^I \to C$, or maps involving $I$ itself whose product induces maps $C^I \to C$?

_Urs_: I hope the remark above now clarifies this. If so, this discussion part here should be removed.

_Toby_: The notation still doesn\'t make literal sense, since $C^I$ (primitive or not) isn\'t a product. But I believe that you just mixed up product and pairing, so I fixed that. In other words, I interpret it that $d_0$ and $d_1$ are each morphisms from $C^I$ to $C$.

[[!redirects path object]]
[[!redirects path objects]]
[[!redirects path space objects]]
[[!redirects cocylinder object]]
[[!redirects cocylinder objects]]
[[!redirects path space]]
