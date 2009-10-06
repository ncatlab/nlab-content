#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

As every [[topos]], the category $PSh(X)$ of [[presheaf|presheaves]] is  [[cartesian monoidal category|cartesian]] [[closed monoidal category|closed monoidal]].

#Definition#

Let $S$ be a [[category]]. 

The standard **monoidal**  structure on presheaves $PSh := [S^{op}, Set]$ is the  [[cartesian monoidal category|cartesian monoidal structure]]. 

Recalling that [[limit]]s of [[presheaf|presheaves]] are computed objectwise, this is the pointwise [[cartesian monoidal category|cartesian]] product in [[Set]]: for two presheaves $F, G$ their product presheaf $F \times G$ is given by

$$
  F \times G : U \mapsto
  F(U) \times G(U)
  \,,
$$

where on the right the product is in [[Set]].


+-- {: .un_prop}
###### Proposition

The corresponding **[[internal hom]]**

$$
  [-,-] : PSh^{op} \times PSh \to PSh
$$

exists and is given by

$$
  [F,G] : U \mapsto Hom_{PSh}( Y(U)\times F, G )
  \,,
$$

where $Y : S \to [S^{op}, Set]$ is the [[Yoneda embedding]].

=--


+-- {: .proof}
###### Proof

First assume that $[F,G]$ exists, so that by the
[[adjoint functor|hom-adjunction isomorphism]]  we have
$Hom(R, [F,G]) \simeq Hom(R \times F, G)$. In particular, for each [[representable functor]] $R = Y(U)$ (with $Y$ the [[Yoneda embedding]]) and using the [[Yoneda lemma]] we get

$$
  \begin{aligned}
     [F,G](U) & \simeq Hom(Y(U), [F,G])
     \\
      & \simeq Hom(Y(U) \times F, G)
  \end{aligned}
  \,.
$$

So if the [[internal hom]] exists, it has to be of the form given. It remains to show that with this definition $[F,-]$ really is [[right adjoint]] to $-\otimes F$.

=--

See pages 46, 47 of 

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]].


## Definition in terms of homs of direct images ##

Often another, equivalent, expression is used to express the internal hom of presheaves:

Let $X$ be a [[site|pre-site]] with underlying [[category]] $S_X$. Recall from the discussion at [[site]] that just means that we have a category $S_X$ on which we consider [[presheaf|presheaves]] $F \in PSh(S_X) := [S_X^{op}, Set]$, but that it suggests that

* to each object $U \in PSh(X)$ and in particular to each $U \in S_X \hookrightarrow PSh(X)$ there is naturally associated the pre-site $U$ with underlying category the [[comma category]] $S_U = (Y/Y(U))$;

* that the canonical [[stuff, structure, property|forgetful]] [[functor]] $j^t_{U \to X} :  S_U \to S_X$, which can be thought of as a [[site|morphism of pre-sites]] $j_{U \to X} : X \to U$ induces the [[direct image]] functor $(j_{U \to X})_* : PSh(X) \to PSh(U)$ which we write $F \mapsto F|_U$.

Then in these terms the above **internal hom**  for presheaves

$$
  hom : PSh(X)^{op} \times PSh(X) \to PSh(X)
$$

is expressed for all $F,G \in PSh(X)$ by

$$
  hom(F,G) : U \mapsto Hom_{PSh(U)}(F|_U, G|_U)
  \,.
$$

## Relation of the two definitions ##

To see the equivalence of the two  definitions, notice

* that by the [[Yoneda lemma]] we have that $S_U$
is simply the [[over category]]
$S_U = S_X/U$;
* by the general properties of [[functors and comma categories]] there is an equivalence $PSh(S_X/U) \simeq PSh(S_X)/y(U)$;
* which identifies the functor $(-)|_U : PSh(S_X) \to PSh(S_U)$ with the functor 
$((-)\times y(U) \stackrel{p_2}{\to} y(U)) : PSh(S_X) \to PSh(S_X)/y(U)$;
* and that $Hom_{PSh(S_X)/y(U)}(y(U) \times F, y(U) \times G) \simeq Hom_{PSh(S_X)}(y(U) \times F, G)$.


#References#

The first definition is discussed for instance in section I.6 of

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]].

The second definition is discussed for instance in section 17.1 of

* Kashiwara-Shapira, [[Categories and Sheaves]]
