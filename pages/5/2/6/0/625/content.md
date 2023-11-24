

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



\tableofcontents

\section{Idea} 

An _isofibration_ is, roughly speaking, a [[functor]] $F: E \rightarrow B$ between [[category|categories]] such that every [[isomorphism]] $f$ in $B$ can be 'lifted' to an isomorphism in $E$. Here 'lifted' means that there is an isomorphism $g$ in $E$ such that $F(g) = f$. 

Alternatively, an isofibration is the analogue of a [[Hurewicz fibration]] for the [[interval object]] in $\mathsf{Cat}$, the [[Cat|category of categories]], given by the [[free-standing isomorphism]]. That this definition is equivalent to the former one will be established below.

It is the second of these definitions that often generalises better to higher categories.  

\section{Definition}

\begin{defn} An **isofibration** is a [[functor]] $p:E\to B$ such that for any [[object]] $e$ of $E$ and any [[isomorphism]] $\phi:p(e) \cong b$, there exists an isomorphism $\psi:e \cong e'$ such that $p(\psi)=\phi$. \end{defn}

\begin{rmk} Equivalently: for any commutative diagram

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
I \ar[r, swap, "\phi"] & B
\end{tikzcd}

in $\mathsf{Cat}$, where $I$ is the [[free-standing isomorphism]], there is a functor $l: I \rightarrow E$ such that the following diagram in $\mathsf{Cat}$ commutes. 

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
I \ar[r, swap, "\phi"] \ar[ur, "l"] & B
\end{tikzcd}

\end{rmk}

\begin{rmk} We can picture this as follows.

$$
  \array{
    e &\stackrel{\exists \psi \in p^{-1}(\phi)}{\to} & \exists e'&&& E 
    \\
     &&&&&  \downarrow^p
    \\
    p(e) &\stackrel{\phi}{\to} & b &&& B
  }
  \,.
$$
\end{rmk}

\begin{rmk} If $p$ is a [[forgetful functor]], then being an isofibration says that whatever stuff $p$ forgets can be "transported along isomorphisms." \end{rmk}

