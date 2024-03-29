
#Contents#
* table of contents
{:toc}

## Idea

A _bi-brane_ is to a [[QFT with defects|defect]] in a [[FQFT]] as a [[brane]] is to a boundary condition.
 
The term "bi-brane" was apparently introduced in

* J&#252;rgen Fuchs, Christoph Schweigert, Konrad Waldorf, _Bi-branes: Target Space Geometry for World Sheet topological Defects_ ([arXiv](http://arxiv.org/abs/hep-th/0703145))

The description below approaches the concept in a slightly more abstract context.



The notion of  [[brane]] and [[bi-brane]] can be made very abstract, but to get the main idea it is useful to start with considering what is usually called the _geometric case_.

Recall for instance from 

* Jacek Brodzki, Varghese Mathai, Jonathan Rosenberg, Richard J. Szabo, _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_ ([arXiv](http://arxiv.org/abs/hep-th/0607020), [blog](http://golem.ph.utexas.edu/string/archives/000879.html))

that a geometric _brane_ on some space $X$ and a bundle gerbe $\mathcal{G}$, regarded as a special kind of 2-vector bundle, on $X$ is

* a map $\iota : Q \to X$

* a morphism $\sigma : 1 \to \iota^* \mathcal{G}$ 
from the trivial 2-vector bundle on $Q$ 
into the pullback of $\mathcal{G}$ to $Q$ -- 
this morphism is called a _gerbe module_ or _twisted vector bundle_.

If we write this more diagrammatically using the classifying (fiber-assigning) cocycle $g : X \to 2 Vect$ of $\mathcal{G}$, then this data of a brane is 
a transformation

$$
 \array{
  && Q
  \\
  & \swarrow && \searrow^{\iota}
  \\
  pt &&\stackrel{\sigma}{\Rightarrow}&& X
  \\
  & \searrow && \swarrow_{g}
  \\
  && 2 Vect
 }
  \,.
$$


Conceived in this form the notion has an obvious generalizations:

let $X$ and $Y$ be two possibly different spaces with two possibly different 2-vector bundles on them, classified by cocycles $g_1$ and $g_2$, then a bi-brane for this situation is 

* a span $ x \stackrel{\iota_1}{\leftarrow} Q 
  \stackrel{\iota_2}{\rightarrow} Y$;

* and a transformation between the two pulled back bundles

$$
 \array{
  && Q
  \\
  & {}^{\iota_1}\swarrow && \searrow^{\iota_2}
  \\
  X &&\stackrel{\bibrane}{\Rightarrow}&& Y
  \\
  & {}_{g_1}\searrow &&& \swarrow_{g_2}
  \\
  && 2 Vect
 }
  \,.
$$

The description of branes in the above diagrammatic form was first given in

* Urs Schreiber, [[quant2states.pdf:file]], talk at Fields Institute workshop _Higher categories and their applications_ (2007)

and described in more detail in

* Urs Schreiber, Konrad Waldorf, _Connections on Nonabelian Gerbes and their Holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923) [blog](http://golem.ph.utexas.edu/category/2008/08/connections_on_nonabelian_gerb.html)).

The generalization to bi-branes is developed at

* [[schreiber:Nonabelian cocycles and their quantum symmetries]].

This is very closely related to the spans appearing in 

* [[geometric function theory]]. 

The relation is discussed a bit at [this blog entry](http://golem.ph.utexas.edu/category/2009/01/benzvi_on_geometric_function_t.html#c021321).

At least some aspects of the concept have more or less implicitly been considered before, notably in the context of  [[topological T-duality]].  A translation of the construction in topological T-duality to the above diagrammatic formulation was originally given [here](http://golem.ph.utexas.edu/category/2007/02/qft_of_charged_nparticle_tdual.html).

The interpretation of T-duality in terms of bi-branes is discussed in more detail in 

* Gor Sarkissian, Christoph Schweigert, _Some remarks on defects and T-duality_ ([arXiv](http://arxiv.org/abs/0810.3159))


##Bi-branes motivated from 2d CFT##


[[2-spectral triple|Recall]] that from a 2-dimensional [[conformal field theory|CFT]] one induces a (generalized) _target space_ geometry in generalization of how a [[spectral triple]] induces such a generalized geometry.

From category-algebraic considerations one obtains [[defect line]]s in 2-d [[conformal field theory|CFT]], which are encoded by bimodules as [brane]s are encoded by modules. **Bi-branes** are the answer to the question: "What is the target space structure corresponding to defect lines in the 2d CFT"?

For certain 2-d CFTs based on current algebras the bi-branes corresponding to certain defect lines in these theories have been introduced and discussed in

* J&#252;rgen Fuchs, Christoph Schweigert, Konrad Waldorf, _Bi-branes: Target Space Geometry for World Sheet topological Defects_ ([arXiv](http://arxiv.org/abs/hep-th/0703145))

##In WZW theories##

In the above article it is found that, just as symmetric conformal branes in WZW models, whose target space is a Lie group $G$, correspond to 
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

## Related concepts

* [[motivic quantization]]

[[!include field theory with boundaries and defects - table]]

## References

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_


[[!redirects bi-branes]]