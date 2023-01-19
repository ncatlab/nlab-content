
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _fundamental $\infty$-groupoid_  $\Pi_\infty(X)$ of a [[topological space]] $X$ is the [[∞-groupoid]] whose [[k-morphisms]] are the $k$-dimensional paths in $X$. This is the higher refinement of the [[fundamental groupoid]] $\Pi_1(X)$.

It is also sometimes called the _$\infty$-Poincar&#233; groupoid_ of the space, in analogy to the term _[[Poincaré groupoid]]_ for the fundamental groupoid.


## Definition

### General version

The following definition is appropriate if we take a [[Kan complex]] as the definition of $\infty$-groupoid.

+-- {: .num_def}
###### Definition


The **fundamental $\infty$-groupoid** $\Pi(X)$ of a [[topological space]] $X$ is given by the [[Kan complex]] 

$$
  Sing X : [k] \mapsto Hom_{Top}(\Delta^k, X)
$$

which is the [[singular simplicial complex]] of $X$.

=--

+-- {: .num_remark}
###### Remark

This construction is [[right adjoint]] to [[geometric realization]].

=--

+-- {: .num_remark}
###### Remark

By choosing [[horn]]-fillers this  becomes an [[algebraic Kan complex]]. In terms of these the [[homotopy hypothesis]] has a direct proof, exhibited by a [[Quillen equivalence]]

$$
  Alg Kan \stackrel{\overset{\Pi}{\leftarrow}}{\to} Top
$$

due to ([Nikolaus](#Nikolaus)).

=--

+-- {: .num_remark}
###### Remark

One may regard the singular simplicial complex functor as the instance of the general abstract notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] by regarding [[Top]] as a [[cohesive (∞,1)-topos]]. See [[discrete ∞-groupoid]] for more on this.

=--

For other models of [[∞Grpd]] there are correspondingly other constructions:

* The definition of [[Trimble n-category]] has the concept of fundamental $n$-groupoid built right into it.


### Strict versions

One can consider [[strict ∞-groupoid]] versions of the fundamental $\infty$-groupoid. These lose information about the [[homotopy type]] of the space, though, but are more tractable and may give in some applications all the information that one is interested in. 

The study of strict fundamental $\infty$-groupoids have been pursued by [[Ronnie Brown]] and his school.



There is a [[strict 2-groupoid|strict]] homotopy 2-groupoid for a [[Hausdorff space]] defined spring , and a weak homotopy 2-groupoid for a general space (by the same authors). They later introduced  a homotopy double groupoid. There is no $n$-dimensional version of these ideas on offer. 

A strict cubical omega-groupoid $\rho X_*$ for a [[filtered space]] $X_*$ was defined by Brown and Higgins in 1981. Form the filtered cubical complex $R X_*$ which in dimension $n$ consists of  filtered maps $I^n_* \to X_*$ and take filter homotopy classes of these _relative to the vertices_. The proof that the compositions in $RX_*$ are inherited by $\rho X_*$ is one of the key points of the development. 

It turns out that $\rho X_*$ is equivalent in a clear sense to the crossed complex $\Pi X_*$ defined using relative homotopy groups by Blakers in 1948 (with other terminology) and that the homotopy types modelled by crossed complexes, or by the corresponding globular or cubical gadget, are restricted, essentially to the _linear_ homotopy types, with no quadratic information.  Nonetheless, it is well known in mathematics that linear approximations can be useful. 

Loday's paper of 1982 on _Spaces with finitely many homotopy groups_ introduced the  entirely new idea of a _cubical resolution_ of a space. Some details were completed by [[Richard Steiner]]. [[Jean-Louis Loday|Loday]] also introduced the fundamental [[cat-n-group]] of an $n$-cube of spaces. In this way we get a model of a space $X$ by a multiple groupoid in which the $r$-dimensional homotopy of $X$ occurs in the right place in the model. Also you can calculate something with this model, and it has led to new algebraic constructions, such as a nonabelian tensor product of groups, with homotopical applications.  

These strict groupoid models do satisfy the dimension condition. 

## Properties

+-- {: .num_prop}
###### Proposition

The 1-[[truncated|truncation]] of $\Pi X$ is the [[fundamental groupoid]] of $X$:

$$
  \tau_{\leq 1} \Pi X \simeq \Pi_1(X)
  \,.
$$

=--



+-- {: .num_prop}
###### Proposition

For $X$ a [[locally contractible topological space]], the fundamental $\infty$-groupoid $Sing X$ is equivalent to the [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]] of the [[(∞,1)-sheaf (∞,1)-topos]] $(\infty,1)Sh(X)$.  

