## Overview

In [[algebraic geometry]], for an algebraic scheme $S$ and positive integer $n$, the __relative affine $n$-space__ $\mathbf{A}^n_S$ (or: [[affine space|affine]] $n$-space over $S$) is the generalization of an affine $n$-space $\mathbf{A}^n_k$ (considered as an algebraic $k$-scheme) from a ground ring $k$ to the category of [[relative scheme]]s over the base scheme $S$.

There are several equivalent definitions. 

## Definition using affine covers

In the affine case, if $S = Spec(B)$ this is simply the spectrum $\mathbf{A}^n_S = Spec(B[x_1,\ldots,x_n])$, and the morphism to the base scheme $S$ is induced by the ring inclusion $B\hookrightarrow B[x_1,\ldots,x_n]$. 

For general scheme, one takes an open cover of $S$ by affine schemes, and notices that the inclusions of double intersections into single intersection induce morphisms of ringed spaces from the double intersection to the single intersection, satisfying the cocycle condition allowing for gluing of such relative affine $n$-spaces over affines. Finally one checks that this definition does not depend on cover.  

## Definition via fiber product

$$
\mathbf{A}^n_S = 
\mathbf{A}^n_{\mathbf{Z}}\times_{Spec{Z}} S 
$$

## Definition via relative spectrum

There is a general notion of a relative spectrum (sometimes called global spectrum) of a sheaf of $\mathcal{O}_T$-algebras over a scheme $T$. The affine $n$-space over a scheme $S$ may be viewed as the $n$-dimensional vector bundle over $S$, but not viewed
as a locally free sheaf but as a total space. Fiberwise, to make a scheme from a vector space, one needs to take the spectrum of a symmetric algebra.

Affine $n$-space over $S$ is simply the spectrum of the symmetric algebra of the direct sum of $n$-copies of the structure sheaf of $S$:
$$ 
\mathbf{A}^n_S = 
Spec(Sym(\mathcal{O}^n_S))
$$

category: algebraic geometry
[[!redirects relative affine space]]