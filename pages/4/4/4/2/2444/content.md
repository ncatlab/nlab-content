
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

There are two different notions that one might mean by "complex supermanifolds", and both are in use (the terminology is a mess!):

1. In the first sense, complex supermanifolds generalize the notion of [[smooth manifolds]] with their [[sheaf]] of smooth complex-valued functions, just as ordinary [[supermanifolds]] are a generalization of ordinary manifold with their sheaf of smooth real-valued functions.

   However, considering ordinary smooth manifolds as [[ringed spaces]] with either their sheaves of real or complex smooth functions gives two equivalent categories, whereas this is not true in the case of real and complex supermanifolds; the corresponding functor is neither [[essentially surjective]] nor [[fully faithful]].

   (For $X$ a complex supermanifold in this sense, the underlying reduced manifold $X_{red}$ is *not* a [[complex manifold]] but just a [[smooth manifold]] regarded as a [[ringed space]] with [[structure sheaf]] taken to be the sheaf of $\mathbb{C}$-valued smooth functions on the ordinary real manifold.)

1. In the second sense, complex supermanifolds are super(complex manifolds), a [[supergeometry|supergeometric]] version of [[complex manifolds]].

## Smooth complex supermanifolds

A **smooth complex supermanifold** is a [[ringed space]] $X = (|X|, O_X)$ such that

* the [[structure sheaf]] $O_X$ a [[sheaf]] of commutative complex [[super algebra]]s

*  locally $O_X$ is [[isomorphism|isomorphic]] to $
  C^\infty(\mathbb{R}^d) \otimes_{\mathbb{C}} \wedge^\bullet \mathbb{C}^\delta$

The pair $d|\delta$ is known as the __superdimension__ of $X$.

Write cSDiff for the [[category]] of complex supermanifolds.


\begin{example}
The functor
$$\Pi : \text{real vector bundles} \to SDiff$$
has a complex analogue
$$\Pi : \text{complex vector bundles} \to cSDiff.$$

Let $E \to X$ be a complex [[vector bundle]] of rank $\delta$.
This gives rise to the complex supermanifold $\Pi E$, in the [[supermanifold|same way]] as a real vector bundle gives rise to a real supermanifold: 
the structure sheaf is given by sections of the exterior algebra of the dual of $E$.
\end{example}

\begin{remark}
The algebra $C^\infty(X) := O_X(X)$ does not in general have a $\mathbb{C}$-antilinear involution  $\bar{-} : C^\infty(X) \to C^\infty(X)$ but there does exist a canonical complex conjugation on the quotient $C^\infty(X)$ by the ideal of nilpotent sections, which is $C^\infty(X_{red}; \mathbb{C})$.
So on a complex supermanifold we have complex conjugation only on the reduced manifold.
\end{remark}


As for ordinary [[supermanifolds]] (and with same proof as in the real case), we have the following two statements.

\begin{theorem}

1. Every complex supermanifold is isomorphic to one of the form $\Pi E$.

1. The functor $C^\infty$ is [[fully faithful]]:
$$cSDiff(X,Y) \simeq  ComplexSuperAlg(C^\infty(Y), C^\infty(X)).$$

\end{theorem}
 
\begin{remark}
It turns out that a $\mathbb{C}$-super algebra homomorphism 
$$\phi : C^\infty(Y) \to C^\infty(X)$$
automatically satisfies
$$\phi_{red}(\overline{f_{red}}) = \overline{\phi_{red}(f_{red})}.$$
\end{remark}

\begin{example}
Define the complex supermanifold $\mathbb{R}_{cs}^{d|\delta}$  as $\mathbb{R}^d$
with structure sheaf $U\mapsto C^\infty(U) \otimes_{\mathbb{C}} \wedge^\bullet \mathbb{C}^\delta$.

Then for $S$ an arbitrary complex supermanifold we have
$$\mathbb{R}_{cs}^{d|\delta}(S)
= cSDiff(S, \mathbb{R}_{cs}^{d|\delta})
= \{ (x_1, \cdots, x_d, \theta_1, \cdots, \theta_{\delta})\},$$
where $x_i \in C^\infty(S)^{ev}$,
$\theta_j \in C^\infty(S)^{odd}$,
and $(x_i)_{red}$ is real: $\overline{(x_i)_{red}} = (x_i)_{red} \}$.
\end{example}

\begin{example}
For
$$\mathbb{R}^{2|1}(S)
= \{ (x,y,\theta) | x,y \in C^\infty(S)^{ev}, 
    \theta \in C^\infty(S)^{odd}; x,y real \}$$
we shall write
$$\simeq \{ (z,\bar z, \theta) | z, \bar z \in C^\infty(S)^{ev}; \overline{z_{red}}
= (\overline z )_{red} \}.$$
\end{example}

## Related concepts

* [[supermanifold]], [[complex manifold]]

* [[super Riemann surface]]


## References 

* {#DeligneMorgan1999} [[Pierre Deligne]], [[John Morgan]], Section 4.8 in: *Notes on supersymmetry*, in *[[Quantum Fields and Strings]], A course for mathematicians*, vol 1, Amer. Math. Soc. (1999) 41-98 &lbrack;[web version](http://www.math.ias.edu/qft), [[DeligneMorgan-NotesOnSusy.pdf:file]], [[DeligneMorgan-SignRule.pdf:file]]&rbrack;



[[!redirects complex supermanifolds]]
