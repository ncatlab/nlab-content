
> This entry is supposed to be a survey of and motivation for the role of [[fiber bundles]] in [[physics]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

All of [[physics]] has two aspects: a local or even [[infinitesimal object|infinitesimal]] aspect, and a global aspect. Much of traditional lore deals just with the local and infinitesimal aspects -- the _[[perturbative field theory|perturbative]]_ aspects_ and [[fiber bundles]] play little role there. But they are the all-important structure that govern the global -- the _[[non-perturbative field theory|non-perturbative]]_ -- aspect. [[bundles|Bundles]] are the _global_ structure of [[physical fields]] and they are irrelevant only for the crude local and perturbative description of reality.

For instance the [[gauge fields]] in [[Yang-Mills theory]], hence in [[electromagnetism]], in [[QED]] and in [[QCD]], hence in the [[standard model of particle physics|standard model of the known universe]], are not really just the local [[differential 1-forms]] "$A_\mu^a$" known from so many textbooks, but are _globally_ really [[connections on principal bundles]] (or their [[associated bundles]]) and this is all-important once one passes to [[non-perturbative field theory|non-perturbative]] [[Yang-Mills theory]], hence to the full story, instead of its infinitesimal or local approximation.

Notably what is called a _[[Yang-Mills instanton]]_ in general and the _[[QCD instanton]]_ in particular is nothing but the underlying nontrivial class of the principal bundle underlying the Yang-Mills [[gauge field]]. Specifically, what physicists call the _[[instanton number]]_ for [[special unitary group|SU(2)]]-[[gauge field theory]] in 4-dimensions is precisely what mathematically is called the [[Chern class|second Chern-class]], a "[[characteristic class]]" of these gauge bundles.

> _YM Instanton = class of principal bundle underlying the non-perturbative gauge field_

To appreciate the utmost relevance of this, observe that the non-perturbative vacuum of the [[experiment|observable world]] is a "sea of instantons" with about one [[Yang-Mills instanton|YM instanton]] per [[femtometer]] to the 4th. See for instance the first sections of ([Schaefer-Shuryak 98](instanton+in+QCD#SchaeferShuryak98))
for a review of this fact. So the very substance of the physical world, the very vacuum that we inhabit, is all controled by non-trivial fiber bundles and is inexplicable without these.

Also [[monopole]] solutions in physics are mathematically nontrivial [[principal bundles]]. For instance the [[Dirac monopole]] (that appears in [[Dirac charge quantization]]) or the [[Yang monopole]].

Similarly [[fiber bundles]] control all other [[topology|topologically]] non-trivial aspects of [[physics]]. For instance most [[quantum anomalies]] are the statement that what looks like an [[action functional|action]] _[[function]]_ to feed into the [[path integral]], is globally really the [[section]] of a non-trivial bundle -- notably a [[Pfaffian line bundle]] resulting from the [[fermionic path integrals]]. Moreover _all_ [[classical anomalies]] are statements of nontrivializability of certain fiber bundles. 

Indeed, as the discussion there shows, [[quantization]] as such, if done [[non-perturbative field theory|non-perturbatively]], is all about lifting [[differential form]] data to [[line bundle]] data, this is called the _[[prequantum line bundle]]_ which exists over any globally quantizable [[phase spaces]] and controls all of its [[quantum theory]]. It reflects itself in many [[central extensions]] that govern [[quantum physics]], such as the [[Heisenberg group]] central extension of the Hamiltonian translation and generally and crucially the [[quantomorphism group]] central extension of the [[Hamiltonian diffeomorphisms]] of [[phase space]]. All these [[central extensions]] are non-trivial fiber bundles, and the "quantum" in "quantization" to a large extent a reference to the discrete (quantized) [[characteristic classes]] of these bundles. One can indeed understand quantization as such as the lift of infinitesimal classical differential form data to global bundle data. This is described in detail at _[quantization -- Motivation from classical mechanics and Lie theory](quantization#MotivationFromClassicalMechanicsAndLieTheory)_.

But actually the role of fiber bundles reaches a good bit deeper still. Quantization is just a certain [[extension]] step in the general story, but already [[classical field theory]] cannot be understood globally without a notion of bundle. Notably the very formalization of what a _[[field (physics)|classical field]]_ really is says: a [[section]] of a _[field bundle]_. For instance the global nature of [[spinors]], hence _[[spin structures]]_ and their subtle effect on [[fermion]] physics are all enoced by the corresponding [[spinor bundles]]. 

Two aspects of bundles in physics come together in the theory of [[gauge fields]] and combine to produce [[fiber infinity-bundle|higher fiber bundles]]: namely we saw above that a [[gauge field]] is itself already a bundle (with a [[connection on a bundle|connection]]), and hence the bundle of which a gauge field is a section has to be a "second-order bundle". This is called _[[gerbe]]_ or _[[principal 2-bundle|2-bundle]]_: the only way to realize the [[Yang-Mills field]] both locally and globally accurately is to consider it as a section of a bundle whose typical fiber is $\mathbf{B}G$, the universal [[moduli stack]] of $G$-[[principal bundles]]. For more on this see on the nLab at _[The traditional idea of field bundles and its problems](field%20%28physics%29#IdeaOfFieldBundlesAndItsProblems)_.

All of this becomes even more pronounced as one digs deeper into _[[local quantum field theory]]_, with locality formalized as in the [[cobordism hypothesis|cobordism theorem]] that classifies local [[topological field theories]]. Then already the [[local Lagrangians]] and [[local action functionals]] themselves are [[principal infinity-connection|higher connections]] on higher bundles over the [[moduli infinity-stack|higher moduli stack]] of fields. For instance the fully local formulation of [[Chern-Simons theory]] exhibits the Chern-Simons [[action functional]]  --- with all its global [[gauge invariance]] correctly realized -- as a [[universal Chern-Simons circle 3-bundle]]. This is such that by [[transgression]] to lower [[codimension]] it reproduces all the global gauge structure of this field theory, such as in codimension 2 the _[[WZW gerbe]]_ (itself a fiber 2-bundle: the [[background gauge field|background]] [[B-field]] of the [[WZW model]]!), in codimension 1 the [[prequantum line bundle]] on the [[moduli space of connections]] whose sections in turn yield the [[Hitchin connection|Hitchin bundle]] of [[conformal blocks]] on the [[moduli space of Riemann surfaces]].

And so on and so forth. In short: all global structure in [[field theory]] is controled by [[fiber bundles]], and all the more the more the field theory is [[quantum field theory|quantum]] and [[gauge field theory|gauge]]. The only reason why this can be ignored to some extent is because field theory is a complex subject and maybe the majority of discussions about it concerns really only a small little perturbative local aspect of it. But this is not the reality. The [[QCD]] [[vacuum]] that we inhabit is filled with a sea of non-trivial bundles and the whole quantum structure of the laws of nature are bundle-theoretic at its very heart.
 
## Related concepts

* [[geometry of physics]]

* [[twisted smooth cohomology in string theory]]

* [[motivation for higher differential geometry]]

* [[higher category theory and physics]]

* [[motives in physics]]


## References

Expositions include

* Luciano Boi, _Geometrical and topological foundations of theoretical physics: From gauge theories to string program_, 2003 ([pdf](http://www.emis.de/journals/HOA/IJMMS/2004/33-361777.pdf))


category: motivation


[[!redirects fiber bundles and physics]]

  