
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[2-category theory]], the notion called *quasi-limits* &lbrack;[Gray (1997)](#Gray74)&rbrack; or *soft limits* &lbrack;[MacDonald & Stone (1989)](#MS89)&rbrack; is a weakening of the notion of [[bilimit]] so as to make them satisfy a 'quasi-universal' property. 
This means that instead of being singled out up to unique [[isomorphism]], quasi-limits are identified only up to unique _[[adjunction]]_. 

## Definition

Recall that [[limits]] and [[colimits]] of shape $\mathbf K$ are computed by the [[right adjoint|right]] and [[left adjoint]], respectively, to the [[diagonal]] [[functor]] $\Delta_{(-)} : \mathbf C \to [\mathbf K, \mathbf C]$ (the one which [[constant functors]]):

\[
   \colim \dashv \Delta \dashv \lim
   \,.
\]

Suppose now $\mathbf C$ is a [[2-category]] and $\mathbf K$ is a [[small category|small 2-category]]. Gray defines quasi(co)limits by relaxing the previous adjunction to be only a [[local adjunction]]:
\[
   \mathrm{qcolim} 
   \dashv_{\mathrm{loc}} 
   \Delta 
   \dashv_{\mathrm{loc}} 
   \mathrm{qlim}
\]
This means that, naturally in $X : \mathbf C$, there are adjunctions (instead of equivalences, like in a [[2-adjunction]]) between hom-categories:
\[
   \mathbf C(X, \mathrm{qlim} F) \rightleftarrows \mathrm{Nat}(\Delta_X, F)
\]

Alternatively, one can give a definition in terms of a weakened representability property.

Let $F : \mathbf K \to \mathbf C$ be a small [[diagram]] in $\mathbf C$. Then recall that a [[bilimit]] for $F$ is an [[object]] $\lim F:\mathbf C$ equipped with a natural family of [[equivalence in a 2-category|equivalences]]
\[
  \phi_X 
  \,\colon\, 
  \mathbf C(X, \lim F) 
    \cong 
  \mathrm{Nat}\Big(
    1, 
    \mathbf C\big(X, F(-)\big)
  \Big)
\]
where $\Delta_{(-)} : \mathbf C \to [\mathbf K, \mathbf C]$ is the diagonal functor.

A **quasi-limit** for $F$ is then an object $\mathrm{qlim} F:\mathbf C$ equipped with a family of adjunctions
\[
  \psi_X 
  \,\colon\, 
  \mathbf C(X, \mathrm{qlim}F) 
  \rightleftarrows 
  \mathrm{Nat}\Big(
    1, 
    \mathbf C\big(X, F(-)\big)
  \Big)
\]
naturally in $X:\mathbf C$.

Notice that by replacing $1 : \mathbf C \to \mathrm{Cat}$ with an arbitrary weight $W$ we can easily give the definition of _weighted quasilimit_.

## Examples

* A **quasi-terminal** object in a 2-category $\mathbf C$ is an object $Q$ such that, for each other object $X: \mathbf C$, there exists a 'quasi-universal map' $t : X \to Q$ such that every other map $f : X \to Q$ admits a unique 2-cell $\phi_f : f \Rightarrow t$ to it. In $\mathbf C = \mathbf{Cat}$ quasi-terminal objects are categories with a [[terminal object]].

From this example alone one can see quasi-limits are, in general, not unique up to isomorphism, like limits and other [[universal constructions]]. The universality of the objects is replaced by universality of their quasi-universal maps. A consequence of this fact is that we can't say _the_ quasi-limit but _a_ quasi-limit.

The following is an example of quasi-colimit from [(Gray '74, p.199)](#Gray74):

* A **quasi-coproduct** of $A_1$ and $A_2$ in a 2-category $\mathbf C$ is an object $A_1 +_q A_2$ together with injections $i_j : A_j \to A_1 +_q A_2$ ($j=1,2$) which satisfies a relaxed version of the universal property of [[coproducts]]. Instead, we require that for any other object $X$ with maps $h_j : A_j \to X$ there is a map $h : A_1 +_q A_2 \to X$ and 2-cells $\lambda_j : h\circ i_j \Rightarrow h_j$ ($j=1,2$) which are terminal as such. This means that given any other $g : A_1 +_q A_2 \to X$ and 2-cells $\gamma_j : g \circ i_j \Rightarrow h_j$ ($j=1,2$), there is a 2-cell $\phi_{(g,\gamma_j)} : g \to h$ that factorizes $\gamma$ through $\lambda$: $(\tau \cdot i_j) \circ \lambda_j = \gamma_j$.

In [Capucci (2022)](#Capucci22) it is shown that this (with [[2-cells]] reversed though) is the [[universal property]] of a certain example of monoidal product common in game theory, called _external choice_.

* A **quasi-product** is dual to a quasi-coproduct in the sense of reversing 1-cells. Reversing 2-cells is also possible, but there doesn't seem to be an agreed terminological scheme to distinguish between the two kinds of quasi-limits.

Notably, the product of sets, which in the 2-category of [[relations]] loses its usual universal property, becomes a quasi-product there. Notice both this and the above example of quasi-coproduct are unique up to iso.

## References

Quasi-limits and their duals have been defined in §I.7.9 of:

* {#Gray74} [[John Gray]], _[[Adjointness for 2-Categories|Formal category theory: adjointness for 2-categories]]_, Lecture Notes in Mathematics **391** 
Springer (1974) &lbrack;[doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280)&rbrack;

See also:

* _["Very lax" 2
-dimensional co/limits](https://mathoverflow.net/questions/386414/very-lax-2-dimensional-co-limits)_, MathOverflow

* {#MS89} MacDonald, Stone, _[Soft adjunction between 2-categories](https://www.sciencedirect.com/science/article/pii/0022404989901278)_, Journal of Pure and Applied Algebra, **60** (1989)

* {#Capucci22} [[Matteo Capucci]], _The Universal Property of External Choice_ (2022) &lbrack;[pdf](https://matteocapucci.files.wordpress.com/2022/03/main.pdf)&rbrack;
