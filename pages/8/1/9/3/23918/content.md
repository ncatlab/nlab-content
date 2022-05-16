
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
Depending on which circle constant you use, given a [[radius]] $r$ of a circle $\mathcal{C}$ in the [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, the circumference of a circle is either $C = \tau r$ or $C = 2$ [[pi|$\pi$]] $r$. 
=--

+-- {: .proof} 
###### Proof 
In this proof, we are using the [[pi|circle constant]] $\tau = 2 \pi$. 

Given any [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, one could select a [[vector basis]] on $\mathbb{R}^2$ by postulating an origin $0$ at the center of the circle $\mathcal{C}$ and two [[orthonormal vectors]] $\hat{i}$ and $\hat{j}$. The circle $\mathcal{C}$ could be parameterized by a function $f\overrightarrow{r}:[0, \tau] \to \mathbb{R}^2$ defined as 
$$\overrightarrow{r}(\theta) \coloneqq r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}$$

Then the circumference of $\mathcal{C}$ is given by the following [[integral]]:

$$C = \int_{0}^{\tau} \vert \overrightarrow{r}(\theta) \vert d \theta$$

which evaluates to 

$$C = \int_{0}^{\tau} \vert r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j} \vert d \theta = \int_{0}^{\tau} r((\cos(\theta))^2 + (\sin(\theta))^2) d \theta = \int_{0}^{\tau} r d \theta = \tau r$$
=--

## See also

* [[circle]]

* [[unit circle]]

* [[arc length]]

* [[area of a circle]]

* [[Euclidean space]]