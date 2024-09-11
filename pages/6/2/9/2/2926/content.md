
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## On Lie groups

### Idea 

For $G$ a [[Lie group]], the _Maurer-Cartan form_ on $G$ is a canonical [[Lie-algebra valued 1-form]] on $G$. One can generalize also to the Maurer-Cartan form on a principal bundle. 

### Definition in synthetic differential geometry

Speaking in terms of [[synthetic differential geometry]] the Maurer-Cartan form has the following definition:

any two points $x,y \in G$ are related by a unique group element $\theta(x,y)$ such that $y = x \cdot \theta(x,y)$. If $x$ and $y$ are [[infinitesimal space|infinitesimally close]] points, defining a [[tangent vector]], then $\theta(x,y)$ is an element of the [[Lie algebra]] of $G$. So $\theta$ restricted to infinitesimally close points is a $\mathfrak{g}$-valued 1-form, and this is the Maurer-Cartan form.

### Analytic definition

In terms of [[analysis]] there is a direct analogue of this definition: a [[tangent vector]] on $G$ at $g \in G$ may be identified with an equivalence class of [[smooth function]] $\gamma : [0,1] \to G$ with $\gamma(0) = g$. The tangent vectors through the origin $x = e$ are canonically identified with the [[Lie algebra]] of $G$. By left-translating a path through $g$ back to the origin $g^{-1}\gamma : [0,1] \to G \stackrel{g^{-1} \cdot(-)}{\to} G$ it represents a Lie algebra element. This map 

$$
  \theta := g^{-1}_* : [\gamma] \mapsto [g^{-1} \gamma]
$$ 

of tangent vectors to Lie algebra elements is the Maurer-Cartan form.

If we write $g : G \to G$ for the identity function on $G$, then $d g : T G \to T G$ is the identity function on the tangent vectors of $G$.  With this the Maurer-Cartan form may be written

$$
  g^{-1}_* d g : T G \to T_e G = \mathfrak{g}
  \,.
$$



If $G$ is a [[matrix Lie group]], then $g^{-1}_*$ is literally just left-multiplication of matrices and therefore the Maurer-Cartan form is often written just 

$$
  \theta = g^{-1} d g
  \,.
$$



## Properties

### Curvature

The Maurer-Cartan form is a Lie-algebra valued form with vanishing [[curvature]].

$$
  d \theta + \frac{1}{2}[\theta \wedge \theta] = 0
$$

This is known as the [[Maurer-Cartan equation]].

Synthetically this is just a restatement of the fact that for $x,y \in G$ there is a _unique_ group element such that $y = x \cdot g$: therefore for three points $x,y,z$ we have

$$
  \array{
    && y
    \\
    & {}^{\mathllap{\theta}(x,y)}\nearrow && \searrow^{\mathrlap{\theta}(y,z)}
    \\
    x &&\stackrel{\theta(x,z)}{\to}&& z
  }
$$

i.e. $\theta(x,y) \theta(y,z) = \theta(x,z)$. This is what analytically becomes the statement of vanishing curvature.


### Pullback

If $X$ is a [[smooth manifold]] and $h : X \to G$ a [[smooth function]] with values in $G$, we have the [[pullback form]] 

$$
  h^* \theta \in \Omega^1(X,\mathfrak{g})
$$

of the Maurer-Cartan form on $X$. Using the above notation, writing simply $h^{-1}$ for $h^{-1}_*$ this is 

$$
  h^* \theta = h^{-1} d h
 \,.
$$

Now $d h : T X \to T G$ is no longer (necessarily) the identity map as $g$ was when we wrote $\theta = g^{-1} d g$ above, but the form of this equation shows why it can be useful to think of $\theta$ itself in terms of the identity map $d g : T G \to T G$.

### Gauge transformations

The Maurer-Cartan form crucially appears in the formula for the gauge transformation of [[Lie-algebra valued 1-form]]s.

