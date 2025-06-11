
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

As every [[topos]], a  [[category of presheaves]] is  [[cartesian monoidal category|cartesian]] [[closed monoidal category|closed monoidal]].

## Definition


+-- {: .num_prop #CartesianClosedMonoidalnessOfCategoriesOfPresheaves}
###### Proposition
**([[cartesian closed category|cartesian closure]] of [[categories of presheaves]])**

Let $\mathcal{C}$ be a [[small category]] and write $[\mathcal{C}^{op}, Set]$ for its [[category of presheaves]].

This is 

1. a [[cartesian monoidal category]], whose [[Cartesian product]] is given objectwise in $\mathcal{C}$ by the [[Cartesian product]] in [[Set]]:

   for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$, their [[Cartesian product]] $\mathbf{X} \times \mathbf{Y}$ exists and is given by

   $$
     \mathbf{X} \times \mathbf{Y}
     \;\;\colon\;\;\phantom{A}
     \array{
       c_1 &\mapsto& \mathbf{X}(c_1) \times \mathbf{Y}(c_1)
       \\
       {}^{\mathllap{f}}\big\downarrow 
         &&
       \big\uparrow^{ \mathrlap{ \mathbf{X}(f) \times \mathbf{Y}(f) } }
       \\
       c_2 &\mapsto& \mathbf{X}(c_2) \times \mathbf{Y}(c_2)
     }
   $$

1. a [[cartesian closed category]], whose [[internal hom]] is given for $\mathbf{X}, \mathbf{Y} \in [\mathcal{C}^{op}, Set]$ by

   $$
     [\mathbf{X}, \mathbf{Y}]
     \;\;\colon\;\;\phantom{A}
     \array{
       c_1 &\mapsto& Hom_{[\mathcal{C}^{op}, Set]}( y(c_1) \times \mathbf{X}, \mathbf{Y} )
       \\
       {}^{ \mathllap{ f } }\big\downarrow 
         &&
       \big\uparrow^{ \mathrlap{ Hom_{[\mathcal{C}^{op}, Set]}( y(f) \times \mathbf{X}, \mathbf{Y} ) } }
       \\
       c_2 &\mapsto& Hom_{[\mathcal{C}^{op}, Set]}( y(c_2) \times \mathbf{X}, \mathbf{Y} )       
     }
   $$

   Here $y \;\colon\; \mathcal{C} \to [\mathcal{C}^{op}, Set]$ denotes the [[Yoneda embedding]] and $Hom_{[\mathcal{C}^{op}, Set]}(-,-)$ is the [[hom-functor]] on the [[category of presheaves]].

=--

(e.g. [MacLane-Moerdijk, section I.6, pages 46-47](#MacLaneMoerdijk)).

+-- {: .proof}
###### Proof

The first statement is a special case of the general fact that [[limits of presheaves are computed objectwise]].

For the second statement, first assume that $[\mathbf{X}, \mathbf{Y}]$ does exist. Then by the [[adjoint functor|hom-adjunction isomorphism]]  we have for any other presheaf $\mathbf{Z}$ a [[natural isomorphism]] of the form


\[
  \label{InternalHomIsoInPresheaves}
  Hom_{[\mathcal{C}^{op}, Set]}(\mathbf{Z}, [\mathbf{X},\mathbf{Y}]) 
    \;\simeq\; 
  Hom_{[\mathcal{C}^{op}, Set]}(\mathbf{Z} \times \mathbf{X}, \mathbf{Y})
  \,.
\]

This holds in particular for $\mathbf{Z} = y(c)$ a [[representable functor]] (i.e. in the [[essential image]] of the [[Yoneda embedding]]) and so the [[Yoneda lemma]] implies that if it exists, then $[\mathbf{X}, \mathbf{Y}]$ must have the claimed form:

$$
  \begin{aligned}
    [\mathbf{X}, \mathbf{Y}](c)
    & \simeq
    Hom_{[\mathcal{C}^{op}, Set]}( y(c), [\mathbf{X}, \mathbf{Y}] )
    \\
    & \simeq Hom_{ [\mathcal{C}^{op}, Set] }( y(c) \times \mathbf{X}, \mathbf{Y} )
    \,.
  \end{aligned}
$$

Hence it remains to show that this formula does make (eq:InternalHomIsoInPresheaves) hold generally.

For this we use the equivalent definition of [[adjoint functors]] in terms of the [[adjunction counit]] providing a system of [[universal arrows]].

Define a would-be [[adjunction counit]], which here is called an _[[evaluation]]_ morphism, by

$$
  \array{
    \mathbf{X} \times [\mathbf{X} , \mathbf{Y}]
    &\overset{ev}{\longrightarrow}&
    \mathbf{Y}
    \\
    \mathbf{X}(c) \times Hom_{[\mathcal{C}^{op}, Set]}(y(c) \times \mathbf{X}, \mathbf{Y})
    &\overset{ev_c}{\longrightarrow}&
    \mathbf{Y}(c)
    \\
    (x, \phi) &\mapsto& \phi_c( id_c, x )
  }
$$

Then it remains to show that for every morphism of presheaves of the form
$ \mathbf{X} \times \mathbf{A} \overset{\phantom{A}f\phantom{A}}{\longrightarrow} \mathbf{Y} $ there is a _unique_  morphism 
$\widetilde f \;\colon\; \mathbf{A} \longrightarrow [\mathbf{X}, \mathbf{Y}]$ such that

\[
  \label{UniversalArrowConditionForEvaluationMapInPresheaves}
  \array{
    \mathbf{X} \times \mathbf{A}
    && \overset{ \mathbf{X} \times \widetilde f  }{\longrightarrow} && 
    \mathbf{X} \times [\mathbf{X}, \mathbf{Y}]
    \\
    & {}_{\mathllap{ \mathrlap{f} }}\searrow 
      && 
    \swarrow_{ \mathrlap{  ev } }
    \\
    && \mathbf{Y}
  }
\]

The [[commuting diagram|commutativity]] of this diagram means in components at $c \in \mathcal{C}$ that, that for all $x \in \mathbf{X}(c)$ and $a \in \mathbf{A}(c)$ we have

$$
  \begin{aligned}
    ev_c( x, \widetilde f_c(a) )
    & \coloneqq
    (\widetilde f_c(a))_c( id_c, x )
    \\
    & = f_c( x, a )
  \end{aligned}
$$

Hence this fixes the component $\widetilde f_c(a)_c$ when its first argument is the [[identity morphism]] $id_c$. But let $g \;\colon\; d \to c$ be any morphism and chase $(id_c, x )$ through the naturality diagram for $\widetilde f_c(a)$:

$$
  \array{
    Hom_{\mathcal{C}}(c,c) \times \mathbf{X}(c)
    &\overset{ (\widetilde f_c(a))_c }{\longrightarrow}&
    \mathbf{Y}(c) 
    \\
    {}^{\mathllap{ g^\ast }}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{ g^\ast }}
    \\
    Hom_{\mathcal{C}}(d,c) \times \mathbf{X}(d)
    &\overset{ (\widetilde f_c(a))_d }{\longrightarrow}&
    \mathbf{Y}(d) 
  }
  \phantom{AAAA}
  \array{
    \{ (id_c, x ) \} &\longrightarrow& \{ f_c( x, a ) \}
    \\
    \big\downarrow && \big\downarrow 
    \\
    \{ (g, g^\ast(x)) \}  &\longrightarrow& \{ f_d( g^\ast(x), g^\ast(a) ) \}
  }
$$

This shows that $(\widetilde f_c(a))_d$ is fixed to be given by

\[
  \label{ComponentFormulaForEvaluationMapInPresheaves}
  (\widetilde f_c(a))_d( g, x' )
  \;=\;
  f_d( x', g^\ast(a) )
\]

at least on those pairs $(g,x')$ such that $x'$ is in the image of $g^\ast$.

But, finally, $(\widetilde f_c(a))_d$ is also natural in $c$

$$
  \array{
    \mathbf{A}(c)
    &\overset{ \widetilde f_c }{\longrightarrow}& [\mathbf{X},\mathbf{Y}](c)
    \\
    {}^{\mathllap{g^\ast}}\big\downarrow && \big\downarrow^{\mathrlap{g^\ast}}
    \\
    \mathbf{A}(d)
    &\overset{ \widetilde f_d }{\longrightarrow}& [\mathbf{X},\mathbf{Y}](d)
  }
$$

which implies that (eq:ComponentFormulaForEvaluationMapInPresheaves) must hold generally. Hence naturality implies that (eq:UniversalArrowConditionForEvaluationMapInPresheaves) indeed has a unique solution.

=--




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
  hom(F,G) = U \mapsto Hom_{PSh(U)}(F|_U, G|_U)
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

## Presheaves over a monoidal category

It is worth noting that in the case where $X$ is itself a [[monoidal category]] $(X, \otimes, I)$, $Psh(X)$ is equipped with another (bi)closed monoidal structure given by the [[Day convolution]] product and its componentwise right adjoints.  Let $F$ and $G$ be two presheaves over $X$.  Their tensor product $F \star G$ can be defined by the following [[coend]] formula:

$$F\star G = U \mapsto \int^{U_1,U_2\in X} Hom_X(U, U_1\otimes U_2) \times F(U_1) \times G(U_2)$$

Then we can define two right adjoints 

$$F\star - \dashv F \backslash -
\qquad -\star G \dashv - / G$$

by the following [[end]] formulas:

$$F \backslash H = V \mapsto \int_{U\in X} F(U) \to H(U\otimes V)$$
$$H / G = U \mapsto \int_{V\in X} G(V) \to H(U\otimes V)$$

In the case where the monoidal structure on $X$ is cartesian, the induced closed monoidal structure on $Psh(X)$ coincides with the cartesian closed structure described in the previous sections.

## Closed monoidal structure on sheaves

* The cartesian closure restricts from presheaves to [[categories of sheaves]] (e.g. [MacLane-Moerdijk, section III.6, p. 136-138](#MacLaneMoerdijk))

Let $X$ be a [[site]] with underlying category $S_X$. Write $PSh(X) = [S^{op}, Set]$ for the [[presheaf]] category of $X$ and $Sh(X)$ for the corresponding [[subcategory]] [[category of sheaves|of sheaves]].

The [[closed monoidal structure on presheaves]] restricts under the inclusion $Sh(X) \hookrightarrow PSh(X)$ to a closed monoidal structure on sheaves.

For $f : X \to Y$ a left exact [[site|morphism of sites]], there is for $F \in Sh(X)$, $F \in Sh(Y)$ a natural [[isomorphism]]
$$f_* hom(f^{-1}G, F) \simeq hom(G, f_* F).$$
Here $f_*$ is the [[direct image]] and $f^{-1}$ the [[inverse image]] operation.

## References

The first definition is discussed for instance in section I.6 of

* {#MacLaneMoerdijk} [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 

The second definition is discussed for instance in section 17.1 of

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

[[!redirects ccc structure on presheaves]]
[[!redirects cartesian closed structure on presheaves]]
[[!redirects cartesian closed monoidal structure on presheaves]]

[[!redirects cartesian closure of categories of presheaves]]
[[!redirects categories of presheaves are cartesian closed]]

[[!redirects closed monoidal structure on sheaves]]