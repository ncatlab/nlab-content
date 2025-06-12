

\tableofcontents

## Definition 

A *band* is a [[semigroup]] in which every element is [[idempotent]]. 

## Order structures on bands 

There are two distinct order structures on bands, referred to in the literature by the "natural poset" structure and the "natural preorder" structure. 

The natural preorder structure is defined by declaring $x \preceq y$ iff $x = x y x$. This is indeed a preorder by the following result. 

\begin{theorem} 
The relation $\preceq$ is reflexive and transitive. 
\end{theorem}

\begin{proof} 
Reflexivity is obvious from $x = x x = x x x$. Transitivity follows from the following argument: let $A$ denote an instance of associativity and $I$ an instance of idempotency. From $x y x = x$ (condition 1) and $y z y = y$ (condition 2), we have 

$$x =_1 x y x =_2 x y z y x =_I x y(z y x)(z y x) =_A x(y z y)x z y x =_2 x y x z y x =_1 x z y x\qquad(P).$$

Then 
$$x z x =_P x z(x z y x) =_A (x z)(x z)y x =_I x z y x =_P x$$

which completes the proof. 
\end{proof} 

## Examples of bands 

A [[semilattice]] is the same thing as a [[commutative]] band. 

A [[rectangular band]] is a band (see there). 

A [[skew lattice]] $(L, \wedge, \vee)$ is a band, using either $\wedge$ or $\vee$ as the semigroup operation. 
