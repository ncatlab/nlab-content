

The traditional story in the [[physics]] textbooks (copied endlessly from one textbook to the next, over generations) of $SU(2)$-[[instantons]] ([[BPTS instantons]]) tends to fail to highlight some key global points, without which the whole construction really collapses. The following text means to explain the correct description (using the mathmatics of [[Cech cohomology]] cocycles via [[clutching construction]] on [[one-point compactification]] of [[Minkowski spacetime]]) but presented and phrased such that the folklore physics story becomes fully visible -- including its crucial fix.

$\,$

The [[spacetime]] is [[Minkowski spacetime]] $\mathbb{R}^4$. The [[gauge group]] is the [[special unitary group]] $SU(2)$. 

For just classifying instantons we may disregard all metric properties and hence regard spacetime just as the [[Cartesian space]] $\mathbb{R}^4$.

An $SU(2)$-[[gauge field]] on any [[space]] $X$ is an $SU(2)$-[[principal connection]] on $X$, hence an $SU(2)$-[[principal bundle]] equipped with a [[connection on a bundle]] $\nabla$. 


The physical energy condition that the [[field strength]] vaishes at infinity we may formalize by saying that our $SU(2)$-[[principal connection]] actually exists on the [[one-point compactification]] of $\mathbb{R}^4$. This is the [[4-sphere]] $S^4$.

With the boundary conditions taken care of this way, an $SU(2)$-instanton now is the [[isomorphism class]] of an $SU(2)$-[[principal bundle]]  on the [[4-sphere]] and equipped with a [[self-dual Yang-Mills theory|self-dual connection]]. A standard theorem says that there is precisely one self-dual connection on every isomorphism class of $SU(2)$-[[principal bundles]], so we are left with classifying these. Moreover, [[Chern-Weil theory]] says that for any [[principal connection]] $\nabla$ on the bundle then the integral of the 4-form $\langle F_\nabla \wedge F_\nabla\rangle $ is independend of the choice of the connection.

There is a [[classifying space]] for $SU(2)$-[[principal bundles]], denoted $B SU(2)$. This being a classifying space means that for $X$ any [[paracompact topological space]], the isomorphism classes of $SU(2)$-[[principal bundles]] on $X$ are in [[bijection]] with [[homotopy classes]] of [[continuous functions]] from $X$ to $B SU(2)$.

$$
  \{X \to B SU(2)\}_{/homotopy}
  \;\simeq\;
  \{ SU(2)\text{-principal bundes}\}_{/\text{gauge tranformations}}
  \,.
$$

Now for $X = S^4$, then 

$$
   \{X \to B SU(2)\}_{/homotopy} 
   \simeq
   \pi_4(B SU(2))
   \simeq
   \mathbb{Z}
$$
 
is the 4th [[homotopy group]] of the [[classifying space]] $B SU(2)$, also called the [[second Chern class]]. This is an [[integer]], and so this integer labels [[isomorphism classes]] of instantons on $S^4$ (hence on $\mathbb{R}^4$). This is going to be the _[[instanton number]]_.

We may construct the bundles that are classified this way explicitly by using [[Cech cohomology]]. This says that we get such a bundle by


1. choosing an [[open cover]] $\{U_i \to X\}$ of $X$ (by "[[charts]]")


1. choosing transition functions $g_{i j} \colon U_i \cap U_j \to SU(2)$ on each double overlap of two charts

1. such that on triple overlaps the cocycle condition $g_{i j} = g_{j k} = g_{i k}$ holds.

Now comes the major fact which gives makes this general theory look like the structures that appear in the physics books: the _[[clutching construction]]_.

Namely, for general $X$ one needs the charts $\{U_i \to X\}$ to form a [[good open cover]] in order to guarantee that all isomorphism classes of gauge bundles are captured by the construction via transition fuctions.

But the _[[clutching construction]]_ says that whenever $X$ happens to be a [[sphere]], then it is _sufficient_ to cover it by two hemispheres that overlap a little:

$$
  U_+ \coloneqq \text{upper hemisphere with a little rim}
$$

$$
  U_- \coloneqq \text{lower hemisphere with a little rim}
  \,.
$$

But since everything is topological now, it doesn't matter that these charts are literally _hemi_-spheres in the metric sense. In ordet to get the standard picture we instead make $U_+$ maximally large and take it to cover all of $S^4$ except the "north pole" (which is really the "point at infinity", due to the [[one-point compactification]] above), while we take $U_-$ to be a tiny [[open neighbourhood]] of that point, sitting there as a tiny ice cap around the north pole. So

$$
  U_+ \coloneqq S^4 - \{\text{point at infinity}\}
$$

$$
  U_- \coloneqq \text{tiny neighbourhood of the point at infinity}
  \,.
$$

Topoligically this is [[homeomorphism|homeomorphic]] to the situation before, and hence just as good.

So now back to the general prescription of building [[principal bundles]] via [[Cech cohomology]], we are to choose transition functions on all overlaps of charts. But thanks to the [[clutching construction]], there is now just a single such overlap, namely

$$
  U_+ \cap U_- = \text{tiny annulus around the point at infinity}
  \,.
$$


Moreover there is no non-trivial triple overlap, hence no cocycle condition that our transition function it to satisfy.

In coclusion, [[Cech cohomology]] and the [[clutching construction]] jointly now say that $SU(2)$-instantons are classified by maps

$$
  U_+ \cap U_- \longrightarrow SU(2)
$$

But notice that that the intersection of two hemi-4-spheres that overlap slightly is just a 3-sphere times a slight thickening:

$$
  U_+ \cap U_-
  \simeq
  S^3 \times \{-\epsilon, \epsilon\}
  \,.
$$

