
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

The [[area]] enclosed by a [[circle]] as discussed in [[Euclidean geometry]]. 

## Definition/proposition and proofs

Strictly speaking, we are talking about the area of the [[disk]] whose [[boundary]] is the circle; however, the average person usually identifies the interior of a geometric shape with its boundary. 

+-- {: .num_prop} 
###### Proposition
Depending on which [[circle constant]] you use, given a radius $r$ of a circle $\mathcal{C}$ in the [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, the area of a circle is expressed either as $A(r) = \frac{1}{2} \tau r^2$ or as $A(r) = \pi r^2$. 
=--

### Proof by double integration

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

Given any [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, one could select an [[orthonormal basis]] on $\mathbb{R}^2$ by postulating an origin $0$ at the center of the circle $\mathcal{C}$ and two [[orthonormal vectors]] $\hat{i}$ and $\hat{j}$. The circle $\mathcal{C}$ could be parameterized by a function $\overrightarrow{r}:[0, \tau] \times [0, r] \to \mathbb{R}^2$ defined as 
$$\overrightarrow{r}(\rho, \theta) \coloneqq \rho \cos(\theta) \hat{i} + \rho \sin(\theta) \hat{j}$$

Then the area of $\mathcal{C}$ is given by the following [[double integral]]:

$$A(r) = \int_{0}^{r} \int_{0}^{\tau} \vert \overrightarrow{r}(\rho, \theta) \vert d \theta d \rho$$

which evaluates to 

$$A(r) = \int_{0}^{r} \int_{0}^{\tau} \vert \rho \cos(\theta) \hat{i} + \rho \sin(\theta) \hat{j} \vert d \theta d \rho = \int_{0}^{r} \int_{0}^{\tau} \rho((\cos(\theta))^2 + (\sin(\theta))^2) d \theta d \rho = \int_{0}^{r} \int_{0}^{\tau} \rho d \theta d \rho = \int_{0}^{r} \tau \rho d \rho = \frac{1}{2} \tau r$$
=--

### Proof by areal velocity

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

Given any [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, one could select an [[orthonormal basis]] on $\mathbb{R}^2$ by postulating an origin $0$ at the center of the circle $\mathcal{C}$ and two [[orthonormal vectors]] $\hat{i}$ and $\hat{j}$. There is an [[geometric algebra]] $\mathbb{G}^2$ on the vector space defined by the equations $\hat{i}^2 = 1$, $\hat{j}^2 = 1$, and $\hat{i} \hat{j} = -\hat{j} \hat{i}$. 

The circle $\mathcal{C}$ could be parameterized by a function $\overrightarrow{r}:[0, \tau] \to \mathbb{R}^2$ defined as 
$$\overrightarrow{r}(\theta) \coloneqq r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}$$

Then the area of $\mathcal{C}$ is given by integrating the magnitude of the [[areal velocity]]:

$$A(r) = \int_{0}^{\tau} \left|\frac{\overrightarrow{r}(\theta) \wedge \overrightarrow{v}(\theta)}{2}\right| d \theta$$

where $a \wedge b$ is the wedge product of two multivectors $a$ and $b$ and $\overrightarrow{v}$ is the [[velocity]] of a point in $\mathcal{C}$. This expression evaluates to 

$$A(r) = \int_{0}^{\tau} \left|\frac{(r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}) \wedge \partial_\theta (r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j})}{2}\right| d \theta$$
$$A(r) = \int_{0}^{\tau} \left|\frac{(r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}) \wedge (-r \sin(\theta) \hat{i} + r \cos(\theta) \hat{j})}{2}\right| d \theta$$
$$A(r) = \int_{0}^{\tau} \left|\frac{(r (\cos(\theta))^2 \hat{i} \hat{j} + r (\sin(\theta))^2 \hat{i} \hat{j})}{2}\right| d \theta$$
$$A(r) = \int_{0}^{\tau} \left|\frac{r \hat{i} \hat{j}}{2}\right| d \theta = \int_{0}^{\tau} \frac{r}{2} d \theta = \frac{1}{2} \tau r$$
=--

### Proof by action functionals

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

Given any [[Euclidean space|Euclidean]] [[plane]] $\mathbb{R}^2$, one could select an [[orthonormal basis]] on $\mathbb{R}^2$ by postulating an origin $0$ at the center of the circle $\mathcal{C}$ and two [[orthonormal vectors]] $\hat{i}$ and $\hat{j}$. The circle $\mathcal{C}$ could be parameterized by a function $\overrightarrow{r}:[0, \tau] \to \mathbb{R}^2$ defined as 
$$\overrightarrow{r}(\theta) \coloneqq r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j}$$

Then the area of $\mathcal{C}$ is given by the [[action functional]] of the parameterized curve:

$$A(r) = \frac{1}{2} \int_{0}^{\tau} {\vert \overrightarrow{r}(\theta) \vert}^2 d \theta$$

which evaluates to 

$$A(r) = \frac{1}{2} \int_{0}^{\tau} {\vert r \cos(\theta) \hat{i} + r \sin(\theta) \hat{j} \vert}^2 d \theta = \frac{1}{2} \int_{0}^{\tau} (r((\cos(\theta))^2 + (\sin(\theta))^2))^2 d \theta = \frac{1}{2} \int_{0}^{\tau} r^2 d \theta = \frac{1}{2} \tau r$$
=--

### Proof by limits of regular polygons

+-- {: .proof} 
###### Proof 
In this proof, we are using the circle constant $\tau = 2 \pi$. 

The area of a [[regular polygon]] $\mathcal{P}_n$ with $n$ sides and [[circumradius]] $r$ is given by the sequence of functions $P:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$

$$A_\mathcal{P}(n)(r) = \frac{1}{2} r^2 (2 n) \sin\left(\frac{\tau}{2 n}\right)$$

which [[embedding|embeds]] in the $\mathbb{R}_+$-[[action]] $A_\mathcal{P}^\prime:\mathbb{R}_+ \to (\mathbb{R} \to \mathbb{R})$, defined as

$$A_\mathcal{P}^\prime(n)(r) = \frac{1}{2} r^2 (2 n) \sin\left(\frac{\tau}{2n}\right)$$

The [[limit of a function|limit]] of $A_\mathcal{P}^\prime$ as $n$ goes to infinity is the area of a circle with radius $r$:

$$A(r) = \lim_{n \to \infty} A_\mathcal{P}^\prime(n)(r) = \lim_{n \to \infty} \frac{1}{2} r^2 (2 n) \sin\left(\frac{\tau}{n}\right) = \frac{1}{2} r^2 \lim_{m \to 0} \frac{\sin(\tau m)}{m} = \frac{1}{2} r^2 \lim_{m \to 0} \frac{\partial_m \sin(\tau m)}{\partial_m m} = \frac{1}{2} r^2 \lim_{m \to 0} \frac{\tau \cos(\tau m)}{1} = \frac{1}{2} \tau r^2$$
=--

## See also

* [[circle]]

* [[unit circle]]

* [[area]]

* [[circumference of a circle]]

* [[Euclidean space]]

[[!redirects area of a circle]]
