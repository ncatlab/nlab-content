
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _enriched model category_ is an [[enriched category]] $C$ together with the structure of a [[model category]] on the [underlying category](http://ncatlab.org/nlab/show/enriched+category#BaseChange) $C_0$ such that both structures are compatible in a reasonable way.


## Definition

Let $V$ be a [[monoidal model category]].

A **$V$-enriched model category** is

* an V-[[enriched category]] $C$

  * which is [[powered and copowered category|powered and copowered]] over $V$;

* with the structure of a [[model category]] on the [underlying category](enriched+category#BaseChange) $C_0$

* such that 

  * {#PullbackPowerAxiom} **([[pullback-power axiom]])** for every [[cofibration]] $i \colon A \to B$ and [[fibration]] $p \colon X \to Y$ in $C_0$ the [[pullback powering]] morphism (dual to the [[pushout product]]) with respect to the powering in $V$ 

    $$
      C(B,X) \stackrel{(i^* , p_*)}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)
    $$ 

    is a fibration with respect to the model structure on $V$;

  * and is an [[acyclic fibration]] whenever $i$ or $p$ are acyclic.

The last two conditions here are equivalent to the fact that the [[copower]]

$$
  \otimes : C \times V \to C
$$

is a [[Quillen bifunctor]].

## Properties

### Change of enrichment

(...)


## Examples

\begin{example}\label{MonoidalModelCategoryIsEnrichedModelOverItself}
**([[monoidal model category]] is enriched model over itself)**
\linebreak
  Every [[monoidal model category]] is an [[enriched model category]] over itself, via the [[enriched category|enrichment]] of its underlying [[closed monoidal category]].
\end{example}
\begin{proof}
  One just needs to see that the [[pullback-power axiom]] is implied by (in fact it is equivalent to) the [[pushout-product axiom]]. This equivalence is an instance of [[Joyal-Tierney calculus]] (see [this Prop.](Introduction+to+Homotopy+Theory#JoyalTierneyCalculus)):

Writing 

* $\mathrm{F}$, $\mathrm{C}$, $\mathrm{W}$ for the classes of [[fibrations]], [[cofibrations]], [[weak equivalences]], respectively;

* $\mathrm{FW}$, $\mathrm{CW}$ for the classes of [[acyclic fibrations]] and [[acyclic cofibrations]], respectively

and

* $(-) \,\perp \, (-)$ for the [[lifting property]],

* $(-) \Box (-)$ for the [[pushout product]],

* $(-)^{\Box (-)}$ for the [[pullback power]],

we have the following logical equivalences.

$$
  \begin{aligned}
    \mathrm{C} \Box \mathrm{C}
    &
    \,\subset\,
    &
    \mathrm{C}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{C} \Box \mathrm{C}
    &\,\perp\,&
    \mathrm{FW}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{C}
    &
    \,\perp\,
    &
    \mathrm{FW}^{\Box \mathrm{C}}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{FW}^{\Box \mathrm{C}}
    &
    \,\subset\,
    & 
    \mathrm{FW}
    \\
    {\phantom{-}}
    \\
    \mathrm{C} \Box \mathrm{CW}
    &
    \,\subset\,
    &
    \mathrm{CW}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{C} \Box \mathrm{CW}
    &\,\perp\,&
    \mathrm{F}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{C}
    &
    \,\perp\,
    &
    \mathrm{F}^{\Box \mathrm{CW}}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{F}^{\Box \mathrm{CW}}
    &
    \,\subset\,
    & 
    \mathrm{FW}
    \\
    &
    &
    &
    &
    &&
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{CW}
    &
    \,\perp\,
    &
    \mathrm{F}^{\Box \mathrm{C}}
    &
    \;\;\;
    \Leftrightarrow
    \;\;\;
    &
    \mathrm{F}^{\Box \mathrm{C}}
    &
    \,\subset\,
    & 
    \mathrm{F}
  \end{aligned}
$$

Here the outer equivalences are by definition of the [[lifting properties]] in a [[model category]], while the middle equivalences are by [[Joyal-Tierney calculus]].
The statements on the far left constitute the [[pushout-product axiom]], while those on the far right constiture the [[pullback-power axiom]].
\end{proof}

\begin{example}\label{TheClassicalModelCategoriesOfTopSpacesAndSimpSets}
  Since the [[model structure on compactly-generated topological spaces]] as well as the [[classical model structure on simplicial sets]] are [[monoidal model categories]], they are,
by by Exp. \ref{MonoidalModelCategoryIsEnrichedModelOverItself},
also enriched modal categories over themselves.
\end{example}

\begin{example}
  A model category enriched over the [[classical model structure on simplicial sets]] is called a *[[simplicial model category]]*.
\end{example}


## Related concepts

* [[derived hom-functor]]

* [[enriched homotopical category]].

* [[pushout-product]], [[pushout-product  axiom]]
 
* [[pullback power]]

## References

Textbook account:

* [[Jacob Lurie]], Def. A.3.1.5 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

See also:

* [[Bertrand Guillou]], [[Peter May]], _Enriched model categories and presheaf categories_, New York J. Math. 26 (2020) 37–9 ([arXiv:1110.3567](http://arxiv.org/abs/1110.3567), [NYJM:2020/26-3](https://www.emis.de/journals/NYJM/j/2020/26-3.html))

[[!redirects enriched model categories]]

[[!redirects enriched model structure]]
[[!redirects enriched model structures]]

[[!redirects enriched model category theory]]


