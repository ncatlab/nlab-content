\tableofcontents

\section{Idea}

The counterpart to [[function extensionality]] but for [[products]]/[[pairs]] of [[elements]] $(a, b)$. Product extensionality characterizes the equality of elements in [[cartesian products]] in [[set theory]] and [[product types]] in [[type theory]]. 

\section{Definition}

\subsection{In set theory}

Product extensionality states that for all elements $a \in A$, $a' \in A$, $b \in B$, and $b' \in B$, $a = a'$ and $b = b'$ if and only if $(a, b) = (a', b')$. Product extensionality is sometimes assumed as an axiom in [[material set theory]] to make the [[pairing structure]] into an [[ordered pairing structure]] $(a, b)$. 

\subsection{In type theory}

In [[intensional type theory]], [[equality]] is represented by the [[identity type]], and furthermore, there might be more than one element of the identity type in [[intensional type theory]], so a naive translation of product extensionality into intensional type theory doesn't result in the right statement. 

Instead, we have the following:

For every type $A$ and $B$ and element $a:A \times B$ and $b:A \times B$, there is a canonical function 
$$\mathrm{idtoprojectionids}(a, b):a =_{A \times B} b \to \left((\pi_1(a) =_A \pi_1(b)) \times (\pi_2(a) =_B \pi_2(b))\right)$$
inductively defined by 
$$\mathrm{idtoprojectionids}(a, a)(\mathrm{refl}_{A \times B}(a)) \equiv (\mathrm{refl}_{A}(\pi_1(a)), \mathrm{refl}_{B}(\pi_2(a)):\Omega(A, \pi_1(a)) \times \Omega(B, \pi_2(a))$$
where $\Omega(A, a)$ is the [[loop space type]] $a =_A a$ of $A$ at $a:A$. 

Product extensionality is the statement that the function $\mathrm{idtoprojectionids}(a, b)$ is an [[equivalence of types]] for all elements $a:A \times B$ and $b:A \times B$:
$$\mathrm{prodext}(a, b):\mathrm{isEquiv}(\mathrm{idtoprojectionids}(a, b))$$

\subsection{Definitional product extensionality}

One could replace the equivalence of types above with a [[definitional equality]] of types, resulting in definitional product extensionality, that for all types $A$ and $B$ and elements $a:A \times B$ and $b:A \times B$,
$$a =_{A \times B} b \equiv (\pi_1(a) =_A \pi_1(b)) \times (\pi_2(a) =_B \pi_2(b))$$

or equivalently, for all types $A$ and $B$ and elements $a:A$, $a':A$, $b:B$, and $b':B$, 
$$(a, b) =_{A \times B} (a', b') \equiv (a =_A a') \times (b =_B b')$$

Definitional product extensionality holds in [[cubical type theory]] and [[higher observational type theory]]. 

\section{See also}

* [[extensionality]]

\section{References}

For definitional product extensionality in higher observational type theory, see

* [[Mike Shulman]], *Towards a Third-Generation HOTT Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

For a proof that the given function above between identity types is a [[quasi-inverse function]] in [[intensional type theory]], see section 2.6:

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))