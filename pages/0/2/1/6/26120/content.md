
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[costate comonads]] are typically discussed on [[cartesian closed categories]] but, of course, the analogous construction exists on any [[closed monoidal category]]. An immediate non-cartesian example is a [[category of vector spaces]]. At least for a [[finite-dimensional vector space]] $\mathscr{H}$, the *linear $\mathscr{H}$-costate comonad* neatly reflects some core structure of [[quantum observables]] in [[quantum physics]] with [[finite-dimensional Hilbert spaces]], as discussed below. Due to this fact and the general broad identification of (multiplicative) [[linear logic]] with a form of [[quantum logic]], the linear costate comonad may deserve to be called the *quantum costate comonad* (cf. the similar situation for the *[[quantum reader monad]]*).


## Preliminaries

We consider the category $Mod_{\mathbb{C}}$ of [[complex vector spaces]] with, as usual:

* [[monoidal category|monoidal structure]] given by the [[tensor product of vector spaces]],

* [[tensor unit]]$\;$ $\mathbb{1} \,\equiv\, \mathbb{C}$ the [[complex numbers]] themselves,

* [[internal hom]]$\;$ $\mathscr{H} \multimap \mathscr{H}'$ the vector space of [[linear maps]].

Throughout the following we fix

\[
  \label{TheFinDimHilbertSpace}
  \mathscr{H} \,\in\, FinDimMod_{\mathbb{C}} \hookrightarrow Mod_{\mathbb{C}}
\] 

a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]]. 

For notational purposes only (at this point) we choose on $\mathscr{H}$:

1. a [[Hermitian form|Hermitian]] [[inner product]] $\left\langle\cdot \vert \cdot\right\rangle$, hence as a [[finite-dimensional Hilbert space]] and use [[bra-ket]] notation to denote the generic elements of $\mathscr{H}$ by 

   $$
     \left\vert \psi \right\rangle
     \,\equiv\,
     \psi \,\in\, \mathscr{H}
   $$

   and those of its [[linear dual space]]

   $$
     \mathscr{H}^\ast
     \,\equiv\,
     \mathscr{H} \multimap \mathbb{1}
   $$

   by 
 
   $$
     \left\langle \phi \right\vert
     \,\equiv\,
     \left\langle \psi \vert (\text{-}) \right\rangle
     \,\in\,
     \mathscr{H}^\ast
   $$

