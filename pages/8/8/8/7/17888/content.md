
# Subtraction
* the following line creates the automatic table of contents
{: toc}

## Idea

The basic example of subtraction is, of course, the partial operation in the monoid of natural numbers or in the integers. It is often the first illustration of a non-associative operation met in abstract algebra. We think of subtraction as an operation $s:\mathbb{Z}\times \mathbb{Z}\to \mathbb{Z}$, where, of course, $s(m,n)=m-n$.

There are numerous related abstractions of this, relating to different aspects of the basic operation.



## Abstract






...


## Definition

1. (Universal Algebra) In the sense of Ursini  in the context of a varietal theory,  a _subtraction term_, $s$, is a binary term $s$ satisfying $s(x, x) = 0$ and $s(x, 0) = x$.
(see [[subtractive variety]]

1. In a [[co-Heyting algebra]], subtraction is the operation [[left adjoint]] to the [[join]] operator:
$$ (- \setminus y) \dashv (y \vee -)$$

This is related to [[subtractive logic]].


## Properties

...


## Examples

* Subtraction in the [[commutative monoid]] of the [[natural numbers]] $\mathbb{N}$ in given by the monus/truncated subtraction operator,
$$\dot - : \mathbb{N}\times \mathbb{N}\rightarrow \mathbb{N}$$
which is defined by,

$$\forall n,m \in \mathbb{N},$$

$$n\dot - m= 

\left\{
  \begin{aligned}
    0 & if\; m\geq n \\ 
    1+[pred(n)\dot -m] & otherwise
  \end{aligned}
\right.
$$

where $pred(n)$, the predecessor function, is the [[inverse]] to the successor function $succ(n) = n+1$.

* Subtraction in the [[abelian group]] of the [[integers]] $\mathbb{Z}$, is an [[entire relation]] on the integers, making it an true [[inverse]] operation to the group multiplication. It is given by,

$$-: \mathbb{Z}\times \mathbb{Z}\rightarrow \mathbb{Z}$$
$$\forall x,y \in \mathbb{Z}$$
$$x-y= 

\left\{
  \begin{aligned}
    0 & if\; x = y \\ 
    1+[pred(x)\dot -y] & if\; x \gt y \\
    (-1)\cdot (1+[pred(x)\dot -y]) & if\; x \lt y
  \end{aligned}
\right.
$$


## References

...


[[!redirects subtraction]]
