
# Commutative squares
* table of contents
{: toc}

## Definition and notation

Let $C$ be a [[category]]. A **square** of morphisms of $C$  consists of objects $X,Y,Z,W$ of $C$ and morphisms $f\colon X \to Z$, $g\colon X \to Y$, $f'\colon Y \to W$, and $g'\colon Z \to W$. This is often pictured as a square 
$$\array{& X & \overset{f}\rightarrow & Z & \\
          g & \downarrow &&\downarrow & g'\\
          &Y & \underset{f'}\rightarrow& W & \\
}$$

The square is **[[commutative diagram|commutative]]** if $g' \circ f = f' \circ g$.

The class of commutative squares in $C$ is written $\square C$.


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

Let $2$ denote the [[walking arrow]]: the category with two objects $0,1$ and one arrow $0 \to 1$. This has the structure of [[cocategory]]. Then the class of commutative squares in $C$  can also be described as $Cat(2 \times 2, C)$.  

If $D$ is a category, then $Cat(D, \square_1 C)$ can be regarded as the class of natural transformations of functors $D \to C$. Then the category structure $\square _2 C$ induces a category structure on $Cat(D,\square _1 C)$ giving the [[functor category]] $CAT(D,C)$: the category of functors and natural transformations. (This account is due to [[Charles Ehresmann]].)

One deduces that if also $E$ is a category then there is a natural bijection  
$$Cat(E \times D, C) \cong (E, CAT(D,C)),$$
which thus states that the category of (small if you like!) categories is [[cartesian closed category|cartesian closed]].

The commutative squares serve as the morphisms in the [[arrow category]] of $C$, which is the functor category $CAT(2,C)$.


[[!redirects commutative square]]
[[!redirects commutative squares]]
[[!redirects commuting square]]
[[!redirects commuting squares]]
