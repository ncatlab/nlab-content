
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

An _inertia orbifold_ $\Lambda \mathcal{X}$ is (a particular representative of) the [[free loop space object]] of an [[orbifold]] $\mathcal{X}$ (or of a plain [[groupoid]] or [[smooth groupoid]]/[[differentiable stack|differentiable]] [[stack]] etc.): the ([[smooth groupoid|smooth]]) [[groupoid]] whose 

* [[objects]] are [[endomorphisms]] (necessarily [[automorphisms]]) in $\mathcal{X}$

\begin{tikzcd}
  {}
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "g"
  ]
  x
\end{tikzcd}

* [[morphisms]] are [[conjugations]] of such automorphisms $g$ by morphisms (necessarily: [[isomorphisms]]) $f$ in $\mathcal{X}$:

\begin{tikzcd}
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "g"
  ]
  x
  \ar[rr, "f"]
  &&
  y
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "f \circ g \circ f^{\mathrlap{-1}}"
  ]
\end{tikzcd}

In the special "[[global quotient orbifold|global]]" case where $\mathcal{X} \simeq X\sslash G$ is a [[quotient stack]] ([[action groupoid]]) of a [[group action]], then the points of the inertia orbifold $\Lambda (X \sslash G)$ are the "inert" actions, consisting of elements of [[stabilizer subgroups]] $Stab_G(x)$ (also "isotropy groups") for points $x$ in $X$ (compare also the terminology "inertia group" for [[stabilizer subgroups]] used in [[number theory]], e.g [here](https://en.wikipedia.org/wiki/Ramification_group#Decomposition_group_and_inertia_group)).


## Definition
 {#Definition}

### For bare groupoids

\begin{definition}\label{InertiaGroupoid}
**(inertia groupoid)** \linebreak
Given a [[groupoid]] $\mathcal{G} \coloneqq (\mathcal{G}_1 \rightrightarrows \mathcal{G}_0)$ ([[internal groupoid|internal to]] [[Sets]]) with 

* set of [[objects]] $\mathcal{G}_0$ 

* set of [[morphisms]] $\mathcal{G}_1$, 

one defines its __inertia groupoid__ $\Lambda \mathcal{G}$ as the groupoid whose 

* set of objects is the set of [[automorphisms]] in $\mathcal{G}$, i.e. the [[equalizer]] of the [[source]] and [[target]] maps $s,t \colon G_1\to G_0$:

  $$
    (\Lambda \mathcal{G})_0 
    \;\coloneqq\;
    \underset{x \in \mathcal{G}_0}{\coprod}
    Aut_{\mathcal{G}}(x)
  $$

* whose [[hom-set]] from $f \colon a \to a$ to $g\colon b \to b$ consists of the [[commutative squares]] with the same vertical maps of the form 

$$
  \array{
    a 
      &\stackrel{f}{\longrightarrow}& 
    a
    \\
    {}^{\mathllap{u}}
    \big\downarrow 
      && 
    \big\downarrow {}^{\mathrlap{u}}
    \\  
    b 
    &\stackrel{g}{\longrightarrow}& 
    b
  }
$$

i.e. of the morphisms $u \colon a\to b$ in $\mathcal{G}_1$ such that $u^{-1}\circ g\circ u = f$.
\end{definition}

\begin{proposition}
The inertia groupoid (Def. \ref{InertiaGroupoid}) is [[equivalence of categories|equivalent]] (in fact [[isomorphism|isomorphic]] as [[groupoid objects]]) to the [[functor groupoid]] 

$$
  \Lambda \mathcal{G}
  \;\simeq\;
  \big[
    \mathbf{B}\mathbb{Z}, \mathcal{G}
  \big]
  \,,
$$ 

where

$$
  \mathbf{B}\mathbb{Z}
  \;\coloneqq\;
  \big(
    \mathbb{Z} \rightrightarrows \ast
  \big)
$$

denotes the [[delooping groupoid]] of the additive group of [[integers]], i.e. the [[free construction|free]] groupoid on a single object with a single [[automorphism]].
\end{proposition}

\begin{proposition}
The inertia groupoid (Def. \ref{InertiaGroupoid}) is also [[equivalence of categories|equivalent]] to the [[free loop space object]] of $\mathcal{G}$ in the [[(2,1)-category]] of groupoids.

$$
  \Lambda \mathcal{G}
  \;\simeq\;
  \mathcal{L} \mathcal{G}
  \;\coloneqq\;
  \mathcal{G} \times^h_{\mathcal{G} \times \mathcal{G}} \mathcal{G}
  \,.
$$

\end{proposition}


### For internal groupoids

The same construction can be performed for [[groupoid objects]] [[internalization|internal]] to any [[finitely complete category]], or more generally whenever the relevant [[limits]] exist.  

### For orbifolds

If a ([[differentiable stack|differential]], [[topological stack|topological]] or [[algebraic stack|algebraic]]) stack (or, in particular, an [[orbifold]]) is represented by a groupoid, then the inertia groupoid of that groupoid represents its [[inertia stack]].  In particular, an [[orbifold]] corresponds to a [[Morita equivalence]] [[equivalence class|class]] of a proper [[étale groupoid]]. The inertia groupoid $\Lambda G$ of $G$ is the Morita equivalence class of the (proper &#233;tale) [[action groupoid]] for the [[conjugation action]] of $\mathcal{G}_1$ on the subspace $S\subset G_1$ of closed loops.  

\begin{remark}\label{DifferentNotionsOfLoopOrbifolds}
**(different notions of loop orbifolds)** \linebreak
For the case of [[orbifolds]], the [[cohesion]] of the loops leads to a distinction between various in-equivalent notions of "[[free loop spaces]]" of orbifolds:

Let:

* $\mathcal{X} \,\in\, SmoothGroupoids_\infty$ be an [[orbifold]], regarded as a [[smooth groupoid]], regarded as a [[differentiable stack]].

* $S^1 \,\in\, SmoothManifolds \hookrightarrow SmoothGroupoids_\infty$ be the [[circle]] with its standard [[cohesion|cohesive]] structure as a [[smooth manifold]], and hence as a [[differentiable stack]].

  Notice that the [[shape modality|shape]] of $S^1$ (in the [[cohesive (infinity,1)-topos|cohesive]]) [[(2,1)-topos]] of [[smooth ∞-groupoids]] is the [[delooping groupoid]] of the [[integers]], regarded as a [[discrete object|discrete]] smooth groupoid

  $$
    &#643;S^1
    \;\simeq\;
    \mathbf{B}\mathbb{Z}
    \;\;\;
    \in
    Groupoids
    \xrightarrow{ \; Disc\; }
    SmoothGroupoids
     \;
    \,.
  $$

* $[-,-]$ denote the [[mapping stack]]-construction.

Then we have:

1. The *cohesive [[free loop orbifold]]* of $\mathcal{X}$ is 

   $$
     \mathcal{L}\mathcal{X}
     \;=\;
     \big[ S^1, \, \mathcal{X} \big]
     \,.
   $$

1. The *inertia orbifold* of $\mathcal{X}$ is

   $$
     \Lambda \mathcal{X}
     \;\simeq\;    
     \big[ &#643;S^1, \, \mathcal{X} \big]
     \;\simeq\;
     \big[ \mathbf{B}\mathbb{Z}, \, \mathcal{X} \big]
     \;\simeq\;
     \mathcal{X} \times^h_{\mathcal{X} \times \mathcal{X}} \mathcal{X}
     \,,
   $$

   which is the actual [[free loop space object]] formed in [[smooth groupoids]].


The [[shape modality]]-[[unit of a monad|unit]] $\mathcal{A} \xrightarrow{ \eta_{\mathcal{A}}} &#643; \mathcal{A}$ induces a canonical comparison morphism between the two

$$
  \Lambda \mathcal{X}
  \;=\;
  \big[ &#643;S^1, \, \mathcal{X} \big]
    \xrightarrow{ \; [\eta_{S^1},\mathcal{X}]\; }
  \big[ S^1, \, \mathcal{X} \big]
  \;=\;
  \mathcal{L} \mathcal{X}
  \,.
$$

When $\mathcal{X} \simeq X \!\sslash\! G$ is a [[global quotient orbifold]] of a [[smooth manifold]] $X$ (for instance for a [[good orbifold]], but $X$ could more generally be a [[diffeological space]] for the present discussion), then this inclusion is the [[n-truncated object of an (infinity,1)-category|faithful inclusion]] of the *cohesively constant loops*, namely those that map to points in the naive quotient space of $\mathcal{X}$.
\end{remark}

\begin{remark}
For [[quantum field theory]] on orbifolds, or rather [[string theory]] on orbifolds, the inertia orbifold is related to so called _twisted sectors_ of the corresponding QFT.  (...)
\end{remark}


## Properties

### Skeleton for global quotient orbifolds
 {#SkeletonForGlobalQuotientOrbifolds}

\begin{proposition}\label{SkeletonOfInertiaOfProperGoodOrbifolds}
**([[skeleton]] of [[inertia orbifold]] for [[proper action|proper]] [[good orbifolds]])** \linebreak
  If $\mathcal{X} \,\simeq\, X \!\sslash\! G $ is a [[good orbifold]] presented as the [[global quotient orbifold]] of a [[smooth manifold]] with [[smooth function|smooth]] [[proper action|proper]] [[group action]] by a [[discrete group]] $G$, then its inertia orbifold is equivalent to the following [[disjoint union]] of [[global quotient orbifolds]]

$$
  \Lambda
  \big(
    X \!\sslash\! G
  \big)
  \;\simeq\;
  \underset{ [g] \in ConjCl(G) }{\coprod}
  X^g \!\sslash\! C_g
  \,,
$$

where

* $ConjCl(G) \coloneqq G /_{ad} G$ is the set of [[conjugacy classes]] of $G$;

* $X^g \coloneqq X^{\langle g\rangle}$ is the [[fixed locus]] of the action of (the [[cyclic group]] generated by) $g \in G$ (which is again a [[smooth manifold]] by the discussion [here](equivariant+differential+topology#FixedSubmanifolds));

* $C_g \subset G$ is the [[centralizer]] of $\{g\} \subset G$.

\end{proposition}



## Examples

### Intertia groupoid of a delooping groupoid

For $G$ a [[finite group]] (most of the following holds more generally for [[discrete groups]]), we discuss the inertia groupoid $\Lambda \mathbf{B}G$ of the [[delooping groupoid]] $\mathbf{B}G \,=\, (G \rightrightarrows \ast)$.

\begin{remark}\label{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}
**([[delooping groupoid]] and [[simplicial classifying space]] of [[finite group]])** \linebreak
The [[nerve]] of the [[delooping groupoid]] of a [[discrete group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial classifying space]] of $G$ (see [this Example](simplicial+classifying+space#SimplicialClassifyingSpaceOfAnOrdinaryGroup)): 
$$
  N
  \big(
    G \rightrightarrows \ast
  \big)
  \;\simeq\;
  \overline{W} G
  \;\;\;
  \in
  \;
  sSet
  \,.
$$
For notational brevity we will be referring to $\overline{W}G$ in the following, but it may be helpful to keep thinking of the nerve of the delooping groupoid. 
From that perspective, an [[n-simplex]] in $\overline{W}G$, which is an [[n-tuple]] of group elements, is suggestively denoted as a sequence of composable arrows:

$$
  \big(\overline{W}G\big)_{n}
  \;\;
    =
  \;\;
  \Big\{
    \bullet
    \xrightarrow{g_{n-1}}
    \bullet
    \xrightarrow{\;}
    \cdots
    \bullet
    \xrightarrow{\;}
    \bullet
    \xrightarrow{g_1}
    \bullet
    \xrightarrow{g_0}
    \bullet
    \;\big\vert\;
    g_i \in G
  \Big\}
  \,.
$$

\end{remark}


\begin{proposition}
The inertia groupoid $\Lambda \mathbf{B} G$ is [[isomorphism|isomorphic]] to the [[action groupoid]] of the [[adjoint action]] of $G$ on itself:
$$
  \Lambda \mathbf{B}G
  \;\simeq\;
  G_{ad} \sslash G
  \;=\;
  \left(
    G \times G
    \underoverset
      {Ad_{(-)}(-)}
      {pr_2}
      {\rightrightarrows}
      G
  \right)
$$
\end{proposition}
This follows by immediate inspection. For more discussion see at *[[free loop space of a classifying space]]* the section *[Examples -- For finite groups](free+loop+space+of+classifying+space#ExampleDiscreteGroups)*.


\begin{proposition}
The [[groupoid convolution algebra]] of the inertia groupoid of the [[delooping groupoid]] $\mathbf{B}G$ is the [[Drinfeld double]] of the [[group convolution algebra]] of $G$.
\end{proposition}



\begin{definition}\label{MinimalSimplicialCircle}
**([[minimal simplicial circle]])** \linebreak
  Write 
  $$
    S 
    \;\coloneqq\;
    \Delta[1]/\partial\Delta[1]
    \;\;\;
    \in
    \;
    sSet
  $$
  for the [[simplicial set]] with exactly two non-degenerate cells, 

* one of which in degree 0, which we denote by $[0] = [1]$,

* and one in degree 1, which we denote by $\big[ [0], [1] \big]$.

\end{definition}

The following proposition follows on abstract grounds, but the explicit component-based proof we give is necessary in order to understand the [[transgression]]-formula for [[cocycles]] in the [[group cohomology]] of $G$ to cocycles on the inertia groupoid.
\begin{proposition}\label{RelationToSimplicialHomComplexIntoClassifyingSpace}
The [[nerve]] of the inertia groupoid of a delooping groupoid of a [[finite group]] $G$ is [[isomorphism|isomorphic]] to the [[simplicial hom complex]] out of the minimal simplicial circle $S$ (Def. \ref{MinimalSimplicialCircle}) into the [[simplicial classifying space]] $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}):

$$
  N\big( \Lambda \mathbf{B}G\big)_\bullet
  \;\simeq\;
  [S,\overline{W}G]_\bullet
  \,.
$$
\end{proposition}
\begin{proof}
We claim that the isomorphism is given by sending, for each $n \in \mathbb{N}$, any [[n-simplex]] $(\gamma, g_{n-1}, \cdots, g_1, g_0)$ of $N\big( Func( \mathbf{B}\mathbb{Z}, \, \mathbf{B}G )\big)$, being a sequence of [[natural transformations]] of the form
$$
  \array{
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j-1}}&
    \bullet
    &\xrightarrow{g_{n-j-2}}&
    \bullet
    &\xrightarrow{g_{n-j-3}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
    \\
    \big\downarrow
    {}^{\mathrlap{  
      \gamma 
    }}
    && 
    \big\downarrow
    {}^{\mathrlap{  
      g_{n-1}^{-1} \cdot \gamma \cdot g_{n-1}
    }}
    && 
    && 
    \big\downarrow
    &&
    \big\downarrow
    && &&
    \big\downarrow 
    {}^{\mathrlap{  
      ( g_{n-1} \cdots g_{0} )^{-1} 
      \cdot
      \gamma 
      \cdot
      ( g_{n-1} \cdots g_{0} )
    }}
    \\
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j-1}}&
    \bullet
    &\xrightarrow{g_{n-j-2}}&
    \bullet
    &\xrightarrow{g_{n-j-3}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
    \mathrlap{\,,}
  }
$$


to the homomorphism of simplicial sets

$$
  \Delta[n] \times S \xrightarrow{\;\;} \overline{W}G
  \,,
$$

which, in turn, sends a non-degenerate $(n+1)$-simplex in $\Delta[n] \times S$ of the form (in the path notation discussed at *[[product of simplices]]*)

$$
  \array{
    (0,[0])
    &\to&
    (1,[0])
    &\to&
    \cdots
    &\to&
    (j,[0])
    \\
    && && && \big\downarrow
    \\
    && && && 
    (j,[1])
    &\to&
    (j+1,[1])
    &\to&
    \cdots
    &\to&
    (n,[1])
  }
$$

to the $n+1$-simplex in $\overline{W}G$ (Rem. \ref{DeloopingGroupoidAndSimplicialClassifyingSpaceOfFiniteGroup}) of the form
 
$$
  \array{
    \bullet
    &\xrightarrow{g_{n-1}}&
    \bullet
    &\xrightarrow{g_{n-2}}&
    \cdots
    &\xrightarrow{g_{n-j}}&
    \bullet
    \\
    && && && 
    \big\downarrow 
    {}^{\mathrlap{  
      ( g_{n-1} \cdots g_{n-j} )^{-1} 
      \cdot
      \gamma 
      \cdot
      ( g_{n-1} \cdots g_{n-j} )
    }}
    \\
    && && && 
    \bullet
    &\xrightarrow{g_{n-j}}&
    \bullet
    &\xrightarrow{g_{n-j-1}}&
    \cdots
    &\xrightarrow{g_{0}}&
    \bullet
  }
$$

\end{proof}


{#FormOfTheSimplicialEvaluationMap} As a consequence, the [[evaluation map]] on the inertia groupoid has essentially this same expression, too, which explains the traditional formula for [[transgression in group cohomology]] (see the details [there](transgression+in+group+cohomology#FormOfTheSimplicialEvaluationMap)).




## Related concepts

* [[free loop orbifold]]

* [[Huan's inertia orbifold]]

* [[free loop space]], [[derived loop space]]

* [[transgression in group cohomology]]


## References

Original articles:

* Tetsuro Kawasaki, _The signature theorem for V-manifolds_, Topology __17__ (1978), no. 1, 75&#8211;83 (<a href="https://doi.org/10.1016/0040-9383(78)90013-7">doi:10.1016/0040-9383(78)90013-7</a>)

Review and further development:

* [[Ernesto Lupercio]], [[Bernardo Uribe]], Section 4 of: _Inertia orbifolds, configuration spaces and the ghost loop space_, Quarterly Journal of Mathematics __55__ 2 (2004) 185-201 &lbrack;[arxiv:math.AT/0210222](http://arxiv.org/abs/math/0210222), [doi:10.1093/qmath/hag053](https://doi.org/10.1093/qmath/hag053)&rbrack;

* {#Moerdijk02} [[Ieke Moerdijk]], Section 6 in: _Orbifolds as Groupoids: an Introduction_, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

* [[Ulrich Bunke]], [[Markus Spitzweck]], [[Thomas Schick]], _Inertia and delocalized twisted cohomology_, Homotopy, Homology and Applications 10(1) 129--180 (2008)[math.KT/0609576](https://arxiv.org/abs/math/0609576)  	
[doi](https://doi.org/10.4310/HHA.2008.v10.n1.a6)

See also:

* [[The Stacks Project]], *[The inertia stack](https://stacks.math.columbia.edu/tag/036X)* ([more](https://stacks.math.columbia.edu/tag/034H), [more](https://stacks.math.columbia.edu/tag/034I))

In relation to [[Drinfeld doubles]]:

* [[Vladimir Hinich]], _Drinfeld double for orbifolds_, Contemporary Math. __433__, AMS Providence, 2007, 251-265,
[arXiv:math.QA/0511476](http://arxiv.org/abs/math/0511476)

In view of the [[Chern character]] for [[twisted K-theory|twisted]] [[orbifold K-theory]]:

* [[Jean-Louis Tu]], [[Ping Xu]], _Chern character for twisted K-theory of orbifolds_, Advances in Mathematics __207__ (2006) 455&#8211;483, [pdf](http://www.math.univ-metz.fr/~tu/publi/orb.pdf) (cf. sec. 2.3)

See also the references at *[[free loop orbifold]]*.

On [[transgression in group cohomology]], for [[discrete groups]], to [[groupoid cohomology]] of [[inertia groupoids]]:

* {#Willerton08} [[Simon Willerton]], Section 1 of: *The twisted Drinfeld double of a finite group via gerbes and finite groupoids*, Algebr. Geom. Topol. 8 (2008) 1419-1457 ([arXiv:math/0503266](https://arxiv.org/abs/math/0503266))

* [[Jean-Louis Tu]], [[Ping Xu]], Section 3 of: *The ring structure for equivariant twisted K-theory*, J. Reine Angew. Math. 635 (2009), 97–148 ([arXiv:math/0604160](https://arxiv.org/abs/math/0604160), [doi:10.1515/CRELLE.2009.077](https://doi.org/10.1515/CRELLE.2009.077))

* [[Alejandro Adem]], [[Yongbin Ruan]], [[Bin Zhang]], Section 4 of: _A Stringy Product on Twisted Orbifold K-theory_, Morfismos (10th Anniversary Issue), Vol. 11, No 2 (2007), 33-64.  ([arXiv:math/0605534](https://arxiv.org/abs/math/0605534), [Morfismos pdf](www.morfismos.cinvestav.mx/Portals/morfismos/SiteDocs/Articulos/Volumen11/No2/Zhang/arz.pdf))

[[!redirects inertia orbifolds]]

[[!redirects inertia stack]]
[[!redirects inertia stacks]]

[[!redirects inertia ∞-stack]]
[[!redirects inertia ∞-stacks]]

[[!redirects inertia groupoid]]
[[!redirects inertia groupoids]]



category: Lie theory
