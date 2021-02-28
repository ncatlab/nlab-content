
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

> **under construction**



#Contents#
* table of contents
{:toc}


## Idea

Nonabelian Hodge theory generalizes aspects of [[Hodge theory]] from abelian cohomology ([[abelian sheaf cohomology]]) to [[nonabelian cohomology]].

## Nonabelian Hodge theorems

### Nonabelian harmonic sections

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

+-- {: .num_defin}
###### Definition

The **energy** of a [[section]] $\sigma$ of an associated $G/K$-bundle as above is the real number

$$
  E(\phi) := \int_X |d \phi|^2
  \,.
$$

=--

Here 

* $\phi$ is the $\rho$-equivariant map describing the section as above, 


* the [[norm]] is taken with respect to the chocen invariant [[metric]] on $G/K$ 

* and the [[integral]] is taken with respect to the [[Riemannian metric]] on $X$.


+-- {: .num_defn}
###### Definition

Such a $\phi$ is called **harmonic** if it is a [[critical point]] of $E(-)$.

=--


+-- {: .num_theorem}
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

This is due to ([Corlett 88](#Corlette88)).
A version of the proof is reproduced in [Simpson 96, p. 8](#Simpson96)


### K&#228;hler case: Equivalence between Local systems and Higgs bundles
 {#LocalSystemsAndHiggsBundles}

The _nonabelian Hodge theorem_ due to ([Simpson 92](#Simpson92)) establishes, for $X$ a [[compact topological space|compact]] [[Kähler manifold]], an [[equivalence]]
between (irreducible) [[flat vector bundles]] on $X$ and (stable) [[Higgs bundles]] with vanishing [[first Chern class]].

#### Relation to the abelian Hodge theorem

The sense in which the nonabelian Hodge theorem of ([Simpson 92](#Simpson92)) generalizes the abelian [[Hodge theorem]] is the following ([Simpson 92, Introduction](#Simpson92)).

The abelian [[cohomology group]] $H^1(X,\mathbb{C}_{disc})$ classifies [[flat vector bundle|flat]] [[complex line bundles]] whose underlying [[line bundle]] is trivial, hence closed [[differential 1-forms]] modulo 0-forms. The abelian [[Hodge theorem]] gives for this hence the decomposition

$$
  H^1(X,\mathbb{C}_{disc}) 
  \simeq
  H^1(X, \mathcal{O}_X) \oplus H^0(X, \Omega^1_X)
  \,.
$$

It is this kind of relation which is generalized by the nonabelian Hodge theorem. Here one starts instead with the [[nonabelian cohomology]] set $H^1(X, GL_n(\mathbb{C})_{disc})$ which classifies [[flat vector bundle|flat]] [[rank]]-$n$ [[vector bundles]] on $X$, for $n \in \mathbb{N}$. The equivalence to [[Higgs bundles]] gives now a decomposition of these structures into a [[holomorphic vector bundle]] classified by $H^1(X, GL_n(\mathcal{O}_X))$ and a differential 1-form with values in endomorphisms of that, subject to some conditions.

#### Statement

A quick review of the theorem in ([Simpson 92](#Simpson92)) is for instance in ([Raboso 15, section 1.2](#Raboso15)). An elegant abstract reformulation in terms of [[differential cohesion]]/[[D-geometry]], following ([Simpson 96](#Simpson96)) is in ([Raboso 15, section 3.3.1](#Raboso15)):

Analogous to how the [[de Rham stack]] $\int_{inf} X = X_{dR}$ of $X$ is the ([[homotopy quotient|homotopy]]) [[quotient]] of $X$ by the first order [[infinitesimal neighbourhood]] of the [[diagonal]] in $X \times X$, so there is a space ([[stack]]) $X_{Dol}$ which is the formal completion of the 0-section of the [[tangent bundle]] of $X$ ([Simpson 96](#Simpson96)).

Now a [[flat vector bundle]] on $X$ is essentially just a [[vector bundle]] on the [[de Rham stack]] $X_{dR}$, and a [[Higgs bundle]] is essentially just a [[vector bundle]] on $X_{Dol}$. Therefore in this language the nonabelian Hodge theorem reads (for $G$ a linear [[algebraic group]] over $\mathbb{C}$)

$$
  \mathbf{H}(X_{dR}, \mathbf{B}G)
  \simeq
  \mathbf{H}(X_{Dol}, \mathbf{B}G)^{ss,0}
  \,,
$$

where the superscript on the right denotes restriction to semistable Higgs bundles with vanishing [[first Chern class]] (see [Raboso 15, Theorem 3.3](#Raboso15)). 

#### Generalizations to twisted bundles

A generalization of the nonabelian Hodge theorem of ([Simpson 92](#Simpson92)) to [[twisted bundles]] in discussed in ([Raboso 14](#Raboso14)).

## Relation to geometric Langlands

Nonabelian Hodge theory is closely related to the [[geometric Langlands correspondence]]. 

## Related concepts

* [[Hodge structure]]

* [[noncommutative Hodge theory]]

## References

Lecture notes on nonabelian Hodge theory include:

* [[Ron Donagi]], [[Tony Pantev]], _Lectures on the geometric Langlands
conjecture and non-abelian Hodge theory_, 2009 ([pdf](http://www.icmat.es/seminarios/langlands/school/handouts/pantev.pdf))

* [[Alberto García Raboso]], [[Steven Rayan]], _Introduction to Nonabelian Hodge Theory: flat connections, Higgs bundles, and complex variations of Hodge structure_,  Fields Inst. Monogr. 34 (2015), 131--171 ([arXiv](https://arxiv.org/abs/1406.1693)) ([Springer](http://link.springer.com/chapter/10.1007/978-1-4939-2830-9_5))

Corlette's nonabelian Hodge theorem can be found in:

* {#Corlette88} K. Corlette, _Flat $G$-bundles with canonical metric_, J. Diff Geometry 28 (1988)
 
Works by [[Carlos Simpson]] on nonabelian Hodge theory include:

* {#Simpson92} [[Carlos Simpson]], _Higgs bundles and local systems_, Inst. Hautes Etudes Sci. Publ. Math. (1992), no. 75, 5{95. MR 1179076 (94d:32027) ([numdam](http://www.numdam.org/item?id=PMIHES_1992__75__5_0))

* {#Simpson96} [[Carlos Simpson]], _The Hodge filtration on nonabelian cohomology_, Santa Cruz 1995, Proc. Sympos. Pure Math., vol. 62, Amer. Math. Soc., Providence, RI, 1997, pp. 217{281. MR
1492538 (99g:14028) ([arXiv:9604005](http://arxiv.org/abs/alg-geom/9604005))
 

* [[Carlos Simpson]], _Secondary Kodaira-Spencer classes and nonabelian Dolbeault cohomology_ ([arXiv:9712020](http://arxiv.org/abs/alg-geom/9712020))

* [[Carlos Simpson]], _Algebraic aspects of higher nonabelian Hodge theory_ ([arXiv:9902067](http://arxiv.org/abs/math/9902067))

* [[Carlos Simpson]], [[Tony Pantev]], [[Ludmil Katzarkov]], _Nonabelian mixed Hodge structures_ ([arXiv](http://arxiv.org/abs/math/0006213))

The nonabelian Hodge theorem of ([Simpson 92](#Simpson92)) is generalized to [[twisted bundles]] in: 

* {#Raboso15} [[Alberto García Raboso]], _A twisted nonabelian Hodge correspondence_, PhD thesis 2014 ([arXiv:1501.05872](http://arxiv.org/abs/1501.05872), [pdf slides](http://www.math.toronto.edu/agraboso/files/TwistedNAHT_Talk_Handout.pdf))


[[!redirects nonabelian Hodge theorem]]
[[!redirects nonabelian Hodge theorems]]