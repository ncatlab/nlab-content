
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea ##

The [[bivector]] whose magnitude equals the rate of change at which area is swept out by a particle as it moves along a curve. 

## Definition

Given an $n$-dimensional [[Euclidean space]] $\mathbb{R}^n$, one could select an [[orthonormal basis]] on $\mathbb{R}^n$ by postulating an origin $0$ and a function $\hat{i}:[1, n] \to \mathbb{R}^n$ such that for all $m, p \in [1, n]$ the pair of vectors $\hat{i}_m$ and $\hat{i}_p$ is mutually [[orthonormal]]. There is an [[geometric algebra]] $\mathbb{G}^n$ on $\mathbb{R}^n$ defined by the equations $\hat{i}_m^2 = 1$ for all $m \in [1, n]$, and $\hat{i}_m \hat{i}_p = -\hat{i}_p \hat{i}_m$ for all $m, p \in [1, n]$.  

A curve $\mathcal{C}$ in $\mathbb{R}^n$ could be parameterized by a function $\overrightarrow{r}:\mathbb{R} \to \mathbb{R}^n$. 

Then the **areal velocity**, **sector velocity**, or **sectorial velocity** of a particle traveling along $\mathcal{C}$ in $\mathbb{R}^n$ is given by the bivector-valued function $A:\mathbb{R} \to \langle \mathbb{G}^n \rangle_2$

$$A(t) = \frac{\overrightarrow{r}(t) \wedge \partial_t\overrightarrow{r}(t)}{2}$$

where $a \wedge b$ is the wedge product of two vectors $a$ and $b$.

## In 3 dimensions

In 3 dimensions, the vector areal velocity $\overrightarrow{a}:\mathbb{R} \to \langle \mathbb{G}^n \rangle_1$ is the [[Hodge dual]] of the areal velocity, which is the product of the pseudoscalar 
$$I = \prod_{i:[1, n]} \hat{i}_i$$ 
with the areal velocity:
$$\overrightarrow{a}(t) = I A(t) = I\left(\frac{\overrightarrow{r}(t) \wedge \partial_t\overrightarrow{r}(t)}{2}\right) = \frac{I(\overrightarrow{r}(t) \wedge \partial_t\overrightarrow{r}(t))}{2} = \frac{\overrightarrow{r}(t) \times \partial_t\overrightarrow{r}(t)}{2}$$

## Conservation of areal velocity

Conservation of areal velocity is the same as the conservation of angular momentum. 

## See also

* [[area]]

* [[area of a circle]]

* [[Euclidean space]]

* [[geometric algebra]]

* [[classical mechanics]]

* [[angular momentum]]

* [[torque]]

## References 

See also:

* Wikipedia, _[Areal velocity](https://en.wikipedia.org/wiki/Areal_velocity)_

[[!redirects areal velocities]]
[[!redirects sector velocity]]
[[!redirects sector velocities]]
[[!redirects sectorial velocity]]
[[!redirects sectorial velocities]]