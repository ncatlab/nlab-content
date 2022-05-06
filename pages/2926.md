
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

For $u : \mathbb{R} \to G$ a smooth function and $A \in \Omega^1(\mathbb{R}, \mathfrak{g})$ a Lie-algebra valued form, the condition that $u$ is _flat_ with respect to $u$ is that it satisfies the [[differential equation]]

$$
  d u = -(R_u)_* \circ A
$$

(where $R$ denotes the right multiplication action of $G$ on itself). This is such that if $G$ happens to be a [[matrix Lie group]] it is equivalent to

$$
  (d + A) u = 0
  \,.
$$

We call the unique solution $u $ of this differential equation that satisfies $u(0) = e$ the [[parallel transport]] of $A$ and write it $u = P \exp(\int_0^{(-)} A)$.

Now for $g : \mathbb{R} \to G$ a function, the _gauge transformed_ parallel transport is

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

The [[synthetic differential geometry|synthetic]] view on the Maurer-Cartan form is discussed in

* [[Anders Kock]], _Synthetic geometry of manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

The synthetic Maurer-Cartan form itself appears in example 3.7.2. The synthetic vanishing of its curvature is corollary 6.7.2.

[[!redirects Maurer-Cartan forms]]