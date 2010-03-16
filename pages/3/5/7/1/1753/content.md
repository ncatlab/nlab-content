
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contenta#
* automatic table of contents goes here
{:toc}

## Idea

The **global model structure on simplicial presheaves** $[C^{op}, sSet_{Quillen}]$ on a [[small category]] $C$ is the [[global model structure on functors]] on $C$ with values in $sSet_{Quillen}$, the standard [[model structure on simplicial sets]].

It [[presentable (∞,1)-category|presented]] the [[(∞,1)-category of (∞,1)-functors]] from $C^{op}$ to [[∞Grpd]], hence the [[(∞,1)-category of (∞,1)-presheaves]] on $C$.

The [[Bousfield localization|left Bousfield localizations]] of $[C^{op}, sSet]_{proj}$ are, up to [[Quillen equivalence]], precisely the [[combinatorial model category|combinatorial model categories]].

In particular, if $C$ carries the structure of a [[site]], then 

* the left Bousfield localization of $[C^{op}, sSet_{Quillen}]$ at [[Cech cover]]s is the [[Cech model structure on simplicial presheaves]];

* the left Bousfield localization at [[hypercover]]s is the [[local model structure on simplicial presheaves]].

These localizations present the [[topological localization]] and [[hypercompletion]] of the [[(∞,1)-topos]] of $(\infty,1)$-presheaves on $C$ to the corresponding [[(∞,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves|(∞,1)-sheaves]]/[[∞-stack]]s on $C$.


## Definition

In every global model structure on simplicial presheaves on $C$ the weak equivalences are _objectwise_ those with respect to the standard [[model structure on simplicial sets]].

So a morphism $f : A \to B $ in $[C^{op}, SSet]$ is a weak equivalence with respect to a global model structure precisely if for all $U \in Obj(C)$ the morphism

$$
  f(U) : A(U) \to B(U)
$$

is a weak equivalence of [[simplicial set]] (i.e. a morphism inducing isomorphisms of [[simplicial homotopy group]]s).


There are several choices for how to extend this notion of weak equivalences to an entire [[model category]] structure.
The two common extreme choices are

* the  **global projective** model structure has as **fibrations** the _objectwise_ fibrations of the standard [[model structure on simplicial sets]] (i.e. the [[Kan fibration]]s);

* the  **global injective** model structure has as **cofibrations** the _objectwise_ cofibrations with respect to the standard [[model structure on simplicial sets]] (i.e. the [[monomorphism]]s).

The other class of morphisms (cofibrations / fibrations) is in each case fixed by the correspinding [[weak factorization system|lifting property]].



## Properties


* Both projective and injective model structures define [[simplicial model category|proper simplicial model categories]].

## References

See also [[model structure on simplicial presheaves]].

The global projective model structure is originally due to

* A. K. Bousfield and D.M. Kan, _Homotopy limits completions and localizations_, Springer Lecture Notes in Math. 304 (2nd corrected printing), Springer-Verlag, Berlin--Heidelberg--New York (1987).

The fact that the global injective model structure yields a proper simplicial cofibrantly generated model category is originally due to 

* A. Heller, _Universal Homotopy Theories_ ([hopf](http://hopf.math.purdue.edu/pub/hopf.html))

The fact that the global projective structure yields a proper simplicial cellular model category is due to Hirschhorn-Bousfield-Kan-Quillen

* P. Hirschhorn, _Localizations of Model Categories_ ([web](http://www-math.mit.edu/~psh/))

A quick review of these facts is on the first few pages of

* Benjamin Blander, _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

Details on the _projective_ global model structure is in

* [[Daniel Dugger]], _[[Universal Homotopy Theories]]_

[[!redirects global model structure on simplicial sheaves]]
