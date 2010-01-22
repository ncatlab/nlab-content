
> under construction

+-- {: .query}

[[Urs Schreiber]]: this is intended to eventually present a general abstract perspective on the various notions of _relative cohomology_ that are traditionally considered in the spirit of the general abstract discussion at [[cohomology]]
 
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

There are several different notions of what what a _relative_ notion of [[cohomology]] is.



### Push-forward not to the point, but to another space {#Push}

In ordinary [[cohomology]] -- as described there -- for a given ambient [[(∞,1)-topos]] $\mathbf{H}$ the cohomology of an object $X \in \mathbf{H}$ with coefficients in an object $A \in \mathbf{H}$ is the set/group of connected components of the [[derived hom space]]

$$
  H(X,A) = \pi_0 \mathbf{H}(X,A)
  \,.
$$

More generally, we may consider a kind of [[internal hom]] instead, whose components are themselves [[(∞,1)-presheaves]].

Fix $p : X \to Y$ a morphism in $\mathbf{H}$. Let $Op(Y) \subset \mathbf{H}_{/Y}$ be some subcategory of the [[over quasi-category]] of $\mathbf{H}$ over $Y$, to be regarded as the [[category of open subsets]] of $Y$ in $\mathbf{H}$. 

Then the functor

$$
  \mathbf{H}(X \times_Y (-), A) : Op(Y)^{op} \to \infty Grpd
$$

$$
  (U \to Y) 
  \mapsto 
  \mathbf{H}(X|_U, A)
$$

with $X|_U := X \times_Y U$ the [[fiber product]], 
produces an $(\infty,1)$-presheaf on $Op(Y)$. This can be regarded as being a cocycle in the  **relative cohomology of $X$ with coefficients in $A$** .

As the formula shows, this is the [[direct image]] of $A|_X$ along $p : X \to Y$.

Notice that in the case the $Y = *$ the [[terminal object]] in $\mathbf{H}$ and taking the only "open subset" of $*$ to be the point itself, this produces an $(\infty,1)$-presheaf on the point, which canonically identifies with an [[∞-groupoid]] that coincides with the one used in the non-relative version of [[cohomology]].

### Quotient cocycles

...