For $u : \mathbb{R} \to G$ a smooth function and $A \in \Omega^1(\mathbb{R}, \mathfrak{g})$ a Lie-algebra valued form, the condition that $u$ is _flat_ with respect to $A$ is that it satisfies the [[differential equation]]

$$
  d u = -(R_u)_* \circ A
$$

(where $R$ denotes the right multiplication action of $G$ on itself). This is such that if $G$ happens to be a [[matrix Lie group]] it is equivalent to

$$
  (d + A) u = 0
  \,.
$$

We call the unique solution $u $ of this differential equation that satisfies $u(0) = e$ the [[parallel transport]] of $A$ and write it $u = P \exp\big(\int_0^{(-)} A\big)$.

Now for $g \colon \mathbb{R} \to G$ a function, the _gauge transformed_ parallel transport is

$$
  g^{-1} P \exp(\int_0^{(-)} A) g
  \,.
$$

This solves a differential equation as above, but for a different 1-form $A'$. The relation is 

$$
  A' = Ad_{g^{-1}} A + g^* \theta
$$

or equivalently, with adopted notation

$$
  A' = g^{-1}A g + g^{-1} d g
  \,.
$$

### In coordinates under the exponential map
 {#InCoordinatesUnderExponentialMap}

Any choice of [[linear basis]] $\mathfrak{g} \;\simeq\; \mathbb{R}\big\langle (T_i)_{i \in I} \big\rangle$ for the [[Lie algebra]] $\mathfrak{g}$ of the given [[Lie group]] $G$ induces linear [[coordinate functions]] $(x^i)_{i \in I}$ on the [[Cartesian space]] [[underlying]] $\mathfrak{g}$, with points parameterized as
$$
  x^i T_i \,\in\, \mathfrak{g}
$$

(where we use the [[Einstein summation convention]] throughout). In terms of these coordinates, the [[pullback of differential forms|pullback]] $(e^i)_{i \in I}$ of the Maurer-Cartan form along the [[exponential map]] $exp \,\colon\, \mathfrak{g} \longrightarrow G$
at any point $X = x^i T_i$ is (by [Helgason 2001 Thm. 7.4](#Helgason01), [Meinrenken 2013 Thm. C.2](#Meinrenken13))
$$
    e^i
    \;=\;
    \mathrm{d}x^i
    \left(
      \frac
        {1 - exp(- ad X)}
        {ad X}
      (\partial_k)
    \right)
    \mathrm{d}x^k
$$
where (by [Helgason p. 36](#Helgason01), [Meinrenken p. 99](#Meinrenken13))
$$
  \frac{1 - exp(-A)}{ A }
  \;\;
  \coloneqq
  \;\;
  \sum_{n=0}^\infty
  \tfrac{1}{(n+1)!}
  (-A)^n
$$
(for $A \colon \mathfrak{g} \to \mathfrak{g}$ any [[linear map|linear]] [[endomorphism]]), so that:
$$
  e^i
  \;=\;
  \mathrm{d}x^i
  \left(
    \textstyle{
      \sum_{n = 0}^\infty
    }
    \tfrac{1}{(n+1)!}
    (
      - ad X
    )^n
    (\partial_k)
  \right)
  \mathrm{d}x^k
  \,.
$$
Unwinding this with 
$$
  (ad X)
  \;=\;
  \big(
    x^j
    f^\bullet_{j \bullet}
  \big)
  \,,
$$
(where $f^i_{j k} \in \mathbb{R}$ denote the structure constants in the given basis, such that $[X_j, X_k] = f^i_{j k} X_i$)
we get:
$$
  e^i
    \;=\;
  \mathrm{d}x^i
  -
  \tfrac{1}{2}
  f^i_{j k}x^j \mathrm{d}x^k
  +
  \tfrac{1}{6}
  f^i_{j k'}
  f^{k'}_{k l}
  x^j x^k \mathrm{d}x^l
  + 
  \cdots
  \,.
$$



## On smooth $\infty$-groups {#OnInftyLieGroup}

The theory of [[Lie groups]] embeds into the more general context of [[smooth ∞-groupoid]]s. In this context the Maurer-Cartan form has an (even) more general abstract definition that does not even presuppose the notion of differential form as such:

for every [[smooth ∞-group]] $G \in Smooth\infty Grpd$ with [[delooping]] $\mathbf{B}G$ there is canonically an [[smooth ∞-groupoid]] $\mathbf{\flat}_{dR} \mathbf{B}G$ as described <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#CoeffsLieAlgForms">here</a>. Morphisms $X\to \mathbf{\flat}_{dR}\mathbf{B}G$ correspond to flat $\mathfrak{g}$-valued differential forms on $G$.

This fits into a double [[(∞,1)-pullback]] diagram

$$
  \array{
    G &\to& *
    \\
    {}^{\mathllap{\theta}}\downarrow && \downarrow
    \\
    \mathbf{\flat}_{dR} \mathbf{B}G &\to& \mathbf{\flat} \mathbf{B}G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \,.
$$

The morphism

$$
  \theta : G \to \mathbf{\flat}_{dR}\mathbf{B}G
$$

in this diagram is the $\infty$-Maurer-Cartan form on $G$. For $G$ an ordinary Lie group, this reduces to the above definition. This statement and its proof is spelled out [here](smooth+infinity-groupoid+--+structures#CanonicalFormOnLieGroup).


## On cohesive and stable homotopy types
 {#OnCohesiveHomotopyTypes}

### Definition

Therefore generally for $\mathbf{H}$ a [[cohesive (∞,1)-topos]] and $G \in \mathbf{H}$ an [[∞-group]] object, one may think of 

$$
  \theta \coloneqq fib(\flat \to \mathbf{B})
$$

as the Maurer-Cartan form on [[∞-group]] objects

$$
  \theta_G \;\colon\; G \stackrel{}{\longrightarrow} \flat_{dR}\mathbf{B}G
  \,.
$$

This is discussed at _[[cohesive infinity-topos -- structures]]_ in the section _[Maurer-Cartan forms and curvature characteristics](cohesive+infinity-topos+--+structures#CurvatureCharacteristics)_.

This includes then for instance Maurer-Cartan forms in higher [[supergeometry]] as discussed at _[[Super Gerbes]]_.

### Properties

#### Relation to the Chern character

Given a [[stable homotopy type]] $\hat E$ in [[cohesion]], then the [[shape modality|shape]] of the Maurer-Cartan form plays the role of the _[[Chern character]]_ on $E \coloneqq \Pi(\hat E)$-cohomology.

See at _[[Chern character]]_ for more on this, and see at _[[differential cohomology diagram]]_.


## Related concepts

* [[invariant differential form]]

## References

### General

Named after

* [[Ludwig Maurer]]: _Über allgemeinere Invarianten-Systeme_, Münchener Berichte **18** (1888) 103-150

and 

* [[Élie Cartan]], *Sur la structure des groupes infinis de transformation*, Annales scientifiques de l’É.N.S. 3e série, tome 21 (1904) 153-206 &lbrack;[numdam:ASENS_1904_3_21__153_0](http://www.numdam.org/item?id=ASENS_1904_3_21__153_0)&rbrack;

Further early discussion: 

* [[Friedrich Schur]]: (16) in: *Zur Theorie der endlichen Transformationsgruppen*, Math. Ann. **38** (1891) 263–286 &lbrack;[doi:10.1007/BF01199254](https://doi.org/10.1007/BF01199254)&rbrack;

Introductions in the broader context of [[Cartan geometry]]:

* [[Richard W. Sharpe]], §3 in: *An introduction to Cartan Geometries*, Proceedings of the 21st Winter School "Geometry and Physics", Circolo Matematico di Palermo (2002) 61-75 &lbrack;[eudml:220395](https://eudml.org/doc/220395), [dml:701688](http://dml.cz/dmlcz/701688)&rbrack;

* [[Benjamin McKay]], pp. 3 of: *An introduction to Cartan geometries*, Proceedings of the 21st Winter School "Geometry and Physics", Palermo (2002) &lbrack;[arXiv:2302.14457](https://arxiv.org/abs/2302.14457), [eudml:220395](https://eudml.org/doc/220395)&rbrack;

* Raphaël Alexandre, Elisha Falbel, §3.1.1 in: *Introduction to Cartan geometry* (2023) &lbrack;[pdf](https://webusers.imj-prg.fr/~elisha.falbel/poly.pdf), [pdf](https://webusers.imj-prg.fr/~elisha.falbel/poly.pdf)&rbrack;


See also:

* Wikipedia, *[Maurer-Cartan form](https://en.wikipedia.org/wiki/Maurer%E2%80%93Cartan_form)*

Discussion in [[synthetic differential geometry]]:

*  {#Kock10} [[Anders Kock]], Ex. 3.7.2 & Cor. 6.7.2 in: *Synthetic geometry of manifolds*, Cambridge Tracts in Mathematics **180** (2010) &lbrack;[doi:10.1017/CBO9780511691690](https://doi.org/10.1017/CBO9780511691690), [pdf](https://tildeweb.au.dk/au76680/SGM-final.pdf)&rbrack;

Discussion via [[Lie algebroids]] and [[Lie groupoids]]:

* Anthony D. Blaom, *A characterisation of smooth maps into a homogeneous space*, SIGMA **18** (2022) 029 &lbrack;[arXiv:1702.02717](https://arxiv.org/abs/1702.02717), [doi:10.3842/SIGMA.2022.029](https://doi.org/10.3842/SIGMA.2022.029)&rbrack;

Expression of the Maurer-Cartan form in linear [[coordinates]] on the [[Lie algebra]] $\mathfrak{g}$ after [[pullback of differential forms|pullback]] along the [[exponential map]] $exp \colon \mathfrak{g} \longrightarrow G$:

* {#Helgason01} [[Sigurdur Helgason]], §I.8 in: *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) \[<a href="https://bookstore.ams.org/gsm-34">ams:gsm-34</a>\]

* {#Meinrenken13} [[Eckhard Meinrenken]], Theorem C.2 in Appendix C of: *Clifford algebras and Lie groups*, Ergebn. Mathem. & Grenzgeb., Springer (2013) &lbrack;[doi:10.1007/978-3-642-36216-3](https://doi.org/10.1007/978-3-642-36216-3)&rbrack;


### On coset spaces
 {#ReferencesOnCosetSpaces}

Discussion of MC forms in the generality on [[coset spaces]] ([[homogeneous spaces]]):

* Wikipedia, *[Maurer-Cartan form -- On a homogeneous space](https://en.wikipedia.org/wiki/Maurer%E2%80%93Cartan_form#On_a_homogeneous_space)*

In application to [[first-order formulation of gravity|first-order formulation]] of ([[supergravity|super]]-)[[gravity]]:

* [[Leonardo Castellani]], [[L. J. Romans]], [[Nicholas P. Warner]], *Symmetries of coset spaces and Kaluza-Klein supergravity*, Annals of Physics **157** 2 (1984) 394-407 \[<a href="https://doi.org/10.1016/0003-4916(84)90066-6">doi:10.1016/0003-4916(84)90066-6</a>, [spire:193940](https://inspirehep.net/literature/193940)\]

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], §I.6.6 in: *[[Supergravity and Superstrings - A Geometric Perspective]]*, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), toc: [[CDF91-TOC.pdf:file]], ch I.6: [[CastellaniDAuriaFre-ChI6.pdf:file]]

* {#Castellani01} [[Leonardo Castellani]], *On G/H geometry and its use in M-theory compactifications*, Annals Phys. **287** (2001) 1-13 &lbrack;[arXiv:hep-th/9912277](https://arxiv.org/abs/hep-th/9912277), [doi:10.1006/aphy.2000.6097](https://doi.org/10.1006/aphy.2000.6097)&rbrack;



[[!redirects Maurer-Cartan forms]]

