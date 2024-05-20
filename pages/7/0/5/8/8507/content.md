
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Since generally an _[[equation]]_ is the statement of [[equality]] $\phi(x) = \psi(y)$ of two [[functions]] $\phi$ and $\psi$ of [[variables]] $x$ and $y$, so a _linear equation_ is an equation between [[linear functions]]. 

### In 1-category theory

Typically here a _[[linear function]]_ is taken to mean an _$R$-[[linear map]]_ over some given [[ring]] $R$, hence a [[homomorphism]] $\phi : X \to Z$ or $\psi : Y \to Z$ of $R$-[[modules]] $X, Y, Z \in R$[[Mod]]. If here $Z$ is an $R$-module of [[rank]] greater than 1, one also speaks of a _system of linear equations_.

Specifically if $R = k$ is a [[field]] then these are linear maps of $k$-[[vector spaces]] and hence in this case a linear equation is a statement of equality of two [[vectors]] $\phi(x) = \psi(y)$ in some [[vector space]] $Z$ that depend linearly on vectors $x$ in a vector spaces $X$ and $y \in Y$.

Frequently this is considered specifically for the case that $g$ is a [[constant function]], hence just a fixed [[vector]]. In this case the linear equation becomes $\phi(x) = g$ for $x \in X$. If moreover $\phi$ here is represented or representable by a [[matrix]] this is typically written as

$$
  \phi \cdot\vec x = \vec g
  \,,
$$

which is the form that one finds in standard textbooks on [[linear algebra]]. If $\vec g = 0$ here this is called a _homogeneous linear equation_.

But linear equations make sense and are important in the greater generality where $R$ is not necessarily a field, and in fact in contexts more general than that of $R$-modules even. For instance [[natural isomorphisms]] between [[linear functors]] are a kind of [[categorification]] of linear equations. 

### In $(\infty,1)$-category theory

Indeed, as discussed at _[[equation]]_, in the [[formal logic]] of [[type theory]] a an equation as above is a [[judgement]] of the form

$$
  x : X , y : Y \vdash (\phi(x) = \psi(y)) : Type
$$

whose solution space is the [[dependent sum]]

$$
  Sol \;\; \coloneqq \vdash \sum_{{x : X} \atop {y : Y}} (\phi(x) = \psi(y)) : Type
$$

and reading this in fact in [[homotopy type theory]] says that $X, Y, Sol$ are _[[homotopy types]]_. 

The generalization of a [[ring]] $R$ to a [[homotopy type]] is an _[[E-∞-ring]]_ and that of an $R$-[[module]] $X, Y$ is a _[[module spectrum]]_. 

Accordingly a linear equation in [[homotopy]]([[homotopy type theory|type]]) [[homotopy theory]] is a statement of [[equivalence]] between elements of an $R$-[[module spectrum]] that depend $R$-linearly on other $R$-module spectra. More precisely, as discussed at _[[equation]]_, the solution space to such an "$\infty$-linear equation" is the [[homotopy pullback]]

$$
  \array{
    X \times_Z^\infty Y &\to& Y
    \\
    \downarrow &\swArrow& \downarrow^{\mathrlap{\psi}}
    \\
    X &\underset{\phi}{\to}& Z
  }
$$

in an [[(∞,1)-category]] of $R$-[[∞-modules]].



## Properties

### Solution spaces of homogeneous $R$-linear equations

We discuss solution space of homogeneous linear equations in the general context of [[linear algebra]] over a [[ring]] $R$ (not necessarily a [[field]]).

So let $R$ be a [[ring]] and let $N \in R$[[Mod]] be an $R$-[[module]].

Let $n_0,n_1 \in \mathbb{N}$ and let $K = (K_{i j})$ be an an $n_0 \times n_1$ [[matrix]] with entries in $R$. By [[matrix multiplication]] this defines a [[linear function]]

$$
  K \cdot (-) : N^{n_0} \to N^{n_1}
  \,.
$$

which takes the element $\vec u = (u_1, \cdots, u_{n_0}) \in N^{n_0}$ to the element $K \cdot \vec u$ with

$$
  (K \cdot \vec u)_i = \sum_{j = 1}^{n_0} K_{i j}\cdot u_j
  \,.
$$

Consider dually the linear map

$$
  (-) \cdot K^T : R^{n_1} \to R^{n_0}
$$

on the [[free modules]] over $R$.

Consider the [[quotient]] [[module]] of $R^{n_1}$ by the [[image]] of this map

$$
  R^{n_1}/ (R^{n_0} \cdot K^T)
  \,,
$$

hence the [[cokernel]] of the map, fitting in the [[exact sequence]]

$$
  R^{n_1} \stackrel{(-)\cdot K}{\to} R^{n_0} \to R^{n_1}/(R^{n_1}\cdot K^T)
  \to 0
$$

Here the morphism on the left is also called the inclusion of the [[syzygies]] of the module on the right.

Applying the [[left exact functor|left exact]] [[hom functor]] $Hom_{R Mod}(-,N)$ to this yields [[exact sequence]]

$$
  0 \to Hom_{R Mod}(R^{n_1}/(R^{n_0}\cdot K^T), N)
  \to 
  N^{n_0}
  \stackrel{K \cdot(-)}{\to}
  N^{n_1}
  \,.
$$

This identifies $Hom_{R Mod}(R^{n_1}/(R^{n_0}\cdot K), N)$ as the space of solutions of the _homogeneous_ linear [[equation]] $K \cdot \vec u = 0$.

(...)

### Relation to syzygies and projective resolutions of modules 

For $R$ a [[ring]], there is close relation between

1. $R$-linear equations in finitely many variables;

1. [[generators and relations|finitely generated]] $R$-[[modules]];

1. [[syzygies]] in these $R$-modules

1. and [[projective resolutions]] of these $R$-modules.

These relations we discuss in the following.


(...)

## Related concepts

* [[differential equation]]

* [[matrix calculus]]

* [[determinant]], [[quasideterminant]]

* [[Gaussian elimination]]

## References

Discussion in the context of [[syzygies]] and [[projective resolutions]] of modules is for instance in section 4.5 of 

* [[Pierre Schapira]], _Categories and homological algebra_, lecture notes (2011) ([pdf](http://people.math.jussieu.fr/~schapira/lectnotes/HomAl.pdf))

Linear equations over [[skewfield]]s were studied in

* [[Oystein Ore]], _Linear equations in non-commutative fields_, Ann. Math. __32__:3 (1931) 463--477 [doi](https://doi.org/10.2307/1968245)

and more lately in the theory of [[quasideterminant]]s, see there.


category: algebra

[[!redirects linear equations]]
