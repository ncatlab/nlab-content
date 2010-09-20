
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

* [[groupoid of Lie-algebra valued forms]]

* **2-groupoid of Lie 2-algebra valued forms**

* [[3-groupoid of Lie 3-algebra valued forms]]

* [[∞-groupoid of ∞-Lie-algebra valued forms]]

***

#Contents#
* automatic table of contents goes here
{:toc}



## Idea

For $\mathfrak{g}$ a [[Lie 2-algebra]] the **2-groupoid of $\mathfrak{g}$-valued forms** is the [[2-groupoid]] whose objects are [[differential form]]s with values in $\mathfrak{g}$, whose morphisms are [[gauge transformation]]s between these, and whose 2-morphisms are _higher order gauge transformations_ of those.

This naturally refines to a non-[[concrete sheaf|concrete]] [[Lie 2-groupoid]] is the 2-[[truncated]] [[∞-Lie groupoid]] whose $U$-parameterized smooth families of objects are smooth [[differential form]]s with values in a [[Lie 2-algebra]], and whose morphisms are gauge transformations of these.

This is the [[higher category theory|higher category]] generalization of the [[groupoid of Lie-algebra valued forms]].

A [[cocycle]] with coefficients in this 2-groupoid is a [[connection on a 2-bundle]].

## Definition

Consider a Lie [[strict 2-group]] $G$ corresponding to a Lie [[crossed module]] $(G_2 \stackrel{\delta}{\to} G_1)$ with action $\alpha : G_1 \to Aut(G_2)$.  Write $\mathbf{B}G$ for the corresponding [[delooping]] 2-groupoid, the one coming from the [[crossed complex]]

$$
  [\mathbf{B}G]
  =
  (G_2 \stackrel{\delta}{\to} G_1 \stackrel{\to}{\to} *)
  \,.
$$

Write $[\mathfrak{g}_2 \stackrel{\delta_*}{\to} \mathfrak{g}_1]$ for the corresponding [[differential crossed module]] with action $\alpha_* : \mathfrak{g}_1 \to der(\mathfrak{g}_2)$ 

+-- {: .un_def }
###### Definition

The 2-groupoid of Lie 2-algebra valued forms is defined to be the 2-stack 

$$
  \bar \mathbf{B}G : CartSp{}^{op} \to 2Grpd
$$ 

which assigns to $U \in CartSp$ the following 2-groupoid:
 
* An [[object]] is a pair 

  $$
    A \in \Omega^1(U,\mathfrak{g}_1)\,, \;\;\;
    B \in \Omega^2(U,\mathfrak{g}_2)
    \,.
  $$ 
  
* A 1-[[morphism]] $(g,a) : (A,B) \to (A',B')$ is a pair

  $$  
    g \in C^\infty(U,G_1)\,,\;\;\; a \in \Omega^1(U,\mathfrak{g}_2)
  $$

  such that

  $$
    A' = g^{-1} A g + g^{-1} d g + g^{-1} \delta_* a g
  $$

  and

  $$
    B' = \alpha_{g^{-1}}(
      B + d a + [a \wedge a] + \alpha_*(A \wedge a)
    )
    \,.
  $$

  The composite of two 1-morphisms

  $$
    (A,B) \stackrel{(g_1,a_1)}{\to} (A',B') \stackrel{(g_2,a_2)}{\to}
    (A'', B'')
  $$

  is given by the pair

  $$
    (g_1 g_2, a_1 + (\alpha_{g_2})_* a_2)
    \,.
  $$

* a [[2-morphism]] $f : (\lambda,a) \to (\lambda', a')$ is a function

  $$
    f \in C^\infty(U,G_2)
  $$

  such that 

  $$
    g' = \delta(f)^{-1} \cdot g 
  $$
 
  and

  $$
    a' = f^{-1} d f + f^{-1} a f + f^{-1}(r_f^{-1} \circ \alpha_f)_*(a)f
  $$

and composition is defined as follows

(...)

=--

## Properties

+-- {: .un_def }
###### Proposition
**(flat Lie 2-algebra valued forms)**


