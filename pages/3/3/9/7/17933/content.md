

The traditional story in the [[physics]] textbooks (copied endlessly from one textbook to the next, over generations) of [[SU(2)]]-[[instantons]] ([[BPST instantons]]) tends to fail to highlight some key global points, without which the whole construction really collapses. The following text means to explain the correct description (using the mathematics of [[Cech cohomology]] cocycles via the [[clutching construction]] on the [[one-point compactification]] of [[Minkowski spacetime]]) but presented and phrased such that the [[folklore]] physics story becomes fully visible -- including its crucial fix.

$\,$

**Instantons**

For $G$ any [[gauge group]] (a [[Lie group]]), a $G$-[[Yang-Mills instanton]] on some 4-dimensional [[spacetime]] (a [[pseudo-Riemannian manifold]]) $X$ is a $G$-[[principal bundle]] on $X$ (whose class is going to be the "instanton sector"), equipped with a $G$-[[principal connection]] $\nabla$ (this is the actual [[gauge field]]) such that this is [[self-dual Yang-Mills theory|self-dual]], in that its [[curvature form]] $F_\nabla$ satisfies $F_\nabla = \star F_{\nabla}$, where $\star$ denotes the [[Hodge star]] operator for the given [[Riemannian metric|metric]] (which represents the field of [[gravity]]).

A standard theorem says that there is precisely one self-dual [[principal connection]] $\nabla$ on every [[isomorphism class]] of $SU(2)$-[[principal bundles]]. Therefore classifying and counting instantons amounts to classifying and counting $G$-[[principal bundles]]. 

This is what makes instantons a "topological" structure in the parlance of physics, meaning that they do not depend on [[Riemannian metric]] information, after all. 

