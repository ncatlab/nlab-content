
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In [[physics]] the term **gauge transformation** means essentially [[isomorphism]]: the configuration [[space]] of a physical theory is typically a [[groupoid]] (an [[orbifold]]) and a _gauge transformation between configurations_ is a [[morphism]] in this groupoid.

More specifically, in physical theories called [[gauge theory]] -- such as describing [[electromagnetism]] and [[Yang-Mills field]]s -- the configuration space is a space of $G$-[[principal bundle]]s (over [[spacetime]] $X$) with [[connection on a bundle|connection]] over a [[Lie group]] $G$ called the **[[gauge group]]**. A _gauge transformation_ in the strict and original sense of the word is a morphism in the groupoid $G Bund_\nabla(X)$ of these bundles with connection.

In this context the connection $\nabla$ itself -- usually thought of in terms of its local [[Lie-algebra valued 1-form]]s $(A_i \in \Omega^1(U_i \subset X, \mathfrak{g}))$ -- is the _[[gauge field]]_ . The equation

$$
  A'_i = h_i^{-1} A_i h_i + g^{-1} d g_i \;\;\;\; ; \;\; g \in C^\infty(U_i,G)
$$

that characterizes morphisms $A_i \stackrel{g}{\to} A'_i$ in the [[groupoid of Lie-algebra valued forms]] is historically the hallmark of the "gauge principle" and is often what is meant specifically by _gauge transformation_ .

But from there on the terminology generalizes to almost all physical theories. For one this is because the configuration space of many theories may be thought of as spaces of bundles with connections, notably also for [[gravity]]. 

Moreover, many formal physical theories such as [[Chern-Simons theory]], [[supergravity]], etc. are described by [[higher category theory|higher categorical]] generalizations of bundles with connections: [[principal ∞-bundle]]s with [[connection on a principal ∞-bundle]] such as the [[Chern-Simons circle 3-bundle]]. Their configuration spaces form not just groupoids but [[∞-groupoid]]s. The [[higher morphism]]s in these are called **higher gauge transformation**.

For instance the configuration space of the [[Kalb-Ramond field]] is the [[2-groupoid]]  of [[circle n-bundle with connection|circle 2-bundles with connection]] over [[spacetime]]. An object in there is locally given by a 2-form $B_i \in \Omega^2(U_i \subset X)$. A 1-[[morphism]] in there is a **first order gauge transformation** $B_i \stackrel{\lambda}{\to} B'_i$ characterized by the equation $B_i' = B_i + d_{dR} \lambda_i$. A [[2-morphism]] in there is a **second order gauge transformation** $\lambda_i \stackrel{g_i}{\Rightarrow} \lambda'_i$ characterized by $\lambda'_i = \lambda_i + d_{dR} g_i$.


The [[Lie algebroid]] of the groupoid of configurations and gauge transformations is known in pyhsics in terms of its dual [[Chevalley-Eilenberg algebra]] called the [[BRST-complex]]. The degree 1 generators in this [[dg-algebra]] are hence the functions on _[[infinitesimal object|infinitesimal]]_ gauge transformations. (A discussion of such infinitesimal transformations is <a href="http://ncatlab.org/nlab/show/infinity-Lie+algebroid-valued+differential+form#InfGaugeTrafo">here</a>.) These graded functions on infintiesimal gauge transformations are called **ghost fields** or **ghosts** for short, in the physics literature. 

If the space of configurations is not just a groupoid in ordinary spaces but a groupoid in _derived_ spaces such as [[derived smooth manifold]]s, then the corresponding [[derived ∞-Lie algebroid]] is called the [[BV-BRST complex]]. 


## Details

### For local connection forms

The formulas for the local gauge transformations and higher gauge transformations for [[connections on bundles]], [[connections on 2-bundles]] and [[connections on 3-bundles]] are discussed, respectively, at

* [[groupoid of Lie-algebra valued 1-forms]]

* [[2-groupoid of Lie 2-algebra valued forms]]

* [[3-groupoid of Lie 3-algebra valued forms]].

The fully general description for [[connections on ∞-bundles]] is at

* [[∞-groupoid of ∞-Lie-algebra valued forms]].

[[!redirects gauge transformations]]