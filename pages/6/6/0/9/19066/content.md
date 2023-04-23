
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

The [[Grothendieck construction]] may be lifted from [[categories]] to [[model categories]], where it serves as a presentation for the [[(infinity,1)-Grothendieck construction]].

## Definition
 {#Definition}

Let $M$ be a [[model category]] and $F \colon M \to ModelCat$ a [[pseudofunctor]], where $ModelCat$ is the [[2-category]] of model categories, [[Quillen adjunctions]] pointing in the direction of their [[left adjoints]], and [[mate]]-pairs of [[natural isomorphisms]].  Assume furthermore that:

* $F$ is *[[relative functor|relative]]*, meaning that whenever $f \colon A\to B$ is a [[weak equivalence]] in $M$, then the Quillen adjunction $f_! \colon F(A) \rightleftarrows F(B) : f^*$ is a [[Quillen equivalence]].  (That is, $F$ is a [[relative functor]].)

* $F$ is "*proper*", meaning that whenever $f \colon A\to B$ is an acyclic cofibration (resp. an acyclic fibration) in $M$, then $f_!$ (resp. $f^*$) preserves [[weak equivalences]].

In the [[Grothendieck construction]] $\int F$ we define a morphism $(f,\phi) \colon (A,X) \to (B,Y)$ (where $f \colon A\to B$ in $M$ and $\phi \colon f_!(X) \to Y$ in $F(B)$), to be:

* a *weak equivalence* iff $f \colon A\to B$ is a weak equivalence in $M$ and $f_!(Q X) \to f_!(X) \xrightarrow{\phi} Y$ is a weak equivalence in $F(B)$, where $Q$ is a [[cofibrant replacement]].  

  (Since $f_!\dashv f^*$ is a Quillen equivalencen by relativeness, this is equivalent to the dual condition that $X \xrightarrow{\hat{\phi}} f^*(Y) \to f^*(R Y)$ is a weak equivalence in $F(A)$.)

* a *cofibration* iff $f$ is a cofibration in $M$ and $\phi \colon f_!(X)\to Y$ is a cofibration in $F(B)$.

* a *fibration* if $f$ is a fibration in $M$ and the [[adjunct]] $\hat{\phi} \colon X\to f^*(Y)$ is a fibration in $F(A)$.

\begin{proposition}\label{ExistenceStatement}
There classes of maps make $\int F$ a model category, called the *integral model structure*.
\end{proposition}
This is [Harpaz & Prasma (2015), Theorem 3.0.12](#HarpazPrasma15).

## Properties

\begin{proposition}
Given a proper relative $F:M\to ModelCat$, we can compose with the underlying [[(infinity,1)-functor|$(\infty,1)$-functor]] $Ho \colon ModelCat \to QCat$ with values in (say) [[quasicategories]].  
Since $F$ is relative, this map takes weak equivalences in $M$ to equivalences of quasicategories, so it induces a functor of quasicategories $Ho(M) \to Ho(QCat) = (\infty,1)Cat$.  The [[(∞,1)-Grothendieck construction]] of this functor is then equivalent, over $Ho(M)$, to the underlying $(\infty,1)$-category of the Grothendieck-construction model structure on $\int F$
\end{proposition}
([Harpaz & Prasma (2015), Proposition 3.1.2](#HarpazPrasma15))

## Examples

### Parameterized objects 
 {#ParameterizedObjects}

> under construction --- handle with care


\begin{proposition}
  Let $\mathcal{C}$ be a [[combinatorial model category|combinatorial]] [[simplicial model category]] in which all [[objects]] are [[cofibrant objects|cofibrant]].
Then then [[pseudofunctor]] on the [[model category of simplicial groupoids]] which sends a [[simplicial groupoid]] $\mathcal{X}$ to the projective [[model structure on simplicial functors]] from $\mathcal{X}$ to $\mathcal{C}$
$$
  \array{
    sGrpd &\longrightarrow& ModCat
    \\
    \mathcal{X} 
      &\mapsto& 
    sFunc(\mathcal{X},\,\mathcal{C})_{proj}
    \\
    \Big\downarrow\mathrlap{^f}
    && 
   \Big\downarrow\mathrlap{^f_!}
    \\
    \mathcal{Y}
    &\mapsto&
    sFunc(\mathcal{Y},\,\mathcal{C})_{proj}
  }
$$
is relative and proper (in the sense [above](#Definition)), hence the integral model structure on the category of *parameterized $\mathcal{C}$ objects*
$$
  \mathcal{C}_{sGrpd}
  \;\;\coloneqq\;\;
  \underset{\mathcal{X} \in sGrpd}{\int}
  sFunc(\mathcal{X},\,\mathcal{C})_{proj}
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
    Func_\infty(\mathcal{X},\,L^W \mathcal{S})
    \mathrlap{\,.}
  }
$$
By passage to [[homotopy category of an (infinity,1)-category|homotopy categories]] and using functoriality it follows that for $f$ an [[equivalence in an (infinity,1)-category|equivalence]], so is the [[derived functor]] of $f_!$, whence $f_!$ is a left [[Quillen equivalence]]. This shows that the pseudofunctor is relative.

Right properness is immediate: Since the weak equivalences in the projective [[model structure on functors]] are objectwise, the precomposition functor $f^\ast$ preserves weak equivalences for all $f$.

It remains to argue left-properness: If $f$ is an acyclic cofibration of simplicial groupoids, then it is so on all connected components, and here it is an injective weak equivalence and hence an acyclic cofibration (see [here](model+structure+on+simplicial+groupoids#sGrpdCofibrationIsObjectwiseSSetCofibration)) of simplicial sets on all endomorphisms objects. 

By groupoidiality we may without restriction assume that $f$ goes between simplicial groupoids whose set of objects is a singleton, hence that $f$ is of the form $f = \mathbf{B}\phi\colon \mathbf{B}H \to \mathbf{B}G$ for $\phi \colon H to G$ a homomorphism of [[simplicial groups]].

In this case the simplicial functors $\mathbf{B}H \to \mathcal{C}$ are equivalently $H$-[[action objects]] in $\mathcal{C}$.
On such an object $(X,\rho)$ the functor $f_!$ is given by the following pushout (this is Lemma \ref{LeftInducedActionViaPushout} below):

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

Here the left morphism is an acyclic cofibration by the [[pushout-product axiom]] in the [[sSet]]-[[enriched model category]] $\mathcal{C}$, using the assumptions that $X$ is cofibrant in $\mathcal{C}$ and that $f$ and hence $\phi$ is an acyclic cofibration.
Therefore also the pushout morphism on the right is an acyclic cofibration, hence a weak equivalences.  
\end{proof}

Now to discuss the lemma used in the proof.

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

\begin{lemma}
\label{LeftInducedActionViaPushout}
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



## Related pages

* The [[formal duality|dual]] notion is a [[model structure on sections]]


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


