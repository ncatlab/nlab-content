[[!redirects huge (infinity,1)-sheaf (infinity,1)-topos]]

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

Fix a [[Grothendieck universe]] $\mathcal{U}$ and a smaller universe $\mathcal{V} \in \mathcal{U}$.  Let $\mathcal{V}$ be the reference-universe, so that sets in $\mathcal{V}$ are called *[[small set]]s*, sets in $\mathcal{U}$ are called *large*, and sets not necessarily in $\mathcal{U}$ are called *very large*.

Write [[∞Grpd]] for the (large) [[(∞,1)-category]] of small [[∞-groupoid]]s and $\infty GRPD$ for the very-large $(\infty,1)$-category of large $\infty$-groupoids.

Then the general procedures of [[universe enlargement]] can be applied to any large $(\infty,1)$-category to produce a very-large one.  Specifically, we have the *locally presentable enlargement*: for $C$ a large [[(∞,1)-category]] with small [[(∞,1)-colimit]]s, write

$$
  \Uparrow C
  \subset
  Func(C^{op}, \infty GRPD)
$$

for the full [[sub-(∞,1)-category]] of the [[(∞,1)-category of (∞,1)-functors]] that preserves small [[(∞,1)-limit]]s.  As described at [[universe enlargement]], if $C$ is locally presentable, then $\Uparrow C$ can be identified with the *naive enlargement*, which consists of the large models of the "theory" of which $C$ consists of the small models.

In particular, when $C$ is an [[(∞,1)-sheaf (∞,1)-topos]] $Sh(S)$ of small (∞,1)-sheaves, then $\Uparrow C$ can be identified with a (∞,1)-category of *large* (∞,1)-sheaves on the same site.  (That is, with a suitable accessible left-exact-reflective subcategory of $PSH(S)$ rather than $Psh(S)$---it is not yet known how to specify such a reflective subcategory purely in terms of data on $S$.)  Thus, we refer to $\Uparrow C$ as the **very large $(\infty,1)$-sheaf $(\infty,1)$-topos** on $C$.

Note that since every topos can be identified with the category of sheaves on itself for the [[canonical topology]], it is also reasonable to denote $\Uparrow \mathbf{H}$ by $SH(\mathbf{H})$.  $\Uparrow C$ can also also be identified with the category of [[ind-object in an (∞,1)-category|ind-objects]] of $\mathbf{H}$, for a suitable [[regular cardinal]] $\kappa$ (namely, the cardinal of $\mathcal{V}$).


## Properties

+-- {: .num_lemma #LeftCosetsDisjoint}
###### Lemma

For every $(\infty,1)$-topos $\mathbf{H}$ there is an [[(∞,1)-functor]]

$$
  \Uparrow ((\infty,1)Topos)
  \to 
  \Uparrow \mathbf{H}
$$

that preserves large [[(∞,1)-colimit]]s and finite [[(∞,1)-limit]]s.  It is defined by sending $F : (\infty,1)Topos^{op} \to \infty GRPD$ to the composite

$$
  \mathbf{H}^{op}
  \simeq
  ((\infty,1)Topos/\mathbf{H})_{et}^{op}
  \to 
  (\infty,1)Topos^{op}
  \xrightarrow{F}
  \infty GRPD
$$

=--

This is [[Higher Topos Theory|HTT, lemma 6.3.5.21]].

## References


This is discussed in section 6.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The definition of $\Uparrow\mathbf{H}$ is in Notation 6.3.5.16 and Remark 6.3.5.17.  The relation to ind-objects appears as remark 6.3.6.18.

[[!redirects huge (infinity,1)-sheaf (infinity,1)-topos]]
[[!redirects huge (∞,1)-sheaf (∞,1)-topos]]
[[!redirects very large (∞,1)-sheaf (∞,1)-topos]]