=--

+-- {: .proof}
###### Proof

Details on this are at [[geometric homotopy groups in an (∞,1)-topos]].

=--

+-- {: .num_remark}
###### Remark

This perspective suggests that when $X$ is not locally contractible, a better replacement for its fundamental $\infty$-groupoid (as usually defined) is the [[shape of an (∞,1)-topos|shape]] of $(\infty,1)Sh(X)$. As discussed there, this coincides with the traditional [[shape theory]] of $X$.

=--

## Related concepts

* [[fundamental groupoid]], **fundamental ∞-groupoid**

* [[fundamental category]], [[fundamental (∞,1)-category]]

* [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]

* [[shape via cohesive path ∞-groupoid]]

## References

The [[fundamental 2-groupoid]]:

as a [[strict 2-groupoid]]:

* [[Keith A. Hardie]], [[Klaus H. Kamps]], [[Rudger Kieboom]], *A homotopy 2-groupoid of a Hausdorff space*. Papers in honour of Bernhard Banaschewski (Cape Town, 1996). Appl. Categ. Structures **8** (2000) 209-234 &lbrack;[doi:10.1023/A:1008758412196](https://doi.org/10.1023/A:1008758412196)&rbrack;

as a [[weak 2-groupoid]]:

* [[Keith A. Hardie]], [[Klaus H. Kamps]], [[Rudger Kieboom]], *A Homotopy Bigroupoid of a Topological Space*, Applied Categorical Structures **9** (2001) 311-327 &lbrack;[doi:10.1023/A:1011270417127](https://doi.org/10.1023/A:1011270417127)&rbrack;

See also:

* [[J.-L. Loday]], *Spaces with finitely many homotopy groups*, J. Pure Appl.  Alg., 24 (1982) 179--202.

* J. M. Casas, G. Ellis, M. Ladra, T. Pirashvili, _Derived functors and the homology of $n$-types_, J. Algebra __256__, 583--598 (2002).

The direct proof of the [[homotopy hypothesis]] for the algebraic version of the fundamental $\infty$-groupoid is in

* {#Nikolaus} [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))


Strict versions of fundamental $\infty$-groupoids are discussed in

* [[Ronnie Brown]] et al. _[[Nonabelian Algebraic Topology]]_

See also

* [[Ronnie Brown]] and [[Philip Higgins]], Colimit theorems for relative homotopy groups, J. Pure Appl. Algebra 22 (1981) 11-41.

*  [[Ronnie Brown]], A new higher homotopy groupoid: the fundamental  globular $\omega$-groupoid of a filtered space, Homotopy, Homology and Applications, 10 (2008), No. 1, pp.327-343.


* [[Richard Steiner]], Resolutions of spaces by  $n$-cubes of fibrations, J. London Math. Soc.(2), 34, 169-176, 1986.


[[!redirects fundamental infinity-groupoids]]
[[!redirects fundamental ∞-groupoid]]
[[!redirects fundamental ∞-groupoids]]

[[!redirects ∞-Poincaré groupoid]]
[[!redirects ∞-Poincaré groupoids]]
[[!redirects infinity-Poincaré groupoid]]
[[!redirects infinity-Poincaré groupoids]]
