#Idea#

The bicrossed product generalizes the [[semidirect product]] of groups.

This construction is essential to the [[quantum double construction]] of Drinfel'd.

#Definition#

Given a pair of matched groups $H$ and $K$, the bicrossed product of groups $H\times K$ on the set $H \times K$
is given by
\[ (h,k)\cdot(h',k') = (h\alpha(k,h'),\beta(k,h')k')\]
with unit $(1,1)$ and $h,h'\in H$, $k,k'\in K$, where $\alpha: K\times H\rightarrow H$, $\beta: K\times H\rightarrow K$ are left and right actions, respectively.

A pair of groups $(H,K)$ is said to be matched if there exists a left action $\alpha$ of $K$ on the set $H$ and a right action $\beta$ of the group $H$ on the set $K$ such that for all $h,h'\in H$, $k,k'\in K$, the following hold:
* $\beta(k k',h) = \beta(k,\alpha(k',h))\beta(k',h)$,
* $\alpha(k,h h') = \alpha(k,h)\alpha(\beta(k,h),h')$,
* $\alpha(k,1) = 1$,
* $\beta(1,h) = 1$.

+-- {: .query}
Need to define the bicrossed product of algebras.
=--


#References#

C. Kassel, Quantum Groups, Graduate Texts in Mathematics 155, Springer-Verlag, New York-Berlin, 1995.