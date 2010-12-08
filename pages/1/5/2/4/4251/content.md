
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--





This is a sub-entry of [[homotopy groups in an (∞,1)-topos]].

For the other notion of homotopy grups in an $(\infty,1)$-topos see [[categorical homotopy groups in an (∞,1)-topos]].

#Contents#
* automatic table of contents goes here
{:toc}

## Idea {#GeomIdea}

An ordinary [[topos]] $E$ is a [[locally connected topos]] if the [[global section]]s [[geometric morphism]] $(LConst \dashv \Gamma) : E \stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}} Set$ is in fact an [[essential geometric morphism]] in that $LConst$ has also a [[left adjoint]] $(\Pi_0 \dashv LConst)$:

$$
  (\Pi_0 \dashv LConst \dashv \Gamma)
  :
  E
  \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
  \,.
$$

This left adjoint $\Pi_0$ sends each object $X$ of $A$ to its [[set]] $\Pi_0$ of connected components. In other words this left adjoint produces the degree 0-part of the homotopy groups of objects of $E$.

This has an obvious generalization of [[(∞,1)-topos]]es.


## Definition {#GeomDef}

The obvious generalization of the notion of $\Pi_0$ for a [[locally connected topos]] is to say that for $n \in \mathbb{N}$ an [[(n,1)-topos]] $\mathbf{H}$ is a [[locally n-connected (∞,1)-topos|locally n-connected (n,1)-topos]] if again the terminal geometric morphism is an essential geometric morphism in that the [[constant stack|constant n-stack]] functor $LConst$ has a [[left adjoint]] $\Pi_n$

