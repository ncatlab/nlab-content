[[!redirects global model structure on simplicial sheaves]]
#Idea#


For $C$ a [[category]] regarded as an [[(infinity,1)-category]], a global [[model category|model structure]] on the [[functor category]] $[C^{op}, SSet]$ of
simplicial presheaves on $C$ is a [[presentable (infinity,1)-category|presentation]] for the [[(infinity,1)-category of (infinity,1)-presheaves]] on $C$.

See [[model structure on simplicial presheaves]].



#Definition#

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

#Remarks#

For $C$ a [[site]],
the [[Bousfield localization]] of these global model structures at morphisms that induce isomorphisms on all [[sheaf|sheaves]] of [[simplicial homotopy group]]s yields the [[local model structure on simplicial presheaves]].


#Properties#


* Both projective and injective model structures define [[simplicial model category|proper simplicial model categories]].

#References#

See also [[model structure on simplicial presheaves]].

The global projective model structure is originally due to

* A. K. Bousfield and D.M. Kan, _Homotopy limits completions and localizations_, Springer Lecture Notes in Math. 304 (2nd corrected printing), Springer-Verlag, Berlin--Heidelberg--New York (1987).

The fact that the global injective model structure yields a proper simplicial cofibrantly generated model category is originally due to 

* A. Heller, _Universal Homotopy Theories_ ([hopf](http://hopf.math.purdue.edu/pub/hopf.html))

The fact that the global projective structure yields a proper simplicial cellular model category is due to Hirschhorn-Bousfield-Kan-Quillen

* P. Hirschhorn, _Localizations of Model Categories_ ([web](http://www-math.mit.edu/~psh/))

A quick review of these facts is on the first few pages of

* Benjamin Blander, _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

