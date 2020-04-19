\tableofcontents

\section{Introduction}

A Galois category is a category equipped with structure allowing for a construction of a 'fundamental group' from it, akin to the construction of the fundamental group of a topological space from the category of covering spaces of it. See [[Grothendieck's Galois theory]] for more on the latter.

\section{Details}

There are two ways to define a Galois category. We give them both below, following [SGA1](#SGA1).

\begin{defn} A _Galois category_ is a category equivalent to the [[classifying topos of a profinite group]]. \end{defn}

\begin{defn} A _Galois category_ is a [[category]] $G$ for which there exists a [[functor]] $F: G \rightarrow \mathsf{FinSet}$, where $\mathsf{FinSet}$ is the category [[FinSet]] of finite sets, such that the following hold.

1. $G$ has [[finite limit|finite limits]]. 
1. $G$ has [[finite colimit|finite colimits]].
1. For every arrow $f: X \rightarrow Y$ of $G$, there are objects $Z_{f}$ and $Z'_{f}$ of $G$ such that $Y$ is isomorphic to the coproduct $Z_{f} \sqcup Z'_{f}$, such that there is a [[strict epimorphism]] $u: X \rightarrow Z_{f}$, and such that the canonical [[coprojection]] functor $v: Z_{f} \rightarrow Y$ is a [[monomorphism]]. 
1. $F$ is [[exact functor|exact]], that is to say, preserves finite limits and finite colimits.
1. $F$ is [[conservative functor|conservative]]. 

\end{defn}

\begin{rmk} The original form of 2. in §4 of SGA1 is slightly weaker, and the axiom 4. was originally two axioms which together were slightly weaker than our axiom, namely that $F$ preserved finite limits, and that $F$ preserved the colimits required to exist in the weaker form of 2. However, as discussed in Remark 4.2 of SGA1, if the weaker axioms hold and the other axioms hold, then 2. and 4. as we have given them hold, so we prefer to use them for simplicity and brevity. \end{rmk}

\section{References}

* {#SGA1} _Revêtements étales et groupe fondamental (SGA 1)_, [[Alexander Grothendieck]], 1971, Springer-Verlag, vol. 224 of _Lecture notes in mathematics_.