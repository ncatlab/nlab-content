
# Idea #

A _twisted principal-bundle_ is the object classified by a cocycle in [[twisted cohomology]] the way an ordinary [[principal bundle]] is the object classified by a cocycle in plain [[cohomology]] (generally in [[nonabelian cohomology]]).

For $\hat G$ a [[group]], a $\hat G$-[[principal bundle]] is classified in degree 1 [[nonabelian cohomology]] with coefficients in the [[delooping|delooped]] [[groupoid]] $\mathbf{B} \hat G$.

Given a realization of $\hat G$ as an abelian extension 

$$
  A \to \hat G \to G
$$

of groups, i.e. given a [[fibration sequence]]

$$
  \mathbf{B}A \to \mathbf{B}\hat G \to \mathbf{B}G
$$

of [[groupoid]]s such that $\mathbf{B}A$ is once [[delooping|deloopable]] so that the [[fibration sequence]] continues to the right at least one step as

$$
  \mathbf{B}\hat G \to \mathbf{B}G \to \mathbf{B}^2 A
$$


the general nonsense of [[twisted cohomology]] induces a notion of _twisted_ $\hat G$-cohomology. The fibrations classified by this are the twisted $\hat G$-bundles.

# Definition #

For every $\mathbf{B}^2 A$-[[cohomology|cocycle]] $c \in \mathbf{H}(X,\mathbf{B}^2 A)$ the $c$-twisted $\hat G$-cohomology $\mathbf{H}^c(X,\mathbf{G} \hat G)$ is the [[homotopy pullback]]

$$
 \array{
  \mathbf{H}^c(X,\mathbf{B}\hat G)
  &\to&
  {*}
  \\
  \downarrow
  &&
  \downarrow^{c}
  \\
  \mathbf{H}(X,\mathbf{B}G)
  &\stackrel{}{\to}&
  \mathbf{H}(X,\mathbf{B}^2 A)
 }
  \,.
$$

The cocycles in $\mathbf{H}^c(X,\mathbf{B}\hat G)$ are called the (representatives of) $c$-twisted $\hat G$-[[principal bundle]]s.


#Details#

One may unwrap this abstract definition to obtain a concrete cocycle formula for twisted bundles.

For that purpose the above [[homotopy pullback]] is conveniently computed as an ordinary [[pullback]] after making the fibrant replacement

$$
  \array{
    \mathbf{H}(X,\mathbf{B}(A \to \hat G)) 
     &\to & 
    \mathbf{H}(X,\mathbf{B}^2 A)
    &\leftarrow&
    {*}
    \\
    \downarrow^{\simeq}
    &&
    \downarrow^{Id}
    &&
    \downarrow^{Id}
    \\
    \mathbf{H}(X,\mathbf{B}G) 
     &\to & 
    \mathbf{H}(X,\mathbf{B}^2 A)
    &\leftarrow&
    {*}
  }
  \,,
$$

where $(A \to \hat G)$ denotes the [[2-group]] corresponding to the [[crossed module]] obtained from the central extension $\hat G$.

Similarly identifying $\mathbf{B}^2 A = \mathbf{B}(A \to 1)$ as the [[delooping]] of the [[2-group]] coming from the [[crossed module]] $(A \to 1)$
the morphism $\mathbf{H}(X,\mathbf{B}(A \to G)) \to \mathbf{H}(X,\mathbf{B}^2 A)$ is now induced from the obvious projection of [[crossed module]]s

$$
 (A \to G) \to (A \to 1)
 \,.
$$

This then says that $c$-twisted $\mathbf{B}\hat G$-cocycles are precisely those $\mathbf{B}(A \to \hat G)$-cocycles whose projection to an $\mathbf{B}(A\to 1)$-cocycle is the prescribed twisting cocycle $c$.

We may consider a [[Čech cohomology|Čech cocycle]] relative to a cover $\{U_i \to X\}$, i.e. an [[anafunctor]] 

$$
  \array{
    C(U) &\stackrel{\hat g_{tw}}{\to}& 
      \mathbf{B}(A \to \hat G)
    \\
    \downarrow
    \\
    X
  }
$$

out of a [[Čech nerve]] $C(U)$ and notice that the functor $\hat g_{tw}$ is an assignment

$$
  \hat g_{tw}
  \;\;
  :
  \;\;
  \array{
    && (x,j)
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    (x,i)
    &&\to&&
    (x,k)
  }
  \;\;\;\;
  \mapsto
  \;\;\;\;
  \array{
    && \bullet
    \\
    & {}^{\hat g_{i j}(x)}\nearrow 
     &\Downarrow^{c_{i j k}(x)}& 
     \searrow^{\hat g_{j k}(x)}
    \\
    \bullet
    &&\stackrel{\hat g_{i k}(x)}{\to}&&
    \bullet
  }
$$

As already indicated by the notation, the further projection
$$
  C(U) \stackrel{\hat g_{tw}}{\to} 
  \mathbf{B}(A \to \hat G)
  \to 
  \mathbf{B}^2 A
$$

is constrained to be the cocycle $c$. Using the rules for [[crossed module]]s one reads off that the existence of the triangular cell on the right in $\mathbf{B}(A \to \hat G)$ is equivalent to the equation

$$
  \hat g_{i j}(x)
  \hat g_{j k}(x)
  =
  \hat g_{i k}(x)
  c_{i j k}(x)
  \,.
$$

In this cocycle equation form twisted bundles traditionally appear in the literature. Alternatively, allowing a general surjective submersion instead of an open cover, this yields the description of twisted bundles as prefered in the literature on [[bundle gerbe]]s, where they are called [[bundle gerbe module]]s: the $\mathbf{B}^2 A$-cocycle $c$ represents the $A$-bundle gerbe.




# Examples #

## twisted K-theory ##

Just as [[vector bundle]]s model cocycles in [[K-theory]], twisted vector bundles model cocycles in [[twisted K-theory]].

For twists $c$ that are torsion class (i.e. have finite order as group elements in the [[cohomology group]] $H(X,\mathbf{B}^2 A)$ ) this was realized in

* P. Bouwknegt, A. L. Carey, V. Mathai, M. K. Murray, D. Stevenson, _Twisted K-theory and K-theory of bundle gerbes_ ([arXiv](http://arxiv.org/abs/hep-th/0106194))

which also, apparently, is the source where gerbe modules as such were first introduced.

The generalization of this construction to non-torsion twists requires using [[vectorial bundle]]s instead of plain [[vector bundle]]s. Full twisted K-theory in terms of twisted vectorial bundles was realized in

* Kiyonori Gomi, _Twisted K-theory and finite-dimensional approximation_ ([arXiv](http://arxiv.org/abs/0803.2327))

There the twisted cocycle equation discussed above appears on the bottom of page 7.

[[!redirects twisted bundles]]