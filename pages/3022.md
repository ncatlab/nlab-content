
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __$1$-topos__, or __$(1,1)$-topos__, is simply a [[topos]] in the usual sense of the word.  The prefix $1$- may be added when also discussing [[higher category theory|higher categorical]] types of topoi in [[higher topos theory]] such as [[2-topos]], $(\infty,1)$-[[(infinity,1)-topoi|topos]], or even $\infty$-[[infinity-topos|topos]].  Compare that a [[(0,1)-topos]] is a [[Heyting algebra]].

Similarly, a __Grothendieck $1$-topos__, or __Grothendieck $(1,1)$-topos__, is simply a [[Grothendieck topos]].  Compare that a [[Grothendieck (0,1)-topos]] is a [[frame]] (or [[locale]]).

Note that a 1-topos is not exactly a particular sort of [[2-topos]] or $\infty$-topos, just as a [[Heyting algebra]] is not a particular sort of 1-topos.  The (1,2)-category of locales (i.e. (0,1)-topoi) embeds fully in the 2-category of Grothendieck 1-topoi by taking sheaves, but a locale is not identical to its topos of sheaves (and in fact no nontrivial 1-topos can be a poset), in that the following [[diagram]] of [[functors]] can *not* be filled by a [[natural isomorphism]]:

\begin{tikzcd}
  \mathrm{Top}_{(0,1)}
  \ar[rr, "\mathrm{Sh}(-)"]
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \ar[drr, phantom, "{\#}"]
  &&
  \mathrm{Top}_{(1,1)}
  \ar[d, "{\mathrm{forget}}"{pos=.9,yshift=5pt,sloped}]
  \\
  \mathrm{Cat}_{(0,1)}
  \ar[rr, hook]
  &&
  \mathrm{Cat}_{(1,1)}  
\end{tikzcd}


Likewise, one expects every Grothendieck 1-topos to give rise to a 2-topos or $\infty$-topos of [[stacks]], hopefully producing a full embedding of some sort.

## Related concepts


[[!include flavors of higher toposes -- list]]



[[!redirects (1,1)-topos]]
[[!redirects Grothendeick 1-topos]]
[[!redirects Grothendeick (1,1)-topos]]

[[!redirects 1-toposes]]
[[!redirects 1-topoi]]