\begin{rmk} {#NotInvariantUnderEquivalence} Notice that this definition of isofibration violates the 1-categorical [[principle of equivalence]] where it demands that $p(\psi)=\phi$ (which includes the requirement that $p(e') = b$): this condition is not invariant under [[equivalence of categories]]. If one changed the definition to involve just an [[isomorphism]] $p(\psi)\cong\phi$, then of course, any functor would qualify. But the point of isofibrations is rather to help present the [[(2,1)-category]] of categories/groupoids in terms of 1-categorical data. For more on this see below at _[As fibrations in canonical model structures](#AsFibrationsInCanonicalModelStructures)_. \end{rmk}

\section{Equivalent definition}

The following may at first seem a little surprising. It says that isofibrations have in fact a stronger lifting property, namely the analogue of that of a [[Hurewicz fibration]] with respect to the [[interval object]] in $\mathsf{Cat}$ given by the [[interval groupoid]]. This stronger lifting property is more conceptually fundamental with regard to finding the correct generalisation of isofibrations to higher categories, where 'correct' refers for instance to defining the fibrations of a [[model structure]].

\begin{prpn} Let $p: E \rightarrow B$ be a [[functor]] between categories. Then $p$ is an isofibration if and only if for every commutative diagram

\begin{tikzcd}
X \ar[r, "f"] \ar[d, swap, "id \times 0"] & E \ar[d, "p"] \\
X \times I \ar[r, swap, "g"] & B
\end{tikzcd}

in $\mathsf{Cat}$, where $I$ is the [[free-standing isomorphism]], there is a  functor $l: X \times I \rightarrow E$ such that the following diagram in $\mathsf{Cat}$ commutes. 

\begin{tikzcd}
X \ar[r, "f"] \ar[d, swap, "id \times 0"] & E \ar[d, "p"] \\
X \times I \ar[r, swap, "g"] \ar[ur, "l"] & B
\end{tikzcd}

\end{prpn}

\begin{proof} The "only if" direction is immediate. Let us demonstrate that the "if" direction holds by constructing $l$. To this end, for any object $x$ of $X$, let $l_{x}$ be the unique functor such that the following diagram in $\mathsf{Cat}$ commutes, which exists since $p$ is an isofibration. 

\begin{tikzcd}
1 \ar[r, "x"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
I \ar[r, swap, "\phi_{x}"] \ar[ur, "l_{x}"] & B
\end{tikzcd}

Here $\phi_{x}$ is the functor representing the isomorphism $g(x, i)$ of $B$, where $i$ is the arrow $0 \rightarrow 1$ of $I$.

* For any object $x$ of $X$, we define $l(0)$ to be $f(x)$, define $l(x, i)$ to be $l_{x}(i)$, define $l\left(x,i^{-1}\right)$ to be $l_{x}\left(x^{-1}\right)$, and define $l(1)$ to be $l_{x}(1)$. 
* For any arrow $r: x \rightarrow x'$ of $X$, we define $l(r,0)$ to be $f(r)$, and define $l(r, 1)$ to be $l_{x'}(i) \circ f(r) \circ l_{x}\left(i^{-1}\right)$.

It is immediately checked that $l$ is well-defined, is indeed a functor, and fits into the required commutative diagram.

\end{proof}

## Properties

### General

Isofibrations have a number of good properties.  For example, any [[strict 2-limit|strict pullback]] of an isofibration is also a [[2-limit|weak pullback]]. (This is also explained by the role of isofibrations as the fibrations in the [[canonical model structures]], see [below](#AsFibrationsInCanonicalModelStructures).)

\begin{example}\label{GrothendieckFibrationsAreIsofibrations}
Any [[Grothendieck fibration]] or opfibration is an isofibration (take the lifts to be the Cartesian lifts), but not in general conversely, unless $B$ is a [[groupoid]].
\end{example}

\begin{example}\label{GrothIsIsoFibBetweenGroupoids}
  For [[groupoids]] $\mathcal{E}, \mathcal{B} \,\in\,$ [[Grpd]], a functor $P \,\colon\, \mathcal{E} \to \mathcal{B}$ the following are equivalent:

1. $P$ is a [[Grothendieck fibration]],

1. $P$ is an [[isofibration]].

\end{example}
\begin{proof}
  The implication $IsoFib \Rightarrow GrothFib$ is Ex. \ref{GrothendieckFibrationsAreIsofibrations}. 

Conversely, if $P$ is an isofibration, it is sufficient to show that any of the lifts $f$ it provides is a [[Cartesian morphism]]. But by assumption the lift is again an [[isomorphism]], and all isomorphisms are Cartesian.

More explicitly (in the notation [there](Grothendieck+fibration#CartesianMorphism))
\begin{tikzcd}[
  sep=20pt
]
  &
  z
  \ar[
    drrr, 
    bend left=20, 
   "{ \forall \, g }"{description}
  ]
  \ar[
    dr, 
    dashed, 
    "{ 
       \exists! \, \widehat{w} 
    }"{description}
  ]
  \\
  \mathcal{E}
  \ar[dd, "{ P }"]
  &&
  x 
  \ar[
     rr, 
     "{ f }"{description},
     "{ \mathrm{cartesian} }"{swap, yshift=-1pt}
  ]  
  && 
  y
  \\
  & 
  P(z)
  \ar[drrr, bend left=20, "{ P(g) }"{description}]
  \ar[
    dr,
    "{ \forall \, w }"{description}
  ]
  \\
  \mathcal{B}
  &&
  P(x) 
  \ar[rr, "{ P(f) }"{description}]
  && 
  P(y)
\end{tikzcd}
the [[invertible morphism|invertibility]] of all morphisms implies that both $w$ and $w'$ are uniquely determined by $f$ and $g$, and then [[functor|functoriality]] of $P$ implies that indeed $P(\widehat{w}) = w$. 
\end{proof}



### As fibrations in canonical model structures
 {#AsFibrationsInCanonicalModelStructures}

The isofibrations are the _[[fibrations]]_ in the [[canonical model structure on categories]] and the [[canonical model structure on groupoids]].  More generally, the fibrations in [[canonical model structures]] on various types of higher categories are usually some generalization of isofibrations.  For example, the fibrations in the Lack model structure on 2-Cat, sometimes known as [[Lack fibration|Lack fibrations]] have "equivalence lifting" and "local isomorphism lifting," and the fibrations in the Joyal model structure for [[quasi-category|quasicategories]] have "equivalence lifting" at all levels.

Generalizing in another direction, internalized isofibrations are the fibrations in the [[2-trivial model structure]] on any finitely complete and cocomplete [[strict 2-category]].

## Related concepts

* [[amnestic isofibration]]

* [[isocofibration]]

## References

For groupoids the definition appears (called "star surjectivity" there) on p. 105 (3 of 30) in

* {#Brown70} [[Ronnie Brown]], _Fibrations of groupoids_, Journal of Algebra Volume 15, Issue 1, May 1970, Pages 103-132 doi:[10.1016/0021-8693(70)90089-X](https://doi.org/10.1016/0021-8693%2870%2990089-X), [author's pdf](http://groupoids.org.uk/pdffiles/fibrationsgpds.pdf)


[[!redirects isofibrations]]
