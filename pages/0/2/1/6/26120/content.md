[[!redirects quantum costate comonad]]

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

The *[[state monads]]* and *[[costate comonads]]* ([[store comonads]]) are typically discussed on [[cartesian closed categories]] --- but, of course, the analogous construction exists on any [[closed monoidal category]]. 

An immediate non-cartesian example is a [[category of vector spaces]]. At least for a [[finite-dimensional vector space]] $\mathscr{H}$ (and generally on a [[compact closed category]]), the *linear $\mathscr{H}$-state/store (co)monads* merge into a single [[Frobenius monad]] (see [below](#FrobeniusStructure)) which reflects some core structure of [[open quantum systems]] ([[mixed states]], [[quantum channels]] and their [[quantum observables]]).

Due to this fact and the general broad identification of (multiplicative) [[linear logic]] with a form of [[quantum logic]], the linear (co)state (co)monad may deserve to be called the *quantum state monad* (cf. the similar situation for the *[[quantum reader monad]]*).

For example, [[unitary quantum channels]] turn out to be embodied by [[monad transformations]] between such quantum state monads, so that with this terminology the plausible and desireable statement "*quantum channels are quantum state transformations*" becomes an actual theorem (see [below](#QuantumChannelsAreQuantumStateTransformations)).

## Preliminaries

For definiteness (only), we consider the category $Mod_{\mathbb{C}}$ of [[complex vector spaces]] with, as usual:

* [[monoidal category|monoidal structure]] given by the [[tensor product of vector spaces]],

* [[tensor unit]]$\;$ $\mathbb{1} \,\equiv\, \mathbb{C}$ the [[complex numbers]] themselves,

* [[internal hom]]$\;$ $\mathscr{H} \multimap \mathscr{H}'$ the vector space of [[linear maps]]

  \[
    \label{InternalHomHomIsomorphism}
    \mathscr{H} \otimes (\text{-})
    \;\;\dashv\;\;
    \mathscr{H} \multimap (\text{-})
  \]

Throughout the following we fix

\[
  \label{TheFinDimHilbertSpace}
  \mathscr{H} \,\in\, FinDimMod_{\mathbb{C}} \hookrightarrow Mod_{\mathbb{C}}
\] 

a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]]. 

But most or all of the following discussion works for $Mod_{\mathbb{C}}$ replaced by any [[symmetric monoidal closed category]] and $\mathscr{H}$ taken from a [[compact closed category|compact closed]] [[subcategory]].

In this vein, for notational purposes only (at this point) we choose on $\mathscr{H}$:

1. a [[Hermitian form|Hermitian]] [[inner product]] $\left\langle\cdot \vert \cdot\right\rangle$, hence consider it as a [[finite-dimensional Hilbert space]] and use [[bra-ket]] notation to denote the generic elements of $\mathscr{H}$ by 

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


## Definition

For $\mathscr{H}$ a [[finite-dimensional Hilbert space]] --- or generally an object in a [[compact closed category]] $QuTypes$ --- its [[internal hom]]-[[adjoint functor|adjunction]] is [[ambidextrous adjunction|ambidextrous]] and associated to a pair of [[Frobenius monads]], in linear version of the classical [[state monads]]/[[store comonad]]-construction:

\begin{imagefromfile}
    "file_name": "QuantumStateFrobeniusMonads-230919.jpg",
    "width": 680,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


Moreover, these (co)monads may equivalently be understood as the ([[cowriter comonad|co]]-)[[writer monads]] induced by the [[endomorphism algebra]] $End(\mathscr{H}) \,\simeq\, \mathscr{H}^\ast \otimes \mathscr{H}$, which is a [[Frobenius algebra]] (by general arguments as recalled in [Lauda 2006](Frobenius+algebra#Lauda2006), made explicit for instance in [Vicary 2011 Lem 3.17](endomorphism+ring#Vicary11)) and as such makes its ([[cowriter comonad|co]]-)[[writer monad]] into a [[Frobenius monad]].

\linebreak

We next spell this out in more detail

> (Beware that there is now a switch in conventions. Will streamline later.)


### The defining adjunction
 {#TheDefiningAdjunction}

The [[internal hom]]-[[adjoint functor|adjunction]] for $\mathscr{H}$ (eq:TheFinDimHilbertSpace)

\[
  \label{TheInternalHomAdjunction}
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
\]

the $\big(\mathscr{H} \otimes (\text{-}) \,\dashv\, \mathscr{H} \multimap (\text{-})\big)$-[[unit of an adjunction|unit]] is:

\[
  \label{TheAdjunctionUnit}
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
\]

Using the [[symmetric monoidal category|symmetric braiding]], an orthonormal basis (eq:OrthonormalBasis) and the compact closure (eq:CompactClosureViaBraKetNotation)
we may equivalently write this as the "insertion of an identity" in the form known from [[quantum mechanics]] textbooks:

$$
  \array{
    (\text{-})
    &
    \overset{
      ret
       ^{ \mathscr{H}State }
       _{\mathbb{1},\mathbb{1}}
    }{\longrightarrow}&
    \mathscr{H}^\ast
      \otimes
    \mathscr{H}
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

The [[adjunction counit]] is the [[evaluation map]]:

\[
  \label{TheAdjunctionCounit}
  \array{
    \mathscr{H}
    \otimes
    \big(
      \mathscr{H}
      \multimap
      (\text{-})
    \big)
    &\overset{
      obt^{ \mathscr{H}Store }_{}
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
    \mathrlap{\,.}
  }
\]

which --- again using the [[symmetric monoidal category|symmetric braiding]], an orthonormal basis (eq:OrthonormalBasis) and the compact closure (eq:CompactClosureViaBraKetNotation) --- is equivalently the [[partial trace]] over $\mathscr{H}$:


\[
  \label{TheAdjunctionCounit}
  \array{
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    \otimes
    (\text{-})
    &\overset{
      obt^{ \mathscr{H}Store }_{}
    }{\longrightarrow}&
    (\text{-})
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\vert \text{-} \right\rangle
    &\mapsto&
    \underset{w}{\sum}
    \left\langle w \vert \psi \right\rangle
    \left\langle \phi \vert w \right\rangle 
    \otimes
    \left\vert \text{-} \right\rangle
    \mathrlap{\,.}
  }
\]


### The linear state monad

The adjunction (eq:TheInternalHomAdjunction)
[induces](monad#RelationBetweenAdjunctionsAndMonads) a linear version of the [[state monad]]:

The [[underlying]] [[endofunctor]] is

\[
 \label{UnderlyingEndofunctorOfQuantumStateMonad}
  \array{
    \mathllap{
      \mathscr{H}
      State
      \;\colon\;
    }
    Mod_{\mathbb{C}}
    &\longrightarrow&
    Mod_{\mathbb{C}}
    \\
    \mathscr{V}
    &\mapsto&
    \Big(
    \mathscr{H}
    \multimap
    \big(
      \mathscr{H}
      \otimes
      \mathscr{V}
    \big)
    \Big)
    \mathrlap{\,.}
  }
\]

The join operation is induced from the adjunction counit (eq:TheAdjunctionCounit) as:

$$
  \array{
    \mathscr{H}^\ast
    \otimes
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    \otimes
    \mathscr{H}
    &
    \overset{
      join^{\mathscr{H}State}_{(\text{-})}
    }{\longrightarrow}
    &
    \mathscr{H}^\ast
    \otimes
    \mathscr{H}
    \\
    \left\langle \text{-} \right\vert
    \otimes
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\vert \text{-} \right\rangle
    &\mapsto&
    \left\langle \phi \vert \psi \right\rangle
    \,
    \left\langle \text{-} \right\vert
    \otimes
    \left\vert \text{-} \right\rangle
    \mathrlap{\,.}
  }
$$


### The linear store comonad

The adjunction (eq:TheInternalHomAdjunction)
[induces](monad#RelationBetweenAdjunctionsAndMonads) a linear version of the [[costate comonad]]:

The [[underlying]] [[endofunctor]] is

\[
 \label{UnderlyingEndofunctorOfQuantumCostateComonad}
  \array{
    \mathllap{
      \mathscr{H}
      Store
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


The duplication (cojoin) operation in the $\mathscr{H}$-CoState comonad (eq:UnderlyingEndofunctor) is induced from the adjunction unit (eq:TheAdjunctionUnit)
as follows:

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
        ^{ \mathscr{H}Store }
        _{ (\text{-}) }
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

Finally, the obtain-operation (the [[counit of a comonad|comonad counit]]) is the adjunction counit (eq:TheAdjunctionCounit)



### Kleisli structure
 {#KleisliStructure}

We assume an ambient [[compact closed category]] such as that of [[finite-dimensional vector spaces]].

For the formula in Prop. \ref{KleisliCompositionIsSuperoperatorComposition} to come out naturally, we take -- without loss of generality -- the generic object on which to apply the linear store comonad to be a [[dual object]] $\mathscr{K}^\ast \coloneqq (\mathscr{K} \multimap \mathbb{1})$. 

\begin{remark}
\label{TheCoKleisliMorphisms}
**(the coKleisli morphisms)**
\linebreak
The [[coKleisli morphisms]] of the quantum store comonad (eq:UnderlyingEndofunctor)

\[
  \label{KleisliMorphism}
  \mathcal{O}_A
  \;\colon\;
  \mathscr{H}
    \otimes
  \big(
  \mathscr{H}
    \multimap
  \mathscr{K}^\ast
  \big)
  \longrightarrow
  \mathscr{K}^\ast
\]

are [[isomorphism|isomorphically]] of the form 

\[
  \label{KleisliMorphismUnderCompactClosure}
  \mathcal{O}_A
  \;\colon\;
  \mathscr{H}
    \otimes
  \mathscr{H}^\ast
    \otimes
  \mathscr{K}^\ast
    \longrightarrow
  \mathscr{K}^\ast
\]

and as such are equivalently ([[adjunct]] to) morphisms of the form

\[
  \label{SuperoperatorOnMatrices}
  A
  \;\colon\;
  \mathscr{H}
    \otimes
  \mathscr{K}^\ast
    \longrightarrow
  \mathscr{H}
    \otimes
  \mathscr{K}^\ast
\]

which in turn are isomorphically "*[[superoperators]]*" of the form

\[
  \label{Superoperator}
  \big(
    \mathscr{K} \multimap \mathscr{H}
  \big)
  \longrightarrow
  \big(
    \mathscr{K} \multimap \mathscr{H}
  \big)
  \,.
\]

\end{remark}

\begin{proposition}
\label{KleisliCompositionIsSuperoperatorComposition}
  The [[Kleisli composition]] on [[Kleisli morphisms]] (eq:KleisliMorphism) of the quantum store comonad is given by the plain composition of the linear duals of the corresponding [[superoperators]] (eq:SuperoperatorOnMatrices):
\[
  \label{KleisliComposition}
  \big(
    extend^{\mathscr{H}Store}
      \mathcal{O}_{A'}
  \big)
  \circ
  \big(
    extend^{\mathscr{H}Store}
      \mathcal{O}_{A}
  \big)
  \;\;=\;\;
  \Big(
    \left\vert \psi \right\rangle
    \left\langle \phi, \kappa \right\vert
    \,\mapsto\,    
    \left\vert \psi \right\rangle
    \left\langle \phi, \kappa \right\vert
    A \circ A'
  \Big)
  \,.
\]
\end{proposition}
Here for $\psi \in \mathscr{H}$ and $\kappa \in \mathscr{K}$ we denote their tensor product as
$$
  \left\vert \psi, \kappa \right\rangle
  \,\in\,
  \mathscr{H} \otimes \mathscr{K}
  \,.
$$
\begin{proof}
The relation between a Kleisli morphism $\mathcal{O}_A$ (eq:KleisliMorphismUnderCompactClosure) and the corresponding super-operator $A$ (eq:SuperoperatorOnMatrices) on matrices is

$$
  \array{
    \mathllap{
      \mathcal{O}_A
      \;\colon\;
    }
    \mathscr{H} 
      \otimes 
    \mathscr{H}^\ast
      \otimes
    \mathscr{K}^\ast
    &\longrightarrow&
    \mathscr{K}^\ast
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \kappa \right\vert
    &\mapsto&    
    \left\langle
      \phi, \kappa
    \right\vert
     A
    \left\vert
      \psi, -
    \right\rangle    
    \mathrlap{\,.}
  }
$$ 

With this and the cojoin operation (eq:DuplicationOperation) it follows that the extend-operation turns $\mathcal{O}_A$ into 

$$
  \array{
    \mathscr{H}
      \otimes
    \big(
      \mathscr{H}
      \multimap
      \mathscr{K}^\ast
    \big)
    &
      \overset{
        dupl^{ \mathscr{H}Store }_{\mathscr{K}^\ast,\mathscr{K}^\ast}
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
          \mathscr{K}^\ast
        \big)
      \Big)
    \bigg)
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
    \big(
      \mathscr{H}
      \multimap
      (\mathscr{K}')^\ast
    \big)
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \kappa \right\vert
    &\mapsto&
    \sum_w
    \left\vert \psi \right\rangle
    \left\langle w \right\vert
    \otimes
    \left\vert w \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \kappa \right\vert
    &\mapsto&
    \;\;
    \underset{
      = 
        \left\vert \psi \right\rangle
        \left\langle \phi, \kappa \right\vert
         A      
    }{
    \underbrace{
    \sum_{w, k'}
        \left\vert \psi \right\rangle
        \left\langle \phi, \kappa \right\vert
         A
        \left\vert w, k' \right\rangle
        \left\langle w, k' \right\vert
    }
    }
  }
$$  

hence
\[
  \label{StoreExtension}
  \array{
    \mathllap{
      exend^{\mathscr{H} Store}
      \mathcal{O}_A
      \;\colon\;
    }
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
      \otimes
    \mathscr{K}^\ast
    &\longrightarrow&
    \mathscr{H}
      \otimes
    \mathscr{H}^\ast
      \otimes
    \mathscr{K}^\ast
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi, \kappa \right\vert
    &\mapsto&    
    \left\vert \psi \right\rangle
    \left\langle \phi, \kappa \right\vert
    A
  }
\]
This implies the claim (eq:KleisliComposition).
\end{proof}

The same argument applies with the second copy of $\mathscr{K}$ replaced by some $\mathscr{K}'$: The Kleisli category is the [[opposite category|opposite]] of that of superoperators of the form

$$
  \mathscr{H}\otimes\mathscr{K}
  \longrightarrow
  \mathscr{H}\otimes\mathscr{K}'
  \longrightarrow
  \mathscr{H}\otimes\mathscr{K}''
  \,.
$$



## Examples

### Quantum observables are the Quantum state contextful scalars

> (The following now starts out a little repetitive, recalling a special case of the general statement above. Will streamline...)

For the classical [[costate comonad]] on a [[cartesian closed category]] its value and its operations on the [[tensor unit]] (the [[terminal object]] in this case) are vacuous. Quite in contrast, the linear CoState comonad on the tensor unit encodes core structure of [[quantum physics]]:

\begin{example}
\label{QuantumObservablesAsQuantumStateContextfulScalars}
**(quantum observables as quantum state contextful scalars)**
\linebreak

First notice that the quantum store on the tensor unit

$$
  \mathscr{H}Store(\mathbb{1})
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
    ext^{ \mathscr{H}Store }_{\mathbb{1},\mathbb{1}} 
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
        dupl^{ \mathscr{H}Store }_{\mathbb{1},\mathbb{1}}
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
  ext^{ \mathscr{H}Store }_{\mathbb{1},\mathbb{1}}
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

\begin{remark}\label{Traces}
Understanding $\mathscr{H}Store$ as a [[Frobenius monad]] as [above](#FrobeniusStructure) makes it natural to combine the [[unit of a monad|monad unit]] (eq:TheAdjunctionUnit) with the Kleisli morphisms of Rem. \ref{TheCoKleisliMorphisms}.

This gives the *[[trace]]* of linear operators, as seen via (eq:StoreExtension):

$$
  \array{
    \mathbb{1}
    &\overset{ret^{\mathscr{H}^\ast State}_{\mathbb{1}}}{\longrightarrow}&
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    &\overset{
      ext^{\mathscr{H}Store}_{\mathbb{1}, \mathbb{1}} \mathcal{O}_{A}
    }{\longrightarrow}&
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    &\overset{obt^{\mathscr{H}Store}_{\mathbb{1}}}{\longrightarrow}&
    \mathbb{1}
    \\
    1
    &\mapsto&
    \underset{w}{\sum}
    \left\vert w \right\rangle
    \left\langle w \right\vert
    &\mapsto&
    \underset{w}{\sum}
    \left\vert w \right\rangle
    \left\langle w \right\vert    
    A
    &\mapsto&
    tr\big( A \big)
  }
$$
and generally the [[partial trace]]:
$$
  \array{
    \mathscr{K}^\ast
    &\overset{ret^{\mathscr{H}^\ast State}_{\mathscr{K}^\ast}}{\longrightarrow}&
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    \otimes
    \mathscr{K}^\ast
    &\overset{
      ext^{\mathscr{H}Store}_{\mathscr{K}^\ast, \mathscr{K}^\ast} \mathcal{O}_{A}
    }{\longrightarrow}&
    \mathscr{H}
    \otimes
    \mathscr{H}^\ast
    \otimes
    \mathscr{K}^\ast
    &\overset{obt^{\mathscr{H}Store}_{\mathscr{K}^\ast}}{\longrightarrow}&
    \mathscr{K}^\ast
    \\
    \left\langle \kappa \right\vert
    &\mapsto&
    &\mapsto&
    &\mapsto&
    \left\langle \kappa \right\vert
    tr_{\mathscr{H}}\big(A \big)
  }
$$
\end{remark}

### Quantum channels that are Quantum state transformations
 {#QuantumChannelsAreQuantumStateTransformations}

\begin{example}
\label{UnitaryQuantumChannelsAsQUantumStateTransformations}
**(unitary quantum channels are quantum state transformations)**
\linebreak
  If $U \,\colon\, \mathscr{H}_1 \to \mathscr{H}_2$ is an [[invertible map]] with [[inverse]] $U^\dagger \,\colon\, \mathscr{H}_2 \to \mathscr{H}_1$, then the "[[unitary quantum channel]]"
$$
  \array{
    \mathscr{H}_1
      \otimes
    \mathscr{H}_1^\ast
      \otimes
    (\text{-})
    &
    \overset{
      U \otimes U^{\dagger \ast}
    }{\longrightarrow}
    &
    \mathscr{H}_2
      \otimes
    \mathscr{H}_2^\ast
      \otimes
    (\text{-})
  }
$$
is a [transformation of](monad#TransformationOfMonadsOnFixedCategory) quantum state monads.
\end{example}
\begin{proof}
By direct unwinding of the definitions, we find that the counit is respected

$$
  \array{
    \mathscr{H}_1
      \otimes
    \mathscr{H}_1^\ast
      \otimes
    (\text{-})
    &
    \overset{
      U 
        \otimes
      U^{\dagger \ast}
      \,
        \otimes
      (\text{-})
    }{\longrightarrow}
    &
    \mathscr{H}_2
      \otimes
    \mathscr{H}_2^\ast
      \otimes
    (\text{-})
    &
    \overset{ 
      obt^{\mathscr{H}_2Store}_{\mathscr{K}_2} 
    }{\longrightarrow}
    &
    (\text{-})
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \text{-} \right\vert    
    &\mapsto&
    U
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    U^\dagger
    \otimes
    \left\langle \text{-} \right\vert    
    &\mapsto&
    \left\langle \phi \right\vert
      U^\dagger
      U
    \left\vert \psi \right\rangle
    \otimes
    \left\langle \text{-} \right\vert        
    \\
    && &=&
    \left\langle \phi \vert \psi \right\rangle
    \otimes
    \left\langle \text{-} \right\vert        
    \\
    && &=&
    obt^{\mathscr{H}_1 Store}_{\mathscr{K}^\ast}
    \big(
      \left\vert \psi \right\rangle
      \left\langle \phi \right\vert
      \otimes
      \left\langle \text{-} \right\vert    
    \big)
  }
$$

by the property that $U^\dagger$ is a [[left inverse]] to $U$, 

and the unit is respected

$$
  \array{
    (\text{-})
    &
    \overset{
      ret^{ \mathscr{H}_1State }_{(\text{-})}
    }{\longrightarrow}
    &
    \mathscr{H}_1
    \otimes
    \mathscr{H}_1^\ast
    \otimes
    (\text{-})    
    &
    \overset{
      U \otimes U^{\dagger\ast}
      \otimes
      (\text{-})
    }{\longrightarrow}
    &
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    \otimes
    (\text{-})    
    \\
    \underset{w}{\sum}
    \left\vert w \right\rangle
    \left\langle w \right\vert
    \otimes
    \left\vert \text{-} \right\rangle    
    &\mapsto&
    \underset{w_1}{\sum}
    U
    \left\vert w_1 \right\rangle
    \left\langle w_1 \right\vert
    U^{\dagger}
    \otimes
    \left\vert \text{-} \right\rangle    
    \\
    && &=&
    \underset{w_2}{\sum}
    \left\vert w_2 \right\rangle
    \left\langle w_2 \right\vert
    \otimes
    \left\vert \text{-} \right\rangle    
    \mathrlap{\,,}
  }
$$

because $U^\dagger$ is also a [[right inverse]] to $U$, using here the [[compact closed category|compact closure]] identification

\[
  \label{SeeingThatUnitaryQuantumChannelPreservesSatteReturn}
  \array{ 
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    &\overset{\sim}{\longrightarrow}&
    \mathscr{H}_2 \multimap \mathscr{H}_2
    &\overset{\sim}{\longrightarrow}&
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    \\
    \underset{w_1}{\sum}
    U
    \left\vert w_1 \right\rangle
    \left\langle w_1 \right\vert
    U^{\dagger}
    &\mapsto&     
    \underset{
      \mathrm{Id}
    }{
    \underbrace{
      U
      \circ 
      Id
      \circ
      U^{\dagger}
    }
    }
    &\mapsto&
    \underset{w_2}{\sum}
    \left\vert w_2 \right\rangle
    \left\langle w_2 \right\vert
    \mathrlap{\,.}
  }
\]

Therefore also the join and cojoin are preserved, eg.:
$$
  \array{
    \mathscr{H}_1
      \otimes
    \mathscr{H}_1^\ast
      \otimes
    (\text{-})
    &
    \overset{
      dupl^{\mathscr{H}_1 Store}_{\mathscr{K}^\ast}
    }{\longrightarrow}
    &
    \mathscr{H}_1
      \otimes
    \mathscr{H}_1^\ast
      \otimes
    \mathscr{H}_1
      \otimes
    \mathscr{H}_1^\ast
      \otimes
    (\text{-})
    &
    \overset{
      U \otimes U^{\dagger\ast}
      \otimes
      U \otimes U^{\dagger\ast}
      \,
      \otimes \mathrm{id}
    }{\longrightarrow}
    &
    \mathscr{H}_2
      \otimes
    \mathscr{H}_2^\ast
      \otimes
    \mathscr{H}_2
      \otimes
    \mathscr{H}_2^\ast
      \otimes
    (\text{-})
    \\
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \text{-} \right\vert  
    &\mapsto&
    \mathclap{
    \underset{w_1}{\sum}
    \,
    \left\vert \psi \right\rangle 
    \left\langle w_1 \right\vert 
    \otimes
    \left\vert w_1 \right\rangle
    \left\langle \phi \right\vert U^\dagger
    \otimes
    \left\langle \text{-} \right\vert  
    }
    &\mapsto&
    \mathclap{
    U \left\vert \psi \right\rangle 
    \Big(
    \underset{
      =
    \underset{w_2}{\sum}
      \left\langle w_2 \right\vert 
      \otimes
      \left\vert w_2 \right\rangle
    }
    {
    \underbrace{
      \underset{w_1}{\sum}
      \left\langle w_1 \right\vert 
      U^\dagger
      \otimes
      U
      \left\vert w_1 \right\rangle
    }
    }
    \Big)
    \left\langle \phi \right\vert U^\dagger
    \otimes
    \left\langle \text{-} \right\vert  
    }
    \\
    && 
    &=&
    \mathclap{
    dupl^{\mathscr{H}_2 Store}_{\mathscr{K}^\ast}
    \circ
    \big(
      U \otimes U^{\dagger \ast} 
      \otimes id
    \big)
    \big(
    \left\vert \psi \right\rangle
    \left\langle \phi \right\vert
    \otimes
    \left\langle \text{-} \right\vert  
    \big)
    }
  }
$$
\end{proof}

\begin{example}
\label{PartialTraceAsComonadicQuantumStateTransformation}
  A [[partial trace quantum channel]] 
$$
  \array{
    (\text{-})
    \otimes
    \mathscr{H}
    \otimes
    \mathscr{B}
    \otimes
    \mathscr{B}^\ast
    \otimes
    \mathscr{H}^\ast
    &
    \xrightarrow{
      id 
      \otimes
      trace^{\mathscr{B}}
    }
    &
    \mathscr{H} \otimes \mathscr{H}^\ast
    \\
    \left\vert \psi, \beta \right\rangle
    \left\langle \beta', \psi' \right\vert
    &\mapsto&
    \left\vert \psi \right\rangle
    \left\langle \beta' \vert \beta \right\rangle
    \left\langle \psi' \right\vert
    \mathrlap{\,.}
  }  
$$
is a comonadic quantum state transformation
$$
  trace^{\mathscr{B}}
  \,\colon\,
  (\mathscr{H} \otimes \mathscr{B})State
  \underoverset{ comon\;transf }{}{\longrightarrow}
  \mathscr{H}State
  \,.
$$
\end{example}
\begin{proof}
Since the structure maps of the $(\mathscr{H} \otimes \mathscr{B})\mathrm{State}$-comonad are [[tensor products]] of structure maps of $\mathscr{H}\mathrm{State}$ and $\mathscr{B}\mathrm{State}$, 
it is sufficient to show this for $\mathscr{H} = \mathbb{1}$ the [[tensor unit]], hence for the case that $\mathscr{H}\mathrm{State} = \mathrm{Id}$.
But in this case $\mathrm{trace}^{\mathscr{B}} \,=\, obt^{ \mathscr{H}^\ast\mathrm{Store} }{}$, which is a comonadic transformation (in fact the [[terminal object|terminal]] one) by [this example](monad#IdentityMonadIsInitial)).

Alternatively, onee readily checks the required conditions explicitly:



\begin{imagefromfile}
    "file_name": "PartialTraceAsQuantumStateComonTransf-230924b.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\end{proof}


### Heisenberg evolution is action of Quantum state transformations
 {#HeisenbergEvolution}

namely on the quantum-state contextful scalars:

\begin{example}
  The quantum state transformation induced by a [[unitary quantum channel]] $U$, according to Exp. \ref{UnitaryQuantumChannelsAsQUantumStateTransformations}, is invertible (its inverse given by the inverse unitary quantum channel) and hence it induces a functor between the [[Kleisli categories]] (by the discussion [here](monad#ExtensionOfFreeModalesAlsoIsomorphicMonadTransformation)) which on the quantum-state contextful scalars $\mathcal{O}_A$ (Exp. \ref{QuantumObservablesAsQuantumStateContextfulScalars}) is given by [[conjugation action|conjugation]] with $U$:
$$
  \array{
    (\text{-})
    \otimes
    \mathscr{H}_1
    \otimes
    \mathscr{H}_1^\ast
    &
    \overset{
      (\text{-})
      \otimes
      U \otimes U^{\dagger\ast}
    }{\longleftarrow}
    &
    (\text{-})
    \otimes
    \mathscr{H}_2
    \otimes
    \mathscr{H}_2^\ast
    \\
    Kl(\mathscr{H}Store)
    &\longrightarrow&
    Kl(\mathscr{H}Store)
    \\
    \left[
    \array{
      \mathscr{H}_1
      \otimes
      \mathscr{H}_1^\ast
      \\
      \Big\downarrow\mathrlap{ \mathcal{O}_A }
      \\
      \mathbb{1}
    }
    \right]
    &\mapsto&
    \left[
    \array{
      \mathscr{H}_2
      \otimes
      \mathscr{H}_2^\ast
      \\
      \Big\downarrow\mathrlap{ 
        \mathcal{O}_{ U \cdot A \cdot U^\dagger } 
      }
      \\
      \mathbb{1}
    }
    \;\;\;\;\;\;
    \right]
  }
$$

This transformation

$$
  A \;\mapsto\; U \cdot A \cdot U^\dagger
$$

is of course the [[Heisenberg picture]]-evolution of [[quantum observables]] $A$ under unitary transformations $U$ of the [[quantum states]].

\end{example}


## Properties

### Interaction with QuantumEnvironment monad

\begin{proposition}
\label{QuantumStoreDistributesOverQuantumReader}
For 

* $\mathscr{H}$ a [[dualizable object|dualizable]] linear type 

* $W$ a [[finite set|finite]] classical type, 

we have:

1. the $\mathscr{H}$QuantumState comonad $\mathscr{H}^\ast Store$ [distributes over](distributive+law#ComonadDistributingOverMonad) the $W$[[quantum reader monad|QuantumEnvironment]] monad $\bigcirc_W$,

1. the $W$-[[quantum reader monad|QuantumEnvironment]] comonad $\bigstar_W$ [distributes over](distributive+law#ComonadDistributingOverMonad) over the $\mathscr{H}$QuantumState monad $\mathscr{H}^\ast Store$.

\begin{imagefromfile}
    "file_name": "DistrStrucQuantumStoreOverQuantumReader-231002.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


\end{proposition}
\begin{proof}
  The relevant conditions (from  [Brookes & Van Stone 1993 Def. 3](distributivity+law#BrookesVanStone93), see [there](distributive+law#MonadDistributingOverComonad)) all follows immediately from the distributivity of the [[tensor product]] (being a [[left adjoint]]) over the [[direct sum]] (being a [[coproduct]]). 

For definiteness, we spell it out. In the first direction we have:

\begin{imagefromfile}
    "file_name": "DistrCondQuantumStoreOverQuantumEnvrn-231002.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

and in the converse direction we have:

\begin{imagefromfile}
    "file_name": "DistrCondQuantumEnvrnOverQuantumStore-231002.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

\end{proof}

\begin{example}
\label{QuantumStateReaderKleisliCategory}
  The two-sided [[Kleisli category]] induced by Prop. \ref{QuantumStoreDistributesOverQuantumReader} (via [Brookes & Van Stone 1993 Thm. 2](distributivity+law#BrookesVanStone93)) equivalently has (by arguing $W$-wise just as in Prop. \ref{KleisliCompositionIsSuperoperatorComposition}):

* as morphisms $W$-indexed sets of linear operators 


\begin{imagefromfile}
    "file_name": "QuantumStateReaderKleisliMap-230929b.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}

* with composition given by their $W$-wise operator products

\begin{imagefromfile}
    "file_name": "QuantumStateReaderKleisliComposition-230929b.jpg",
    "width": 700,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}


\end{example}


## Related concepts

* [[quantum reader monad]]


[[!redirects quantum costate comonads]]

[[!redirects quantum store comonad]]
[[!redirects quantum store comonad]]

[[!redirects linear costate comonad]]
[[!redirects linear costate comonads]]

[[!redirects linear store comonad]]
[[!redirects linear store comonad]]



