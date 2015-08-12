
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


#Contents#
* automatic table of contents goes here
{:toc}



## Idea

For $\mathfrak{g}$ a [[Lie 2-algebra]] the **2-groupoid of $\mathfrak{g}$-valued forms** is the [[2-groupoid]] whose objects are [[differential form]]s with values in $\mathfrak{g}$, whose morphisms are [[gauge transformation]]s between these, and whose 2-morphisms are _higher order gauge transformations_ of those.

This naturally refines to a non-[[concrete sheaf|concrete]] [[Lie 2-groupoid]] is the 2-[[truncated]] [[∞-Lie groupoid]] whose $U$-parameterized smooth families of objects are smooth [[differential form]]s with values in a [[Lie 2-algebra]], and whose morphisms are gauge transformations of these.

This is the [[higher category theory|higher category]] generalization of the [[groupoid of Lie-algebra valued forms]].

A [[cocycle]] with coefficients in this 2-groupoid is a [[connection on a 2-bundle]].

## Definition

### For strict Lie 2-algebras

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
    A' = Ad_{g^{-1}}\left( A + \delta_* a \right) + g^{-1} d g
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

* a [[2-morphism]] $f : (g,a) \Rightarrow (g', a'):(A,B)\to (A',B')$ is a function

  $$
    f \in C^\infty(U,G_2)
  $$

  such that 

  $$
    g' = \delta(f)^{-1} \cdot g 
  $$
 
  and

  $$
    a' = Ad_{f^{-1}} \left(a  + (r_f^{-1} \circ \alpha_f)_*(A)\right) + f^{-1} d f
  $$


and composition is defined as follows: vertical composition is given by pointwise multiplication ([[David Roberts|DR]]: the order still needs sorting out!) and horizontal composition is given as horizontal composition in the one-object 2-groupoid $\mathbf{B}G)$.


=--

### For general Lie 2-algebras
 {#ForGeneralLie2Algebras}

We consider now $\mathfrak{g}$ a general [[Lie 2-algebra]].

Let $\mathfrak{g}_0$ and $\mathfrak{g}_1$ be the two vector spaces involved and let

$$
  \{t^a\} \,, \;\;\; \{b^i\}
$$

be a dual basis, respectively. The structure of a Lie 2-algebra is conveniently determined by writing out the most general [[Chevalley-Eilenberg algebra]] 

$$
  CE(\mathfrak{g}) \in cdgAlg_\mathbb{R}
$$

with these generators.

We thus have

$$
  d_{CE(\mathfrak{g})} t^a = - \frac{1}{2}C^a{}_{b c} t^b \wedge t^c - r^a{}_i b^i
$$

$$
  d_{CE(\mathfrak{g})} b^i = -\alpha^i_{a j} t^a \wedge b^j  
    - 
    r_{a b c} t^a \wedge t^b \wedge t^c
  \,,
$$

for collections of structure constants $\{C^a{}_{b c}\}$ (the bracket on $\mathfrak{g}_0$) and $\{r^i_a\}$ (the differential $\mathfrak{g}_1 \to \mathfrak{g}_0$) and $\{\alpha^i{}_{a j}\}$ (the [[action]] of $\mathfrak{g}_0$ on $\mathfrak{g}_1$) and $\{r_{a b c}\}$ (the "Jacobiator" for the bracket on $\mathfrak{g}_0$).

These constants are subject to constraints (the weak [[Jacobi identity]] and its higher [[coherence law]]s) which are precisely equivalent to the condition

$$
  (d_{CE(\mathfrak{g})})^2 = 0
  \,.
$$

Over a test space $U$ a $\mathfrak{g}$-valued form datum is a morphism

$$
  \Omega^\bullet(U) \leftarrow W(\mathfrak{g}) 
   : 
  (A,B)
$$

from the [[Weil algebra]] $W(\mathfrak{g})$.

This is given by a 1-form

$$
  A \in \Omega^1(U, \mathfrak{g}_0)
$$

and a 2-form

$$
  B \in \Omega^2(U, \mathfrak{g}_1)
  \,.
$$

The [[curvature]] of this is $(\beta, H)$, where the 2-form component ("fake curvature") is

$$
  \beta^a = d_{dR} A^a + \frac{1}{2}C^a{}_{b c} A^b \wedge A^c
  + r^a{}_i B^i
$$

and whose 3-form component is 

$$
  H^i
     =
    d_{dR} B^i 
    +
   \alpha^i{}_{a j} A^a \wedge B^j
   +
   t_{a b c} A^a \wedge A^b \wedge A^c
  \,.
$$


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

is equivalent to the [[2-groupoid]] of $G$-[[principal 2-bundle]]s with [[connection on a 2-bundle|2-connection]].

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


## Related concepts

* [[groupoid of Lie-algebra valued forms]]

* **2-groupoid of Lie 2-algebra valued forms**

  * [[nonabelian Stokes theorem]]

* [[3-groupoid of Lie 3-algebra valued forms]]

* [[∞-groupoid of ∞-Lie-algebra valued forms]]



## References

The 2-groupoid of Lie 2-algebra valued forms described in [definition 2.11](http://arxiv.org/PS_cache/arxiv/pdf/0802/0802.0663v3.pdf#page=27) of 

* Schreiber, Waldorf, _Smooth functors versus differential forms_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SWII">web</a>). {#SchWalII}

There are many possible conventions. The one reproduced above is supposed to describe the _bidual_ [[opposite 2-category]] of the 2-groupoid as defined in that article, with the direction of 1- and 2-morphisms reversed. 

See also

<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+survey#ConnectionOn2Bundle">differential cohomology in an (∞,1)-topos -- survey - connections on 2-bundles</a>.

[[!redirects Lie 2-algebra valued 2-form]]

[[!redirects Lie 2-algebra valued forms]]
[[!redirects Lie 2-algebra valued differential forms]]
[[!redirects Lie 2-algebra valued form]]