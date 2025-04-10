

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _local system_  -- which is short for _local system of [[coefficients]] for [[cohomology]]_ -- is a system of coefficients for [[twisted cohomology]].

Often this is presented or taken to be presented by a [[locally constant sheaf]]. Then cohomology with coefficients in a local system is the corresponding [[sheaf cohomology]].

More generally, we say a _local system_ is a [[locally constant stack]], ... and eventually a [[locally constant ∞-stack]].

Under suitable conditions (if we have [[Galois theory]]) local systems on $X$ correspond to [[functor]]s out of the [[fundamental groupoid]] of $X$, or more generally to [[(∞,1)-functor]]s out of the [[fundamental ∞-groupoid]]. These in turn are equivalently [[flat connections]] (this relation is known as the _[[Riemann-Hilbert correspondence]]_) or generally [[flat ∞-connections]].



## Definitions

A notion of [[cohomology]] exists intrinsically within any [[(∞,1)-topos]]. We discuss local systems first in this generality and then look at special cases, such as local systems as ordinary [[sheaves]].

### General 

For $\mathbf{H}$ an [[(∞,1)-sheaf (∞,1)-topos]], write

$$
  (LConst \dashv \Gamma)
  : 
  \mathbf{H}
   \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

for the [[terminal object|terminal]] [[(∞,1)-geometric morphism]], where $\Gamma$ is the [[global section]] [[(∞,1)-functor]] and $LConst$ the [[constant ∞-stack]]-functor.

Write $\mathcal{S} := core(Fin \infty Grpd) \in $ [[∞Grpd]] for the [[core]] [[∞-groupoid]] of the [[(∞,1)-category]] of finite $\infty$-groupoids. (We can drop the finiteness condition by making use of a higher [[universe]].) This is canonically a [[pointed object]] $* \to \mathcal{S}$, with points the terminal groupoid.


+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}$ an [[object]], a **local system** or _[[locally constant ∞-stack]]_ on $X$ is a morphism

$$
  \tilde \nabla \colon X \longrightarrow LConst \mathcal{S}
$$

in $\mathbf{H}$ or equivalently the object in the [[over-(∞,1)-topos]]

$$
  (P \to X) \in \mathbf{H}/X
$$

that is classified by $\tilde \nabla$ under the [[(∞,1)-Grothendieck construction]]

$$
  \array{
    P &\to& LConst \mathcal{Z}
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\tilde \nabla}{\to}&  LConst \mathcal{S}
  }
$$

In other words, local systems are [[locally constant ∞-stacks]] or equivalently their classifying [[cocycles]] for [[cohomology with constant coefficients]].

=--

(See [[principal ∞-bundle]] for discussion of how [[cocycle]]s $\tilde \nabla : X \to LConst \mathcal{S}$ classify morphisms $P \to X$.)

+-- {: num_remark}
###### Remark

If $\mathbf{H}$ happens to be a [[locally ∞-connected (∞,1)-topos]] in that there is the further [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ 

$$
  (\Pi \dashv LConst \dashv \Gamma) : \mathbf{H} \to \infty Grpd
$$

we call $\Pi(X)$ the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]. In this case, by the adjunction hom-equivalence we have 

$$
  \mathbf{H}(X, LConst \mathcal{S})
  \simeq
  Func(\Pi(X), \mathcal{S})
  \,.
$$

This means that local systems are naturally identified with [[representations]] ($\infty$-[[permutation representation]]s, as it were) of the [[fundamental ∞-groupoid]] $\Pi(X)$:

$$
  Maps(X, LConst \mathcal{S}) \simeq Maps(\Pi(X), \mathcal{S})
  \,.
$$

This is essentially the basic statement around which [[Galois theory]] revolves.

The [[(∞,1)-sheaf (∞,1)-topos]] over a [[locally contractible space]] is locally $\infty$-connected, and many authors identify local systems on such a topological space with representations of its [[fundamental groupoid]].

=--


+-- {: .num_defn}
###### Definition

Given a local system $\tilde \nabla : X \to LConst \mathcal{S}$, the cohomology of $X$ with this **local system of coefficients** is 
the intrinsic [[cohomology]] of the [[over-(∞,1)-topos]] $\mathbf{H}/X$:

  $$
    H(X,\tilde \nabla)
    :=
    \mathbf{H}_{/X}(X, P_{\tilde \nabla})
    \,,
  $$

where $P_{\tilde\nabla}$ is the [[homotopy fiber]] of $\tilde \nabla$.

=--

+-- {: .num_remark}
###### Remark

Unwinding the definitions and using the universality of the [[(∞,1)-pullback]], one sees that a [[cocycle]] $c \in \mathbf{H}(X,\tilde \nabla)$ is a [[diagram]]

$$
  \array{
    X &&\stackrel{c}{\to}&& *
    \\
    & \searrow &\swArrow& \swarrow
    \\
    && LConst \mathcal{S}
  }
$$

in $\mathbf{H}$. This is precisely a [[section]] of the [[locally constant ∞-stack]] $\tilde \nabla$.

=--


### Sheaf-theoretic case

Local systems can also be considered in abelian contexts. One finds the following version of a local system

+-- {: .num_defn}
###### Definition

A **linear local system** is a [[locally constant sheaf]] on a [[topological space]] $X$ (or manifold, analytic manifold, or algebraic variety) whose stalk is a finite-dimensional [[vector space]]. 

=--

Regarded as a sheaf $F$ with values in [[abelian group]]s, such a linear local system serves as the coefficient for [[abelian sheaf cohomology]]. As discussed there, this is in degree $n$ nothing but the intrinsic cohomology of the $\infty$-topos with coefficients in the [[Eilenberg-MacLane object]] $\mathbf{B}^n F$.

+-- {: .num_lemma}
###### Lemma

