

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[complex geometry]], the _Oka-Grauert principle_ states that over [[complex manifolds]] $S$ which are *[[Stein manifolds]]*, the [[non-abelian cohomology]]-classification of [[holomorphic vector bundles]] coincides with that of [[topological vector bundles]], 

$$
  S \;\text{is Stein}
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;
  H^1
  \Big(
    S;
    \,
    \underline{GL(n, \mathbb{C})}_{hol}
  \Big)
  \,\simeq\,
  H^1
  \Big(
    S;
    \,
    \underline{GL(n, \mathbb{C})}_{top}
  \Big)
  \,.
$$

This was originally proven for holomorphic [[line bundles]] by [Oka 1939](#Oka39) (in which case it says that [[holomorphic line bundles]] over [[Stein manifolds]] are fully classified by their [[first Chern class]]) and generalized by [Grauert 1958](#Grauert58) to [[holomorphic vector bundles]] and further to holomorphic [[principal bundles]] with [[structure group]] any [[complex Lie group]].

As a principle, this *Oka-Grauert principle* is sometimes stated as follows ([Forstnerič 2012](#Forstneric12)):

> Analytic problems on Stein spaces which can be cohomologically formulated have only topological [[obstructions]].

More generally, for suitable [[complex manifolds]] $A$ now called *[[Oka manifolds]]* ([Forstnerič 2009a](#Forstneric09a)) -- including (see [here](Oka+manifold#ComplexProjectiveSpaceIsOkaManifold)) the complex [[Grassmannians]] that serve as [[classifying spaces]] for [[complex vector bundles]] --, the inclusion into the [[compact-open topology|space of continuous maps]] $S \to A$, out of a [[Stein manifold]] $S$, of the [[topological subspace|subspace]] of [[holomorphic functions]] is a [[weak homotopy equivalence]]:

$$
  Maps_{hol}(S, \, A) 
    \xhookrightarrow{ \simeq_{whe} } 
  Maps(S, \, A)
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  \underset{n \in \mathbb{N}}{\forall}
  \;\;
  \pi_n
  \big(
    Maps_{hol}(S, \, A) 
  \big)
    \xrightarrow{\sim}
  \pi_n 
  \big( 
    Maps(S, \, A)
  \big)  
  \,.
$$

(review in [Forstnerič & Lárusson 2011, Cor. 3.5](#ForstnericLarusson11), [Forstnerič 2013, (1.1)](#Forstneric13))

More generally, an analogous statement applies to suitable [[fiber bundles]] of [[Oka manifolds]] over [[Stein manifolds]] and their [[spaces of sections]] ([Forstnerič 2009b](#Forstneric09b)).

This [[homotopy theory|homotopy theoretic]] *weak homotopy equivalence Oka principle* goes back to results of [Gromov 89](#Gromov89), where (?) it is viewed an an example of the [[h-principle]]. 

The [[duality]] between [[Stein manifolds]] and [[Oka manifolds]] in this [[homotopy theory|homotopy]]-theoretic Oka principle is fully brought out by the existence of a [[model category]] for [[complex analytic ∞-groupoids]] in which a [[complex manifold]] is [[cofibrant object|cofibrant]]/[[fibrant object]] if it is [[Stein manifold|Stein]]/[[Oka manifold|Oka]], respectively ([Lárusson 2001](#Larusson01), [03](#Larusson03)).


## Homotopical Oka principle
 {#HomotopicalOkaPrinciple}

\begin{prop}\label{WeakHomotopyEquivalenceOkaPrinciples}
**(weak homotopy equivalence Oka principle)**
For 

* $S$ a [[Stein manifold]],

* $X$ an [[Oka manifold]],

the inclusion
$$
  Maps_{hol}
  \big(
    S, \, X
  \big)
  \xhookrightarrow{\;\simeq_{whe}\;}
  Maps
  \big(
    S ,\, X
  \big)
$$
of the [[subspace]] of [[holomorphic functions]] 
into the [[mapping space]] of their [[underlying]] [[topological spaces]] (with the [[compact-open topology]])
is a [[weak homotopy equivalence]].
\end{prop}
(review in [Forstnerič & Lárusson 2011, Cor. 3.5](#ForstnericLarusson11))

More generally, for $Z \xrightarrow{\;} S$ a stratified holomorphic [[fiber bundle]] of [[Oka manifolds]], the corresponding inclusion of [[spaces of sections]]

$$
  \Gamma_{hol}\big(S, \, Z \big)
  \xhookrightarrow{\;\simeq_{whe}\;}
  \Gamma\big(S, \, Z \big)
$$

is a [[weak homotopy equivalence]].

([Forstnerič 2011, Cor. 5.4.8](#Forstneric11))

## In higher complex analytic geometry
 {#StatementInComplexAnalyticGeometry}

In ([Lárusson 2001](#Larusson01), [Lárusson 2003](#Larusson03)) this is formulated in terms of [[higher complex analytic geometry]] of [[complex analytic infinity-groupoids]].

Say that a [[complex manifold]] $X$ is an _[[Oka manifold]]_ if for every [[Stein manifold]] $\Sigma$ the canonical morphism

$$
  Maps_{hol}(\Sigma, X) \longrightarrow Maps_{top}(\Sigma, X)
$$

from the [[mapping space]] of [[holomorphic functions]] to that of [[continuous functions]] (both equipped with the [[compact-open topology]]) is a [[weak homotopy equivalence]].

+-- {: .num_theorem}
###### Theorem

This is the case precisely if $Maps_{hol}(-,X) \in Psh_\infty(SteinSp)$ satisfies [[descent]] with respect to [[finite set|finite]] [[covers]].

=--

([Larusson 01, theorem 2.1](#Larusson01))

+-- {: .num_theorem}
###### Theorem

The category of [[complex manifolds]] and [[holomorphic maps]] can be embedded into a Quillen [[model category]] such that:

* a holomorphic map is a [[weak equivalence]] in the ambient model category if and only if it is a [[homotopy equivalence]] in the usual topological sense;

* a holomorphic map is a [[fibration]] if and only if it is an Oka map. In particular, a complex manifold is [[fibrant object|fibrant]] if and only if it is an [[Oka manifold]];

* a [[complex manifold]] is [[cofibrant]] if and only if it is [[Stein manifold|Stein]];

* a Stein inclusion is a [[cofibration]].

=--

([Larusson 03](#Larusson03) -- apparently this follows an observation due to [[J. F. Jardine]] and uses his [[intermediate model structure on simplicial presheaves]])


## Related concepts

* [[Oka manifold]]

* [[homotopy of rational maps]]

* [[smooth Oka principle]]

## References

Introduction and review:

* {#Larusson10} [[Finnur Lárusson]], _What is an Oka manifold?_, Notices AMS Volume 57, Number 1, 2010 ([pdf](http://www.ams.org/notices/201001/rtx100100050p.pdf), [[Larussen_OkaManifolds.pdf:file]])

* {#ForstnericLarusson11} [[Franc Forstnerič]], [[Finnur Lárusson]], *Survey of Oka theory*, New York J. Math., 17a (2011), 1-28 ([arXiv:1009.1934](https://arxiv.org/abs/1009.1934), [eudml:232963](https://eudml.org/doc/232963))

* {#Forstneric11} [[Franc Forstnerič]], Section 5.3 of: _Stein manifolds and holomorphic mappings -- The homotopy principle in complex analysis_, Springer 2011 ([doi:10.1007/978-3-642-22250-4](https://link.springer.com/book/10.1007/978-3-642-22250-4))

* {#Forstneric13} [[Franc Forstnerič]] (appendix by [[Finnur Lárusson]]), *Oka manifolds: From Oka to Stein and back*, Annales de la Faculté des sciences de Toulouse, Mathématiques, Série 6, Tome 22 (2013) no. 4, pp. 747-809 ([numdam:AFST_2013_6_22_4_747_0](https://afst.centre-mersenne.org/item/?id=AFST_2013_6_22_4_747_0))

* [[Franc Forstnerič]], *Developments in Oka theory since 2017* ([arXiv:2006.07888](https://arxiv.org/abs/2006.07888))

* {#Forstneric12} [[Franc Forstnerič]], *Gromov's contribution to the Oka principle*, 2012 ([pdf](https://www.fmf.uni-lj.si/~forstneric/papers/2012Gromov%27scontribution.pdf), [[Forstneric_GromovContributionToOka.pdf:file]])

See also:

* Georges Elencwajg, [MO:a/60053](http://mathoverflow.net/a/60053/381)


Original articles:

* {#Oka39} [[Kiyoshi Oka]], _Sur les fonctions des plusieurs variables. III: Deuxi&#232;me probl&#232;me de Cousin_, J. Sc. Hiroshima Univ. __9__, 7&#8211;19 (1939) ([doi:10.32917/hmj/1558490525](https://projecteuclid.org/journals/hiroshima-mathematical-journal/volume-9/issue-none/Sur-les-fonctions-analytiques-de-plusieurs-variables-IIIDeuxi%c3%a8me-probl%c3%a8me-de/10.32917/hmj/1558490525.full))

* {#Grauert58} [[Hans Grauert]], _Analytische Faserungen &#252;ber holomorph-vollst&#228;ndigen R&#228;umen_, Math. Ann. __135__, 263&#8211;-273 (1958) ([doi:10.1007/BF01351803](http://dx.doi.org/10.1007/BF01351803))
 
* {#Gromov89} [[Mikhail Gromov]], _Oka's principle for holomorphic sections of elliptic bundles_, J. Amer. Math. Soc. __2__ (1989), 851&#8211;-897 ([doi:10.2307/1990897](https://doi.org/10.2307/1990897))

* [[Franc Forstnerič]], _The Oka principle for sections of stratified fiber bundles_, Pure Appl. Math. Quarterly (Special Issue in honor of Joseph J. Kohn), 6 (2010), no. 3, 843--874 ([arxiv/0705.0591](http://arxiv.org/abs/0705.0591), [doi:10.4310/PAMQ.2010.v6.n3.a11](https://dx.doi.org/10.4310/PAMQ.2010.v6.n3.a11))

Proof of the [[homotopy theory|homotopy-theoretic]] Oka principle:

* {#Forstneric09a} [[Franc Forstnerič]], _Oka manifolds_, Comptes Rendus Mathematique, Acad. Sci. Paris 347 (2009), 1017&#8211;20 ([arXiv:0906.2421](https://arxiv.org/abs/0906.2421), [doi:10.1016/j.crma.2009.07.005](https://doi.org/10.1016/j.crma.2009.07.005))

* {#Forstneric09b} [[Franc Forstnerič]], _Oka maps_, Comptes Rendus Mathematique, Acad. Sci. Paris, Ser. I 348 (2010) 145-148 ([arxiv/0911.3439](http://arxiv.org/abs/0911.3439), [doi:10.1016/j.crma.2009.12.004](https://doi.org/10.1016/j.crma.2009.12.004))

See also:

* [[Finnur Lárusson]], *Applications of a Parametric Oka Principle for Liftings*, In: *Complex Analysis*. Trends in Mathematics. Birkhäuser (2010) ([doi:10.1007/978-3-0346-0009-5_12](https://doi.org/10.1007/978-3-0346-0009-5_12)) 


Discussion in terms of [[higher complex analytic geometry]] and [[complex analytic ∞-groupoids]]:

* {#Larusson01} [[Finnur Lárusson]], _Excision for simplicial sheaves on the Stein site and Gromov's Oka principle_,  International Journal of Mathematics Vol. 14, No. 02, pp. 191-209 (2003)  ([arXiv:math/0101103](http://arxiv.org/abs/math/0101103), [doi:10.1142/S0129167X03001727](https://doi.org/10.1142/S0129167X03001727))

* {#Larusson03} [[Finnur Lárusson]], _Model structures and the Oka principle_, Journal of Pure and Applied Algebra Volume 192, Issues 1–3, 1 September 2004, Pages 203-223 ([math.CV/0303355](http://arxiv.org/abs/math/0303355), [doi:10.1016/j.jpaa.2004.02.005](https://doi.org/10.1016/j.jpaa.2004.02.005))

Application to [[minimal surfaces]]:

* [[Antonio Alarcón]], [[Franc Forstnerič]], *New complex analytic methods in the theory of minimal surfaces: a survey*,  Journal of the Australian Mathematical Society, 106(3), 287-341 ([arXiv:1711.08024](https://arxiv.org/abs/1711.08024), [doi:10.1017/S1446788718000125](https://doi.org/10.1017/S1446788718000125))

See also:

* Tyson Ritter, _A strong Oka principle for embeddings of some planar domains into $C\times C^*$_, [arxiv/1011.4116](http://arxiv.org/abs/1011.4116)


[[!redirects Oka theory]]
[[!redirects Oka's theory]]
[[!redirects Oka's principle]]

[[!redirects Oka-Grauert principle]]

[[!redirects homotopical Oka principle]]
