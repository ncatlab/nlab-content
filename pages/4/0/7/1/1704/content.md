#Idea#


The notion of _principal $\infty$-bundle_ is a [[vertical categorification|categorification]] of [[principal bundle]] from [[group]]s and [[groupoid]]s to [[infinity-groupoid]]s, or rather from parameterized groupoids (generalized spaces called [[stack]]s) to parameterized $\infty$-groupoids (generalized spaces called [[infinity-stack]]s).



For motivation, background and further details see 

* [[motivation for sheaves, cohomology and higher stacks]]
* [[gerbe]]
* [[principal 2-bundle]].

#Definition#

Let $C$ be an [[(infinity,1)-topos]], i.e. an [[(infinity,1)-category of (infinity,1)-sheaves]] whose objects behave as used to from [[topological space]]s, but are actually _parameterized_ topological spaces (for instance [[generalized smooth space|smooth]] spaces), namely [[infinity-stack]]s.

Let $\mathbf{B} G$ be a one-object $\infty$-groupoid in $C$, defining an $\infty$-group $G$. 

Then for $X$ any object in $C$, a $G$-principal $\infty$-bundle $P \to X$ is a [[fibration sequence|homotopy fiber]] of a morphism  $X \to \mathbf{B} G$

$$
  \array{
    P &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{g}{\to}& \mathbf{B} G
  }
$$

for some classifying morphism $g : X \to \mathbf{B} G$.

Notice that $g$ is a cocycle in the [[nonabelian cohomology|nonabelian]] [[cohomology]] on $X$ with coefficients in $G$.

The morphisms of principal $\infty$-bundles are to be such that the [[infinity-groupoid]] $G Bund(X)$ of $G$-principal $\infty$-bundles on $X$ is naturally equivalent to the cocycle $\infty$-groupoid $Hom_C(X, \mathbf{B} G)$

$$
  G Bund(X) \simeq Hom_C(X, \mathbf{B} G)
  \,.
$$

Then this says that $G$-principal bundles are classified by $G$-[[cohomology]]

$$
  G Bund(X)/_\simeq = H(X,\mathbf{B}G) := Ho_C(X, \mathbf{B}G)
$$

given by the [[hom-set]] in the [[homotopy category of an (infinity,1)-category|homotopy category of the (infinity,1)-category]] $C$.

#Connection#

By refining the classifying [[nonabelian cohomology|cocycles]] $g : X \to \mathbf{B} G$ to cocycles 
$\Pi(X) \to \mathbf{B} G$
on higher [[path groupoid]]s of $X$, one obtains higher versions of the notion of [[connection on a bundle]]. This is described in more detail at [[schreiber:Differential Nonabelian Cohomology|Differential Nonabelian Cohomology]].

#References#

The notion of principal $\infty$-bundle (often addressed in the relevant literature in the language of [[torsor]]s) appears in the context of the [[simplicial presheaf]] [[model structure on simplicial presheaves|model]] for generalized spaces in

* Jardine, _Cocycle categories_ ([pdf](http://arxiv.org/abs/math.AT/0605198)) .


An earlier description in terms of simplicial objects is

* P. Glenn, _Realization of cohomology classes in arbitrary exact categories_, J. Pure Appl. Algebra 25, 1982, no. 1, 33--105.

In article not the total space of the bundle $P \to X$ is axiomatized, but the $\infty$-[[action groupoid]] of the action of $G$ on it.

See the remarks at [[principal 2-bundle]].