$$
  (\Pi_n \dashv LConst \dashv \Gamma)
  :
  \mathbf{H}
  \stackrel{\overset{\Pi_n}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  n Grpd
  \,.
$$

Here we may take $n = \infty$ and say that an [[(∞,1)-topos]] is [[locally n-connected (∞,1)-topos|locally contractible]] if we have an [[essential geometric morphism]]

$$
  (\Pi \dashv LConst \dashv \Gamma)
  :
  \mathbf{H}
  \stackrel{\overset{\Pi}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  \infty Grpd
$$

to [[? Grpd]], with $\Pi$ the left [[adjoint (∞,1)-functor]] to the [[constant ∞-stack]] [[(∞,1)-functor]] $LConst$. For $X \in \mathbf{H}$ any object, the [[∞-groupoid]] $\Pi(X)$ deserves to be called the 
**[[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]** of $X$
Its ordinary [[homotopy group]]s are the homotopy groups of $X$.

While an obvious slight generalization or refinement of what is considered in previous literature, it seems that the simple picture of a left [[adjoint (∞,1)-functor]] to the [[constant ∞-stack]] functor has not been made explicit in the existing literature (though possibly in the thesis by [[Richard Williamson]]).

However, up to some straightforward translations of concepts and notation, it turns out that essentially all aspects of this picture are present and well known -- if somewhat implicitly -- in existing literature. A detailed commented account of what is in the literature is in the following subsection and in particular in the section [Examples](#GeomExamples) below.

There are essentially three different methods concretely constructing the abstractly defined  [[schreiber:homotopy ∞-groupoid]]-functor $\Pi(-)$.

1. by constructing the left adjoint $\Pi(-)$ as the functor 
   that takes an object to its **local contraction** 
   -- this is described in the 
   section _[In terms of local contractions](#LocalContraction);

1. by using **monodromy**/[[Galois theory]] of [[locally constant ∞-stack]]s to reproduce $\Pi()$ by [[Tannaka duality]] -- this is described in the section [In terms of monodromy and Galois theory](Monodromy);

1. by constructing $\Pi(-)$ explicitly as a path 
   $\infty$-groupoid in terms of paths modeled on 
   an [[interval object]] in $\mathbf{H}$ -- 
   this is described in the section 
   _[In terms of concrete paths](Paths)_ .


## In terms of local contractions {#LocalContraction}

If the [[locally contractible (∞,1)-topos]] $\mathbf{H}$ has a [[site]] $C$ with $\mathbf{H} \simeq Sh_{(\infty,1)}(C)$ such that the objects of the site are **geometrically contractible** in that _constant_ [[(∞,1)-presheaf|(∞,1)-presheaves]] already satisfy [[descent]] over objects in $C$, then the [[left adjoint]] $\Pi : \mathbf{H} \to \infty Grpd$ to $LConst$ may be constructed explicitly as follows.

Following the discussion at [[models for ∞-stack (∞,1)-toposes]] there is a [[model structure on simplicial presheaves]] $sPSh(C)_{proj}^{loc}$ wich [[presentable (∞,1)-category|presents]] $\mathbf{H}$. 

**Proposition** The [[adjoint (∞,1)-functor|(∞,1)-adjunction]] $(\Pi \dashv LConst) : Sh_{(\infty,1)}(C) \stackrel{\leftarrow}{\to} \infty Grpd$ is presented  by an [[SSet]]-[[enriched category theory|enriched]] [[Quillen adjunction]]

$$
  (\Pi \dashv LConst) : sPSh(C)_{proj}^{loc}
   \stackrel{\overset{\Pi}{\to}}{\overset{LConst}{\leftarrow}}
  sSet_{Quillen}
  \,,
$$

where 

* for $S \in sSet$ the presheaf $LConst_S$ sends all $U \mapsto S$, for all $U$;

* the functor $\Pi$ acts by $Pi(X) = \int^{U \in C} X = \lim_\to X$.

The total left [[derived functor]] of $\Pi$ first takes an object $X$ to a [[simplicial presheaf]] that is degreewise a [[coproduct]] of [[representable functor|representables]] and then _contracts_ all these representables to the [[terminal object]], regarding the resulting constant simplicial presheaf as a simplicial set:

$$
  \mathbb{L} \Pi : 
  X \mapsto
  Q X = \int^{[n] \in \Delta} \Delta[n] \cdot
   \left( \coprod_{i_n} U_i \right)
  \mapsto
  \Pi(Q X) = 
  \int^{[n] \in \Delta} \Delta[n] \cdot
   \left( \coprod_{i_n} * \right)
  \,.
$$

**Proof**

This is discussed at [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]] and [[cohesive (∞,1)-topos]].


### References {#LocalContractionRef}

Essentially the construction of $\mathbb{L} \Pi$ as above is an old construction in terms of -- somewhat implicitly -- the structure of a [[category of fibrant objects]] on [[simplicial object]]s in a [[topos]]:

the discussion on page 18 of

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995) .

which goes back to 

* Artin, Mazur, _Etale Homotopy_ Springer Lecture Notes in Mathematics 100, Berlin (1969)


goes as follows:

Let $E = Sh(C)$ be a [[locally connected topos]]

$$
  (\Pi_0 \dashv LConst) : Sh(C) \stackrel{\leftarrow}{\to} Set
$$

that here we think of as a [[petit topos|petit]] over-topos over a given object $X$ in some ambient [[gros topos]]. Accordingly we write $X = *$ for the [[terminal object]] in $Sh(C)$. 

Assume that $E$ has [[point of a topos|enough point]]. Then [[stalk]]wise [[Kan fibration|Kan-fibrant]] [[simplicial object]]s in $E$, i.e. [[stalk]]-wise Kan-fibrant simplicial sheaves on $C$ form a [[category of fibrant objects]]. In particular a fibrant simplicial object $Y \in [\Delta^{op}, Sh(C)]$ equipped with an acyclic fibration $Y \to X$ to the [[terminal object]] $X = *$ is a [[hypercover]] of $X$.

The definition of the [[∞-groupoid]] $\Pi(X)$ as defined in the above references (notice that only its homotopy groups are written down explicitly there, but it's immediate to equivalently write it as we do now) is

$$
  \Pi(X) =
  \lim_\to \Pi_0( Y_\bullet)
  \,,
$$

where 

* the [[colimit]] is taken over the category of acyclic fibrations/hypercovers $Y \to X$;

* the connected components functor $\Pi_0 : Sh(C) \to Set$ is applied degreewise to the simplicial sheaf $Y = (Y_\bullet)$ to produce a [[simplicial set]].

In Artin-Mazur it is discussed that this prescription does produce the right homotopy groups for $X$  a [[topological space]] if one assumes that this space is [[locally contractible space]].

If we therefore interpret this as saying that for the above prescription to yield the correct result we generally ought to assume that $Sh_{(\infty,1)}(C)$ is a [[locally contractible (∞,1)-topos]],  then this prescription can be seen to model implicitly the left Quillen functor $\Pi(-)$ that we described above:

In terms of the full [[model category]] structure on $sPSh(C)_{proj}^{loc}$ among all these hypercovers is one that is the cofibrant object

$$
  Y = Q X = \int^{[n] \in \Delta} \Delta[n] \cdot
  \left(
    \coprod_{i_n} U_i
  \right)
$$

mentioned above, consisting degreewise of coproducts of representables with $\Pi_0(U_i) = *$. For instance if $X$ admits a [[good open cover]], we can take $Y$ to be the [[Cech nerve]] of that good cover. (For more on this see [[∞-Lie groupoid]].) Due to the lifting property of cofibrant objects, any colimit over all hypercovers can be computed by evaluating just at that hypercover.

There the Artin-Mazur-Moerdijk-prescription yields

$$
  \Pi(Q X) = 
  \Pi_0((Q X)_\bullet)
  =
  \int^{[n] \in \Delta}
  \Delta[n] \cdot \Pi_0\left(
    \coprod_{i_n} U_{i_n}
  \right)
  =
  \int^{[n] \in \Delta}
  \Delta[n] \cdot \Pi_0\left(
    \coprod_{i_n} *
  \right)  
  \,.
$$

This is indeed the action of the left Quillen functor from above.

It is the [[nerve theorem]] that asserts that for $Y$ the [[Cech nerve]] of a [[good open cover]], this simplicial set is homotopy equivalent to the original [[paracompact space]].


A closely related, implicitly slightly more general statement is in on p. 25 of

* [[Daniel Dugger]], _[[DuggerUniv.pdf:file]]_  

which describes this construction for the case $\mathbf{H} = Sh_{(\infty,1)}(Diff)$ (the [[gros topos]] of $\infty$-stacks on [[Diff]]). 

With even more general sites allowed, but working only at the level of [[homotopy category|homotopy categories]] the left adjoint $\Pi$ and its construction is described in [Proposition 2.18](http://math.berkeley.edu/~teleman/math/simpson.pdf#page=5) of

  * [[Carlos Simpson]], [[Constantin Teleman]], _de Rham's theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

See also the discussion at [[locally contractible (∞,1)-topos]].



## In terms of monodromy and Galois theory {#Monodromy}

Given an [[(∞,1)-topos]] $\mathbf{H} = Sh_{(\infty,1)}(C)$ we define the [[∞-groupoid]] of [[locally constant ∞-stack]]s on an object $X \in \mathbf{H}$ to be

$$
  \infty CovBund(X) := \mathbf{H}(X, LConst_{Core(\infty Grpd)})
  \,,
$$

where $LConst_{Core(\infty Grpd)}$ is the [[constant ∞-stack]] on the [[core]] [[∞-groupoid]] of [[? Grpd]].

If $\mathbf{H}$ is a [[locally contractible (∞,1)-topos]] in that $LConst$ has the left [[adjoint (∞,1)-functor]] $\Pi(-)$, then by definition of adjunction we have the equivalence

$$
  \infty CovBund(X) \simeq Func(\Pi(X), \infty Grpd)
$$

with [[locally constant ∞-stack]]s/$\infty$-[[covering space]]s on the one hand and [[(∞,1)-functor]]s from $\Pi(X)$ to [[∞Grpd]] on the other.

Concrete realizations of this equivalence are discussed in the [Examples](GeomExamples)-section below. Here we describe how one may _[[reconstruction theorem|reconstruct]]_ in terms [[Tannaka duality]] $\Pi(X)$ from just knowing $\infty CovBund(X)$ 
in terms of the [[automorphism]] [[∞-group]] of a fiber functor 

$$
  F_x :  \infty CovBund(X) \to \infty Grpd
$$

from $\infty$-[[covering space|coverin bundle]]s/[[locally constant ∞-stack]]s over $X$ to [[∞-groupoid]].

-- these automorphism are called the **monodromy** of $X$.

We want to show that these automorphism [[∞-group]]s are the [[loop space object]]s of $\Pi(X)$, hence the geometric homotopy $\infty$-groups.

$$
  Aut (F_x) = \Omega^{geom}_x X =: \Omega_x \Pi(X)
  \,.
$$

This is the reconstruction of the geometric homotopy [[∞-group]]s of an [[∞-stack]] $X$ from its **monodromy** or **[[Galois theory]]**.


**Proof**

The underlying mechanism is just $(\infty,1)$-[[Tannaka duality]], i.e. essentially the [[(∞,1)-Yoneda lemma]] applied a few times in a row:

suppose we knew $\Pi(X)$, so that by adjunction we have

$$
  CovBund(X) \simeq \infty Func(\Pi(X), \infty Grpd)
  \,.
$$

Then for each point $x \in \Pi(X)$ given by a morphism $i : {*} \to \Pi(X)$ we get a fiber functor

$$
  F_x := \infty Func(i, \infty Grpd) : Func(\Pi(X), \infty Grpd)
  \to \infty Grpd
$$

which takes a [[local system]] $\rho : \Pi(X) \to \infty Grpd$ and evaluates it on $x$. By the [[(∞,1)-Yoneda lemma]] this means that $F_x$ is given by homming out of the local system $Y_{\Pi(X)^{op}} x$ [[representable functor|represented by]] $x$:

$$
  \infty Func(i, \infty Grpd)
  \simeq
  Hom_{PSh_{(\infty,1)}(\Pi(X)^{op})}(Y_{\Pi(X)^{op}}) x, -)
  \,.
$$

But this in turn means that $\infty Func(i,\infty Grpd) : \infty Func(\Pi(X),\infty Grod) \to \infty Grpd$ is itself a representable functor, in the [[(∞,1)-category of (∞,1)-presheaves]]  $PSh_{(\infty,1)}(PSh_{(\infty,1)}(\Pi(X)^{op})^{op})$:

$$
  \infty Func(i, \infty Grpd)
  \simeq
  Y_{(PSh_{(\infty,1)}(\Pi(X)^{op}))^{op}} Y_{\Pi(X)^{op}} x
  \,.
$$

This way we find, by applying the [[(∞,1)-Yoneda lemma]] two more times, that the automorphism [[∞-group]] of  the fiber functor is

$$
  \begin{aligned}
    Aut_{PSh_{(\infty,1)}((PSh_{(\infty,1)}(\Pi(X)^{op}))^{op})}
    \infty Func(i, \infty Grod)
    &
    =
    Aut_{PSh_{(\infty,1)}((PSh_{(\infty,1)}(\Pi(X)^{op}))^{op})}
    Y_{(PSh_{(\infty,1)}(\Pi(X)^{op}))^{op}} Y_{\Pi(X)^{op}} x
    \\
    & \simeq
    Aut_{(PSh_{(\infty,1)}(\Pi(X)^{op}))^{op}}
    Y_{\Pi(X)^{op}} x     
    \\
    & \simeq
    Aut_{\Pi(X)^{op}} x
    \\
    & \simeq \Omega_x \Pi(X)
    \\
    & =:
    \Omega_x^{geom} X
    \,.
  \end{aligned}
$$

Now, the same is of course true even if we don't have $\Pi(X)$ in hands yet, but only know the [[∞-groupoid]] $CovBund(X)$ of covering $\infty$-bundles / [[locally constant ∞-stack]]s in $X$: in terms of this we may reconstruct the automorphism [[∞-group]]s of $\Pi(X)$ as

$$
  Aut( CovBund(X) \stackrel{F_x}{\to} \infty Grpd )
  \simeq
  \Omega_x \Pi(X) =: \Omega^{geom}_x X
  \,.
$$


### References

The idea that geometric homotopy groups of generalized [[space]]s given by [[sheaf|sheaves]], [[stack]]s, [[∞-stack]]s is detected and definable by the behaviour of locally constant sheaves, stacks, $\infty$-stacks on these objects goes back to [[Grothendieck's Galois theory]] and the notion of [[fundamental group of a topos]]. The state of the art treatment of the Galois theory of coverings in a topos is in

* Marta Bunge, _Galois groupoids and covering morphisms in topos theory_,  Galois theory, Hopf algebras, and semiabelian categories,  131--161, Fields Inst. Commun., 43, Amer. Math. Soc., Providence, RI, 2004, [links](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.15.7071).

In [[Pursuing Stacks]] [[Alexander Grothendieck|Grothendieck]] talked about how this 1-categorical situation generalizes to [[∞-stack]]s. 

After _Pursuing Stacks_, apparently the first to publish a detailed formalization and proof of how the [[homotopy group]]s of a [[topological space]] $X$ may be recovered from the behaviour of [[locally constant ∞-stack]]s on $X$ was 

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

This has a followup construction in

* [[Bertrand Toen]] and [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ , Proceedings of the
Program Stacks, Intersection theory and Non-abelian Hodge Theory, MSRI, Berkeley, January-May 2002 ([arxiv:math/0212330](http://arxiv.org/abs/math/0212330)).


Very similar constructions and statement then appeared in 

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf)) 

* [[Mike Shulman]], _Parametrized spaces model locally constant homotopy sheaves_ ([arXiv:0706.2874](http://arxiv.org/abs/0706.2874))

and, building on that, in example 1.8 of

* [[Denis-Charles Cisinski]], _Locally constant functors_ , Math. Proc. Camb. Phil. Soc. , 147 ([pdf](http://www-math.univ-paris13.fr/~cisinski/lcmodcat3.pdf))


Notably the article by [[Pietro Polesello]] and [[Ingo Waschkies]] makes fully explicit the observation that _locally_ constant $n$-stacks are precisely the sections of the _constant_ $(n+1)$-stack on the $(n+1)$-groupoid $n Grpd$. This is a key observation for bringing the full power of the adjunction $(\Pi \dashv LConst)$ into the picture, as we do here.

It was pointed out to [[Urs Schreiber]] by [[Richard Williamson]] that these constructions should generalize from topological spaces to objects in any [[(∞,1)-topos]], maybe along the lines outlined above, and that this way suitable $(\infty,1)$-toposes $\mathbf{H}$ comes canonically equipped with a notion of [[schreiber:homotopy ∞-groupoid]] $\Pi(X)$ of every object $X \in \mathbf{H}$.


## In terms of concrete paths {#Paths}

...

### References

The following references discuss fundamental groupoids of an entire [[topos]] constructed from concrete [[interval object]]s. In the context of the above discussion these toposes are to be thought of as _[[petit topos|petit]]_ over-toposes over a given object in an ambient [[gros topos]], and as such are concerned with the fundamental groupoid of that object, in our sense.

The construction of the [[fundamental groupoid]] of a topos from [[interval object]]s is in 

* [[Ieke Moerdijk]], [[Gavin Wraith]], _Connected locally connected toposes are path-connected_ , Transactions of the AMS, volume 295, number 2, (1986)

The comparison of this construction with the one by monodromy/Galois theory is in 

* [[Marta Bunge]], [[Ieke Moerdijk]], _On the construction of the Grothendieck fundamental group of a topos by paths_ , J. Pure and Applied Algebra, 116 (1997)







## Examples {#GeomExamples}


### Geometric $\Pi_0$ of a sheaf on a locally connected topological space {#Pi0Ofsheafontopspace}

Here we discuss the 0-th geometric homotopy group $\Pi_0 : Sh(X) \to Set$ of objects in a [[Grothendieck topos|sheaf topos]] in terms of a [[left adjoint]] $\Pi_0$ of the [[constant sheaf]] functor. This is a special case of the more general situation discussed in [Pi0 of a general object in a locally connected topos](Pi0InLocConTop) below.



Let $X$ be a sufficiently nice [[topological space]]. 

+-- {: .un_proposition}
###### Observation

There is a triple of [[adjoint functor]]s

$$
  (\Pi_0 \dashv LConst \dashv \Gamma) \;\;\;
  :
  \;\;\; Sh(X) \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
$$

where 

* $(LConst \dashv \Gamma)$ is the usual [[global section]] [[geometric morphism]] with $LConst_S$ the [[constant sheaf]] of [[locally constant function]]s with values in $S \in Set$ and 

* $\Pi : Sh(X) \to Set$ is [[left adjoint]] to $LConst$ and sends each sheaf $A$ to the set of connected components of the corresponding [[etale space]] $p_A : Et(A) \to X$:

  $$
    \Pi_0(A) = \pi_0 Et(A)
    \,.
  $$

=--

+-- {: .proof}
###### Proof


The [[etale space]] of $LConst_S$ is $E(LConst_S) = X \times S$. By the relation of [[sheaves]] on $X$ with [[etale space]]s over $X$ we have

$$
  Hom_{Sh(X)}(A, LConst_S) 
  \simeq
  Hom_{Et/X}(E(A), X \times S)
$$

For $\gamma : I \to E(A)$ any continuous path in $E(A)$, and for $f : E(A) \to X \times S$ a morphism in $Et/X$, the image of $\gamma$ in $X \times I$ is fixed by, say, the image $f(\gamma(0)) = (p_A(\gamma_0),s)$ to be $f(\gamma) : t \mapsto (p_A(\gamma(t)),s)$. This means that the value of $f$ on any path component of $E(A)$ is uniquely fixed by its value on any point in that path component.

Choosing a basepoint in each path component therefore induces  bijection

$$
  \simeq Hom_{Set}(\pi_0(Et(A)), S) = Hom_{Set}(\Pi_0(A),S)
  \,.
$$


=--

### Geometric $\Pi_0$ of a general object in a locally connected topos {#Pi0InLocConTop}

More generally, if $E$ is a [[locally connected topos]] then the [[global section]]s [[geometric morphism]] $(LConst \dashv \Gamma) : E \stackrel{\leftarrow}{\to} Set$ has also a [[left adjoint]] $\Pi_0$ to $LConst$:

$$
  (\Pi_0 \dashv LConst \dashv \Gamma) :
  E \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\overset{\Gamma}{\to}}}
  Set
  \,.
$$

For instance page 17 of

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995)



### Geometric $\pi_1$ of objects in a 1-topos

The general idea is that of 

* [[Grothendieck's Galois theory]]. 

A discussion of of how this produces first homotopy groups of a 1-[[topos]] is at

* [[fundamental group of a topos]].

The general construction of the first geometric homotopy group of objects in a [[Grothendieck topos]] is for instance in section 8.4 of

* [[Peter Johnstone]], _Topos theory_ .


### Geometric $\Pi_2$ of a topological space

This case is discussed in 

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf)) 

We indicate briefly how the results stated in this article fit into the general abstract picture as indicated above:

The authors consider locally constant 1-stacks and 2-stacks on sites of open subsets of sufficiently nice [[topological space]]s.

Prop. 1.1.9 gives the [[adjunction]]

$$
  (LConst \dashv \Gamma) : Sh_{(2,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}} Grpd
$$

between forming constant stacks and taking global sections.

Then prop 1.2.5, 1.2.6, culminating in 
[theorem 1.2.9, p. 121](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=13) gives (somewhat implicitly) the other adjunction

$$
  (\Pi_1\dashv LConst) : Op(X) \hookrightarrow Sh_{(2,1)}(X) \stackrel{\overset{\Pi_1}{\to}}{\underset{LConst}{\leftarrow}} Grpd
$$

with the [[right adjoint]] to $LConst$ being the [[fundamental groupoid]] functor on representables. (Where we change a bit the perspective on the results as presented there, to amplify the pattern indicated above. For instance where the authors write $\Gamma(X,C_X)$ we think of this here equivalently as $Sh_{(2,1)}(X)(X,LConst(C))$, so that the theorem then gives the adjunction equivalence $\cdots \simeq Grpd(\Pi_1(X),C)$).

Then in essentially verbatim analogy, these results are lifted from stacks to 2-stacks in section 2, where now prop 2.2.2, 2.2.3, culminating in [theorem 2.2.5, p. 132](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=24) gives (somewhat implicitly) the adjunction

$$
  (\Pi_2\dashv LConst) : Op(X) \hookrightarrow Sh_{(3,1)}(X) \stackrel{\overset{\Pi_2}{\to}}{\underset{LConst}{\leftarrow}} Grpd
$$

now with the [[path n-groupoid|path 2-groupoid]] operation (locally) left adjoint to forming constant 2-stacks.




### Geometric $\Pi_\infty$ of a topological space {#ooStackOnTopSpace}


 Let $X$ be a sufficiently nice (I think this should be locally (relatively) contractible. -DR) ([[paracompact space|paracompact]]) [[topological space]]. The canonical map $X \to {*}$ induces the [[geometric morphism]]

$$
  Sh_{(\infty,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

where the [[right adjoint]] $\Gamma$ is taking [[global section]]s and the [[left adjoint]] is forming the [[constant ∞-stack]] on an $\infty$-groupoid $K$. If $K = Core (\infty Grpd)$ then $LConst_K$ is the [[constant ∞-stack]] of [[locally constant ∞-stack]]s and we write

$$
  LConst(X) := Sh_{(\infty,1)}(X, LConst_{\infty Grpd})= \Gamma LConst_{\infty Grpd}
$$

for the $\infty$-groupoid of locally constant $\infty$-stacks on $X$.

Write $ \Pi(X) := Sing X$ for the [[fundamental ∞-groupoid]] of $X$.

+-- {: .un_theorem}
###### Claim

There is an equivalence of $\infty$-groupoids

$$
  LConst(X) \simeq \infty Grpd(\Pi(X), \infty Grpd)
  \,.
$$

=--

> [[Urs Schreiber]]: I think this is proven in the literature, if maybe slightly implicitly so. I'll now go through the available references to discuss this.


After old ideas by [[Alexander Grothendieck]] from [[Pursuing Stacks]], it seems that the first explicit formalization and proof of this statement is given in 

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

In [theorem 2.13, p. 25](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0007/0007157v4.pdf#page=25) the author proves an equivalence of [[(∞,1)-categories]] (modeled there as [[Segal category|Segal categories]])

$$
  LConst(X) \simeq Fib(\Pi(X))
$$

of [[locally constant ∞-stack]]s on $X$ and [[Kan fibration]]s over the [[fundamental ∞-groupoid]] $\Pi(X) = Sing(X)$.

But Kan fibrations over a Kan complex such as $\Pi(X)$ are equivalently [[left fibration]]s (as discussed there) and by by the [[(∞,1)-Grothendieck construction]] these are equivalent to [[(∞,1)-functor]]s $\Pi(X) \to \infty Grpd$. So under the [[(∞,1)-Grothendieck construction]] To&#235;n's result does actually produce an equivalence

$$
  LConst(X) \simeq Func(\Pi(X), \infty Grpd)
  \,.
$$

In 

* [[Bertrand Toen]] and [[Gabriele Vezzosi]], _Segal topoi and stacks over Segal categories_ , Proceedings of the
Program Stacks, Intersection theory and Non-abelian Hodge Theory, MSRI, Berkeley, January-May 2002 ([arxiv:math/0212330](http://arxiv.org/abs/math/0212330)).

this is discussed in the context of [[Segal-topos]]es.

Very similar statements are discussed in

* [[Mike Shulman]], _Parametrized spaces model locally constant homotopy sheaves_ ([arXiv:0706.2874](http://arxiv.org/abs/0706.2874))

and, building on that, in example 1.8 of

* [[Denis-Charles Cisinski]], _Locally constant functors_ , Math. Proc. Camb. Phil. Soc. , 147 ([pdf](http://www-math.univ-paris13.fr/~cisinski/lcmodcat3.pdf))

A variant of this statement -- more general in one respect, less general in another -- appears in 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

as [theorem 7.1.0.1](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=545). 

There it is shown that for any $K \in \infty Grpd$ there is a bijection of homotopy sets of morphisms

$$
  \pi_0 Top(X, |K|) \simeq \pi_0(p_* p^* K)
  \,,
$$

where $(p^* \dashv p_*) : Sh_{(\infty,1)}(X) \to \infty Grpd$ is the geometric morphism we denoted $(LConst \dashv \Gamma)$ above. 

If we also rewrite the left using [[homotopy hypothesis|the equivalence]] of $Top$ with $sSet$, this reads

$$
  \pi_0 \infty Grpd(\Pi(X), K) \simeq \pi_0(\Gamma LConst_K)
  = \pi_0 Sh_{(\infty,1)}(X,LConst_K)
  \,, 
$$

For $K = Core(\infty Grpd)$ this is the $\pi_0$-[[decategorification]] of the above statement.


### Geometric $\Pi_\infty$ of the terminal object in a locally $\infty$-connected $(\infty,1)$-topos {#GeomPiOfTermObj}

The geometric $\Pi_\infty$ of the terminal object in a locally ∞-connected (∞,1)-topos can be called the [[fundamental ∞-groupoid of an (∞,1)-topos|fundamental ∞-groupoid]] of the topos.  It [[representable functor|represents]] the [[shape of an (∞,1)-topos|shape]] of the topos.

On page 18-19 of

* [[Ieke Moerdijk]], _Classifying Spaces and Classifying Topoi_ Lecture Notes in Mathematics 1616, Springer (1995)

is described the construction of $\Pi(X) \in \infty Grpd$ for $X$ the [[terminal object]] in $Sh_{(\infty,1)}(C)$ on an ordinary [[site]] $C$ with $\Pi(X)$ as described above in [Geometric fundamental oo-groupoid](PiConstruction).

This reviews in particular (slightly implicitly)

+-- {: .num_theorem}
###### Theorem

Let $X$ be a [[topological space]] that has a basis of contractible open subsets. Write $X$ also for $X$ regarded as the terminal object in $Sh_{(\infty,1)}(X)$. Then the image of $X$ under $\Pi : Sh_{(\infty,1)}(X) \to \infty Grpd$ has the same homtopy groups as $X$ regarded as an object in [[Top]]:

$$
  \pi_n \Pi(X) \simeq \pi_n(X)
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is a slight reformulation of the statement in

M. Artin, B. Mazur, _Etale homotopy_ , Springer lecture notes in mathematics 100, Berlin 1969


=--

Notice the local contractibility assumption. This is necessary in general for $\Pi(X)$ to make sense.





## Examples {#GeneralExamples}

Let $C =$ [[Diff]] and consider in $Sh_{(\infty,1)}(Diff)$ the two objects

* $S^1$, the $\infty$-stack represented by the standard circle in $Diff$;

* $\mathbf{B}\mathbb{Z}$ -- the $\infty$-stack constant on the [[delooping]] [[groupoid]] of the additive group $\mathbb{Z}$.

Then

* the _categorical_ homotopy groups of $S^1$ are all trivial

  $$
    \pi_n^{cat}(S^1) = {*}
  $$

* the _geometric_ homotopy groups of $S^1$ are the usual ones obtained from regarding $S^1$ as an object in [[Top]]:

  $$  
    \pi^{geom}_0(S^1) = *
  $$

  $$  
    \pi^{geom}_1(S^1) = \mathbb{Z}
  $$

  etc.

For $\mathbf{B}\mathbb{Z}$ it is the other way round:

* the _categorical_ homotopy groups of $\mathbf{B}\mathbb{Z}$ are 

  $$  
    \pi_n^{cat}(\mathbf{B}\mathbb{Z}) = 
    \left\{
      \array{
         \mathbb{Z} & | if\; n=1
         \\
         * & | otherwise
      }
    \right.
    \,.
  $$


[[!redirects geometric homotopy groups in an (infinity,1)-topos]]