
\begin{lemma}
**(Milnor's exercise)**
\linebreak
For a [[smooth manifold]] $X \in SmthMfd$, the [[evaluation map]] (from its [[underlying]] [[set]] to the [[hom-set]])
$$
  \begin{array}{l}
   X 
     &\overset{ev}{\longrightarrow}& 
   Hom_{Alg_{\mathbb{R}}}
   \big(
     C^\infty(X)
     ,\,
     \mathbb{R}
   \big)
   \\
   x &\mapsto&
   \big(
     \phi \,\mapsto\, \phi(x)
   \big)
  \end{array}
$$
is a [[bijection]].
\end{lemma}
([Kolář, Michor & Slovák 1993 Cor. 35.9](#KolarSlovakMichor93))



## References

* {#KolarSlovakMichor93} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], chapter 35 of: _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[book webpage](http://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;


***

$$
  \phi 
  \;\in\;
  Hom\big(
    C^\infty(
      \mathbb{R}^n, \mathbb{R}
    )
    \;,\;
    \mathbb{R}[\epsilon]/(\epsilon^2)
  \big)
$$

$$
  x^a \;\mapsto\; \epsilon v^a
$$

$$
  f - f(y)\cdot 1 -  \big(\partial_a f(y)\big)\cdot (x-y)^a
  \;\mapsto\;
  0
$$

$$
  \phi
  \;\in\;
  Hom\big(
    C^\infty(\mathbb{R}^n, \mathbb{R})
    ,\,
    C^\infty(\mathbb{R}^m, \mathbb{R}) \otimes W
  \big)
$$

$$
  (ev_x \otimes id)\circ \phi
  \,\in\,
  Hom\big(
    C^\infty(\mathbb{R}^n, \mathbb{R})
    ,\,
    W
  \big)
$$


