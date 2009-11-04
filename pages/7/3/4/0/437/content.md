<div class="rightHandSide toc">
[[!include homotopy - contents]]
</div>


#Definition#

In a [[category with weak equivalences]] and with [[product]]s a **path object** for an object $C$ is a factorization of the morphism $C \stackrel{Id \times Id}{\to} C \times C$ as
$$
  C \stackrel{s}{\to} C^I \stackrel{(d_0, d_1)}{\to} C \times C
$$
such that $s$ is a weak equivalence.


**Notice.** Here $C^I$ is a primitive symbol. $I$ is _not_ assumed to be an object and $C^I$ is not assumed to be an [[closed category|internal hom]]. This is standard but somewhat abusive notation. It is supposed to remind us of the "nice" situation where the path object _is_ co-represented after all. See [[interval object]].


If the category in question also has a notion of [[fibration]]s, such as in a [[category of fibrant objects]] or in a [[model category]], the morphism 
$C^I \stackrel{(d_0, d_1)}{\to} C \times C$ in the definition of a path object is required to be a fibration.

#Remarks#

Path objects are used to define a notion of [[homotopy]] between morphisms in a category. Thus they capture aspects of [[higher category theory]] in a 1-categorical context.

#Discussion#

Originally the remark on abusive notation was missing and Toby asked:

What is $I$ here? Is it something that any category with weak equivalences must have (although I don\'t see how offhand), or is part of the data of the path object? (Indeed, it seems to be the only actual *object* in that data!) And then what are $d_0$ and $d_1$ exactly; maps $C^I \to C$, or maps involving $I$ itself whose product induces maps $C^I \to C$?

_Urs_: I hope the remark above now clarifies this. If so, this discussion part here should be removed.

_Toby_: The notation still doesn\'t make literal sense, since $C^I$ (primitive or not) isn\'t a product. But I believe that you just mixed up product and pairing, so I fixed that. In other words, I interpret it that $d_0$ and $d_1$ are each morphisms from $C^I$ to $C$.

[[!redirects path objects]]
[[!redirects cocylinder object]]
[[!redirects cocylinder objects]]
