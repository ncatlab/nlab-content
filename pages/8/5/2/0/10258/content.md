
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A _real structure_ on a [[complex vector space]] $V$ is an [[antilinear map]] $\sigma \colon V \to V$ which is an [[involution]].

Equivalently this is a [[real vector space]] $W$ and an [[isomorphism]] $V \simeq W \otimes_{\mathbb{R}} \mathbb{C}$ of $V$ with its [[complexification]].

Here $W = Eig(\sigma,1) \hookrightarrow V$ is the [[eigenspace]] of $\sigma$ for [[eigenvalue]] 1 and $W \otimes \{i\} = Eig(\sigma,-1) \hookrightarrow V$ is the [[eigenspace]] for [[eigenvalue]] -1. 


## Examples
 {#Examples}

\begin{example}\label{RealStructuresOnComplexLine}
**(real structures on the complex line)**
\linebreak
The standard real structure on the [[complex line]] $\mathbb{C}$ is [[complex conjugation]] $\overline{x + \mathrm{i} y} \,\equiv\, x - \mathrm{i}y$:
$$
  \array{
    \mathbb{C}
    &\longrightarrow&
    \mathbb{C}
    \\
    z 
      &\mapsto& 
    \overline{z}
    \mathrlap{\,.}
  }
$$
The [[fixed locus]] of this real structure are the [[real numbers]] under their defining embedding into the complex numbers: 
$$
  \mathbb{C}^{\overline{(\text{-})}}
  \;\simeq\;
  \mathbb{R} 
    \hookrightarrow 
  \mathbb{R} \oplus \mathrm{i} \mathbb{R} 
    \,\equiv\, 
  \mathbb{C}
$$
with
$$
  \array{
    \mathbb{R} \otimes_{{}_{\mathbb{R}}} \mathbb{C}
    &\xrightarrow{ \;\sim\; }&
    \mathbb{C}
    \\
    (x', x + \mathrm{i} y)
    &\mapsto&
    x' x + \mathrm{i} x' y
    \mathrlap{\,.}
  }
$$

Restricting the canonical complex-[[bilinear form]]
\[
  \label{CanonicalComplexBilinearFormOnComplexLine}
  \array{
    \mathbb{C} \otimes_{\mathbb{C}} \mathbb{C}
    &\longrightarrow&
    \mathbb{C}
    \\
    (z_1, z_2)
    &\mapsto&
    z_1 z_2
  }
\]
along this inclusion yields the canonical $\mathbb{R}$-bilinear form on $\mathbb{R}$:
$$
  \array{
    \mathbb{R} \otimes_{\mathbb{R}} \mathbb{R}
    &\hookrightarrow&
    \mathbb{C} \otimes_{\mathbb{C}} \mathbb{C}
    &\longrightarrow&
    \mathbb{C}
    \\
    (x_1, x_2)
    &\mapsto&
    (x_1, x_2)
    &\mapsto&
    x_1 x_2
    \mathrlap{\,.}
  }
$$

Another real structure on $\mathbb{C}$ is:
$$
  \array{
    \mathbb{C}
    &\longrightarrow&
    \mathbb{C}
    \\
    z 
      &\mapsto& 
    -\overline{z}
    \mathrlap{\,.}
  }
$$
Now the fixed locus is the [[imaginary numbers]] $\mathrm{i} \mathbb{R}$
$$
  \mathbb{C}^{-\overline{(\text{-})}}
  \;\simeq\;
  \mathrm{i}\mathbb{R} 
    \hookrightarrow 
  \mathbb{R} \oplus \mathrm{i} \mathbb{R} 
    \,\equiv\, 
  \mathbb{C}
$$
with
$$
  \array{
    \mathrm{i}\mathbb{R} \otimes_{{}_{\mathbb{R}}} \mathbb{C}
    &\xrightarrow{ \;\sim\; }&
    \mathbb{C}
    \\
    (\mathrm{i} x', x + \mathrm{i} y)
    &\mapsto&
    - x' y + \mathrm{i} x' x
    \mathrlap{\,.}
  }
$$
Restricting the canonical complex bilinear form (eq:CanonicalComplexBilinearFormOnComplexLine) along this inclusion now yields minus the canonical real bilinear form 
$$
  \array{
    \mathbb{R} \otimes_{\mathbb{R}} \mathbb{R}
    &\hookrightarrow&
    \mathbb{C} \otimes_{\mathbb{C}} \mathbb{C}
    &\longrightarrow&
    \mathbb{C}
    \\
    (x_1 ,\, x_2)
    &\mapsto&
    (\mathrm{i} x_1 ,\, \mathrm{i}x_2)
    &\mapsto&
    - x_1 x_2
    \mathrlap{\,.}
  }
$$ 
\end{example}



\begin{example}
**(real structures on the complex plane)**
\linebreak
On the [[complex plane]] $\mathbb{C}^2 \,\equiv\, \mathbb{C} \oplus \mathbb{C}$ we have first of all the real structures inherited from $\mathbb{C}$ (Ex. \ref{RealStructuresOnComplexLine}).
$$
  \array{
    \mathbb{C}^2 
    &\longrightarrow&
    \mathbb{C}^2
    \\
    (z_1, z_2) &\mapsto& (\overline{z_1}, \overline{z_2})
  }
$$
and
$$
  \array{
    \mathbb{C}^2 
    &\longrightarrow&
    \mathbb{C}^2
    \\
    (z_1, z_2) &\mapsto& -(\overline{z_1}, \overline{z_2})
    \,.
  }
$$
In addition, there is for instance
$$
  \array{
    \mathbb{C}^2 
    &\longrightarrow&
    \mathbb{C}^2
    \\
    \left[
    \array{
      z_1
      \\
      z_2
    } 
    \right]
    &\mapsto& 
    \left[
    \array{
      +\overline{z_1}
      \\
      -\overline{z_2}
    }
    \right]
    \,.
  }
$$
whose fixed locus is
$$
  \array{
    \mathbb{R}^2 
    &\hookrightarrow&
    \mathbb{C}^2
    \\
    \left[
    \array{
      x_1
      \\
      x_2
    }
    \right]
    &\mapsto&
    \left[
    \array{
      x_1
      \\
      \mathrm{i} x_2
    }
    \right]    
    \mathrlap{\,,}
  }
$$
the restriction to which of the canonical complex bilinear form on the complex plane
\[
  \label{CanonicalComplexBilinearFormOnComplexPlane}
  \array{
     \mathbb{C}^2 
     \otimes_{\mathbb{C}}
     \mathbb{C}^2
     &\longrightarrow&
     \mathbb{C}
     \\
     \left(
       \left[
       \array{
         z_1
         \\
         z_2
       }
       \right]
       ,\,
       \left[
       \array{
         z'_1
         \\
         z'_2
       }
       \right]
     \right)
     &\mapsto&
     z_1 z'_1 
       + 
     z_2 z'_2
  }
\]
is the [[hyperbolic form]] on the real [[plane]]:
$$
  \array{
     \mathbb{R}^2 \otimes_{\mathbb{R}} \mathbb{R}^2
     &\hookrightarrow&
     \mathbb{C}^2 
     \otimes_{\mathbb{C}}
     \mathbb{C}^2
     &\longrightarrow&
     \mathbb{C}
     \\
     \left(
       \left[
       \array{
         x_1
         \\
         x_2
       }
       \right]
       ,\,
       \left[
       \array{
         x'_1
         \\
         x'_2
       }
       \right]
     \right)
     &\mapsto&
     \left(
       \left[
       \array{
         x_1
         \\
         \mathrm{i}x_2
       }
       \right]
       ,\,
       \left[
       \array{
         x'_1
         \\
         \mathrm{i} x'_2
       }
       \right]
     \right)
     &\mapsto&
     x_1 x'_1 - x_2 x'_2 
     \mathrlap{\,.}
  }
$$

Yet another real structure is
$$
  \array{
    \mathbb{C}^2 
    &\longrightarrow&
    \mathbb{C}^2
    \\
    \left[
    \array{
      z_1
      \\
      z_2
    } 
    \right]
    &\mapsto& 
    \left[
    \array{
      \overline{z_2}
      \\
      \overline{z_1}
    }
    \right]
    \,.
  }
$$
whose [[fixed locus]] is
$$
  \array{
    \mathbb{R}^2 
    &\hookrightarrow&
    \mathbb{C}^2
    \\
    \left[
    \array{
      x_1
      \\
      x_2
    }
    \right]
    &\mapsto&
    \left[
    \array{
      x_1 + \mathrm{i} x_2
      \\
      x_1 - \mathrm{i} x_2
    }
    \right]    
    \,,
  }
$$
the restriction to which of the canonical complex bilinear form (eq:CanonicalComplexBilinearFormOnComplexPlane)
is twice the [[hyperbolic form]] on $\mathbb{R}^2$
$$
  \array{
     \mathbb{R}^2 \otimes_{\mathbb{R}} \mathbb{R}^2
     &\hookrightarrow&
     \mathbb{C}^2 
     \otimes_{\mathbb{C}}
     \mathbb{C}^2
     &\longrightarrow&
     \mathbb{C}
     \\
     \left(
       \left[
       \array{
         x_1
         \\
         x_2
       }
       \right]
       ,\,
       \left[
       \array{
         x'_1
         \\
         x'_2
       }
       \right]
     \right)
     &\mapsto&
     \left(
       \left[
       \array{
         x_1 + \mathrm{i}x_2
         \\
         x_1 - \mathrm{i}x_2
       }
       \right]
       ,\,
       \left[
       \array{
         x'_1 + \mathrm{i}x'_2
         \\
         x'_1 - \mathrm{i}x'_2
       }
       \right]
     \right)
     &\mapsto&
     2 x_1 x'_1 - 2 x_2 x'_2 
     \mathrlap{\,.}
  }
$$
\end{example}


\begin{example}\label{RealStrucAsDaggerSelfDualHermitian}
**(real structure as dagger-self-dual Hermitian structure)**
\linebreak
  Let $\mathscr{V}$ be a [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]] equipped with *both*

1. a non-degenerate [[sesquilinear form|sesquilinear]] ([[Hermitian form|Hermitian]]) [[inner product]] ${\langle - \vert - \rangle}$,

1. a non-degenerate symmetric [[bilinear form|bilinear]] [[inner product]] ${(-\vert-)}$

such that 

* the Hermitian-[[adjoint operator|adjoint]] ${(-\vert-)}^\dagger$ of the bilinear pairing is the [[coevaluation map]] that exhibits $\mathscr{V}$ as a [[self-dual object]],

then this induces a [[real structure]] on $\mathscr{V}$. 

Moreover, for $\mathscr{W}$ another [[finite-dimensional vector space|finite-dimensional]] [[complex vector space]] equipped with a compatible pair of such structures, then the linear maps
$$
  \mathscr{V}
  \longrightarrow
  \mathscr{W}
$$
which preserve both structures also preserve that real structure, hence come from $\mathbb{R}$-[[linear maps]] of underlying [[real vector spaces]].
\end{example}
\begin{proof}
To start with, we note some generalities:

1. the non-degenerate sesquilinear form ${\langle -\vert -\rangle}$ is equivalently given by an [[antilinear map]]  
$a \colon \mathscr{V} \to \mathscr{V}^\ast$ to the [[dual linear space]], via 

   $$ 
     {\langle - \vert -\rangle} 
       \,=\, 
     a(-)(-) 
   $$

1. the non-degenerate bilinear form ${(- \vert -)}$ is equivalently given by a complex [[linear map]] $l \,\colon\, \mathscr{V} \to \mathscr{V}^\ast$, via

   $$
     {(- \vert -)} 
       \,=\, 
     l(-)(-)
   $$

(where the second argument means [[evaluation]]).

In [[bra-ket notation]] this is suggestively written as:

$$
  {( v \vert} \;\;\coloneqq\;\; l {\vert v )} 
  \,\;\;\;\;\;
  {\langle w \vert} \;\;\coloneqq\;\; a {\vert w \rangle} 
  \,.
$$

For example, the [[Hermitian adjoint]] $f^\dagger \,\colon\, W \to \mathscr{V}$ of any linear map $f \,\colon\, \mathscr{V} \to \mathscr{W}$

is

$$
  f^\dagger {\vert w \rangle}
  \;\coloneqq\;
  a^{-1}\big( {\langle w \vert} f\big)
  \;=\;
  a^{-1} \circ f^\ast \circ a {\vert w \rangle}
  \,.
$$

Moreover, if $\big\{ {\vert w \rangle} \big\}_{w \in W}$ is any [[orthonormal basis]] of $\mathscr{V}$ with respect to $\langle - \vert - \rangle$, then the [[coevaluation map]] which exhibits $\mathscr{V}^\ast \,\coloneqq\, Map_{\mathbb{C}}(\mathscr{V}, \mathbb{C})$ as the [[linear dual space]] to $\mathscr{V}$ may be written as

\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}^\ast
  \\
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & \mathcal{V}
  \\[3pt]
  1 
   \ar[r, phantom, "{\mapsto}"]
  &
  \underset{w \in W}{\sum}
  \vert w \rangle \langle w \vert
\end{tikzcd}
and hence equivalently as
\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}
  \ar[r, "{ a }"]
  &
  \mathcal{V}^\ast
  \\
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & 
  \mathcal{V}^\ast
  \ar[r, "{ a^{-1} }"]
  &
  \mathcal{V}
  \mathrlap{\,,}
