
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents 
{:toc}

## Idea

Traditionally, a _homotopy type_ is a [[topological space]] regarded up to [[weak homotopy equivalence]]. Formally this may be taken to mean the [[object]] that $X$ represents in the standard [[homotopy category]] [[Ho(Top)]], or, better, in the [[(∞,1)-category]] [[Top]] of which the former is the [[decategorification]].

More generally, then, we may think of every object in any [[(∞,1)-category]] or at least every [[(∞,1)-topos]] $\mathcal{C}$ as being a _homotopy type_ in the context $\mathcal{C}$. For instance if $\mathcal{C}$ is an [[(∞,1)-category of (∞,1)-sheaves]]/of [[∞-stacks]] over some [[(∞,1)-site]] $C$, then an object of $\mathcal{C}$ may be thought of as a _homotopy type over $C$_.

This general perspective is notably enforced by _[[homotopy type theory]]_, which is a formal language for reasoning about such general homotopy types (at least when $\mathcal{C}$ is a [[locally cartesian closed (∞,1)-category]]).

## Examples

### In topological spaces

In traditional [[homotopy theory]] of [[topological spaces]] one sometimes distinguishes the notion of _strong homotopy types_ from that of _weak homotopy types_, depending on wher one regards topological spaces up to _[[homotopy equivalence]]_ or up to _[[weak homotopy equivalence]]_.

The two notions agree on good [[cofibrant object|cofibrant spaces]], namely on the [[CW-complexes]] (see [[model structure on topological spaces]]) and for homotopy theory proper it is the _weak_ homotopy equivalences that matter.

More precisely, weak homotopy equivalences between spaces give an equivalence relation on the class of topological spaces, and referring to a _homotopy type_ means that you are to consider properties of a space that are shared by any of the spaces weakly equivalent to it and thus in that [[equivalence class]].  In this expanded sense, therefore, a **homotopy type** is such a weak equivalence class of spaces. Using the terminology from [[homotopy category]], two spaces _have the same homotopy type_ if they are isomorphic in [[Ho(Top)]]. 

By standard theorems, homotopy types in topological can also be 'modeled' by many other structures, such as

* [[simplicial set|simplicial sets]] up to weak homotopy equivalence;
* small [[category|categories]] up to weak homotopy equivalence of their [[nerves]];
* $\infty$-[[infinity-groupoid|groupoids]] up to category-theoretic [[equivalence of categories|equivalence]] (this is the content of the [[homotopy hypothesis]]).

In most cases the tools of [[homotopy theory]], in particular [[model category|model categories]], can be used to establish these equivalences.

The sense of 'modeled' is related to Whithead's [[algebraic homotopy|algebraic homotopy theory]]. A setting such as those above acts as a model for homotopy types if there are comparison functors between $\Spaces$ and the category, and some notion of homotopy within the category yielding an equivalence of [[homotopy category|homotopy categories]]. 

+-- {: .num_remark}
###### Remark

Although the notion of homotopy type is defined for arbitrary spaces, it is most usual to restrict attention to 'locally [[nice topological space|nice]]' spaces such as polyhedra (i.e. realisations of [[simplicial complex|simplicial complexes]] or CW-complexes). Various other classes of space occur naturally in various parts of mathematics in particular in analysis and algebraic geometry and there the methods of abstract homotopy theory provide a way of mimicking the basic idea of homotopy type as described above. 

=--

+-- {: .num_remark}
###### Remark

Using variants of 'weak equivalence', for instance, '$n$-equivalence', one gets  coarser notions of equivalence which can be very useful. The particular case of $n$-equivalence leads to the related notion of [[homotopy n-type]].

=--

## Related concepts

[[!include notions of type]]


## Literature

There are some useful points made in:

* [[H. J. Baues]], _[[Homotopy Types]]_, in  _Handbook of Algebraic Topology_, (edited by I.M. James), North Holland, 1995.


[[!redirects homotopy types]]
[[!redirects weak homotopy type]]
[[!redirects strong homotopy type]]