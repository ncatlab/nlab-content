#Idea#

A **double complex** is a [[complex]] in a category of [[complex]]es. Accordingly, a **double chain complex** is a [[chain complex]] in a [[category of chain complexes]].

In the presence of enough [[product]]s and/or [[coproduct]]s, there is a _total complex_ associated to a double complex, and the interest in double complexes is usually that in these total complexes.

Double chain complexes usually arise from the application of [[bifunctor]]s of [[additive category|additive categories]] $C_1, C_2, C_3$

$$
  F :  C_1 \times C_2 \to C_3
$$

to complexes in their two arguments. Combining this with the formation of total complexes then yields bifunctors from  categories of complexes to categories of complexes. 

$$
 \tilde F : Ch(C)^{op} \times Ch(C) \to Ch(C)
 \,.
$$

The most important examples of this are induced by the [[hom-functor]] and the [[tensor product]] functor.

Under the [[Dold-Kan correspondence]] then $\tilde F$ can be understood as the [[internal hom]] between [[infinity-groupoid|higher groupoids]].


#Definition#


bla bla

$$
  \array{
   && \vdots && \vdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n,m} &\stackrel{d_X^h}{\to}& X_{n,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
    \cdots &\to & 
    X_{n,m} &\stackrel{d_X^h}{\to}& X_{n,m-1}
    & \to & \cdots
   \\
   & & \downarrow^{d_X^v} && \downarrow^{d_X^v}
   \\
   && \vdots && \vdots
  }
$$

bla bla


$$
  tot_{\oplus}^k = \bigoplus_{m+n=k} X_{n,m}
$$
$$
  d^k_{tot_\oplus}|_{X_{n,m}} = 
  d^v_X \sqcup (-1)^\bullet d_X^h 
$$

bla bla

$$
  tot_{\prod}^k = \prod_{m+n=k} X_{n,m}
$$
$$
  d^k_{tot_\prod}|_{X_{n,m}} = 
  d^v_X + (-1)^\bullet d_X^h 
$$

...