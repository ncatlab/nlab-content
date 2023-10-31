

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[canonical model structure]] on the 1-[[category]] of [[groupoids]] and [[functors]] is a presentation of the [[(2,1)-category]] of [[groupoids]], [[functor]]s and [[natural isomorphisms]].

This is one flavor of the various [[natural model structure]]s on categories and higher categories.

## Definition


+-- {: .num_defn}
###### Definition

Let [[Grpd]] be the 1-[[category]] of [[small category|small]] [[groupoid]]s and [[functor]]s between them. Say that a morphism in $Grpd$ --- a [[functor]] $f \colon C \longrightarrow D$ --- is 

* a _[[weak equivalence]]_ if it is an [[equivalence of categories]];

* a _[[fibration]]_ if it is an [[isofibration]];

* a _[[cofibration]]_ if it is [[injective-on-objects functor|injective on objects]].

=--

+-- {: .num_prop}
###### Proposition

Equipped with this structure $Grpd_{nat}$ is a [[model category]] which is

* [[cofibrantly generated model category|cofibrantly generated]];

* [[left proper model category|left proper]]

* a [[simplicial model category]] with respect to the natural [[sSet]]-[[enriched category]] structure induced by the canonical enrichment over itself, under the [[nerve]].

=--

The claim that this is indeed a model structure is due to [Anderson 1978](#Anderson78), repeated by [Bousfield 1989](#Bousfield89). The first to publish a proof seems to be [Strickland 2000](#Strickland00). In the context of the [[model structure for (2,1)-sheaves]] it appears as [Hollander 2001, theorem 2.1](#Hollander01).

## Properties

+-- {: .num_prop}
###### Observation

The model structure $Grpd_{nat}$ is the restriction of the
[[canonical model structure on Cat]] from [[categories]] to groupoids.

=--

See [[natural model structure]] for more.

+-- {: .num_defn}
###### Definition

Let

$$
  (\tau \dashv N) : Grpd \stackrel{\overset{\tau}{\leftarrow}}{\underset{N}{\to}}
   sSet
$$

be the pair of [[adjoint functor]]s, where $N$ is the [[nerve]] of [[groupoid]]s with values in [[sSet]].

=--

+-- {: .num_prop}
###### Proposition

With the natural model structure on $Grpd$ and the standard [[model structure on simplicial sets]] this is a [[Quillen adjunction]]

$$
  (\tau \dashv N) : Grpd_{nat} \stackrel{\overset{\tau}{\leftarrow}}{\underset{N}{\to}}
   sSet_{Quillen}
  \,.
$$

and $Grpd_{nat}$ is the [[transferred model structure]] obtained from $sSet_{Quillen}$ under this adjunction.

=--

## Related concepts

* [[canonical model structure]]

* [[canonical model structure on Cat]]

* **canonical model structure on $Grpd$**

  * [[model structure for n-groupoids]]

  * [[model structure for ∞-groupoids]]

* [[canonical model structure on Operad]]


## References

Some aspects (like the pullback stability of fibrations of groupoids in its prop. 2.8) appeared in 

* {#Brown70} [[Ronnie Brown]], *Fibrations of groupoids*, Journal of Algebra **15** 1 (1970) 103-132

The existence of the model structure is stated (without proof) in 

* {#Anderson78} [[Donald W. Anderson]], p. 783 (12 of 37) in: *Fibrations and geometric realization*,  Bull. Amer. Math. Soc. **84** 5 (1978) 765-788 &lbrack;[euclid:1183541139](http://projecteuclid.org/euclid.bams/1183541139)&rbrack;

and (by referencing Anderson, still without proof) in:

* {#Bousfield89} [[Aldridge Bousfield]], _Homotopy Spectral Sequences and Obstructions_ , Israel Journal of Math., **66** 1-3 (1989) 54-105 &lbrack;[doi:10.1007/BF02765886](https://doi.org/10.1007/BF02765886)

The actual proof is spelled out in:

* {#Strickland00} [[Neil Strickland]], §6.1 of: _$K(n)$-local duality for finite groups and groupoids_ , Topology **39** 4 (2000) &lbrack;[arXiv:math/0011109](https://arxiv.org/abs/math/0011109), <a href="https://doi.org/10.1016/S0040-9383(99)00031-2">doi:10.1016/S0040-9383(99)00031-2</a>&rbrack;

The model structure on functors with values in $Grpd_{nat}$ (a [[model structure for (2,1)-sheaves]]):

* {#Hollander01} [[Sharon Hollander]], *A homotopy theory for stacks*, Israel Journal of Mathematics **163** 1 (2008) 93-124 &lbrack;[arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247), [doi:10.1007/s11856-008-0006-5](https://doi.org/10.1007/s11856-008-0006-5)&rbrack;


That the model structure on groupoids is a [[cartesian monoidal model category]] follows with 

* [[Amit Sharma]], Thm. 2.24 in: *Picard groupoids and $\Gamma$-categories*, [[Cahiers]] **LXIV** 3 (2023) &lbrack;[arXiv:2002.05811](https://arxiv.org/abs/2002.05811), [pdf](http://cahierstgdc.com/wp-content/uploads/2023/07/SHARMA_LXIV-3.pdf)&rbrack;

(The theorem there is stated there for the groupoidal localization of the model structure on $Cat$, instead, but it immediately applies to the model structure on groupoids, too.)

[[!redirects natural model structure on groupoids]]


[[!redirects canonical model structure on Grpd]]

[[!redirects model structure on groupoids]]
[[!redirects model structures on groupoids]]


