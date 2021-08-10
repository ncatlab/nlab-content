

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _contact manifold_ is a [[smooth manifold]] $P$ of odd [[dimension]] $2n+1$ which is equipped with a [[differential form|differential 1-form]] $A$ that is non-degenerate in the sense that the [[wedge product]] $A \wedge (d_{dR} A)^{\wedge^n}$ does not vanish.

The special case of [[closed manifold|closed]] _regular_ contact manifolds $(P,A)$ are essentially equivalent to the total spaces of [[circle bundles]] $P \to X$ over an $2n$-dimensional manifold equipped with a [[connection on a bundle|connection]] such that $A$ is the corresponding [[Ehresmann connection]] 1-form on the total space ([BoothbyWang (1958)](#BoothbyWang)). 

If in this case the [[curvature]] 2-form $\omega$ on $X$ makes the base space $X$ into a [[symplectic manifold]], then $(P,A)$ is a corresponding [[prequantum circle bundle]] that provides a [[geometric prequantization]] of $(X,\omega)$. 

A [[diffeomorphism]] $f : P \to P$ of a contact manifold $(P,A)$ is called a _contactomorphism_ (in analogy with _[[symplectomorphism]]_) if it preserves the 1-form $A$ up to multiplication by a function. If $(P,A)$ is regular and hence a [[prequantum line bundle]] a contactomorphism that strictly preserves the connection 1-form is called a _[[quantomorphism]]_. The [[Lie algebra]] of the [[quantomorphism group]] is that of the [[Poisson algebra]] of the base symplectic manifold $(X,\omega)$. 

## Properties

### Darboux theorem

There is a [[Darboux theorem]] for contact structures, stating how they are locally equivalent to a standard contact structure (e.g. [Arnold 78, page 362](#Arnold78))

### Relation to $U(1)$-principal connections
+-- {: .num_theorem}
###### Theorem

If $X$ is a [[closed manifold|closed]] [[smooth manifold]], $P \to X$ a smooth [[circle bundle]] ($U(1)$-[[principal bundle]]) and $\omega \in \Omega^2(X)$ a [[differential 2-form]] representing its [[Chern class]] in [[de Rham cohomology]], then there is a corresponding [[Ehresmann connection]] 1-form $A \in \Omega^1(P)$ with [[curvature]] $\omega$ and such that

1. $A$ is a regular contact form on $P$;

1. the [[Reeb vector field]] of $A$ generates the given $U(1)$-[[action]] on $P$.

Moreover, every regular contact form $A$ on a closed manifold $P$ arises this way, up to rescaling by a constant.

=--

This is due to ([Boothby-Wang 58](#BoothbyWang)). The proof is recalled (and completed) in ([Geiges 08, theorem 7.2.4, 7.2.5](#Geiges)).


## History
 {#History}

> The following is taken from ([Lin](#Lin)).

Originating in [[Hamiltonian mechanics]] and [[geometric optics]], contact geometry caught geometers' attention much earlier. In 1953, [[Shiing-shen Chern]] showed that the structure group of a contact manifold $M^{2n+1}$ can be reduced to the [[unitary group]] $U(n)$ and therefore all
of its odd [[characteristic classes]] vanish. Since all the characteristic classes of a closed, orientable 3-manifold vanish, Chern in 1966 posed the questions of whether such a manifold always admits a contact structure and whether there are non-isomorphic contact structures on
one manifold.

One of the milestones in the study of contact geometry is [[Daniel Bennequin|Bennequin]]'s proof of the existence of exotic contact structures (i. e., contact structures not isomorphic to the standard one) on $\mathbb{R}^3$ ([Bennequin 83](#Bennequin83)). Bennequin recognized that the induced singular [[foliation]] on a [[surface]] [[embedding|embedded]] in a contact 3-manifold plays a crucial role for the classification of contact structures. This role was further explored in the work of Eliashberg, who distinguished two classes of contact structures in dimension 3, overtwisted and tight, and gave a homotopy classification for overtwisted contact structures on 3-manifolds ([Eliashberg 89](#Eliashberg89)). Eliashberg also proved that on $\mathbb{R}^3$ and $S^3$, the standard contact structure is the only tight contact structure.

## Related concepts

* [[Legendrean submanifold]]

* [[symplectic manifold]]

* [[symplectic field theory]]

* [[generalized contact geometry]]

* [[Sasakian manifold]]


## References

### General

Monographs and introductions include 

* [[Hansjörg Geiges]], _Contact geometry_, in F. J. E. Dillen and L. C. A. Verstraelen, (eds.), _Handbook of Differential Geometry vol. 2  North-Holland, Amsterdam (2006), pp. 315-382 ([arXiv:math/0307242](http://arxiv.org/abs/math/0307242))


* {#Geiges} [[Hansjörg Geiges]], _An Introduction to Contact Topology_, Cambridge Studies in Advanced Mathematics 109, Cambridge University Press, Cambridge, (2008) ([doi:10.1017/CBO9780511611438]( https://doi.org/10.1017/CBO9780511611438))
 

* {#Lin}Xiao-Song Lin, _An introduction to 3-dimensional contact geometry_ ([pdf](http://math.ucr.edu/~xl/contact.pdf))
  

* John Etnyre, _Introductory lectures on contact geometry_ Proc. Sympos. Pure Math.  71 (2003), 81-107.  ([pdf](http://people.math.gatech.edu/~etnyre/preprints/papers/contlect.pdf))

Discussion in terms of (a modification of) [[G-structures]]:

* Alfonso Giuseppe Tortorella, Luca Vitagliano & Ori Yudilevich, _Homogeneous G-structures_, Annali di Matematica (2020) ([doi:10.1007/s10231-020-00972-9](https://doi.org/10.1007/s10231-020-00972-9))
 


A [[higher differential geometry]]-generalization of contact geometry in line with [[multisymplectic geometry]]/[[n-plectic geometry]] is discussed in 

* Luca Vitagliano, _L-infinity Algebras From Multicontact Geometry_ ([arXiv.1311.2751](http://arxiv.org/abs/1311.2751))

* {#Arnold78} [[Vladimir Arnol'd]], _[[Mathematical methods of classical mechanics]]_, Graduate texts in Mathematics 60 (1978)
 

### Characterization

The observation that regular contact manifolds are prequantum circle bundles is due to

* {#BoothbyWang} W. M. Boothby and H. C. Wang, _On contact manifolds_, Ann. of Math. (2) 68 (1958) 721&#8211;734. ([jstor:10.2307/1970165](http://www.jstor.org/stable/10.2307/1970165))
 

A modern review of this is in ([Geiges, section 7.2](#Geiges)).

An analogous result for a weaker form of regularity is discussed in

* C. Thomas, _Almost regular contact manifolds_, J. Diff. Geom. 11 (1976) ([euclid:jdg/1214433722](http://projecteuclid.org/euclid.jdg/1214433722))

A characterization of $S^1$-invariant contact structures on [[circle bundles]] is in 

* {#DingGeiges} Fan Ding, [[Hansjörg Geiges]], _Contact structures on principal circle bundle_, Bull. London Math. Soc, ([arXiv:1107.4948](http://arxiv.org/abs/1107.4948))
 

For the special case of 2-dimensional base manifolds ($n = 1$) this was obtained before in 

* R. Lutz, _Structures de contact sur les fibr&#233;s principaux en cercles de dimension trois_, Ann. Inst. Fourier (Grenoble) 27 (1977) no. 3, 1&#8211;15.

See also

* John Bland, Tom Duchamp, _The Group of Contact Diffeomorphisms for Compact Contact Manifolds_ ([arXiv:1007.2036](http://arxiv.org/abs/1007.2036))

### Further 

* {#Bennequin83} [[Daniel Bennequin]], _Entrelacements et equations de Pfaff_, Ast&#233;rique, 107-108 (1983), 87-161. ([pdf](http://www.numdam.org/article/AST_1983__107-108__87_0.pdf))

* {#Eliashberg89} [[Yakov Eliashberg]], _Classification of overtwisted contact structures on 3-manifolds_, Invent. Math. 98 (1989), 623-637. ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.465.8237&rep=rep1&type=pdf))

* {#Eliashberg92} [[Yakov Eliashberg]], _Contact 3-manifolds twenty years since J Martinet’s work_, Ann. Inst. Fourier, 42 (1992), 165-192. ([pdf](http://www.numdam.org/item/10.5802/aif.1288.pdf))

* [[Hansjörg Geiges]], _Contact structures on 1-connected 5-manifolds_, Mathematika 38 (1991), 303-311; 

* [[Hansjörg Geiges]], _Contact structures on $(n-1)$-connected $(2n+1)$-manifolds_, Pacific J. Math. 161 (1993), 129-137; 

* [[Hansjörg Geiges]], _Constructions of contact manifolds_, Math. Proc. Cambridge Philos. Soc. 121 (1997), 455-464; 

* [[Hansjörg Geiges]], _Normal contact structures on 3-manifolds_,
T&#244;hoku Math. J. 49 (1997), 415-422. 

* [[Hansjörg Geiges]], J. Gonzalo, _Moduli of contact circles_, J. Reine Angew. Math. 551 (2002), 41-85; _Contact geometry and complex surfaces_, Invent. Math. 121 (1995), 147-209. 

[[!redirects contact manifolds]]

[[!redirects contactomorphism]]
[[!redirects contactomorphisms]]


[[!redirects contact structure]]
[[!redirects contact structures]]

[[!redirects regular contact manifold]]
[[!redirects regular contact manifolds]]


[[!redirects contact geometry]]
[[!redirects contact geometries]]


[[!redirects contactomorphism]]
[[!redirects contactomorphisms]]

[[!redirects contact form]]
[[!redirects contact forms]]
