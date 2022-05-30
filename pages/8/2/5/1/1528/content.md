
# Moore path categories
* table of contents
{: toc}

## Idea

The classical  _Moore path category_ of a [[topological space]] $X$ is a variant on the usual space of [[paths]] $I \to X$, but one which yields a [[strict category]] (even an [[internal category|internal]] [[dagger category|$\dagger$-category]] in [[Top]]).

## Definition

\begin{definition}
Let $X$ be a [[topological space]]. Its **Moore path category** $M X$ has

* as space of objects $M_0 X \coloneqq (M X)_0 \coloneqq X$;

* as space of morphisms $M_1 X \coloneqq (M X)_1 \subseteq X^{[0,\infty]} \times [0,\infty)$ the subspace of pairs $(\gamma, len(\gamma))$ where $\gamma \colon [0, \infty) \to X$ is continuous and constant on $[len(\gamma), \infty]$;
 the source $s(\gamma)$ of $\gamma$ is $\gamma(0)$ and the target $t(\gamma)$ of $\gamma$ is $\gamma(len(\gamma))=\gamma(\infty)$;

* as composition ${\circ} \colon M_1 X \times_{M_0 X} M_1 X \to M_1 X$, given by $len(\gamma' \circ \gamma) = len (\gamma) + len (\gamma')$, $(\gamma' \circ \gamma)(t)=\gamma(t)$ for $t\in[0, len (\gamma)]$ and $(\gamma' \circ \gamma)(t)=\gamma'(t - len (\gamma))$ otherwise;

* as identity-assigning map $X \to M_1 X$ the map sending $x\in X$ to the pair $(t \mapsto x, 0)$;

* as [[dagger-category|path-reversal]] map $(\gamma, len (\gamma))^\dagger \coloneqq (t \mapsto \gamma(len (\gamma) - t), len (\gamma))$.

\end{definition}

The reference below defines $M_*(X)$ as a strict [[cubical omega-category|cubical]] $\omega$-category. It also has connections, which satisfy all the laws except cancellation of $\Gamma^-_i$ and $\Gamma^+_i$ under composition. This structure seems a sensible home for $n$-paths in $X$ for all $n \geq 0$, and has the advantage  over simplicial or globular versions of "$\infty$-groupoids" of easily encompassing multiple compositions. 

\begin{definition}
Suppose $f \colon X \to Y$ is a continuous map. The **Moore mapping path space** $\Gamma f$ is the [[pullback]]

\begin{tikzcd}
  \Gamma f \arrow[r] \arrow[d] \arrow[dr, phantom, "\lrcorner" , very near start]
& M_1 Y \arrow[d, "s"] \\
  X \arrow[r, "f"]
& Y\text.
\end{tikzcd}

\end{definition}
([Barthel–Riehl 2013, definition 3.2](#BarthelRiehl2013))

## Properties

### Functorial factorization

\begin{proposition}
The Moore mapping path space construction $\Gamma\colon Top^\to \to Top$ yields a [[functorial factorization]] of maps $f\colon X\to Y$ as a composition

$$
  X \stackrel{L f}{\to} \Gamma f \stackrel{R f}{\to} Y
$$

of a [[Strøm model structure|(closed) trivial Hurewicz cofibration]] $L f$ and a [[Hurewicz fibration]] $R f$.
\end{proposition}
([Barthel–Riehl 2013, section 3.1 and corollary 3.12](#BarthelRiehl2013))

\begin{proposition}
A morphism of $Top$ is

* a Hurewicz fibration iff it admits an [[algebra for an endofunctor|algebra structure]] for the [[pointed endofunctor]] $R$;

* a [[Strøm model structure|(closed) trivial Hurewicz cofibration]] iff it admits a [[coalgebra for an endofunctor|coalgebra structure]] for the [[copointed endofunctor]] $L$ (a _Moore strong deformation retraction_).

\end{proposition}
([Barthel–Riehl 2013, section 3.3](#BarthelRiehl2013))


## Related concepts

* [[schedule]]


## Reference

* {#BarthelRiehl13} [[Tobias Barthel]], [[Emily Riehl]], _On the construction of functorial factorizations for model categories_, Algebr. Geom. Topol. 13 (2013) 1089-1124 ([arXiv:1204.5427](http://arxiv.org/abs/1204.5427), [doi:10.2140/agt.2013.13.1089](https://doi.org/10.2140/agt.2013.13.1089), [euclid:agt/1513715550](https://projecteuclid.org/euclid.agt/1513715550))

* [[Ronnie Brown|R. Brown]], _Moore hyperrectangles on a space form a strict cubical omega-category_, [arXiv 0909.2212v2](http://arxiv.org/abs/0909.2212)


[[!redirects Moore path space]]
[[!redirects Moore path spaces]]