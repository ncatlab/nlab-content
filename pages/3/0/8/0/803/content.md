
##Definition#


The **double comma object** of three morphisms $f:A\to D$, $g:B\to D$, and $h:C\to D$ in a [[2-category]] can be defined as
$$(f/g/h) = (f/g)\times_B (g/h)$$
where $(f/g)$ and $(g/h)$ are the ordinary [[comma object]]s.  It can also be characterized as a [[2-limit]] in its own right.


## Examples

### in [[Cat]] ####

A double comma category is among other things the strict pullback

$$
  \array{
     (f/g/h) &\to& [I^{\vee 2}, D]
     \\
     \downarrow && \downarrow^{d_0 \times d_1 \times d_2}
     \\
     A \times B \times C &\stackrel{f\times g \times h}{\to}&
     D \times D \times D
  }
  \,,
$$

where $I^{\vee 2} = \{a \to b \to c\}$ is the category freely generated from two composable morphisms (the linear [[quiver]] of length 2), obtained from the standard [[interval object]] in [[Cat]] by gluing it to itself. $[I^{\vee 2],D]$ is the [[functor category]], i.e. the category of composable pairs of morphisms in $D$.



* If $A=C=1$ are the [[terminal category]] in [[Cat]] and $g$ is the identity functor, then $f=x$ and $h=y$ are objects of $D$ and $(f/g/h) = (x/D/y)$ is sometimes called the **[[over category|over]]-[[under category|under]]-category**.

* If $f,g,h$ are all the identity functor of $A$, then $(f/g/h)$ is the [[power]] $A^{(\to\to)}$, the "object of composable pairs in $A$."

[[!redirects double comma objects]]