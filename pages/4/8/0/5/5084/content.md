[[!redirects huge (∞,1)-sheaf (∞,1)-topos]]

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


Fix a [[universe]] $\mathcal{U}$ and a smaller universe $\mathcal{V} \in \mathcal{U}$. Let $\mathcal{V}$ be the reference-universa, so that $\mathcal{V}$-sets are called [[small set]]s. 


Write [[∞Grpd]] for the [[(∞,1)-category]] of small [[∞-groupoid]]s and $\infty \hat Grpd$ for the $\mathcal{U}$-small ones.

For $C$ an [[(∞,1)-category]] with [[(∞,1)-colimit]]s , write

$$
  (\infty,1)\hat Sh(C)
  \subset
  Func(C^{op}, \infty \hat Grpd)
$$

for the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] that preserves [[(∞,1)-limit]]s.

This is the **huge $(\infty,1)$-sheaf $(\infty,1)$-topos** on $C$.

Notice that for a suitable [[regular cardinal]] $\kappa$ this is the category of [[ind-object in an (∞,1)-category|ind-objects]] of $\mathbf{H}$.


## Properties

+-- {: .num_lemma #LeftCosetsDisjoint}
###### Lemma

For every $(\infty,1)$-topos $\mathbf{H}$ there is an [[(∞,1)-functor]]

$$
  (\infty,1)\hat Sh((\infty,1)Topos)
  \to 
  (\infty,1)\hat Sh(\mathbf{H})
$$

that preserves $\mathcal{U}$-small [[(∞,1)-colimit]]s and finite [[(∞,1)-limit]]s

give by sending $F : (\infty,1)Topos^{op} \to \infty \hat Grpd$ to the composite

$$
  \mathbf{H}^{op}
  \simeq
  ((\infty,1)Topos/\mathbf{H})_{et}^{op}
  \to 
  (\infty,1)Topos^{op}
  \stackrel{F}{\to}
  \infty \hat Grpd
$$

=--

This is [[Higher Topos Theory|HTT, lemma 6.3.5.21]].

## References


This is discussed in section 6.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The definition of $(\infty,1)\hat Sh(\mathbf{H})$ is in notation 6.3.5.16 and remark 6.3.5.17.  The relation to ind-objects appears as remark 6.3.6.18.

