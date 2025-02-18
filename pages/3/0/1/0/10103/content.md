
> For the cartesian case see at *[[distributive category]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

* table of contents
{: toc}

## Idea

A _distributive monoidal_ category is a [[monoidal category]] whose [[tensor product]] [[distributive law|distributes]] over [[coproducts]].

## Definition

A **distributive monoidal category** (this is not entirely standard terminology) is a [[monoidal category]] with [[coproducts]] whose [[tensor product]] [[preserved colimit|preserves]] [[coproducts]] in each variable: i.e. such that the canonical morphisms
$$\coprod_i (X\otimes Y_i)\to X \otimes \coprod_i Y_i$$
$$\coprod_i (X_i\otimes Y)\to \Big(\coprod_i X_i\Big) \otimes Y$$
are [[isomorphisms]].

Depending on the arity of the coproducts in question, we may speak of a **finitary** or **infinitary** distributive monoidal category. 

The special case of distributive [[cartesian monoidal categories]] is known simply as  *[[distributive categories]]*. Conversely, distributive monoidal categories are a special case of [[rig categories]]. 

See also at *[[distributivity for monoidal structures]]*.

A more abstract way to say this, due to Weber and Batanin, is that if $M$ is the free monoidal category [[monad]] and $M V \xrightarrow{\otimes} V$ is the structure map of a monoidal category $V$, then $V$ is distributive if it admits [[left Kan extensions]] along functors $f:A\to B$ between [[discrete categories]] (of some size), and moreover if
$$\array{
  A && \xrightarrow{f} && B\\
  & \searrow & \xRightarrow{\phi} & \swarrow\\
  && V
}$$
is such a Kan extension, then so is
$$\array{
  M A && \xrightarrow{M f} && M B\\
  & \searrow & \xRightarrow{M \phi} & \swarrow\\
  && M V\\
  && \downarrow^\otimes\\
  && V.
}$$

## Examples
 {#Examples}

### Various

Beyond [[distributive categories]], examples of distributive monoidal categories include the following:

* [[Ab]], the category of [[abelian groups]] equipped with the [[tensor product of abelian groups]]

* $R$[[Mod]], the category of [[modules]] over a [[commutative ring]] $R$, equipped  with the [[tensor product of modules]]

* $k$[[Vect]] = $k$[[Mod]], the category of [[vector space]] over some [[field]] $k$, equipped with the [[tensor product of vector spaces]],

* $k$[[Vect(X)]], the category of ([[topological vector bundles|topological]]) [[vector bundles]] over some ([[topological space|topological]]) [[space]], equipped with the [[tensor product of vector bundles]],


In all these cases the coproduct is the respective [[direct sum]] (e.g. [[direct sum of vector bundles]] in the case of vector bundles).

Also:

* the category of [[pointed sets]] with respect to forming [[smash product]] and [[wedge sum]],

* more generally, the category of [[pointed topological spaces]] with respect to forming [[smash product]] and [[wedge sum]] (e.g. [Hatcher, Section 4.F](algebraic+topology#Hatcher)).

* $k$[[VectBund]], the category of ([[topological vector bundles|topological]]) [[vector bundles]] over any ([[convenient category of topological spaces|convenient]]) [[topological spaces]], equipped with the [[external tensor product of vector bundles]] (more on this [below](#ExamplesBundlesWithExternalTensorProduct)).


### Vector bundles with external tensor product
 {#ExamplesBundlesWithExternalTensorProduct}

We spell out in much detail the example of the [[category]] [[VectBund|$Vect_{Set}$]] of [[vector bundles]] over arbitrary base spaces and equipped with the [[external tensor product]] [[external tensor product of vector bundles|of vector bundles]] --- for the simple special case that the base spaces are [[discrete topological spaces]], i.e. plain [[sets]]:

\begin{definition}
  For any [[ground field]], write [[VectBund|$Vect_{Set}$]] for the [[category]] of [[indexed sets]] of [[vector spaces]].
\end{definition}
\begin{remark}
We may and will present [[objects]] $\mathcal{V}$ of [[VectBund|$Vect_{Set}$]] as [[pairs]] consisting of a [[set]] $S$ and a [[function]] $\mathcal{V}_{(-)}$ (really a [[functor]] on the [[discrete category]] on $S$) to [[Vect]]:
$$
  \left(
    \array{
      S &\longrightarrow& Vect
      \\
      s &\mapsto& \mathcal{V}_s
    }
  \right)
  \;\;
  \in
  \;\;
  Vect_{Set}
  \mathrlap{\,.}
$$
\end{remark}

\begin{definition}
\label{ExternalTensorProductInVectSet}
The "[[external tensor product|external]]" [[tensor product]] on [[VectBund|$Vect_{Set}$]] is the [[functor]] 
$$
  \boxtimes
  \,\colon\,
  Vect_{Set} \times Vect_{Set} 
    \longrightarrow
  Vect_{Set}
$$
given by
$$
  \big(
    \mathcal{V}_{(-)} \,\colon\, S \to \Vect
  \big)
  \,\boxtimes\,
  \big(
    \mathcal{V}'_{(-)} \,\colon\, S' \to \Vect
  \big)
  \;\;
  \coloneqq
  \;\;
  \left(
    \array{
      S \times S' &\longrightarrow& \Vect
      \\
      (s, s') 
        &\mapsto& 
      \mathcal{V}_s \otimes \mathcal{V}'_{s'}
    }
  \right)
  \mathrlap{\,.}
$$
\end{definition}

\begin{proposition}
\label{CoproductInVectSet}
  The [[coproduct]] in [[VectBund|$Vect_{Set}$]] is given by [[disjoint union]] of [[bundles]]:
$$
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to \Vect
  \big)
  \;
  \sqcup
  \;
  \big(
    \mathcal{V}^{(1)}_{(-)} \,\colon\, S_2 \to \Vect
  \big)
  \;\;
  \simeq
  \;\;
  \left(
    \array{
      S_1 \sqcup S_2 &\longrightarrow& \Vect
      \\
      s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
    }
  \right)
$$
\end{proposition}
\begin{proof}
  It is immediate to check the [[universal property]] characterizing the coproduct.
\end{proof}

\begin{proposition}
The [[external tensor product]] $\boxtimes$ 
(Def. \ref{ExternalTensorProductInVectSet})
[[distributive monoidal category|distributes]] over the coproduct (Prop. \ref{CoproductInVectSet}):
$$
  \mathcal{E} \boxtimes ( \mathcal{V}^{(1)} \sqcup  \mathcal{V}^{(2)}) 
  \;\simeq\;
  \big(  
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
  \big)
  \,\sqcup\,
  \big(
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \big)
$$
and hence gives a [[distributive monoidal category]]:
$$
  \big(
    Vect_{Set}
    ,
    \sqcup
    ,
    \boxtimes
  \big)
  \;\in\;
  DistMonCat
  \mathrlap{\,.}
$$
\end{proposition}
\begin{proof}
Unwinding the above definitions and using that [[Set]] is a [[distributive category]], we have the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{l}
    \mathcal{E} 
    \,\boxtimes\,
    \big(
      \mathcal{V}^{(1)}
      \,\sqcup\,
      \mathcal{V}^{(2)}
    \big)
    \\
    \;\equiv\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \Big(
      \big(
        \mathcal{V}^{(1)}_{(-)} \,\colon\, S_1 \to Vect
      \big)
      \,\sqcup\,
      \big(
        \mathcal{V}^{(2)}_{(-)} \,\colon\, S_2 \to Vect
      \big)
    \Big)
    \\
    \;\simeq\;
    \big(
      \mathcal{E}_{(-)} \,\colon\, S_E \to Vect
    \big)
    \,\boxtimes\,
    \left(
      \array{
        S_1 \sqcup S_2 &\longrightarrow& Vect
        \\
        s_i &\mapsto& \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times (S_1 \sqcup S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        (S_E \times S_1) \,\sqcup\, (S_2 \times S_2)
        &\longrightarrow& Vect
        \\
        (s_E , s_i) &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(i)}_{s_i}
      }
    \right)
    \\
    \;\simeq\;
    \left(
      \array{
        S_E \times S_1 
        &\longrightarrow& Vect
        \\
        (s_E , s_1) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(1)}_{s_1}
      }
    \right)
    \,\sqcup\,
    \left(
      \array{
        S_E \times S_2 
        &\longrightarrow& Vect
        \\
        (s_E , s_2) 
         &\mapsto&
        \mathcal{E}_{s_E} \otimes \mathcal{V}^{(2)}_{s_2}
      }
    \right)
    \\
    \;\equiv\;
    \mathcal{E} \boxtimes \mathcal{V}^{(1)}
    \,\sqcup\,
    \mathcal{E} \boxtimes \mathcal{V}^{(2)}
  \end{array}
$$
\end{proof}



## Properties

### The weakly semicartesian case

+-- {: .num_remark} 
###### Remark 
A monoidal category is finitary distributive if its tensor product preserves binary coproducts in each variable and the monoidal unit $I$ is [[weak limit|weakly]] [[terminal object|terminal]] (e.g., if there is a morphism $1 \to I$ out of a terminal object). 
=-- 

+-- {: .proof} 
###### Proof 
There is a canonical isomorphism 
$$x \otimes 0 + x \otimes y \to x \otimes (0 + y)$$ 
and thus a canonical isomorphism 
$$\phi: x \otimes 0 + x \otimes y \to x \otimes y$$ 
whose restriction along the coproduct inclusion $x \otimes y \to x \otimes 0 + x \otimes y$ is the identity $1_{x \otimes y}$. Let $k: x \otimes 0 \to x \otimes y$ be the restriction of $\phi$ along the other coproduct inclusion. Then $\phi$ induces an evident bijection 
$$\hom(x \otimes y, y) \stackrel{\langle [k], id \rangle}{\to} \hom(x \otimes 0, y) \times \hom(x \otimes y, y).$$ 
Since $\hom(x \otimes y, y)$ is inhabited for all $x, y$ (with the help of some map $x \to I$, there is some map $x \otimes y \to I \otimes y \cong y$), this forces $\hom(x \otimes 0, y)$ to be a singleton for any $y$, so that $x \otimes 0$ is initial. 
=-- 


### Free monoids

A distinguishing feature of (infinitary) distributive monoidal categories is that the [[monad]] $T$ for [[monoid objects]] in such a category has a particularly simple expression:
$$ T X = \coprod_n X^{\otimes n}.$$
The same is true for the monad on enriched graphs whose algebras are categories enriched over such a monoidal category.  This also generalizes to [[lax monoidal categories]], a.k.a. "multitensors"; see [Weber 13](#Weber13).

## Related concepts

* [[distributive law]]

* [[distributivity for monoidal structures]]

  * [[distributive monoidal category]]

  * [[bipermutative category]]

  * [[linearly distributive category]]

  * [[rig category]]


## References

* [[Hans-Joachim Baues]], [[Mamuka Jibladze]], [[Andy Tonks]], first page of: *Cohomology of monoids in monoidal categories*, in: *Operads: Proceedings of Renaissance Conferences*, Contemporary Mathematics **202**, AMS (1997) 137-166 &lbrack;[doi:10.1090/conm/202](https://doi.org/10.1090/conm/202), preprint:[pdf](https://archive.mpim-bonn.mpg.de/id/eprint/1484/1/preprint_1995_121.pdf)&rbrack;

* [[Anna Labella]], *Categories with sums and right distributive tensor product*, Journal of Pure and Applied Algebra **178** 3 (2003) 273-296 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(02)00169-X">doi:10.1016/S0022-4049(02)00169-X</a>&rbrack;

* {#Weber13} [[Mark Weber]], *Multitensors and monads on categories of enriched graphs*, [[TAC]] **28** 26 (2013) &lbrack;[tac:28-26](http://www.tac.mta.ca/tac/volumes/28/26/28-26abs.html)&rbrack; 

[[!redirects distributive monoidal categories]]
