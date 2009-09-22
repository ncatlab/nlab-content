<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
</div>

#Contents#
* tic
{:toc}


#Idea#

[[model category|Model structures]] on [[simplicial presheaf|simplicial presheaves]] are [[models for ∞-stack (∞,1)-toposes]].

Recall that

* a [[model category]] is a way to [[presentable (infinity,1)-category|present]] an [[(∞,1)-category]];

* in the context of [[(∞,1)-categories]] [[presheaf|presheaves]] on an $(\infty,1)$-category $C$ are given by [[(∞,1)-functors]] $C^{op} \to$ [[SSet]].

This suggests that the [[(∞,1)-category of (∞,1)-sheaves]] on some [[site]] $C$ can be 
[[presentable (infinity,1)-category|presented]]
by a [[model category]] structure on the ordinary
[[functor category]] 

$$
  [C^{op},SSet] \simeq [\Delta^{op}, PSh(C)]
$$ 

-- the category of [[simplicial presheaf|simplicial presheaves]] .

Various interrelated flavors of model structures on the category of simplicial presheaves on $C$ have been introduced and studied since the 1970s, originally by K. Brown and A. Jocal and then developed in detail by Jardine.

Notice that when regarded as a presentation of an [[(∞,1)-sheaf]], i.e. of an [[∞-stack]], a simplicial presheaf -- being an ordinary functor instead of a [[pseudofunctor]] -- corresponds to a [[rectified ∞-stack]]. It might therefore seem that a model given by simplicial presheaves is too restrictive to capture the full expected flexibility of a notion of [[∞-stack]].
But this is not so. 

In 

* [[Jacob Lurie]], [[Higher Topos Theory]]

a fully general definition of a [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-category of ∞-stacks]] is given it is shown -- proposition 6.5.2.1 --
that, indeed, the Brown--Joyal--Jardine model is a [[presentable (infinity,1)-category|presentation]] of that.

More precisely

* the [[global model structure on simplicial presheaves]] on a category is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-presheaves]];

* the [[Cech model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category of (∞,1)-sheaves]];

* the [[local model structure on simplicial presheaves]] on a [[site]] is a [[presentable (infinity,1)-category|presentation]] of the _hypercompletion_ of the [[(∞,1)-category of (∞,1)-sheaves]] (see the discussion at [[hypercover]]).

* the [[Bousfield localization]] of the global [[model category]] structure to the local one presents the corresponding [[localization of an (∞,1)-category]] from presheaves to sheaves, mimicking the corresponding statement for a [[category of sheaves]].

Originally K. Brown had considered in [[BrownAHT]] not a model structure on simplicial presheaves but

* a [[category of fibrant objects]] structure on locally Kan simplicial sheaves (see there for details)

and Joyal had originally considered a 

* [[local model structure on simplicial sheaves]].

Joyal's [[local model structure on simplicial sheaves]] is [[Quillen equivalence|Quillen equivalent]] to the injective [[local model structure on simplicial presheaves]]. 

By repackaging [[Kan complex]]es as [[simplicial groupoids]] one obtains a [[model structure on presheaves of simplicial groupoids]] which is also Quillen equivalent to the above.

If K. Brown's [[category of fibrant objects]] on locally Kan simplicial sheaves is restricted to globally Kan simplicial sheaves on a [[topos]] with [[point of a topos|enough point]] then it is the full subcategory on the fibrant objects in the projective [[local model structure on simplicial sheaves]].