On a connected topological space this is the same as a sheaf of sections of a finite-dimensional [[vector bundle]] equipped with flat [[connection on a bundle]]; and it also corresponds to the [[representations]] of the [[fundamental group]] $\pi_1(X,x_0)$ in the typical stalk. On an analytic manifold or a variety, there is an equivalence between the category of non-singular coherent 
$D_X$-[[D-module|modules]] and local systems on $X$.

=--



## Related concepts

* [[flat vector bundle]], [[Gauss-Manin connection]]

* [[infinity-local system]]

* [[inner local system]]

* [[simplicial local system]]: within Sullivan's (1977) theory of _Infinitesimal computations in topology_, he refers to 'local systems' several times. This seems to be simplicial in nature. [[simplicial local system|This]] entry explores some of the uses of that notion based on Halperin's lecture notes on minimal models

  * D. Sullivan, _Infinitesimal computations in topology_ ([pdf](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1977__47_/PMIHES_1977__47__269_0/PMIHES_1977__47__269_0.pdf))

* [[twisted cohomology]], [[local coefficient bundle]], [[twisted infinity-bundle]]







## References

An early version of the definition of local system appears in

* [[Norman Steenrod]]: _Homology with local coefficients_, Annals 44 (1943) pp. 610 - 627,

This is before the formal notion of [[sheaf]] was published by [[Jean Leray]].  (Wikipedia's entry on [Sheaf theory](http://en.wikipedia.org/wiki/Sheaf_%28mathematics%29#History) is interesting for its historical perspective on this.)

A definition  appears as an exercise in 

* {#Spanier66} [[Edwin Spanier]], _Algebraic topology_, McGraw Hill (1966), Springer (1982) &lbrack;[doi:10.1007/978-1-4684-9322-1](https://link.springer.com/book/10.1007/978-1-4684-9322-1)&rbrack;

> _A local system on a space $X$ is a [[covariant functor]] from the [[fundamental groupoid]] of $X$ to some [[category]]._ &lbrack;p. 58&rbrack;

Then the first major account with discussion of the relation to [[twisted de Rham cohomology]]:

* {#Deligne70} [[Pierre Deligne]], *Equations différentielles à points singuliers réguliers*, Lecture Notes  Math. **163**, Springer (1970) &lbrack;[publications.ias:355](https://publications.ias.edu/node/355)&rbrack;

Making explicit that instead of the [[fundamental group]] one may use the [[fundamental groupoid]] of the base space:

* [[George W. Whitehead]], p. 257 in: *Elements of Homotopy Theory*, Springer (1978) &lbrack;[doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0)&rbrack;


Textbook accounts:

* {#Voisin02} [[Claire Voisin]] (translated by [[Leila Schneps]]), Section I 9.2.1 of: _[[Hodge theory and Complex algebraic geometry]] I_, Cambridge Stud. in Adv. Math. __76, 77__, 2002/3 ([doi:10.1017/CBO9780511615344](https://doi.org/10.1017/CBO9780511615344))

* [[Alexandru Dimca]], Section 2.5 of: *Sheaves in Topology*, Universitext, Springer (2004) $[$[doi:10.1007/978-3-642-18868-8](https://doi.org/10.1007/978-3-642-18868-8)$]$

* [[Tamás Szamuely]], section 2.6 of: *Galois groups and fundamental groups*, Cambridge Stud. Adv. Math. **117**, Cambridge University Press, (2009) &lbrack;[doi:10.1017/CBO9780511627064](https://doi.org/10.1017/CBO9780511627064)&rbrack;


See also:

* [[Anatoly Libgober]], [[Sergey Yuzvinsky]], *Cohomology of local systems*, Advanced Studies in Pure Mathematics **27**, Mathematics Society of Japan (2000) 169-184 &lbrack;[pdf](http://homepages.math.uic.edu/~libgober/otherpapers/export/2000sergeytokyo.pdf), [doi:10.2969/aspm/02710169](https://doi.org/10.2969/aspm/02710169)&rbrack;

A blog exposition of some aspects of linear local system is developed here:

* [[David Speyer]], _Three ways of looking at a local system_

  * [Introduction and connection to cohomology theories](http://sbseminar.wordpress.com/2009/04/20/three-ways-of-looking-at-a-local-system-introduction-and-connection-to-cohomology-theories/)

  * [the path groupoid approach](http://sbseminar.wordpress.com/2009/04/21/local-systems-the-path-groupoid-approach/)

  * [the infinitesimal perspective](http://sbseminar.wordpress.com/2009/04/30/three-ways-of-looking-at-a-local-system-the-infinitesimal-perspective/)

  * [the infinitesimal site](http://sbseminar.wordpress.com/2009/05/06/the-infinitesimal-site/)


A clear-sighted description of locally constant $(n-1)$-stacks / $n$-local systems as sections of constant $n$-stacks is in

* [[Pietro Polesello]], [[Ingo Waschkies]], *Higher monodromy*, Homology, Homotopy and Applications **7** 1 (2005) 109-150 &lbrack;[arXiv:0407507](http://arxiv.org/abs/math/0407507)&rbrack;

for [[locally constant stacks]] on [[topological space]]s. The above formulation is pretty much the evident generalization of this to general [[(∞,1)-topos]]es.

Discussion of [[Galois representations]] as encoding local systems in [[arithmetic geometry]] includes

* {#Lovering} Tom Lovering, _&#201;tale cohomology and Galois Representations_, 2012 ([pdf](http://tlovering.files.wordpress.com/2012/06/essay-body1.pdf))

See also at _[[function field analogy]]_.

[[!redirects local systems]]

[[!redirects local system of coefficients]]
[[!redirects local systems of coefficients]]


[[!redirects cohomology with a local system of coefficients]]