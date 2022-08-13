
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given an [[endofunctor]] $F$ such that the [[category]] of [[algebra for an endofunctor|$F$-algebras]] has an [[initial object]] $(\mu F, in)$, the *catamorphism* for an $F$-algebra $(A, \varphi)$ is the unique [[homomorphism]] from the [[initial algebra of an endofunctor | initial $F$-algebra]] $(\mu F, in)$ to $(A, \varphi)$. The unique morphism between the carriers is also denoted $cata \varphi : \mu F \rightarrow A$.

From the commuting square of the homomorphism, we have $(cata \varphi) \circ in = \varphi \circ F (cata \varphi)$. By [[initial algebra of an endofunctor#LambeksTheorem|Lambek's theorem]], $\mathit{in}$ has an inverse $\mathit{out}$, so the catamorphism can be recursively defined by $cata \varphi = \varphi \circ F (cata \varphi) \circ out$.

\begin{centre}
\begin{tikzcd}
F (\mu F)
  \arrow[r, "F (\textrm{cata}\:\varphi)"]
  \arrow[d, "\textrm{in}"] &
F A
  \arrow[d, "\phi"] \\
\mu F
  \arrow[r, "\textrm{cata}\:\varphi"] &
A
\end{tikzcd}
\end{centre}

## Properties

### Fusion law

\begin{lemma}
Let $h: A \rightarrow B$ be a homomorphism between two F-algebras $\varphi: F A \rightarrow A$ and $\psi: F B \rightarrow B$ so that $h \circ \varphi = \psi \circ F h$. Then $h \circ cata \varphi = cata \psi$.
\end{lemma}

\begin{centre}
\begin{tikzcd}
F (\mu F)
  \arrow[r, "F (\textrm{cata}\:\varphi)"]
  \arrow[d, "\textrm{in}"] &
F A
  \arrow[r, "F h"]
  \arrow[d, "\varphi"] &
F B
  \arrow[d, "\psi"] \\
\mu F
  \arrow[r, "\textrm{cata}\:\varphi"] &
A \arrow[r, "h"] &
B
\end{tikzcd}
\end{centre}

## As a recursion scheme

If $\mu F$ is an inductive type, then the catamorphism is a fold over the type. Some recursive functions can then be implemented in terms of a catamorphism.

### Example: Natural numbers

Let $F$ be the functor $F X = 1 + X$ so that the naturals $\mathbb{N} = \mu F$ are represented by the fixed point of $F$ (i.e. the carrier of the initial F-algebra). The recursor for the naturals can then be defined by a catamorphism.

$$
\begin{array}{l l}
natrec &: \forall A. A \rightarrow (A \rightarrow A) \rightarrow \mathbb{N} \rightarrow A \\
natrec & A z s = cata \varphi, where \\
& \varphi (inl \ast) = z \\
& \varphi (inr n) = s n
\end{array}
$$

## References

* HaskellWiki, [Catamorphisms](https://wiki.haskell.org/Catamorphisms)

* Wikipedia, [Catamorphism](https://en.wikipedia.org/wiki/Catamorphism)

* {#BirdMoor1997} [[Richard Bird]], [[Oege de Moor]] (1997), [_Algebra of Programming_](http://www.cs.ox.ac.uk/publications/books/algebra/), Prentice Hall

* {#Fokkinga1992} [[Maarten M. Fokkinga]] (1992), [_Law and Order in Algorithmics_](https://research.utwente.nl/en/publications/law-and-order-in-algorithmics), PhD thesis, University of Twente

* {#BackhouseBruinMalcolmVoermansWoude1991} [[Roland C. Backhouse]], [[Peter J. de Bruin]], [[Ed Voermans]], [[Jaap van der Woude]] (1991), [_Relational Catamorphisms_](https://research.tue.nl/en/publications/relational-catamorphisms-2), Computing Science Notes, Vol. 9111, Technische Universiteit Eindhoven

[[!redirects catamorphisms]]