But since in all cases the weak equivalences are the same (where they apply, for Brown's model if the topos has enough points), all these local [[homotopical category|homotopical categories]] define equivalent [[homotopy category|homotopy categories]].

By Lurie's result these are in each case in turn equivalent to the [[homotopy category of an (infinity,1)-category|homtopy category of]] the [[(∞,1)-topos]] of [[∞-stacks]]. So in particular they serve as a home for general [[cohomology]].


Various old results appear in a new light this way. For instance using the old result of [[BrownAHT]] on the way ordinary [[abelian sheaf cohomology]] is embedded in the [[homotopy theory]] of simplicial sheaves, one sees that the old right derived functor definition of [[abelian sheaf cohomology]] really computes the [[∞-stackification]] of a sheaf of [[chain complex]]es regarded under the [[Dold?Kan correspondence]] as a simplicial sheaf.


# Map #

It is the very point of [[model category]] structures on a given [[homotopical category]] that there may be several of them: each [[presentable (infinity,1)-category|presenting]] the same [[(∞,1)-category]] but also each suited for different computational purposes.

So it is good that there are many model structures on simplicial (pre)sheaves, as there are. The following diagram is a map for part of the territory:

$$
  \array{
     &&
       (\infty,1)Sh(C)
     &&&
       (\infty,1)PSh(C)
     &&&
       (\infty,1)Sh(C)
     \\
     && 
       \uparrow^{presentation}
     &&&
       \uparrow^{presentation}
     &&& 
       \uparrow^{presentation}
     \\
     SSh(C)^{l loc}_{inj} & 
     \stackrel{\stackrel{sheafification}{\leftarrow}}
       {\stackrel{embedding}{\to}}& 
     SPSh(C)^{l loc}_{inj} 
     &\stackrel{}{\leftarrow}|&
     SPSh(C)_{inj}
     &\stackrel{\stackrel{Id}{\leftarrow}}
       {\stackrel{Id}{\rightarrow}}&
     SPSh(C)_{proj}
     &\stackrel{}{\mapsto}&
     SPSh(C)_{proj}^{l loc}
     &
     \stackrel{\stackrel{sheafification}{\to}}
       {\stackrel{embedding}{\leftarrow}}& 
     SSh(C)_{proj}^{l loc}
     \\
     Joyal
     &\stackrel{Quillen equivalence}{\leftrightarrow}&
     Jardine
     &\stackrel{left Bousf. localization}{\leftarrow|}&
     Heller
     &\stackrel{Quillen equivalence}{\leftrightarrow}&
     Bousfield-Kan 
    &\stackrel{left Bousf. localization}{\mapsto}&
     Blander
     &\stackrel{Quillen equivalence}{\leftrightarrow}& 
     Brown-Gersten    
     \\
     \\
     &
     everything cofibrant;
     \\
     & fibrant = global injective fib...     
     \\
     \;\;\; 
     & ...satisfying descent
     &&&&&&&&
     cofibrant = global projective cofib;
     \\
     &&&&&&&&&
     fibrant = Kan valued and...    
     \\
     &&&&&&&&&
     \;\;\; 
     ...satisfying descent

  }
$$

Here 

* "inj" denotes the injective model structure: fibrations are objectwise fibrations

* "proj" denotes the projective model structure: fibrations are objectwise fibrations

* no "loc" subscript means global model structure: weak equivalences are the objectwise weak equivalences:

* "l loc" denotes **left** [[Bousfield localization]] at [[hypercovers]] (at [[stalk]]wise acyclic fibrations if the [[point of a topos|topos has enough points]])

The identity functor on the category $SPSh(C)$ of [[simplicial presheaves]] is a [[Quillen adjunction]] for the projective and injective [[global model structure on simplicial presheaves|global model structure]] and this is a [[Quillen equivalence]].

The [[local model structure on simplicial sheaves|local model structures on simplicial sheaves]] are just the restrictions of [[local model structure on simplicial presheaves|those on simplicial presheaves]]. 

These are related by a [[Quillen adjunction]] given by the usual [[geometric embedding]] of the [[category of sheaves]] as a full [[subcategory]] of that of presheaves -- with [[sheafification]] the [[left adjoint]] -- and this is also  [[Quillen equivalence]].

The characteristic of the _left_ Bousfield localizations is that for them the fibrant objects are those that satisfy
[[descent]]: see [[descent for simplicial presheaves]].

In either case 

* the global model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-presheaves]]

while

* the local model structures [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category of (∞,1)-sheaves]] (i.e. [[∞-stacks]]).


The following diagram collection [[model category|model categories]] that are [[presentable (infinity,1)-category|presentations]] for the [[(∞,1)-category of (∞,1)-sheaves]]. All indicated morphism pairs are [[Quillen equivalences]].

