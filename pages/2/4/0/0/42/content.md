*[since odd graded differential 1-forms, being of total even degree, do not have a top exterior power]:I don't understand. What does this mean? (Bruce Bartlett)


#Idea#

There are different ways to define a differential volume element on a smooth manifold. Some of these definitions can be carried over to supergeometry, others cannot. The possibly most familiar way of talking about differential volume elements, in terms of top-degree differential forms, does _not_ carry over to supermanifolds.

###No top-degree forms in supergeometry###

In supergeometry the notion of _top-degree form_ does not in general make sense, since there are no top-degree wedge powers of "odd 1-forms": if for instance $\theta_1$ and $\theta_2$ are odd functions on some supermanifold and $d \theta_1$ and $d \theta_2$ are their differential 1-forms, then the wedge product of these is symmetric in that
$$
  d\theta_1 \wedge d \theta_2 = + 
  d\theta_2 \wedge d \theta_1
  \,.
$$


+-- {: .query}
_Question:_ Okay, but what is the _differential $d\theta_1$ of an odd co-ordinate function_? How are we to think of it geometrically? Does it measure a rate of change of something?
=--

####Differential forms on supermanifolds####

_Answer:_ In supergeometry the idea is to define everything in sight in terms of the algebras of local coordinate functions. (One really proceeds precisely as physicists do and always did, only difference being that before doing so one spends a minute to wonder about what doing so really means.) This means that the deRham complex of differential forms on a supermanifold is define in the obvious way:

let $C^\infty(U)$ be the algebra of functions on patch $U$ of your supermanifold. Then the corresponding deRham complex over $U$ is the [[L-infinity Lie algebroid|qDGCA]] which as a free graded-commutative algebra is generated over $C^\infty(X)$ by $C^\infty(U)[1]$. This means that for each element $f \in C^\infty(U)$ we add a new element denoted $d f \in C^\infty(U)[1]$ which we take to be "shifted in degree by 1" with respect to $f$. If we are just in the usual $\mathbb{Z}_2$-graded context of supermanifolds, this just means that $d f$ is of odd or even grade if $f$ is of even or odd grade, respective.

On the free graded-commutative algebra $\Omega^\bullet(U) := \wedge^\bullet_{C^\infty(U)} C^\infty(U) = S^\bullet_{C^\infty(U)} C^\infty(U)[1]$ obtained this way we naturally obtain an odd degree algebra derivation 
$$
  d : \Omega^\bullet(U) \to \Omega^\bullet(U)
$$
by taking it on generators $f \in C^\infty(U)$ to be given b
$$
  d : f \maspto d f
$, naturally, and extended that as an odd graded derivation to all of $\Omega^\bullet(U)$. This defines the qDGCA $(\Omega^\bullet(U), d)$. This construction glues on intersections of different patches $U_1$, $U_2$ and hence defines a qDGCA $(\Omega^\bullet(X),d)$, the **de Rham complex of the supermanifold $X$**.


Okay, back to the discussion of integration:

### Again: no top-degree forms in supergeometry###

In supergeometry the notion of _top-degree form_ does not in general make sense, since there are no top-degree wedge powers of "odd 1-forms": if for instance $\theta_1$ and $\theta_2$ are odd functions on some supermanifold and $d \theta_1$ and $d \theta_2$ are their differential 1-forms, then the wedge product of these is symmetric in that
$$
  d\theta_1 \wedge d \theta_2 = + 
  d\theta_2 \wedge d \theta_1
  \,.
$$


Notice the plus sign on the right.
You can think of this plus sign as being the product of one minus sign for interchanging $\theta_1$ and $\theta_2$, and another minus sign for interchanging the two differentials.

Accordingly, the wedge product of the differential of an odd function $\theta$ with itself does not in general vanish:
$$
  (d \theta \wedge d\theta = 0)
  \Leftrightarrow
  (\theta = 0)
  \,.
$$

On the cartesian supermanifold $\mathbb{R}^{n|m}$ with canonical even coordinate functions $\{x^i\}_1^n$ and canonical odd coordinate functions $\{\theta^j\}_1^m$ the differential form which one would want to regard as the canonical volume form is
$$
  \omega :=
  d x^1 \wedge \cdots \wedge dx^n \wedge 
  d\theta^1 \wedge \cdots \wedge d\theta^m
  \,.
$$
Due to the above, this is not a _top_ form, since for instance
$$
  \omega \wedge d\theta^1 \neq 0
  \,.
$$

But this example also indicates the solution: apparently for integration it is not really essential that a form is a top power, what is rather essential is that it is, locally, the wedge product of a _basis_ of 1-forms. This perspective then does lead to a sensible definition of volume forms (and more generally "integrable forms") on supermanifolds, described below.

###Solution: ###

Therefore the na&#239;ve identification of differential volume measures with top degree forms has to be refined. The idea is to characterize a volume form by other means, in particular as an equivalence class of choices of bases for the space of 1-forms, and then to define **integrable forms** to be pairs consisting of such a generalized volume form and a **multivector**: this pair is supposed to represent the differential form one would obtain could one contract the multivector with the volume form, as in ordinary differential geometry.

The definition of integration of integrable forms in supergeometry in terms of multivectorfields leads, in the case that the supermanifold in an [[NQ-supermanifold]] to the [[BV-theory|BV-formalism]].

#Details#

A summary of the standard lore is here: 

Urs Schreiber, [_Integration over supermanifolds_](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf)