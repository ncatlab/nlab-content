\tableofcontents

\section{Idea}

The counterpart to [[function extensionality]] but for [[products]]/[[pairs]] of [[elements]] $(a, b)$. Product extensionality characterizes the equality of elements in [[cartesian products]] in [[set theory]] and [[product types]] in [[type theory]]. 

\section{Definition}

\subsection{In set theory}

Product extensionality states that for all elements $a \in A$, $a' \in A$, $b \in B$, and $b' \in B$, if $a = a'$ and $b = b'$, then the ordered pairs $(a, b) = (a', b')$. 

\subsection{In type theory}

In [[intensional type theory]], [[equality]] is represented by the [[identity type]], and furthermore, there might be more than one element of the identity type in [[intensional type theory]], so a naive translation of product extensionality into intensional type theory doesn't result in the right statement. 

Instead, we have the following:

For every type $A$ and $B$ and element $a:A \times B$ and $b:A \times B$, there is a canonical function 
$$\mathrm{idtocomponentid}(a, b):a =_{A \times B} b \to \left((\pi_1(a) =_A \pi_1(b)) \times (\pi_2(a) =_B \pi_2(b))\right)$$
inductively defined by 
$$\mathrm{idtocomponentid}(a, a)(\mathrm{refl}_{A \times B}(a)) \equiv (\mathrm{refl}_{A}(\pi_1(a)), \mathrm{refl}_{B}(\pi_2(a)):\Omega(A, \pi_1(a)) \times \Omega(B, \pi_2(a))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

Product extensionality is the statement that the function $\mathrm{idtocomponentid}(a, b)$ is an [[equivalence of types]] for all elements $a:A \times B$ and $b:A \times B$:
$$\mathrm{prodext}(a, b):\mathrm{isEquiv}(\mathrm{idtocomponentid}(a, b))$$

\subsection{Definitional product extensionality}

One could replace the equivalence of types above with a [[definitional equality]] of types, resulting in definitional product extensionality, that for all types $A$ and $B$ and elements $a:A \times B$ and $b:A \times B$,
$$a =_{A \times B} b \equiv (\pi_1(a) =_A \pi_1(b)) \times (\pi_2(a) =_B \pi_2(b))$$

or equivalently, for all types $A$ and $B$ and elements $a:A$, $a':A$, $b:B$, and $b':B$, 
$$(a, b) =_{A \times B} (a', b') \equiv (a =_A a') \times (b =_B b')$$

Definitional product extensionality holds in [[cubical type theory]] and [[higher observational type theory]]. 

\section{See also}

* [[function extensionality]] (for functions)

* [[universe extensionality]] (for small types)

* [[propositional extensionality]] (for [[subsingletons]]/[[h-propositions]])

* [[axiom of extensionality]] (for pure sets)