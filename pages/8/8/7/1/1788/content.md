

## Idea

In [[quantum physics]] and specifically in [[quantum information theory]], the *principle of deffered measurement* is a [[theorem]] which says that 

* any [[quantum circuit]] involving [[quantum measurement]] of some of the [[qbits]] followed by [[quantum gates]] [[controlled quantum gate|controlled]] by the respective measurement outcomes 

is equivalent ([[equality|equal]] as a [[function]] from given input to output [[data types]]) as

* a [[quantum circuit]] in which all [[quantum measurement]] happens "at the end", i.e. where no [[quantum gates]] are [[controlled quantum gate|controlled]] by previous measurement results.

The principle can be useful in practice for optimizing [[quantum circuits]]. It also clearly relates to the issue of [[interpretations of quantum mechanics]]: Since it is the [[collapse of the wavefunction]] upon [[quantum measurement]] which makes the [[interpretation of quantum mechanics]] subtle, it is interesting to note that this collapse may be (arbitrarily) deferred, in a precise sense.

***

\begin{center}
\begin{tikzcd}
X\times X \arrow[d, "f\times f"'] \arrow[r, "\displaystyle\mu_{X}"] & X \arrow[d, "f"] \\
Y\times Y \arrow[r, "\displaystyle\mu_{Y}"']                        & Y               
\end{tikzcd}
\end{center}
\begin{center}
\begin{tikzcd}
X\times X \arrow[d, "f\times f"'] \arrow[r, "\mu_{X}"] & X \arrow[d, "f"] \\
Y\times Y \arrow[r, "\mu_{Y}"']                        & Y               
\end{tikzcd}
\end{center}
[[MeasurementViaWriterComonad-221026.jpg:file]]

\begin{tikzcd}
  \mathcal{C}
  \ar[
    from=r,
    "{ U }"{description}
  ]
  \ar[
    r,
    shift left=14pt,
    "{ F }"
  ]
  \ar[
    r,
    shift left=8pt,
    phantom,
    "{ \scalebox{.7}{$\bot$} }"
  ]
  &
  \mathcal{D}
  \simeq
  \mathrm{EM}(\mathrm{ U \circ F })
\end{tikzcd}

[[ANDGates-221026.jpg:file]]

[[QuantumCircuitScheme-221025c.jpg:file]]

[[DefinitelyRandomlyViaPossiblyNecessarily.jpg:file]]

[[MeasurementViaWriterComonad-221025b.jpg:file]]

[[ContingentTypesAsPossibilityActions-201024.jpg:file]]

\begin{example}
**(matrix multiplication as Kleisli composition)**
\linebreak
  For

  * $k$ a [[field]]

  * $B$ be a [[finite set]]

  consider the [[base change]] [[adjoint triple]] of $B$-[[indexed sets]] of $k$-[[vector spaces]] ($k$-[[vector bundles]] over $B$):

\begin{tikzcd}
  k\mathrm{Vec}_B
  \ar[
    r,
    shift left=18pt,
    "{ (p_B)_! }"
  ]
  \ar[
    from=r, 
    "{ (p_B)^\ast }"{description}
  ]
  \ar[
    r,
    shift right=18pt,
    "{ (p_B)_\ast }"{swap}
  ]
  \ar[
    r,
    phantom,
    shift left=10pt,
    "{ \scalebox{.65}{$\bot$} }"
  ]
  \ar[
    r,
    phantom,
    shift right=10pt,
    "{ \scalebox{.65}{$\bot$} }"
  ]
  &
  k\mathrm{Vec}
  \mathrlap{\,.}
\end{tikzcd}

By the assumption that $B$ is [[finite set|finite]] and since [[Vect]] has [[biproducts]], the [[colimit]]/[[coproduct]] 

$$
  (p_B)_! \mathscr{V}_\bullet 
  \;=\; 
  \coprod_{b : B} \mathscr{V}_b
$$

and the [[limit]]/[[product]]

$$
  (p_B)_\ast \mathscr{V}_\bullet 
  \;=\; 
  \prod_{b : B} \mathscr{V}_b
$$

agree (we have an [[ambidextrous adjunction]]) and are both equivalent to the [[direct sum]]:

$$
  (p_B)_! \mathscr{V}_\bullet 
    \;\simeq\;
  (p_B)_\ast \mathscr{V}_\bullet 
  \;=\;
    \underset{b \colon B}{\bigoplus}
  \mathcal{V}_b
  \,.
$$

Accordingly, the underlying [[endofunctors]] of the induced [[monad]] and [[comonad]] on $k Vec_B$ 

$$
  \Box_B
  \;\coloneqq\;
  (p_B)^\ast (p_B)_\ast
  \;\;\vdash\;\;
  \lozenge_B
  \;\coloneqq\;
  (p_B)^\ast (p_B)_!
  \;\;\colon\;\;
  k Vec_B
  \longrightarrow
  k Vec_B
$$

agree, to make a [[self-adjoint functor]]

$$
  (p_B)^\ast
  \bigotimes_B 
  \;\;\vdash\;\; 
  (p_B)^\ast
  \bigotimes_B
  \;\;\;\colon\;\;\;
  k Vec
  \longrightarrow 
  k Vec
$$

which carries the [[structure]] both of a [[monad]] and of a [[comonad]].

We claim that 

1. the categories of

   1. [free $(p_B)^\ast \oplus_B$-algebras](algebra+over+a+monad#FreeAlgebras) 

   1. co-free $(p_B)^\ast \oplus_B$-coalgebras 

   are both [[equivalence of categories|equivalent]] to the categories of $k$-vector spaces.

1. where

   1. the [[Kleisli category]] of $\bigoplus_B$ exhibits such linear maps as $B$-[[tuples]] of *columns* of $B \times B$-block [[matrices]];

   1. the [[coKleisli category]] of $\bigoplus_B$ exhibits such linear maps as $B$-[[tuples]] of *rows* of $B \times B$-block [[matrices]]

  with (co)[[Kleisli composition]] expressing the operation block-[[matrix multiplication]].

In particular, on the (co)free algebras of the form $\bigotimes_B (p_B)^\ast k$ this statement holds in the sense of actual $B \times B$-matrices with entries in $k$ (as opposed to block matrices).

Since every [[linear map]] admits *some* $B \times B$-block matrix representation, the second statement implies the first by the Kleisli theorem (see [here](Kleisli+category#InTermsOfKleisliMorphisms)). 

Moreover, the second statement follows by direct inspection of the [[Kleisli morphisms]] (and [[formal duality|dually]] for the [[coKleisli morphisms]]):

For this, identify a [[coKleisli morphism]]

$$
  b \colon B
  \;\;
    \vdash
  \;\;
  \Big(
    \underset{b' \colon B}{\bigoplus}
    \mathscr{V}_{b'}
  \Big)
  \xrightarrow{\; A_b \;}
  \mathscr{W}_b
$$

with the $B$-tuple of "block $B \times 1$" matrices $(A_b)_{b \colon B}$ that it evidently encodes. 

Observe that the comultiplication on the $\bigotimes_B$-[[comonad]] is given by the [[diagonal map]] into the [[biproduct]], coming from the "randomness unit" (terminology from [modal quantum logic](necessity+and+possibility#ModalQuantumLogic)):

\begin{imagefromfile}
    "file_name": "QCwthLHT-QuantumModalUnits-221021b.jpg",
    "width": "750",
    "unit": "px",
    "margin": {
        "top": -10,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

This readily shows that the Kleisli construction indeed sends such $B$-tuples $(A_b)_{b \colon B}$ of block-matrix rows to the linear map given by the corresponding full matrix, and that the [[Kleisli composite]] with any other

$$
  b \colon B
  \;\;
    \vdash
  \;\;
  \Big(
    \underset{b' \colon B}{\bigoplus}
    \mathscr{W}_{b'}
  \Big)
  \xrightarrow{\; B_b \;}
  \mathscr{Z}_b
$$

is indeed the row-decomposition of the corresponding [[matrix product]]:

\begin{tikzcd}
  b : B
  \;\;\vdash\;\;
  &
  \Big(
    \underset{b' \!\colon\! B}{\bigoplus}
    \,
    \mathcal{V}_{b'}
  \Big) 
  \ar[
    rr,
    "{ 
      v 
      \;\mapsto\; 
      \underset{ b'' \!\colon\! B }{\sum}
      \,
      v_{b''}
    }"
  ]
  \ar[
    rrrr,
    bend right=14,
    "{
      v 
      \;\mapsto\; 
      \underset{ b'' \!\colon\! B }{\sum}
      \,
      A_{b''}(v)
      \;=\;
      A(v)
    }"{swap}
  ]
  \ar[
    rrrrrr,
    bend right=25,
    "{
      v 
      \;\mapsto\; 
      \big(B \circ A(v)\big)_b
    }"{swap}
  ]
  &&
  \Big(
    \underset{b'' \!\colon\! B}{\bigoplus}  
    \;
    \underset{b' \!\colon\! B}{\bigoplus}
    \,
    \mathcal{V}_{b'}
  \Big)
  \ar[
    rr,
    "{  
       \underset{b'' \colon B}{\bigoplus}
       \,
       A_{b''}
     }"
  ]
  &&
  \Big(
    \underset{b'' \colon B}{\bigoplus}
    \,
    \mathcal{W}_{b''}
  \Big)  
  \ar[
    rr,
    "{ B_b }"
  ]
  &&
  \mathcal{Z}_{b}
  \\
\end{tikzcd}

Dually:

\begin{tikzcd}
  b \!\colon\! B
  \;\;\vdash
  &
  \mathcal{V}_b
  \ar[
    rr,
    "{ 
      A_b
    }"
  ]
  \ar[
    rrrrrr,
    bend right=25,
    "{
      v_b
      \;\mapsto\;
      \big(
        B \cdot A_b(v_b)
      \big)
    }"{swap}
  ]
  &&
  \big(
  \underset{
    b'' \!\colon\!\! B
  }{
    \bigoplus
  }
  \mathcal{W}_{b''}
  \big)
  \ar[
    rr,
    "{
      \underset{b'' \!\colon\!\! B}{\bigoplus}
      B_{b''}
    }"
  ]
  \ar[
    rrrr,
    bend right=14,
    "{
      v
      \;\mapsto\;
      \underset{b'' \!\colon\!\! B}{\sum} 
      B_{b''}(v)
      \;=\;
      B(v)
    }"{swap}
  ]
  &&
  \big(
  \underset{
    b'' \!\colon\! B
  }{
    \bigoplus
  }
  \;
  \underset{
    b' \!\colon\! B
  }{
    \bigoplus
  }
  \mathcal{Z}_{b'}
  \big)
  \ar[
    rr, 
    "{
      \underset{b'' \!\colon\!\! B}{\oplus}
      v_{b''}
      \;\mapsto\;
      \underset{b'' \!\colon\!\! B}{\sum}
      v_{b''}
    }"
  ]
  &&
  \big(
  \underset{
    b' \!\colon\!\! B
  }{
    \bigoplus
  }
  \mathcal{Z}_{b'}
  \big)
\end{tikzcd}

\end{example}


[[QCwthLHT-QBitStatePreparationCondt-221021.jpg:file]]

[[QCwthLHT-QBitStatePreparation-221021.jpg:file]]

[[QCwthLHT-BellStatePreparation-221021.jpg:file]]

[[TheFourModalitiesOfBaseChange-20221021.jpg:file]]

[[QCwthLHT-QuantumGates-221021.jpg:file]]

[[QCwthLHT-QuantumModalUnits-221021b.jpg:file]]

\begin{tikzcd}
  \mathcal{C}^B
  \ar[
    r,
    shift left=14pt,
    "{ \coprod_B }"
  ]
  \ar[
    from=r,
    "{ \mathrm{cnst}_B }"{description}
  ]
  \ar[
    r,
    shift right=14pt,
    "{ \prod_B }"{swap}
  ]
  \ar[
    r,
    phantom,
    shift left=8pt,
    "{ \scalebox{.7}{$\bot$} }"
  ]
  \ar[
    r,
    phantom,
    shift right=8pt,
    "{ \scalebox{.7}{$\bot$} }"
  ]
  &
  \mathcal{C}
\end{tikzcd}


\begin{tikzcd}
  \mathrm{LinType}_{B}
  \ar[
    rr,
    shift left=12pt,
    "{ (p_B)_! }"
  ]
  \ar[
    from=rr,
    "{ (p_B)^\ast }"{description}
  ]
  \ar[
    rr,
    shift right=12pt,
    "{ (p_B)_\ast }"{swap}
  ]
  &&
  \mathrm{LinType}
\end{tikzcd}


$$
  \array{
  &
  (p_B)_\ast
  \big(
    (p_B)^\ast 
    (p_B)_! \mathscr{H}_\bullet
    \xrightarrow{\phantom{-}f\phantom{-}}
    \mathscr{H}_\bullet
  \big)
  \\
  \;=\;
  &
  (p_B)_\ast (p_B)^\ast \mathscr{H}
  \xrightarrow{ (p_{B})_\ast }
  \mathscr{H}
  \\
  \;\leftrightarrow\;
  &
  \mathscr{H}
  \xrightarrow{ \widetilde{(p_{B})_\ast} }
  Read_B \mathscr{H}
  }
$$


\begin{theorem} {#Ref}
\end{theorem}

\begin{remark} \label{t-a} {#Ref-A}
\end{remark}

\ref{t-a}

\ref{Ref-A}

\begin{equation}
\label{equation-Label}
a + b = c
\end{equation}

Eq: \eqref{equation-Label}

X: \ref{ItemA}
Y: \ref{AItemA}

[A link](#Item-A)

* {#Item-A} Item A
* {#ItemB} Item B

&#246;

$\act$

1. a

   1. aa

   1. ab

   1. ac

1. b

\begin{center}
\begin{tikzcd}
                                                                             & {} \arrow[dd, "\alpha"', Rightarrow] & {} \arrow[dd, "\beta", Rightarrow] &      \\
\mathrm{Mag} \arrow[rrr, "(-)^2"', bend right=60] \arrow[rrr, "(-)^3", bend left=60] &                                      &                                    & \mathrm{Set} \\
                                                                             & {}                                   & {}                                 &     
\end{tikzcd}
\end{center}


