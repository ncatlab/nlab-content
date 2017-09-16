Recall that [[cohomology]] in an [[(infinity,1)-topos]] $\mathbf{H}$ on an object $X$ with coefficients in an object $A$ is the [[hom-set]] in the [[homotopy category of an (infinity,1)-category]]

$$
  H(X,A) = \pi_0 \mathbf{H}(X,A)
  \,.  
$$

This is the _cohomology set_ . 

It is a [[pointed set]] if $A$ is a [[pointed object]].

In the case that $A$ moreover carries the structure of a [[group object]], the set $H(X,A)$ inherits naturally itself the structure of a [[group]]. In this case one speaks of the _cohomology group_ of $X$ with coefficients in $A$.

+-- {: .query}
Dually, is this why n-spheres are good for homotopy as they are cogroups? ---David
=--

#Examples#

# generalized abelian cohomology # 

In all of what is called [[generalized cohomology]]  -- which is really generalized _abelian_ cohomology, compare [[nonabelian cohomology]] -- the coefficient object is taken to be not just a [[group object]] but a "maximally abelian" group object called a [[stable (infinity,1)-category|stable object]] in general and called a [[spectrum]] in the case that $\mathbf{H}$ = [[Top]].

In that case all the [[delooping hypothesis|deloopings]] $\mathbf{B}^n A$ of $A$ exists and are still stably abelian group objects.

So in that case not only is the cohomology set $H(X,A)$ naturally an abelian group, but there is an infinite sequence of such cohomology groups, one for each delooping $\mathbf{B}^n A$. This yields the traditional notation for graded cohomology groups by setting

$$
  H^n(X,A) := H(X, \mathbf{B}^n A)
  \,.
$$



## "ordinary" (integral/Eilenberg-Mac Lane-) cohomology ##


The standard example are the **"ordinary" cohomology groups** that come from taking $\mathbf{H} = $ [[Top]] or = [[Infinity-Grpd]] (see [[homotopy hypothesis]]) and choosing the coefficient object to be the [[Eilenberg-Mac Lane spectrum]]

$$
  A := \mathbf{B} \mathbb{Z}
  \,.
$$

The for $X \in \mathbf{H}$ any object (a [[topological space]] or an [[infinity-groupoid]]) the "ordinary" cohimology of $X$ in degree $n$ is

$$
  H^n(X) := H^n(X,\mathbb{Z})
  :=
  H(X, \mathbf{B}^n \mathbb{Z})
  =
  \pi_0 \mathbf{H}(X, \mathbf{B}\mathbb{Z})
  =: [X, K(n, \mathbb{Z})]
  \,.
$$

Here on the left we have the standard notation for the ordinary cohomology groups, and on the right their expression in terms of homotopy classes of maps into an [[Eilenberg-Mac Lane space]].

## Cohomology groups in nonabelian cohomology ##

The standard **counter-example** to keep in mind for a [[nonabelian cohomology]] set that does _not_ carry a group structure is "nonabelian cohomology in degree 1" that classifies $G$-[[principal bundle]]s, for $G$ some nonabelian group.

This cohomology set

$$
  H^1(X,G)
  := H(X, \mathbf{B}G)
  =:
  [X, \mathbf{B} G]
  \simeq
  G Bund(X)/_\sim
$$

clearly has no natural group structure on it, unless $G$ is in fact abelian (in which case $\mathbf{B}G$ is indeed a [[group object]], namely a [[2-group]]).

But when we pass from group-principal bundles to groupoid-principal bundles, then there may be cohomology sets with group structure even in nonabelian cohomology.

Let for instance $G_{(2)}$ be a [[2-group]], i.e. a [[groupoid]] with group structure, such as the automrophism 2-group $G_{(2)} := AUT(H) := Aut_{Grpd}(\mathbf{B}H)$ of an  ordinary group $H$, then there is the nonabelian cohomology set

$$
  H^1(X, G_{(2)}) := H(X, G_{(2)})
  \simeq G_{(2)} GrpdBund(X)/_\sim
  \,.
$$

and this does carry a _nonabelian_ (in general) group structure.

This is to be distinguished from the cohomology set

$$
  H^2(X, G_{(2)}) := H(X, \mathbf{B} G_{(2)})
  \simeq G_{(2)} Bund(X)/_\sim
$$

that classifies $G_{(2)}$ [[principal 2-bundle]]s as opposed to groupoid principal 1-bundles and which is not in general a group (unless $G_{(2)}$ in turn is sufficiently abelian).

For $G_{(2)} = AUT(H)$ both these cohomology sets play a role in the description of [[gerbe]]s (see [[gerbe (as a stack)]] and [[gerbe (in nonabelian cohomology)]]).

