[[frame#As sites|section link test]]

Please do not delete the following example for the moment!

An article by \cite{vandenBergGarner2011} and another by \cite{MarraReggio2020}.

\section{References}

\bibitem{MarraReggio2020}

\bibitem{vandenBergGarner2011}

\bibitem{AdámekRosícky2020}

\linebreak

\bibitem{Witten1995}

\linebreak



> With all due respect to anyone who is interested in them, they are a mess. There is a lot of detailed information known about them, but I won't try to summarize it here. ([Adams](https://www.uio.no/studier/emner/matnat/math/MAT9580/v17/documents/adams-shgh.pdf#page=212))

> Of these little is known but their name. They elude both hunters and philosophers. Let them go. I know little more of them, nor does anybody else. ([Melville](https://margot-quotes.livejournal.com/173747.html))


\linebreak

\linebreak


In [[metrology]] and [[data analysis]], where an [[observable]] is typically a [[function]] $X \overset{f}{\longrightarrow} \mathbb{R}^n$ from the given data set $X$ to the set of [[real numbers]] $\mathbb{R}^1$, or to an [[n-tuple]] of such (varying in a [[Cartesian space]] $\mathbb{R}^n$), an _iso-hypersurface_ or _level-hypersuface_ is a [[level set]] of this observable, hence the [[subset]] of $X$ consisting all those points $x \in X$ on which this observable $f$ takes the same given value $f(x) = c$. 

For example, if $X$ is a model for the Earth's atmosphere, and $f$ assigns to each point the atmospheric [[pressure]] $p(x)$ at this point, in some suitable [[physical unit]], then an iso-surface for $p$ is an _[[isobar]]_: a [[surface]] of constant pressure.

For such a [[level set]] to actually be a [[hypersurface]], hence a [[differentiable manifold]] at least to some suitable level of approximation, some minimal regularity conditions on $f$ need to be satisfied, such as that $f$ is a [[differentiable function]] to suitable degree, and, crucially, that its value $c$ (whose [[pre-image]] is formed) is a _[[regular value]]_.

Phrased this way, the construction of iso-hypersurfaces turns out to be a central topic also in areas of pure mathematics, such as in [[differential topology]] and [[cobordism theory]], where the formation of [[pre-images]] of [[regular values]] inside $\mathbb{R}^n$ is known as part of the [[Pontryagin construction]].

Curiously, this means that[[Pontryagin's theorem]] applies to iso-hypersurfaces, saying here that, as the value $c$ of the [[observable]] $f$ varies, the shape ([[topology]]) of the corresponding iso-hypersurfaces changes (at most) by a _[[cobordism]]_, and that the resulting ([[normally framed submanifold|normally framed]]) [[cobordism class]] of all these hypersurfaces corresponds to the class of $f$ in the $n$-[[Cohomotopy theory]] of the data set $X$.

While Pontryagin's theorem is ancient, the idea that it thus implies the possibility of [[topological data analysis]] via [[Cohomotopy theory]] of [[observables]] and [[cobordism theory]] of their iso-hypersurfaces appears only recently.