\end{tikzcd}  
which we use at the very end below.


Now regarding the concrete proof:

The composite

$$
  \tau
  \;\coloneqq\;
  a^{-1} \circ l
  \;\colon\;
  \mathscr{V} \to \mathscr{V}
  \,,
$$

is an [[antilinear map|antilinear]] [[endomorphism]] of $\mathscr{V}$, hence it will be sufficient to show that it is an [[involution]] (and hence the sought-after real structure). For that, in turn, it is clearly sufficient that

\[
  \label{InterchangeOfBiAndSesquilinearForms}
  a^{-1} \circ l
  \,=\,
  l^{-1} \circ a
  \,.
\]

because then

$$
  \tau \circ \tau
  \;=\;
  \big(
    a^{-1} \circ l
  \big)
  \circ
  \big(
    a^{-1} \circ l
  \big)
  \;=\;
    a^{-1} \circ l
  \circ
    l^{-1} \circ a
  \;=\;
  id_{\mathscr{V}}
  \,.
$$

We now show that this condition (eq:InterchangeOfBiAndSesquilinearForms) is equivalent to the assumption that $(-\vert-)^\dagger$ is the coevaluation map.

Namely, with 

\begin{tikzcd}[
  row sep=-1pt
]
  &[-5pt]
  \mathcal{V}
  \ar[r, equals]
  &
  \mathcal{V}
  \\
  (-\vert-)
  \;:\;
  &
  \otimes
  &
  \otimes
  \ar[r, "{ \mathrm{ev} }"]
  & 
  \mathbb{C}
  \\
  &
  \mathcal{V}
  \ar[
    r,
    "{ l }"{description}
  ]
  &
  \mathcal{V}^\ast