We now take the [[spacetime]] to be [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ and the [[gauge group]] to be the [[special unitary group]] $SU(2)$. This is the case of "[[BPST-instantons]]". Of course other choices are possible and may lead to richer situations, but this simple case is what the physics textbooks tend to focus on (not the least, of course, because these choices are relevant for [[phenomenology]] of the [[weak nuclear force]] as seen in accelerator experiments) and it already serves to highlight key points.
Since, as we just said, we may disregard all metric properties, this means now that we regard spacetime to be just the [[Cartesian space]] $\mathbb{R}^4$.

Or almost. At this point one needs to be careful with the [[boundary conditions]] in order to get the topology right.

$\,$

**Vanishing at infinity**

The physical [[energy]] condition on an instanton is that the [[field strength]] $F_\nabla$ vanishes "at infinity". Mathematically, a [[continuous function]] on a [[locally compact topological space|locally compact]] [[topological space]] $X$ _[[vanishing at infinity|vanishes at infinity]]_ precisely if it extends to the "[[one-point compactification]]" $X^+ \coloneqq X \cup \{\infty\}$ of $X$ -- where we literally adjoin the "point at infinity" "$\infty$" and glue it to $X$ by defining a suitable [[topological space|topology]] on $X \cup \{\infty\}$.


Hence we may formalize the boundary condition by saying that our $SU(2)$-[[principal connection]] actually exists on the [[one-point compactification]] of $\mathbb{R}^4$. This is the [[4-sphere]]

$$
  S^4
  \simeq
  \mathbb{R}^4 \cup \{\infty\}
  \,.
$$

It is this passage from $\mathbb{R}^4$ to $S^4$ which takes care of the subtleties that often tend to be glossed over.

With the boundary conditions "at infinity" taken care of this way, an $SU(2)$-instanton now is the [[isomorphism class]] of an $SU(2)$-[[principal bundle]]  on the [[4-sphere]] $S^4$.

$\,$

**Instanton number**

There is a [[classifying space]] for $SU(2)$-[[principal bundles]], denoted $B SU(2)$. This being a [[classifying space]] means that for $X$ any [[paracompact topological space]], we have that the [[isomorphism classes]] of $SU(2)$-[[principal bundles]] on $X$ are in [[bijection]] with [[homotopy classes]] of [[continuous functions]] from $X$ to $B SU(2)$.

$$
  \{X \to B SU(2)\}_{/homotopy}
  \;\simeq\;
  \{ SU(2)\text{-principal bundles}\}_{/\text{gauge transformations}}
  \,.
$$

Now for $X = S^4$, it follows that 

$$
   \{S^4 \to B SU(2)\}_{/homotopy} 
   \simeq
   \pi_4(B SU(2))
   \simeq
   \mathbb{Z}
$$
 
is the 4th [[homotopy group]] of the [[classifying space]] $B SU(2)$. 

This is an [[integer]], and so this integer labels [[isomorphism classes]] of instantons on $S^4$ (hence on $\mathbb{R}^4$). We see below that [[Chern-Weil theory]] identifies this number with the [[instanton number]].

But this counting of instantons works more generally, if we use a suitable counting function. First of all, there is a [[topological space]] whose _only_ non-trivial [[homotopy group]] is $\pi_4$, and such that this is the group of integers. This is the [[Eilenberg-MacLane space]] $K(\mathbb{Z},4)$:

$$
  \{S^4 \to K(\mathbb{Z},4)\}_{/homotopy}
  \simeq
  \mathbb{Z}
  \;\;\;\;\;
  \text{and}
  \;\;\;\;\;
  \{S^{d\neq 4} \to K(\mathbb{Z},4)\}_{/homotopy} 
  \simeq
  0
  \,.
$$

This space has the following remarkable property: [[homotopy classes]] of [[continuous functions]] into it compute [[ordinary cohomology]] with [[integer]] [[coefficients]]:

$$
  \left\{
    X \longrightarrow K(\mathbb{Z},4)
  \right\}_{/homotopy}
  \;\simeq\;
  H^4(X,\mathbb{Z})
  \,.
$$

Now there is a [[continuous function]]

$$
  c_2 \;\colon\; B SU(2) \longrightarrow K(\mathbb{Z},4)
$$

called the _universal [[second Chern class]]_. This hence sends $SU(2)$-[[principal bundles]], classified by some map

$$
  \chi  \;\colon\; X \longrightarrow B SU(2)
$$

to classes in degree-4 cohomology

$$
  c_2(\chi)
  \;\colon\;
  X \longrightarrow B SU(2) \overset{c_2}{\longrightarrow} K(\mathbb{Z},4)
  \,.
$$

This [[cohomology class]]

$$
  c_2(\chi) \in H^4(X,\mathbb{Z})
$$

is hence called the [[second Chern class]] of the $SU(2)$-[[principal bundle]].

This is one in a whole sequence of _[[characteristic classes]]_ which are carried by $SU(2)$-[[principal bundles]], the _[[Chern classes]]_.

But in the special case that the base space $X$ is 4-[[dimension|dimensional]], we have that only a single one of these classes may be non-trivial, namely the [[second Chern class]] $c_2$. Therefore this class completely characterizes $SU(2)$-[[principal bundles]] in 4d. 

In conclusion: _Where a [[BPST-instanton]] is manifested by an [[special unitary group|SU(2)]]-[[principal bundle]] on a 4-dimensional [[manifold]], the [[instanton number]] is the [[second Chern class]] of this bundle._

$\,$

**Constructing instantons from gauge transformations**


We may construct the bundles, that are classified this way, explicitly by using [[Cech cohomology]]. This says that we get such a bundle by


1. choosing an [[open cover]] $\{U_i \to X\}$ of $X$ (by "[[charts]]")


1. choosing [[transition functions]] $g_{i j} \colon U_i \cap U_j \to SU(2)$ on each double overlap of two charts

1. such that on triple overlaps the cocycle condition $g_{i j} \cdot g_{j k} = g_{i k}$ holds.

Now comes the major fact which makes this general theory look like the structures that appear in the physics books: the _[[clutching construction]]_.

Namely, for general $X$ one needs the charts $\{U_i \to X\}$ to form a [[good open cover]] in order to guarantee that all isomorphism classes of gauge bundles are captured by the construction via transition functions.

But the _[[clutching construction]]_ says that whenever $X$ happens to be a [[sphere]], then it is _sufficient_ to cover it by two [[hemispheres]] that overlap a little:

$$
  U_+ \coloneqq \text{upper hemisphere with a little rim}
$$

$$
  U_- \coloneqq \text{lower hemisphere with a little rim}
  \,.
$$

But since everything is topological now, it doesn't matter that these charts are literally _hemi_-spheres in the metric sense. In order to get the standard picture we instead make $U_+$ maximally large and take it to cover all of $S^4$ except the "north pole" (which is really the "point at infinity", due to the [[one-point compactification]] above), while we take $U_-$ to be a tiny [[open neighbourhood]] of that point, sitting there as a tiny ice cap around the north pole. So

$$
  U_+ \coloneqq S^4 - \{\text{point at infinity}\}
$$

$$
  U_- \coloneqq \text{tiny neighbourhood of the point at infinity}
  \,.
$$

Topologically this is [[homeomorphism|homeomorphic]] to the situation before, and hence just as good.

So now back to the general prescription of building [[principal bundles]] via [[Cech cohomology]], we are to choose transition functions on all overlaps of charts. But thanks to the [[clutching construction]], there is now just a single such overlap, namely

$$
  U_+ \cap U_- = \text{tiny annulus around the point at infinity}
  \,.
$$


Moreover, there is no non-trivial triple overlap, hence no cocycle condition that our transition function is to satisfy.

In conclusion, [[Cech cohomology]] and the [[clutching construction]] jointly now say that $SU(2)$-instantons are classified by maps

$$
  U_+ \cap U_- \longrightarrow SU(2)
$$

But notice here that the intersection of two hemi-4-spheres that overlap slightly is just a 3-sphere times a slight thickening:

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

This is where this "gauge transformation at infinity" in the physics textbooks really comes from. The key point here is that it is indeed gauge transforming, namely the restriction of our bundle to $U_+$ is gauge transformed to its restriction to the "neighbourhood of infinity" $U_-$. 

But, as topological spaces, $SU(2) \simeq S^3$ and so 

$$
  \{ U_+ \cap U_- \to SU(2) \}_{/homotopy}
  \simeq 
  \pi_3(S^3)
  \simeq
  \mathbb{Z}
  \,.
$$

This way we get the same classification from [[Cech cohomology]] that we got from [[classifying space]] theory, as it must be. But now we know how that [[second Chern class]] may be concretely embodied in the "gauge transformation at infinity".

$\,$

**Gauge fields vanishing at infinity**

Now we bring in connections. As discussed before, we may just as well consider any [[principal connection]]. In the [[Cech cohomology]] picture and still using the [[clutching construction]] this now means to choose

1. $\mathfrak{su}(2)$-valued 1-forms $A_{\pm}$ on $U_\pm$

1. such that on the tiny intersection of the two charts at infinity we have

   $$
     A_- = g A_* g^{-1} + g d g^{-1}
   $$

Now observe that in the given situation of using the [[clutching construction]] on a [[sphere]], we may always _choose_

$$
  A_- = 0
  \,.
$$ 

Because then the above just says that $A_+$ on $U_+$ becomes gauge trivial "at infinity", _by the given gauge transformation_ $g \colon S^3 \to SU(2)$ (the one whose winding number counts our instantons). 

(In the present case this is really simple; but also generally there is a [[partition of unity]]-argument to construct connections on any bundle in generalization of this simple situation, see [here](connection+on+a+bundle#ExistenceOfConnections).)

$\,$

**Counting instantons by integrating $tr(F_\nabla \wedge F_\nabla)$**

So far we have derived the physics picture of an instanton: An $SU(2)$-gauge field which becomes gauge trivial "at infinity", witnessed by a gauge transformation on the "annulus at infinity" $S^3 \to SU(2)$, whose winding number is the instanton number. But the key point is that we see that the little neighbourhood of infinity $U_-$ is part of the picture, and that is necessary now to understand the Chern 4-form.

Namely to every $\mathfrak{su}(2)$-valued 1-form $A$ we may assign the ordinary (abelian)[[differential 4-form]]


$$
  \langle F_A \wedge F_A\rangle
  \coloneqq
  tr(F_A \wedge F_A)
  \,,
$$


where $F_A$ is the [[curvature form]] of $A$.

Now a general fact of [[Chern-Weil theory]] is that the 4-form built this way from a single $A$ is always exact, a potential is given by the [[Chern-Simons form]] $CS(A)$:

$$
  d CS(A) = \langle F_A \wedge F_A\rangle
  \,.
$$

But beware that this is only true on _a single chart_. And just because our chart $U_+$ covers "everything except infinity", we must not forget that there is a second chart $U_-$, the "neighbourhood of infinity".

Namely the 4-form $\langle F_\nabla \wedge F_\nabla\rangle$ that is defined on the whole of the 4-sphere $S^4$, this 4-form is only _locally exact_ (as every closed 4-form is, by the [[Poincare lemma]]). Generally, we define it chart-wise by

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


This does indeed give a globally defined 4-form, no matter what the local connection forms $A_{\pm}$ are, as long as they satisfy the required condition that they are related by a [[gauge transformation]] on the overlap $U_+ \cap U_-$. Because the 4-form is gauge invariant.

So the 4-form thus defined

$$
  \langle F_{\nabla} \wedge F_{\nabla} \rangle
   \in
  \Omega^4_{cl}(S^4)
$$

has 


1. a potential 3-form $CS(A_+)$ when restricted to $U_+$;

1. a potential 3-form $CS(A_-)$ when restricted to $U_-$;

but it does not have a potential 3-form on all of $S^4$, unless the instanton number vanishes.


Put this way this should be very obvious now. But it is easy to get confused about this, due to the sheer convenience of the [[clutching construction]] used above: we actually were allowed to choose $A_- = 0$! 

This might make it superficially look like there is only a single local gauge potential $A_+$ around, and that the 4-form is locally exact. But this is not the case: there are two local gauge potentials on two different charts, and just because one of them happens to be equal to zero still does not mean that the extension of the 4-form to all of the 4-sphere has a global potential. It has a potential $CS(A_+)$ only after restricting it to $U_+$, even if this means "only removing the point at infinity".

With it thus being understood that $\langle F_\nabla \wedge F_\nabla\rangle$ is not globally exact, it becomes believable that the integral

$$
  \int_{S^4} \langle F_\nabla \wedge F_\nabla\rangle
  \;\in\;
  \mathbb{N}
$$

is generally non-vanishing, and is in fact yet another incarnation of the same integer that we had before, the instanton number. That this is so is given to us by [[Chern-Weil theory]].

$\,$

**Outlook: Chern-Simons 2-Gerbes**

In fact the full story is nicer still. Namely the local [[Chern-Simons 3-forms]] $CS(A_\pm)$ together with the gauge transformation at infinity form a [[Cech cohomology]] cocycle for a [[circle 3-bundle with connection]] (a [[bundle 2-gerbe]]). This is the [[Chern-Simons 2-gerbe]] of the gauge field. And the fourth incarnation of the instanton number is: the [[Dixmier-Douady class]] of this 2-gerbe