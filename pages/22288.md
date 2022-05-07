
#Contents#
* table of contents
{:toc}


## Idea

The small and large inductive dimensions, together with the Lebesgue [[covering dimension]] are the three main notions of [[dimension]] for [[topological spaces]].
They coincide in some, but not all, cases.

## Small inductive dimension

The __small inductive dimension__ (alias __Menger–Urysohn dimension__) $ind(X)$
of a [[regular topological space]] $X$ is defined as follows:
$ind(\emptyset)=-1$
and $ind(X)\le n$ ($n\ge0$) if for any $x\in X$ and any [[neighborhood]] $V\subset X$ of $x$ there is an [[open subset]] $U\subset X$ such that $x\in U$, $U\subset V$,
and $ind(\bar U\setminus U)\le n-1$.

## Large inductive dimension

The __large inductive dimension__ (alias __Brouwer–Čech dimension__) $Ind(X)$ of a [[normal topological space]] $X$
is defined as follows: $Ind(\emptyset)=-1$
and $Ind(X)\le n$ ($n\ge0$) if for any [[closed subset]] $A\subset X$
and any [[open subset]] $V\subset X$ such that $A\subset V$
there is an [[open subset]] $U\subset X$ such that $A\subset U\subset V$
and $Ind(\bar U\setminus U)\le n-1$.

## Properties

The subspace theorem: for every subspace $M$ of a [[regular space]] $X$ we have $ind(M)\le ind(X)$.
(Theorem 1.1.2 in \cite{Engelking95}.)

## Related concepts

[[!include notions of dimension -- contents]]


## References

* {#Engelking78} [[Ryszard Engelking]], _Dimension Theory_, Mathematical Library **19**, North-Holland Publishing/Polish Scientific Publishers 1978 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/engelking.pdf))

* {#Engelking95} [[Ryszard Engelking]], _Theory of Dimensions -- Finite and Infinite_, Sigma Series in Pure Mathematics **10**, Helderman 1995 ([pdf](http://www.gbv.de/dms/goettingen/187241074.pdf))





