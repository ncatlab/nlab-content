\tableofcontents

\section{Idea}

Given a [[curve]] $X$ in [[algebraic geometry]] over some field $F$, especially some kind of [[number field]], the field of moduli of $X$ with respect to $F$ is, roughly speaking, the largest field invariant under those automorphisms of $\overline{F}$, the algebraic closure of $F$, which do not change $X / \overline{F}$. 

Automorphisms of $\overline{F}$ which fix $F$ are fundamental in [[Galois theory]], forming the [[absolute Galois group]] of $F$, and indeed in mathematics generally: the absolute Galois group of the [[rational number|rational numbers]] is a very deep object, for example. Considering a curve over its field of moduli is a kind of geometric analogue of this. 

\section{Definition}

There are slightly different ways to give a precise definition. We choose the following formulation (see \cite{Mochizuki2015} for example, although the notion goes back at least to the era of [[André Weil]]).  

\begin{defn} \label{DefinitionFieldOfModuli} Let $X$ be a [[curve]] in the sense of algebraic geometry, defined over a [[field]] $F / \mathbb{Q}$. Given an automorphism $\sigma$ of $\overline{F}$, one can ask that the [[scheme]] $X_{\overline{F}} = X \times_{F} \overline{F}$ (where the projection morphisms are the obvious ones) is isomorphic to the [[base change]] of $X_{\overline{F}}$ along $\sigma$. The _field of moduli_ of $X$ with respect to $F$ is the sub-field of $\overline{F}$ fixed by all such automorphisms  $\sigma$ which belong to the [[Galois group]] $Gal\left(\overline{F} / \mathbb{Q} \right)$, namely which fix $\mathbb{Q}$. \end{defn}

\begin{rmk} The field of moduli of $X$ with respect to $F$ is a finite extension of $F$. \end{rmk}

\begin{rmk} A curve $X$ over $F$ need not be definable over $F_{mod}$, that is, there may not exist any scheme over $F_{mod}$ which is isomorphic to $X_{\overline{F}}$ after base change along the canonical morphism $\overline{F} \rightarrow F_{mod}$. \end{rmk}

\section{References} 

Definition \ref{DefinitionFieldOfModuli} is 5.1 (ii) in the following. 

\bibitem{Mochizuki2015}
