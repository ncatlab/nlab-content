#Definition#

The **category algebra** $k[C]$ over a ground field $k$ of a small [[category]] $C$ is as a vector space spanned by the morphisms of $C$, 

$$k[C] = span_k(C_1)
\,,
$$ 

where the product of two morphisms $f$ and $g$ is defined to be their composite if composable, and 0 otherwise

$$
  f \cdot g := \left\lbrace
    \array{
      g \circ f & if composable
      \\
      0 & otherwise
    }
  \right.
 \,.
$$ 

#Remarks#

If the category $C = \mathbf{B}G$ is a [[groupoid]] with a single object, which is canonically identified with a group $G$, then the category algebra coincides with the familiar [[group algebra]], 

$$
 k[\mathbf{B}G] = k[G]
  \,.
$$

+--{.query}

I think that the nLab presents a fantastic opportunity to define familiar concepts _arrow theoretically_. Is there a more arrow theoretic way to define a category algebra? - [[Eric Forgy|Eric]]

=--