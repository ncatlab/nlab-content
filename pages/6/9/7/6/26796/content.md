
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


\tableofcontents

## Idea

The *Schur complement* of (i,j)-entry of a [[partitioned matrix|block]] $2\times 2$ [[matrix]]

$$
\left(
  \begin{matrix}
    A & B          
    \\
    C & D
  \end{matrix}
\right)
$$

is the following expression involving the [[inverse matrix]] of that entry:

* $D- C A^{-1} B$ if the entry is (1,1)

* $C- D B^{-1} A$ if the entry is (1,2)

* $B- A C^{-1} D$ if the entry is (2,1)

* $A- B D^{-1} C$ if the entry is (2,2)

whenever the inverses involved make sense. Typically the case at main diagonal are used compatibly with a standard choice of the shape of triangular matrices in Gauss procedure.

These expressions are related to [[quasideterminants]], Gauss elimination procedure and [[matrix inverse]]. 

The Schur complement is obtained as one of the entries by performing the block matrix version of row operation to obtain a triangular matrix:
$$
\left(
  \begin{matrix}
    I & 0          
    \\
  -C A^{-1} & I
  \end{matrix}
\right)
\left(
  \begin{matrix}
    A & B          
    \\
    C & D
  \end{matrix}
\right) 
= \left(
  \begin{matrix}
    A & B          
    \\
    0 & D - C A^{-1} B
  \end{matrix}
\right)
$$
If we continue with row operations,
$$
\left(
  \begin{matrix}
    I & - B (D - C A^{-1} B)^{-1}        
    \\
    0 & I
  \end{matrix}
\right) \left(
  \begin{matrix}
    A & B          
    \\
    0 & D - C A^{-1} B
  \end{matrix}
\right)
= \left(
  \begin{matrix}
    A &  0         
    \\
    0 & D - C A^{-1} B
  \end{matrix}
\right)
$$
we obtain a block diagonal matrix, hence
$$\left(
\begin{matrix}
    A & B      
    \\
    C & D
  \end{matrix} 
\right)^{-1} = 
\left(\begin{matrix}
    A^{-1} & 0        
    \\
    0 & (D - C A^{-1} B)^{-1}
  \end{matrix}\right)
\left(\begin{matrix}
    I & - B (D - C A^{-1} B)^{-1}        
    \\
    0 & I
  \end{matrix}
\right) 
\left(\begin{matrix}
    I & 0        
    \\
   -C A^{-1} & I
  \end{matrix}\right)
$$
$$
\left(
\begin{matrix}
    A & B      
    \\
    C & D
  \end{matrix} 
\right)^{-1} = \left(\begin{matrix}
   A^{-1}+A^{-1} B (D - C A^{-1} B)^{-1}C A^{-1} & - A^{-1} B (D - C A^{-1} B)^{-1}   
    \\
 -(D - C A^{-1} B)^{-1} C A^{-1} & (D - C A^{-1} B)^{-1}
  \end{matrix}
\right) 
$$
whenever the inverses of $A$ and of the Schur complement $D - C A^{-1} B$ exist.

There are alternative expressions for those (if certain inverses exist) thanks to the homological identities for quasideterminants or equivalently Woodbury matrix identity ([wikipedia](https://en.wikipedia.org/wiki/Woodbury_matrix_identity)). For example, if we start with using the Schur complement $A-B D^{-1}C$ and compare the two expressions for the inverse at the position $(1,1)$ we
obtain
$$
A^{-1}+A^{-1} B (D - C A^{-1} B)^{-1}C A^{-1} 
= (A-B D^{-1}C)^{-1}
$$

## References

* Wikipedia, *[Schur complement](https://en.wikipedia.org/wiki/Schur_complement)*

* Wikipedia, *[Woodbury matrix identity](https://en.wikipedia.org/wiki/Woodbury_matrix_identity)*

category: algebra

[[!redirects Schur complements]]