\end{tikzcd}

we have

\begin{tikzcd}[
  row sep=-1pt
]
  && \mathcal{V}^\ast
  \ar[rrr, "{ a^{-1} }"]
  &&& 
  \mathcal{V}
  \\
  & 
  \mathbb{C}
  \ar[
    r, 
    "{ \mathrm{coev} }"
  ]
  & 
  \otimes
  \\
  &
  &
  \mathcal{V}
  \ar[r, equals]
  &
  \mathcal{V}
  \\
  (-\vert-)^\dagger
  \;:\;
  &
  \otimes
  &
  \otimes
  &
  \otimes
  \ar[r, "{ \mathrm{ev} }"]
  & 
  \mathbb{C}
  \\
  &
  &
  \mathcal{V}
  \ar[
    r,
    "{ l }"{description}
  ]
  &
  \mathcal{V}^\ast
  \\
  &
  \mathbb{C}
  \ar[
    r,
    "{ \mathrm{coev} }"
  ]
  &
  \otimes
  \\
  &&
  \mathcal{V}^\ast
  \ar[rrr, "{ a^{-1} }"]
  &&& 
  \mathcal{V}
  \mathrlap{\,,}
\end{tikzcd}

which by the [[zig-zag identity]] for $ev$ & $coev$ equals