The full sub-2-groupoid on _flat_ Lie 2-algebra valued forms, i.e. those pairs $(A,B)$ for which the 2-form [[curvature]]

$$
  \delta_* B - d A + [A \wedge A] = 0
$$

and the 3-form [[curvature]]

$$
  d B + [A \wedge B] = 0
$$

vanishes is a resolution of the underlying discrete Lie 2-groupoid $\mathbf{\flat} \mathbf{B}G$ of the Lie 2-groupoid $\mathbf{B}G$.

=--

This is discussed at [[∞-Lie groupoid]] in the section <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#DiffCoeffsForLie2Group">strict Lie 2-groups -- differential coefficients</a>.

+-- {: .un_def }
###### Proposition

Let $\mathbf{\Pi}_2 : CartSp \to 2LieGrpd$ be the smooth 2-[[fundamental groupoid]] functor and let $P_2 : CartSp \to 2LieGrpd$ be the [[path n-groupoid|path 2-groupoid]] functor, taking values in the 2-catgeory $2Grpd(Difeol)$ of 2-groupoids [[internal category|internalization]] to [[diffeological space]]s. Then

* the 2-groupoid of Lie 2-algebra valued forms for which both 2- and 3-form curvature vanish is canonically equivalent to

  $$
    Hom_{2Grpd(Diffeol)}(\Pi_2(-), \mathbf{B}G) : CartSp^{op} \to 2Grpd
    \,;
  $$

* the 2-groupoid of Lie 2-algebra valued forms for which the 2-form curvature vanishes is canonically equivalent to

  $$
    Hom_{2Grpd(Diffeol)}(P_2(-), \mathbf{B}G) : CartSp^{op} \to 2Grpd
    \,;
  $$

=--

The equivalence is given by 2-dimensional [[parallel transport]].
A proof is in [SchrWalII](http://arxiv.org/abs/0802.0663).

The following proposition asserts that the Lie 2-groupoid of Lie 2-algebra valued forms is the coefficient object for for _differential nonabelian cohomology_ in degree 2, namely for _connections_ on [[principal 2-bundle]]s and in particular on [[gerbe]]s. 

+-- {: .un_def }
###### Proposition
**(2-bundles with connection)**

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]] and $\{U_i \to X\}$ a [[good open cover]] the 2-groupoid, let $X \stackrel{\simeq}{\leftarrow} C(\{U_i\})$ be the corresponding [[Cech nerve]] smooth 2-groupoid. Then 

$$ 
  Hom_{2Grpd(Diffeol)}( C(\{U_i\}), \bar \mathbf{B}G)
$$

is equivalent to the 2-groupoid of $G$-[[principal 2-bundle]]s with connection.

=--

This is discussed and proven in 
[SchrWalII](http://arxiv.org/abs/0802.0663) for the case where the 2-form curvature is restricted to vanish. In this case the above can be written as

$$ 
  Hom( C(\{U_i\}), Hom(P_2(-), \mathbf{B}G))
  \simeq
  Hom(P_2(C(\{\U_i\})), \mathbf{B}G)
  \,,
$$

where $P_2(C(\{\U_i\}) \in 2LieGrpd$ is a resolution of the [[path 2-groupoid]] of $X$.


## References

The 2-groupoid of Lie 2-algebra valued forms described in [definition 2.11](http://arxiv.org/PS_cache/arxiv/pdf/0802/0802.0663v3.pdf#page=27) of 

* Schreiber, Waldorf, _Smooth functors versus differential forms_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWII">web</a>). 

There are many possible conventions. The one reproduced above is supposed to describe the _bidual_ [[opposite 2-category]] of the 2-groupoid as defined in that article, with the direction of 1- and 2-morphisms reversed. 

See also

<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#ConnectionOn2Bundle">differential cohomology in an (∞,1)-topos -- survey - connections on 2-bundles</a>.

[[!redirects Lie 2-algebra valued forms]]
[[!redirects Lie 2-algebra valued differential forms]]
[[!redirects Lie 2-algebra valued form]]