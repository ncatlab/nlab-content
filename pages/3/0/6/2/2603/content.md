# Contents #

* tic
{: toc}


## Definition ##

A [[multiset]] $\mathcal{X} = \langle X,\mu_X\rangle$ consists of a set $X$ and a function $\mu_X:U\to\mathbb{N}$, where $U$ is a universal set and $\mu_X(e) \gt 0$ if and only if $e\in X$.

We can add two multisets $\mathcal{X} = \langle X,\mu_X\rangle$ and $\mathcal{Y} = \langle Y,\mu_Y\rangle$ to get

$$\mathcal{X} + \mathcal{Y} = \langle X\cup Y,\mu_X+\mu_Y\rangle.$$

Note that we can write

$$k\mathcal{X} = \langle X,k\mu_X\rangle$$

for $k\in\mathbb{N}$.

We can also define an **inner product of multisets** via

$$\langle \mathcal{X},\mathcal{Y}\rangle = \sum_{e\in\mathcal{X}\cup \mathcal{Y}} \mu_X(e) \mu_Y(e).$$

Note that when $\mathcal{X}$ and $\mathcal{Y}$ are simply sets, $\mu_X$ and $\mu_Y$ are the characteristic functions and

$$\langle \mathcal{X},\mathcal{Y}\rangle = |X\cap Y|,$$

where $|\cdot|$ denotes the cardinality of the set.

Using this inner product, we can define the **angle between multisets** as

$$\cos\theta_{\mathcal{X},\mathcal{Y}} = \frac{\langle \mathcal{X},\mathcal{Y}\rangle}{\sqrt{\langle \mathcal{X},\mathcal{X}\rangle \langle \mathcal{Y},\mathcal{Y}\rangle}}.$$

In particular, when $\mathcal{X}=\mathcal{Y}$ we have

$$cos\theta_{{\mathcal{X}},{\mathcal{Y}}} = 1$$

and when $X\cap Y = \emptyset$ we have

$$cos\theta_{{\mathcal{X}},{\mathcal{Y}}} = 0.$$

When $\mathcal{X}$ and $\mathcal{Y}$ are simply sets, the angle between them is given by

$$cos\theta_{{\mathcal{X}},{\mathcal{Y}}} = \frac{|X\cap Y|}{\sqrt{|X||Y|}}.$$

With this notion of addition, the collection of multisets in $U$ becomes the $\mathbb{N}$-[[module]] (that is [[abelian monoid]]) $\mathbb{N}^U$; this inner product makes it an [[inner product space]] analogous to the Banach space $\mathbb{R}^n$. 


## Machine Learning ##

The inner product of multisets is closely related to the "bag of words" kernel in machine learning (see <a href="http://golem.ph.utexas.edu/category/2007/06/kernels_in_machine_learning_ii.html">n-Cafe</a>).

## Related concepts

* [[multiset]]