1. an [[orthonormal linear basis]] $\big(\left\vert w \right\rangle \,\in\, \mathscr{H} \big)_{w \colon W}$, hence such that

   \[
     \label{OrthonormalBasis}
     w,w' \,\colon\, W
     \;\;\;\;
       \vdash
     \;\;\;\;
     \left\langle w \vert w' \right\rangle
     \,=\,
     \delta_{w, w'}
   \]

   ([[Kronecker delta]]).

Furthermore, for $\psi \in \mathscr{H}$, $\phi \in \mathscr{K}$ we leave the [[tensor product]]-symbol implicit in

$$
  \left\vert \psi \right\rangle
  \left\langle \phi \right\vert
  \;\;
    \equiv
  \;\;
  \psi 
    \otimes 
  \left\langle \phi \vert \text{-} \right\rangle
  \;\;
  \in
  \;\;
  \mathscr{H} \otimes \mathscr{K}^\ast
  \,.
$$

In this [[bra-ket]]-notation, the 
[[compact closed category|compact closure]] for [[finite-dimensional vector space|finite-dimensional]] $\mathscr{H}$ (see [there](finite-dimensional+vector+space#CompactClosure)) is witnessed by the following [[isomorphism]]

\[
  \label{CompactClosureViaBraKetNotation}
  \array{
    \Big(
      \mathscr{H}
      \multimap
      \mathscr{H}'
    \Big)
    &\overset{\;\; \sim \;\;}{\longrightarrow}&
    \mathscr{H}' \otimes \mathscr{H}^\ast
    \\
    \Big(
      \left\vert w \right\rangle
      \,\mapsto\,
      \underset{w'}{\sum}
      \left\vert w' \right\rangle
      \cdot
      A_{w', w}
    \Big) 
    &\mapsto&
      \underset{w,w'}{\sum} 
      \left\vert w' \right\rangle
      A_{w', w}
      \left\langle w \right\vert
    \mathrlap{\,.}
  }
\]



## The Linear CoState comonad

The [[internal hom]]-[[adjoint functor|adjunction]] for $\mathscr{H}$ (eq:TheFinDimHilbertSpace)

$$
  Mod_{\mathbb{C}}
  \underoverset
    {
       \underset{
         \mathscr{H} \multimap (\text{-})
       }{\longrightarrow}}
    {
      \overset{
        \mathscr{H} \otimes (\text{-})
      }{\longleftarrow}
    }
    {\;\; \bot \;\;}
  Mod_{\mathbb{C}}
$$

[induces](monad#RelationBetweenAdjunctionsAndMonads) a linear version of the [[costate comonad]]

\[
 \label{UnderlyingEndofunctor}
  \array{
    \mathllap{
      \mathscr{H}
      \;\colon\;
    }
    Mod_{\mathbb{C}}
    &\longrightarrow&
    Mod_{\mathbb{C}}
    \\
    \mathscr{V}
    &\mapsto&
    \mathscr{H}
    \otimes
    \big(
      \mathscr{H}
      \multimap
      \mathscr{V}
    \big)
    \mathrlap{\,.}
  }
\]

To see its duplication operation (the comonad coproduct) notice first that the $\big(\mathscr{H} \otimes (\text{-}) \,\dashv\, \mathscr{H} \multimap (\text{-})\big)$-[[unit of an adjunction|unit]] is:

$$
  \array{
    (\text{-})
    &\overset{
      ret
       ^{ \mathscr{H}State }
       _{\mathbb{1},\mathbb{1}}
    }{\longrightarrow}&
    \mathscr{H} 
      \multimap
    \big(
     \mathscr{H}
       \otimes
     (\text{-})
    \big)
    \\
    \left\vert \psi \right\rangle
    &\mapsto&
    \big(
      \left\vert \psi' \right\rangle
      \mapsto
      \left\vert \psi' \right\rangle 
      \otimes
      \left\vert \psi \right\rangle
    \big)
    \mathrlap{\,.}
  }
$$

Using the orthonormal basis (eq:OrthonormalBasis) and the compact closure (eq:CompactClosureViaBraKetNotation)
we may equivalently write this as:

$$
  \array{
    (\text{-})
    &
    \overset{
      ret
       ^{ \mathscr{H}State }
       _{\mathbb{1},\mathbb{1}}
    }{\longrightarrow}&
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
      \otimes
    (\text{-})
    \\
    \vert \psi \rangle
    &\mapsto&
    \sum_w
    \left\vert w \right\rangle
    \left\langle w \right\vert 
    \otimes
    \left\vert \psi \right\rangle
    \mathrlap{\,.}
  }
$$

This means that the duplication (cojoin) operation in the $\mathscr{H}$-CoState comonad (eq:UnderlyingEndofunctor) is as follows:

\[
  \label{DuplicationOperation}
  \array{
    \mathscr{H}
      \otimes
    \big(
      \mathscr{H}
      \multimap
      (\text{-})
    \big)
    &
    \overset{
      dupl
        ^{ \mathscr{H}CoState }
        _{ \mathbb{1} }
    }{\longrightarrow}
    &
    \mathscr{H}
    \otimes
    \bigg(
      \mathscr{H}
      \multimap
      \Big(
        \mathscr{H}
          \otimes
        \big(
          \mathscr{H}
          \multimap
          (\text{-})
        \big)
      \Big)
    \bigg)
    \\
    \left\vert \psi \right \rangle
    \left\langle \phi \right\vert
    \otimes
    \left\vert \text{-} \right \rangle
    &\mapsto&
    \sum_w
    \left\vert \psi \right\rangle
    \left\langle w \right\vert
    \otimes
    \left\vert w \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\vert \text{-} \right \rangle
    \mathrlap{\,.}
  }
\]

Finally, the obtain-operation (the [[counit of a comonad|comonad counit]]) is the [[evaluation map]], hence the [[partial trace]] over $\mathscr{H}$:

$$
  \array{
    \mathscr{H}
    \otimes
    \big(
      \mathscr{H}
      \multimap
      (\text{-})
    \big)
    &\overset{
      obt^{ \mathscr{H}CoState }_{}
    }{\longrightarrow}&
    (\text{-})
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\vert \text{-} \right\rangle
    &\mapsto&
    \left\langle \phi \vert \psi \right\rangle
    \,
    \left\vert \text{-} \right\rangle    
  }
$$

The [[coKleisli morphisms]] are the [[superoperators]]:

$$
  \frac{
  \mathscr{H}
    \otimes
  \mathscr{H}^\ast
    \otimes
  \mathscr{K}
  \longrightarrow
  \mathscr{K}
  }{
  \mathscr{H}
    \otimes
  \mathscr{H}^\ast
  \longrightarrow
  \mathscr{K}
    \otimes
  \mathscr{K}^\ast
  }
$$


## Costate co-effects are quantum observables

For the classical [[costate comonad]] on a [[cartesian closed category]] the monad and its operations on the [[tensor unit]] (the [[terminal object]] in this case) are vacuous. Quite in contrast, the linear CoState comonad on the tensor unit encodes core structure of [[quantum physics]]:

\begin{example}
**(quantum observables as CoState coeffects)**
\linebreak

First notice that the value of the costate comonad on the tensor unit

$$
  \mathscr{H}CoState(\mathbb{1})
  \;\equiv\;
  \mathscr{H} 
    \otimes
  \big(
    \mathscr{H}
    \multimap
    \mathbb{1}
  \big)
  \;=\;
  \mathscr{H} \otimes \mathscr{H}^\ast  
$$

is the home of [[density matrices]]/[[mixed quantum states]] generalizing the [[pure states]] in $\mathscr{H}$.

Moreover, an $\mathscr{H}$-CoState [[coKleisli morphism]] on the tensor unit is equivalently a [[linear operator]] 
$$
  A \,\colon\, \mathscr{H} \to \mathscr{H}
  \,,
$$
hence a [[quantum observables]] -- incarnated via its [[expectation values]] on quantum states

\[
  \label{CoKleisliMorphism}
  \array{
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    &\overset{\mathcal{O}_A}{\longrightarrow}&
    \mathbb{1}
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    &\mapsto&
    \left\langle \phi \right\vert
    A
    \left\vert \psi \right\rangle  
    \mathrlap{\,.}
  }
\]

\end{example}

\begin{proposition}
  Composition of quantum observables $\mathcal{O}_A$, $\mathcal{O}_{A'}$ (eq:CoKleisliMorphism) in the [[coKleisli category]] is given by ordinary composition $A \circ A'$ of the corresponding [[linear operators]]:
$$
  \mathcal{O}_{A'}
  \circ
  \big(
    ext^{ \mathscr{H}CoState }_{\mathbb{1},\mathbb{1}} 
    \mathcal{O}_A
  \big)
  \;\;
    =
  \;\;
  \mathcal{O}_{ A' \circ A }
  \;\colon\;
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \,\mapsto\,
    \left\langle \phi \right\vert
    A A'
    \left\vert \psi \right\rangle
  \,.
$$
\end{proposition}
\begin{proof}
  From (eq:DuplicationOperation) we find that the extension operation is given as follows:
$$
  \array{
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
    &
      \overset{
        dupl^{ \mathscr{H}CoState }_{\mathbb{1},\mathbb{1}}
      }{\longrightarrow}
    &
    \mathscr{H}
    \otimes
    \big(
      \mathscr{H}
      \multimap
      \mathscr{H}
      \otimes
      \mathscr{H}^\ast
    \big)
    &\overset{
      \mathscr{H} 
      \otimes
      \big(
        \mathscr{H}
          \multimap
        \mathcal{O}_A
      \big)
    }{\longrightarrow}&
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    &\mapsto&
    \sum_w
    \left\vert \psi \right\rangle
    \left\langle w \right\vert
    \otimes
    \left\vert w \right\rangle
    \left\langle \phi \right\vert
    &\mapsto&
    \;\;
    \mathclap{
    \underset{
    {
      =\, 
      \left\vert \psi \right\rangle
      \left\langle \phi \right\vert
      A  
    }
    }
    {
      \underbrace{
        \sum_w
        \left\vert \psi \right\rangle
        \left\langle w \right\vert
        \otimes
        \left\langle \phi \right\vert
         A
        \left\vert w \right\rangle
      }
    }
    }
  }
$$  

hence

$$
  ext^{ \mathscr{H}CoState }_{\mathbb{1},\mathbb{1}}
  \,\colon\,
  \Big(
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \,\mapsto\,
    \left\langle \phi \right\vert
    A
    \left\vert \psi \right\rangle
  \Big)
  \,\mapsto\,
  \Big(
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \,\mapsto\,
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    A
  \Big)
$$

\end{proof}


[[!redirects quantum costate comonads]]

[[!redirects linear costate comonad]]
[[!redirects linear costate comonads]]




