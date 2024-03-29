
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--


This entry is about the article

* [[William Lawvere]], 

  _Some Thoughts on the Future of Category Theory_

  ([doi:10.1007/BFb0084208](https://link.springer.com/chapter/10.1007/BFb0084208))

  In: A. Carboni, M. Pedicchio, G. Rosolini (ed.s) 

  _Category Theory_, 

  [[Como|Proceedings of the International Conference held in Como]], 

  Lecture Notes in Mathematics 1488, Springer (1991)

about the formalization of the "[[objective logic]]" of [[Hegel|Hegelian]] [[metaphysics]] ([[Science of Logic]]) and in particular (implicitly) the notion of [[cohesive toposes]]. (See there for further references and other background material).

A closely related text is _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_.

#Contents#
* table of contents
{:toc}

## Exegesis

The article is written in a style typical for Lawvere, where precise general abstract [[category theory|category theoretic]] and [[topos theory|topos theoretic]] situations are discussed more in prose than in the usual style of mathematical writing. The thoughts revolve around a topic that Lawvere takes up in various later articles, which are all listed in the References-section at _[[cohesive topos]]_. In the following we try to illuminate what the article here is saying. Of course such an _exegesis_ may or may not accurately reflect some of the original author's actual intentions.

Pages 6 to 8 in section II of the text is to a large extent a proposal that there is a useful formalization of the [[unity of opposites]] and their "[[Aufhebung]]" that governs [[Georg Hegel]]'s [[metaphysics]] as laid out in his _[[Science of Logic]]_. The proposal is that a "determination of [[being]] and [[becoming]]" is expressed by an [[adjoint modality]]. The tautological example $(\emptyset \dashv \ast)$ is "pure being" and refinements thereof such as $(\flat \dashv \sharp)$ ([[flat modality]] $\dashv$ [[sharp modality]]) characterize more determinate ways of entities to be.


Specifically, the notion of a **[[category of being]]** that Lawvere discusses (following terminology in [[Hegel|Hegel's]] _[[Science of Logic]]_) in _Some Thoughts on the Future of Category Theory_ is the notion that more recently he has been calling a _category of cohesion_ . The following tries to illuminate a bit what's going on .

We restrict attention to the case that the [[category]] "of [[being|Being]]" is a [[topos]] and say _[[cohesive topos]]_ for short. This is a topos that satisfies a small collection of simple but powerful axioms that are supposed to ensure that its [[object]]s may consistently be thought of as _[[geometry|geometric]] [[space]]s_ built out of [[point]]s that are equipped with "cohesive" structure (for instance [[topology|topological structure]], or [[smooth structure]], etc.). So the idea is to axiomatize [[big topos]]es in which [[geometry]] may take place. 

We walk through the main bits of the article:

One [[axiom]] on a [[cohesive topos]] $\mathcal{E}$ is that the [[global section]] [[geometric morphism]] $\Gamma : \mathcal{E} \to \mathcal{S}$  to the given [[base topos]] $\mathcal{S}$ has a further [[left adjoint]] $\Pi_0 := \Gamma_! : \mathcal{E} \to \mathcal{S}$ to its [[inverse image]] $\Gamma^{\ast}$, which we shall write $\mathrm{Disc} := \Gamma^{\ast}$, for reasons discussed below. This extra left adjoint has the interpretation that it sends any object $X$ to the set $\Pi_0(X)$ "of [[connected]] components". What Lawvere calls a [[locally connected topos|connected object]] in the article (p. 4) is hence one that is sent by $\Pi_0$ to the [[terminal object]].

Another [[axiom]] is that $\Pi_0$ preserves finite [[product]]s. This implies by the above that the collection of connected objects is closed under finite products. This appears on page 6. What he mentions there with reference to Hurewicz is that given a topos with such $\Pi_0$, it becomes canonically [[enriched category|enriched]] over the [[base topos]] in a second way, a geometric way.

The meaning of this, like that of various other aspects of cohesive toposes, may be clearer as we make the evident step to 
[[cohesive (∞,1)-topos]]es.  (But notice that this, while inspired by Lawvere, is not due to him.) 

In this more encompassing context the extra [[left adjoint]] $\Pi_0$ becomes a left [[adjoint (∞,1)-functor]] $\Pi_\infty$ which we just write $\Pi$: it sends, one can show, any object to its [[fundamental infinity-groupoid in a locally infinity-connected (infinity,1)-topos
|geometric fundamental ∞-groupoid]], for a notion of geometric paths intrinsic to the $\infty$-topos. The fact that this preserves finite [[product]]s then says that there is a notion of _[[concordance]]_ of [[principal ∞-bundle]]s in the $(\infty,1)$-topos.

The next [[axiom]] on a cohesive topos says that there is also a further [[right adjoint]] $\mathrm{coDisc} := \Gamma^! : \mathcal{S} \to \mathcal{E}$ to a total [[adjoint quadruple]]

$$
  (\Pi_0 \dashv \mathrm{Disc} \dashv \Gamma \dashv \mathrm{coDisc}) :=
  (\Gamma_! \dashv \Gamma^* \dashv \Gamma_* \dashv \Gamma^!) : \mathcal{E} \to \mathcal{S}
$$

such that both $\mathrm{Disc}$ as well as $\mathrm{coDisc}$ are [[full and faithful functor|full and faithful]].

This is what Lawvere is talking about from the bottom of p. 6 on. The _downward functor_ that he mentions is $\Gamma : \mathcal{E} \to \mathcal{S}$. This has the interpretation of sending a cohesive space to its underlying set of points, as seen by the [[base topos]] $\mathcal{S}$. The left and right adjoint inclusions to this are $\mathrm{Disc}$ and $\mathrm{coDisc}$. These have the interpretation of sending a set of points to the corresponding space equipped with either _[[discrete space|discrete cohesion]]_ or _[[codiscrete space|codiscrete (indiscrete) cohesion]]_ . For instance in the case that cohesive structure is [[topology|topological structure]], this will be the [[discrete topology]] and the [[indiscrete space|indiscrete topology]], respectively, on a given set. Being full and faithful, $\mathrm{Disc}$ and $\mathrm{coDisc}$ hence make $\mathcal{S}$ a [[full subcategory]] of $\mathcal{E}$ in two ways (p. 7), though only the image of $\mathrm{coDisc}$ will also be a [[subtopos]], as he mentions on page 7. 

(This has, by the way, an important implication that Lawvere does not seem to mention: it implies that we are entitled to the corresponding [[quasi-topos]] induced by the sub-topos. That, one can show, may be identified with the collection of _[[concrete sheaf|concrete]]_ cohesive spaces. In the case of the cohesive topos for differential geometry, the concrete objects in this sense are precisely the _[[diffeological space]]s_ .  )

He calls the subtopos given by the image of $\mathrm{coDisc} : \mathcal{S} \to \mathcal{E}$ that of "pure [[becoming|Becoming]]" further down on p. 7, whereas the subcategory of discrete objects he calls that of "non [[becoming|Becoming]]". One way one might understand this terminology is as follows:

whereas any old [[(∞,1)-topos]] is a collection of _[[space]]s_ , a [[cohesive (∞,1)-topos]] comes with the extra adjoint $\Pi$ which, as mentioned above, has the interpretation of sending any space to its [[fundamental ∞-groupoid]]. Therefore there is an intrinsic notion of _geometric paths_ in any cohesive $\infty$-topos. This allows notably to define [[parallel transport]] along paths and [[higher parallel transport]] along higher [[dimension]]al paths, hence a kind of _dynamics_ . In fact there is [[differential cohomology]] in every cohesive $(\infty,1)$-topos. 

Now, in a [[discrete space|discrete object]] there are no non-trivial paths (formally because   by the fact that $Disc$  is [[full and faithful functor|full and faithful]] and [[left adjoint]] to $\Pi$ we have $\Pi Disc \simeq Id$), so there is "no dynamics" in a discrete object hence "no [[becoming]]", if one wishes. Conversely in a [[codiscrete space|codiscrete object]] every sequence of points whatsoever counts as a path, hence the distinction between the space and its "dynamics" disappears and so we have "pure [[becoming]]", if one wishes.

Notice next that every [[adjoint triple]] induces an [[adjoint monad]]. In the present situation we get

$$
  (\mathrm{Disc} \;\Gamma \dashv \mathrm{coDisc}\; \Gamma) : \mathcal{E} \to \mathcal{E}
$$

This is what Lawvere calls the _skeleton_ and the _coskeleton_ on p. 7. In the [[(∞,1)-topos]] context the left adjoint $\mathbf{\flat} := \mathrm{Disc} \; \Gamma$ has the interpretation of sending any object $A$ to the coefficient for cohomology of [[local system]]s with coefficients in $A$.

The paragraph wrapping from page 7 to 8 comments on the possibility that the [[base topos]] $\mathcal{S}$ is not just that of sets. $\mathcal{S} =$ [[Set]], but something richer. An example of this is that of _super cohesion_ (in the sense of [[superalgebra]] and [[supergeometry]]): the topos of [[smooth super ∞-groupoid|smooth super-geometry]] is cohesive over the base topos of [[super ∞-groupoid|bare super-sets]].


What follows on page 9 are thoughts which it seems Lawvere has not formalized further later on. But then on the bottom of p. 9 he gets to the axiomatic identification of [[infinitesimal space|infinitesimal]] or _formal_ spaces in the cohesive topos. In the more recent article _Axiomatic Cohesion_ what he says here on p. 9 is formalized as follows: he says an object $X \in \mathcal{E}$ is infinitesimal if the canonical morphism $\Gamma X \to \Pi_0 X$ is an [[isomorphism]]. To see what this means, suppose that $\Pi_0 X = *$, hence that $X$ is connected. Then the isomorphism condition means that $X$ has exactly one global point. But $X$ may be bigger: it may be a formal neighbourhood of that point, for instance it may be [[infinitesimally thickened point]]  $\mathrm{Spec} \;k[x]/(x^2)$ that is formally dual to the [[ring of dual numbers]]. A general $X$ for which $\Gamma X \to \Pi_0 X$ is an iso is hence a disjoint union of formal neighbourhoods of points.

Again, the meaning of this becomes more pronounced in the context of [[cohesive (∞,1)-topos]]es: there objects $X$ for which $\Gamma X \simeq * \simeq \Pi X$ have the interpretation of being _[[∞-Lie algebroid|formal ∞-groupoid]]s_ , for instance [[Lie integration|formally exponentiated]] [[L-∞ algebra]]s. And so there is [[∞-Lie theory]] canonically in every cohesive $\infty$-topos.

More discussion of all this is at [[schreiber:differential cohomology in a cohesive topos]].


## Related entries

18 years later at the same place, Lawvere gives a lecture series on this topic: _[[Cohesive Toposes -- Combinatorial and Infinitesimal Cases]]_.

## References

* A sequence of videos covering the talk in Como is available [on YouTube](http://www.youtube.com/playlist?list=PLRIsuk3ZOitzDqeVKOZhe0MrzEUtRNAh5)

category: reference