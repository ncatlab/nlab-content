
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **&#268;ech model structure on simplicial presheaves** on a [[site]] $C$ is a model for the [[topological localization]] of an [[(∞,1)-category of (∞,1)-presheaves]] on $C$ to the [[(∞,1)-category of (∞,1)-sheaves]]. 

It is obtained from the the [[global model structure on simplicial presheaves]] on $C$ by [[Bousfield localization of model categories|left Bousfield localization]]s at [[Cech cover]]s:  its fibrant objects are [[∞-stack]]s that satisfy [[descent]] over [[?ech cover]]s but not necessarily over [[hypercover]]s.

Accordingly, the [[(∞,1)-topos]] [[presentable (infinity,1)-category|presented]] by the &#268;ech model structure has as its [[cohomology]] theory [[?ech cohomology]].

Further [[Bousfield localization of model categories|left Bousfield localization]] at [[hypercover]]s leads from the &#268;ech model structure to the Joyal-Jardine [[local model structure on simplicial presheaves]] that presents the [[hypercomplete (∞,1)-topos]] which is the [[hypercompletion]] of that presented by the &#268;ech model structure.


## Definition

Let $C$ be a small [[site]] and write $[C^{op}, sSet]_{proj}$ and $[C^{op}, sSet]_{inj}$ for the projective and injective [[global model structure on simplicial presheaves]], respectively. 

For $\{U_i \to V\}_i$ a covering family in the [[site]] $C$, let

$$
  C(\{U_i\})
  :=
  \left(
    \cdots\stackrel{\to}{\stackrel{\to}{\to}}\coprod_{i j} U_{i j}\stackrel{\to}{\to}\coprod_i U_i
  \right)
$$

be the corresponding [[Cech nerve]], regarded as a [[simplicial presheaf]] on $C$. This comes canonically with a morphism

$$
  C(\{U_i\}) \to V
$$

of simplicial presheaves, the corresponding _&#268;ech cover morphism_ .

Notice that by the discussion at [model structure on simplicial presheaves - fibrant and cofibrant objects](http://ncatlab.org/nlab/show/model+structure+on+simplicial+presheaves#FibAndCofibObjects) this is a morphism between cofibrant objects.

+-- {: .un_defn}
###### Definition

The injective (projective) **&#268;ech model structure on simplicial presheaves** $[C^{op},sSet]_{Cech}$ on $C$ is the [[Bousfield localization of model categories|left Bousfield localization]] of $[C^{op}, sSet]_{inj}$ ($[C^{op}, sSet]_{proj}$) at the set of &#268;ech cover morphisms.


=--

By the general poperties of [[Bousfield localization of model categories|Bousfield localization]] this means that the fibrant-cofibrant objects $A$ of $[C^{op},sSet]_{Cech}$ are precisely those that are fibrant-cofibrant in the global model structure and in addition satisfy the [[descent]] condition that for all covers $\{U_i \to V\}$ the morphism of simplicial sets

$$
  A(U) \simeq [C^op,sSet](V,U) \to [C^{op},sSet](C(\{U_i\}), A)
$$

is a weak equivalence in the standard [[model structure on simplicial sets]].

This is the model for the $\infty$-analog of the [[sheaf]] condition, modelling the [[topological localization]] of an $(\infty,1)$-presheaf $(\infty,1)$-topos.


+--{: .query}
[[Mike Shulman]]: Two questions, one (hopefully) easy and one (perhaps) hard:

1. Is there a Quillen equivalent &#268;ech model structure on simplicial *sheaves*?  Can we just lift the model structure for simplicial presheaves along the sheafification adjunction?

1. Is there a characterization of the weak equivalences in either &#268;ech model structure?

I am particularly interested in this for the following reason.  According to Beke in *Sheafifiable homotopy model categories*, the weak equivalences in the [[local model structure on simplicial sheaves]] are precisely those maps $f\colon X\to Y$ of simplicial objects in the corresponding 1-topos of sheaves of sets such that the statement "$f$ is a weak equivalence of simplicial sets" is true in the [[internal logic]] of the topos (at least, interperiting "$f$ is a weak equivalence of simplicial sets" by one particular set of geometric sentences whose interpretation in $Set$ is equivalent to saying that a simplicial map is a weak equivalence).  But if, as [[HTT]] teaches us, &#268;ech descent is often to be preferred to hyperdescent, then we should be interested in &#268;ech weak equivalences instead.  So I would really like to know what it means for a map of simplicial sheaves to be a &#268;ech weak equivalence, in the *internal logic* of the 1-topos of sheaves of sets.  If nothing else, I think such a characterization would help me understand the real meaning of [[hypercompletion]].  But any sort of characterization of them would be better than none.

[[Urs Schreiber]]: below is a reply to the first question.

[[Mike Shulman]]: Thanks for attacking this.  I thought I should also mention, for anyone listening in, that this question is evidently also relevant to what the correct notion of [[internal ∞-groupoid]] may be.
=--

> check

We may form the [[transferred model structure]] on simplicial _[[sheaf|sheaves]]_ by transferring along the degreewise [[sheafification]] [[adjunction]]

$$
  Sh(C) \stackrel{\overset{sh}{\leftarrow}}{\underset{}{\hookrightarrow}}
  PSh(C)
  \,.
$$

This defines fibrations and weak equivalences in $sSh(C)$ to be those morphisms that are fibrations or weak equivalences, respectively, as morphism in  $sPSh(C)_{Cech} = [C^{op},sSet]_{Cech}$.


As discussed there, sufficient conditions for this to be a model structure is that

* the inclusion $Sh(C) \hookrightarrow PSh(C)$ preserves [[filtered colimit]]s;

* $sSh(C)$ has functorial fibrant replacement and functorial [[path object]]s for fibrant objects. 

Since [[sheafification]] does preserve [[filtered colimit]]s the first condition is satisfied degreewise and hence is satisfied.

+--{: .query}
[[Mike Shulman]]: I believe that sheafification preserves $\kappa$-filtered colimits for some sufficiently large $\kappa$, but if the site has covers of infinite cardinality, I don't see why sheafification would preserve $\omega$-filtered colimits.  But I think this is enough for the proof to work.
=--

Since the [[small object argument]] holds in $sSh(C)$ for generating acyclic cofibrations we have functorial fibrant replacement. And a path object is obtained just by forming objectwise the standard path object in [[sSet]], as in $[C^{op}, sSet]$.

+--{: .query}
[[Mike Shulman]]: The small object argument doesn't automatically produce functorial fibrant replacements in this context... isn't the whole question whether the map to the "fibrant replacement" is still a weak equivalence (in the underlying category)?  I.e. whether $F(J)$-cell complexes are still weak equivalences.
=--


## References

A detailed though unfinished account of the &#268;ech model structure is given in

* Daniel Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

But beware of this document is unfinished. Some aspects of this appeared in 

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  


[[!redirects ?ech model structure on simplicial presheaves]]
[[!redirects Cech model structure on simplicial presheaves]]
[[!redirects ?ech model structure on simplicial presheaves]]
