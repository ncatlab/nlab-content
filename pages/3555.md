
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

If an [[(∞,1)-topos]] $\mathbf{H}$ is that of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]] on (the [[site]] of [[category of open subsets|open subsets]] of) a [[paracompact space|paracompact]] [[topological space]] -- $\mathbf{H} = Sh_{(\infty,1)}(X)$ --  then its **shape** is the _strong shape_ of $X$ in the sense of [[shape theory]]: a [[pro-object]] $Shp(X)$ in the [[category]] of [[CW-complexes]].

It turns out that $Shp(X)$ may be extracted in a canonical fashion from just the [[(∞,1)-topos]] $Sh_{(\infty,1)}(X)$, and in a way that makes sense for any [[(∞,1)-topos]]. This then gives a definition of shape of general $(\infty,1)$-toposes.

## Definition
 {#Definition}

We state three somewhat different-looking definitions, and show that they are all equivalent to each other.


\begin{definition}\label{ShapeOfAnInfinityTopos}
**(shape of an $\infty$-topos -- [Toën-Vezzosi 2002, Def. 5.3.2](#ToenVezzosi02))**
\linebreak
The composite [[(∞,1)-functor]]

$$
  Shp 
  \;\colon\; 
  (\infty,1)Topos 
     \stackrel{Y}{\to}  
  Func((\infty,1)Topos, \infty Grpd)^{op}
      \stackrel{Lex(PSh(-), \infty Grpd)}{\to}
      AccLex(\infty Grpd, \infty Grpd)^{op}
     \simeq
       Pro \infty Grpd
$$

is the **shape functor** . Its value 

$$
  Shp(\mathbf{H}) = 
  (\infty,1)Topos
  \big(
    \mathbf{H}
    ,\, 
    PSh(-)
  \big)
$$ 

on an $(\infty,1)$-topos $\mathbf{H}$ is the **shape** of $\mathbf{H}$.
\end{definition}

Here:

* [[(∞,1)Topos]] is the [[(∞,1)-category]] of [[(∞,1)-topos]]es;

* [[∞Grpd]] is the $(\infty,1)$-category of [[∞-groupoid]]s;

* $Y$ is the [[(∞,1)-Yoneda embedding]];

* $Func(-,-)$ is the [[(∞,1)-category of (∞,1)-functors]];

* $AccLex(-,-) \subset (\infty,1)Func(-,-)$ is the full [[sub-(∞,1)-category]]
  of the [[(∞,1)-category of (∞,1)-functors]] on those which are left [[exact functor]]s (preserve finite [[(∞,1)-limit]]s) and also [[accessible (∞,1)-functor|accessible]].

* $PSh(-) : \infty Grpd \to (\infty,1)Topos$ is the functor that 
  produces the [[(∞,1)-category of (∞,1)-presheaves]] $Func(X^{op}, \infty Grpd)$ on $X$ (equivalently on the equivalent [[opposite (∞,1)-category|opposite ∞-groupoid]] $X^{op}$);

* $Pro \infty Grpd$ is the [[pro-object in an (∞,1)-category|(∞,1)-category of pro-objects]] in $\infty Grpd$.

That this does indeed land in accessible left exact functors follows from the equivalence to the following definition, see Rem. \ref{ShapeIsLexAndAccessible} below.

Notice (see [here](https://ncatlab.org/nlab/show/infinity1-topos#GlobalSectionsGeometricMorphism)) that for every [[(∞,1)-topos]] $\mathbf{H}$ there is a unique [[geometric morphism]]

$$
  (LConst \dashv \Gamma)   
  \;\colon\; 
  \mathbf{H} 
  \underoverset
    { \underset{\Gamma}{\longrightarrow} }
    { \overset{LConst}{\longleftarrow} }
    { \bot }
  \infty Grpd
  \,,
$$

where 

* [[∞Grpd]] is the $(\infty,1)$-topos of [[∞-groupoids]]

* $\Gamma$ is the [[global sections]] [[(∞,1)-functor]] 

* $LConst$ is the [[constant ∞-stack]] functor.


\begin{definition}\label{LurieShapeOfAnInfinityTopos}
**(shape of an $\infty$-topos -- [Lurie 2009, Def. 7.1.6.3](#Lurie09))**
\linebreak
The *shape* of an [[(infinity,1)-topos|$(\infty,1)$-topos]] $\mathbf{H}$ is the composite [[(infinity,1)-functor|$(\infty,1)$-functor]]

$$
  Shp(\mathbf{H}) 
  \;\coloneqq\; 
  \Gamma \circ LConst
  \;\;:\;\;
  \infty Grpd \stackrel{LConst}{\to}
  \mathbf{H}
  \stackrel{\;\;\Gamma\;\;}{\to}
  \infty Grpd
$$

regarded as a [[pro-object in an (infinity,1)-category|pro-]][[infinity-groupoid|$\infty$-groupoid]]:

$$
  Shp(\mathbf{H})
  \;\in\;
  Pro(\infty Grpd)
  \;=\;
  Lex(\infty Grpd, \infty Grpd)^{op}
  \,.
$$
\end{definition}

\begin{proposition}\label{ShapeIsGlobalSectionsOfLConst}
Def. \ref{ShapeOfAnInfinityTopos}
and Def. \ref{LurieShapeOfAnInfinityTopos} are equivalent.
\end{proposition}
\begin{proof}
For $X \in $ [[∞Grpd]] we have by the [[(∞,1)-Grothendieck construction]]-theorem and using that up to equivalence every morphism of $\infty$-groupoids is a [[Cartesian fibration]] (see there) that 

$$
  Func(X,\infty Grpd) 
  \;\simeq\; 
  \infty Grpd_{/X}
$$ 

is the [[slice (∞,1)-category]].  Moreover, by [this theorem](limit+in+a+quasi-category#WithValInooGrpd) about limits in ∞Grpd we have that the terminal geometric morphism $Hom(*,-): [X, \infty Grpd] \to \infty Grpd$ is the canonical projection $\infty Grpd/ X \to \infty Grpd$. This means that it is an [[etale geometric morphism]]. So for any [[geometric morphism]] $f : \mathbf{H} \to [X, \infty Grpd]$  we have a system of [[adjoint (∞,1)-functor]]s

$$
  (LConst \dashv \Gamma)
  \;\colon\;
  \mathbf{H}
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
   \infty Grpd/X
    \stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}    
   \infty Grpd
  \,.
$$

whose composite is the [[global section]] geometric morphism as indicated, because that is terminal.

Notice that in $\infty Grpd/X$ there is a canonical morphism

$$
  (* \to  \pi^* X) 
  \;\coloneqq\; 
  (X \stackrel{(Id,Id)}{\to} X \times X)
  \,.
$$

The image of this under $f^*$ is (using that this preserves the terminal object) a morphism  in $\mathbf{H}$ of the form

$$
  * \to f^* \pi^* X = LConst X
  \,.
$$


Conversely, given a morphism of the form $* \to LConst X$ in $\mathbf{H}$ we obtain the [[base change geometric morphism]] of [[slice (infinity,1)-topos|slice $(\infty,1)$-toposes]]

$$
  \mathbf{H} 
  \,\simeq\, 
   \mathbf{H}_{/*} 
   \xrightarrow{\;\;} 
   \mathbf{H}_{/LConst X}
   \xrightarrow{\;\; \Gamma\;\;}  
  \infty Grpd_{/X}
  \,.
$$

One checks that these constructions establish an equivalence

$$
  (\infty,1)Topos
  \big(
    \mathbf{H}
    ,\,
    \infty Grpd_{/X}
  \big)
  \;\simeq\;
  \mathbf{H}
  (*, LConst X)
  \,.
$$

{#UsingThis} Using this, we find the following sequence of [[equivalence in an (infinity,1)-category|equiavlences]]:

$$
  \begin{aligned}
    Shp (\mathbf{H})   
    \;\colon\; 
    X 
    \;\;
   \mapsto 
   \;\;
   & 
   (\infty,1)Topos
   \big(
     \mathbf{H}
     ,\, 
     \infty Grpd_{/X}
   \big)
     \\
      & \simeq \mathbf{H}(*,LConst X)
     \\
      & \simeq \mathbf{H}(LConst *, LConst X)
     \\
      & \simeq \infty Grpd(*, \Gamma LConst X)
    \\
      & \simeq \Gamma \circ LConst(X)
  \end{aligned}   
  \,.
$$

The [[composition|composite]] of these is the equivalence to be shown.
\end{proof}

\begin{remark}\label{ShapeIsLexAndAccessible}
Prop. \ref{ShapeIsGlobalSectionsOfLConst} immediately implies that $Shp(\mathbf{H}) \;\colon\; \infty Grpd \to \infty Grpd$ according to Def. \ref{ShapeOfAnInfinityTopos} does preserve finite $(\infty,1)$-limits, since in the equivalent Def. \ref{LurieShapeOfAnInfinityTopos} this is manifest:
There $\Gamma$ clearly preserves all limits, [[right adjoints preserve limits|since]] it is a [[right adjoint]], and $LConst$ preserves of finite limits, since it is a [[left exact functor]] by definition.
Similarly, this makes manifest that $Shp(\mathbf{H})$ is [[accessible (infinity,1)-functor|accessible]], since $\Gamma$ and $LConst$ are both accessible.
\end{remark}



\begin{definition}\label{ShapeOfToposAsImageOfItsPointUnderProLeftAdjointToLConst}
**(shape of an $\infty$-topos -- [Hoyois 2013, p. 3](#Hoyois13))**
\linebreak
  For $(\Gamma \dashv LConst) \;\colon\; \mathbf{H} \to \infty Grpd$ an [[(infinity,1)-topos|$(\infty,1)$-topos]],
  write (with convenient overloading of notation)
  \[
    \label{ProLeftAdjointToLConst}
    \array{
      Shp 
      \;\colon\; 
      &
      \mathbf{H} 
      &\longrightarrow&
      Pro(\infty Grpd)
      \\
      &
      X
      &\mapsto&
      \mathbf{H}  
      \big(
        X
        ,\,
        LConst(-)
      \big)
    }
  \]
  for the [[pro-left adjoint]] to $LConst \,\colon\, \infty Grpd \to \mathbf{H},$ and say that the *shape of $\mathbf{H}$* is the image under this pro-left adjoint of its [[terminal object]] $\ast_{\mathbf{H}}$:
$$
  Shp(\mathbf{H})
  \;\coloneqq\;
  Shp(\ast_{\mathbf{H}})
  \,.
$$
\end{definition}

\begin{prop}
  Def. \ref{ShapeOfToposAsImageOfItsPointUnderProLeftAdjointToLConst}
  is equivalent to Def. \ref{LurieShapeOfAnInfinityTopos}
\end{prop}
\begin{proof}
Consider the following sequence of [[natural equivalence|natural]] [[equivalence in an (infinity,1)-category|equivalences]]:
$$
\begin{aligned}
  Shp(\mathbf{H})
  &
  \;\simeq\;
  \Gamma \circ LConst(-)
  \\
  &
  \;\simeq\;
  \infty Grpd
  \big(
    \ast
    ,\,
    \Gamma \circ LConst(-)
  \big)
  \\
  & 
  \;\simeq\;
  \mathbf{H}
  \big(
    LConst(\ast)
    ,\,
    LConst(-)
  \big)
  \\
  & \;\simeq\;
  \mathbf{H}
  \big(
    \ast_{\mathbf{H}}
    ,\,
    LConst(-)
  \big)
  \\
  & 
  \;\simeq\;
  Shp(\ast_{\mathbf{H}})
\end{aligned}
$$
Here the line is just Def. \ref{LurieShapeOfAnInfinityTopos} (alternatively: is Prop. \ref{ShapeIsGlobalSectionsOfLConst}), and the second line is, if one wishes, the geometric discreteness of plain $\infty$-groupoids.
The third line is the characteristic [hom-equivalences](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences) of the [[adjoint (infinity,1)-functor|adjunction]] $\Gamma \dashv LConst$ . In the second but last step we use that $LConst$, being a [[left exact functor]], [[preserved limit|preserves]] [[terminal object in an (infinity,1)-category|terminal objects]]. The last step is the definition (eq:ProLeftAdjointToLConst) of the [[pro-left adjoint]].
\end{proof}



\linebreak

## Examples

### Shape of a locally $\infty$-connected topos

Suppose that $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]], meaning that $\LConst$ has a [[left adjoint|left]] [[adjoint (infinity,1)-functor|$(\infty,1)$-functor]] $Shp$ (see at *[[shape modality]]*) which constructs the [[geometric homotopy groups in an (∞,1)-topos|homotopy ∞-groupoids]] of objects of $\mathbf{H}$.  Then $\Shape(\mathbf{H})$ is [[representable functor|represented]] by $Shp(*)\in \infty Grpd$, for we have the following sequence of [[natural equivalence|natural]] [[equivalences of ∞-groupoids]]:

$$
\begin{aligned}
Shape(\mathbf{H})(A) &\simeq \Gamma(LConst(A))\\
&\simeq Hom_{\infty Grpd}(*, \Gamma(LConst(A)))\\
&\simeq Hom_{\mathbf{H}}(LConst(*), LConst(A)) \\
&\simeq Hom_{\mathbf{H}}(*, LConst(A)) \\
&\simeq Hom_{\infty Grpd}(Shp(*),A).
\end{aligned}
$$

Thus, if we regard $Shp(*)$ as "the [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|fundamental ∞-groupoid]] of $\mathbf{H}$" --- which is reasonable since when $\mathbf{H}=Sh(X)$ consists of sheaves on a locally contractible [[topological space]] $X$, $Shp_{\mathbf{H}}(*)$ is equivalent to the usual [[fundamental ∞-groupoid]] of $X$ --- then we can regard the shape of an $(\infty,1)$-topos as a generalized version of the "homotopy $\infty$-groupoid" which nevertheless makes sense even for non-locally-contractible toposes, by taking values in the larger category of "pro-$\infty$-groupoids."

It follows also that $\mathbf{H}$ is not only locally ∞-connected but also [[∞-connected (∞,1)-topos|∞-connected]], then it has the shape of a point.


### Shape of an essential retract
 {#Retract}

The following is trivial to observe, but useful to note.

\begin{remark}
Let $(f_! \dashv f^* \dashv f_*) : \mathbf{H} \xrightarrow{\;\;} \mathbf{B}$ be an [[essential geometric morphism]] of $(\infty,1)$-toposes that exhibits $\mathbf{B}$ as an essential [[retract]] of $\mathbf{H}$ in that 

$$
  (Id \dashv Id)
  \;\;
  \simeq
  \;\;
  \mathbf{B}
    \underoverset
      {\underset{f^*}{\longrightarrow}} 
      {\overset{f_!}{\longleftarrow}}
      {\;\;\;\bot\;\;\;}
  \mathbf{H}
    \underoverset
      {\underset{f_*}{\longrightarrow}} 
      {\overset{f^*}{\longleftarrow}}
      {\;\;\;\bot\;\;\;}
  \mathbf{B}
  \,.
$$

Then the shape of $\mathbf{B}$ is equivalent to that of $\mathbf{H}$.
\end{remark}
\begin{proof}
Since $\infty Grpd$ is the [[terminal object in an (infinity,1)-category|terminal object]] in the [[(infinity,1)-category|$(\infty,1)$-category]] of [[infinity-stack (infinity,1)-topos|Grothendieck $(\infty,1)$-toposes]] and [[geometric morphisms]] (see [here](infinity1-topos#GlobalSectionsGeometricMorphism)), we have

$$
  \begin{aligned}
    & 
    (\infty Grpd 
      \xrightarrow{\;LConst_{\mathbf{B}}\;}
     \mathbf{B} 
       \xrightarrow{\;\Gamma_\mathbf{B}\;} 
     \infty Grpd)
    \\
    &
    \simeq
    (\infty Grpd 
      \xrightarrow{\;LConst_{\mathbf{B}}\;}
      \mathbf{B} 
      \xrightarrow{\;f^*\;} 
      \mathbf{H}   
      \xrightarrow{f_*} 
      \mathbf{B}
      \xrightarrow{\Gamma_\mathbf{B}}
     \infty Grpd)
    \\
    &
    \simeq
    (\infty Grpd 
     \xrightarrow{LConst_\mathbf{H}}
     \mathbf{H} 
     \xrightarrow{\Gamma_\mathbf{H}}
     \infty Grpd)    
  \end{aligned}
  \,.
$$
\end{proof}

\begin{example}\label{CohesiveInfinityToposHasTrivialShape}
**([[cohesive (∞,1)-topos]] has trivial shape)**
\linebreak
Every 

* $\infty$-topos which is both [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] and [[∞-connected (∞,1)-topos|$\infty$-connected]],

* in particular every [[cohesive (∞,1)-topos]] 

over $\infty Grpd$ has the shape of the point.
\end{example}
\begin{proof}
By definition $\mathbf{H}$ is $\infty$-connected if the [[constant ∞-stack]] [[inverse image]] $f^* = L Const$ is 

1. not only a left but also a [[right adjoint]];

1. is a [[full and faithful (∞,1)-functor]].

By standard properties of [[adjoint (∞,1)-functor]]s we have that a [[right adjoint]] $f^*$ is a [[full and faithful (∞,1)-functor]] precisely if the counit $f_! f^* \to Id$ is an [[equivalence in a quasi-category|equivalence]].

Equivalently, we can observe that a locally ∞-connected (∞,1)-topos is ∞-connected precisely when $Shp$ preserves the terminal object, and apply the above observation that the shape of a locally ∞-connected (∞,1)-topos is represented by $Shp(*)$.
\end{proof}

\begin{remark}\label{TrivialShapeAndGrosToposes}
**(trivial shape of gros $\infty$-toposes)**
\linebreak
  That [[cohesive (infinity,1)-toposes|cohesive $(\infty,1)$-toposes]] have trivial shape (Exp. \ref{CohesiveInfinityToposHasTrivialShape}) is a reflection of their characteristic nature as [[gros toposes]]: Rather than representing a single specific non-trivial space, cohesive $\infty$-toposes are gros $\infty$-categories *of spaces* (of geometric/cohesive spaces, specifically).

This is further brought out by Prop. \ref{ShapeOfSliceOfCohesiveInfinityTopos} below, in view of which Exp. \ref{CohesiveInfinityToposHasTrivialShape}, may be read as saying that the shape of a cohesive $\infty$-topos does not interfere with the cohesive shapes of its objects.
\end{remark}


### Shape of slice of a cohesive $\infty$-topos
 {#ShapeOfSlicesOfCohesiveInfinityToposes}


\begin{proposition}\label{ShapeOfSliceOfCohesiveInfinityTopos}
  If $\mathbf{H}$ is a [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] with [[shape modality]]
$$
  &#643;
  \;\;
   \colon
  \;\;
  \mathbf{H}
  \xrightarrow{\;Shp\;}
  \Grp_\infty
  \xrightarrow{\;Disc\;}
  \mathbf{H}
$$
then for every [[object]] $X \,\in\, \mathbf{H}$ the shape of the [[slice (infinity,1)-topos|slice $(\infty,1)$-topos]] $\mathbf{H}_{/X}$, according to Def. \ref{ShapeOfAnInfinityTopos}, is [[equivalence in an (infinity,1)-category|equivalently]] the [[shape modality|cohesive shape]] of $X$:
$$
  Shp
  \big(
    \mathbf{H}_{/X}
  \big)
  \;\;
    \simeq 
  \;\;
  Shp(X)
  \;\;\;\;\;
  \in
  \;
  Grp_\infty
  \xhookrightarrow{\;}
  Pro(Grp_\infty)
  \,.
$$
\end{proposition}
\begin{proof}
For $\mathbf{H}$ any [[(infinity,1)-topos|$(\infty,1)$-topos]]
and $X \,\in\, \mathbf{H}$ an [[object]], the [[slice (infinity,1)-topos|slice $(\infty,1)$-topos]] $\mathbf{H}_{/X}$ is related to $\mathbf{H}$ by the [[base change]] [[adjoint triple]] shown on the left here, together with, on the right, part of the [[adjoint quadruple]] that exhibits the [[cohesion]] of $\mathbf{H}$:

\begin{tikzcd}[column sep=large]
    \Gamma_X
    \;\;\;
    \colon
    &[-40pt]
    \mathbf{H}_{/X}
    \ar[
      rr,
      phantom,
      shift left=10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      phantom,
      shift left=-10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      shift left=20+10pt,
      "{ \sum_X }"{description}
    ]
    \ar[
      rr,
      shift left=-20+10pt,
      "{ \prod_X }"{description}
    ]
    &&
    \mathbf{H}
    \ar[
      ll,
      shift right=+10pt,
      "{ X \times (-) }"{description}
    ]
    \ar[
      rr,
      phantom,
      shift left=10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      phantom,
      shift left=-10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      shift left=20+10pt,
      "{ \mathrm{Shp} }"{description},
      "{\mathclap{\times}}"{description, pos=0}
    ]
    \ar[
      rr,
      shift left=-20+10pt,
      "{ \mathrm{Pnts} }"{description}
    ]
    &&
    \mathrm{Grp}_\infty
    \ar[
      ll,
      hook',
      shift right=+10pt,
      "{ \mathrm{Disc} }"{description}
    ]
    &[-40pt]
    \colon
    \;\;\;
    \mathrm{LConst}_X
\end{tikzcd}

By essential uniqueness of [[adjoint (infinity,1)-functors|adjoint $(\infty,1)$-functors]] ([here](adjoint+infinity1-functor#UniquenessOfAdjoints)) and of the terminal [[(infinity,1)-geometric morphism|$(\infty,1)$-geometric morphism]] ([here](infinity1-topos#GlobalSectionsGeometricMorphism)), the composite adjunction is the [[global section]] geometric morphism of the slice topos:

$$
  \big(
    \mathrm{LConst}_X
    \;\;
      \dashv
    \;\;
    \Gamma_X
  \big)
  \;\;\;\;\simeq\;\;\;\;
  \big(
    X \times \mathrm{Disc} (-)
    \;\;
    \dashv
    \;\;
    \mathrm{Pnts} \circ \prod_X
  \big)
  \,.
$$

Hence, by Prop. \ref{ShapeIsGlobalSectionsOfLConst}, we need to exhibit a [[natural equivalence]] of this form:

\[
  \label{CohesiveShapeCorepresentsShapeOfSlice}
  \Gamma_X \circ LConst_X(-)
  \;\;
  \simeq
  \;\;
  Grp_\infty
  \big(
    Shp(X)
    ,\,
    -
  \big)
\]

Therefore, consider, for $S_1, S_2 \,\in\, Grpd_\infty$, 
the following sequence of [[natural equivalences|natural]] [[equivalence in an (infinity,1)-category|equivalences]]:

$$
  \begin{aligned}
    &
    \mathrm{Grp}_\infty
    \big(
      S_1
      ,\,
      \Gamma_X
      \circ
      \mathrm{LConst}_X(S_2)
    \big)
    \\
    &
    \;\simeq\;
    \mathbf{H}_{/X}
    \big(
      \mathrm{LConst}_X( S_1 ) 
      ,\,
      \mathrm{LConst}_X(S_2)
    \big)
    \\
    & \;\simeq\;
    \mathbf{H}_{/X}
    \big(
      X \times \mathrm{Disc}(S_1)
      ,\,
      X \times \mathrm{Disc}(S_2)
    \big)    
    \\
    &
    \;\simeq\;
    \mathbf{H}
    \big(
      X \times \mathrm{Disc}(S_1)
      ,\,
      \mathrm{Disc}(S_2)
    \big)
    \\
    & \;\simeq\;
    \mathrm{Grp}_\infty
    \big(
      \mathrm{Shp}
      \big(
        X \times \mathrm{Disc}(S_1)
      \big)
      ,\,
      S_2
    \big)
    \\
    & \;\simeq\;
    \mathrm{Grp}_\infty
    \big(
      \mathrm{Shp}(X)
      \times
      S_1
      ,\,
      S_2
    \big)
    \\
    & \;\simeq\;
    \mathrm{Grp}_\infty
    \Big(
      S_1
      ,\,
      \mathrm{Grp}_\infty
      \big(
        \mathrm{Shp}(X)
        ,\,
        S_2
      \big)
    \Big)
  \end{aligned}
$$

Here the first four steps use the [hom-equivalences](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences) of the above adjunctions. The second but last step uses [[cohesion]], namely that the [[shape modality]] preserves [[finite product|finite]] [[homotopy products]] and is [[idempotent (infinity,1)-monad|idempotent]]. The last step is the [hom-equivalence](adjoint+infinity1-functor#CharacterizationInTermsOfHomEquivalences) for the [[cartesian monoidal (infinity,1)-category|cartesian monoidal]]-structure of [[∞Grpd]].

By the [[(infinity,1)-Yoneda lemma|$(\infty,1)$-Yoneda lemma]], this implies the equivalence (eq:CohesiveShapeCorepresentsShapeOfSlice) and hence the claim to be proven.
\end{proof}


### Shape of a topological space
 {#ShapeOfATopologicalSpace}

For a discussion of how the $(\infty,1)$-topos theoretic shape of the [[(infinity,1)-category of (infinity,1)-sheaves|$(\infty,1)$-category of $(\infty,1)$-sheaves]] $Sh_{(\infty,1)}(X)$ on a [[topological space]]  $X$ relates to the ordinary shape-theoretic _strong shape_ of the topological space $X$ see [this section](shape+theory#StrongShapeViaInfinityToposTheory) at *[[shape theory]]*.


## Related concepts

* [[étale homotopy]]

* [[shape modality]]

* [[coshape of an (∞,1)-topos]]


## References

The notion of shape of an $\infty$-topos first appears, in essentially the form of the above Def. \ref{ShapeOfAnInfinityTopos}, in: 

* {#ToenVezzosi02} [[Bertrand Toën]], [[Gabriele Vezzosi]],  Def. 5.3.2 in: _Segal topoi and stacks over Segal categories_, in: Proceedings of the Program _Stacks, Intersection theory and Non-abelian Hodge Theory_, MSRI, Berkeley, January-May 2002 ([arXiv:math/0212330](http://arxiv.org/abs/math/0212330)).

The concise formulation as $\Gamma \circ LConst(-)$, as in the above Def. \ref{LurieShapeOfAnInfinityTopos}, 
and discussion of relation to classical ([[strong shape|strong]]) [[shape theory]], of [[topological spaces]], is due to

* {#Lurie09} [[Jacob Lurie]], Section 7.1.6 of: _[[Higher Topos Theory]]_, 2009

The further re-formulation as the image of the [[terminal object]] under the [[pro-left adjoint]] to $LConst$ is highlighted in

* {#Hoyois13} [[Marc Hoyois]], Def. 2.3 _Higher Galois theory_, Algebraic & Geometric Topology __17__ 1 (2017) 567-643 ([arxiv/1506.07155](https://arxiv.org/abs/1506.07155), [doi:10.2140/agt.2017.17.567](https://doi.org/10.2140/agt.2017.17.567))

See also

* [[Ilan Barnea]], [[Yonatan Harpaz]], [[Geoffroy Horel]], Section 6 of: _Pro-categories in homotopy theory_, Algebraic & Geometric Topology 17 (2017) 567–643 ([arxiv:1507.01564](https://arxiv.org/abs/1507.01564), [doi:10.2140/agt.2017.17.567](https://doi.org/10.2140/agt.2017.17.567))


[[!redirects shape of an (∞,1)-topos]]

[[!redirects shape of an infinity1-topos]]


