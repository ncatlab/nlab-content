
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In **string topology** one studies the [[BV-algebra]]-structure on the [[ordinary homology]] of the [[free loop space]] $X^{S^1}$ of an [[oriented]] [[manifold]] $X$, or more generally the [[framed little 2-disk operad|framed little 2-disk algebra]]-structure on the singular [[chain complex]]. This is a special case of the general algebraic structure on higher order [[Hochschild cohomology]], as discussed there. 

The study of _string topology_ was initated by [[Moira Chas]] and [[Dennis Sullivan]]. 

## The string operations

Let $X$ be a [[smooth manifold]], write $L X$ for its [[free loop space]] (for $X$ regarded as a [[topological space]]) and $H_\bullet(L X)$ for the [[ordinary homology]] of this space (with coefficients in the [[integer]]s $\mathbb{Z}$).


### The string product 

+-- {: .num_defn }
###### Definition

The **string product** is a morphism of [[abelian group]]s

$$
  (-)\cdot(-) : 
  H_\bullet(L X) \otimes H_\bullet(L X)
  \to 
  H_{\bullet - dim X}(L X)
  \,,
$$

where $dim X$ is the [[dimension]] of $X$, defined as follows:

Write $ev_* : L X \to X$ for the [[evaluation map]] at the basepoint of the loops. 

For $[\alpha] \in H_i(L X)$ and $[\beta] \in H_j(L X)$ we can find representatives $\alpha$ and $\beta$ such that $ev(\alpha)$ and $ev(\beta)$ intersect [[transversal map|transversally]]. There is then an $((i+j)-dim X)$-chain $\alpha \cdot \beta$ such that $ev(\alpha \cdot \beta)$ is the chain given by that intersection: above $x \in ev(\alpha \cdot \beta)$ this is the loop obtained by concatenating $\alpha_x$ and $\beta_x$ at their common basepoint. The _string product_ is then defined using such representatives by

$$
  [\alpha] \cdot [\beta] := [\alpha \cdot \beta]
  \,.
$$

=--

+-- {: .num_theorem }
###### Theorem

The string product is [[associativity|associative]] and graded-commutative. 

=--

