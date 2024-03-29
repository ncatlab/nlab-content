
This page contains technical details to be used at the main page _[[differential string structure]]_ . See there for context.

--

#Contents#
* table of contents
{:toc}


## Factorization of the $L_\infty$-cocycle
  {#FactorizationOfTheLInfintiyCocycle}

+-- {: .num_prop #FactorizationOfTheCocycle}
###### Proposition

The $L_\infty$-algebra cocycle

$$
  \mu : \mathfrak{so} \to b^2 \mathbb{R}
$$

factors as

$$
  \mathfrak{so} \stackrel{}{\to} (b \mathbb{R} \to \mathfrak{string})
  \stackrel{}{\to}
  b^2 \mathbb{R}
$$

given dually on CE-algebras by

$$
  CE(\mathfrak{so}) 
     \stackrel{
       \left(
       \array{
        t^a \mapsto t^a
        \\  
        b \mapsto 0
        \\   
        c \mapsto \mu
     }
     \right)
     }{\leftarrow} 
  CE(b \mathbb{R} \to \mathfrak{string})
   \stackrel{
     \left(
     \array{
        c \mapsto c
     }
     \right)
   }{\leftarrow}
  CE(b^2 \mathbb{R})
  \,.
$$

The left morphism is a [[quasi-isomorphism]].

=--

+-- {: .proof}
###### Proof

To see that we have a quasi-isomorphism, notice that the dg-algebra $CE(b \mathbb{R} \to \mathfrak{string})$ is [[isomorphic]] to the one with generators $\{t^a, b, c'\}$ and differentials

$$
  \begin{aligned}
    d|_{\mathfrak{g}^*} & = [-,-]^*
    \\
    d  b & = c'
    \\
    d c' & =  0
  \end{aligned}
  \,,
$$

where the isomorphism is given by the identity on the $t^a$s and on $b$ and by

$$
  c \mapsto c' + \mu
  \,.
$$

The primed dg-algebra is the [[tensor product]] $CE(\mathfrak{g}) \otimes CE( inn(b \mathbb{R}))$, where the second factor is manifestly cohomologically trivial.

=--



## Factorization of the differential $L_\infty$-cocycle
  {#FactorizationOfTheLInfintiyCocycle}


We now give a concrete construction showing

+-- {: .num_prop #DifferentialLInfinityLift}
###### Proposition

The factorization 

$$
  CE(\mathfrak{so}) 
     \stackrel{
     \left(
     \array{
        t^a \mapsto t^a
        \\  
        b \mapsto 0
        \\   
        c \mapsto \mu
     }
     \right)
     }{\leftarrow} 
  CE(b \mathbb{R} \to \mathfrak{string})
   \stackrel{
     \left(
     \array{
        c \mapsto c
     }
     \right)
   }{\leftarrow}
  CE(b^2 \mathbb{R})
$$

from [above](#FactorizationOfTheLInfintiyCocycle) lifts to a factorization of differential $L_\infty$-algebraic cocycles

$$
  \array{
    CE(\mathfrak{so}) 
     &
       \underoverset{\simeq}{
       \left(
       \array{   
          t^a \mapsto t^a
          \\  
          b \mapsto 0
          \\   
          c \mapsto \mu
       }
       \right)
       }{\leftarrow} 
     &
    CE(b \mathbb{R} \to \mathfrak{string}) 
     &
     \stackrel{
       \left(
       \array{
          c \mapsto c
       }
       \right)
     }{\leftarrow}
     &
    CE(b^2 \mathbb{R})
    \\
    \uparrow^\mathrlap{} 
     && 
    \uparrow^\mathrlap{}  
     && 
    \uparrow^\mathrlap{}  
    \\    
    W(\mathfrak{so}) 
      &
       \underoverset{\simeq}{
       }{\leftarrow} 
      &
    W(b \mathbb{R} \to \mathfrak{string}) 
      &
     \stackrel{
     }{\leftarrow}
     &
    W(b^2 \mathbb{R})
    \\
    \uparrow^\mathrlap{} 
     && 
    \uparrow^\mathrlap{}  
     && 
    \uparrow^\mathrlap{}  
    \\    
    inv(\mathfrak{so}) 
      &
       \underoverset{\simeq}{
       }{\leftarrow} 
      &
     \tilde inv(b \mathbb{R} \to \mathfrak{string})
      &
     \stackrel{
     }{\leftarrow}
     &
    inv(b^2 \mathbb{R})
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is at its heart trivial, but potentially a bit tedious. We proceed in two steps:

1. consider a "modified Weil algebra" of the twisted string Lie 3-algebra $(b \mathbb{R} \to \mathfrak{string})$ 

   in [The modified Weil algebra](#ModifiedWeilAlgebra);

1. construct the desired factorization by factoring itself through two fairly evident morphisms into and out of the modified Weil algebra, 

   in [The differential lift](TheLInftyDifferentialLift).

=--

### The modified Weil algebra
 {#ModifiedWeilAlgebra}

Our factorization [below]() makes use of an isomorphic copy of the Weil algebra $W(b\mathbb{R} \to \mathfrak{g}_\mu)$.

+-- {: .num_prop #ShiftedWeilAlgebra}
###### Proposition

The [[Weil algebra]] $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ of $(b^2 \mathbb{R} \to \mathfrak{g})$ is given on the extra shifted generators 
$\{r^a := \sigma t^a, h := \sigma b, g := \sigma c\}$  (where $\sigma$ is the shift operator extended as a graded derivation, see [[Weil algebra]]) by

* $d t^a = -\frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d b = - \mu + c + h$;

* $d c = g$, 

with [[Bianchi identities]]

* $d r^a = - C^a{}_{b c} t^b \wedge r^c$

* $d h = \sigma \mu - g$;

* $d g = 0$.



Let $\tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)$ be the dg-algebra
with the same underlying graded algebra as $W(b\mathbb{R} \to \mathfrak{g}_\mu)$ 
but with the differential modified as follows

* $d t^a = -\frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a$;

* $d r^a  = - C^a{}_{b c} t^b \wedge r^a$;

* $d b = - cs + c + \tilde h$;

* $d \tilde h = \langle -,-\rangle - g$;

* $d c = g$ .

* $d g = 0$,

where "$\tilde h$" is the new name for the generator that used to be called "$h$"

There is an [[isomorphism]] 

$$
  W(b\mathbb{R} \to \mathfrak{g}_\mu)
  \to 
  \tilde W(b\mathbb{R} \to \mathfrak{g}_\mu)
$$

in [[dgAlg]] that is the identity on all generators except on $h$, where it is given by

$$
  h \mapsto \tilde h + (\mu - cs)
  \,.
$$

=--

+-- {: .num_note #RemarkOnShiftedWeilAlgebra}
###### Note

Where the formula for the differential of $W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the 3-cocycle $\mu$ that for $\tilde W(b\mathbb{R}\to \mathfrak{g}_\mu)$ has the [[Chern-Simons element]] $cs$.  The shift by $cs-\mu$ is precisely what shifts the curvature characteristic $d_{W(\mathfrak{g})}\mu$ into the shifted copy of $\mathfrak{g}^*$ in the Weil algebra, thus exhibiting the modified $h$ as an [[invariant polynomial]].

=--


+-- {: .num_cor #TheInvariantPolynomials}
###### Corollary

The [[invariant polynomial]]s on $(b \mathbb{R} \to \mathfrak{g}_\mu)$ are generated from those of $\mathfrak{g}_\mu$ together with $\tilde h$ and $g$:

$$
  \tilde inv(b \mathbb{R} \to \mathfrak{string})
  =
  (inv(\mathfrak{so})\otimes \langle \tilde h, g\rangle)/(d \tilde h = \langle -,-\rangle - g)
  \,.
$$

=--



### The differential lift
 {#TheLInftyDifferentialLift}

We now use the isomorphism

$$
  W(b \mathbb{R} \to \mathfrak{string}) \stackrel{\simeq}{\to}
  \tilde W(b \mathbb{R} \to \mathfrak{string})
$$

from prop. \ref{ShiftedWeilAlgebra} and obtain the desired factorization,  as the composite

$$
  \array{
    CE(\mathfrak{so}) 
     &
       \underoverset{\simeq}{
       \left(
       \array{   
          t^a \mapsto t^a
          \\  
          b \mapsto 0
          \\   
          c \mapsto \mu
       }
       \right)
       }{\leftarrow} 
     &
    CE(b \mathbb{R} \to \mathfrak{string}) 
     &
     =
     &
    CE(b \mathbb{R} \to \mathfrak{string}) 
     &
     \stackrel{
       \left(
       \array{
          c \mapsto c
       }
       \right)
     }{\leftarrow}
     &
    CE(b^2 \mathbb{R})
    \\
    \uparrow^\mathrlap{i^*_{\mathfrak{so}}} 
     && 
    \uparrow^\mathrlap{i^*_{(b\mathbb{R} \to \mathfrak{string})}}  
     && 
    \uparrow^\mathrlap{}  
     && 
    \uparrow^\mathrlap{i^*_{b^2 \mathbb{R}}}  
    \\    
    W(\mathfrak{so}) 
      &
       \underoverset{\simeq}{
       \left(
       \array{   
         t^a \mapsto t^a
         \\
         b \mapsto 0
         \\
         c \mapsto cs
         \\
         r^a \mapsto r^a
         \\
         \tilde h \mapsto 0  
         \\
         g \mapsto \langle-,-\rangle
       }
       \right)
       }{\leftarrow} 
      &
    W(b \mathbb{R} \to \mathfrak{string}) 
     &
     \underoverset{\simeq}{
      \left(
        \array{
          \tilde h \mapsto h + (cs - \mu)
        }
      \right)
     }
     {\leftarrow}
     &
    \tilde W(b \mathbb{R} \to \mathfrak{string}) 
      &
     \stackrel{
       \left(
       \array{
         c \mapsto c
         \\
         g \mapsto g
       }
       \right)
     }{\leftarrow}
     &
    W(b^2 \mathbb{R})
    \\
    \uparrow^\mathrlap{p^*_{\mathfrak{so}}} 
     && 
    \uparrow^\mathrlap{}  
     && 
    \uparrow^\mathrlap{p^*_{(b \mathbb{R} \to \mathfrak{string})}}  
     && 
    \uparrow^\mathrlap{p^*_{b^2 \mathbb{R}}}  
    \\    
    inv(\mathfrak{so}) 
      &
       \underoverset{\simeq}{
       \left(
       \array{
         \tilde h \mapsto 0
         \\   
         g \mapsto \langle -,-\rangle
         \\   
         \langle \cdots \rangle
         \mapsto 
         \langle \cdots \rangle
       }
       \right)
       }{\leftarrow} 
      &
    \tilde inv(b \mathbb{R} \to \mathfrak{string}) 
      &
       =
      &
    \tilde inv(b \mathbb{R} \to \mathfrak{string}) 
      &
     \stackrel{
       \left(
       \array{
         g \mapsto g
       }
       \right)
     }{\leftarrow}
     &
    inv(b^2 \mathbb{R})
  }
  \,.
$$

Here 

* the unlabelled vertical morphisms are defined as the unique ones that make the respective square commute;

* the notation $\langle \cdots \rangle$ stands for all the [[invariant polynomial]]s of $\mathfrak{so}$ and $\langle-,-\rangle$ specifically for the [[Killing form]].
