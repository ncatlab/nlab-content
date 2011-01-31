
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## In representation theory

In [[representation theory]], **Frobenius reciprocity** (sometimes _Frobenious_) is the statement that the [[induction functor]] for [[group representation|representations of groups]] (or in some other [[algebraic categories]]) is [[left adjoint]] to the [[restriction]] functor.

## In category theory

In [[category theory]], Frobenius reciprocity is a condition on a pair of [[adjoint functors]] $f_! \dashv f^*$.  If both categories are [[cartesian closed]], then the adjunction is said to satisfy **Frobenius reciprocity** if the right adjoint $f^*$ is a [[cartesian closed functor]]; that is, if the canonical map $f^*(B^A) \to f^*(B)^{f^*(A)}$ is an [[isomorphism]].

By the calculus of [[mates]], this condition is equivalent to asking that the canonical morphism $f_!(A \times f^*B) \to (f_! A) \times B$ is an isomorphism.  This clearly makes sense if the categories are [[cartesian category|cartesian]] but not [[closed category|closed]], and is the usual formulation found in the literature.

This terminology is most commonly used in the following situations:

* When $f^*$ and $f_!$ are the [[inverse image|inverse]] and [[direct image]] functors along a map $f$ in a [[hyperdoctrine]].  Here $S$ is a category and $P \colon S^{op} \to Cat$ is an $S$-[[indexed category]] such that each category $P X$ is [[cartesian closed]] and each functor $f^* = P f$ has a 
[[left adjoint]] $\exists_f$ (also written $f_!$).  Then $P$ is said to satisfy Frobenius reciprocity, or the **Frobenius condition** , if each of the [[adjunction]]s $\exists_f\dashv f^*$ does.

* When $f^*$ is the [[inverse image]] part of a [[geometric morphism]] between [[(n,1)-topoi]] and $f_!$ is a [[left adjoint]] of it, if the [[adjunction]] $f_!\dashv f^*$ satisfies  Frobenius reciprocity, then the geometric morphism is called [[locally n-connected (n+1,1)-topos|locally (n-1)-connected]].  In particular, if $n=0$ so that we have a [[continuous map]] of [[locales]], then a left adjoint $f_!$ satisfying Frobenius reciprocity makes it at [[open map]], and if $n=1$ so that we have 1-[[topoi]], then it is [[locally connected geometric morphism|locally connected]].

  This usage of "Frobenius reciprocity" is sometimes also extended to the dual situation of [[proper map]]s of locales and topoi.


[[!redirects Frobenius reciprocity]]
[[!redirects Frobenious reciprocity]]