This is due to ([ChasSullivan](#ChasSullivan)).
There is is a more elegant way to capture this, due to ([CohenJones](#CohenJones)):

Let 

$$
  S^1 \coprod S^1 \to 8 \leftarrow S^1
$$

be the [[cospan]] that exhibts the inner and the outer circle of the figure "8" topological space. By forming [[hom space]]s this induces the [[span]]

$$
  \array{
      && X^8
      \\
      & {}^{\mathllap{in}}\swarrow && \searrow^{\mathrlap{out}}
     \\
     L X \times L X &&&& L X
  }
  \,.
$$ 

Write $in^!$ for the "pullback" in [[ordinary homology]] along $in$ (the dual [[fiber integration]]) and $out_*$ for the ordinary pushforward. 

+-- {: .num_theorem }
###### Theorem

The string product is the pull-push operation

$$
  out_* \circ in^! : H_\bullet(L X \times L X)
  \simeq H_\bullet(L X) \otimes H_\bullet(L X)
  \to 
  H_{\bullet - dim X}(L X)
  \,.
$$

=--

This is due to ([CohenJones](#CohenJones)).

### The BV-operator

+-- {: .num_defn }
###### Definition

Define a morphism of [[abelian group]]s

$$
  \Delta : H_\bullet(L X) \to H_{\bullet + 1}(L X)
$$

as follows. Consider first the rotation map

$$
  \rho : S^1 \times L X \to L X
$$

that sends $(\theta, \gamma) \mapsto (t \mapsto \gamma(\theta + t))$.  Then take

$$
  \Delta : a \mapsto \rho_* ([S^1] \times a)
  \,,
$$

where $[S^1] \in H_1(S^1)$ is the [[fundamental class]] of the [[circle]]. 

=--

This is called the **BV-operator** for string topology.



+-- {: .num_prop }
###### Proposition

The [[Goldman bracket]] on $H_0(L X)$ is equivalent to the string product applied to the image of the BV-operator

$$
  \{[\gamma_1], [\gamma_2]\}
  = 
  \Delta[\Gamma_1] \cdot \Delta[\Gamma_2]
  \,.
$$

=--

This is due to ([ChasSullivan](#ChasSullivan)).


## String operations as operators in a topological quantum field theory
 {#InTermsOfTQFTs}

The structures studied in the _string topology_ of a [[smooth manifold]] $X$ may be understood as being essentially the data of a 2-dimensional [[topological field theory]] [[sigma model]] with [[target space]] $X$, or rather its linearization to an [[HQFT]] (with due care on some technical subtleties). 

The idea is that the [[configuration space]] of a closed or open [[string]]-[[sigma-model]] propagating on $X$ is the [[loop space]] or path space of $X$, respectively. The space of [[state]]s of the string is some space of sections over this configuration space, to which the (co)homology $H_\bullet(L X)$ is an approximation. The string topology operations are then the [[cobordism]]-representation with [[coefficients]] in the [[category of chain complexes]]

$$
  H_\bullet(Bord_2) \to Ch_\bullet
$$

given by the [[FQFT]] corresponding to the $\sigma$-modelon these state spaces, acting on these state spaces.

$\,,$


Let $X$ be an [[orientation|oriented]] [[compact space|compact]] [[manifold]] of dimension $d$.
 
For $\mathcal{B} = \{A, B , \cdots\}$
a collection of oriented compact submanifolds write
$P_X(A,B)$ for the [[path space]] of paths in $X$ that start in $A \subset X$ and end in $B \subset X$.

+-- {: .num_theorem }
###### Theorem

The  tuple $(H_\bullet(L M, \mathbb{Q}), \{H_\bullet(P_X(A,B), \mathbb{Q})\}_{A,B \in \mathcal{B}})$ carries the
structure of a $d$-dimensional [[HCFT]] with _positive boundary_ and set of [[branes]] $\mathcal{B}$, such that the correlators in the closed sector are the standard string topology operation.

=--

For [[closed strings]] this is discussed in ([Cohen-Godin 03](#CohenGodin03), [Tamanoi 07](#Tamanoi07)). 
For [[open strings]] on  a single [[brane]] $\mathcal{B} = \{*\}$ this was shown in ([Godin 07](#Godin)), where the general statement for arbitrary branes is conjectured. A detailed proof of this general statement is in ([Kupers 11](#Kupers)). 

+-- {: .num_remark }
###### Remark

These constructions work by regarding the [[mapping spaces]] from 2-dimensional [[cobordisms]] with maps to the base space as [[correspondences]] and then applying pull-push (pullback followed by [[push-forward in generalized cohomology|push-forward in cohomology]]/[[Umkehr maps]]) to these. Hence these quantum field theory realizations of string topology may be thought of as arising from a [[quantization]] process  of the form _[[path integral as a pull-push transform]]/[[motivic quantization]]_.

=--

## Related concepts

* [[Goldman bracket]]

* [[path integral as a pull-push transform]]

## References

The original references include the following:

* [[Moira Chas]], [[Dennis Sullivan]], _String topology_, Ann. Math. [math.GT/9911159](http://arxiv.org/abs/math/9911159)
 {#ChasSullivan}

* [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_, [math.GT/05036259](http://arxiv.org/abs/math/0503625), 95 pp. published as a part of R. Cohen, [[Kathryn Hess|K. Hess]], A. Voronov, _String topology and cyclic homology_, CRM Barcelona courseware, Springer, [description](http://www.springer.com/birkhauser/mathematics/book/978-3-7643-2182-6), [doi](http://dx.doi.org/10.1007/3-7643-7388-1), [pdf](http://gen.lib.rus.ec/get?md5=adde9464705ede0fea6b435edb58fbe7)

* [[Dennis Sullivan]], _Open and closed string field theory interpreted in classical algebraic topology_,  Topology, geometry, and quantum field theory, 344&#8211;357. London Math. Soc. Lec. Notes __308__, Cambridge Univ. Press. 2004.

*  [[Ralph Cohen]], John R. Klein, Dennis Sullivan, _The homotopy invariance of the string topology loop product and string bracket_, J. of Topology 2008 __1__(2):391-408; [doi](http://dx.doi.org/10.1112/jtopol/jtn001) 

* [[Ralph Cohen]], _Homotopy and geometric perspectives on string topology_, [pdf](http://math.stanford.edu/~ralph/skyesummary.pdf)

In 

* {#CohenJones} [[Ralph Cohen]] and J.D.S. Jones, _A homotopy theoretic realization of string topology_ , Math. Ann. 324
(2002), no. 4, ([arXiv:0107187](http://arxiv.org/abs/math/0107187))
 

the string product was realized as genuine pull-push (in terms of dual [[fiber integration]] via [[Thom isomorphism]]).

The interpretation of closed string topology as an [[HQFT]] is discussed in

* [[Ralph Cohen]], [[Veronique Godin]], 
  _[[A Polarized View of String Topology]]_ ([arXiv:math/0303003](http://arxiv.org/abs/math/0303003))
 {#CohenGodin03}

* Hirotaka Tamanoi, _Loop coproducts in string topology and triviality of higher genus TQFT operations_ (2007) ([arXiv](http://arxiv.org/abs/0706.1276))
 {#Tamanoi07}

A detailed discussion and generalization to the open-closed [[HQFT]] in the presence of a single space-filling [[brane]] is in

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}

The generalization to multiple [[D-brane]]s is discussed in

* [[Sander Kupers]], _String topology operations_ MS thesis (2011) ([pdf](http://math.stanford.edu/~kupers/thesis7thjune2011.pdf))
 {#Kupers}

For target space a [[classifying space]] of a [[finite group]] or [[compact space|compact]] [[Lie group]] this is discussed in

* David Chataur, [[Luc Menichi]], _String topology of classifying spaces_ ([pdf](http://math.univ-angers.fr/perso/lmenichi/String_Classifiant09.pdf))

Arguments that this string-topology [[HQFT]] should refine to a chain-level theory -- a [[TCFT]] -- were given in

* [[Kevin Costello]],  _Topological conformal field theories and Calabi-Yau $A_\infty$-categories_ (2004) , ([arXiv:0412149](http://arxiv.org/abs/0412149))
 {#Costello}

and 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_
 {#Lurie}
(see example 4.2.16, remark 4.2.17).

For the string product and the BV-operator this extension has been known early on, it yields a [[homotopy BV algebra]] considered around page 101 of

* [[Scott Wilson]], _On the Algebra and Geometry of a Manifold's
Chains and Cochains_ (2005) ([pdf](http://qcpages.qc.cuny.edu/~swilson/main.pdf))

Evidence for the existence of the [[TCFT]] version by exhibiting a [[dg-category]] that looks like it ought to be the dg-category of string-topology [[branes]] (hence ought to correspond to the TCFT under the suitable version of the [[TCFT]]-version of the [[cobordism hypothesis]]) is discussed in

* [[Andrew Blumberg]], [[Ralph Cohen]], [[Constantin Teleman]], _Open-closed field theories, string topology, and Hochschild homology_ ([arXiv:0906.5198](http://arxiv.org/abs/0906.5198))
 {#BlumbergCoheneTeleman09}

Refinements of string topology from [[homology groups]] to the full [[ordinary homology]]-[[spectra]] is discussed in ([Blumberg-Cohen-Teleman 09](#BlumbergCoheneTeleman09)) and in

* [[Ralph Cohen]], [[John Jones]], _A homotopy theoretic realization of string topology_, Mathematische Annalen ([arXiv:math/0107187](http://arxiv.org/abs/math/0107187))

* [[Ralph Cohen]], [[John Jones]], _Gauge theory and string topology_ ([arXiv:1304.0613](http://arxiv.org/abs/1304.0613))

A generalization of string topology with target manifolds generalized to [[orbifolds]] is discussed in

* Alejandro Adem, Johanna Leida, Yongbin Ruan, _Orbifolds and string topology_, Cambridge Tracts in Mathematics 171, 2007 ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

Further generalization to target spaces that are more generally [[differentiable stacks]]/[[Lie groupoids]] is discussed in

* [[Kai Behrend]], [[Gregory Ginot]], [[Behrang Noohi]], [[Ping Xu]], _String topology for stacks_, (89 pages) [arxiv/0712.3857](http://arxiv.org/abs/0712.3857); _String topology for loop stacks_, C. R. Math. Acad. Sci. Paris, __344__ (2007), no. 4, 247--252, (6 pages, [pdf]())

* Po Hu, _Higher string topology on general spaces_, Proc. London Math. Soc. __93__ (2006) 515-544, [doi](http://dx.doi.org/10.1112/S0024611506015838), [ps](http://www.math.wayne.edu/~po/koszul04.ps)

The relation between string topology and [[Hochschild cohomology]] in dimenion $\gt 1$ is discussed in

* [[Dmitry Vaintrob]], _The String topology BV algebra, Hochschild cohomology and the Goldman bracket on surfces_ ([arXiv:0702859](http://arxiv.org/abs/math/0702859))

More developments are in

* Eric Malm, _String topology and the based loop space_, 2009 ([arXiv:1103.6198](http://arxiv.org/abs/1103.6198), [slides](http://math.ucr.edu/~jbergner/ucr-st-present.pdf))