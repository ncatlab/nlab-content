## Idea

While unital ring $R$ is simply an algebra over $\mathbf{Z}$ and $A$-algebras for $A$ (commutative) subring of the center of $R$ (more generally, if the unit map $\eta: A\to Center(R)$ is given) center are hence generalizing the rings over possibly noncommutative rings express general objects in coslice category $Ring/A$ for arbitrary $A$.

In some sense a dual notion is the notion of an $A$-coring.

## Details

If $K$ is a commutative ring (or especially a [[field]]), then an [[associative algebra]] over $K$ is a monoid object in $K$-[[Mod]]; this is a special case of the previous section.

If $A$ is a noncommutative ring, then a __ring over $A$__, or simply an __$A$-ring__, is a monoid object $R$ in $A$-[[Bimod]] (that is, in $_A Mod _A$).  Every $A$-ring is a ring in the usual sense, in the sense that there is an obvious [[forgetful functor]] to the usual rings. In fact the unit map $A \to R$ is a morphism of rings, and the category of $A$-rings is precisely the [[coslice category]] or under-category $A/Ring$. Thus by category-theoretic rules, one might be led to unconventionally call $A$-rings "rings *under* $A$". Unfortunately, standard name for $A$-rings is "rings *over* $A$", like conventionally calling $k$-algebras the "algebras *over* $K$". 

Unlike for the $k$-algebras, the multiplication $R\times R\to R$ which is the morphism of $A$-[[bimodules]], is not (left) $A$-linear in the *second* factor, but only $A^{op}$-linear (that is, $A$-linear on the right). In other words, the axiom for $K$-algebras $k (r s) = r (k s)$ is not true, for $k\in A$, $r,s\in R$, although $k (r s) = (k r) s$ and $(r s) k = r (s k)$ do hold.  

Both for a discussion for under-over and also for this difference between $K$-algebras and $A$-rings see the Caf&#233;\'s [quick algebra quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html).

## $A\otimes A^{op}$-rings

The structure of an $A\otimes A^{op}$-ring $(R,\mu,\eta)$ is determined by
the structure of $A$ as a ring, together with the two natural homomorphisms
of rings
$s = \eta(-\otimes 1_A):A\to R$ and $t=\eta(1_A\otimes -):A^{op}\to R$ which have commuting images ($s(a)t(a')=t(a')s(a)$, for all $a,a'\in A$). In theory of [[associative bialgebroid]]s these are the dual versions of the source and target maps from the study of [[groupoid]]s.

There is (not always associative) product in the study of $A\otimes A^{op}$-rings, so called [[Takeuchi product]].


## Literature

...
