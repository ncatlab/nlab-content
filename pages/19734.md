\tableofcontents

\section{Introduction}

_Bertrand's postulate_, first proven by analytic methods by Chebyshev in 1852,  is one of the few simple facts providing precise bounds on the occurrence of primes. 

\section{Bertrand's postulate}

Given an integer $i \geq 1$, let $p_{i}$ denote the $i^{th}$ prime. _Bertrand's postulate_ is the following. 

\begin{thm} \label{TheoremBertrandsPostulate} For any integer $n \geq 1$, we have that $p_{n+1} \lt 2p_{n}$. \end{thm}

\begin{rmk} \label{RemarkAlternativeFormulations} There are a number of equivalent formulations of Theorem \ref{TheoremBertrandsPostulate}. One is that, for any integer $n \gt 3$, there is a prime $p$ such that $n \lt p \lt 2n$. \end{rmk}

\section{Proof given Goldbach's conjecture}

Around 2005, it was noticed by Henry J. Ricardo and Yoshihiro Tanaka that Bertrand's postulate follows from the Goldbach conjecture. We record the proof (of the formulation in Remark \ref{RemarkAlternativeFormulations}).

\begin{proof} If the Goldbach conjecture holds, there are prime numbers $p_{1}$ and $p_{2}$ such that $2n = p_{1} + p_{2}$. We must have that at least one of $p_{1}$ and $p_{2}$ is greater than or equal to $n$. Without loss of generality, suppose that $p_{1}$ has this property. 

If $n$ is not prime, then it is immediate that $n \lt p_{1} \lt 2n$, as required. Suppose instead that $n$ is prime. Then $n+1$ is composite, since it must be divisible by $2$. 

By Goldbach's conjecture once more, there are prime numbers $p_{1}'$ and $p_{2}'$ such that $2(n+1) = p_{1}' + p_{2}'$. As above, at least one of $p_{1}'$ and $p_{2}'$ must be greater than or equal to $n+1$. Without loss of generality, suppose that $p_{1}'$ has this property.

Then since $n+1$ is not prime, we have that $n+1 \lt p_{1}' \lt 2(n+1)$, and thus that $n \lt p_{1}' \lt 2(n+1)$.

Now, $p_{1}'$ is not equal to $2n+1$, for this would imply that $p_{2}'=1$, which is impossible. Moreover, $p_{1}'$ is not equal to $2n$, since $2n$ is not prime. We deduce that $p_{1}' \lt 2n$, as required. 

\end{proof} 

\section{References}

Henry J. Ricardo, _Goldbach's conjecture implies Bertrand's postulate, Amer. Math. Monthly, 112, pg. 492, 2005