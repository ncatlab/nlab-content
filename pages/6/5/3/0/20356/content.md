
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

The *Samelson product* associated with a [[grouplike space]] (such as a [[topological group]] or a [[based loop space]]) is the [[group commutator]] operation descended from the [[Cartesian product]] to the [[smash product]] of the space with itself.

## Definition
 {#Definition}

Let $\mathcal{G}$ be a [[grouplike space]] with:

* [[neutral element]] $\mathrm{e} \,\colon\, \ast \longrightarrow \mathcal{G}$,

* [[binary operation]] $(-)\cdot(-) \,\colon\, \mathcal{G} \times \mathcal{G} \longrightarrow \mathcal{G}$,

* [[inverse]]-assigning map $(-)^{-1} \,\colon\, \mathcal{G} \longrightarrow \mathcal{G}$,

and regarded as a [[pointed topological space]] with base point $\mathrm{e}$.

Consider the "[[group commutator]]"

\[
  \label{TheGrouplikeCommutator}
  \begin{array}{ccc}
    \mathcal{G} \times \mathcal{G}
      &\overset{[-,-]}{\longrightarrow}&
    \mathcal{G}
    \\
    (g_1 , g_2) 
      &\mapsto&
    (g_1 \cdot g_2) \cdot (g_1^{-1} \cdot g_2^{-1})
  \end{array}
\]

(or any other way of bracketing it) and observe that this is a pointed map which as such vanishes on the [[wedge sum]]

$$
  \begin{array}{ccc}
    \mathcal{G} \vee \mathcal{G}
      &\xhookrightarrow{\phantom{--}}&
    \mathcal{G} \times \mathcal{G}
  \end{array}
$$

in that $[g,\mathrm{e}] = [\mathrm{e}, g] = \ast$ for all $g \in \mathcal{G}$. Therefore this map descends to the [[quotient space]] which is the *[[smash product]]*

$$
  \mathcal{G} \wedge \mathcal{G}
  \,\coloneqq\,
  \frac{
    \mathcal{G} \times \mathcal{G}
  }{
    \mathcal{G} \vee \mathcal{G}
  }
  \,.
$$

\begin{definition}
This descended map is, up to [[homotopy]], the *Samelson product* on $\mathcal{G}$, which we shall denote by the same symbols:
$$
  \mathcal{G} \wedge \mathcal{G}
  \xrightarrow{ [-,-] }
  \mathcal{G}
  \mathrlap{\,.}
$$
\end{definition}

Induced from this, is the *Samelson product on homotopy groups* 
$$
  \pi_{n_1}(\mathcal{G})
  \times
  \pi_{n_2}(\mathcal{G})
  \xrightarrow{ [-,-] }
  \pi_{n_1 + n_2}(\mathcal{G})
$$
for $n_1, n_2 \in \mathbb{N}$, given by sending representative [[maps]]
$$
  g_i \colon S^{n_i} \longrightarrow \mathcal{G}
$$
to the [[homotopy class]] of the composite
$$
  S^{n_1 + n_2}
  \simeq
  S^{n_1} \wedge S^{n_2}
  \xrightarrow{
    g_1 \wedge g_2
  }
  \mathcal{G} \wedge \mathcal{G}
  \xrightarrow{ [-,-] }
  \mathcal{G}
  \mathrlap{\,.}
$$



## Related concepts

* [[Whitehead product]]

* [[Pontrjagin product]]

## References

Original reference, proving that the [[Whitehead product]] is the [[commutator]] of the [[Pontrjagin product]]:

* [[Hans Samelson]], *A Connection Between the Whitehead and the Pontryagin Product*, American Journal of Mathematics **75** 4 (1953) 744–752  &lbrack;[doi:10.2307/2372549](https://doi.org/10.2307/2372549)&rbrack;


Expository accounts:

* [[Joseph Neisendorfer]]: _Samelson products and exponents of homotopy groups_,  Journal of Homotopy and Related Structures **8** 2 (2013) 239-277 &lbrack;[doi:10.1007/s40062-012-0021-4](http://dx.doi.org/10.1007/s40062-012-0021-4)&rbrack;

* [[Joseph Neisendorfer]]:  *Samelson products*, Chapter 6 in: _Algebraic Methods in Unstable Homotopy Theory_, 158-220.  Cambridge University Press.  &lbrack;[doi:10.1017/cbo9780511691638.008](https://doi.org/10.1017/cbo9780511691638.008)&rbrack;

History:

* {#James71} [[Ioan Mackenzie James]]: *Products between homotopy groups*,  Compositio Mathematica, **23** 3 (1971) 329-345 &lbrack;[numdam:CM_1971__23_3_329_0](http://www.numdam.org/item/?id=CM_1971__23_3_329_0)&rbrack;

In the context of [[gauge groups]] ([[automorphism groups]]) of [[principal bundles]]:

* [[Christoph Wockel]]: *The Samelson Product and Rational Homotopy for Gauge Groups*, Abh. Math. Sem. Univ. Hamburg **77** (2007) 219-228 &lbrack;[arXiv:math/0511404](https://arxiv.org/abs/math/0511404)&rbrack;


[[!redirects Samelson products]]