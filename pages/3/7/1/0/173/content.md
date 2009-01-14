The term "bi-brane" was apparently introduced in

* J&#252;rgen Fuchs, Christoph Schweigert, Konrad Waldorf, _Bi-branes: Target Space Geometry for World Sheet topological Defects_ ([arXiv](http://arxiv.org/abs/hep-th/0703145))

The description below approaches the concept in a slightly more abstract context.


#Idea#

The notion of  [[brane]] and [[bi-brane]] can be made very abstract, but to get the main idea it is useful to start with considering what is usually called the _geometric case_.

Recall for instance from 

* Jacek Brodzki, Varghese Mathai, Jonathan Rosenberg, Richard J. Szabo, _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_ ([arXiv](http://arxiv.org/abs/hep-th/0607020), [blog](http://golem.ph.utexas.edu/string/archives/000879.html))

that a geometric _brane_ on some space $X$ and a bundle gerbe $\mathcal{G}$, regarded as a special kind of 2-vector bundle, on $X$ is

* a map $\iota : Q \to X$

* a morphism $\sigma : 1 \to \iota^* \mathcal{G}$ 
from the trivial 2-vector bundle into the pullback of $\mathcal{G}$ to $Q$, called a _gerbe module_ or _twisted vector bundle_.

If we write this more diagrammatically using that classifying (fiber-assigning) cocycle $g : X \to 2 Vect$ of $\mathcal{G}$, then this data of a brane is a transformation

$$
 \array{
  && Q
  \\
  & \swarrow && \searrow^{\iota}
  \\
  pt &&\stackrel{\sigma}{\Rightarrow}&& X
  \\
  & \searrow &&& \swarrow_{g}
  \\
  && 2 Vect
 }
  \,.
$$


Conceived in this form the notion has an obvious generalizations:

let $X$ and $Y$ be two possibly different spaces with two possibly different 2-vector bundles on them, classified by cocycles $g_1$ and $g_2$, then a bi-brane for this situation is a transformation

$$
 \array{
  && Q
  \\
  & \swarrow && \searrow^{\iota}
  \\
  X &&\stackrel{\bibrane}{\Rightarrow}&& Y
  \\
  & {}_{g_1}\searrow &&& \swarrow_{g_2}
  \\
  && 2 Vect
 }
  \,.
$$

The description of branes in the above diagrammtic form was first given in

* Urs Schreiber, [[Quantum 2-States, Sections of 2-Vector Bundles]], talk at Fields Institute workshop _Higher categories and their applications_ (2007)

and described in more detail in

* Urs Schreiber, Konrad Waldorf, _Connections on Nonabelian Gerbes and their Holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923) [blog](http://golem.ph.utexas.edu/category/2008/08/connections_on_nonabelian_gerb.html)).

The generalization to bi-branes is developed at

* [[schreiber:Nonabelian cocycles and their quantum symmetries]].

This is very closely related to the spans appearing in 

* [[geometric function theory]].

At least some aspects of the concept have more or less implicitly been considered before, notably in the context of  _topological T-duality_. See

* _Mathai on T-duality_:

  * I: [Overview](http://golem.ph.utexas.edu/string/archives/000827.html)

  * II: [T-dual K-classes by Fourier-Mukai](http://golem.ph.utexas.edu/string/archives/000828.html)

for an overview and references.


##Bi-branes motivated from 2d CFT##


[[2-spectral triple|Recall]] that from a 2-dimensional [[conformal field theory|CFT]] one induces a (generalized) _target space_ geometry in generalization of how a [[spectral triple]] induces such a generalized geometry.

From category-algebraic considerations one obtains [[defect line]]s in 2-d [[conformal field theory|CFT]], which are encoded by bimodules as [brane]s are encoded by modules. **Bi-branes** are the answer to the question: "What is the target space structure corresponding to defect lines in the 2d CFT"?

For certain 2-d CFTs based on current algebras the bi-branes corresponding to certain defect lines in these theories have been introduced and discussed in

* J&#252;rgen Fuchs, Christoph Schweigert, Konrad Waldorf, _Bi-branes: Target Space Geometry for World Sheet topological Defects_ ([arXiv](http://arxiv.org/abs/hep-th/0703145))

##In WZW theories##

It is found that, just as symmetric conformal branes in WZW models, whose target space is a Lie group $G$, correspond to 
submanifolds of $G$ given by conjugacy classes in $G$, bi-branes in WZW model correspond to [[span]]s or _correspondences_
$$
  \array{
     && B
     \\
     & \swarrow &&\searrow
      \\
     G &&&& G
  }
$$
where $B$ is a [[higher group character|biconjugacy class]] of $G$.


