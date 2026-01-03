
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition and notation

Let $C$ be a [[category]]. A **square** of morphisms of $C$  consists of objects $X,Y,Z,W$ of $C$ and morphisms $f\colon X \to Z$, $g\colon X \to Y$, $f'\colon Y \to W$, and $g'\colon Z \to W$. This is often pictured as a square 
$$\array{& X & \overset{f}\rightarrow & Z & \\
          g & \downarrow &&\downarrow & g'\\
          &Y & \underset{f'}\rightarrow& W & \\
}$$

The square is **[[commutative diagram|commutative]]** if $g' \circ f = f' \circ g$.

The category of commutative squares in $C$ is written $\square C$.

### Using the walking commutative square

Alternatively, let $\mathbb{I}$ denote the [[walking morphism]] and let $\mathbb{I}^2 = \mathbb{I} \times \mathbb{I}$ be the [[product category]] of the walking morphism with itself; $\mathbb{I}^2$ is the **walking commutative square** or the **2-cube category**. 

Then a **commutative square** in a category $C$ is a [[functor]] from $\mathbb{I}^2$ to $C$, and the category of commutative squares in $C$ can also be described as the [[functor category]] $C^{\mathbb{I}^2}$.  

## Structure

This class has partial compositions $\circ_1$ and $\circ_2$ which are vertical and horizontal: 
$$  \array{ \bullet & {\to} & \bullet & \\
           \downarrow &&\downarrow \\
          \bullet  & {\to}& \bullet \\
            \downarrow &  & \downarrow\\
            \bullet  & \to & \bullet
}  \quad \quad 
 \array{\bullet & {\to} & \bullet & \to & \bullet  \\
           \downarrow &&\downarrow && \downarrow  \\
          \bullet  & {\to}& \bullet & \to & \bullet   }
$$
thus forming a (strict) [[double category]], also written $\square C$, whose objects are those of $C$, whose horizontal and vertical 1-cells are given by morphisms in $C$, and whose 2-cells exhibit commutative squares. It contains the _vertical category_ $\square_1 C$ and the _horizontal category_ $\square _2 C$. 

One can also form _multiple compositions_ $[a_{ij}]$ of arrays $(a_{ij})$, $i=1, \ldots, m; j=1, \ldots , n$,  of commutative squares   provided that in the obvious sense _adjacent squares are composible_. One checks by induction that:

_any composition of commutative squares is commutative._


## Applications

If $D$ is a category, then $Cat(D, \square_1 C)$ can be regarded as the class of natural transformations of functors $D \to C$. Then the category structure $\square _2 C$ induces a category structure on $Cat(D,\square _1 C)$ giving the [[functor category]] $C^D$: the category of functors and natural transformations. (This account is due to [[Charles Ehresmann]].)

One deduces that if also $E$ is a category then there is a natural bijection  
$$Cat(E \times D, C) \cong (E, C^D),$$
which thus states that the category of (small if you like!) categories is [[cartesian closed category|cartesian closed]].

The commutative squares serve as the morphisms in the [[arrow category]] of $C$, which is the functor category $C^\mathbb{I}$.

## Related concepts

* [[square]]

* [[commutative triangle]]

## References

Commutative squares are defined in:

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], page 9 of: *Synthetic Category Theory*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects commutative square]]
[[!redirects commutative squares]]
[[!redirects commuting square]]
[[!redirects commuting squares]]

[[!redirects walking commutative square]]
[[!redirects walking commutative squares]]

[[!redirects 2-cube category]]
[[!redirects 2-cube categories]]