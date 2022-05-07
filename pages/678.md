
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic toc goes here
{:toc}

## Definition ##

_Simplicial presheaves_ over some [[site]] $S$ are
 
* [[presheaf|Presheaves]] with values in the category [[SimpSet]] of simplicial sets, i.e., functors $S^{op} \to \Simp\Set$, i.e., functors $S^{op} \to [\Delta^{op}, \Set]$;

or equivalently, using the Hom-[[adjoint functor|adjunction]] and symmetry of the [[closed monoidal category|closed monoidal structure]] on [[Cat]]

* simplicial objects in the category of presheaves, i.e. functors $\Delta^{op} \to [S^{op},\Set]$.

## Interpretation as $\infty$-stacks ##

Regarding $\Simp\Set$ as a [[model category]] using the standard [[model structure on simplicial sets]] and inducing from that a model structure on $[S^{op}, \Simp\Set]$ makes simplicial presheaves a model for $\infty$-[[infinity-stack|stacks]], as described at [[infinity-stack homotopically]].

In more illustrative language this means that a simplicial presheaf on $S$ can be regarded as an $\infty$-[[infinity-groupoid|groupoid]] (in particular a [[Kan complex]]) whose space of $n$-morphisms is modeled on the objects of $S$ in the sense described at [[space and quantity]].

## Examples ##

* Notice that most definitions of $\infty$-[[infinity-category|category]] the $\infty$-category is itself defined to be a [[simplicial set]] with extra structure (in a [[geometric definition of higher category]]) or gives rise to a simplicial set under taking its [[nerve]] (in an [[algebraic definition of higher category]]). So most notions of presheaves of higher categories will naturally induce presheaves of simplicial sets.

* In particular, regarding a [[group]] $G$ as  a one object category $\mathbf{B}G$ and then taking the nerve $N(\mathbf{B}G) \in \Simp\Set$ of these (the "classifying simplicial set of the group whose [[geometric realization]] is the [[classifying space]] $\mathcal{B}G$), which is clearly a functorial operation, turns any presheaf with values in groups into a simplicial presheaf.

## Remarks ##

* There are various useful [[model category]] structures on the category of simplicial presheaves. See [[model structure on simplicial presheaves]].

## Properties ##

Here are some basic but useful facts about simplicial presheaves.

+--{: .un_prop}
######Proposition

Every simplicial presheaf $X$ is a 
[[homotopy limit|homotopy colimit]] over a [[diagram]]
of [[Set]]-valued sheaves regarded as discrete simplicial sheaves.

More precisely, for $X : S^{op} \to SSet$ a simplicial presheaf, 
let $D_X : \Delta^{op} \to [S^{op},Set] \hookrightarrow [S^{op},SSet]$ be
given by $D_X : [n] \mapsto X_n$. Then there is a weak equivalence
$$
  hocolim_{[n] \in \Delta} D_X([n]) \stackrel{\simeq}{\to} X
  \,.
$$
=--

+--{: .proof}
######Proof
See for instance [remark 2.1, p. 6](http://www.math.uiuc.edu/K-theory/0563/spre.pdf#page=6)

* [[Daniel Dugger]], [[Sharon Hollander]], [[Daniel Isaksen]], _Hypercovers and simplicial presheaves_, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 136 Issue 1, 2004 ([arXiv:math/0205027](https://arxiv.org/abs/math/0205027), [K-theory:0563](http://www.math.uiuc.edu/K-theory/0563), [doi:10.1017/S0305004103007175](https://doi.org/10.1017/S0305004103007175)) 

(which is otherwise about [[descent for simplicial presheaves]]).
=--

+--{: .un_cor}
######Corollary

Let $[-,-] : (SSet^{S^{op}})^{op} \times SSet^{S^{op}} \to SSet$ be the canonical $SSet$-enrichment of the category of simplicial presheaves (i.e. the assignment of [[SSet]]-[[enriched functor category|enriched functor categories]]).

It follows in particular from the above that every such [[hom-object]] $[X,A]$ of simplical presheaves can be written as a [[homotopy limit]] (in [[SSet]] for instance realized as a [[weighted limit]], as described there) over evaluations of $A$.
=--

+--{: .proof}
######Proof

First the above yields
$$
  \begin{aligned}
     [X, A ]  & \simeq [ hocolim_{[n] \in \Delta} X_n , A ]
  \\
      & holim_{[n] \in \Delta} [X_n, A]
  \end{aligned}
  \,.
$$

Next from the [[co-Yoneda lemma]] we know that the [[Set]]-valued presheaves $X_n$ are in turn colimits over representables in $S$, so that
$$
  \begin{aligned}
     \cdots & \simeq 
     holim_{[n] \in \Delta} 
     [ colim_i U_{i}, A]
     \\
     & \simeq
     holim_{[n] \in \Delta} lim_i
     [  U_{i}, A]       
  \end{aligned}
  \,.
$$

And finally the [[Yoneda lemma]] reduces this to
$$
  \begin{aligned}
     \cdots
      & 
     holim_{[n] \in \Delta} lim_i
     A(U_i)            
  \end{aligned}
  \,.
$$
=--

Notice that these kinds of computations are in particular often used when checking/computing [[descent|descent and codescent]] along a [[cover]] or [[hypercover]]. For more on that in the context of simplicial presheaves see [[descent for simplicial presheaves]].


## Related entries ##

* [[model structure on simplicial presheaves]]

* [[descent for simplicial presheaves]]

* [[presheaf of spectra]]

Applications appear for instance at

* [[geometric infinity-function theory]]

## References ##

The original articles are

* [[Kenneth S. Brown]], _Abstract homotopy theory and generalized sheaf cohomology_.  Transactions of the American Mathematical Society 186 (1973), 419-419.  [doi](http://dx.doi.org/10.1090/s0002-9947-1973-0341469-9).

* [[Kenneth S. Brown]], [[Stephen M. Gersten]], _Algebraic K-theory as generalized sheaf cohomology_.  In: Higher K-Theories.  Lecture Notes in Mathematics (1973), 266–292.  [doi](http://dx.doi.org/10.1007/bfb0067062).

* [[J. F. Jardine]], _Simplicial objects in a Grothendieck topos_.  In: Applications of algebraic K-theory to algebraic geometry and number theory.  Contemporary Mathematics (1986), 193-239.  [doi](http://dx.doi.org/10.1090/conm/055.1/862637)

* [[J. F. Jardine]], _Simplical presheaves_.  Journal of Pure and Applied Algebra 47:1 (1987), 35-87.  [doi][1]
  [1]: http://dx.doi.org/10.1016/0022-4049(87)90100-9

A modern expository account is

* [[John F. Jardine]], _Local Homotopy Theory_, Springer, 2015.  [doi](http://dx.doi.org/10.1007/978-1-4939-2300-7).


Further articles:

* [[J. F. Jardine]], _Stacks and the homotopy theory of simplicial sheaves_.  Homology, Homotopy and Applications 3:2 (2001), 361-384.  [doi](http://dx.doi.org/10.4310/hha.2001.v3.n2.a5).

* [[J. F. Jardine]], _Fields Lectures: Simplicial presheaves_.
[PDF](https://www.uwo.ca/math/faculty/jardine/courses/fields/fields-01.pdf).

For their interpretation in the more general context of [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-sheaves]] see Section 6.5.2 of

*  [[Jacob Lurie]], [[Higher Topos Theory]].

[[!redirects simplicial presheaves]]

[[!redirects category of simplicial presheaves]]
[[!redirects categories of simplicial presheaves]]