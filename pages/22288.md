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

