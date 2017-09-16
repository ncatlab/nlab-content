#Idea#

As every [[topos]], the category $PSh(X)$ of [[presheaf|presheaves]] is  [[cartesian monoidal category|cartesian]] [[closed monoidal category|closed mnonoidal]].

#Definition#

Let $S$ be a [[category]]. 

The standard **monoidal**  structure on presheaves $PSh := [S^{op}, Set]$ is the pointwise [[cartesian monoidal category|cartesian]] product in [[Set]]: for two presheaves $F, G$ their product presheaf $F \times G$ is given by

$$
  F \times G : U \mapsto
  F(U) \times G(U)
  \,,
$$

where on the right the product is in [[Set]].

By the [[adjoint functor|hom-adjunction isomorphism]] it follows that the corresponding **internal hom**

$$
  [-,-] : PSh^{op} \times PSh \to PSh
$$

is given by

$$
  [F,G] : U \mapsto Hom_{PSh}( Y(U)\times F, G )
  \,,
$$

where $Y : S \to [S^{op}, Set]$ is the [[Yoneda embedding]].


## Definition in terms of homs of direct images ##

+-- {: .query}

[[Urs Schreiber|Urs]]: I have to admit that I am not entirely sure how to show that the following reproduces the above. It must be simple and I seem to almost see how to do the computation, but I must be missing something. Help is appreciated.

[[Todd Trimble|Todd]]: Hi. I've already sent a detailed email, but in a nutshell, it boils down to 
* This $S_U$ is nothing but $S_X/U$. 
* $PreSh(S_X/U)$ is equivalent to $PreSh(S_X)/y(U)$. 
* The functor $F \mapsto F|U$ is thereby identified with the functor $F \mapsto y(U) \times F$, viewed in the comma category $PreSh(S_X)/y(U)$. When you calculate the hom of maps $y(U) \times F \to y(U) \times G$ in this comma category, you get the hom of maps $y(U) \times F \to G$. 

=--

Let $X$ be a [[site|pre-site]] with underlying [[category]] $S_X$. Recall from the discussion at [[site]] that just means that we have a category $S_X$ on which we consider [[presheaf|presheaves]] $F \in PSh(S_X) := [S_X^{op}, Set]$, but that it suggests that

* to each object $U \in PSh(X)$ and in particular to each $U \in S_X \hookrightarrow PSh(X)$ there is naturally associated the pre-site $U$ with underlying category the [[comma category]] $S_U = (Y/Y(U))$;

* that the canonical [[stuff, structure, property|forgetful]] [[functor]] $j^t_{U \to X} :  S_U \to S_X$, which can be thought of as a [[site|morphism of pre-sites]] $j_{U \to X} : X \to U$ induces the [[direct image]] functor $(j_{U \to X})_* : PSh(X) \to PSh(U)$ which we write $F \mapsto F|_U$.

The **internal hom**  for presheaves

$$
  hom : PSh(X)^{op} \times PSh(X) \to PSh(X)
$$

is given for all $F,G \in PSh(X)$ by

$$
  hom(F,G) : U \mapsto Hom_{PSh(U)}(F|_U, G|_U)
  \,.
$$

#References#

The first definition is discussed for instance in section I.6 of

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]].

The second definition is discussed for instance in section 17.1 of

* Kashiwara-Shapira, [[Categories and Sheaves]]
