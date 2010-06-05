#Contents#
* automatic table of contents goes here
{:toc}

## Idea

--

## Definition

Let $A$ be a small category, and let $Psh(A)$ denote the functor category $[A^{op}, Set]$.  An object $X\in Ob(Psh(A))$ is called a [[presheaf]] (of sets).   

A *cylinder on a presheaf* $X$ is a presheaf $IX$ with the following data:  


* Two jointly monomorphic morphisms $\partial^0_X, \partial^1_X\in Hom_{Psh(A)}(X,IX)$ admitting a common [[retraction]] $\sigma_X:IX\to X$.  That is, the induced map $\partial^0_X\coprod \partial^1_X:X\coprod X\to IX$ is a monomorphism, and $\sigma_X\circ \partial^j_X=id_X$ for $j\in \{0,1\}$.

That is, a cylinder is an object $IX$ with the morphisms above making the diagram below commute: 



A morphism of cylinders on presheaves $X$ and $Y$ is given by a pair of morphisms $\phi:X\to Y$ and $\psi:IX\to IY$ making the following diagram commute:

$$\begin{matrix}
&&\partial^j_X &&\sigma_X&&\\
&X&\to&IX&\to&X&\\
\phi&\downarrow&&\psi\downarrow&&\downarrow&\phi\\
&Y&\to&IY&\to&Y&\\
&&\partial^j_Y&&\sigma_Y&&\end{matrix}$$

In particular, $\phi$ is a [[retract]] of $\psi$.  

(More to come..)