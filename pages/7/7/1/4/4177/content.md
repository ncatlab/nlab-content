#Contents#
* automatic table of contents goes here
{:toc}

## Idea

--

## Definition

###Cylinder Object

Let $A$ be a small category, and let $Psh(A)$ denote the functor category $[A^{op}, Set]$.  An object $X\in Ob(Psh(A))$ is called a [[presheaf]] (of sets).   

A *cylinder on a presheaf* $X$ is a presheaf $I X$ with the following data:  


* Two jointly monomorphic morphisms $\partial^0_X, \partial^1_X\in Hom_{Psh(A)}(X,I X)$ admitting a common [[retraction]] $\sigma_X:I X\to X$.  That is, the induced map $\partial^0_X\coprod \partial^1_X:X\coprod X\to I X$ is a monomorphism, and $\sigma_X\circ \partial^j_X=id_X$ for $j\in \{0,1\}$.

That is, a cylinder is an object $I X$ with the morphisms above making the diagram below commute: 

(PLACEHOLDER!)

A morphism of cylinders on presheaves $X$ and $Y$ is given by a pair of morphisms $\phi:X\to Y$ and $\psi:I X\to I Y$ making the following diagram commute:

$$\begin{matrix}
&&\partial^j_X &&\sigma_X&&\\
&X&\to&I X&\to&X&\\
\phi&\downarrow&&\psi\downarrow&&\downarrow&\phi\\
&Y&\to&I Y&\to&Y&\\
&&\partial^j_Y&&\sigma_Y&&\end{matrix}$$

In particular, $\phi$ is a [[retract]] of $\psi$.  

###Cylinder Functor

A _cylinder functor_ is a cylinder object for the identity functor $1_Psh(A)$ in the endofunctor category $[Psh(A),Psh(A)]$.  

####Elementary Homotopy Data

A presheaf category is said to have a _elementary homotopy data_ if it is equipped with a cylinder functor I such that 

* the functor I commutes with all small colimits;
* the functor I respects monomorphisms; 
* the natural transformation $\partial^j_{(-)}:1_{Psh(A)}\to I$ sends arrows of Psh(A) to commutative squares in Psh(A) in the obvious way.  We require that it sends all monomorphisms to [[pushout|cartesian squares]].

(More to come..)