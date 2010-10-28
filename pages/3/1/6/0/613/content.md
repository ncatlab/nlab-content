
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
* automatic table of contents goes here
{:toc}

## Idea

The _fundamental $\infty$-groupoid_ of a [[topological space]] is the [[∞-groupoid]] whose [[k-morphism]]s are the $k$-dimensional paths in $X$.



## Definition

### General version

+-- {: .un_def}
###### Definition


The **fundamental $\infty$-groupoid** $\Pi(X)$ of a [[topological space]] $X$ is given by the [[Kan complex]] 

$$
  Sing X : [k] \mapsto Hom_{Top}(\Delta^k, X)
$$

which is the [[singular simplicial complex]] of $X$.

=--

+-- {: .un_remark}
###### Remark

This construction is adjoint to [[geometric realization]].

=--

+-- {: .un_remark}
###### Remark

By choosing [[horn]]-fillers this  becomes an [[algebraic Kan complex]]. In terms of these the [[homotopy hypothesis]] has a direct proof, exhibited by a [[Quillen equivalence]]

$$
  Alg Kan \stackrel{\overset{\Pi}{\leftarrow}}{\to} Top
$$

due to ([Nikolaus](#Nikolaus)).

=--

For other models of [[∞Grpd]] there are correspondingly other constructions:

* The definition of [[Trimble n-category]] has the concept of fundamental $n$-groupoid built right into it.


### Strict versions

One can consider [[strict ∞-groupoid]] versions of the fundamental $infty$-groupoid. These lose information about the [[homotopy type]] of the space, though, but are more tractable and may give in some applications all the information that one is interested in. 

The study of strict fundamental $\infty$-groupoids have been pursued by [[Ronnie Brown]] and his school.



There is a strict homotopy 2-groupoid for a Hausdorff space defined by  Hardie, K. A.; Kamps, K. H.; Kieboom, R. W. (MR1785844) and this was later developed into a homotopy double groupoid by Kamps et al. There is no $n$-dimensional version of these ideas on offer. 

A strict cubical omega-groupoid $\rho X_*$ for a [[filtered space]] $X_*$ was defined by Brown and Higgins in 1981. Form the filtered cubical complex $R X_*$ which in dimension $n$ consists of  filtered maps $I^n_* \to X_*$ and take filter homotopy classes of these _relative to the vertices_. The proof that the compositions in $RX_*$ are inherited by $\rho X_*$ is one of the key points of the development. 

It turns out that $\rho X_*$ is equivalent in a clear sense to the crossed complex $\Pi X_*$ defined using relative homotopy groups by Blakers in 1948 (with other terminology) and that the homotopy types modelled by crossed complexes, or by the corresponding globular or cubical gadget, are restricted, essentially to the _linear_ homotopy types, with no quadratic information.  Nonetheless, it is well known in mathematics that linear approximations can be useful. 

Loday's paper of 1982 on _Spaces with finitely many homotopy groups_ introduced the  entirely new idea of a _cubical resolution_ of a space. Some details were completed by Richard Steiner. Loday also introduced the fundamental [[cat-n-group]] of an $n$-cube of spaces. In this way we get a model of a space $X$ by a multiple groupoid in which the $r$-dimensional homotopy of $X$ occurs in the right place in the model. Also you can calculate something with this model, and it has led to new algebraic constructions, such as a nonabelian tensor product of groups, with homotopical applications.  

These strict groupoid models do satisfy the dimension condition. 

## Properties

+-- {: .un_prop}
###### Proposition

The 1-[[truncated|truncation]] of $\Pi X$ is the [[fundamental groupoid]] of $X$:

$$
  \tau_{\leq 1} \Pi X \simeq \Pi_1(X)
  \,.
$$

=--



+-- {: .un_prop}
###### Proposition

For $X$ a [[locally contractible topological space]], the fundamental $\infty$-groupoid $Sing X$ is equivalent to the [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]] of the [[(∞,1)-sheaf (∞,1)-topos]] $(\infty,1)Sh(X)$.  

=--

+-- {: .proof}
###### Proof

Details on this are at [[geometric homotopy groups in an (∞,1)-topos]].

=--

+-- {: .un_remark}
###### Remark

This perspective suggests that when $X$ is not locally contractible, a better replacement for its fundamental $\infty$-groupoid (as usually defined) is the [[shape of an (∞,1)-topos|shape]] of $(\infty,1)Sh(X)$. As discussed there, this coincides with the traditional [[shape theory]] of $X$.

=--

## Related concepts

* [[fundamental groupoid]], **fundamental ∞-groupoid**

* [[fundamental category]], [[fundamental (∞,1)-category]]

* [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] / [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos|of a locally ∞-connected (∞,1)-topos]]

## References

* Hardie, K. A.; Kamps, K. H.; Kieboom, A homotopy 2-groupoid of a Hausdorff space. Papers in honour of Bernhard Banaschewski (Cape Town, 1996). Appl. Categ. Structures 8 (2000), no. 1-2, 209--234. 

* J.-L. Loday, Spaces with finitely many homotopy groups,
J.Pure Appl.  Alg., 24 (1982) 179--202.

* J. M. Casas, G. Ellis, M. Ladra, T. Pirashvili, _Derived functors and the homology of $n$-types_, J. Algebra __256__, 583--598 (2002).

The direct proof of the [[homotopy hypothesis]] for the algebraic version of the fundamental $\infty$-groupoid is in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

Strict versions of fundamental $\infty$-groupoids are discussed in

* [[Ronnie Brown]] et al. _[[Nonabelian Algebraic Topology]]_

See also

* [[Ronnie Brown]] and P.J. Higgins, Colimit theorems for relative homotopy groups, J. Pure Appl. Algebra 22 (1981) 11-41.

*  [[Ronnie Brown]], A new higher homotopy groupoid: the fundamental  globular $\omega$-groupoid of a filtered space, Homotopy, Homology and Applications, 10 (2008), No. 1, pp.327-343.


* R.Steiner, Resolutions of spaces by  $n$-cubes of fibrations, J. London Math. Soc.(2), 34, 169-176, 1986.


[[!redirects fundamental infinity-groupoids]]
[[!redirects fundamental ∞-groupoid]]
[[!redirects fundamental ∞-groupoids]]