Moreover, the thickening direction here is trivial, and so one finds that instantons are classified by homotopy classes of maps

$$
  g \;\colon\; S^3 \longrightarrow SU(2)
$$

This is where this "gauge transformation at infinity" in the physics textbooks really comes from. The key point here is that it is indeed gauge transforming, namely the restriction of our bundle to $U_+$ to its restriction to the "neighbourhood of infinity" $U_-$. 

But as topological spaces $SU(2) \simeq S^3$ and so 

$$
  \{ U_+ \cap U_- \to SU(2) \}_{/homotopy}
  \simeq 
  \pi_3(S^3)
  \simeq
  \mathbb{Z}
  \,.
$$

So we get the same classification from [[Cech cohomology]] that we got from [[classifying space]] theory, as it must be. But now we know how that [[second Chern class]] may be concretely embodied in that "gauge transformation at infinity".


Now we bring in connections. As discussed before, we may just as well consider any [[principal connection]]. In the [[Cech cohomology]] picture and still using the [[clutching construction]] this now means to choose

1. $\mathfrak{su}(2)$-valued 1-forms $A_{\pm}$ on $U_\pm$

1. such that on the tiny intersection of the two charts at infinity we have

   $$
     A_- = g A_* g^{-1} + g d g^{-1}
   $$

Now observe that in the given situation of using the [[clutching construction]] on a [[sphere]], then we may always _choose_

$$
  A_- = 0
  \,.
$$ 

Because then the above just says that $A_+$ on $U_+$ becomes gauge trivial "at infinity", _by the given gauge transformation_ $g \colon S^3 \to SU(2)$ (the one whose winding number counts our instantons). 

(In the present case this is really simple, but also generally there is a [[partition of unity]]-argument to construct connections on any bundle in generalizatin of this simple situation, see [here](connection+on+a+bundle#ExistenceOfConnections).)

So far we have derived the physics picture of an instanton: An $SU(2)$-gauge field which becomes gauge trivial "at infinity", witnessed by a gauge transformation on the "annulus at infinity" $S^3 \to SU(2)$ whose winding number is the instanton number. But the key point is that we see that the leittle neighbourhood of infinity $U_-$ is part of the picture, and that is necessary now to understand the Chern 4-form.

Namely to every $\mathfrak{su}(2)$-valued 1-form $A$ we may assign the ordinary (abelian) 4-form


$$
  \langle F_A \wedge F_A\rangle
  \coloneqq
  tr(F_A \wedge F_A)
  \,,
$$


where $F_A$ is the [[curvature form]] of $A$.

Now a general fact of [[Chern-Weil theory]] is that the 4-form build this way from a single $A$ is always exact, a potential is given by the [[Chern-Simons form]] $CS(A)$:

$$
  d CS(A) = \langle F_A \wedge F_A\rangle
  \,.
$$

But beware now this is only true on _a single chart_. And just because our chart $U_+$ covers "everything except infinity", we must not forget that there is a second chart $U_-$, the "neighbourhood of infinity".

Namely the 4-form $\langle F_\nabla \wedge F_\nabla\rangle$ that is defined on the whose of the 4-sphere $S^4$, this 4-form is only _locally exact_ (as every closed 4-form is, by the [[Poincare lemma]]). Generally, we define it chart-wise by

$$
  \langle F_{\nabla} \wedge F_\nabla \rangle |_{U_+}
   \coloneqq
  \langle F_{A_+} \wedge F_{A_+}\rangle
$$


and

$$
  \langle F_{\nabla} \wedge F_\nabla \rangle |_{U_-}
   \coloneqq
  \langle F_{A_-} \wedge F_{A_-}\rangle
  \,.
$$


This does indeed give a globally defined 4-form, no matter what the local connection forms $A_{\pm}$ are, as long as they satisfy the required condition that they are related by a gauge transformation on the overlap $U_+ \cap U_-$. Because the 4-form is gauge invariant.

So the 4-form thus defined

$$
  \langle F_{\nabla} \wedge F_{\nabla} \rangle
   \in
  \Omega^4_{cl}(S^4)
$$

has 


1. a potential 3-form $CS(A_+)$ when restricted to $U_+$;

1. a potential 3-form $CS(A_-)$ when restricted to $U_-$;

but it does not have a potential 3-form on all of $S^4$, unless the instaton number vanishes.


Put this way this should be very obvious now. But it is easy to get confused about this due to the sheer convenince of the [[clutching construction]] used above: we actually were allowed to choose $A_- = 0$! 

This might make it superficially look like there is only a single local gauge potential $A_+$ around, and that the 4-form is locally exact. But this is not the case: there are two local gauge potentials on two different charts, and just because one of them happens to be equal to zero still does not mean that the extension of the 4-form to all of the 4-sphere has a global potential. It has a potential $CS(A_+)$ only after restricting it to $U_+$, even if this means "only removing the point at infinity".

With thus understood that $\langle F_\nabla \wedge F_\nabla\rangle$ is not globally exact, it becomes believable that the integral

$$
  \int_{S^4} \langle F_\nabla \wedge F_\nabla\rangle
  \;\in\;
  \mathbb{N}
$$

is generally non-vanishing, and is in fact yet another incarnation of the same integer that we had before, the instanton number. That this is so is given to us by [[Chern-Weil theory]].

In fact the full story is nicer still. Namely the local [[Chern-Simons 3-forms]] $CS(A_\pm)$ together with the gauge transformation at infinity form a [[Cech cohomology]] cocycle for a [[circle 3-bundle with connection]] (a [[bundle 2-gerbe]]). This is the [[Chern-Simons 2-gerbe]] of the gauge field. And the fourth incarnation of the instanton number is: the [[Dixmier-Douady class]] of this 2-gerbe