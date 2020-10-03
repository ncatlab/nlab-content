
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[rational homotopy theory]] one considers [[topological spaces]] $X$ only up to maps that induce [[isomorphisms]] on _rationalized_ [[homotopy groups]] $\pi_\bullet(X) \otimes_{\mathbb{Z}} \mathbb{Q}$ (as opposed to genuine [[weak homotopy equivalences]], which are those maps that induce [[isomorphism]] on the genuine [[homotopy groups]].)

Every simply connected space is in this sense equivalent to a [[rational space]]: this is its **rationalization**.

Similarly one may consider "real-ification" by considering $\pi_\bullet(X) \otimes_{\mathbb{Z}} \mathbb{R}$, etc.

## Definition

### Rationalization of a single space

A **rationalization** of a [[simply connected space|simply connected]] [[topological space]] $X$ is a [[continuous function]] $\phi \colon X \to Y$, where

* $Y$ is a [[simply connected space|simply connected]] [[rational space]];

* $\phi$ induces an [[isomorphism]] on rationalized [[homotopy groups]]:

  $$
    \pi_\bullet(\phi)\otimes \mathbb{Q}   
    \;\colon\;
    \pi_\bullet(X) \otimes \mathbb{Q}
    \stackrel{\simeq}{\longrightarrow} 
    \pi_\bullet(Y) \otimes \mathbb{Q}
  $$

  or equivalently if $\phi$ induces an isomorphism on [[rational cohomology]] groups

  $$
    H^\bullet(\phi,\mathbb{Q}) 
    \;\colon\;
    H^\bullet(X,\mathbb{Q})
    \stackrel{\simeq}{\longrightarrow}
    H^\bullet(Y,\mathbb{Q})
    \,.
  $$

  or equivalently if $\phi$ induces an isomorphism on rational [[homology]] groups

  $$
    H_\bullet(\phi,\mathbb{Q}) 
    \;\colon\;
    H_\bullet(X,\mathbb{Q})
    \stackrel{\simeq}{\longrightarrow}
    H_\bullet(Y,\mathbb{Q})
    \,.
  $$

([Bousfield-Kan 72, p. 133-140](#BousfieldKan72), [Bousfield-Gugenheim 76, 11.1](#BousfieldGugenheim76), [Hess 06, Def. 1.4 with Def. 1.7](#Hess06))

### Rationalization as a localization of $Top$/$\infty Grpd$

In [[rational homotopy theory]] one considers
the [[Quillen adjunction]]

$$
  (\Omega^\bullet
   \dashv K)
  :
  dgAlg_{\mathbb{Q}} 
   \stackrel{\overset{\Omega^\bullet}{\leftarrow}}{\underset{K}{\to}}
  sSet
$$

between the [[model structure on dg-algebras]] and the standard [[model structure on simplicial sets]], where $\Omega^\bullet$ is forming [[Sullivan differential forms]]:

$$
  \Omega^\bullet(X) = Hom_{sSet}(X, \Omega^\bullet_{pl}(\Delta^\bullet_{Diff}))
  \,.
$$

Intrinsically this should model something like the (partially) left exact [[localization of an (∞,1)-category]] of [[∞Grpd]] at those morphisms that are [[rational homotopy equivalence]]s.

$$
  \infty Grpd_{ratio} \stackrel{\leftarrow}{\hookrightarrow} 
  \infty Grpd
  \,.
$$

Below we review classical results that says that the left [[adjoint (infinity,1)-functor]] here indeed preserves at least [[homotopy pullback]]s.

More generally, a setup by [[Bertrand Toen]] serves to provide a more comprehensive description of this situtation: see [[rational homotopy theory in an (infinity,1)-topos]].


## Properties 
  {#Properties}

### Rationalization via PL de Rham theory

+-- {: .num_defn #NilpotententFiniteRationalHomotopyTypes} 
###### Definition
**(nilpotent and finite rational homotopy types)**

Write

\[
  \label{NilpotentQFiniteHomotopyTypes}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)^{fin_{\mathbb{Q}}}_{\geq 1, nil}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)
\]

for the [[full subcategory]] of the [[classical homotopy category]]  ([[homotopy category]] of the [[classical model structure on simplicial sets]]) on those [[homotopy types]] $X$ which are

* [[connected topological space|connected]]: $\pi_0(X) = \ast$

* [[nilpotent space|nilpotent]]: $\pi_1(X)$ is a [[nilpotent group]]

* rational [[finite type]]: $dim_{\mathbb{Q}}\big( H^n(X;,\mathbb{Q}) \big) \lt \infty$ for all $n \in \mathbb{N}$.

and

\[
  \label{NilpotentFiniteRationalHomotopyTypes}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     SimplicialSets_{Qu}
  \big)
\]

for the futher [[full subcategory]] on those [[homotopy types]] that are already [[rational spaces|rational]].


Similarly, write

\[
  \label{NilpotentFiniteTypedgcAlgebras}
  Ho
  \big(
     DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)_{fin}^{\geq 1}
  \overset{
    \phantom{AAA}
  }{\hookrightarrow}
  Ho
  \big(
     DiffGradedCommAlgebras^{\geq 0}_{\mathbb{Q}}
  \big)
\]

for the [[full subcategory]] of the [[homotopy category]] of the [[projective model structure on connective dgc-algebras]] on those [[dgc-algebras]] $A$ which are

* connected: $H^0(A) \simeq \mathbb{Q}$

* [[finite type]]: $dim_{\mathbb{Q}}\big( H^n(A) \big) \lt \infty$ for all $n \in \mathbb{N}$.

=--

([Bousfield-Gugenheim 76, 9.2](#BousfieldGugenheim76))


+-- {: .num_pro #FundamentalTheoremOfdgAlgebraicRationalHomotopyTheory} 
###### Proposition
**([[fundamental theorem of dg-algebraic rational homotopy theory]])**

The [[derived adjunction]]

$$
  Ho
  \left(
    \big(
      DiffGradedCommAlgebras^{\geq 0}_{k}
    \big)^{op}_{proj}
  \right)
  \underoverset
    {
      \underset
        {\;\;\; \mathbb{R} exp \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\; \mathbb{L} \Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot}
  Ho
  \big(
    HoSimplicialSets_{Qu}
  \big)
$$

of the [[Quillen adjunction between simplicial sets and connective dgc-algebras]] (whose [[left adjoint]] is the [[PL de Rham complex]]-[[functor]]) has the following properties:

* on connected, nilpotent rationally finite homotopy types $X$ (eq:NilpotentQFiniteHomotopyTypes) the [[derived adjunction unit]] is [[rationalization]]

  $$
    \array{
    Ho
    \big(
       SimplicialSets_{Qu}
    \big)^{fin_{\mathbb{Q}}}_{\geq 1, nil}
    &
      \overset{
      }{\longrightarrow}
    &
    Ho
    \big(
       SimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
    \\
    X
    &\mapsto&
    \mathbb{R}\exp \circ \Omega^\bullet_{PLdR}(X)
    }    
  $$

  $$
    X
    \underoverset
      {\eta_X^{der}}
      {rationalization}
      {\longrightarrow}
    \mathbb{R}\exp \circ \Omega^\bullet_{PLdR}(X)
  $$

* on the [[full subcategories]] of nilpotent and finite rational homotopy types from Def. \ref{NilpotententFiniteRationalHomotopyTypes} it restricts to an [[equivalence of categories]]:

  $$
    Ho
    \left(
      \big(
        DiffGradedCommAlgebras^{\geq 0}_{k}
      \big)^{op}_{proj}
    \right)^{\geq 1}_{fin}
    \underoverset
      {
        \underset
          {\;\;\; \mathbb{R} exp \;\;\;}
          {\longrightarrow}
      }
      {
        \overset
          {\;\;\; \mathbb{L} \Omega^\bullet_{PLdR}\;\;\;}
          {\longleftarrow}
      }
      {\simeq}
    Ho
    \big(
      HoSimplicialSets_{Qu}
    \big)^{\mathbb{Q}, fin_{\mathbb{Q}}}_{\geq 1, nil}
  $$


=--

([Bousfield-Gugenheim 76, Theorems 9.4 & 11.2](#BousfieldGugenheim76))





### Preservation of homotopy pullbacks

+-- {: .num_theorem}
###### Theorem

The left [[derived functor]] of the [[Quillen functor|Quillen left adjoint]] $\Omega^\bullet : sSet \to dgAlg_{\mathbb{Q}}$ preserves [[homotopy pullbacks]] of objects of [[finite type]] (each rational homotopy group is a [[finite dimensional vector space]] over the [[ground field]]).

In other words in the induced pair of [[adjoint (∞,1)-functors]]

$$
  (\Omega^\bullet \dashv K)
   :
  (dgAlg_\mathbb{Q}^{op})^\circ
  \stackrel{\overset{}{\leftarrow}}{\underset{}{\to}}
  \infty Grpd
$$

the left adjoint preserves [[limit in a quasi-category|(∞,1)-categorical pullbacks]] of objects of finite type.

=--

+-- {: .proof}
###### Proof

This is effectively a restatement of a result that appears effectively below proposition 15.8 in HalperinThomas and is reproduced in some repackaged form as theorem 2.2 of [He06](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf). We recall the [[model category|model category-theoretic]] context that allows to rephrase this result in the above form.

Let $C = \{a \to c \leftarrow b\}$ be the pullback [[diagram]] category.

The [[homotopy limit]] functor is the right [[derived functor]] $\mathbb{R} lim_C$ for the [[Quillen adjunction]] (described in detail at [[homotopy Kan extension]])

$$
  [C,sSet]_{inj} \stackrel{\overset{const}{\leftarrow}}{\underset{lim_C}{\to}}
  sSet
  \,.
$$
 
At [[model structure on functors]] it is discussed that composition with the Quillen pair $\Omega^\bullet \dashv K$ induces a Quillen adjunction

$$
  ([C,\Omega^\bullet] \dashv [C,K])
  :
  [C, dgAlg^{op}]
  \stackrel{\overset{[C,\Omega^\bullet]}{\leftarrow}}{\underset{[C,K]}{\to}}
  [C,sSet]
  \,.
$$

We need to show that for every fibrant and cofibrant pullback diagram $F \in [C,sSet]$ there exists a weak equivalence 

$$
  \Omega^\bullet \circ lim_C F
  \;\;
  \simeq
  \;\;
  lim_C   \widehat{\Omega^\bullet(F)}
  \,,
$$

here $\widehat{\Omega^\bullet(F)}$ is a fibrant replacement of $\Omega^\bullet(F)$ in $dgAlg^{op}$.

Every object $f \in [C,sSet]_{inj}$ is cofibrant. It is fibrant if all three objects $F(a)$, $F(b)$ and $F(c)$ are fibrant and one of the two morphisms is a fibration. Let us assume without restriction of generality that it is the morphism $F(a) \to F(c)$ that is a fibration. So we assume that $F(a), F(b)$ and $F(c)$ are three [[Kan complex]]es and that $F(a) \to F(b)$ is a [[Kan fibration]]. Then $lim_C$ sends $F$ to the ordinary [[pullback]]  $lim_C F = F(a) \times_{F(c)} F(b)$ in $sSet$, and so the left hand side of the above equivalence is

$$
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$


Recall that the [[Sullivan algebra]]s are the cofibrant objects in $dgAlg$, hence the fibrant objects of $dgAlg^{op}$. Therefore a fibrant replacement of $\Omega^\bullet(F)$ may be obtained by

* first choosing a [[Sullivan model]] $(\wedge^\bullet V, d_V) \stackrel{\simeq}{\to} \Omega^\bullet(c)$ 

* then choosing factorizations in $dgAlg$ of the composites of this with $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(a)) $ and $\Omega^\bullet(F(c)) \to \Omega^\bullet(F(b))$ into cofibrations follows by weak equivalences.

The result is a diagram

$$
  \array{
    (\wedge^\bullet U^*, d_U)   
    &\leftarrow&
    (\wedge^\bullet V^*, d_V)
    &\hookrightarrow&
    (\wedge^\bullet W^* , d_W)
    \\
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    &&
    \downarrow^{\simeq}
    \\
    \Omega^\bullet(F(a))
    &\stackrel{}{\leftarrow}&
    \Omega^\bullet(F(c))
    &\stackrel{}{\to}&
    \Omega^\bullet(F(b))
  }
$$

that in $dgAlg^{op}$ exhibits a fibrant replacement of $\Omega^\bullet(F)$. The limit over that in $dgAlg^{op}$ is the colimit

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
$$

in $dgAlg$. So the statement to be proven is that there exists a weak equivalence

$$
  (\wedge^\bullet U^* , d_U)
  \otimes_{(\wedge^\bullet V^* , d_V)}
  (\wedge^\bullet W^* , d_W)
  \simeq  
  \Omega^\bullet(F(a) \times_{F(c)} F(b))
  \,.
$$

This is precisely the statement of that quoted result [He, theorem 2.2](http://www.math.uic.edu/~bshipley/hess_ratlhtpy.pdf).

=--

> check the following

+-- {: .num_cor}
###### Corollary

Rationalization preserves homotopy pullbacks of objects of finite type.

=--

+-- {: .proof}
###### Proof

The theory of [[Sullivan model]]s asserts that rationalization of a space $X$ (a simplicial set $X$) is the derived unit of the derived adjunction $(\Omega^\bullet \dashv K)$, namely that the rationalization is modeled by $K$ applied to a Sullivan model $(\wedge^\bullet V^*, d)$ for $\Omega^\bullet(X)$.

$$
  X \to K \Omega^\bullet(X) \stackrel{\simeq}{\leftarrow} K \widehat {\Omega^\bullet(X)} := K (\wedge^\bullet V^* , d_V)
  \,.
$$

Being a Quillen right adjoint, the right derived functor of $K$ of course preserves homotopy limits. Hence the composite $K \circ \widehat{\Omega^\bullet(-)}$ preserves homotopy pullbacks between objects of finite type.


=--


### Preservation of homotopy fibers

See at _[[rational fibration lemma]]_.


### Rationalization of spectra
 {#RationalizationOfSpectra}

On [[spectra]], rationalization is a [[smashing localization]], given by [[smash product]] with the [[Eilenberg-MacLane spectrum]] $H \mathbb{Q}$. (e.g. [Bauer 11, example 1.7 (4)](#Bauer11)).

For more see at _[[rational stable homotopy theory]]_.

## Related concepts

* [[p-localization]], [[p-completion]]

* [[fracture square]]

* [[rational homotopy theory]]

* [[equivariant rationalization]]

* [[rational equivariant homotopy theory]]

* [[rational equivariant stable homotopy theory]]

## References

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], p. 133-140 in: _Homotopy Limits, Completions and Localizations_, Lecture Notes in Mathematics Vol. 304, Springer 1972 ([doi:10.1007/978-3-540-38117-4](https://doi.org/10.1007/978-3-540-38117-4))

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], Def. 11.1 in: _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

* {#Hess06} [[Kathryn Hess]], Def. 1.7 in: _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)), chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007 ([doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))
* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_ (2011) ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

[[!redirects rationalizations]]

[[!redirects rationalisation]]
[[!redirects rationalisations]]