$$
  \array{
     PSh(X, SGrpd)
     &\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&
     Sh(X,SGrpd)
     &\stackrel{}{\leftrightarrow}&
     Sh(X, SSet)^{l loc}_{inj}
     &\stackrel{\stackrel{sheafification}{\leftarrow}}
        {\stackrel{embedding}{\to}}&
     PSh(X, SSet)^{l loc}_{inj}
     &\stackrel{\stackrel{Id}{\leftarrow}}
        {\stackrel{Id}{\to}}&
     PSh(X, SSet)^{l loc}_{proj}
     &\stackrel{\stackrel{embedding}{\leftarrow}}
       {\stackrel{sheafification}{\to}}&
     Sh(X, SSet)^{l loc}_{proj}
     \\
     \\
     Luo-Bubenik-Tim
     &&
     Joyal-Tierney
     &&
     Joyal
     &&
     Jardine
     &&
     Blander
     &&
     Brown-Gersten     
  }
$$

On the right this lists the model structures on simplicial (pre)sheaves, here displayed as (pre)sheaves with values in [[simplicial sets]], using $SPSh(C) \simeq PSh(C,SSet)$.

On the left we have the Joyal--Tierney and Luo--Bubenik--Tim [[model structures on presheaves of simplicial groupoids]].

(...have to check here the relation $Sh(X,SGrpd)\leftrightarrow PSh(X, SGrpd)$)

#References#

A nicely helpful introduction and survey is provided in the notes

* Dan Dugger, _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://math.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))

This in particular gives a detailed account on the relation and difference between the "Cech model structure" (section 3) which localizes (only) at Cech [[covers]], and the Jardine model structure (section 4), which localizes at all [[stalk]]wise weak equivalences ([[hypercovers]]). The latter is what in [[Higher Topos Theory|HTT]] is called the _hypercompletion_ .

The standard lecture notes are

* **Jardine07** J. Jardine, _Field Lectures: Simplicial presheaves_ ([pdf](http://www.math.uwo.ca/~jardine/papers/Fields-01.pdf))

based on

* **Jardine01** J. Jardine, _Stacks and the homotopy theory of simplicial sheaves_, Homology, homotopy and applications, vol. 3 (2), 2001, pp.361--384

and ...

See also

* Benjamin Blander, _Local projective model structures on simplicial presheaves_,  K-Theory, Volume 24, Number 3, November 2001 , pp. 283--301(19) ([journal](http://www.ingentaconnect.com/content/klu/kthe/2001/00000024/00000003/00384649?crawler=true))

A detailed study of [[descent]] for simplicial presheaves is given in

* **DHI04** Daniel Dugger, Sharon Hollander, Daniel C. Isaksen, _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/)) 

* **DI02** D. Dugger, D. Isaksen, _Weak equivalences of simplicial presheaves_ ([arXiv](http://arxiv.org/abs/math/0205025))

A survey of many of the model structures together with a treatment of the left local projective one is in

* Benjamin Blander, _Local projective model structure on simplicial presheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0462/combination2.pdf))

See also

* Daniel Isaksen, _Flasque model structure for simplicial presheaves_  ([web](http://www.math.uiuc.edu/K-theory/0679/), [pdf](http://www.math.uiuc.edu/K-theory/0679/flasque.pdf))

The characterization of the model category of simplicial presheaves as the canonical [[presentable (infinity,1)-category|presentation]] of the (hypercompletion of) the [[(∞,1)-category of (∞,1)-sheaves]] on a site is in

* [proposition 6.5.2.1](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=528) of 

  * [[Jacob Lurie]], [[Higher Topos Theory]]

Last not least, it is noteworthy that the idea of localizing simplicial sheaves at stalkwise weak equivalences is already described and applied in 

* Kenneth Brown, [[BrownAHT|Abstract Homotopy Theory and Generalized Sheaff cohomology]],

using instead of a full [[model category]] structure the more lightweight one of a Brown [[category of fibrant objects]].

[[Note on Formatting|?]]