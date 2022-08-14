
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

In [[differential topology]], given a [[pair]] $X$, $Y$ of [[smooth manifolds]], and a [[pair]] of [[parallel morphism|parallel]] [[smooth functions]] $X \underoverset{f_1}{f_0}{\rightrightarrows} Y$ between them, a _smooth homotopy_ between these is (typically defined to be) a [[left homotopy]] by a [[smooth function]], hence a [[smooth function]] $ \eta \;\colon\; X \times \mathbb{R} \longrightarrow Y$ on the [[product manifold]] of $X$ with the [[real line]],  which restricts to $f_i$ at $X \times \{i\}$, for $i \in \{0,1\} \subset \mathbb{R}$.

More generally, for $X$, $Y$ [[differentiable manifolds]] and $f_0$ and $f_1$ [[differentiable functions]], one may ask for _differentiable homotopies_, all to any given order(s) of differentiability.

## Properties

### Continuous homotopy implies smooth homotopy
  {#ContinuousHomotopyImpliesSmoothHomotopy}

\begin{proposition}
At least if $X$ and $Y$ are [[closed manifolds]], then a smooth homotopy exists between any [[pair]] of [[parallel morphism|parallel]] [[smooth functions]] $(f_0, f_1)$ between them as soon as there exists an ordinary (i.e. [[continuous function|continuous]]) [[left homotopy]] between their underlying [[continuous functions]].

More generally, if $(f_0, f_1)$ are $n+2$-fold [[differentiable function|differentiable]], then an ordinary continuous homotopy between them implies an $n$-fold differentiable homotopy.
\end{proposition} 

([Pontrjagin 55, Thm. 8, p. 41](#Pontrjagin55)))

More in detail:

\begin{proposition}
\label{SmoothRefinementOfContinuousHomotopyRelativeClosedSubset}
  Let $X$ and $Y$ by [[smooth manifolds]] where $X$ may be a [[manifold with boundary]]. If [[continuous functions]] $f,g \;\colon\; X \xrightarrow{\;} Y$ are continuously [[homotopy|homotopic]] relative to a [[closed subset]] $A \subset X$, then they are also smoothly homotopic relative to $A$ 
\end{proposition}
([Lee 2012, Thm. 10.22 (1st ed.) / Thm. 6.29 (2nd ed.)](#Lee12))

\begin{example}\label{HomotopyOfSmoothPathsRelativeToTheirEndpoints}
**(homotopy of smooth paths relative to their endpoints)**
\linebreak
  In the case that $X \,=\, [0,1]$ is the [[closed interval]] and $Y$ any smooth manifold, then Prop. \ref{SmoothRefinementOfContinuousHomotopyRelativeClosedSubset} say that continuous homotopy classes of smooth *[[paths]]* in $Y$, relative to their endpoints are equivalent to smooth such homotopy classes. This is relevant for instance for the characterization of the *[[fundamental groupoid]]* and the [[universal cover]] of a smooth manifold.
\end{example}

\begin{proposition}
  Let $X$ and $Y$ by [[smooth manifolds]], both possibly [[manifold with boundary|with boundary]]. If [[continuous functions]] $f,g \;\colon\; X \xrightarrow{\;} Y$ are continuously [[homotopy|homotopic]], then they are also smoothly homotopic  
\end{proposition}

([Lee 2012, Thm. 9.28 (2nd ed.)](#Lee12))


## Related concepts

* [[smooth isotopy]]

* [[smooth homotopy type]]

## References

* {#Pontrjagin55} {#Pontryagin55} [[Lev Pontrjagin]], _[[Smooth manifolds and their applications in Homotopy theory]]_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/pont001.pdf))

* {#Lee12} [[John Lee]], *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;


[[!redirects smooth homotopies]]
