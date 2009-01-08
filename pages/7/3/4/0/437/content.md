#Definition#

In a [[category with weak equivalences]] and with [[product]]s a _path object_ for an object $C$ is a factorization of the morphism $C \stackrel{Id \times Id}{\to} C \times C$ as
$$
  C \stackrel{s}{\to} C^I \stackrel{d_0 \times d_1}{\to} C \times C
$$
such that $s$ is a weak equivalence.

+--{.query}
What is $I$ here? Is it something that any category with weak equivalences must have (although I don\'t see how offhand), or is part of the data of the path object? (Indeed, it seems to be the only actual *object* in that data!) And then what are $d_0$ and $d_1$ exactly; maps $C^I \to C$, or maps involving $I$ itself whose product induces maps $C^I \to C$?
=--

If the category in question also has a notion of [[fibration]]s, such as in a [[category of fibrant objects]] or in a [[model category]], the morphism 
$C^I \stackrel{d_0 \times d_1}{\to} C \times C$ in the definition of a path object is required to be a fibration.

#Remarks#

Path objects are used to define a notion of [[homotopy]] between morphisms in a category. Thus they capture aspects of [[higher category theory]] in a 1-categorical context.