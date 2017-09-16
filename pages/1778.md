
Cech cohomology is less a special kind of [[cohomology]] than a special algorithm for _computing_ cohomology classes.

On the other hand, while the algorithm always produces results that look like cohomology classes, these actually are the abstractly defined cohomology classes only under certain assumptions. Historically Cech cohomology has often been understood as being defined as whatever that algorithm computes, and theorems would be proven that determine under which conditions such "Cech cohomology" coincides with cohomology defined by other means, where "by other means" traditionally is: "in terms of right derived functor definition of [[abelian sheaf cohomology]]".

From the discussion at [[abelian sheaf cohomology]] we know that the right derived functor definition computes the hom-set in the [[homotopy category of an (infinity,1)-category|homotopy category]] of an [[(infinity,1)-topos]] $\mathbf{H}$ that may alternatively be computed as a colimit over resolutions of the domain object

$$
  H(X,A)
  := 
  \pi_0 \mathbf{H}(X,A)
  = colim_{Y \stackrel{\in W \cap F}{\to} X} 
  C_H(Y,A)
$$

where the colimit is over all acyclic fibrations $Y \stackrel{\in W \cap }{\to} X$ in an appropriate [[model category]] $C_H$ that [[presentable (infinity,1)-category|presents]] $\mathbf{H}$. For $\mathbf{H}$ an [[infinity-stack]] [[(infinity,1)-topos]] this $C_H$ is a [[model structure on simplicial presheaves]] and the acyclic fibrations $Y \stackrel{\in W \cap F}{\to} X$ for $X$ an ordinary space are the [[hypercover]]s.

Now, for some coefficient objects $A$ it is sufficient to take the colimit here not over all [[hypercover]]s, but just over [[Cech cover]]s. The resulting formula

$$
  H(X,A)
  = colim_{Y \stackrel{Cech cover}{\to} X} 
  C_H(Y,A)
$$

is then called the formula for **Cech cohomology** on $X$ with values in $A$.

Here a Cech cover is a simplicial presheaf that arises from an ordinary covering map $U \to X$ of $X$ by another space $U$ as the corresponding [[Cech nerve]] simplicial presheaf

$$
 \begin{aligned}
  Y := \left( 
    \cdots
    U \times_X U \times_X U
    \stackrel{\to}{\stackrel{\to}{\to}}
    U \times_X U \stackrel{\to}{\to} U 
  \right)
  \simeq
  hocolim_{[k] \in \Delta} U^{\times_X k}
 \end{aligned}
  \,.
$$

See [[descent for simplicial presheaves]] for more on the manipulations involved here.

To amplify, a general [[hypercover]] would start in degree 0 with a $U$ as above, but then in the next degree would have a cover $V \to U \times_X U$ of the fiber product, and so on, each fiber product in turn being covered by another space.

If $Y$ is not simply a Cech cover but also not the most general hypercover in that this iterative choice of further covering stops in degree $n$, then one also speaks of **Cech cover of level $n$** and of the corresponding cohomology formula as **higher Cech cohomology**. See for instance the reference by Tibor Beke below.

#References#

* Tibor Beke, _Higher Cech theory_ ([journal](http://www.math.uiuc.edu/K-theory/0646/) [pdf](http://www.math.uiuc.edu/K-theory/0646/cech.pdf))