\begin{tikzcd}[
  row sep=-1pt
]
  & 
  &
  \mathcal{V}
  \ar[r, "{ l }"]
  &
  \mathcal{V}^\ast
  \ar[r, "{ a^{-1} }"]
  &
  \mathcal{V}
  \\
  (-\vert-)^\dagger
  \;:
  &
  \mathbb{C}
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  &&
  \otimes
  \\
  &&
  \mathcal{V}^\ast
  \ar[rr, "{ a^{-1} }"]
  &&
  \mathcal{V}
  \mathrlap{\,.}
\end{tikzcd}

On the other hand, the coevaluation which exhibits $(-\vert-)$ as a [[self-dual object|self-duality]] is clearly

\begin{tikzcd}[row sep=-1pt]
  & \mathcal{V}^\ast 
  \ar[r, "{ l^{-1} }"]
  & 
  \mathcal{V}
  \\
  \mathbb{C} 
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  &
  \mathcal{V} 
  \ar[r, equals]
  & 
  \mathcal{V}
\end{tikzcd}

which by the above discussion equals

\begin{tikzcd}[row sep=-1pt]
  & 
  \mathcal{V}
  \ar[r, "{ a }"]
  &
  \mathcal{V}^\ast 
  \ar[r, "{ l^{-1} }"]
  & 
  \mathcal{V}
  \\
  \mathbb{C} 
  \ar[r, "{ \mathrm{coev} }"]
  &
  \otimes
  \\
  & 
  \mathcal{V}^\ast
  \ar[rr, "{ a^{-1} }"]
  &
  & 
  \mathcal{V}
\end{tikzcd}

This being equal to $(-\vert-)^\dagger$ above is clearly equivalent to (eq:InterchangeOfBiAndSesquilinearForms).
\end{proof}


## Related concepts

* [[complex structure]]

* [[quaternionic structure]]

* [[real space]]

* [[real oriented cohomology theory]]

  * [[KR-theory]]


## References

* Wikipedia, *[Real structure](https://en.wikipedia.org/wiki/Real_structure)*

More generally in [[spectral geometry]] (via [[spectral triples]]) and [[KR-theory]]:

* {#Connes95} [[Alain Connes]], definition 3 of _Noncommutative geometry and reality_, J. Math. Phys. 36 (11), 1995 ([pdf](http://www.alainconnes.org/docs/reality.pdf))


[[!redirects real structures]]
