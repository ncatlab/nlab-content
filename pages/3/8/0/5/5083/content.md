
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

## Definition

+-- {: .un_defn}
###### Definition

For $\mathbf{H}$ an [[(∞,1)-topos]] we say its **co-shape** $\Gamma \mathbf{H}$  is the object

$$
  \Gamma(\mathbf{H}) : A
  \mapsto
  (\infty,1)Topos((\infty,1)PSh(A), \mathbf{H})
  \in
  (\infty,1)\hat Sh(\infty Grpd)
$$

in the [[huge (∞,1)-sheaf (∞,1)-topos]] on [[∞Grpd]].

=--

+-- {: .un_remar}
###### Remark

For $\mathcal{U}$ the bigger [[universe]] and $\kappa$ a [[regular cardinal]] such that [[small set]]s are $\kappa$-smal, we have that 

$$
  (\infty,1)\hat Sh(\infty Grpd) \simeq \hat Ind_\kappa(\infty Grpd)
$$

is identified with the $\kappa$-[[ind-object in an (∞,1)-category|ind-objects]] of [[∞Grpd]].

=--


## Properties

+-- {: .un_prop}
###### Proposition

Coshape [[Yoneda extension|Yoneda-extends]] to a pair of [[adjoint (∞,1)-functor]]s between the [[huge (∞,1)-sheaf (∞,1)-topos]]es

$$
  (\infty,1)\hat Sh(\infty Grpd)
  \stackrel{\overset{\Gamma}{\leftarrow}}{\underset{Codisc}{\to}}
  \infty \hat Sh((\infty,1)Topos)
$$

on [[∞Grpd]] and [[(∞,1)Topos]], respectively.

=--

+-- {: .proof}
###### Proof

By [[Higher Topos Theory|HTT, lemma 6.3.5.21]] we have an [[(∞,1)-functor]] 

$$
  (\infty,1)\hat Sh((\infty,1)Topos)
  \to 
  (\infty,1)\hat Sh(\infty Grpd)
$$

that preserves $\mathcal{U}$-small colimits and finite limits and is given by sending

$$
  F : (\infty,1)Topos^{op} \to \infty Grpd
$$

to the composite

$$
   \infty Grpd
   \stackrel{PSh(-)}{\to}
   (\infty Topos/\infty Grpd)_{et}^{op}
   \stackrel{}{\to}
   (\infty,1)Topos^{op}
   \stackrel{F}{\to}
   \infty Grpd
  \,,
$$

where the first step is forming [[(∞,1)-presheaf (∞,1)-topos]]es which sit by their terminal [[global section]] [[(∞,1)-geometric morphism]] over [[∞Grpd]] and the second step is the evident projection.

Applied to a [[representable functor|representable]] 
$F = (\infty,1)Topos(-,\mathbf{H})$ this composite is hence 

$$
  A \mapsto \Gamma(\mathbf{H})(A)
  \,.
$$

=--
