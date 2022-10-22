[[!redirects co-Kleisli category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


[[formal dual|Formally dually]] to how a [[monad]] has a [[Kleisli category]] so also a [[comonad]] $P \colon \mathcal{C}\to\mathcal{C}$ has a (co-)Kleisli category: its [[objects]] are the objects of $\mathcal{C}$, a [[morphism]] $f \colon c_1 \to c_2$ in the co-Kleisli category is a morphism

$$
  \tilde f \colon P(c_1) \longrightarrow c_2
$$

in $\mathcal{C}$, and the composition of two such in the co-Kleisli category is represented by the morphism in $\mathcal{C}$ given by

$$
  \widetilde{f_2 \circ f_1}
  \colon
  P(c_1) \longrightarrow P(P(c_1)) \stackrel{P(\tilde f_1)}{\longrightarrow}
  P(c_2) \stackrel{\tilde f_2}{\longrightarrow}
  c_3
 \,.
$$

## Examples
 {#Examples}



### General 

\begin{example}
For an [[idempotent comonad]] the co-Kleisli category is the [[coreflective subcategory]] of its [[modal types]].
\end{example}

\begin{example}\label{CallByNameProgramming}
In [[type theory|typed]] [[functional programming]],
the Kleisli category of a comonad can be used to model [[call-by-name]] programming languages.
Dually, the [[Kleisli category]] of a monad may be used to model [[call-by-value]]-programming, see [there](Kleisli+category#CallByValueProgramming).

Generally, see at *[[monad (in computer science)]]* for more on this.
\end{example}


### Specific

\begin{example}\label{MatrixmultiplicationAsCoKleisliComposition}
**([[matrix multiplication]] as (co-)Kleisli composition)**
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

   are both [[equivalence of categories|equivalent]] to the category [[Vect|$k Vec$]] of $k$-vector spaces,

1. where:

   1. the [[Kleisli category]] of $\bigoplus_B$ exhibits such linear maps as $B$-[[tuples]] of *columns* of $B \times B$-block [[matrices]];

   1. the [[coKleisli category]] of $\bigoplus_B$ exhibits such linear maps as $B$-[[tuples]] of *rows* of $B \times B$-block [[matrices]]

  with (co)[[Kleisli composition]] expressing the operation of block-[[matrix multiplication]].

In particular, on the (co)free algebras of the form $\bigotimes_B (p_B)^\ast k$ this statement holds in the sense of actual $B \times B$-matrices with entries in $k$ (as opposed to block matrices).

Since every [[linear map]] admits *some* $B \times B$-block matrix representation, the second statement implies the first by the Kleisli theorem (see [here](Kleisli+category#InTermsOfKleisliMorphisms)). 

Moreover, the second statement follows by direct inspection of the [[Kleisli morphisms]] (and [[formal duality|dually]] for the [[coKleisli morphisms]]):

For this, identify a [[coKleisli morphism]] (where our notation now borrows from [[dependent linear type theory]] in order to express morphisms between $B$-[[indexed sets]] of vector spaces)

$$
  b \colon B
  \;\;
    \vdash
  \;\;
  \Big(
    \underset{b' \colon B}{\bigoplus}
    \mathscr{V}_{b'}
  \Big)
  \xrightarrow{\; F_b \;}
  \mathscr{W}_b
$$

with the $B$-tuple of "block $B \times 1$" matrices $(F_b)_{b \colon B}$ that it evidently encodes. 

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

Using this, one readily sees that the Kleisli construction indeed sends such $B$-tuples $(F_b)_{b \colon B}$ of block-matrix rows to the linear map $F$ which is given by the corresponding full matrix, and that the [[Kleisli composite]] with any other

$$
  b \colon B
  \;\;
    \vdash
  \;\;
  \Big(
    \underset{b' \colon B}{\bigoplus}
    \mathscr{W}_{b'}
  \Big)
  \xrightarrow{\; G_b \;}
  \mathscr{Z}_b
$$

is indeed the row-decomposition of the corresponding [[matrix product]]:

\begin{tikzcd}
  b : B
  \;\;\vdash
  &[-10pt]
  \Big(
    \underset{b' \!\colon\!\! B}{\bigoplus}
    \,
    \mathcal{V}_{b'}
  \Big) 
  \ar[
    rr,
    "{ 
      v 
      \;\mapsto\; 
      \underset{ b'' \!\colon\!\! B }{\sum}
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
      \underset{ b'' \!\colon\!\! B }{\sum}
      \,
      F_{b''}(v)
      \;=\;
      F(v)
    }"{swap}
  ]
  \ar[
    rrrrrr,
    bend right=25,
    "{
      v 
      \;\mapsto\; 
      \big(G \circ F(v)\big)_b
    }"{swap}
  ]
  &&
  \Big(
    \underset{b'' \!\colon\!\! B}{\bigoplus}  
    \;
    \underset{b' \!\colon\!\! B}{\bigoplus}
    \,
    \mathcal{V}_{b'}
  \Big)
  \ar[
    rr,
    "{  
       \underset{b'' \!\colon\!\! B}{\bigoplus}
       \,
       F_{b''}
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
    "{ G_b }"
  ]
  &&
  \mathcal{Z}_{b}
  \\
\end{tikzcd}

The [[formal duality|formally dual]] argument (now using the "definiteness counit") shows the analogous statement for Kleisli morphisms and column-decomposition of block matrices:

\begin{tikzcd}
  b \!\colon\! B
  \;\;\vdash
  &
  \mathcal{V}_b
  \ar[
    rr,
    "{ 
      F_b
    }"
  ]
  \ar[
    rrrrrr,
    bend right=25,
    "{
      v_b
      \;\mapsto\;
      \big(
        G \cdot F_b(v_b)
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
      G_{b''}
    }"
  ]
  \ar[
    rrrr,
    bend right=14,
    "{
      v
      \;\mapsto\;
      \underset{b'' \!\colon\!\! B}{\sum} 
      G_{b''}(v)
      \;=\;
      G(v)
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

\begin{example}
For $P= Jet$ a [[jet comonad]], then morphisms in its coKleisli category are [[differential operators]] (see [there](jet+comonad#Marvan86)).
\end{example}

## Related concepts

* [[Kleisli category]]
* [[Eilenberg-Moore category]]
* [[monad (in computer science)]]


## References

The [[equivalence of categories]] between the [[co-Kleisli category]] over a given [[comonad]] with the [[Kleisli category]] of an [[adjoint functor|adjoint]] [[monad]] (if it exists):

* [[Mark Kleiner]],  *Adjoint monads and an isomorphism of the Kleisli categories*, Journal of Algebra
Volume **133** 1 (1990) 79-82 &lbrack;<a href="https://doi.org/10.1016/0021-8693(90)90069-Z">doi:10.1016/0021-8693(90)90069-Z</a>&rbrack;


Some introductory material on [[comonads]], [[coalgebras]] and [[co-Kleisli morphisms]]:

* [[Paolo Perrone]], _Notes on Category Theory with examples from basic mathematics_, Chapter 5. ([arXiv](http://arxiv.org/abs/1912.10642))


[[!redirects co-Kleisli categories]]
[[!redirects coKleisli category]]
[[!redirects coKleisli categories]]
[[!redirects Kleisli category of a comonad]] 
[[!redirects Kleisli category for a comonad]] 

[[!redirects co-Kleisli morphism]]
[[!redirects co-Kleisli morphisms]]

[[!redirects coKleisli morphism]]
[[!redirects coKleisli morphisms]]


