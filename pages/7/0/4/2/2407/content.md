
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
__Propositional logic__, also called __$0$th-order logic__ and __sentential logic__, is that part of [[logic]] that deals only with [[propositions]] with no [[bound variables]].  

Compare [[predicate logic]], or $1$st-order logic, and [[higher-order logic]].  Note that while one can have *free* variables in $0$th-order logic, one cannot really do anything with them; each $P(x)$ in a $0$th-order proposition might as well be thought of as atomic.

This can be understood more cleanly in the language of many-sorted logic, where each variable has to have a specified sort.
Then ordinary predicate logic has exactly one sort, usually unnamed.
Propositional logic is for a signature with no sorts, hence no variables at all.

A __propositional calculus__, also called __sentential calculus__, is simply a system for describing and working with propositional logic.  The precise form of such a calculus (and hence of the logic itself) depends on whether one is using [[classical logic]], [[intuitionistic logic]], [[linear logic]], etc; see those articles for details.

## Notation

* $\wedge$ The [[propositional logic]] conjunction, or AND [[operator]]. For formula, $\phi,\psi$,

\begin{theorem} 
$\phi \wedge \psi = \neg (\neg \phi \vee \neg \psi)$
\end{theorem}

* $\vee$ The [[propositional logic]] inclusive dysjunction, or OR [[operator]].

* $\veebar$ The [[propositional logic]] exclusive dysjunction, or XOR [[operator]].

* $\Rightarrow$ The [[propositional logic]] implication, conditional, or implies [[operator]]. For formula,
$\phi, \psi$, 

\begin{theorem} $\phi \Rightarrow \psi = \neg \phi \vee \psi$ \end{theorem}

* $\Leftrightarrow$ The [[propositional logic]] equivalence, biconditional, or equals [[operator]]. For formula $\phi, \psi$,

\begin{theorem} $\phi \Leftrightarrow \psi = \phi \Rightarrow \psi \wedge \psi \Rightarrow \phi$ 
\end{theorem}

## Related concepts

* [[logic]]

  * **propositional logic** (0th order)

  * [[predicate logic]] (1st order)

  * [[higher order logic]]

  * [[modal logic]]

  * [[propositional logic as a dependent type theory]]

[[!redirects propositional logic]]
[[!redirects propositional calculus]]
[[!redirects 0th-order logic]]
[[!redirects 0-th-order logic]]
[[!redirects zeroth-order logic]]
[[!redirects zeroeth-order logic]]
[[!redirects 0th order logic]]
[[!redirects 0-th order logic]]
[[!redirects zeroth order logic]]
[[!redirects zeroeth order logic]]
[[!redirects sentential logic]]
[[!redirects sentential calculus]]
[[!redirects sentensial logic]]
[[!redirects sentensial calculus]]

[[!redirects propositional logics]]
