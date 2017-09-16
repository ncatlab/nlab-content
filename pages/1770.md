
# Idea #

Following the logic of [[space and quantity]], a _smooth space_ is, in full generality, a space that may be probed by standard smooth test spaces.

See [[generalized smooth space]] for more on the general idea and for examples and variations.

Here standard smooth test spaces may be taken to be smooth [[manifold]]s. But since [[manifold]]s themselves are built from gluing together smooth open balls $D^n_{int} \subset \mathbb{R}^n$, one may just as well consider just smooth balls as test spaces. Finally, since $D^n$ is diffeomorphic to $\mathbb{R}^n$, one can just as well take just the cartesian smooth spaces $\mathbb{R}^n$ as test objects.

#Definition#

The category of **smooth space**s is the [[sheaf]] [[topos]]

$$
  SmoothSpaces := Sh(Diff)
$$

of [[sheaf|sheaves]] on a small version of the [[site]] [[Diff]] of smooth manifolds equipped with its standard [[coverage]] ([[Grothendieck topology]]) given by open covers of manifolds.

One may for instance take $Diff$ to be the category of [[manifold]]s _embedded_ into $\mathbb{R}^\infty$. This makes $Diff$ a [[small category]].

But since manifolds themselves are defined in terms of gluing conditons, the [[Grothendieck topos]] $SmoothSpaces$ depends on much less than all of $Diff$.

Let

$$
  Balls := \{ (D^n_{int} \to D^m_{int}) \in Diff | n,m \in \mathbb{N}\}
$$

and

$$
  CartesianSpaces := \{ (\mathbb{R}^n \to \mathbb{R}^m) \in Diff  | n,m \in \mathbb{N}\}
$$

be the full [[subcategory|subcategories]] of $Diff$ on open balls and on cartesian manifolds, respectively. Then the corresponding [[sheaf]] [[topos]]s are still those of smooth spaces:

$$
  \begin{aligned}
    SmoothSpaces &\simeq Sh(Balls)
    \\
     & \simeq Sh(CartesianSpaces)
  \end{aligned}
  \,.
$$

#Examples#

* The category of ordinary [[manifold]]s is a
  full subcategory of smooth spaces:
  $$
    Diff \hookrightarrow SmoothSpaces 
    \,.
  $$
  When one regards smooth spaces concretely as sheaves
  on $Diff$, then this inclusion is of course just the
  [[Yoneda embedding]].

* The full [[subcategory]] 
  $$
    DiffeologicalSpaces \subset SmoothSpaces
  $$
  on [[concrete sheaf|concrete sheaves]] is 
  called the
  category of [[diffeological space]]s..

* The canonical examples of smooth spaces that
  are not diffeological spaces are the sheaves of
  (closed) differential forms:
  $$
    K^n : U \mapsto \Omega^n_{closed}(U)
    \,.
  $$

* The category 
  $$
    SimpSmoothSpaces :=
    SmoothSpaces^{\Delta^{op}}
  $$
  equivalently that of sheaves on $Diff$ with
  values in [[simplicial set]]s
  $$
    \cdots \simeq Sh(Diff, SSet)
  $$
  of [[simplicial object]]s in smooth spaces
  naturally carries the structure of a 
  [[homotopical category]] 
  (for instance the 
    [[model structure on simplicial sheaves]]
  or that of a Brown [[category of fibrant objects]]
  (if one restricts to locally Kan simplicial sheaves))
  and as such is a 
  [[presentable (infinity,1)-category|presentation]]
  for the [[(infinity,1)-topos]] of 
  [[smooth infinity-stack]]s.


# Topos points and stalks #


+-- {: .un_lemma }
###### Lemma

For every $n \in N$ there is a 
[[point of a topos|topos point]]

$$
  D^n : Set \stackrel{\stackrel{(D^n)^*}{\leftarrow}}
    {\stackrel{D^n_*}{\to}}
    SmoothSpaces
$$

where the [[inverse image]] morphism -- the [[stalk]] --
is given on $A \in SmoothSpaces$ by

$$
  (D^n)^* A :=
  \colim_{\mathbb{R}^n \supset U \ni 0} A(U)
  \,,
$$

where the colimit is over all open neighbourhoods of the
origin in $\mathbb{R}^n$.

=--

+-- {: .un_lemma }
###### Lemma

SmoothSpaces has [[point of a topos|enough points]]:
they are given by the
$D^n$ for $n \in \mathbb{N}$.

=--




#References#

The category $SmoothSpaces := Sh(Diff)$ is discussed with an eye towards its generalization to [[smooth infinity-stack]]s  in section 3.4, from page 29 on in

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html))


The [[point of a topos|topos points]] of $Sh(Diff)$ are discussed there in example 4.1.2 on p. 36. (they are mentioned before on p. 31).