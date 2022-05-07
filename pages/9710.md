
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The *pentagon identity* is the [[coherence]] [[identity]] satisfied by an [[associator]] in a [[monoidal category]] or more generally in a [[bicategory]], [[(2,1)-category]] etc, asserting that the following [[pentagon|pentagonal]] [[commuting diagram|diagram commutes]], where 

$$
  a_{x,y,z}
  \;\colon\;
  (x \otimes y) \otimes z
  \longrightarrow
  x \otimes (y \otimes z)
$$ 

is the [[associator]] [[natural transformation]] (or more generally: [[associator]] [[2-morphism]]).

\begin{centre}

\begin{tikzcd}[column sep = -3.1em, row sep = 10em, every label/.append style = {font = \Large}, font=\Large]
    & & (w \otimes x) \otimes (y \otimes z) \arrow[drr, "a_{w, x, y \otimes z}"] & & \\
    ((w \otimes x) \otimes y) \otimes z \arrow[urr, "a_{w \otimes x, y, z}"] \arrow[dr,"a_{w,x,y} \otimes \mathrm{id}_{z}", swap] & & & & w \otimes (x \otimes (y \otimes z)) \\
    & (w \otimes (x \otimes y)) \otimes z \arrow[rr, "a_{w, x \otimes y, z}", swap] & & w \otimes ((x \otimes y) \otimes z) \arrow[ur, "\mathrm{id}_{w} \otimes a_{x,y,z}", swap] &
\end{tikzcd}

\end{centre}

## Related concepts

* [[coherence law]]

* [[pentagonator]]

## References

* {#JoyalStreet} [[André Joyal]],[[Ross Street]], p. 10 of _Braided tensor categories_,  Adv. Math. 1993 ([pdf](http://web.science.mq.edu.au/~street/JS1.pdf))

For more references see at _[[braided monoidal category]]_ and at _[[coherence law]]_.



[[!redirects pentagon equation]]
[[!redirects pentagon equations]]

[[!redirects pentagon identities]]