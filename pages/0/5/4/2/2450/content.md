<div class="rightHandSide toc">
[[!include supergeometry - contents]]
</div>



#Contents#

* tic
{:toc}


#Idea#

A _Euclidean supermanifold_ is a [[supermanifold]] that can be thought of as being equipped with a flat [[Riemannian metric]].

Alternatively, it is a [[supermanifold]] for which the transition functions of an [[manifold|atlas]] are restricted to be elements of the [[super Euclidean group]].

#Definition#


A **Euclidean supermanifold** of dimension $(p|q)$is a [[supermanifold]] that is quipped with an **$(X,G)$-structure** , where $X = \mathbb{R}^{p|q}$ and where $G$ is the [[super Euclidean group]] on $\mathbb{R}^{p|q}$.

Here an $(X,G)$-structure is defined as follows.

**Definition** ([[Stephan Stolz|Stolz]], [[Peter Teichner|Teichner]]) A $(X,G)$-structure on a $(d|\delta)$-dimensional [[supermanifold]] $Y$ consists of

* a maximal [[manifold|atlas]] consisting of charts

  $$
    Y \sup_{opn} U_i
    \stackrel{\phi_i}{\to_\simeq}
    V_i \subset_{open} X
  $$

  (where on the left $Y_\red\supset_{open} (U_i)_{red}$) with $O_Y|_{(U_i)_{red} = O_{U_i}}$

* such that the transition function 

  $$
    X \supset \phi_i(U_i \cap U_j) 
    \stackrel{\phi_j \circ \phi_i^{-1}}{\to}
    \phi_j(U_i \cap U_j)
    \subset X
  $$

  is the restriction of a map

  $$
    X \simeq
    X \times pt
    \stackrel{id \times g}{\to}
    X \times G
    \stackrel{action}{\to}
    X
  $$

## family version ##

**definition** A family of $(X,G)$-(complex-, super-)manifolds is a map

$$
  \array{
    Y \\ \downarrow^p \\ S
  }
$$

together with a maximal atlas of charts

$$
  \array{
     Y \supset_{open} U_i &&\stackrel{\phi_i}{\to_\simeq}&&
      V_i \subset_{open} S \times X
     \\
     & \searrow && \swarrow
     \\
     && S
  }
$$

such that the transition maps

$$
  \array{  
     S \times X \supset \phi_i(U_i \times U_j)
     &&\to&&
     \phi_j(U_i \cap U_j)
     \subset S \times X
     \\
     & \searrow && \swarrow
     \\
     && S
  }
$$

are the restriction of a map of the following form 

$$
  S\times X \stackrel{Id \times g \times id}{\to}
  S \times G \times X
  \stackrel{Id \times action}{\to}
$$

for some

$$
  S \stackrel{g}{\to} G
$$

**example** a family $Y \to S$ of $(\mathbb{R}^d, Eucl(\mathbb{R}^d))$-manifolds, for $S$ an ordinary [[manifold]] is a [[submersion]] with flat [[Riemannian metric]] on the [[fiber]]s.

