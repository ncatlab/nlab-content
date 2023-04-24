
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[Grothendieck construction]] may be lifted from [[categories]] to [[model categories]], where it serves as a presentation for the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]].

## Definition
 {#Definition}

Let $\mathcal{M}$ be a [[model category]] and 

\[
  \label{ThePseudofunctor}
  \array{
    \mathcal{M} &\longrightarrow& Mod Cat
    \\
    X &\mapsto& F(X)
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \mathllap{^{f^\ast}}\Big\uparrow
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    Y &\mapsto& F(Y)
  }
\]

a [[pseudofunctor]], where $ModelCat$ is the [[2-category]] of model categories, [[Quillen adjunctions]] (pointing in the direction of their [[left adjoints]] $f_!$), and [[mate]]-pairs of [[natural isomorphisms]].  

We say that:

\begin{definition}\label{RelativePseudoFunctor}
$F$ is *[[relative functor]]* if for any [[weak equivalence]] $f$ in $M$, the associated Quillen adjunction $f_! \dashv f^*$ is a [[Quillen equivalence]].  
\end{definition}

\begin{definition}\label{ProperPseudofunctor}
$F$ is "*proper*", if when $f \colon A\to B$ is an [[acyclic cofibration]] (resp. an [[acyclic fibration]]) in $\mathcal{M}$ then $f_!$ (resp. $f^*$) preserves all [[weak equivalences]].
\end{definition}

\begin{definition}\label{IntegralModelStructure}
**(integral model structure)**
\linebreak
Given a [[pseudofunctor]] as in (eq:ThePseudofunctor),
we say that a morphism 
$$
  (f,\phi) 
   \;\colon\; 
  (X,A) \longrightarrow (Y,B)
$$ 
in its [[Grothendieck construction]] $\int_{X \in \mathcal{M}} F(X)$
(where $f \colon X\to Y$ in $\mathcal{M}$ and $\phi \colon f_!(A) \to B$ in $F(Y)$) is:

* an *integral equivalence* iff 

  1. $f \colon X \to Y$ is a [[weak equivalence]] in $\mathcal{M}$ 

  2. $f_!(Q A) \to f_!(A) \xrightarrow{\phi} B$ is a [[weak equivalence]] in $F(Y)$, where $Q$ is a [[cofibrant replacement]].  

     (Since $f_!\dashv f^*$ is a Quillen equivalence by relativeness, this is equivalent to the [[adjunct]] condition that $A \xrightarrow{\widetilde{\phi}} f^*(B) \to f^*(R B)$ is a weak equivalence in $F(X)$.)

* an *integral cofibration* iff 

  1. $f$ is a [[cofibration]] in $\mathcal{M}$ 

  1. $\phi \colon f_!(A) \to B$ is a [[cofibration]] in $F(Y)$.

* an *integral fibration* iff 

  1. $f$ is a [[fibration]] in $\mathcal{M}$ 

  1. the [[adjunct]] $\widetilde{\phi} \colon A \to f^*(B)$ is a [[fibration]] in $F(X)$.

\end{definition}

\begin{proposition}\label{ExistenceStatement}
If the pseudofunctor (eq:ThePseudofunctor) is relative (Def. \ref{RelativePseudoFunctor}) and proper (Def. \ref{ProperPseudofunctor}) then the classes of maps in Def. \ref{IntegralModelStructure}
make $\int_{X \in \mathcal{M}} F(X)$ a [[model category]].
\end{proposition}
This is [Harpaz & Prasma (2015), Theorem 3.0.12](#HarpazPrasma15).

## Properties

\begin{proposition}
Given a proper relative $F \colon \mathcal{M} \to ModelCat$, we can compose with the underlying [[(infinity,1)-functor|$(\infty,1)$-functor]] $Ho \colon ModelCat \to QCat$ with values in (say) [[quasicategories]].  
Since $F$ is relative, this map takes weak equivalences in $\mathcal{M}$ to [[equivalences of quasicategories]], so it induces a functor of quasicategories $Ho(M) \to Ho(QCat) = (\infty,1)Cat$.  The [[(∞,1)-Grothendieck construction]] of this functor is then equivalent, over $Ho(M)$, to the underlying $(\infty,1)$-category of the Grothendieck-construction model structure on $\int F$
\end{proposition}
([Harpaz & Prasma (2015), Proposition 3.1.2](#HarpazPrasma15))


## Examples

### Parameterized objects 
 {#ParameterizedObjects}

> under construction --- handle with care

#### Plain model structure

\begin{definition}
**(Notation)**
For 

1. $\mathbf{C} \in sSet Cat$ an [[sSet-enriched category]];

1. $\mathbf{C} \in sGrpd$ a Dwyer-Kan [[simplicial groupoid]], i.e an [[sSet]]-[[enriched groupoid]],

let's write
$$
  \mathbf{C}^{\mathcal{X}}
  \;\;
  \coloneqq
  sFunc(\mathcal{X}, \mathbf{}C)
$$
for the [[sSet]]-[[enriched functor category]] from $\mathcal{X}$ (regarded as a [[small category|small]] [[sSet-enriched category]]) to $\mathbf{C}$.

We denote the generic object here

$$
  \mathscr{V}_{\mathcal{X}}
  \;\in\;
  \mathbf{C}^{\mathcal{X}}
  \,.
$$

If $\mathbf{C}$ is [[cocomplete category|cocomplete]], then by [[left Kan extension]] $(-)_!$ these categories arrange into a [[pseudofunctor]]
$$
  \array{
    \mathllap{
      \mathbf{C}^{(-)}
      \;\colon\;
    }
    sGrpd &\longrightarrow& Cat
    \\
    \mathcal{X} 
      &\mapsto& 
    \mathbf{C}^{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{{}^f}
    && 
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    \mathcal{Y}
    &\mapsto&
    \mathbf{C}^{\mathcal{X}}
  }
$$

whose [[Grothendieck construction]] we abbreviate by
\[
  \label{CategoryOfParameterizedObjects}
  \mathbf{C}_{sGrpd}
  \;\;
    \coloneqq
  \;\;
  \underset{\mathcal{X} \in sGrpd}{\int}
  \mathbf{C}^{\mathcal{X}}
  \,.
\]

We may think of this as the category of *$sGrpd$-parameterized objects of $\mathbf{C}$*.

We denote the morphisms in $\mathbf{C}_{sGrpd}$ by their $f_! \dashv f^\ast$ [[adjuncts]]:
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


\end{definition}

\begin{example}\label{InitialParameterizedObject}
**(initial parameterized object)**
\linebreak
With the [[initial objects]] 

* of $sGrpd$ denoted $\varnothing \,\in\, sGrpd$

* of $\mathbf{C}$ denoted $0 \,in\, \mathbf{C}$;

* of $\mathbf{C}^{\mathcal{X}}$ denoted $0_{\mathcal{X}} \,in\, \mathbf{C}^{\mathcal{X}}$;

the [[initial object]] of $\mathbf{C}_{sGrpd}$ is 

* $0_{\varnothing} \,\in\, \mathbf{C}_{sGrpd}$.

\end{example}



\begin{proposition}
  \label{ModelStructureOnParameterizedObjects}
**(integral model structure on parameterized objects)**
\linebreak
  Let $\mathbf{C}$ be a [[combinatorial model category|combinatorial]] [[simplicial model category]] in which all [[objects]] are [[cofibrant objects|cofibrant]].

Then the [[pseudofunctor]] on the [[model category of simplicial groupoids]] which sends a [[simplicial groupoid]] $\mathcal{X}$ to the [[projective model structure on simplicial functors]] $\mathbf{C}^{\mathcal{X}}_{proj}$
$$
  \array{
    sGrpd &\longrightarrow& ModCat
    \\
    \mathcal{X} 
      &\mapsto& 
    \mathbf{C}^{\mathcal{X}}_{proj}
    \\
    \Big\downarrow\mathrlap{^f}
    && 
   \Big\downarrow\mathrlap{^f_!}
    \\
    \mathcal{Y}
    &\mapsto&
    \mathbf{C}^{\mathcal{X}}_{proj}
  }
$$
is relative and proper (in the sense [above](#Definition)), hence the integral model structure (Prop. \ref{ExistenceStatement}) on the category of *parameterized $\mathbf{C}$ objects* (eq:CategoryOfParameterizedObjects)
$$
  \mathbf{C}_{sGrpd}
  \;\;\coloneqq\;\;
  \underset{\mathcal{X} \in sGrpd}{\int}
  \mathbf{C}^{\mathcal{X}}_{proj}
$$
exists.
\end{proposition}
\begin{proof}
By general results in [[Higher Topos Theory]], the given pseudofunctor presents the $\infty$-functor 
$$
  \array{
    Grpd_\infty &\longrightarrow& Cat_\infty
    \\
    \mathcal{X} 
      &\mapsto& 
    Func_\infty(\mathcal{X},\,L^W \mathbf{C})
    \mathrlap{\,.}
  }
$$
By passage to [[homotopy category of an (infinity,1)-category|homotopy categories]] and using functoriality it follows that for $f$ an [[equivalence in an (infinity,1)-category|equivalence]], so is the [[derived functor]] of $f_!$, whence $f_!$ is a left [[Quillen equivalence]]. This shows that the pseudofunctor is relative.

Right properness is immediate: Since the weak equivalences in the projective [[model structure on functors]] are objectwise, the precomposition functor $f^\ast$ preserves weak equivalences for all $f$.

It remains to argue left-properness: If $f$ is an acyclic cofibration of simplicial groupoids, then it is so on all connected components, and here it is an injective weak equivalence and hence an acyclic cofibration (see [here](model+structure+on+simplicial+groupoids#sGrpdCofibrationIsObjectwiseSSetCofibration)) of simplicial sets on all endomorphisms objects. 

By groupoidiality we may without restriction assume that $f$ goes between simplicial groupoids whose set of objects is a singleton, hence that $f$ is of the form $f = \mathbf{B}\phi\colon \mathbf{B}H \to \mathbf{B}G$ for $\phi \colon H to G$ a homomorphism of [[simplicial groups]].

In this case the simplicial functors $\mathbf{B}H \to \mathbf{C}$ are equivalently $H$-[[action objects]] in $\mathbf{C}$.
On such an object $(X,\rho)$ the functor $f_!$ is given by the following [[pushout]] (this is proven as Lemma \ref{LeftInducedActionViaPushout} below):

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

Here the left morphism is an [[acyclic cofibration]] by the [[pushout-product axiom]] in the [[sSet]]-[[enriched model category]] $\mathbf{C}$, using the assumptions that $X$ is cofibrant in $\mathbf{C}$ and that $f$ and hence $\phi$ is an acyclic cofibration.
Therefore also the pushout morphism on the right is an acyclic cofibration, hence a weak equivalences.  
\end{proof}

Now to discuss the lemma used in the proof.

Let $\mathbf{C}$ be a [[simplicial model category]].
We write $\cdot \,\colon\, sSet \times \mathbf{C} \to \mathbf{C}$ for its [[sSet]]-[[tensoring]]. (The following clearly works more general enriched categories, too.)

For $H \in Grp(sSet)$ a [[simplicial group]] and $X \in Obj(C)$, we may consider [[group actions]] $\rho \colon H \cdot X \to X$. Write $H Act(\mathbf{C})$ for the [[category]] these form.

Then for $\phi \colon H \to G$ a morphism in $Grp(sSet)$ we have the "restriction" functor

\[
  \label{RestrictionOfSimplicialGroupActions}
  \phi^\ast 
    \,\colon\, 
  G Act(\mathbf{C}) \to H Act(\mathbf{C})
  \,.
\]

At least for $\mathbf{C} = $ [[sSet]] itself, it is a classical elementary fact that such functors (eq:RestrictionOfSimplicialGroupActions) have [[left adjoints]] $\phi_!$ sending action on $X$ to the "left induced action $G \cdot_{_H} X$". We will need the following [[pushout]]-construction of such left-induced actions:

\begin{lemma}
\label{LeftInducedActionViaPushout}
  The functor (eq:RestrictionOfSimplicialGroupActions) has a [[left adjoint]] which sends $(X,\rho) \in H Act(\mathbf{C})$ to the unique $(G \cdot_{_H} X,\, \phi_!(\rho))$ that makes the following [[commuting diagram|diagram commute]] such that the bottom (and hence the top) square are [[pushouts]] in $\mathbf{C}$: 

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

\end{lemma}
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

* $(X, \rho) \,\in\, H Act(\mathbf{C})$

* $(Y, \rho_Y) \,\in\, G Act(\mathbf{C})$.

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

Conversely, given such $f \circ \iota$ which is $H$-equivariant, then defining $f \circ q$ by this formula gives the bottom commuting square and hence extends to a $G$-equivariant map $G \cdot_H X \to Y$ by the [[universal property]] of the [[pushout]]. 
\end{proof}


#### Monoidal model structure

Now assume that $\mathbf{C}$ is in addition a [[symmetric monoidal category|symmetric]] [[monoidal model category]] with

* [[tensor product]] denoted $(-) \otimes (-) \,\colon\, \mathbf{C} \times \mathbf{C} \to \mathbf{C}$

* [[internal hom]] denoted $[-,-] \,\colon\, \mathbf{C}^{op} \times \mathbf{C} \to \mathbf{C}$

\begin{definition}\label{ExternalTensorProduct}
**(external tensor product)**
\linebreak
  The *[[external tensor product]]* on $\mathbf{C}_{sGrpd}$ (eq:CategoryOfParameterizedObjects) 

$$
  \boxtimes
  \;\colon\;
  \mathbf{C}_{sGrpd}
  \times
  \mathbf{C}_{sGrpd}
  \longrightarrow
  \mathbf{C}_{sGrpd}
$$

is defined first on morphisms covering [[identity morphisms]] in $sGrpd$ by

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

and then in general by

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
\end{definition}

\begin{lemma}
  The functor forming the [[external tensor product]] (Def. \ref{ExternalTensorProduct}) with a fixed object $\mathscr{V}'_{\mathcal{X}'} \,\in\, \mathbf{C}_{sGrpd}$
$$
  (-) \boxtimes \mathscr{V}'_{\mathcal{X}'}
  \;\colon\;
  \mathbf{C}_{sGrpd}
  \longrightarrow
  \mathbf{C}_{sGrpd}
$$
is a [[left Quillen functor]] on the integral model structure of Prop \ref{ModelStructureOnParameterizedObjects}.
\end{lemma}
\begin{proof}
  For $\phi_f \;\colon\; \mathscr{V}_{\mathcal{X}} \to \mathscr{W}_{\mathcal{Y}}$ an (acyclic) integral cofibration, 
we need to show that the adjunct of the component map 

$$
  \big(
    (\mathrm{pr}_{\mathcal{X}})^\ast
    \phi
  \big)
  \otimes
  (f \times id)^\ast
  (pr_{\mathcal{X}'})^\ast
  id_{\mathscr{V}'}
$$

is an (acyclic) cofibration in $\mathbf{C}$. Here on the right we have inserted the operation $(f \times id)^\ast$ --- which we may since it equals the identity in its postcomposition with $(pr_{\mathcal{X}'})^\ast$. But with that term inserted, we may apply [[Frobenius reciprocity]] when computing the [[adjunct]] of this map as its image under $(f \times id)_!$ composed with the counit. 

This formula for the adjunct is the total left morphism in the following commuting diagram. Here

* the top left square is the [[naturality square]] of the [[projection formula]]

* the bottom left square is from [this Remarj](Wirthmüller+context#ProjectionComposedWithCounitInRemainingVariable)

* the top right square is a [[Beck-Chevalley condition|Beck-Chevalley]] [[naturality square]]

* the bottom right square expresses the equality of two ways of moving the zig-zag morphism through the [[pasting diagram]] further below to the top right, one direct and the other by first moving its to the bottom left, using that the pasting of the left two squares and that of the bottom three squares are isomorphisms.


<img src="/nlab/files/LemmaDiagram-230424b.jpg" width="800">

The upshot is that the adjunct morphism on the left of the big diagram above is isomorphic to the composite on the right. That composite on the right, however, is the adjunct of $\phi$ pulled back to a product space and tensored with an object of $\mathbf{C}$. Thus...

(...)
\end{proof}

\linebreak

## Related pages

* The [[formal duality|dual]] notion is a [[model structure on sections]]

* [[tangent (infinity,1)-topos]]

* [[Joyal locus]]

* [[parameterized homotopy theory]]

* [[parameterized stable homotopy theory]]


## References

The first [[model category]] version of the [[Grothendieck construction]] was given in

* {#Roig94} [[Agustí Roig]], _Model category structures in bifibred categories_, Journal of Pure and Applied Algebra **95** 2 (1994) 203–223 &lbrack;<a href="https://doi.org/10.1016/0022-4049(94)90074-4">doi:10.1016/0022-4049(94)90074-4</a>&rbrack;

This article ([Roig 94](#Roig94)) had a mistake, which was fixed in

* {#Stanculesu12} [[Alexandru E. Stanculescu]], *Bifibrations and weak factorisation systems*, Applied Categorical Structures **20** 1 (2012) 19–30 &lbrack;<a href="https://link.springer.com/article/10.1007/s10485-009-9214-3">doi:10.1007/s10485-009-9214-3</a>&rbrack;

The construction was then generalized in

* {#HarpazPrasma15} [[Yonatan Harpaz]], [[Matan Prasma]], _The Grothendieck construction for model categories_, Advances in Mathematics **281** (2015) 1306-1363 &lbrack;[arXiv:1404.1852](https://arxiv.org/abs/1404.1852), [10.1016/j.aim.2015.03.031](https://doi.org/10.1016/j.aim.2015.03.031)&rbrack;

Another approach is found in

* [[Pierre Cagne]], [[Paul-André Melliès]], _On bifibrations of model categories_, ([arXiv:1709.10484](https://arxiv.org/abs/1709.10484))


For the special case of pseudofunctors with values in [[groupoids]], a [[model category]] version of the Grothendieck construction was discussed in

* [[Sharon Hollander]], _A homotopy theory for stacks_ ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247)).


[[!redirects Grothendieck construction of model categories]]
[[!redirects model category-theoretic Grothendieck construction]]

[[!redirects integral model structure]]
[[!redirects integral model structures]]
[[!redirects lax colimit model structure]]
[[!redirects lax colimit model structures]]
[[!redirects model structure on a lax colimit]]
[[!redirects model structures on a lax colimit]]
[[!redirects model structures on lax colimits]]

[[!redirects model structure on Grothendieck fibration]]
[[!redirects model structures on Grothendieck fibrations]]

[[!redirects model structure on a Grothendieck construction]]
[[!redirects model structure on the Grothendieck construction]]
[[!redirects model structure on Grothendieck constructions]]


