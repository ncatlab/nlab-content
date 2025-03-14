
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

On the one hand, [[infinity-groupoids|$\infty$-groupoids]] form an [[(infinity,1)-topos|$(\infty,1)$-topos]] ($Grpd_\infty$), while their [[stabilization]] -- plain [[spectra]] -- form instead a [[stable (infinity,1)-category|stable $(\infty,1)$-category]]; on the other hand, the collection of (ie.: the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]] on) *[[parameterized spectra]]*, parameterized over [[infinity-groupoids|$\infty$-groupoids]], forms again an [[(infinity,1)-topos|$(\infty,1)$-topos]]: the "[[tangent (infinity,1)-topos|tangent $(\infty,1)$-topos]]" $T Grpd_\infty$.

This observation is originally due to [Biedermann (2007)](#Biedermann07), noted down in [Joyal (2008) §35](#Joyal08).

In search for a term to capture this curious phenomenon more generally, [Joyal 2015](#Joyal15) proposed to call a ([[pointed (infinity,1)-category|pointed]]) [[presentable (infinity,1)-category|presentable $(\infty,1)$-category]] $\mathcal{C}$ an "$\infty$-locus" if the collection of its $Grpd_\infty$-parameterized objects (namely [[(infinity,1)-functors|$(\infty,1)$-functors]] $Grpd_\infty \to \mathcal{C}$) forms an [[(infinity,1)-topos|$(\infty,1)$-topos]]. 

Notice that the terminology "locus" here is unrelated to the common use of *[[locus]]* in mathematics. Compare the earlier proposal in [Joyal 2008](#Joyal08) to say "[[logos]]" for *[[(infinity,1)-category|$(\infty,1)$-category]]*, which is similarly ideosyncratic.

More generally, one may consider "loci" given by [[(infinity,2)-sheaves|$(\infty,2)$-sheaves]] on any [[(infinity,1)-topos|$(\infty,1)$-topos]] ([Hoyois 2019](#Hoyois19)). 


## Examples

In the above motivating example, $\mathcal{C} =$ [[Spectra]]. In fact, every [[presentable (infinity,1)-category|presentable]] [[stable (infinity,1)-category|stable $(\infty,1)$-category]] is a Joyal $\infty$-locus (essentially by the [stable Giraud theorem](stable+infinity-category#StableGiraud), cf. [Hoyois 2019, p. 1 and Ex. 7](#Hoyois19)).
But, for instance, not just [[spectra]] but already [[prespectra]] and in fact just [[pointed homotopy types]] form a Joyal $\infty$-locus, in this sense. 

If one drops the requirement that $\mathcal{C}$ be [[pointed (infinity,1)-category|pointed]], then every [[(infinity,1)-topos|$(\infty,1)$-topos]] is a Joyal $\infty$-locus (cf. [Hoyois 2019, Ex. 6](#Hoyois19)).


For the case over more general [[base (infinity,1)-toposes|base $(\infty,1)$-toposes]]: [[sheaves of spectra]] over an [[(infinity,1)-site|$(\infty,1)$-site]] $\mathcal{S}$ may be [[parameterized spectrum|parameterized]] over objects of the [[infinity-stack (infinity,1)-topos|$\infty$-stack $(\infinity,1)$-topos]] $Sh_\infty(\mathcal{S})$ and the collection of these parameterized sheaves of spectra forms the [[tangent (infinity,1)-topos|tangent $(\infty,1)$-topos]] $T Sh_\infty(\mathcal{S})$. Analogous statements hold more generally for [[n-excisive (infinity,1)-functors|$n$-excisive $(\infty,1)$-functors]] into any [[(infinity,1)-topos|$(\infty,1)$-topos]] (see [there](https://ncatlab.org/nlab/show/n-excisive+functor#nExcisiveFunctorsFormInfinityTopos)).

## Related concepts

* [[doubly monoidal (∞,1)-topos]]

* [[doubly closed monoidal category]]

## References

The terminology was proposed in:

* {#Joyal15} [[André Joyal]] at [58:00](https://youtu.be/qmCh9KwrQq8?t=3476), [59:52](https://youtu.be/qmCh9KwrQq8?t=3592) in: *New variations on the notion of topos*, talk at IHES (2015) &lbrack;[video](https://www.youtube.com/watch?v=qmCh9KwrQq8)&rbrack;

apparently motivated by the archetypical example of the [[tangent (infinity,1)-topos|tangent]] [[(infinity,1)-topos|$(\infty,1)$-topos]] of [[parameterized spectra]], previously noticed in 

* {#Joyal08} [[André Joyal]], §35 of: _Notes on Logoi_ (2008) &lbrack;[pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf), [[JoyalOnLogoi2008.pdf:file]]&rbrack;

and further highlighted in

* [[Mathieu Anel]], [[André Joyal]], §4.2.3 in: *Topo-logie*, in *[[New Spaces for Mathematics and Physics]]*, Cambridge University Press (2021) 155-257 &lbrack;[doi:10.1017/9781108854429.007](https://doi.org/10.1017/9781108854429.007), [pdf](http://mathieu.anel.free.fr/mat/doc/Anel-Joyal-Topo-logie.pdf)&rbrack;

which goes back to 

* {#Biedermann07} [[Georg Biedermann]], private communication with Joyal (2007)

Dedicated discussion of the notion is in:

* {#Hoyois19} [[Marc Hoyois]], *Topoi of parametrized objects*, Theory and Applications of Categories, **34** 9 (2019) 243-248 &lbrack;[arXiv:1611.02267](https://arxiv.org/abs/1611.02267), [tac:34-09](http://www.tac.mta.ca/tac/volumes/34/9/34-09abs.html)&rbrack;


[[!redirects Joyal loci]]

[[!redirects Joyal infinity locus]]
[[!redirects Joyal infinity loci]]

[[!redirects Joyal infinity-locus]]
[[!redirects Joyal infinity-loci]]

[[!redirects Joyal ∞ locus]]
[[!redirects Joyal ∞ loci]]

[[!redirects Joyal ∞-locus]]
[[!redirects Joyal ∞-loci]]





