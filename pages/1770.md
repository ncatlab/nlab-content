# Idea #

Following the logic of [[space and quantity]], a _smooth space_ is, in full generality, a space that may be probed by standard smooth test spaces.

See [[generalized smooth space]] for more on the general idea and for examples and variations.

Here standard smooth test spaces may be taken to be smooth [[manifolds]]. But since [[manifolds]] themselves are built from gluing together smooth open balls $D^n_{int} \subset \mathbb{R}^n$, one may just as well consider just smooth balls as test spaces. Finally, since $D^n$ is diffeomorphic to $\mathbb{R}^n$, one can just as well take just the cartesian smooth spaces $\mathbb{R}^n$ as test objects.

#Definition#

The category of **smooth space**s is the [[sheaf]] [[topos]]

$$
  SmoothSp := Sh(Diff)
$$

of [[sheaf|sheaves]] on the [[site]] [[Diff]] of smooth manifolds equipped with its standard [[coverage]] ([[Grothendieck topology]]) given by open covers of manifolds.

Since $Diff$ is [[equivalence of categories|equivalent]] to the category of [[manifolds]] _embedded_ into $\mathbb{R}^\infty$, $Diff$ is an [[essentially small category]], so there are no size issues involved in this definition.

But since manifolds themselves are defined in terms of gluing conditons, the [[Grothendieck topos]] $SmoothSp$ depends on much less than all of $Diff$.

Let

$$
  Ball := \{ (D^n_{int} \to D^m_{int}) \in Diff | n,m \in \mathbb{N}\}
$$

and

$$
  CartSp := \{ (\mathbb{R}^n \to \mathbb{R}^m) \in Diff  | n,m \in \mathbb{N}\}
$$

be the full [[subcategory|subcategories]] $Ball$ and [[CartSp]] of $Diff$ on open balls and on cartesian spaces, respectively. Then the corresponding [[sheaf]] [[topos]]es are still those of smooth spaces:

$$
  \begin{aligned}
    SmoothSp &\simeq Sh(Ball)
    \\
     & \simeq Sh(CartSp)
  \end{aligned}
  \,.
$$

#Examples#

* The category of ordinary [[manifolds]] is a
  full subcategory of smooth spaces:
  $$
    Diff \hookrightarrow SmoothSp 
    \,.
  $$
  When one regards smooth spaces concretely as sheaves
  on $Diff$, then this inclusion is of course just the
  [[Yoneda embedding]].

* The full [[subcategory]] 
  $$
    DiffSp \subset SmoothSp
  $$
  on [[concrete sheaf|concrete sheaves]] is 
  called the
  category of [[diffeological spaces]].

  * The standard class of examples of smooth spaces that motivate their use even in cases where one starts out being intersted just in smooth [[manifolds]] are **mapping spaces**: for $X$ and $\Sigma$ two smooth spaces (possibly just ordinary smooth manifolds), by the [[closed monoidal structure on presheaves]] the **mapping space** $[\Sigma,X]$, i.e. the space of smooth maps $\Sigma \to X$ exists again naturally as a smooth. By the general formula it is given as a [[sheaf]] by the assignment

    $$
      [\Sigma,X] : U \mapsto SmoothSp(\Sigma \times U, X)
     \,.
    $$

    If $X$ and $\Sigma$ are ordinary manifolds, then the [[hom-set]] on the right sits inside that of the underlying sets $SmoothSp(\Sigma \times U , X) \subset Set(|\Sigma| \times |U|, |X| )$ so that $[\Sigma,X]$ is a [[diffeological space]].

    The above formula says that a $U$-parameterized family of maps $\Sigma \to X$ is smooth as a map into the smooth space $[\Sigma,X ]$ precisely if the corresponding map of sets $U \times \Sigma \to X$ is an ordinary morphism of smooth manifolds.

* The canonical examples of smooth spaces that
  are not diffeological spaces are the sheaves of
  (closed) differential forms:
  $$
    K^n : U \mapsto \Omega^n_{closed}(U)
    \,.
  $$

* The category 
  $$
    SimpSmoothSp :=
    SmoothSp^{\Delta^{op}}
  $$
  equivalently that of sheaves on $Diff$ with
  values in [[simplicial sets]]
  $$
    \cdots \simeq Sh(Diff, SSet)
  $$
  of [[simplicial objects]] in smooth spaces
  naturally carries the structure of a 
  [[homotopical category]] 
  (for instance the 
    [[model structure on simplicial sheaves]]
  or that of a Brown [[category of fibrant objects]]
  (if one restricts to locally Kan simplicial sheaves))
  and as such is a 
  [[presentable (∞,1)-category|presentation]]
  for the [[(∞,1)-topos]] of 
  [[smooth ∞-stacks]].

# Topos points and stalks #

+-- {: .un_lemma }
###### Lemma

For every $n \in N$ there is a 
[[point of a topos|topos point]]

$$
  D^n : Set \stackrel{\stackrel{(D^n)^*}{\leftarrow}}
    {\stackrel{D^n_*}{\to}}
    SmoothSp
$$

where the [[inverse image]] morphism -- the [[stalk]] --
is given on $A \in SmoothSp$ by

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

SmoothSp has [[point of a topos|enough points]]:
they are given by the
$D^n$ for $n \in \mathbb{N}$.

=--




#References#

The category $SmoothSp := Sh(Diff)$ is discussed with an eye towards its generalization to [[smooth ∞-stacks]]  in section 3.4, from page 29 on in

* Daniel Dugger, _Sheaves and Homotopy Theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html))


The [[point of a topos|topos points]] of $Sh(Diff)$ are discussed there in example 4.1.2 on p. 36. (they are mentioned before on p. 31).

[[!redirects smooth spaces]]
