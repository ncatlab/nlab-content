

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea


The [[model category|model structure]] $sPSh(C)$ on [[sSet]]-[[enriched functor category|enriched presheaves]] is supposed to be a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]] on an [[sSet-site]] $C$.

It generalizes the [[model structure on simplicial presheaves]] which is the special case obtained when $C$ happens to be just an ordinary [[category]].

This means that in as far as the [[model structure on simplicial presheaves]] models [[∞-stack]]s, the model structure on [[sSet]]-[[enriched category|enriched categories]] model [[derived stack]]s.

## Definition 

The construction of the model structure on [[sSet]]-[[enriched category|enriched categories]] closely follows the discussion of the [[model structure on simplicial presheaves]], only that everything now takes place in [[enriched category theory]].

+-- {: .un_def}
###### Notation and conventions

Regard the [[closed monoidal  category]]  [[sSet]] as a [[simplicially enriched category]] in the canonical way.

For $C$ any $sSet$-category, write $sk_1 C$ for its underlying ordinary [[category]].

Write $[C^{op}, sSet]$ for the [[enriched functor category]].

=--

Hence the ordinary category $sk_1 [C^{op}, sSet]$ has as objects [[enriched functor]]s $C^{op} \to sSet$ and a morphism $f : A \to B$ in $sk_1 [C^{op}, sSet]$ is a [[natural transformation]]  given by a collection of morphisms $f_c : A(c) \to B(c)$ in [[sSet]], for each object $c \in C$.


+-- {: .un_defn}
###### Definition
**(global model structure)**

Let be $C$ a [[simplicially enriched category]]. 

The **global projective model structure** $sk_1[C^{op},sSet]_{proj}$ on $sk_1[C^{op}, sSet]$ 

* fibrations and weak equivalences are those transformations that are objectwise fibrations and weak equivalences in the standard [[model structure on simplicial sets]].

=--

+-- {: .un_prop}
###### Proposition

The global projective model structure on $sk_1 [C^{op}, sSet]$ makes the $sSet$-category $[C^{op}, sSet]$ a [[combinatorial simplicial model category]].

=--

+-- {: .un_def}
###### Definition

For $C$ an [[sSet-site]], the **local projective model structure** on $sk_1 [C^{op}, sSet]$ is the [[Bousfield localization of model categories|left Bousfield localization]] of $sk_1 [C^{op}, sSet]_{proj}$ at...

=--

This appears on ([To&#235;nVezzosi, page 14](#Toenvezzosi)).



## Properties

### Over an unenriched site

It seems that the claim is that, indeed, in the special case that $C$ happens to be an ordinary category, the model structure on $sPSh(C)_{proj}^{l loc}$ reproduces the projective [[local model structure on simplicial presheaves]].

### Presentation of $(\infty,1)$-toposes


+-- {: .un_defn}
###### Definition

For an [[sSet-site]] $C$ regarded as an [[(∞,1)-site]], the local model structure on $[C^{op}, sSet]$ is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]] on $C$, in that there is an [[equivalence of (∞,1)-categories]]

$$
  ([C^{op}, sSet]_{loc})^\circ \simeq Sh_{(\infty,1)}(C)
  \,.
$$

=--

This is [Lurie, prop. 6.5.2.14, remark 6.5.2.15](#Lurie).

## Examples

### Derived geometry

Where a [[topos]] or [[(∞,1)-topos]] over an ordinary [[site]] encodes [[higher geometry]], over a genuine [[sSet-site]] one speaks of [[derived geometry]]. An [[∞-stack]] on such a higher site is also called a [[derived stack]]. 

Therefore the model structure on $sSet$-presheaves serves to model contexts of derived geometry. For instance over the [[etale (∞,1)-site]].

(...)

## References

The theory of model structures on $sSet$-enriched presheaf categories was developed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Topos Theory_ ([arXiv](http://arxiv.org/abs/math/0207028))
{#ToenVezzosi}

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ Proceedings of the Program _Stacks, Intersection theory and Non-abelian Hodge Theory_ , MSRI, Berkeley, January-May
2002 ([arXiv:0212330](http://arxiv.org/abs/math/0212330))

The relation to intrinsically defined [[(∞,1)-topos theory]] is around remark 6.5.2.15 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
{#Lurie}



[[!redirects model structure on SimpSet-enriched presheaves]]
[[!redirects model structure on sSet-enriched presheaves]]
[[!redirects model structure on SSet-enriched presheaves]]
[[!redirects model structure on sSet-presheaves]]
[[!redirects model structure on SSet-presheaves]]
[[!redirects model structure on simplicially enriched presheaves]]