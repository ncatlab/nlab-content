
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

> For disambiguation see at *[[wreath product]]*.


\tableofcontents

## Idea

[[wreath|Wreaths]] are the natural generalization of [[distributive laws]]. Like the latter, they produce a sort of composite [[monad]], the **wreath product**.

Formally, let $EM(\mathcal{K})$ be the free completion of a 2-category under [[Eilenberg--Moore object|$EM$ objects]]. A wreath is an object in $EM(EM(\mathcal{K}))$, and since $EM$ is a monad, it admits a multplication which is indeed the wreath product $\wr : EM(EM(\mathcal{K})) \to EM(\mathcal{K})$.

## Definition

Let $(A,(t,\eta,\mu),(s, \lambda, \sigma, \nu))$ be a [[wreath]] in $\mathcal{K}$. Its **wreath product** is the monad on $A$ in $\mathcal{K}$ so defined:

1. its carrier 1-cell is $st$ (first $t$ then $s$),
1. its unit is $\sigma : 1 \to st$,
1. its multiplication is
\[
  stst \xrightarrow{s \lambda t} sstt \xrightarrow{ss \mu} sst \xrightarrow{\nu t} stt \xrightarrow{s\mu} st
\]

\begin{remark}
Every [[distributive law]] is a wreath, and the wreath product of a distributive law *qua* wreath indeed coincides with the composite monad one would get out of the distributive law.
\end{remark}

## Related concepts

* [[wreath]]
* [[weak wreath product]]

## References

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], *The formal theory of monads II*, Journal of Pure and Applied Algebra **175** 1-3 (2002) 243-265 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00137-8">doi:10.1016/S0022-4049(02)00137-8</a>&rbrack;
