
\begin{proposition}
**(normal form for 2d cobordisms)**
\linebreak
Every *[[connected topological space|connected]]* [[cobordism]] with

* $n_{in}$ ingoing boundary components

* $n_{ouy}$ outgoing boundary components

* [[genus of a surfce|genus]] $g$

is equivalent ([[diffeomorphism|diffeomorphic]]) to the [[composition]] of 

* $n_{in}-1$ [[trinions]] regarded as $S^1 \times S^1 \to S^1$

* $g$ 2-punctured [[tori]] $S^1 \to S^1$

* $n_{out}-1$ [[trinions]] regared as $S^1 \to S^1 \times S^1$

as shown in the following example for 

* $n_{in} = 5$

* $g = 4$

* $n_{out}$

<center>
<img src="/nlab/files/2dCObordismNormalForm.jpg" width="600">
</center>

> (graphics from [Kock 2004, p. 64](#Kock2004))

\end{proposition}
This fact probably ought to be regarded as classical; an explicit account is given in [Kock 2004, §3.1.2](#Kock2004).

By the [relation](#RelationTo2DTQFT) between 2d cobordism and Frobenius algebras this means equivalently that:



\begin{corollary}\label{NormalFormForFrobeniusMaps}
**(normal form for Frobenius maps)**
\linebreak
Given a Frobenius algebra

$$
  \big(
    A 
    ,\,
    unit
    ,\,
    counit
    ,\,
    prod
    ,\,
    coprod
  \big)
$$

then every linear map of the form

$$
  A^{\otimes^{n_{in}}}
  \longrightarrow
  A^{\otimes^{n_{out}}}
$$

which is 

1. entirely the composite of the algebra's structure maps, ie. of the (co)unit and the (co)product, 

1. *connected* in that it does not decompose as a tensor product of such morphisms,

is equal to the composite of

* $n_{in}-1$ copies of $prod$

* some number ($g$) of copies of $prod \circ coprod$

* $n_{out}$ copies of $coprod$ 
  
\end{corollary}
