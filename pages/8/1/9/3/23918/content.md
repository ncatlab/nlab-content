
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
=--
=--

# Contents
* table of contents
{: toc}

## Idea ##

The circumference of a [[circle]] (the [[length]] of the [[curve]] that is the circle) as discussed in geometry. 

## Definition/proposition and proof

+-- {: .num_prop} 
###### Proposition
Depending on which [[circle constant]] you use, given a [[radius]] $r$ of a circle $\mathcal{C}$ in the [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, the circumference of a circle is either $C(r) = \tau r$ or $C(r) = 2 \pi r$. 
=--

### Proof by integration

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

Given any [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, one could select an [[orthonormal basis]] on $\mathbb{R}^2$ by postulating an origin $0$ at the center of the circle $\mathcal{C}$ and two [[orthonormal vectors]] $\hat{i}$ and $\hat{j}$. The circle $\mathcal{C}$ could be parameterized by a function $\overrightarrow{r}:[0, \tau] \to \mathbb{R}^2$ defined as 
$$\overrightarrow{r}(\theta) \coloneqq r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}$$

Then the circumference of $\mathcal{C}$ is given by the following [[integral]]:

$$C(r) = \int_{0}^{\tau} \vert \overrightarrow{r}(\theta) \vert d \theta$$

which evaluates to 

$$C(r) = \int_{0}^{\tau} \vert r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j} \vert d \theta = \int_{0}^{\tau} r((\cos(\theta))^2 + (\sin(\theta))^2) d \theta = \int_{0}^{\tau} r d \theta = \tau r$$
=--

### Proof by limits of regular polygons

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

The perimeter of a [[regular polygon]] $\mathcal{P}_n$ (strictly speaking, a [[regular polygonal line]]) with $n$ sides and [[circumradius]] $r$ is given by the sequence of functions $P_\mathcal{P}:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$

$$P_\mathcal{P}(n)(r) = r (2 n) \sin\left(\frac{\tau}{2n}\right)$$

which [[embedding|embeds]] in the $\mathbb{R}_+$-[[action]] $P_\mathcal{P}^\prime:\mathbb{R}_+ \to (\mathbb{R} \to \mathbb{R})$, defined as

$$P_\mathcal{P}^\prime(n)(r) = r (2 n) \sin\left(\frac{\tau}{2 n}\right)$$

The [[limit of a function|limit]] of $P^\prime$ as $n$ goes to infinity is the circumference of a circle with radius $r$:

$$C(r) = \lim_{n \to \infty} P_\mathcal{P}^\prime(n)(r) = \lim_{n \to \infty} r (2 n) \sin\left(\frac{\tau}{2 n}\right) = r \lim_{m \to 0} \frac{\sin(\tau m)}{m} = r \lim_{m \to 0} \frac{\partial_m \sin(\tau m)}{\partial_m m} = r \lim_{m \to 0} \frac{\tau \cos(\tau m)}{1} = \tau r$$
=--

## See also

* [[pi]]

* [[circle]]

* [[unit circle]]

* [[arc length]]

* [[area of a circle]]

* [[Euclidean space]]