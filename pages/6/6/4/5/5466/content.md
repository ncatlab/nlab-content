## Idea

A __class__ $L$ is __big__ if for any set $X\in L$ there exists a set $Y\in L$ such that $X\in Y$. 

## A metalanguage formulation

Consider class $L$ as a formula $\phi(z)$ with a free variable $z$; intuitively $L$ is the collection of all sets such that $\phi(z)$ is true. Then, in the metalanguage, $L$ is big (i.e. formula $\phi(x)$ exhibits a big class) if

$$
\phi(X) \implies (\exists Y)(\phi(Y) \wedge (X\in Y)) 
$$

[[!redirects big set]]
[[!redirects big classes]]
[[!redirects big sets]]