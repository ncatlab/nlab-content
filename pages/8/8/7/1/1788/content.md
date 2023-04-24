
$$
  \array{
    \mathscr{V} \otimes f^\ast \mathscr{V}'
    \\
    \Big\downarrow\mathrlap{{}^{ \phi \otimes f^\ast(id) }}
    \\
    f^\ast( \mathscr{W}) 
      \otimes 
    f^\ast(\mathscr{V}')
  }
  \;\;\;
  =
  \;\;\;
$$

By definition we have

$$
  \left[
  \array{
    \mathscr{V}_{\mathcal{X}} 
    \boxtimes
    \mathscr{V}'_{\mathcal{X}'}
    \\
    \Big\downarrow\mathrlap{{}^{\phi_f \boxtimes id}}
    \\
    \mathscr{W}_{\mathcal{Y}} 
    \boxtimes
    \mathscr{V}'_{\mathcal{X}'}
  }
  \;\;\;\;
  \right]
  \;\;\;\;=\;\;\;\;
  \left[
  \array{
    \big(
      (pr_{\mathcal{X}})^\ast \mathscr{V}
    \big)
    \otimes
    \big(
      (pr_{\mathcal{X}'})^\ast \mathscr{V}'
    \big)
    \\
    \Big\downarrow\mathrlap{{}^{
      \Big(
        \big((pr_{\mathcal{X}})^\ast \phi\big)
        \otimes 
        (pr_{\mathcal{X}'})^\ast id_{\mathscr{V}'}
      \Big)_{f \times id}
    }}
    \\
    \big(
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
    \otimes
    \big(
      (pr_{\mathcal{X}'})^\ast \mathscr{V}'
    \big)
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \right]
$$


noticing here that 

$$
  \mathcal{X} \times \mathcal{X}'
  \overset{ pr_{\mathcal{X}'} }{\longrightarrow}
  \mathcal{X}'
  \;\;\;\;\;
  =
  \;\;\;\;\;
  \mathcal{X} \times \mathcal{X}' 
  \overset{ f \times id}{\longrightarrow}
  \mathcal{Y} \times \mathcal{X}' 
  \overset{ pr_{\mathcal{X}'} }{\longrightarrow}
  \mathcal{X}'
$$

this equals

$$
  \cdots
  \;\;\;\;=\;\;\;\;
  \left[
  \array{
    \big(
      (pr_{\mathcal{X}})^\ast \mathscr{V}
    \big)
    \otimes
    \big(
      (f \times id)^\ast
      (pr_{\mathcal{X}'})^\ast \mathscr{V}'
    \big)
    \\
    \Big\downarrow\mathrlap{{}^{
      \Big(
        \big((pr_{\mathcal{X}})^\ast \phi\big)
        \otimes 
        (f \times id)^\ast
        (pr_{\mathcal{X}'})^\ast id_{\mathscr{V}'}
      \Big)_{f \times id}
    }}
    \\
    \big(
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
    \otimes
    \big(
      (pr_{\mathcal{X}'})^\ast 
      \mathscr{V}'
    \big)
  }
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \right]
$$

which, by definition, has component maps

$$
  \array{
    \big(
      (pr_{\mathcal{X}})^\ast \mathscr{V}
    \big)
    \otimes
    \big(
      (f \times id)^\ast
      (pr_{\mathcal{X}'})^\ast \mathscr{V}'
    \big)
    \\
    \Big\downarrow\mathrlap{{}^{
      \Big(
        \big((pr_{\mathcal{X}})^\ast \phi\big)
        \otimes 
        (f \times id)^\ast
        (pr_{\mathcal{X}'})^\ast id_{\mathscr{V}'}
      \Big)
    }}
    \\
    \big(
      (f \times id)^\ast
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
    \otimes
    \big(
      (f \times id)^\ast
      (pr_{\mathcal{X}'})^\ast 
      \mathscr{V}'
    \big)
    \mathrlap{\,,}
  }
$$

where at the bottom we used that $(-)^\ast$ is strong monoidal.

By [[natural transformation|natural]] [[Frobenius reciprocity]], the image under $(f \times id)_!$ of this morphism is

$$
  (f \times id)_!(\cdots)
  \;\;=\;\;
  \array{
    \big(
      (f \times id)_!
      (pr_{\mathcal{X}})^\ast \mathscr{V}
    \big)
    \otimes
      (pr_{\mathcal{X}'})^\ast \mathscr{V}'
    \\
    \Big\downarrow\mathrlap{{}^{
        (f \times id)_!
        \big((pr_{\mathcal{X}})^\ast \phi\big)
        \otimes 
        (pr_{\mathcal{X}'})^\ast id_{\mathscr{V}'}
    }}
    \\
    \big(
      (f \times id)_!
      (f \times id)^\ast
      (pr_{\mathcal{Y}})^\ast \mathscr{W}
    \big)
    \otimes
    \big(
      (pr_{\mathcal{X}'})^\ast 
      \mathscr{V}'
    \big)
  }
$$



We shall denote morphisms in $\mathbf{C}_{sGrpd}$ as follows:

$$
  \phi_f
  \;\;\colon\;\;
  \left(
  \array{
    \mathscr{V}_{\mathcal{X}}
    &\overset{\phi}{\longrightarrow}&
    f^\ast \mathscr{W}_{\mathcal{Y}}
    \\
    \mathcal{X}
    &\overset{f}{\longrightarrow}&
    \mathcal{Y}
  }
  \right)
$$


Let $\mathbf{C}$ be a [[symmetric monoidal category|symmetric]] [[closed monoidal category]] [[sSet-enriched category]] with 

* [[tensor product]] denoted $(-)\otimes (-)$

* [[internal hom]] denoted $[-,-]$.

With this

$$
  \mathbf{C}^{\mathcal{X}} 
    \,\coloneqq\,
  sFunc\big(
    \mathcal{X}
    ,\,
    \mathbf{C}
  \big)
$$
becomes closed monoidal with the pointwise operations.

Furthermore, 

$$
  \mathbf{C}_{sGrpd}
  \;\coloneqq\;
  \int_{\mathcal{X} \in sGrpd} \mathbf{C}^{\mathcal{X}}
$$

becomes monoidal with respect to the [[external tensor product]]

which is defined first on morphisms which are constant in $sGrpd$ by 

$$
  \boxtimes
  \;\colon\;
  \mathbf{C}^{\mathcal{X}}
  \times
  \mathbf{C}^{\mathcal{Y}}
  \overset{
    (pr_{\mathcal{X}})^\ast
    \times
    (pr_{\mathcal{Y}})^\ast
  }{\longrightarrow}
  \mathbf{C}^{\mathcal{X} \times \mathcal{Y}}
  \times
  \mathbf{C}^{\mathcal{X} \times \mathcal{Y}}
  \overset{
    \otimes
  }{\longrightarrow}
  \mathbf{C}^{\mathcal{X} \times \mathcal{Y}}
$$

$$
  \left[
  \array{
    \mathscr{V}_{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{^{\phi_f}}
    \\
    \mathscr{W}_{\mathcal{Y}}
  }
  \;\;\,
  \right]
  \boxtimes
  \left[
  \array{
    \mathscr{V}'_{\mathcal{X}'}
    \\
    \Big\downarrow\mathrlap{^{\phi'_{f'}}}
    \\
    \mathscr{W}'_{\mathcal{Y}'}
  }
  \;\;\;
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
  \array{
    \mathscr{V}_{\mathcal{X}}
    \boxtimes
    \mathscr{V}'_{\mathcal{X}'}
    \\
    \Big\downarrow\mathrlap{{}^{\phi_f \boxtimes \phi'_{f'}}}
    \\
    \mathscr{W}_{\mathcal{Y}}
    \boxtimes
    \mathscr{W}'_{\mathcal{Y}'}
  }
  \;\;\;\;
  \right]
$$




If $\mathcal{C}$ is symmetric monoidal model then so is $C_{sGrpd}$ under the external tensor.


\begin{lemma}
  Let $\mathscr{V}'_{}$
\end{lemma}


Namely, first use projection formula to see that external tensor by objects preserves the fiberwise (acyclic) cofibrations. 

...

Let $\mathcal{C}$ an [[simplicial model category]].
We write $\cdot \,\colon\, sSet \times \mathcal{C} \to \mathcal{C}$ for its [[sSet]]-[[tensoring]]. (The following clearly works more generally, too.)

For $H \in Grp(sSet)$ a [[simplicial group]] and $X \in Obj(C)$, we may consider [[group actions]] $\rho \colon H \cdot X \to X$. Write $H Act(\mathcal{C})$ for the [[category]] these form.

Then for $\phi \colon H \to G$ a morphism in $Grp(sSet)$ we have the "restriction" functor

\[
  \label{RestrictionOfSimplicialGroupActions}
  \phi^\ast 
    \,\colon\, 
  G Act(\mathcal{C}) \to H Act(\mathcal{C})
  \,.
\]

At least for $\mathcal{C} = sSet$ itself, it is a classical elementary fact that such functors (eq:RestrictionOfSimplicialGroupActions) have [[left adjoints]] $\phi_!$ sending action on $X$ to the "left induced action $G \cdot_{_H} X$". We will need the following [[pushout]]-construction of such left-induced actions:

\begin{proposition}
  The functor (eq:RestrictionOfSimplicialGroupActions) has a [[left adjoint]] which sends $(X,\rho) \in H Act(\mathcal{C})$ to the unique $(G \cdot_{_H} X,\, \phi_!(\rho))$ that makes the following [[commuting diagram|diagram commute]] such that the bottom (and hence the top) square are [[pushouts]] in $\mathcal{C}$: 

\begin{tikzcd}
    \ast \cdot H \cdot X
    \ar[
      dr,
      "{ \mathrm{e} \cdot \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rr,
      "{ \mathrm{id} \,\cdot\, \rho }"{description}
    ]
    &&
    \ast \cdot X
    \ar[
      dd,
      equals
    ]
    \ar[
      dr,
      "{
        \mathrm{e} \,\cdot\, \iota
      }"{description}
    ]
    \\
    & 
    G \cdot G \cdot X
    \ar[
      rr,
      crossing over
    ]
    &&
    G \cdot \big( G  \cdot_{_H} X \big)
    \ar[
      dd,
      dashed,
      "{
        \phi_!(\rho)
      }"{description}
    ]
    \\
    H \cdot X
    \ar[
      from=uu,
      equals
    ]
    \ar[
      dr,
      "{ \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rr,
      "{ \rho }"{description, pos=.8}
    ]
    &&
    X
    \ar[
      dr,
      "{ \iota }"{description}
    ]
    \\
    & 
    G \cdot X
    \ar[
      from=uu,
      crossing over,
      "{
        \mu \,\cdot\, \mathrm{id}
      }"{description, pos=.3}
    ]
    \ar[rr]
    &&
    G \cdot_{_H} X
\end{tikzcd}

\end{proposition}
\begin{proof}
This is elementary, but we spell it out in pedantic detail.

We will denote the [[neutral element]] and the group operation in $H$ by

$$
  \mathrm{e} \colon \ast \to H
  ,\;\;\;\;
  \mu \colon H \cdot H \to X
  \,,
$$

respectively.

Given

* $(X, \rho) \,\in\, H Act(\mathcal{C})$

* $(Y, \rho_Y) \,\in\, G Act(\mathcal{C})$.

we need to establish a [[natural bijection]] of morphisms

$$
  \frac{
    G \cdot_{_H} X \overset{f}{\longrightarrow} X
  }{
    X \overset{\;\;\; f \circ \iota \;\;\;}{\longrightarrow} Y
  }
$$

where top one is $G$-equivariant, and the bottom one $H$-equivariant.

To have the top morphism means to have a commuting diagram as follows:

\begin{tikzcd}[
    row sep=10pt
  ]
    &
    \ast \cdot H \cdot X
    \ar[
      ddr,
      "{ \mathrm{e} \cdot \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rr,
      "{ \mathrm{id} \,\cdot\, \rho }"{description}
    ]
    \ar[
      dddd,
      equals
    ]
    &&
    \ast \cdot X
    \ar[
      dddd,
      equals
    ]
    \ar[
      ddr,
      "{ \mathrm{e} \,\cdot\, \iota }"{description}
    ]
    \\
    \\
    &
    & 
    G \cdot G \cdot X
    \ar[
      rr,
      crossing over,
      "{ \mathrm{id} \,\cdot\,   q }"{description, pos=.2}
    ]
    &&
    G \cdot \big( G  \cdot_{_H} X \big)
    \ar[
      dddd,
      dashed,
      "{
        \phi_!(\rho)
      }"{description}
    ]
    \ar[
      drr,
      "{ \mathrm{id} \,\cdot\, f }"{description}
    ]
    \\
    &
    && &&&
    G \cdot Y
    \ar[
      dddd,
      "{ \rho_{_Y} }"{description}
    ]
    \\
    &
    H \cdot X
    \ar[
      ddr,
      "{ \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rr,
      "{ \rho }"{description, pos=.8}
    ]
    &&
    X
    \ar[
      ddr,
      "{
        \iota
      }"{description}
    ]
    \\
    \\
    &
    & 
    G \cdot X
    \ar[
      from=uuuu,
      crossing over,
      "{
        \mu \,\cdot\, \mathrm{id}
      }"{description, pos=.3}
    ]
    \ar[
      rr,
      "{ q }"{description}
    ]
    &&
    G \cdot_{_H} X
    \ar[ 
      drr,
      "{ f }"{description}
    ]
    \\
    &
    &&&&& 
    Y
\end{tikzcd}

We claim that $f \circ q$ here is fixed to be 

$$
  f \circ q
  \;=\;
  \rho_Y
  \circ
  \big(
    \mathrm{id} \cdot (f \circ \iota)
  \big)
  \,.
$$

To see this, use the [[unitality]] of $\mu$ and $\rho$ 

\begin{tikzcd}[
    row sep=10pt
  ]
    {}
    &
    &
    \ast \cdot H \cdot X
    \ar[
      ddr,
      "{ \mathrm{e} \cdot \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rrr,
      "{ \mathrm{id} \,\cdot\, \rho }"{description}
    ]
    &&&
    \ast \cdot X
    \ar[
      dddd,
      equals
    ]
    \ar[
      ddr,
      "{ \mathrm{e} \,\cdot\, \iota }"{description}
    ]
    \\
    \\
    G \cdot \ast \cdot X
    &
    &
    & 
    G \cdot G \cdot X
    \ar[
      rrr,
      crossing over,
      "{ \mathrm{id} \,\cdot\,   q }"{description, pos=.2}
    ]
    &&&
    G \cdot \big( G  \cdot_{_H} X \big)
    \ar[
      dddd,
      dashed,
      "{
        \phi_!(\rho)
      }"{description}
    ]
    \ar[
      drr,
      "{ \mathrm{id} \,\cdot\, f }"{description}
    ]
    \\
    &
    \ast \cdot X
    \ar[
      dr,
      "{ \mathrm{e} \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rrr,
      equals
    ]
    &
    &
    & 
    X
    \ar[dr, equals]
    &&
    &&
    G \cdot Y
    \ar[
      dddd,
      "{ \rho_{_Y} }"{description}
    ]
    \\
    &
    &
    H \cdot X
    \ar[
      from=uuuu,
      crossing over,
      equals
    ]
    \ar[
      ddr,
      "{ \phi \cdot \mathrm{id} }"{description}
    ]
    \ar[
      rrr,
      "{ \rho }"{description, pos=.8}
    ]
    &&&
    X
    \ar[
      ddr,
      "{
        \iota
      }"{description}
    ]
    \\
    \\
    G \cdot X
    \ar[rrr, equals]
    \ar[from=uuuu, equals]
    &
    &
    & 
    G \cdot X
    \ar[
      from=uuuu,
      crossing over,
      "{
        \mu \,\cdot\, \mathrm{id}
      }"{description, pos=.8}
    ]
    \ar[
      rrr,
      "{ q }"{description}
    ]
    &&&
    G \cdot_{_H} X
    \ar[ 
      drr,
      "{ f }"{description}
    ]
    \\
    &
    &
    &&&&& &
    Y
    %
    \ar[
      from=3-1, 
      to=3-4,
      crossing over,
      "{ \mathrm{id} \cdot \mathrm{e} \cdot \mathrm{id} }"{description, pos=.3}
    ]
\end{tikzcd}

to compute as follows:

$$
  \begin{array}{l}
    f \circ q
    \\
    \;=\;
    f 
      \circ 
    q 
      \circ 
    (\mu \cdot \mathrm{id}) 
      \circ 
    (\mathrm{id} \cdot \mathrm{e} \cdot \mathrm{id})
    \\
    \;=\;
    f 
      \circ
    \phi_!(\rho)
      \circ
    (\mathrm{id} \cdot q)
      \circ 
    (\mathrm{id} \cdot \mathrm{e} \cdot \mathrm{id})
    \\
    \;=\;
    \rho_Y
      \circ
    (\mathrm{id} \cdot f)
      \circ
    (\mathrm{id} \cdot q)
      \circ 
    (\mathrm{id} \cdot \mathrm{e} \cdot \mathrm{id})
    \\
    \;=\;
    \rho_Y
      \circ
    (\mathrm{id} \cdot f)
      \circ
    \Big(
      \mathrm{id}
        \cdot
      \big( q \circ (\mathrm{e} \cdot \mathrm{id}) \big)
    \Big)
    \\
    \;=\;
    \rho_Y
      \circ
    \big(\mathrm{id} \cdot (f \circ \iota) \big)
  \end{array}
$$

Conversely, given such $f \circ \iota$ which is $H$-equivariant, then defining $f \circ q$ by this formula gives the bottom commuting square and hence extends to a $G$-equivariant map $G \cdot_H X \to Y$ by the universality of the pushout. 
\end{proof}

\begin{proposition}
  Let $\mathcal{C}$ be a [[combinatorial model category|combinatorial]] [[simplicial model category]] in which all [[objects]] are [[cofibrant objects|cofibrant]].
Then then [[pseudofunctor]]
$$
  \array{
    sGrpd &\longrightarrow& ModCat
    \\
    \mathcal{X} 
      &\mapsto& 
    sFunc(\mathcal{X},\,\mathcal{S})_{proj}
    \\
    \Big\downarrow\mathrlap{^f}
    && 
   \Big\downarrow\mathrlap{^f_!}
    \\
    \mathcal{Y}
    &\mapsto&
    sFunc(\mathcal{Y},\,\mathcal{S})_{proj}
  }
$$
is relative and proper.
\end{proposition}
\begin{proof}
  By general results in [[Higher Topos Theory]], the pseudofunctor presents the $\infty$-functor 
$$
  \array{
    Grpd_\infty &\longrightarrow& Cat_\infty
    \\
    \mathcal{X} 
      &\mapsto& 
    Func_\infty(\mathcal{X},\,L^W \mathcal{S})
  }
$$
By passage to [[homotopy category of an (infinity,1)-category|homotopy categories]] and using functoriality it follows that for $f$ an [[equivalence in an (infinity,1)-category|equivalence]], so is the [[derived functor]] of $f_!$, whence $f_!$ is a left [[Quillen equivalence]]. This shows that the pseudofunctor is relative.

Right properness is immediate: Since the weak equivalences in the projective [[model structure on functors]] are objectwise, the precomposition functor $f^\ast$ preserves weak equivalences for all $f$.

Left properness follows from Lemma ...: If $f$ is an acyclic cofibration of simplicial groupoids, then it is so on all connected components, and here it is an injective weak equivalence and hence an acyclic cofibration of simplicial sets on all endomorphisms objects. 

By groupoidiality we may without restriction assume that $f$ goes between simplicial groupoids whose set of objects is a singleton, hence that $f$ is of the form $f = \mathbf{B}\phi\colon \mathbf{B}H \to \mathbf{B}G$ for $\phi \colon H to G$ a homomorphism of [[simplicial groups]].

In this case the simplicial functors $\mathbf{B}H \to \mathcal{C}$ are equivalently $H$-actions in $\mathcal{C}$


Hence by lemma ... the functor $f_!$ is given on such an object $(X,\rho)$ by the following pushout:

$$
  \array{
    H \cdot X &\overset{\rho}{\longrightarrow}& X
    \\
    \mathllap{^{\phi \cdot id}}
    \big\downarrow
      &^{_{(po)}}& 
    \big\downarrow
    \\
    G \cdot X
    &\longrightarrow&
    G \cdot_{_H} X
  }
$$

Here the left morphism is an acyclic cofibration by the [[pushout-product axiom]] in the [[sSet]]-[[enriched model category]] $\mathcal{C}$, using the assumptions that $X$ is cofibrant in $\mathcal{X}$ and that $f$ and hence $\phi$ is an acyclic cofibration.
Therefore also the pushout morphism on the right is an acyclic cofibration, hence a weak equivalences.  
\end{proof}

***

Consider

* $k$ a [[field]];

* $Ch_\bullet(k)$ its [[category of chain complexes]] (unbounded) of $k$-[[vector spaces]] equipped with its projective [[model category]] [[structure]] (this is a [[proper model category|proper]] [[combinatorial model category]], by [this Prop.](model+structure+on+chain+complexes#StandardModelStructureOnUnboundedComplexes))

* $sCh_\bullet(k)$ the corresponding [[category of simplicial objects]] equipped with a [[Bousfield localization of model categories|left Bousfield localization]] of the corresponding [[Reedy model structure]] which makes it (by [this Prop.](model+structure+on+chain+complexes#LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes)) a [[simplicial model category]] whose [[underlying]] model category is [[Quillen equivalence|Quillen equivalent]] to $Ch_\bullet(k)$;

  ($sCh_\bullet(k)$ is, besides being [[simplicial model category|simplicial]], a [[left proper model category|left proper]] [[combinatorial model category]] by [this Prop.](Reedy+model+structure#LeftProperness) and [this Prop.](Bousfield+localization+of+model+categories#ExistenceForLeftProperCombinatorialSimplicialModelCategories))

* $sGrpd$ the category of Dwyer-Kan [[simplicial groupoids]] equipped with the projective [[model structure on simplicial groupoids]];

* $sFunc\big(\mathcal{X}, sCh_\bullet(k)\big)$, for $\mathcal{X} \in sGrpd$, the [[sSet]]-[[enriched functor category]] from the [[sSet-enriched category]] [[underlying]] $\mathcal{X}$ and equipped with the injective [[model structure on functors]]

  (this exists and is [[combinatorial model category|combinatorial]], by discussion [there](model+structure+on+functors#CombinatorialCase), because $sCh_\bullet(k)$ is combinatorial);

* $sFunc\big(-,sCh_\bullet(k)\big) \colon sGrpd \to Cat$ the [[pseudofunctor]] to [[Cat]] which on [[morphisms]] $f \colon \mathcal{X} \to \mathcal{Y}$ is given by [[left Kan extension]] $f_! \,\colon\, sFunc\big(\mathcal{X},sCh_\bullet(k)\big) \to sFunc\big(\mathcal{Y},sCh_\bullet(k)\big)$

  > mistake here: $f_!$ is left Quillen on the projective but not on the injective model structure...

* $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ the [[Grothendieck construction]] on this pseudofunctor.

\begin{proposition}
  The category $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ admits the corresponding [[integral model structure]].
\end{proposition}
\begin{proof}
  By the discussion [there](Grothendieck+construction+for+model+categories#Definition), it is sufficient to check that $sFunc\big(-,sCh_\bullet(k)\big)$

1. is "*relative*" as a functor to [[Ho(CombModCat)]] in that it sends weak equivalences in $sGrpd$ to [[Quillen equivalences]];

1. is "*proper*" in that

   1. for $f$ an [[acyclic fibration]] in $sGrpd$ the induced [[right Quillen functor]] $f^\ast$ preservers weak equivalences.

   1. for $f$ an [[acyclic cofibration]] in $sGrpd$ the induced [[left Quillen functor]] $f_!$ preservers weak equivalences,


We discuss these conditions in turn:

1. To see relative-ness:

   By general facts in *[[Higher Topos Theory]]* and using the [[stable Dold-Kan correspondence]], our functor [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-functor|$\infty$-functor]] $Func_\infty\big(-; (H k) Mod\big) \,\colon\, Grpd_\infty \to (H k) Mod$ assigning to base-[[infinity-groupoids|$\infty$-groupoids]] their [[stable (infinity,1)-categories|stable $\infty$-categories]] of [[parameterized spectra|parameterized]] [[Eilenberg-MacLane spectrum|$H \mathbb{C}$]]-[[module spectra]] ("[[infinity-local system|$\infty$-local systems]]"). By $\infty$-functoriality, this preserves [[equivalence in an (infinity,1)-category|$\infty$-equivalences]] which here means that weak equivalences $f$ in $sGrpd$ are sent to [[derived functors]] $\mathbb{L} f_!$ that, in particular, induce [[equivalence of categories|equivalences]] on the [[homotopy category of an (infinity,1)-category|homotopy categories of $\infty$-catgories]], hence of [[homotopy category of a model category|homotopy categories of model categories]]. But this  means that [[Quillen adjunction]] $f_! \dashv f^\ast$ induced by an equivalence $f$ is indeed a [[Quillen equivalence]].

1. To see properness:

   1. Recall that the weak equivalences in [[model structure on functors]] are objectwise in $sGrpd$ the weak equivalences in $sCh_\bullet$. This immediately implies that $f^\ast$ (given by precomposition of functors) preserves weak equivalences (no matter the nature of $f$).

   1. We will show that $f_!$ preserves weak equivalences (again independently of the nature of $f$, even) by arguing that it essentially acts as its own derived functor already.

This last argument occupies the remainder of the proof:

> The following is besides the point, since it is referring to the injective model structure where it should be referring to the projective one. Will fix...

First observe that, while not all chain complexes are cofibrant ([this remark](model+structure+on+chain+complexes#NotAllUnboundedComplexesAreProjectivelyCofibrant)), *all [[bounded-below chain complexes]] are cofibrant* (by [this Prop.](model+structure+on+chain+complexes#BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant) and using that we are working over a [[field]] all whose [[modules]], namely [[vector spaces]], are [[projective module|projective]], by [this Prop.](projective+module#ModuleOverAFieldIsProjective) ).

But every chain complex $V_\bullet \,\in\, Ch_\bullet(k)$ is the [[colimit]] over its [[cotower]] of $n$-[[connective covers]] 

$$
  V_\bullet
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \big(
  \cdots
  \hookrightarrow
  cn_{\geq n+1} V_\bullet
  \hookrightarrow
  cn_{\geq n} V_\bullet
  \hookrightarrow
  cn_{\geq n-1} V_\bullet
  \cdots
  \big)
  \,,
$$
and since [[colimits]] of [[simplicial objects]] are computed degreewise (by [[limits of presheaves are computed objectwise|general facts]]), the same holds for any functor of simplicial chain complexes $V^\bullet_\bullet(-) \in sFunc\big(\mathcal{X}, sCh_\bullet(k)\big)$:
$$
  V^\bullet_\bullet(-)
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \big(
  \cdots
  \hookrightarrow
  cn_{\geq n+1} V^\bullet_\bullet(-)
  \hookrightarrow
  cn_{\geq n} V^\bullet_\bullet(-)
  \hookrightarrow
  cn_{\geq n-1} V^\bullet_\bullet(-)
  \cdots
  \big)
$$
(where the [[connective cover]]-constructions now act objectwise as before, for each $\mathcal{X} \in sGrpd$ and $[k] \in \Delta$).

With this and since [[left adjoints preserve colimits]], we find that 

$$
  f_! V^\bullet_\bullet(-)
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \Big(
  \cdots
  \hookrightarrow
  f_! \big(cn_{\geq n+1} V^\bullet_\bullet(-)\big)
  \hookrightarrow
  f_! \big(cn_{\geq n} V^\bullet_\bullet(-)\big)
  \hookrightarrow
  f_!\big(cn_{\geq n-1} V^\bullet_\bullet(-)\big)
  \cdots
  \Big)
  \,.
$$

Now we claim that each $cn_{\geq n} V^\bullet_\bullet(-)$ is a [[cofibrant object]] in $sFunc\big(sGrpd, sCh_\bullet(k)\big)$. Because:

Since we are using the injective [[model structure on functors]], we need to see that for $\mathcal{X} \in sGrpd$ the object $cn_{\geq n} V^\bullet_\bullet(\mathcal{X})$ is cofibrant in the Bousfield localized Reedy model structure. Since left Bousfield localization does not change the class of [[cofibrations]] ([by definition](Bousfield+localization+of+model+categories#DefinitionOfLeftBousfieldLocalizations)) we are reduced to arguing this for plain [[Reedy model structure|Reedy cofibrancy]]. 
Here, again [by definition](Reedy+model+structure#ReedyModelStructure),
this means that we need to show that the [comparison maps](Reedy+model+structure#eq:ComparisonMapsFromLatchingToMatchingObject) $L_r(-) \to (-)_r$ from its [[latching objects]] are cofibrations in $Ch_\bullet(k)$.

But since $Ch_\bullet(k)$ is an [[abelian category]] (see [there](category+of+chain \+complexes#AbelianCategoryStructure)), it follows (by [this prop.](Reedy+model+structure#LatchingInAbelianCategoryIsDegeneracySubobject)) that $L_r(-) \to (-)_r$ is a monomorphism on our objects. Monomorphisms are cofibrations in the [[model structure on chain complexes]] over a [[field]] (where all injections are split) iff their [[cokernel]] is cofibrant (by [this Prop.](model+structure+on+chain+complexes#StandardModelStructureOnUnboundedComplexes)). But since we are dealing with maps between $n$-connective covers, also the cokernels are $n$-connective and hence cofibrant by the above argument. QED.

It follows that the [[left Quillen functor]] $f_!$ on the right hand side in the above formula is applied to cofibrant objects and hence coincides with its [[derived functor]] there, thus sending weak equivalences to weak equivalences ([Ken Brown's lemma](Introduction+to+Homotopy+Theory#KenBrownLemma)). 

So far this means that $f_!$ sends any weak equivalence to a colimit, in the [[arrow category]], of weak equivalences between stages in the [[connective cover]]-[[cotowers]] of the given objects. But, by the same cofibrancy argument just invoked, the structure morphisms in these cotowers are (monomorphisms and hence) cofibrations, so that this colimit is a [[homotopy colimit]] (see [there](homotopy+limit#CotowerColimits)) and hence preserves weak equivalences. 
This concludes the proof that also $f_!$ preserves weak equivalences. 
\end{proof}



