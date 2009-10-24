
> **under construction**



#Contents#
* automatic table of contents goes here
{:toc}


#Idea#

Nonabelian Hodge theory generalizes aspects of [[Hodge theory]] from abelian cohomology ([[abelian sheaf cohomology]]) to [[nonabelian cohomology]].

# nonabelian Hodge theorem #

Notice or recall (for instance from [[generalized universal bundle]] and [[action groupoid]]) the following equivalent description of [[section]]s of [[associated bundle]]s:

for $G$ a [[group]] with [[action]] $\rho$ on an object $V$ witnessed by the [[action groupoid]] sequence

$$
  V \to V//G \to \mathbf{B}G
$$

the $\rho$-[[associated bundle]] $E \to X$ to a $G$-[[principal bundle]] $P \to X$ classified by an [[anafunctor]] $X \stackrel{\simeq}{\leftarrow} Y  \to \mathbf{B}G$ is the [[pullback]]

$$
  \array{
    E &\to& V//G
    \\
    \downarrow && \downarrow
    \\
    Y &\to& \mathbf{B}G
  }
  \,.
$$

Since this is a [[pullback]] diagram by definition, a glance at a pasting diagram of the form

$$
  \array{
    && E &\to& V//G
    \\
    & \nearrow & \downarrow && \downarrow
    \\
    Y &\stackrel{=}{\to}& Y &\to& \mathbf{B}G
  }
$$

shows that [[section]]s 

$$
  \array{
     && E
     \\
     & {}^{\sigma}\nearrow & \downarrow
     \\
     Y &\stackrel{=}{\to}& Y
  }
$$

are in bijection with maps $Y \to V//G$ that make 

$$
  \array{
    Y &\to& V//G
    \\
    \downarrow^= && \downarrow
    \\
    Y &\to& \mathbf{B}G
  }
$$

commute. 

In the special case that $X$ is a connected [[manifold]] and $G$ a discrete group we can without restriction take $Y = \hat X//\pi_1(X)$ be the [[action groupoid]] of the  [[universal cover]] by the [[fundamental group|homotopy group]], so that the classifying map $Y \to \mathbf{B}G$ is the same as a [[group]] homomorphism 

$$
  \rho : \pi_1(X) \to G
  \,.
$$ 

In that case the above says that a section of the associated bundle is a $\rho$-equivariant map 

$$
  \phi : \hat X \to V
  \,.
$$

This is the way these sections are formulated usually in the literature. The above description has the advantage that it works more generally in [[nonabelian cohomology]] for [[principal bundle]]s generalized to [[principal ∞-bundle]]s.

Next consider furthermore the special case that $V = G/K$ is the [[coset]] [[homogeneous space]] of $G$ quotiented by a subgroup $K$. Then if $G$ is a [[Lie group]] or [[algebraic group]] consider moreover a choice of $G$-invariant metric on the quotient $G/K$. Also consider a [[Riemannian manifold]] structure on $X$.

Then 

+-- {: .un_definition}
###### Definition

The **energy** of a [[section]] $\sigma$ of an associated $G/K$-bundle as above is the real number

$$
  E(\phi) := \int_X |d \phi|^2
  \,.
$$

=--

Here 

* $\phi$ is the $\rho$-equivariant map describing the section as above, 

* the [[norm]] is taken with respect to the chocen invariant metric on $G/K$ 

* and the [[integral]] is taken with respect to the [[Riemannian metric]] on $X$.


+-- {: .un_definition}
###### Definition

Such a $\phi$ is called **harmonic** of it is a critical point of $E(-)$.

=--


+-- {: .un_theorem}
###### Theorem
**(Corlette, generalizing Eells-Sampson)**

If $\rho : \pi_1(X) \to G$  is a representation with

* $G$ a [[reductive group|reductive]] [[algebraic group]] 

* $K$ is a [[maximal compact subgroup]] 
* $\rho(\pi_1(X))$ is 

  * Zariski-dense in $G$ 

  * or its Zariski-closure is itself reductive

then there exists a _harmonic_ section $\phi$ in the above sense.

=--

+-- {: .proof}
###### Proof

A version of the proof is reproduced on p.8 of

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9604005))

=--


#References#

Corlette's nonabelian Hodge theorem is in

* K. Corlette, _Flat $G$-bundles with canonical metric_ J. Diff Geometry 28 (1988)

Work by [[Carlos Simpson]]:

* [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9604005))

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv](http://arxiv.org/abs/alg-geom/9712020))

* [[Carlos Simpson]], _Algebraic aspects of higher nonabelian Hodge theory_ ([arXiv](http://arxiv.org/abs/math/9902067))

* [[Carlos Simpson]], [[Tony Pantev]], [[Ludmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv](http://arxiv.org/abs/math/0006213))

